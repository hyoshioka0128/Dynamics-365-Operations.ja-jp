---
title: Finance and Operations サポート エクスペリエンスの管理
description: このトピックでは、Microsoft Dynamics Lifecycle Services のサポート ツールを使用して、サポート インシデントを管理する方法について説明します。
author: kfend
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 60373
ms.assetid: 0fa10573-8146-446e-8124-8a7af9546add
ms.search.region: Global
ms.author: anupams
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13a1169e226666cf87e78cf7e62f42da1c675a1f
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741206"
---
# <a name="manage-finance-and-operations-support-experiences"></a>Finance and Operations サポート エクスペリエンスの管理

[!include [banner](../includes/banner.md)]

サポート ツールを使用するには、あらかじめ Lifecycle Services (LCS) でプロジェクトを作成して、環境にシステム診断プログラムをインストールして実行する必要があります。 詳細については、[システム診断 (Lifecycle Services, LCS)](ax-2012/system-diagnostics-lcs.md) を参照してください。

## <a name="open-a-new-incident"></a>新しいインシデントを開く
1. LCS にて、サポート インシデントを提出するプロジェクトに移動します。 

2. **サポート** タイルをクリックします。

   ![サポート メニュー](media/CPS1.png)

3. **Microsoft に送信**タブで、**インシデントの送信**ボタンをクリックします。

   ![サポート ボタン](media/CPS2.png)

4. 問題のカテゴリを選択します。

5. 問題の領域を選択します。

6. **問題の説明** 欄で、次の内容を入力します。

   - 環境で問題が発生した場合は、 **はい** を選択して下さい。 環境名を選択します。  
   - **タイトル**フィールドの問題について短い説明を入力します。
   - 問題の詳細と、エラーを再生成するために必要なステップに関する詳細を提供します。
   - 該当する場合は、エラー メッセージを入力します。 
   - 可能であれば、問題を示すスクリーン ショットを関連付けます。 これを行うには、**コンピュータからの添付ファイル** をクリックします。
 
 
   > [!NOTE]
   > インシデントを作成するときは、問題検索によって、ユーザーの選択と入力にもとづいて、上位 10 の「実行可能な問題のソリューション」という検索結果が設定され、サポート ケースの作成時に詳細情報が提供されると、これらの結果が動的に更新されます。 
   > 
   > さらにソリューションを検索する必要がある場合は、ドロップダウン メニューからスタンドアロン問題検索にアクセスできます。 
 
7. 基本連絡先情報を入力します。 これらの連絡先の詳細は、カスタマー サポート チームがケースについて連絡するために使用されます。

8. サポート契約と重要度レベルを選択します。 
    
   - オンプレミス環境のサポート契約では、インシデント数に制限があります。 
   - クラウド環境のサポート契約では、インシデント数が無制限です。 
   - オンプレミス製品またはクラウド環境では、使用可能なサポート契約の一覧から、複数層のサポート契約がある場合に使用するサポート オプションを選択します。 
  
9. **送信** をクリックします。 

**送信**をクリックした後、インシデントが作成され**インシデント** リストに追加されます。 このケースに割り当てられている Microsoft サポート エンジニアから、電子メール メッセージを受け取ります。 


## <a name="support-plans-in-lifecycle-services"></a>Lifecycle Servicesにおけるサポートプラン
サポートプランのエンタイトルメントは、さまざまな識別子に基づき提供されます。 すべてが適用されるわけではありません。 サポートプランまたはLCSでエンタイトルメントが見つからない場合は、LCSのプロジェクトでどのような識別子が関連付けられるべきかを決定することになります。 複数の組織がある場合は、LCSの右上の名称をクリックすることで現行のものを示してください。 シナリオに適合し、利用したいベネフィットを含む組織を選択して下さい。

### <a name="unique-contract-idaccess-id"></a>契約者固有ID/固有アクセスID
次のオンライン サポートプランでは、LCSでのサインインと関連付けられた契約者固有ID/固有アクセスIDが必要です。

-   統合サポート
-   プレミア
-   パートナー様向け Advanced サポート

契約者固有ID/固有アクセスIDの組み合わせがわからない場合は、マイクロソフトの顧客担当者に問い合わせの上IDの再作成をご依頼ください。

アカウントと契約社ID/アクセスIDを関連付けるには、次の手順を完了してください

1. プロジェクト内から選択 **サポート** し、メイン メニューなどの選択から **管理サポート プラン** します。 
2. **契約の追加** を選択します

   ![契約の追加](media/56c7bfd469f6d850d456e9e7a89e0d8d.png)

3. アクセスIDと、パスワードまたは契約IDを入力し、 **契約の追加** を選択します。

   ![契約の資格情報の追加](media/4abba1127549ef484a58daf51609d924.png)

### <a name="partnersource-business-center-account"></a>PartnerSource Business Center アカウント
利用可能な場合は、次のサポートプランインシデントがPartnerSource業務部門 (PSBC) アカウントの一部として使用できます。 

> [!NOTE]
> PSBCアカウントではオンライン サポートプランはご利用できません。

-   顧客向け オンプレミス インシデントの高度なサポート
-   優先 または 優先 + オンプレミスインシデント
-   既存のインシデントタイプのプランごとの支払いについては、PSBCに算出されます。

PartnerSourceビジネス センター アカウントが見つからない場合は、PSBCの組織でサインインがプロフェッショナルとして追加されているか確認してください。 同一のMicrosoftアカウントまたは職場アカウントを使用してログインしていることを確認します。 このアカウントは、オンプレミスプロジェクトにのみ有効です。

![契約の追加](media/56c7bfd469f6d850d456e9e7a89e0d8d.png)

### <a name="sign-in-specfic-options"></a>サインイン 特定のオプション
該当するものがある場合、ログインのアカウントに基づき次の問題とサポートの特典が表示されます。

-   MPN gold および シルバー インシデント
-   シグネイチャークラウドサポート
-   個々のインシデントと [support.microsoft.com/supportforbusiness] で購入した5パック 

   > [!NOTE]
   > インシデントはMicrosoftアカウントを使用して購入する必要があります。 Microsoftアカウントは \@hotmail.com または \@outlook.com のような形式です。 作業アカウントまたは Azure Active Directory アカウントは、それぞれに関連付けられているインシデントを持つことはできません。

### <a name="tenant-subscription"></a>テナントサブスクリプション
次のエンタイトルメントが、サブスクリプションおよびテナント組織内でのProDirect購入に基づいて表示されます。

-   定期売買
-   ProDirect

### <a name="software-assurance"></a>ソフトウェア保証
次のエンタイトルメントは、定期売買番号および連絡先電子メール アドレスを連携させることで追加可能です。

-   ソフトウェア保証

サポート インシデントを作成する際に **ソフトウェア保証プラン追加** することで追加します。 定期売買番号および連絡先の電子メールを入力し、 **続行します** をクリックします。

![ソフトウェア保証プラン](media/cd8f65a32c30722ea687dfbc5cc30874.png)
   
## <a name="report-production-outage"></a>稼働停止のレポート
プロダクション環境の品質が低下または使用不可能になった際に、Microsoft サポートに迅速に問題を効果的にエスカレーションするには、 [Report a production outage](report-production-outage.md) をご確認ください。

## <a name="phone-support"></a>電話サポート
[新しいインシデントを開く](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/cloud-powered-support-lcs#open-a-new-incident) の手順に従ってサポートに連絡することをお勧めします。 LCS で新しいインシデントを開けない場合は、次のいずれかのオプションで電話サポートを受けることができます:

- [プレミア電話サポート](https://support.microsoft.com/premier/contacts)
- [広範な商業電話サポート](https://mbs.microsoft.com/customersource/northamerica/GP/support/support-news/global_support_contacts_eng)
