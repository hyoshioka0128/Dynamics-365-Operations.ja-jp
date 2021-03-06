---
title: Azure Event Grid を使用したビジネス イベントの消費
description: このトピックでは、Finance and Operations コネクタを介して Azure イベント グリッドで使用可能となるビジネス イベントに関する情報を提供します。
author: ibenbouzid
manager: AnnBe
ms.date: 07/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: imbenbou
ms.search.validFrom: Platform update 27
ms.dyn365.ops.version: 2019-6-30
ms.openlocfilehash: f9e0a133d300648042af7f9b230121c6e90c7883
ms.sourcegitcommit: 6c4fab381c8974e9aef4421058f31c9917806a45
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/24/2019
ms.locfileid: "1788351"
---
# <a name="consume-business-events-by-using-azure-event-grid"></a>Azure Event Grid を使用したビジネス イベントの消費
[!include[banner](../../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations で Microsoft Azure イベント グリッド エンドポイントを構成する方法と、イベント グリッドからビジネス イベントを消費する方法について説明します。

## <a name="scenario-overview"></a>シナリオの概要

セキュリティのベスト プラクティスでは、接続文字列をアプリケーション外の Azure Key Vault ドライブに保存し、アプリケーションに対して Key Vault キー、シークレット、証明書の適切なアクセス権を付与することをお勧めします。

このアプローチの多くの利点のうち 2 つを次に示します。

- アプリケーション データベースにアクセスできるユーザーは、サードパーティの接続文字列を取得できません。
- 特に複数のアプリケーションが同じリソースにアクセスする場合、更新する必要がある接続文字列が 1 か所だけなのでメンテナンスが簡単です。

完了する必要がある手順の概要を次に示します。

1. 新しいイベント グリッド トピックを作成します。
2. イベント グリッド トピックのキーを格納する新しいキー コンテナーを作成します。
3. Finance and Operations に代わって Key Vault にアクセス権限を持つ Azure アプリを登録します。
4. Finance and Operations エンドポイントのパラメーターを構成します。
5. ビジネス イベントを消費します。

## <a name="procedure-1-create-a-new-event-grid-topic"></a>手順 1: 新しいイベント グリッド トピックを作成します。

1. Azure ポータルにサインインします。
2. **すべてのサービス \> 統合 \> イベント グリッド トピック** を選択します。
3. **追加** を選択して新しいイベント グリッド トピックを作成します。 パラメーターを設定してから **作成** を選択します。 ラボのコンテナーとして新しいリソース グループを作成するか、または既存のリソース グループを使用できます。
4. 配置が完了したら、新しいイベント グリッドを選択します。 プロパティ ブレードで **概要** を選択し、**トピック エンドポイント** 値をメモしておきます。 この値は後で Finance and Operations で必要になります。

    <img alt="Event grid topic" src="../../media/BEF-Howto-EventGrid-03.png" width="70%">

5. プロパティ ブレードに戻って **アクセス キー** を選択して **キー 1** の値をコピーします。 次の手順でキー コンテナーを構成するときに、この値が必要になります。

    <img alt="Event grid access key" src="../../media/BEF-Howto-EventGrid-04.png" width="70%">

## <a name="procedure-2-create-a-key-vault"></a>手順 2: 新しいキー コンテナーの作成

この手順では、前の手順でコピーしたキーを保存する Key Vault を作成します。 Key Vault は、キー、シークレット、証明書を保存するために使用する安全なドライブです。 接続文字列を Finance and Operations に保存する代わりに、より一般的で安全なアプローチは Key Vault に保存することです。 その後、新しいアプリケーションを Azure Active Directory (Azure AD) に登録し、Finance and Operations に代わって Key Vault からシークレットを取得する権限を付与できます。

1. Azure ポータルで **すべてのサービス \> セキュリティ \> Key Vaults** を選択します。
2. リソース グループに新しい Key Vault を作成し、デフォルトのパラメーターを設定します。

    <img alt="New Key Vault" src="../../media/BEF-Howto-Keyvault-02.png" width="50%">

3. **概要** を選択し、Key Vault の **DNS 名** 値をコピーして保存します。 この値は後で使用します。

    <img alt="Key vault DNS name" src="../../media/BEF-Howto-Keyvault-03.png" width="70%">

4. **BE-Key Vault \> シークレット \> 生成/インポート** を選択します。 シークレットの名前を入力し、先に保存した Service Bus 接続文字列を貼り付けます。

    <img alt="Key vault secret " src="../../media/BEF-Howto-Keyvault-04.png" width="70%">

5. **作成**を選択します。

## <a name="procedure-3-register-a-new-application"></a>手順 3: 新しいアプリケーションの登録

この手順では、新しいアプリケーションを Azure AD に登録して、Key Vault のシークレットの読み取りと取得アクセスを許可します。 すると Finance and Operations はこのアプリケーションを使用してイベント グリッドのシークレットを取得します。

1. Azure ポータルで **すべてのサービス \> セキュリティ \> Azure Active Directory** を選択します。
2. **アプリ登録 (プレビュー) \> 新しい登録** を選択し、次にアプリケーションの名前を入力します。
3. **登録** を選択します。
4. 新しいアプリケーションを選択して **証明書とシークレット \> 新しいクライアント シークレット** を選択します。 シークレットの名前を入力し、有効期限が切れないようにシークレットを設定します。 その後 **追加** を選択します。

    <img alt="Azure App secret " src="../../media/BEF-Howto-Keyvault-07.png" width="50%">

5. 新しいシークレットをコピーして保存します。 これは後で使用します。

    > [!IMPORTANT]
    > シークレットは一度だけ表示されます。 シークレットをコピーし忘れた場合は、削除してから新しいシークレットを作成する必要があります。

    <img alt="Copy App secret " src="../../media/BEF-Howto-Keyvault-08.png" width="70%">

6. **概要** を選択し、アプリケーション ID をコピーして保存します。 この値は後で使用します。

    <img alt="Copy App Id " src="../../media/BEF-Howto-Keyvault-09.png" width="70%">

7. **すべてのサービス \> セキュリティ \> Key Vaults** を選択します。
8. 前に作成した Key Vault を選択してから **アクセスポリシー \> 新規追加** を選択します。
9. **プリンシパル** ブレードで、新しい登録済みアプリケーションを選択します。 Key Vault のシークレットを取得するには、**Get** と **List** シークレット アクセス許可のチェック ボックスを選択します。

    <img alt="Key Vault access policy " src="../../media/BEF-Howto-Keyvault-12.png" width="50%">

10. 新しいアクセス ポリシーを保存します。

## <a name="procedure-4-configure-a-business-events-endpoint-in-finance-and-operations"></a>手順 4: Finance and Operationsでビジネス イベント エンドポイントを構成

1. Finance and Operations にサインインします。
2. **システム管理 \> 設定 \> ビジネス イベント** に移動します。
3. **エンドポイント** を選択します。
4. **新規** を選択します。
5. **Azure Event Grid** を選択します。
6. **次へ** を選択します。
7. 必要なパラメーター値を設定します。

    <img alt="Event grid endpoint" src="../../media/BEF-Howto-EventGrid-06.png" width="50%">

8. **OK** を選択します。

## <a name="procedure-5-consume-a-business-event"></a>手順 5: ビジネス イベントの消費

ビジネス シナリオでは、USMF 会社に自由書式の請求書が転記されるたびに電子メール メッセージを送信します。 顧客アカウント番号、顧客名、請求書の合計金額など、詳細がメッセージ`に含まれる必要があります。

1. Finance and Operations でビジネス イベント カタログを選択して **自由書式の請求書が転記されました** ビジネス イベントを探します
2. 次に USMF 会社のビジネス イベントを有効化します。 有効にすると Finance and Operations はテスト メッセージを送信して構成を検証し、接続をキャッシュします。
3. テスト メッセージが受信されたことを確認するには、Azure ポータルでイベント グリッド トピックを選択して **メトリック** を選択します。 **公開されたイベント** メトリックと **一致しないイベント** メトリックの両方が少なくとも **1** の値を示していることを確認します。 そうでない場合は、バッチ ジョブがメッセージを受信するまで待ちます。

    <img alt="Event grid metrics" src="../../media/BEF-Howto-EventGrid-08.png" width="70%">

    両方のメトリックの値が少なくとも **1** の場合、イベント グリッド トピックをサブスクライブする新しいロジック アプリを作成します。

4. **すべてのサービス \> 統合 \> ロジック アプリ** を順に選択します。
5. リソース グループに新しいロジック アプリを作成します。

    <img alt="New logic apps" src="../../media/BEF-Howto-EventGrid-10.png" width="50%">

6. ロジック アプリ リソースを作成したら、空のロジック アプリを作成するオプションを選択します。
7. **イベント グリッド** を検索して **リソース イベントが発生した場合 (プレビュー)** トリガーを選択します。

    <img alt="Event grid trigger" src="../../media/BEF-Howto-EventGrid-11.png" width="50%">

8. サブスクリプションを選択し、リソース タイプとして **Microsoft.EventGrid.Topics** を選択し、手順 1 で作成したイベント グリッド トピックの名前を選択します。

    <img alt="Event grid trigger parameters" src="../../media/BEF-Howto-EventGrid-12.png" width="50%">

9. **新規ステップ** を選択して新しいアクションを追加します。
10. **JSON の解析** データ処理を検索します。 このステップは、Finance and Operations が提供するデータ コントラクトのスキーマを使用してメッセージを解析するために必要です。
11. **Json 解析** アクションの **コンテンツ** フィールドをクリックします。 表示されるウィンドウには前のトリガーからのオプションが表示されます。 Finance and Operations で送信されるペイロードを含むイベント グリッド メッセージの **データ オブジェクト** フィールドを選択する必要があります。

    <img alt="Logic appas parse JSON " src="../../media/BEF-Howto-EventGrid-14.png" width="50%">

    次に Finance and Operations から受け取った契約のスキーマを入力する必要があります。 Finance and Operations はサンプル ペイロードのみを提供します。 ただし、Azure ロジック アプリの機能を使用してペイロードからスキーマを生成できます。

12. Finance and Operations でビジネス イベント カタログのイベントを選択し、**スキーマのダウンロード** リンクを選択します。 テキスト ファイルがダウンロードされます。 テキストファイルを開いて内容をコピーします。
13. ロジック アプリに戻って **サンプル ペイロードを使用してスキーマを生成** リンクを選択します。 テキスト ファイルの内容を貼り付けて **完了** を選択します。

    <img alt="Event schema " src="../../media/BEF-Howto-EventGrid-16.png" width="70%">

14. サンプル ペイロードの品質により、特に実値がサンプル ペイロードで整数として与えられた場合、ジェネレーターは整数と実値を区別しません。 生成されたスキーマを確認して **整数** データ型のフィールドを **数値** データ型に変更する必要があるか判断します。 (JavaScript Object Notation \[JSON\] で **数値** データ型は実数値を表します。)

    <img alt="JSON data types " src="../../media/BEF-Howto-EventGrid-17.png" width="100%">

    次に、顧客の支払いの詳細を含む通知電子メールの送信など、最終的なアクションを選択します。

15. **電子メールの送信** アクションを検索し、自分の Microsoft Office 365 アカウントにサインインします。
16. メッセージの本文および、必須項目を入力します。
17. ロジック アプリを保存します。
18. 顧客の支払いを転記して、ビジネス イベントをトリガーします。 そして、ロジック アプリが実行されていること、顧客の支払いの詳細が記載された電子メールを受信することを確認します。
