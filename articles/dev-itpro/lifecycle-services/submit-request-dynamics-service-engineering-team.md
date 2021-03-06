---
title: Dynamics Service Engineering チームへのサービス要求の送信
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して、Dynamics サービス エンジニアリング チームにサービス要求を直接送信する方法について説明します。
author: manalidongre
manager: AnnBe
ms.date: 06/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 254564
ms.assetid: 43ea0eae-34c8-4f97-8c98-c711844534d9
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 77a1643c9b370e01ec48b41d4e1c8ac0d59da8d9
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851819"
---
# <a name="submit-service-requests-to-the-dynamics-service-engineering-team"></a>Dynamics Service Engineering チームへのサービス要求の送信

[!include [banner](../includes/banner.md)]

サービス要求は、Dynamics サービス エンジニア リング (DSE) チームがお客様の環境で事前定義された一連のタスクを実行することを要求するために使用するチケットです。

> [!NOTE]
> 製品問題にサービス要求を使用しないでください。 このトピックに記載されているタスクに適合しない状況が発生した場合は、代わりにサポート チケットを提出します。 サポート チケットの詳細については、[Microsoft Dynamics for Finance and Operations のサポートの検索](lcs-support.md) を参照してください。

Microsoft Dynamics Lifecycle Services (LCS) を使用して、DSE チームにサービス要求を直接送信することができます。 ユーザーの環境でどの要求が送信、実行、およびキャンセルされたか表示することもできます。


## <a name="view-service-requests"></a>サービス要求の表示

サービス要求を表示する方法は 2 つあります。

- プロジェクト ダッシュ ボードの、**環境**セクションで、**サービス要求**を選択します。

    ![サービス要求](./media/submit-service-request-01.png)

- **メニュー** ボタンを選択し、**作業項目** を選択します。 **作業項目**ページで、**サービス要求**タブを選択します。

    ![作業項目](./media/submit-service-request-02.png)

既定では、**作業項目**ページの**サービス要求**タブは現在有効なすべての要求と拒否された要求を一覧表示します。 ただし、フィルター オプションを使用して、キャンセル済みおよびと完了済みの要求を表示することもできます。

![サービス要求リスト](./media/submit-service-request-03.png)

要求を送信した後、ステータスは**要求済**になります。 DSE チームによって要求が処理される前に、**コメント** フィールドにコメントを入力して説明を求める場合があります。 たとえば、実稼働環境の配置を要求する場合、DSE チームからコメントを受け取る場合がありますが、データ センターは、サンド ボックス環境が展開されているデータ センターとは異なります。 コメントを慎重にレビューし、必要な説明をコメントに記入してください。 特定の要求の詳細を表示したり、サービス要求のコメントを送信するには、要求 ID を選択します。

LCS 通知を申し込んだ場合、サービス要求のステータスが変更になる、またはコメントが入力されると、電子メールが表示されます。

DSE チームにサービス要求を提出し、そのアクションがチームの範囲外にある場合、サービス要求は拒否されます。 この場合、拒否の理由と今後の操作の提案が提供されます。 DSE チームが拒否するサービス要求の典型的ないくつかの例については、このトピックで後述の「否されるサービス要求」を参照してください。

## <a name="create-service-requests"></a>サービス要求の作成

サービス要求を作成する方法は、自動とオンデマンドの 2 つの方法があります。

- **自動** - 環境の配置またはパッケージのアプリケーションを要求すると、サービス要求が自動的に作成されます。
- **オンデマンド** – データベース ポイントインタイム復元、およびその他のサービスの要求を入力する場合は、サービス要求を手動で作成します。

### <a name="automatically-create-a-service-request"></a>自動的にサービス要求を作成する

- **環境配置** - 配置オプションを設定し、DSE チームに新しい環境を配置する要求を送信するには、**環境**セクションで**コンフィギュレーション**を選択します。
- **パッケージ アプリケーション** – パッケージを実稼働環境に適用するには、**環境の詳細**ページで、**メンテナンス**を選択し、適用するパッケージを選択してから、**スケジュール**を選択します。 詳細については、[クラウド環境への更新プログラムの適用](../deployment/apply-deployable-package-system.md) を参照してください。

### <a name="create-a-service-request-on-demand"></a>必要に応じたサービス要求を作成する
要求時に作成されたサービス要求は、DSE チームにより明示的に受け入れられません。 DSE チームがリクエストでコメントを入力した場合やリクエストを拒否した場合を除き、指定されたダウンタイム期間で対処されます。 詳細については、サービス要求内でコメントを確認します。

Microsoft は、受信したすべてのサービス要求を頻繁に確認します。 シナリオに適したタイプのサービス要求を選択することにより、DSE チームが適切なタイミングで要求を処理することができます。

1. **作業項目**ページの、**サービス要求**タブで、**追加**を選択します。
2. **要求の作成**ダイアログ ボックスで、作成するサービス要求のタイプを選択します。 ページのオプションは、選択した特定のタイプの要求を反映します。

   - **サンドボックス ポイントインタイム復元要求** - *非実稼働* データベースを特定の時点に復元するには、この要求タイプを選択します。 詳細については、[ポイントインタイム復元要求](../database/request-point-in-time-restore.md) を参照してください。

        > [!NOTE]
        > 切替フェーズで *実稼働* データベースを以前の特定時点に復元する必要がある場合は、**実稼働ポイントインタイム復元要求** タイプを選択してください。 すでに運用中の運用データベースを復元する必要がある場合は、LCS を介してサポート チケットを提出します。

   - **データベース更新の要求** - 実稼動環境からサンドボックス環境に、またはあるサンドボックス環境から別の環境にデータベースを更新するには、この要求タイプを選択します。 詳細については、[サンドボックス データベース更新の要求](../database/database-refresh.md) を参照してください。  *この要求の種類は、2019 年 1 月 31 日に終了*します。

        > [!NOTE]
        > 切替フェーズでサンドボックス環境から実稼働環境にデータベースをリフレッシュする必要がある場合は、**サンドボックスから実稼働** タイプを選択します。

    - **サンドボックスから生産** - 切り替えフェーズで、コンフィギュレーション データの実稼働環境へのデータベース更新を実行します。 詳細については、[Finance and Operations データベースを SQL Server から Azure SQL データベース環境にコピー](../database/copy-database-from-sql-server-to-azure-sql.md#submit-a-service-request-to-copy-the-database) の "データベースのコピーにサービス要求を送信する" セクションを参照してください。

   - **その他の要求** – **その他の要求** タイプをここで説明されているとおりに使用する必要があります。 DSE チームに明確ではない方法でリクエストを言葉で言うと、チームは説明を求めるコメントを入力し、リクエストが遅れます。 下記に記載されていないリクエストに対して**その他の要求**タイプを使用すると、リクエストは拒否されます。 DSE チームが次のアクションのいずれかを実行することを要求するには、この要求タイプを選択します。

      - 実稼動環境でのメンテナンス モードをオンにします。 詳細については、[メンテナンス モード](../sysadmin/maintenance-mode.md) を参照してください。
      - 実稼動環境で明示的なインターネット プロトコル (IP) ホワイト リスト ルールを定義します。
      - "Power BI が有効になっていません" メッセージを受け取った場合に、サンドボックス環境、標準受け入れテスト環境、または実稼働環境で Microsoft Power BI Embedded をアクティブ化することを要求します。 システム管理者に問い合わせてください。


### <a name="commonly-denied-service-requests"></a>一般的に拒否されるサービス要求

拒否されるサービス要求の典型的な例を次に示します。

- 次のいずれかのアクションに対して **その他の要求** タイプの要求を送信しましたが、代わりにサポート チケットを送信する必要がありました。

    - 稼働開始後、または実稼働環境を要求したあと、新しいサブスクリプション見積を有効にする必要があります。
    - Microsoft Dynamics 365 for Finance and Operations 財務諸表のリリース 7.2.6.0 よりも以前のリリースの財務諸表データ マートをリセットする必要があります。
    - go-live 後に、本番データベースを復元する必要があります。
    - DSE チームがアプリケーションのアップグレードを実行した後に、問題が発生しました。

- 別の要求タイプで要求したアクションに対して、**その他の要求** タイプの要求を送信します。 例には、非製造環境のデータベース更新プログラムが含まれます。
- 自身で実行する必要があるアクションに対して、**その他の要求** タイプの要求を送信します。 例には、開発環境のデータベース更新プログラムが含まれます。

## <a name="service-request-types-and-slas"></a>サービス要求のタイプと SLA

| サービス要求のタイプ           | 適用可能な環境 | 要求されたサービス | リード タイム | ダウンタイム |
|--------------------------------|-------------------------|-------------------|-----------|----------|
| 環境配置         | 任意 | 環境配置 | サービス レベル契約 (SLA): 2 営業日以内 | |
| パッケージ アプリケーション            | 生産 | 配置可能パッケージ アプリケーション | 5 時間 | 5 時間 |
| サンドボックスのポイントインタイム復元 | レベル 2 またはそれ以上のサンドボックス | データベース ポイントインタイム復元 | 5 時間 | 4 時間 |
| 実稼働環境のポイントインタイム復元 | 生産 | データベース ポイントインタイム復元 | 5 時間 | 4 時間 |
| サンドボックス環境から実稼働環境          | 第 2 層以上のサンドボックスから実稼働環境 | サンドボックス環境から実稼働環境 | 5 時間 | 4 時間 |
| 外                          | 生産 | メンテナンス モード | 5 時間 | 顧客はサービス要求においていつ環境のメンテナンス モードを再度終了する必要があるかを示しているため、適用不可 |
|                                | 生産 | IP ホワイトリスト ルール | 5 時間 | 2 時間 |
|                                | 生産 | Power BI Embedded | 5 時間 | 2 時間 |

