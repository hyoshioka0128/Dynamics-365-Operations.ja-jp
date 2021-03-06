---
title: Retail Store Scale Unit のコンフィギュレーションとインストール
description: このトピックでは、セルフ サービスを使用して、小売用バックオフィスで Retail Store Scale Unit を構成し、ダウンロードして、実店舗の 1 台以上のコンピューターにインストールする方法について説明します。
author: jashanno
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SysAADClientTable, RetailCDXDataStore, RetailCDXDataGroup, RetailChannelProfile, RetailSharedParameters, RetailStoreTable
audience: IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail, Core
ms.custom: 219744
ms.assetid: 5e28948f-d40a-40e8-843b-8c2747916546
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cb40f9981ffd1f0e81aa6e67c7b452c1dbe283f9
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833121"
---
# <a name="configure-and-install-retail-store-scale-unit"></a>Retail Store Scale Unit のコンフィギュレーションとインストール

[!include [banner](../includes/banner.md)]

このトピックでは、セルフ サービスを使用して、Microsoft Dynamics 365 for Retail バックオフィスで Retail Store Scale Unit を構成し、ダウンロードして、実店舗の 1 台以上のコンピューターにインストールする方法について説明します。 Retail Store Scale Unit は、Retail チャネル データベース、Retail Async Client、Retail Server、Retail Cloud 販売時点管理 (POS) コンポーネントを組み合わせます。 Microsoft Dynamics 365 for Retail 環境では、これらのコンポーネントが既に提供されています。 ただし、単一コンピューターのセットアップ (既定のオプション) または複数コンピューターのセットアップのいずれかで、ストア内でローカルに動作するように構成できるようになりました。 このトピックは、Retail Store Scale Unit のアンインストールとトラブルシューティングの方法についても説明します。

## <a name="before-you-begin"></a>準備

> [!IMPORTANT]
> 会社全体で高いレベルのセキュリティを維持するために、作成する小売店舗ごとに新しいアプリケーション ID (クライアント ID) とキー (シークレット) を作成することを強くお勧めします。 このステップでは、新しい Web アプリが必要です。

1. アプリケーション ID (クライアント ID) とキー (シークレット) を作成する Microsoft Azure Active Directory (Azure AD) アプリ登録を生成します。 手順については、[Azure Active Directory アプリケーションを作成する](/azure/azure-resource-manager/resource-group-create-service-principal-portal#create-an-azure-active-directory-application) を参照してください。 このトピックでは、Azure ユーザーのアクセス許可と要件を確認し、アプリ登録を生成する方法について説明します。 

> [!IMPORTANT]
> Azure ではなく Active Directory フェデレーション サービスを使用する設置環境で使用する Retail Store Scale Unit をインストールする場合は、設置環境の Retail インストール ドキュメントの手順に従います。 詳細については、[オンプレミス環境での小売チャネルのコンポーネントのインストール手順](../../dev-itpro/deployment/deploy-retail-onprem.md)を参照してください。

2. Retail Store Scale Unit のアプリケーション ID (クライアント ID) とキーが作成された後、クライアント ID を、小売で受け入れる必要があります。 **システム管理** &gt; **設定** &gt; **Azure Active Directory アプリケーション** の順に移動します。 アプリケーション ID (クライアントID) を**クライアント ID** 列に入力し、説明のテキストを**名**列に入力および **RetailServiceAccount** を**ユーザー ID** 列に入力します。

## <a name="configure-a-new-retail-store-scale-unit"></a>新しい Retail Store Scale Unit のコンフィギュレーション

機能する Retail Store Scale Unit を作成するには、「Retail Store Scale Unit インストーラーの実行」の手順に従ってこのトピックのすべてのセクションの手順を実行してください。 構成とインストールを完了するには、まず小売用バックオフィスで初期構成を行う必要があります。 次に、インストールを完了する必要があります。 最後に、Retail Store Scale Unit が正しく動作するよう、コンフィギュレーションを完了する小売用バック オフィスを返す必要があります。

> [!IMPORTANT]
> 設置配置では、次の手順に従います。
>   1. **小売** &gt; **本社の設定** &gt; **小売用スケジューラ** &gt; **チャンネル データベース グループ**の順に移動します。
>   2. アクション ウィンドウで、**新規**を選択します。
>   3. **名前** フィールドに、**既定**と入力します。 必要に応じて、**説明** フィールドに説明を入力します。
>   4. **Retail チャネル スキーマ** フィールドで、**AX7** を選択します。
>   5. **作業フォルダー** フィールドで、**ファイル ストレージ** を選択します。
>   6. アクション ウィンドウで、**保存**を選択します。

1. 小売用バックオフィスで、**小売** &gt; **本社の設定** &gt; **小売用スケジューラ** &gt; **チャネル データベース** に移動します。
2. **チャネル データベース**ページの、アクション ウィンドウで、**新規**を選択します。
3. **チャネル データベース ID** フィールドに、固有の値を入力します。
4. **チャンル データ グループ** フィールドで、**既定**オプションを選択します。 作成されている任意のオプションを選択します。

    > [!IMPORTANT]
    > オンプレミス配置では、この値が前にこのトピックで説明した**既定**値になります。

5. **タイプ** フィールドで、既定値 (**チャネル データベース**) を選択したままにします。
6. **データ同期間隔** フィールドは空白のままにすることができます。 あるいは、このフィールドで値を選択することができます。 たとえば、デモ データでは、**D60-U15** の値が 15 分の同期間隔を指定します。

    **データの同期間隔** 値は、チャネル データベース (Retail Store Scale Unit) および小売用バックオフィス間でデータを同期する頻度を決定します。 値が入力されていない場合は、Retail Store Scale Unit で設定されている既定の間隔が使用されます。 この既定の間隔は、3 分です。

7. **小売チャネル**のクイック タブで、**追加**を選択し、**チャネル フィールド**で、適切な小売店舗のチャンネルを選択します。 このデータベースを使用するすべてのチャンネルを追加するには、この手順を繰り返します。

    また、このデータベースを使用しないチャンネルを追加することもできます。 この方法で、Retail Store Scale Unit のチャネル データベースのチャネルのデータを保持します。 このデータベースを頻繁に使用する Retail 店舗チャネルは、ローカルでそのデータにアクセスできます。
    
    > [!IMPORTANT]
    > オンプレミス配置では、アクション ウィンドウの **ダウンロード** ボタンを選択し、**Retail Store Scale Unit** を選択します。  これにより、既知のエラーが発生し、このドキュメントの次の手順を正しく完了できるように、アップロード ロジックが開始されます。 アップロード ロジックが完了するまで 1 分待ってください。

8. **店舗スケール ユニット パッケージ**クイック タブの、**名前**フィールドで、適切な Retail Store Scale Unit パッケージを選択します。

    各環境では、基本な Retail Store Scale Unit パッケージを生成します。 したがって、このフィールドには常に少なくとも 1 つのオプションが含まれます。

9. アクション ウィンドウで、**保存**を選択します。
10. **小売** &gt; **チャンネル設定** &gt; **チャンネル プロファイル** の順に移動します。
11. アクション ウィンドウで、**新規**を選択します。
12. **名前**フィールドに、チャネル プロセスの一意な名前を入力します。

    > [!IMPORTANT]
    > オンプレミス配置の場合、このフィールドにはどのような値も入力できますが、 **既定** の値は一般となります。

13. アクション ウィンドウで、**保存**を選択します。
14. 新しいチャネル プロファイルの**プロファイルのプロパティ**クイック タブで、**追加**を選択します。
15. **プロパティ キー** フィールドで、**Retail サーバー URL** を選択します。
16. **プロパティ値**フィールドに、Retail Store Scale Unit にインストールする必要のある Retail サーバーの URL を入力します。

    Retail サーバーの URL の標準形式は、**https://&lt;コンピューター名&gt;:&lt;ポート&gt;/RetailServer/Commerce** です。 この形式で、**&lt;コンピューター名&gt;** は Retail Store Scale Unit がインストールされているコンピューター、またはドメイン、フル コンピューター名に結合されていないシステムの完全修飾ドメイン名 (FQDN) のどちらかです。 **&lt;ポート&gt;** はインストールに使用するポート番号です。 ポート番号は、 1 ～ 65535 の範囲の値である必要があります。 既定の HTTPS ポート (443) を使用している場合、ポート番号を指定する必要はありません。

17. 新しいチャネル プロファイルの**プロファイルのプロパティ**クイック タブで、**追加**を選択します。
18. **プロパティ キー** フィールドで、**クラウド POS URL** を選択します。
19. **プロパティ値**フィールドに、Retail Store Scale Unit にインストールする必要のある Retail Cloud POS インスタンスの URL を入力します。

    クラウド POS の URL の標準形式は、**https://&lt;コンピューター名&gt;:&lt;ポート&gt;/POS** です。 この形式で、**&lt;コンピューター名&gt;** は Retail Store Scale Unit がインストールされているコンピューター、またはドメイン、フル コンピューター名に結合されていないシステムの FQDN のどちらかです。 **&lt;ポート&gt;** はインストールに使用するポート番号です。 ポート番号は、 1 ～ 65535 の範囲の値である必要があります。 既定の HTTPS ポート (443) を使用している場合、ポート番号を指定する必要はありません。

20. アクション ウィンドウで、**保存**を選択します。

    > [!NOTE]
    > メディアがよく使用される場合、プロファイルの **メディア サーバー ベース URL** を生成する必要があります。  テストとわかりやすくするために、**既定の**チャネル プロファイルに存在する URL を再利用できます。 
    >
    > オンプレミス配置では、**メディア サーバー ベースの URL** は、POS デバイスのすべてのメディアが格納されている場所になります。  

21. **小売** &gt; **チャンネル** &gt; **小売店舗** &gt; **すべての小売店舗**の順に移動します。
22. 新しいチャネル データベースを使用する小売店の小売チャネル ID を選択します。
23. 選択したストアの詳細ページにある、アクション ウィンドウで、**編集**を選択します。
24. 店舗の**一般**クイック タブの、**ライブ チャネル データベース**フィールドで、手順 3 で作成したチャネル データベースを選択します。
25. アクション ウィンドウで、**保存**を選択します。
26. 店舗の**一般**クイック タブの、**チャネル プロファイル**フィールドで、手順 12 で作成したチャネル プロファイルを選択します。
27. **小売** &gt; **本社の設定** &gt; **小売用スケジューラ** &gt; **チャンネル データ グループ**の順に移動します。
28. **既定** データ グループを選択した後、アクション ウィンドウで、**完全データ同期** を選択します。**配送スケジュールの選択** のフィールドで、ジョブ **9999** を選択し、**OK** を選択します。 表示されるダイアログ ボックスで、**OK** を選択して完全同期を確認します。 チャンネル データベース内のすべてのデータはダウンロードの準備をします。

    > [!NOTE]
    > 最初の Retail Store Scale Unit を作成したら、チャネル データ グループではなくチャンネル データベースからの完全なデータ同期を実行するために必要なデータ生成が少なくなります。
    
    > [!IMPORTANT]
    > オンプレミス配置の場合、 **既定** のチャンネルのデータ グループはありません。  新しいデータ グループを作成します (そしてそれをチャネル データベースとディストリビューション スケジュールジョブに関連付けます)。

### <a name="download-the-retail-store-scale-unit-installer"></a>Retail Store Scale Unit インストーラーをダウンロードします。

1. 小売用バックオフィスで、**小売** &gt; **本社の設定** &gt; **小売用スケジューラ** &gt; **チャネル データベース** に移動します。
2. 左のチャネル データベースの一覧で、以前に作成したチャネル データベースを選択します。
3. アクション ウィンドウで、**ダウンロード**を選択します。
4. ドロップダウン メニューで、**コンフィギュレーション ファイル**を選択します。

    > [!NOTE]
    > Retail Store Scale Unit インストーラーが構成ファイル (XML ファイル) を正しく使用するためには、構成ファイルをインストーラと同じ場所に保存する必要があります。
    >
    > オンプレミス配置では、構成ファイル (この時点で) を手動で編集する必要があります。
    > - StoreSystemAosUrl には、Headquarters (AX) へのアクセスに使用される値が必要です。  この URL の末尾にスラッシュを保持することが重要です (たとえば、**https://myContosoURL.com/namespaces/AXSF/**)。
    > - AADTokenIssuerPrefix には値 **https://NOTUSED.microsoft.com** が必要です
    > - TransactionServiceAzureAuthority には値 **https://<ADFS FQDN (.com を含む)>/adfs** が必要です。
    > - TransactionServiceAzureResourceには、上記のように編集された **StoreSystemAosUrl** のベースURL値が必要です。 たとえば、上記の例では **https://myContosoURL.com** が値として使用され、URLの **/namespaces/AXSF/** 部分が削除されます。

5. Internet Explorer ウィンドウの下部に表示される通知バーで、**保存**を選択します。 (通知バーは、他のブラウザでは別の場所に表示される場合があります。)

    ブラウザーは、生成されたダウンロード ポップアップをブロックする可能性があります。 **1 回許可** または **このサイトのオプション** &gt; **常に許可** を選択します。 その後、再度 **ダウンロード** を選択します。

6. アクション ウィンドウで、**ダウンロード**を選択します。
7. ドロップダウン メニューで、**Retail Store Scale Unit パッケージ**を選択します。
8. Internet Explorer ウィンドウの下部に表示される通知バーで、**保存**を選択します。 (通知バーは、他のブラウザでは別の場所に表示される場合があります。)

    選択したチャネル データベースの Retail Store Scale Unit パッケージに基づいて、適切なパッケージがダウンロード用に自動的に選択されます。

9. セットアップ インストーラが保存されたら、通知バーの、**実行**を選択します。 (この手順はブラウザの種類によって異なる場合があります。)

### <a name="run-the-retail-store-scale-unit-installer"></a>Retail Store Scale Unit インストーラーを実行

> [!NOTE]
> Retail Cloud POS をインストールし、使用する場合は、次の手順に従って、インストーラーを初めて実行するときに構成を初期化する必要があります。

Retail Store Scale Unit インストーラーを実行する前に、すべての [システム要件](../../fin-and-ops/get-started/system-requirements.md) が満たされていることを確認してください。 

> [!IMPORTANT]
> オンプレミス環境で使用する Retail Store Scale Unit をインストールする場合は、次のように、管理者権限を使用して、コマンド ラインから起動する必要があります: StoreSystemSetup.exe -UseAdfsAuthentication

Retail Store Scale Unit インストーラーが最初に関連付けられているファイルを展開します。 インストールを開始します。

1. インストーラーの最初のページで、インストールするコンポーネントを選択します。 次のコンポーネントをインストールすることができます。

   - 小売チャンネル データベースと非同期クライアント
   - Retail サーバー
   - 小売クラウド POS

     > [!NOTE]
     > - Retail Cloud POS をインストールするには、Retail Server も選択してインストールする必要があります。 店舗内で Retail Modern POS のみを使用する場合は、**Retail Cloud POS** チェック ボックスをオフにして、ここで説明されているようにインストール プロセスを続行します。
     > - 既定では、インストーラーはすべてのコンポーネントを 1 台のコンピュータにインストールします。 複数のコンピューターにコンポーネントをインストールするには、追加の手動手順を完了する必要があります。 詳細については、「複数のコンピューターのインストール」セクションを参照してください。

     インストールするすべてのコンポーネントを選択した後、**次**を選択して続行します。

2. インストーラーは、すべての前提条件が満たされていることを検証します。 Microsoft SQL Server の有効なバージョンが見つからない場合は、インストーラーが、Microsoft SQL Server 2014 with Service Pack 2 をダウンロードし、インストールします。

    > [!NOTE]
    > - この前提条件を満たすためには、SQL Server に全文検索機能を搭載し、最低限トランスポート層セキュリティ (TLS) 1.2 がサポートされている必要があります。 Microsoft SQL Server 2012 では、最低でも、Service Pack 3 がインストールされる必要があります。 Microsoft SQL Server 2014 では、Service Pack 2 がインストールされている必要があります。
    > - システムの再起動が必要な場合、インストーラーはユーザーにプロンプトを表示します。  この確認は、再起動が必要かどうかをすべてのアプリケーションに通知する Windows システム レジストリ キーに基づいています。  インストールを続行する前に再起動することをお勧めしますが、再起動は必須ではなく、インストーラーはコンピュータを再起動せずに続行することができます。

3. Application Object Server (AOS) の URL を確認し、**次へ** を選択します。 (AOS URL とは、小売用バックオフィスにアクセスするために使用される URL のことです。)

    > [!NOTE]
    > Retail Server URL は、構成ファイルから自動的に入力されます。

4. HTTPS 通信に使用する、有効な Secure Sockets Layer (SSL) 証明書を選択します。

    証明書は秘密キー ストレージを使用する必要があり、サーバー認証は拡張キー使用プロパティにリストされている必要があります。 また、証明書はローカルに信頼される必要があり、期限切れにすることはできません。 ローカル コンピューターの個人用証明書格納場所に保存する必要があります。

5. 特定のユーザーが必要な場合は、アプリケーション プールを実行するために必要なユーザー名とパスワードを入力します。 既定では、インストーラーは自動的に使用するサービス アカウントを生成します。 この方法は、安全性がより向上するためお勧めします。

    > [!NOTE]
    > 最初から用意されているサービス アカウントは、他のすべてのアカウントに定義されているのと同じパスワード ポリシー下で引き続き機能する点に留意することは重要です。  つまり、最小限のパスワード有効期間ポリシーが引き続き Retail Store Scale Unit サービス アカウントに適用されるため、必要な場合に更新する必要があります。  既定では、Windows Server 2012 R2 では通常 42 日です。  使用されるサービス アカウントのパスワードが期限切れの場合、問題が解決されるまで Retail サーバーが機能しなくなります。

6. 次のページで、小売サーバー アプリケーション プールと Async Client のユーザー アカウントとパスワードを入力します。 既定では、このアカウントは自動的に生成されます。 ただし、ユーザー アカウントとパスワードを手動で入力できます。
7. 使用する HTTPS ポートを入力し、コンピューターのホスト名が正しいことを確認します。 その後、**次へ** を選択して続行します。

    > [!NOTE]
    > - インストーラーは自動的にホスト名を入力します。 何らかの理由で、インストールのためにホスト名を変更する必要がある場合は、ここで変更します。 ホスト名はシステムの FQDN でなければなりません。また、選択した Store システム エントリの **ホスト名**フィールドに入力する必要があります。

8. アプリケーション ID (クライアント ID) および Retail Store Scale Unit インストールと関連するキー (シークレット) を入力します。 また、コンフィギュレーション ファイルから自動的に入力されるチャネル データベース ID を確認します。 その後、**インストール** を選択します。 Retail Cloud POS を使用する場合は、ページの下部にある **Retail Cloud POS のコンフィギュレーション** チェック ボックスが選択されていることを確認します。 この構成では Azure AD サインインが要求され、必要なすべての情報が Azure で自動的に生成され、Retail Cloud POS をオンプレミスで使用できるようになります。 オンプレミス環境で使用する Retail Store Scale Unit をインストールする場合、このオプションをオフにする必要があります。

    Azure で Web アプリケーションを作成する方法については、[Azure Active Directory アプリケーションを作成する](/azure/azure-resource-manager/resource-group-create-service-principal-portal#create-an-azure-active-directory-application) を参照してください。 
    
    > [!IMPORTANT] 
    > - プレミス環境で使用する Retail Store Scale Unit をインストールするとき、Retail クラウド POS は Azure または AD FS アプリケーションの構成を要求しないため、**Retail クラウド POS のコンフィギュレーション** のマークを解除することが重要です。
    > - オンプレミス環境で使用する Retail Store Scale Unit をインストールするとき、使用されるクライアント ID (アプリケーション ID) およびシークレット (キー) は、[オンプレミス環境の Retail チャネル コンポーネントのインストール手順](../../dev-itpro/deployment/deploy-retail-onprem.md)トピックの手順6 ～ 8 で実行される構成手順で実行される PowerShell スクリプトによって生成される値になります。 (手順 6 ではクライアント ID を作成し、手順 8 ではコピーされるシークレットをリセットします)。

    Web アプリを作成するとき、最初の URI と URL は特定の値である必要はありません。 作成されるアプリケーション ID (クライアント ID) とキー (シークレット) のみ重要です。

9. Retail Store Scale Unit にアプリケーション ID (クライアント ID) とキー (シークレット) が作成され、アプリケーション ID (クライアント ID) は、小売で受け入れる必要があります。 小売用バックオフィスでコンフィギュレーションを完了する次の手順に従います。
10. インストールが完了すると、最終正常性ページが表示されます。 このページには、インストールが成功したかどうかが表示されます。 また、基本的な接続テストに基づいた各コンポーネントの正常性と、このトピックの場所について示します。 インストールに失敗した場合は、ページにログ ファイルの場所が表示されます。 Retail Store Scale Unit のコンフィギュレーションを完了して、すべてのコンポーネントが正しく動作するまで、この最終正常性ページを開いたままにしておくことをお勧めします。

### <a name="finish-the-retail-store-scale-unit-configuration-in-headquarters"></a>Headquarters で Retail Store Scale Unit のコンフィギュレーションを完了する

最後のステップでは、Azure アプリケーション ID (クライアント ID) とキー (シークレット) が小売用バックオフィスで正しく受け入れられ、環境と新しい Retail Store Scale Unit との接続が可能であることを検証し、確認する必要があります。

1. Retail Store Scale Unit にアプリケーション ID (クライアント ID) とキー (シークレット) が作成され、インストーラーに入力された後、アプリケーション ID (クライアント ID) は、小売用バック オフィスで受け入れる必要があります。 小売用バックオフィスで、**システム管理** &gt; **セットアップ** &gt; **Azure Active Directory アプリケーション** に移動します。 アプリケーション ID (クライアントID) を**クライアント ID** 列に入力し、説明のテキストを**名**列に入力および **RetailServiceAccount** を**ユーザー ID** 列に入力します。

2. Retail Cloud POS を使用するように設定されている場合、インストールの最後にクライアント ID が表示されます。 このクライアント ID を小売の **小売共有パラメーター** ページに追加する必要があります、

    > [!IMPORTANT] 
    > オンプレミス型環境では、このステップは必須ではありません。

    1. 小売用バックオフィスで、**Retail** &gt; **本社の設定** &gt; **パラメーター** &gt; **小売共有パラメーター**に移動します。
    2. **ID プロバイダー** を選択します。
    3. **ID プロバイダー** クイック タブで、`HTTPS://sts.windows.net/` で始まるプロバイダーを選択します。 選択に基づいて、**依存する関係者** FastTab の値が設定されます。
    4. **依存する関係者**クイック タブで、**追加**を選択します。 Retail Store Scale Unit インストーラーの最終正常性ページに表示されているクライアント ID を入力します。 **Type** フィールドを **Public** に、**UserType** フィールドを **Worker** に設定します。 [アクション] ウィンドウで、**保存** を選択します。
    5. 新しい依存する関係者を選択し、**サーバー リソース ID** クイック タブで **追加** を選択します。 **サーバー リソース ID** 列に、`https://retailstorescaleunit.retailserver.com` と入力します。
    6. アクション ウィンドウで、**保存**を選択します。

3. 小売用バックオフィスで、**Retail** &gt; **本社の設定** &gt; **パラメーター** &gt; **小売共有パラメーター**に移動します。
4. **ID プロバイダー** を選択します。
5. **ID プロバイダー**クイック タブで、**追加**を選択します。
6. 新しい**発行者**行に、新たにインストールした Retail Store Scale Unit の Retail サーバー URL を入力します。 URL の末尾に **/auth** を追加します。URL は `https://<My Case-Sensitive Computer Name>:<Port Number>/RetailServer/auth` のようになります。

    > [!NOTE]
    > 上記 URL では、大文字と小文字を区別します。
    > インストールされている各 Retail Store Scale Unit に新しい ID プロバイダー行があります。 各 Retail Store Scale Unit では、この URL に似た URL が作成されます。

7. **名前**列に、URL が属する店舗の説明を入力します。
8. **タイプ**列で、**OpenID 接続**を選択します。

    > [!NOTE]
    > この新しい行は、すべての Retail Store Scale Unit のインストール (つまり、一意の URL ごと) ごとに複製する必要があります。

9. アクション ウィンドウで、**保存**を選択します。
10. **ID プロバイダー**クイック タブで、新しく作成された明細行を選択します。 選択に基づいて、**依存する関係者** FastTab の値が設定されます。
11. **依存する関係者**クイック タブで、**追加**を選択し、次の 2 つのエントリを追加します。

    - **ClientId** 列に、**クラウド POS** を入力します。 **Type** フィールドを **Public** に、**UserType** フィールドを **Worker** に設定します。
    - **ClientId** 列に、**Modern POS** を入力します。 **Type** フィールドを **Public** に、**UserType** フィールドを **Worker** に設定します。

12. アクション ウィンドウで、**保存**を選択します。
13. Retail では、**Retail** &gt; **Retail IT** &gt; **配送スケジュール**へ移動し、CDX ジョブ **1110** を実行します。
14. 完了したら、インストーラーに戻り、**完了** を選択します。

    インストーラーの最後のページには、すべてのコンポーネントが正しく動作することをテストして検証するために使用できる貴重な情報が含まれています。 このページは、検証が完了する段階まで開いたままにしておきます。

> [!NOTE]
> インストーラーが Retail Server、Async Client、またはその他のコンポーネントのチェック マークを表示しない場合は、10 分待って、キャッシュされた値をクラウドで更新できるようにします。 再び確認します。 それでもインストーラーが完全に成功しない場合は、このインストールを使用する新しいチャンネル データベースで完全同期を実行します。
>
> すべての手順を正しく実行する場合、構成には次の特性が必要です。
>
> - Azure では、2 つの Web アプリケーションはインストーラー経由で自動的に生成されています。
>
>   - Retail Store Scale Unitクラウド POS
>   - Retail Store Scale Unit Cloud POS 用 Retail サーバー
>
> - Azure では、Web アプリケーション (つまり、新しい Azure ポータルでのアプリ登録) は各 Retail Store Scale Unit インストールに対して手動で作成されています (たとえば、RetailStoreScaleUnitHouston)。 作成されたキー (シークレット) は、前述のようにインストーラーで使用できます。
> - 手動で作成した Web アプリケーションのアプリケーション ID (クライアント ID) は、前の手順のステップ 1 で説明したように、Retail の **Azure Active Directory アプリケーション** ページに追加されています。
> - Retail Store Scale Unit インストーラーの最後に表示される Retail Cloud POS アプリケーション ID (クライアント ID) は、「Retail Store Scale Unit インストーラーを実行」セクションの最後の手順で説明されているように、**ID プロバイダー** クイック タブに追加されています。

### <a name="multiple-computer-installation"></a>複数のコンピューターのインストール

上級者のみ、複数のコンピュータに Retail Store Scale Unit をインストールする必要があります。 次の一連の手順では、1 台のコンピューターに Retail チャネル データベースと Async Client、2 台目のコンピューターに Retail Server と Retail Cloud POS をインストールする方法について説明します。 指示では、両方のシステムが同じドメイン上にあり、インストールされるサービスのユーザーが両方のシステムで既に作成されていることが前提です。 小売用バックオフィスですべてのコンフィギュレーションを行うことが重要です。

#### <a name="installation-on-the-first-computer"></a>最初のコンピューターへのインストール

最初のコンピューターで、このトピックの前のところで説明したように、Retail Store Scale Unit セルフ サービス インストーラーを実行しますが、次の変更を行います。

1. インストールするコンポーネントとして Retail チャネル データベースと非同期クライアントのみを選択します。 その後 **次へ** を選択して、インストールを続行します。 

    > [!NOTE]
    > Async Client はインストールされたコンピューターの外部からアクセスすることができないため、Async Client のために生成されたサービス アカウントを使用することができます。

2. クライアント ID およびキー (シークレット) を入力します。 2 台目のコンピューターで再度使用できるように、これらの詳細情報を使用可能な状態にしておきます。
3. Retail Store Scale Unit のクライアント ID と キー (シークレット) が作成された後、クライアント ID を、小売で受け入れる必要があります。 **システム管理** &gt; **設定** &gt; **Azure Active Directory アプリケーション** の順に移動します。 クライアント ID を**クライアント ID** 列に入力し、説明のテキストを**名**列に入力および **RetailServiceAccount** を**ユーザー ID** 列に入力します。
4. セットアップが正常に行われたときは、SQL Server 構成マネージャーを起動します。
5. SQL Server インスタンスの **SQL Server ネットワークの構成** &gt; **プロトコル**に移動します。
6. 右クリックし、**プロパティ** を選択します。
7. **フラグ** セクションで、**強制暗号化の設定**の値を**はい**に変更します。
8. **証明書**セクションで、ドロップダウン メニューから SSL 証明書を選択します。 この SQL Server SSL 証明書は、インストーラーで使用されているのと同じ証明書です。
9. **OK**を選択します。
10. SQL Server 構成マネージャで**プロトコル**に戻り、次のプロトコルを有効にします。

    - 名前付きパイプ
    - TCP/IP

11. **TCP/IP** プロトコルを右クリックし、**プロパティ** を選択します。
12. **IP アドレス** セクションで、一覧を **IPALL** まで下方向にスクロールします。
13. **TCPPort = 1433** と入力します。
14. **OK** を選択します。
15. 高度なセキュリティの Microsoft Windows ファイアウォールを起動します。
16. Windows ファイアウォールで、TCP ポート 1433 を開放する受信ルールを作成します。

SQL Server および Windows ファイアウォールに関する詳細については、[データベース エンジンへ アクセス用の Windows ファイアウォールをコンフィギュレーションする](https://msdn.microsoft.com/library/ms175043.aspx) を参照してください。

#### <a name="installation-on-the-second-computer"></a>2 台目のコンピューターへのインストール

2 台目のコンピューターで、このトピックの前のところで説明したように、Retail Store Scale Unit セルフ サービス インストーラーを実行しますが、次の変更を行います。

1. インストールするコンポーネントとして Retail Server と Retail Cloud POS のみを選択します。 Retail サーバーをインストールする必要がある場合は、Retail クラウド POS を選択できません。 その後 **次へ** を選択して、インストールを続行します。
2. 最初のコンピュータで、SQL Server にアクセスする権限を持つドメイン ユーザーの資格情報 (ユーザー名およびパスワード) を入力します。 その後、**次へ** を選択します。

    > [!NOTE]
    > Retail サーバーでは、最初のコンピューター上の SQL データベースへのアクセスが必要なため、生成されたサービス アカウントは使用できません。 ドメイン アカウントを使用する必要があります。

3. 最初のコンピューターで使用される同じクライアント ID およびキー (シークレット) を入力します。

    > [!IMPORTANT]
    > 前述のように Retail にこのクライアント ID を追加することが重要です。

4. **クラウド POS のコンフィギュレーション** を選択し、Azure Web アプリケーションを作成するための適切なアクセス許可を持つ Azure AD 資格情報を入力します。 

    Azure Web アプリ、それを作成する方法、および新しいキー (シークレット) を生成する方法の詳細については、[リソースにアクセスできる Azure Active Directory アプリケーションおよびサービス プリンシパルを作成するポータルの使用](https://azure.microsoft.com/documentation/articles/resource-group-create-service-principal-portal/) を参照してください。 サインイン URL やアプリ ID URI は重要ではないことに注意してください。

5. セットアップが正常に行われたときは、インストーラーを終了しません。 

    > [!NOTE]
    > 最初は、データベースがまだ正しく設定されていないため、ヘルスチェック ping は成功しません。 この手順の残りのステップを完了した後は、再度稼働状況チェックをテストできます。

6. **Microsoft インターネット インフォメーション サービス (IIS)** を起動し、**Retail Store Scale Unit** Web サイトを選択して **Retail Server** Web アプリケーションを選択します。
7. 作業ディレクトリを検証します。
8. Web.config ファイルを開いて、**connectionStrings** セクションで、**サーバー名**を追加します。 **サーバー名** はユーザーがコンポーネントをインストールした最初のコンピュータの名前です。 ファイル保存します。
9. 使用されている証明書が信頼できる機関の有効な信頼できる証明書でない場合は、CERTMGR.MSC を開いて次の手順を実行します。

    1. 前に作成した SQL Server SSL 証明書をインポートし、信頼されたルートに追加します。
    2. 管理者として**コマンド プロンプト** ウィンドウを開き、**IISRESET** と入力し、Enter キーを押します。

10. Retail Cloud POS を使用するように設定されている場合は、クライアント ID が表示されます。 このクライアント ID を小売の **小売共有パラメーター** ページに追加する必要があります、

    1. Retail で、**Retail** &gt; **本社の設定** &gt; **パラメーター** &gt; **小売共有パラメーター**に移動します。
    2. **ID プロバイダー** を選択します。
    3. **ID プロバイダー** クイック タブで、`HTTPS://sts.windows.net/` で始まるプロバイダーを選択します。 選択に基づいて、**依存する関係者** FastTab の値が設定されます。
    4. **依存する関係者**クイック タブで、**追加**を選択します。 Retail Store Scale Unit インストーラーに表示されているクライアント ID を入力します。 **Type** フィールドを **Public** に、**UserType** フィールドを **Worker** に設定します。 [アクション] ウィンドウで、**保存** を選択します。
    5. 新しい依存する関係者を選択し、**サーバー リソース ID** クイック タブで **追加** を選択します。 **サーバー リソース ID** 列に、`https://retailstorescaleunit.retailserver.com` と入力します。
    6. アクション ウィンドウで、**保存**を選択します。

11. Retail で、**Retail** &gt; **本社の設定** &gt; **小売用スケジューラ** &gt; **チャネル データベース**に移動し、これらの手順に従います。

    1. このトピックの先頭に作成したチャネルのデータベースを選択します。
    2. アクション ウィンドウで、**完全な同期** &gt; **ジョブ 9999** を選択します。 完全な同期には数分間かかる場合があります。
    3. Retail Store Scale Unit のインストーラーで、すべての機能が正常に機能していることを確認するために再テストします。

12. POS 操作を使用しているコンピューターから Retail Cloud POS を起動します。 (このコンピューターは、Retail Store Scale Unit システムとは別の 3 台目のコンピューターです。)
13. このコンピューターを使用している Retail Cloud POS デバイスを有効化します。
14. 完全なエンド ツー エンドの機能を確認する簡易販売を実行します。

### <a name="help-secure-retail-store-scale-unit"></a>Retail Store Scale Unit のセキュリティを強化する

現在のセキュリティ基準によると、実稼動環境で次のオプションを設定する必要があります。

- コンピューターの SSL (v2およびv3) を完全に無効にする必要があります。
- TLS バージョン 1.2 (または、現時点で最も新しいバージョン) のみを有効にし、使用する必要があります。

    > [!NOTE]
    > 既定では、SSL および TLS 1.2 を除くすべてのバージョンの TLS は無効です。 これらの設定を編集または有効にするには、次の手順を実行します。
    >
    > 1. Windows ロゴキーと R キーを同時に押して、**実行**ウィンドウを開きます。
    > 2. **開く**フィールドに、**Regedit** と入力してから **OK** を選択します。
    > 3. **ユーザー アカウント制御**ウィンドウで、**はい** (この手順が必要である場合) を選択してから、新しい**レジストリ エディター** ウィンドウで **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\SecurityProviders\\SCHANNEL\\Protocols** に移動します。
    > 4. 次のキーは自動的に入力され、TLS 1.2 のみが有効になります。
    >
    >     - TLS 1.2\\Server:Enabled=1
    >     - TLS 1.2\\Server:DisabledByDefault=0
    >     - TLS 1.2\\Client:Enabled=1
    >     - TLS 1.2\\Client:DisabledByDefault=0
    >     - TLS 1.1\\Server:Enabled=0
    >     - TLS 1.1\\Client:Enabled=0
    >     - TLS 1.0\\Server:Enabled=0
    >     - TLS 1.0\\Client:Enabled=0
    >     - SSL 3.0\\Server:Enabled=0
    >     - SSL 3.0\\Client:Enabled=0
    >     - SSL 2.0\\Server:Enabled=0
    >     - SSL 2.0\\Client:Enabled=0

- 知られている特定の理由で必要とされない限り、追加のネットワーク ポートを開かないでください。
- クロスオリジンのリソース共有を無効にし、許可され承認されたオリジンを指定する必要があります。
- Store システムのコンピューターで使用する証明書の取得には、信頼された証明機関のみを活用してください。

> [!IMPORTANT]
> IIS と Payment Card Industry (PCI) の要件向けのセキュリティ ガイドラインを確認することが重要です。

### <a name="troubleshoot-retail-store-scale-unit"></a>Retail Store Scale Unit のトラブルシューティング

確認する項目のチェックリストを次に示します。

1. Retail の**小売共有パラメーター** ページで、適切なクライアント ID が**依存する関係者**クイック タブに追加されていることを確認します。 また、正しい `https://retailstorescaleunit.retailserver.com` エントリが **サーバー リソース ID** クイック タブに追加されていることを確認します。
2. Retail で、各小売店舗に生成されたすべてのクライアント ID が **Azure Active Directory アプリケーション** ページに存在することを確認します。
3. Retail の**チャネル プロファイル** ページで、URL が正しいことを確認します。 (つまり、各 URL のコンピュータ名が正しいこと、URL が正しく書式設定されていることなどを確認します。)
4. Retail の**チャネル データベース** ページで、新しいチャネル データベースに完全同期が正しく発生したことを確認します。
5. 新しいチャネル データベースを使用するように小売店舗が正しく構成されていることを確認します。

Retail Store Scale Unit が一定時間の後に停止した場合、確認すべき 2 つの簡単なことがあります。

- パスワード ポリシーにより、パスワード (パスワードの有効期限) を変更するために生成されたサービス アカウントが求められているかどうかを確認します。
- 現在のインストール (非べき等) で同一のインストーラーを再実行します。これにより、サービス アカウントのパスワードが更新されるか、選択したアカウントのパスワードの更新が許可されます。

### <a name="uninstall-retail-store-system"></a>Retail Store システムのアンインストール

Microsoft Windows でコントロール パネルを使用して Retail Store システムをアンインストールします。

1. Windows ロゴ キーを押し、検索ボックスに**コントロール パネル**と入力します。 検索結果で、**コントロール パネル**を選択します。
2. コントロール パネルで、**プログラム** &gt; **プログラムのアンインストール**を選択します。
3. **プログラムと機能**ウィンドウで、**Microsoft Dynamics 365 for Retail ストア システム**を選択してから、プログラムの一覧で**アンインストール**を選択します。
4. アンインストールがプログラムの削除を完了するまで待ちます。
