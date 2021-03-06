---
title: データベースの更新
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースの更新を実行する方法について説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 04/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 257614
ms.assetid: 558598db-937e-4bfe-80c7-a861be021db1
ms.search.region: Global
ms.author: laneswenka
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 231e9687a325bc5840f8d46078f92acb11622c3f
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848163"
---
# <a name="refresh-database"></a>データベースの更新

[!include [banner](../includes/banner.md)]

サンドボックス ユーザー受け入れテスト (UAT) 環境への Dynamics 365 for Finance and Operations のデータベースの更新の実行に Microsoft Dynamics Lifecycle Services (LCS) を使用できます。 データベースの更新対象となるサンド ボックス UAT 環境に、本番環境のトランザクションおよび財務報告データベースをコピーできます。 別のサンドボックス環境を使用する場合は、その環境から対象のサンドボックス UAT 環境にデータベースをコピーすることもできます。

> [!IMPORTANT]
> 生産報告を目的としてサンドボックス環境に生産のデータをコピーすることはできません。

## <a name="self-service-database-refresh"></a>データベースのセルフ サービスエ更新
人手または手動のプロセスに依存しないでお客様にデータ アプリケーション ライフサイクル管理 (*DataALM* とも呼ばれます) 機能を提供することを目標として、Lifecycle Services チームは自動化された**データベースの更新**アクションを導入しました。 このプロセスの概要を以下に示します。

1. **環境の詳細** ページで 対象のサンドボックスを確認し 、メニューオプションの **メンテナンス** \> **データベースの移動** をクリックします。
2. **データベースの選択** オプションを選択し、ソース環境を選択します。
3. 警告に注意し、ソース環境からコピーされていないデータの要素の一覧を確認します。
4. 更新操作がすぐに開始されます。
5. 更新操作が完了したら、パッケージ展開、データベース移動、アップグレードなどの別のサービス操作を実行する前に、工程で**サインオフ**する必要があります。

### <a name="refresh-operation-failed"></a>更新操作が失敗しました
失敗した場合、ロールバックを実行するオプションを使用できます。  工程が最初に失敗した後に**ロールバック** オプションをクリックすると、対象となるサンドボックス環境が更新の開始前の状態に戻されます。 Azure SQL ポイントインタイム復元機能により、データベースを復元できるようになります。 新しく更新されたデータでデータベースの同期を完了できないをターゲット サンドボックスにカスタマイズがある場合は、これがよく必要になります。

失敗の根本原因を特定するには、ロールバック操作を開始する前に、使用可能なボタンを使用して Runbook ログをダウンロードします。

### <a name="data-elements-that-arent-copied-during-refresh"></a>更新中にはコピーされないデータ要素
実稼働環境をサンドボックス環境に、またはサンドボックス環境を別のサンドボックス環境に更新するときは、ターゲット環境にコピーされない特定のデータベース要素があります。 これらの要素として次のものがあります。

* LogisticsElectronicAddress テーブル内の電子メール アドレス。
* BatchJobHistory、BatchHistory、および BatchConstraintHistory テーブルのバッチ ジョブ履歴。
* SysEmailSMTPPassword テーブルの SMTP パスワード。
* SysEmailParameters テーブルの SMTP 中継サーバー。
* PrintMgmtSettings と PrintMgmtDocInstance テーブルの印刷管理設定。
* SysServerConfig、SysServerSessions、SysCorpNetPrinters、SysClientSessions、BatchServerConfig、および BatchServerGroup テーブル内の環境固有のレコード。
* DocuValue テーブル内のドキュメント添付ファイル。
* 管理者以外のすべてのユーザーは **無効** のステータスに設定されます。
* すべてのバッチ ジョブは、 **保留** 状態に設定されます。

これらの要素は、環境固有のものであるためコピーされません。 この例には、BatchServerConfigおよびSysCorpNetPrintersの各レコードが含まれます。 その他の要素は、サポート チケットのデータ量が多くなる懸念があるためコピーされません。 たとえば、簡易メール転送プロトコル (SMTP) はUAT環境でも有効になっているため、重複する電子メールが送信されてしまう可能性があります。また、バッチジョブも有効になっているため、無効な統合メッセージが送信されてしまう可能性もあるため、管理者がポストリフレッシュクリーンアップを行う前にユーザーが有効化されてしまう可能性があります。

### <a name="environment-administrator"></a>環境管理者
対象となる環境のシステム管理者アカウント ('Admin' の UserId) は、ターゲットの web.config file ファイルにある値にリセットされます。  これは、Lifecycle Services の管理者と同じ値になります。  これがどのアカウントになるかをプレビューするには、LCS でターゲット サンドボックスの **環境の詳細** ページにアクセスします。  環境が最初に展開されたときに選択された **環境管理者** フィールドの値は、トランザクション データベース内のシステム管理者となるように更新されます。 これは、環境のテナントが環境管理者のテナントとなることも意味します。

web.config ファイルを別の値に変更するために環境で管理者ユーザー プロビジョニング ツールを使用した場合は、Lifecycle Services の内容と一致しない可能性があります。  別のアカウントを使用することを要求する場合、ターゲット サンドボックスを割り当て解除して削除し、別のアカウントを選択して再展開する必要があります。 この後、データを復元するためにデータベースの更新操作をもう 1 回実行することができます。

### <a name="conditions-of-a-database-refresh"></a>データベース更新の条件
データベース更新の操作の要件および条件の一覧を次に示します。

- パッケージの展開や事前データベース更新など、環境の詳細ページから以前のサービス操作を*サインオフする必要があります*。
- 更新により、ターゲット環境の既存のデータベースが消去されます。 更新が完了すると、既存のデータベースを復元することはできません。
- 更新プロセスが完了するまで、ターゲット環境は使用できなくなります。
- リフレッシュは、Finance and Operations and Financial Reporting データベースにのみ影響します。
- Azure blob storage のドキュメントは、ある環境から別の環境にコピーされません。 つまり、添付されたドキュメント処理ドキュメントとチームプレートは変更されず、現在の状態にとどまります。
- 管理者ユーザー、およびその他の内部サービス ユーザー アカウントを除くすべてのユーザーは使用できなくなります。 このプロセスにより、ほかのユーザーがシステムに復帰する前に管理者ユーザーがデータを削除または難読化できます。
- 管理者ユーザーは、特定のサービスまたは URL に統合エンドポイントを再接続するなど、必要な構成の変更を加える必要があります。
- 定期的なインポートおよびエクスポート ジョブを持つすべてのデータ管理フレームワークは完全に処理され復元が開始される前にターゲット システムで停止する必要があります。 さらに、すべての定期的なインポートおよびエクスポート ジョブが完全に処理された後に、データベースをソースから選択することをお勧めします。 これにより、いずれかのシステムから Azure ストレージにオーファン ファイルが存在しないことが保証されます。 これは、データベースがターゲット環境にリストアされた後にオーファン ファイルを処理できないため重要です。 復元後、統合ジョブを再開することができます。
- LCS でプロジェクト所有者または環境マネージャーのロールを持つユーザーは、すべての非実稼働環境の SQL とマシンの資格情報にアクセスできます。

## <a name="steps-to-complete-after-a-database-refresh-for-environments-that-use-retail-functionality"></a>Retail 機能を使用する環境のデータベース更新後に実行する手順
[!include [environment-reprovision](../includes/environment-reprovision.md)]

## <a name="known-issues"></a>既知の問題

### <a name="refresh-is-denied-for-environments-running-platform-update-12-or-earlier"></a>プラットフォーム アップデート 12 以前を実行する環境で更新が拒否される
Microsoft Dynamics 365 for Finance and Operations 、Enterprise Edition のプラットフォームアップデート 12 (2017年 11月) 更新版 またはそれ以前の環境で動作している場合は、データベース更新の処理を実行することはできません。 詳細は、[現在サポートされているプラットフォーム更新の一覧](../migration-upgrade/versions-update-policy.md)を参照してください。

### <a name="incompatible-version-of-financial-reporting-between-source-and-target-environments"></a>ソース環境とターゲット環境間での財務報告の互換性のないバージョン
実行対象とする環境の財務報告のバージョンが実行元の環境よりも古い場合は、データベースの更新プロセス (セルフサービスまたはサービス要求経由) を正常に完了できません。 この問題を解決するには、両方の環境で財務報告が最新バージョンとなるように更新を行ってください。

実行対象と実行元の環境でインストールしたバージョンを確認するには、 **詳細バージョン情報を表示** のリンクを確認します。これは **環境の詳細** ページにあります。

<img src="media/FinancialReporting_Binaries1.png" width="350px" alt="View detailed version information"><br/>

**MRApplicationService** を検索し、対象となる環境が実行元の環境と同等かそれ以上のバージョンあることを確認してください。

<img src="media/FinancialReporting_Binaries2.png" width="500px" alt="MRApplicationService">

8.1またはそれ以降のバージョンを使用しているお客様
1. **更新** のタイルメニューを開き、UAT環境を更新します。 更新内容をプロジェクトの資産ライブラリに保存します。
2. このパッケージをUAT環境に適用します。
3. エラーが解決されたことを確認してください。

8.0 またはそれ以前のバージョンを使用しているお客様
1. 実行元環境の環境履歴を確認します。 具体的には、「プラットフォームおよびアプリケーションのバイナリ パッケージ」のいずれかが実行元の環境に展開されていることを確認します。対象の環境ではありませんのでご注意ください。
2. このバイナリパッケージをUAT環境に適用します。
3. エラーが解決されたことを確認してください。

### <a name="incompatible-application-versions-between-source-and-target-environments"></a>ソース環境とターゲット環境間での互換性のないアプリケーション バージョン
ソースおよびターゲット環境のアプリケーション リリースが同じでない場合は、データベースの更新プロセス (セルフサービスまたはサービス要求経由) を正常に完了できません。 これは、データ アップグレード プロセスが、更新などのデータベース移動操作によって実行されず、データ損失が発生する可能性があるためです。

新しいアプリケーション バージョンにサンドボックス UAT 環境をアップグレードする場合 (たとえば、7.3 から 8.1)、必ずアップグレードを開始する前にデータベースの更新アクションを実行してください。 サンドボックスが新しいバージョンにアップグレードされると、サンドボックス UAT 環境に古い実稼働環境データベースを復元することはできません。

逆に、実稼働環境がターゲット サンドボックスよりも新しい場合、更新前にターゲット サンドボックスをアップグレードするか、更新の実行前にそのまま割り当て解除、削除、および再展開する必要があります。
