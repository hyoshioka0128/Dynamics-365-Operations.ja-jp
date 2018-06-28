---
title: "外部ギフト カードのサポート"
description: "このトピックでは、Microsoft Dynamics 365 for Retail で現在利用できる外部ギフト カードのサポートについて説明します。"
author: sericks007
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.devlang: 
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: retail
ms.author: ivanv
ms.search.validFrom: 2017-10-02
ms.dyn365.ops.version: Application update 4
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fe07a9a8c760ddb94a70ab23d5d00126efc3a3ea
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="external-gift-card-support"></a><span data-ttu-id="89dbc-103">外部ギフト カードのサポート</span><span class="sxs-lookup"><span data-stu-id="89dbc-103">External gift card support</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="89dbc-104">顧客にシームレスなエクスペリエンスを提供するために、小売業者はさまざまな支払方法を受け入れることができることを望んでいます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-104">To provide a seamless experience for their customers, retailers want to be able to accept a wide variety of payment methods.</span></span> <span data-ttu-id="89dbc-105">ギフト カードは、現金やクレジット カードの次に最も頻繁に使用される支払方法の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="89dbc-105">Gift cards are one of the most frequently used payment methods after cash and credit cards.</span></span> <span data-ttu-id="89dbc-106">多くの小売業者にとっての重要な要件は、販売時点管理 (POS) でさまざまなタイプのギフト カードを各種プロバイダーから受け入れることです。</span><span class="sxs-lookup"><span data-stu-id="89dbc-106">An important requirement for many retailers is the ability to accept various types of gift cards, from various providers, at the point of sale (POS).</span></span>

<span data-ttu-id="89dbc-107">Microsoft Dynamics 365 for Retail は、外部のギフト カードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="89dbc-107">Microsoft Dynamics 365 for Retail now supports external gift cards.</span></span> <span data-ttu-id="89dbc-108">したがって、小売業者は、GiveX などのギフト カード プロバイダーからのサードパーティ ギフト カードを POS を使用して受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-108">Therefore, retailers can accept third-party gift cards from gift card providers such GiveX by using the POS.</span></span> <span data-ttu-id="89dbc-109">この機能を活用するには、外部のギフト カード サービス プロバイダのアカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="89dbc-109">To take advantage of this functionality, you must have an account with an external gift card service provider.</span></span> <span data-ttu-id="89dbc-110">この機能は、ソリューションが提供していた標準のギフト カード サポートとは異なります。</span><span class="sxs-lookup"><span data-stu-id="89dbc-110">This functionality differs from the out-of-box gift card support that the solution offered.</span></span>

<span data-ttu-id="89dbc-111">最初から用意されている Verifone Payment コネクタもアップデートされ、外部ギフト カードの機能をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="89dbc-111">The out-of-box Verifone Payment connector has also been updated so that it supports the functionality for external gift cards.</span></span> <span data-ttu-id="89dbc-112">最初の更新で GiveX との統合が可能になりました。</span><span class="sxs-lookup"><span data-stu-id="89dbc-112">The initial update enables integration with GiveX.</span></span>

<span data-ttu-id="89dbc-113">外部ギフト カードは、小売用バックオフィスと POS の両方に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89dbc-113">The external gift card must be configured for both the Retail headquarters and the POS.</span></span> <span data-ttu-id="89dbc-114">ギフト カードをコンフィギュレーションする前に、小売業者は外部のギフト カード サービス プロバイダーのアカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="89dbc-114">Before the gift card can be configured, the retailer must have an account with an external gift card service provider.</span></span>

## <a name="retail-headquarters-configuration"></a><span data-ttu-id="89dbc-115">小売用バックオフィス コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="89dbc-115">Retail headquarters configuration</span></span>

1. <span data-ttu-id="89dbc-116">**ハードウェア プロファイル**を検索して **POS ハードウェア プロファイル** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-116">Search for **hardware profile** to open the **POS hardware profile** page.</span></span>
2. <span data-ttu-id="89dbc-117">**POS ハードウェア プロファイル**ページで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="89dbc-117">On the **POS hardware profile** page, follow these steps:</span></span>

   1. <span data-ttu-id="89dbc-118">ページの左側にあるナビゲーション バーで、**仮想**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-118">On the navigation bar on the left side of the page, select **Virtual**.</span></span>
   2. <span data-ttu-id="89dbc-119">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-119">Select **Edit**.</span></span>
   3. <span data-ttu-id="89dbc-120">**ETF サービス**クイック タブの、**コネクタ**グリッドで、最初の入力 **TestConnector** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-120">On the **ETF service** FastTab, in the **Connectors** grid, select the first entry, **TestConnector**.</span></span>
   4. <span data-ttu-id="89dbc-121">**サポートされる支払/入金タイプ** フィールドに、**GiftCard** を追加します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-121">In the **Supported Tender Types** field, add **GiftCard**.</span></span>

       ![サポートされている支払/入金タイプのリストへの GiftCard の追加](./media/01.png)

   5. <span data-ttu-id="89dbc-123">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-123">Select **Save**.</span></span>

      > [!NOTE]
      > <span data-ttu-id="89dbc-124">また、**新規** ボタンを使用して複数の支払コネクタを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-124">You can also use the **New** button to create multiple payment connectors.</span></span> <span data-ttu-id="89dbc-125">この方法で、ソリューションに追加された複数のコネクタのサポートを利用できます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-125">In this way, you can take advantage of the support for multiple connectors that has been added to the solution.</span></span> <span data-ttu-id="89dbc-126">異なる支払メソッドのために異なる支払コネクタを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-126">You can then have different payment connectors for different payment methods.</span></span> <span data-ttu-id="89dbc-127">たとえば、1 つのコネクタですべてのクレジット カードを処理できますが、別のコネクタでギフト カードを処理することができます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-127">For example, all credit cards can be processed through one connector, but the gift card can be processed through a different connector.</span></span>

3. <span data-ttu-id="89dbc-128">**支払方法** を検索して **支払方法** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-128">Search for **payment methods** to open the **Payment methods** page.</span></span>
4. <span data-ttu-id="89dbc-129">**新規** を選択し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="89dbc-129">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="89dbc-130">**支払方法**フィールドに **12** と入力します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-130">In the **Payment method** field, enter **12**.</span></span>
    2. <span data-ttu-id="89dbc-131">**支払方法名**フィールドに、**外部ギフト カード**と入力します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-131">In the **Payment method name** field, enter **External Gift Card**.</span></span>
    3. <span data-ttu-id="89dbc-132">**既定の機能**フィールドで、**カード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-132">In the **Default function** field, select **Card**.</span></span>
    4. <span data-ttu-id="89dbc-133">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-133">Select **Save**.</span></span>

5. <span data-ttu-id="89dbc-134">**すべての小売店舗**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-134">Open the **All retail stores** page.</span></span>
6. <span data-ttu-id="89dbc-135">一覧で、**ヒューストン**の店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-135">In the list, select the **Houston** store.</span></span>
7. <span data-ttu-id="89dbc-136">アクション ウィンドウで、**設定** &gt; **支払方法**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-136">On the Action Pane, select **Set up** &gt; **Payment methods**.</span></span>
8. <span data-ttu-id="89dbc-137">**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-137">Select **New**.</span></span>
9. <span data-ttu-id="89dbc-138">**支払方法**フィールドに **12** と入力します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-138">In the **Payment method** field, enter **12**.</span></span> <span data-ttu-id="89dbc-139">次に、**支払方法名** および **関数** フィールドが自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-139">The **Payment method name** and **Function** fields should then be set automatically.</span></span>
10. <span data-ttu-id="89dbc-140">**一般**クイック タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-140">On the **General** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="89dbc-141">**工程名** フィールドを **支払ギフト カード** に設定します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-141">Set the **Operation name** field to **Pay gift card**.</span></span>
    - <span data-ttu-id="89dbc-142">**コネクタ名** フィールドを **TestConnector** に設定します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-142">Set the **Connector name** field to **TestConnector**.</span></span>

11. <span data-ttu-id="89dbc-143">**転記**クイック タブで、**ギフト カード品目番号**フィールドを **0010** に設定します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-143">On the **Posting** FastTab, set the **Gift card item number** field to **0010**.</span></span>

    ![ギフト カード品目の番号フィールドの設定](./media/05_02.png)

12. <span data-ttu-id="89dbc-145">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-145">Select **Save**.</span></span>
13. <span data-ttu-id="89dbc-146">**ボタン グリッド**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-146">Open the **Button grid** page.</span></span>
14. <span data-ttu-id="89dbc-147">ページの左側にあるナビゲーション バーで、**F2S1M** を検索してフィルター処理オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-147">In the navigation bar on the left side of the page, search for **F2S1M**, and select the filtered option.</span></span>
15. <span data-ttu-id="89dbc-148">アクション ウィンドウで、**デザイナー**を選択しボタン デザイナー アプリケーションをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="89dbc-148">On the Action Pane, select **Designer** to download the button designer application.</span></span>
16. <span data-ttu-id="89dbc-149">グリッド デザイナーが表示されたら、空の (灰色) 領域を右クリックして、**新規作成ボタン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-149">When the grid designer appears, right-click on an empty (gray) area, and then select **New button**.</span></span>

    ![新しいボタン](./media/07.png)

17. <span data-ttu-id="89dbc-151">新しいボタンを右クリックし、**ボタン プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-151">Right-click the new button, and then select **Button properties**.</span></span>
18. <span data-ttu-id="89dbc-152">次のマトリックスに従って **アクション**、**支払タイプ**、および**ボタンのテキスト** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-152">Set the **Action**, **Payment type**, and **Text on button** properties according to the following matrix.</span></span>

    | <span data-ttu-id="89dbc-153">アクション</span><span class="sxs-lookup"><span data-stu-id="89dbc-153">Action</span></span>            | <span data-ttu-id="89dbc-154">支払タイプ</span><span class="sxs-lookup"><span data-stu-id="89dbc-154">Payment type</span></span>       | <span data-ttu-id="89dbc-155">ボタンのテキスト</span><span class="sxs-lookup"><span data-stu-id="89dbc-155">Text on button</span></span>        |
    |-------------------|--------------------|-----------------------|
    | <span data-ttu-id="89dbc-156">ギフト カードの発行</span><span class="sxs-lookup"><span data-stu-id="89dbc-156">Issue gift card</span></span>   | <span data-ttu-id="89dbc-157">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="89dbc-157">External Gift Card</span></span> | <span data-ttu-id="89dbc-158">Ext Issue ギフト カード</span><span class="sxs-lookup"><span data-stu-id="89dbc-158">Ext Issue gift card</span></span>   |
    | <span data-ttu-id="89dbc-159">ギフト カードに追加</span><span class="sxs-lookup"><span data-stu-id="89dbc-159">Add to gift card</span></span>  | <span data-ttu-id="89dbc-160">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="89dbc-160">External Gift Card</span></span> | <span data-ttu-id="89dbc-161">ギフト カードに Ext 追加</span><span class="sxs-lookup"><span data-stu-id="89dbc-161">Ext Add to gift card</span></span>  |
    | <span data-ttu-id="89dbc-162">ギフト カード残高</span><span class="sxs-lookup"><span data-stu-id="89dbc-162">Gift card balance</span></span> | <span data-ttu-id="89dbc-163">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="89dbc-163">External Gift Card</span></span> | <span data-ttu-id="89dbc-164">Ext Gift カード残高</span><span class="sxs-lookup"><span data-stu-id="89dbc-164">Ext Gift card balance</span></span> |
    | <span data-ttu-id="89dbc-165">ギフト カードで支払う</span><span class="sxs-lookup"><span data-stu-id="89dbc-165">Pay gift card</span></span>     | <span data-ttu-id="89dbc-166">外部ギフト カード</span><span class="sxs-lookup"><span data-stu-id="89dbc-166">External Gift Card</span></span> | <span data-ttu-id="89dbc-167">Ext Pay ギフト カード</span><span class="sxs-lookup"><span data-stu-id="89dbc-167">Ext Pay gift card</span></span>     |

    <span data-ttu-id="89dbc-168">完了したら、ボタンのレイアウトは次の図のようになります。</span><span class="sxs-lookup"><span data-stu-id="89dbc-168">When you've finished, your button layout should resemble the following illustration.</span></span>

    ![完了したボタン レイアウト](./media/10.png)

19. <span data-ttu-id="89dbc-170">デザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-170">Close the designer.</span></span>
20. <span data-ttu-id="89dbc-171">**配送スケジュール**を検索します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-171">Search for **Distribution Schedule**.</span></span>
21. <span data-ttu-id="89dbc-172">ページの左側にあるナビゲーション バーで、**1090**、**1115**、および **1070** を検索します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-172">In the navigation bar on the left side of the page, search for **1090**, **1115**, and **1070**.</span></span>
22. <span data-ttu-id="89dbc-173">アクション ウィンドウで、**今すぐ実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-173">On the Action Pane, select **Run now**.</span></span>
23. <span data-ttu-id="89dbc-174">**ダウンロード セッション**を検索してジョブのステータスを確認してください。</span><span class="sxs-lookup"><span data-stu-id="89dbc-174">Check the status of the job by searching for **Download sessions**.</span></span>
24. <span data-ttu-id="89dbc-175">すべてのジョブの横に **適用済** が表示されるまで待ってから、ブラウザーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-175">Wait until **Applied** appears next to all the jobs, and then close the browser.</span></span>

## <a name="reset-iis-if-youre-using-retail-store-scale-unit"></a><span data-ttu-id="89dbc-176">Retail Store スケール ユニットを使用している場合は、IIS をリセット</span><span class="sxs-lookup"><span data-stu-id="89dbc-176">Reset IIS if you're using Retail Store Scale Unit</span></span>

<span data-ttu-id="89dbc-177">ストアにある小売店舗スケール ユニット (RSSU) を使用している場合は、管理者としてコマンド プロンプト ウィンドウを開き、**iisreset** と入力します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-177">If you're using a Retail Store Scale Unit (RSSU) that is located in the store, open a Command Prompt window as an administrator, and enter **iisreset**.</span></span> <span data-ttu-id="89dbc-178">それ以外の場合、Retail サーバーが更新されるまで待機します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-178">Otherwise, wait for the Retail Server to be updated.</span></span>

## <a name="update-merchant-properties"></a><span data-ttu-id="89dbc-179">商人プロパティの更新</span><span class="sxs-lookup"><span data-stu-id="89dbc-179">Update merchant properties</span></span>

1. <span data-ttu-id="89dbc-180">ファイル エクスプローラーで、**C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Hardware Station\\ConfigurationUtility** に移動します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-180">In File Explorer, go to **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Hardware Station\\ConfigurationUtility**.</span></span>
2. <span data-ttu-id="89dbc-181">**HardwareStationConfigurationUtility** 実行可能プログラムを実行します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-181">Run the **HardwareStationConfigurationUtility** executable program.</span></span>
3. <span data-ttu-id="89dbc-182">正しい Retail サーバー URL を入力してユーティリティをコンフィギュレーションし、**インストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-182">Configure the utility by entering the correct Retail Server URL, and then select **Install**.</span></span>
4. <span data-ttu-id="89dbc-183">ダウンロードが正常に完了したことを確認するには、**c:\\ProgramData\\Microsoft Dynamics AX\\Retail Hardware Station** に移動し、**MerchantInformation.xml** ファイルのタイムスタンプを確認します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-183">To verify that the download was successful, go to **C:\\ProgramData\\Microsoft Dynamics AX\\Retail Hardware Station**, and look at the timestamp of the **MerchantInformation.xml** file.</span></span> <span data-ttu-id="89dbc-184">これは最新である必要があります。</span><span class="sxs-lookup"><span data-stu-id="89dbc-184">It should be very recent.</span></span>

## <a name="configure-and-test-retail-modern-pos"></a><span data-ttu-id="89dbc-185">Retail Modern POS のコンフィギュレーションおよびテスト</span><span class="sxs-lookup"><span data-stu-id="89dbc-185">Configure and test Retail Modern POS</span></span>

1. <span data-ttu-id="89dbc-186">Retail Modern POS (MPOS) アプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-186">Start the Retail Modern POS (MPOS) application.</span></span>
2. <span data-ttu-id="89dbc-187">標準の資格情報を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="89dbc-187">Sign in by using the standard credentials.</span></span>
3. <span data-ttu-id="89dbc-188">メッセージが表示されたら、**ドロワー以外の操作の実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-188">When you're prompted, select **Perform a non-drawer operation**.</span></span>
4. <span data-ttu-id="89dbc-189">メイン画面で、**ハードウェア ステーションの選択**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-189">On the main screen, select **Select hardware station**.</span></span>
5. <span data-ttu-id="89dbc-190">ページの右側にあるバーで、**管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-190">On the bar on the right side of the page, select **Manage**.</span></span>
6. <span data-ttu-id="89dbc-191">**仮想周辺機器** をオンにし、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-191">Turn on **Virtual Peripherals**, and then select **OK**.</span></span>
7. <span data-ttu-id="89dbc-192">**使用可能なペアリング済ステーション** フィールドで、**仮想周辺機器**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-192">In the **Available paired stations** field, select **Virtual Peripherals**.</span></span>
8. <span data-ttu-id="89dbc-193">新しいシフトを開くか、非ドロワー操作を実行するように求められます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-193">You're prompted to either open a new shift or perform non-drawer operations.</span></span> <span data-ttu-id="89dbc-194">新しいシフトを開くことができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="89dbc-194">You can now open a new shift.</span></span>
9. <span data-ttu-id="89dbc-195">メイン画面で、**現在のトランザクション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-195">On the main screen, select **Current transaction**.</span></span>
10. <span data-ttu-id="89dbc-196">**ギフト カード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-196">Select **Gift cards**.</span></span>
11. <span data-ttu-id="89dbc-197">**Ext Issue ギフト カード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-197">Select **Ext Issue gift card**.</span></span>
12. <span data-ttu-id="89dbc-198">**9** で始まる数を入力し、次に金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-198">Enter a number that starts with **9**, and then provide an amount.</span></span>
13. <span data-ttu-id="89dbc-199">品目がカートに追加された後、現金またはカードを使用して支払うことができます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-199">After items are added to the cart, you can pay by using cash or a card.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="89dbc-200">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="89dbc-200">Troubleshooting</span></span> 

### <a name="issue-an-error-occurs-when-you-start-the-hardwarestationconfigurationutility-program"></a><span data-ttu-id="89dbc-201">問題: HardwareStationConfigurationUtility プログラムの起動時にエラーが発生します</span><span class="sxs-lookup"><span data-stu-id="89dbc-201">Issue: An error occurs when you start the HardwareStationConfigurationUtility program</span></span>

1. <span data-ttu-id="89dbc-202">上位のコマンド プロンプトからは、メモ帳で **HardwareStationConfigurationUtility.exe.config** ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-202">From an elevated command prompt, open the **HardwareStationConfigurationUtility.exe.config** file in Notepad.</span></span>
2. <span data-ttu-id="89dbc-203">ファイルで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="89dbc-203">In the file, follow these steps:</span></span>

    1. <span data-ttu-id="89dbc-204">**DataServiceUrl** 値を適切な Retail サーバー URL に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-204">Replace the **DataServiceUrl** value with the correct Retail Server URL.</span></span>
    2. <span data-ttu-id="89dbc-205">**AADLogonUrl** の値が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-205">Verify that the **AADLogonUrl** value is correct.</span></span>

3. <span data-ttu-id="89dbc-206">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-206">Save and close the file.</span></span>
4. <span data-ttu-id="89dbc-207">ユーティリティを再起動します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-207">Restart the utility.</span></span>

### <a name="issue-a-token-error-occurs-when-you-try-to-pair-virtual-peripherals"></a><span data-ttu-id="89dbc-208">問題: 仮想周辺機器をペアリングしようとしたときにトークン エラーが発生します</span><span class="sxs-lookup"><span data-stu-id="89dbc-208">Issue: A token error occurs when you try to pair virtual peripherals</span></span>

1. <span data-ttu-id="89dbc-209">MPOS を終了します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-209">Exit MPOS.</span></span>
2. <span data-ttu-id="89dbc-210">**C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Hardware Station\\Package** に移動します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-210">Go to **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Hardware Station\\Package**.</span></span>
3. <span data-ttu-id="89dbc-211">上位のコマンド プロンプトからは、メモ帳で **Web.config** ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-211">From an elevated command prompt, open the **Web.config** file in Notepad.</span></span>
4. <span data-ttu-id="89dbc-212">**RetailServer** 値を適切な Retail サーバー値に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-212">Replace the **RetailServer** value with the correct Retail Server value.</span></span>
5. <span data-ttu-id="89dbc-213">ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="89dbc-213">Save and close the file.</span></span>
6. <span data-ttu-id="89dbc-214">MPOS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="89dbc-214">Restart MPOS.</span></span>
7. <span data-ttu-id="89dbc-215">問題が解消しない場合は、MPOS を終了し、タスク マネージャーを使用して、実行中の dllhost.exe インスタンスを終了させ、インターネット インフォメーション サービス (IIS) のリセットを別に行います。</span><span class="sxs-lookup"><span data-stu-id="89dbc-215">If the issue persists, exit MPOS, use Task Manager to end any instances of dllhost.exe that are running, and then do another reset of Internet Information Services (IIS).</span></span>
