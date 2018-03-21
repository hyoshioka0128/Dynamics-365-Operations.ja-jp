--- 
title: "古い形式の製品バリアントを検索する"
description: "この手順では、古い形式のリリース済製品または製品バリアントを検索する方法と、古い形式の製品に製品ライフサイクルの状態を関連付ける方法を説明します。"
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d445ea2f2362f146a1e3e7bcf747898dc2cc89ba
ms.openlocfilehash: 3a59f988de5290d1d69d013b762f87d0cce10e39
ms.contentlocale: ja-jp
ms.lasthandoff: 02/08/2018

---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="fa8b4-103">古い形式の製品バリアントを検索する</span><span class="sxs-lookup"><span data-stu-id="fa8b4-103">Find obsolete product variants</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fa8b4-104">この手順では、古い形式のリリース済製品または製品バリアントを検索する方法と、古い形式の製品に製品ライフサイクルの状態を関連付ける方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="fa8b4-105">前提条件: このタスク ガイドを実行する前に計画に対して無効である、少なくとも 1 つの製品ライフサイクルの状態を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="fa8b4-106">シミュレーションの実行</span><span class="sxs-lookup"><span data-stu-id="fa8b4-106">Run a simulation</span></span>
1. <span data-ttu-id="fa8b4-107">[製品情報管理] > [定期処理のタスク] > [販売終了製品のライフサイクル状態の変更] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="fa8b4-108">[新製品ライフサイクルの状態] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="fa8b4-109">[製品データを更新せずシミュレーションを実行する] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="fa8b4-110">[この日数内に作成された製品を除外する] フィールドで、数字を入力します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="fa8b4-111">[トランザクションで使用される製品を除外する (日数)] フィールドで、数字を入力します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="fa8b4-112">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="fa8b4-113">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-113">Click Filter.</span></span>
8. <span data-ttu-id="fa8b4-114">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="fa8b4-115">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="fa8b4-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-116">Click OK.</span></span>
11. <span data-ttu-id="fa8b4-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="fa8b4-118">多数の製品を検索する場合は、バッチでシミュレーションを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="fa8b4-119">また、シミュレーションが、会社の最も有効な作業時間中に実行されないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="fa8b4-120">シミュレーション結果の確認</span><span class="sxs-lookup"><span data-stu-id="fa8b4-120">Review the simulation results</span></span>
1. <span data-ttu-id="fa8b4-121">[製品情報管理] > [照会やレポート] > [製品のライフサイクル状態の管理履歴] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="fa8b4-122">このページで、シミュレーション結果を表示でき、シミュレーション無しで更新が実行中に、いくつの製品と製品バリアントが新しい製品ライフサイクルの状態に関連付けられるのか評価できます。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="fa8b4-123">古い形式の製品に対する製品ライフサイクルの状態の更新を実行します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="fa8b4-124">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-124">Close the page.</span></span>
2. <span data-ttu-id="fa8b4-125">[製品情報管理] > [定期処理のタスク] > [販売終了製品のライフサイクル状態の変更] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="fa8b4-126">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="fa8b4-127">最後の選択内容が保存されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="fa8b4-128">[製品データを更新せずシミュレーションを実行する] フィールドで [いいえ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="fa8b4-129">[バックグラウンドで実行] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="fa8b4-130">いくつの製品と製品バリアントが影響を受けたかに応じて、このジョブをバッチで実行するかを検討します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="fa8b4-131">会社で最も有効な作業時間中に大きな更新ジョブを実行していないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="fa8b4-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-132">Click OK.</span></span>
7. <span data-ttu-id="fa8b4-133">[製品情報管理] > [照会やレポート] > [製品のライフサイクル状態の管理履歴] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="fa8b4-134">リリースされた製品および製品バリアントの変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="fa8b4-135">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="fa8b4-135">In the list, find and select the desired record.</span></span>

