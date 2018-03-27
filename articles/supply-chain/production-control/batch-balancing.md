---
title: "バッチ バランシング"
description: "このトピックでは、バッチ バランシング プロセスについて説明します。"
author: johanhoffmann
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 84e00ef62a995d37878de6b2786dbc2ee2277070
ms.openlocfilehash: 8a1ec5a3b19d1022232527f4960617bd985bc2b3
ms.contentlocale: ja-jp
ms.lasthandoff: 03/12/2018

---

# <a name="batch-balancing"></a><span data-ttu-id="21d01-103">バッチ バランシング</span><span class="sxs-lookup"><span data-stu-id="21d01-103">Batch balancing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="21d01-104">このトピックでは、バッチ バランシング プロセスのサポート方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="21d01-104">This topic describes how the batch balancing process is supported.</span></span>

<span data-ttu-id="21d01-105">バッチ バランシング プロセスでは、生産バッチで使用する成分の量は、選択した製品バッチ内の有効成分の濃度から計算されます。</span><span class="sxs-lookup"><span data-stu-id="21d01-105">In the batch balancing process, the amount of ingredients to use in a production batch is calculated from the concentration of active ingredients in selected product batches.</span></span>

<a name="products-that-have-an-active-ingredient"></a><span data-ttu-id="21d01-106">有効成分を有する製品</span><span class="sxs-lookup"><span data-stu-id="21d01-106">Products that have an active ingredient</span></span>
---------------------------------------

<span data-ttu-id="21d01-107">製品は、その有効成分の濃度で定義できます。</span><span class="sxs-lookup"><span data-stu-id="21d01-107">A product can be defined by its concentration of an active ingredient.</span></span> <span data-ttu-id="21d01-108">製品の有効成分は、最小値、最大値、および目標レベルを持つ製品固有のバッチ属性を使用してモデル化されます。</span><span class="sxs-lookup"><span data-stu-id="21d01-108">The active ingredient of a product is modeled by using a product-specific batch attribute that has a minimum value, a maximum value, and a target level.</span></span>

<span data-ttu-id="21d01-109">バッチ属性の目標レベルは、製品内の有効成分の推定割合を表します。</span><span class="sxs-lookup"><span data-stu-id="21d01-109">The target level of a batch attribute represents the estimated percentage of an active ingredient in a product.</span></span> <span data-ttu-id="21d01-110">最小値および最大値は、目標レベルからの許容誤差を表します。</span><span class="sxs-lookup"><span data-stu-id="21d01-110">The minimum and maximum values represent the accepted deviation from the target level.</span></span> <span data-ttu-id="21d01-111">これらをたとえば、製品受領時に許容されるバッチの許容範囲として使用できます。</span><span class="sxs-lookup"><span data-stu-id="21d01-111">They can be used, for example, as an accepted tolerance for batches at product receipt.</span></span>

<span data-ttu-id="21d01-112">製品は 1 つの有効成分のみを有することができます。</span><span class="sxs-lookup"><span data-stu-id="21d01-112">A product can have only one active ingredient.</span></span> <span data-ttu-id="21d01-113">製品の有効成分を指定するには、最初に製品固有のバッチ属性を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21d01-113">To specify the active ingredient of a product, you must first define a product-specific batch attribute.</span></span> <span data-ttu-id="21d01-114">次に、その属性を製品の基本属性として関連付けます。</span><span class="sxs-lookup"><span data-stu-id="21d01-114">You then associate the attribute as a base attribute of the product.</span></span>

<span data-ttu-id="21d01-115">製品レベルでは、製品のバッチに対する有効成分のレベルを記録する方法も指定する必要があります。購買入庫プロセスの一環として、または品質指示プロセスの一環としてです。</span><span class="sxs-lookup"><span data-stu-id="21d01-115">On the product level, you must also specify how the level of the active ingredient for a batch of the product should be recorded: as part of the purchase receipt process or as part of a quality order process.</span></span>

<span data-ttu-id="21d01-116">製品に基準属性を関連付けるには、次の設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="21d01-116">To associate a base attribute with a product, the following setup is required:</span></span>

-   <span data-ttu-id="21d01-117">製品はバッチ管理されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="21d01-117">The product must be batch-controlled.</span></span> <span data-ttu-id="21d01-118">製品をバッチ管理するには、有効なバッチ分析コードを持つ製品に追跡用分析コード グループを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="21d01-118">To make a product batch-controlled, you must assign a tracking dimension group to the product that has an active Batch dimension.</span></span>

-   <span data-ttu-id="21d01-119">成分レベルを示す属性は、製品に対する製品固有のバッチ属性として定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21d01-119">The attribute that indicates the ingredient levels must be defined as a product-specific batch attribute for the product.</span></span>

<span data-ttu-id="21d01-120">[在庫バッチ属性] ページで、バッチの有効成分の実際値を検索して編集することができます。</span><span class="sxs-lookup"><span data-stu-id="21d01-120">You can look up and edit the actual value of the active ingredient for a batch on the **Inventory batch attributes** page.</span></span> 

-  <span data-ttu-id="21d01-121">[在庫管理] \> [照会およびレポート] \> [追跡用分析コード] \> [バッチ] \> [在庫バッチ属性] を選択します。</span><span class="sxs-lookup"><span data-stu-id="21d01-121">Select **Inventory management** \> **Inquiries and reports** \> **Tracking dimensions** \> **Batches** \> **Inventory batch attributes**.</span></span>

<a name="ingredient-types-and-how-they-interact-in-the-batch-balancing-process"></a><span data-ttu-id="21d01-122">成分タイプおよびバッチ バランシング プロセス内でそれらがどのように相互作用するか</span><span class="sxs-lookup"><span data-stu-id="21d01-122">Ingredient types and how they interact in the batch balancing process</span></span>
---------------------------------------------------------------------

<span data-ttu-id="21d01-123">作成されるフォーミュラ明細行はこれらの成分タイプのいずれかを有することができます。</span><span class="sxs-lookup"><span data-stu-id="21d01-123">A formula line that is created can have one of these ingredient types:</span></span>

-   <span data-ttu-id="21d01-124">None</span><span class="sxs-lookup"><span data-stu-id="21d01-124">None</span></span>

-   <span data-ttu-id="21d01-125">使用可能</span><span class="sxs-lookup"><span data-stu-id="21d01-125">Active</span></span>

-   <span data-ttu-id="21d01-126">補償</span><span class="sxs-lookup"><span data-stu-id="21d01-126">Compensating</span></span>

-   <span data-ttu-id="21d01-127">充填剤</span><span class="sxs-lookup"><span data-stu-id="21d01-127">Filler</span></span>

<span data-ttu-id="21d01-128">このセクションの残りの部分では、各成分タイプの仕組みを示す例を示します。</span><span class="sxs-lookup"><span data-stu-id="21d01-128">The rest of this section provides examples that show how each ingredient type works.</span></span> <span data-ttu-id="21d01-129">例では、100 リットルの合計バッチ サイズを有する以下のフォーミュラに基づいています。</span><span class="sxs-lookup"><span data-stu-id="21d01-129">The examples are based on the following formula that has a total batch size of 100 liters.</span></span>

| <span data-ttu-id="21d01-130">**成分タイプ**</span><span class="sxs-lookup"><span data-stu-id="21d01-130">**Ingredient type**</span></span> | <span data-ttu-id="21d01-131">**品目番号**</span><span class="sxs-lookup"><span data-stu-id="21d01-131">**Item number**</span></span> | <span data-ttu-id="21d01-132">[フォーミュラ明細行の数量]</span><span class="sxs-lookup"><span data-stu-id="21d01-132">**Formula line quantity**</span></span> | <span data-ttu-id="21d01-133">**単位**</span><span class="sxs-lookup"><span data-stu-id="21d01-133">**Unit**</span></span> |
|---------------------|-----------------|---------------------------|----------|
| <span data-ttu-id="21d01-134">None</span><span class="sxs-lookup"><span data-stu-id="21d01-134">None</span></span>                | <span data-ttu-id="21d01-135">A</span><span class="sxs-lookup"><span data-stu-id="21d01-135">A</span></span>               | <span data-ttu-id="21d01-136">20</span><span class="sxs-lookup"><span data-stu-id="21d01-136">20</span></span>                        | <span data-ttu-id="21d01-137">リットル</span><span class="sxs-lookup"><span data-stu-id="21d01-137">Liter</span></span>    |
| <span data-ttu-id="21d01-138">使用可能</span><span class="sxs-lookup"><span data-stu-id="21d01-138">Active</span></span>              | <span data-ttu-id="21d01-139">B</span><span class="sxs-lookup"><span data-stu-id="21d01-139">B</span></span>               | <span data-ttu-id="21d01-140">30</span><span class="sxs-lookup"><span data-stu-id="21d01-140">30</span></span>                        | <span data-ttu-id="21d01-141">リットル</span><span class="sxs-lookup"><span data-stu-id="21d01-141">Liter</span></span>    |
| <span data-ttu-id="21d01-142">補償</span><span class="sxs-lookup"><span data-stu-id="21d01-142">Compensating</span></span>        | <span data-ttu-id="21d01-143">C</span><span class="sxs-lookup"><span data-stu-id="21d01-143">C</span></span>               | <span data-ttu-id="21d01-144">10</span><span class="sxs-lookup"><span data-stu-id="21d01-144">10</span></span>                        | <span data-ttu-id="21d01-145">リットル</span><span class="sxs-lookup"><span data-stu-id="21d01-145">Liter</span></span>    |
| <span data-ttu-id="21d01-146">充填剤</span><span class="sxs-lookup"><span data-stu-id="21d01-146">Filler</span></span>              | <span data-ttu-id="21d01-147">D</span><span class="sxs-lookup"><span data-stu-id="21d01-147">D</span></span>               | <span data-ttu-id="21d01-148">40</span><span class="sxs-lookup"><span data-stu-id="21d01-148">40</span></span>                        | <span data-ttu-id="21d01-149">リットル</span><span class="sxs-lookup"><span data-stu-id="21d01-149">Liter</span></span>    |

### <a name="active"></a><span data-ttu-id="21d01-150">使用可能</span><span class="sxs-lookup"><span data-stu-id="21d01-150">Active</span></span>

<span data-ttu-id="21d01-151">基準属性を持つ製品をフォーミュラ行に追加すると、式の*アクティブ成分*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="21d01-151">When a product that has a base attribute is added to a formula line, it's referred to as an *active ingredient* of the formula.</span></span> <span data-ttu-id="21d01-152">バッチ バランシング プロセスに対して、有効成分を含む式を有するバッチ注文を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="21d01-152">Batch orders that have formulas that include active ingredients can be used for the batch balancing process.</span></span> <span data-ttu-id="21d01-153">フォーミュラ内の各成分について、バッチ バランシング プロセスは、製品を生産するために必要な量を見積もります。</span><span class="sxs-lookup"><span data-stu-id="21d01-153">For each ingredient in the formula, the batch balancing process estimates the amount that is required to produce the product.</span></span> <span data-ttu-id="21d01-154">合計量の見積もりは、選択されたバッチ内の有効成分の濃度に基づきます。</span><span class="sxs-lookup"><span data-stu-id="21d01-154">The estimate of amounts is based on the concentration of active ingredients in the selected batches.</span></span>

<span data-ttu-id="21d01-155">**例**</span><span class="sxs-lookup"><span data-stu-id="21d01-155">**Example**</span></span>

<span data-ttu-id="21d01-156">成分 Bは、基準属性 X および目標レベル 30 を有し、100 リットルの製品毎に 30 リットルの成分 B を必要とするフォーミュラに含まれます。</span><span class="sxs-lookup"><span data-stu-id="21d01-156">Ingredient B has base attribute X and a target level of 30, and it's included in a formula that requires 30 liters of ingredient B for every 100 liters of the product.</span></span> <span data-ttu-id="21d01-157">バッチ サイズが 100 リットルのバッチ オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="21d01-157">A batch order is created that has a batch size of 100 liters.</span></span> <span data-ttu-id="21d01-158">バッチ オーダーが開始され、バッチ バランシング プロセスの間に、ユーザーはポテンシー レベル 35 を有する成分 B のバッチを選択します。</span><span class="sxs-lookup"><span data-stu-id="21d01-158">The batch order is started, and during the batch balancing process, the user selects a batch of ingredient B that has a potency level of 35.</span></span> <span data-ttu-id="21d01-159">ポテンシー レベル 35 は目標レベル 30 より高いので、ポテンシー値とバッチの目標レベルの比を使用して、見積数量を乗算することにより、成分 B の残高数量を減らします。</span><span class="sxs-lookup"><span data-stu-id="21d01-159">Because the potency level of 35 is higher than the target level of 30, the balanced quantity of ingredient B is reduced by using the ratio of the potency value to the target level of the batch, which is multiplied by the estimated quantity.</span></span> <span data-ttu-id="21d01-160">残高数量の計算は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="21d01-160">The calculation of the balanced quantity looks like this:</span></span>

<span data-ttu-id="21d01-161">(30 ÷ 35) × 30 リットル = 25.71 リットル</span><span class="sxs-lookup"><span data-stu-id="21d01-161">(30 ÷ 35) × 30 liters = 25.71 liters</span></span>

| <span data-ttu-id="21d01-162">**品目番号**</span><span class="sxs-lookup"><span data-stu-id="21d01-162">**Item number**</span></span> | <span data-ttu-id="21d01-163">**成分タイプ**</span><span class="sxs-lookup"><span data-stu-id="21d01-163">**Ingredient type**</span></span> | <span data-ttu-id="21d01-164">**見積済数量**</span><span class="sxs-lookup"><span data-stu-id="21d01-164">**Estimated quantity**</span></span> | <span data-ttu-id="21d01-165">**残高数量**</span><span class="sxs-lookup"><span data-stu-id="21d01-165">**Balanced quantity**</span></span> | <span data-ttu-id="21d01-166">**有効な数量**</span><span class="sxs-lookup"><span data-stu-id="21d01-166">**Active quantity**</span></span> | <span data-ttu-id="21d01-167">**単位**</span><span class="sxs-lookup"><span data-stu-id="21d01-167">**Unit**</span></span> | <span data-ttu-id="21d01-168">**基準額**</span><span class="sxs-lookup"><span data-stu-id="21d01-168">**Base value**</span></span> |
|-----------------|---------------------|------------------------|-----------------------|---------------------|----------|----------------|
| <span data-ttu-id="21d01-169">A</span><span class="sxs-lookup"><span data-stu-id="21d01-169">A</span></span>               | <span data-ttu-id="21d01-170">None</span><span class="sxs-lookup"><span data-stu-id="21d01-170">None</span></span>                | <span data-ttu-id="21d01-171">20</span><span class="sxs-lookup"><span data-stu-id="21d01-171">20</span></span>                     | <span data-ttu-id="21d01-172">20</span><span class="sxs-lookup"><span data-stu-id="21d01-172">20</span></span>                    |                     | <span data-ttu-id="21d01-173">リットル</span><span class="sxs-lookup"><span data-stu-id="21d01-173">Liter</span></span>    |                |
| <span data-ttu-id="21d01-174">B</span><span class="sxs-lookup"><span data-stu-id="21d01-174">B</span></span>               | <span data-ttu-id="21d01-175">使用可能</span><span class="sxs-lookup"><span data-stu-id="21d01-175">Active</span></span>              | <span data-ttu-id="21d01-176">30</span><span class="sxs-lookup"><span data-stu-id="21d01-176">30</span></span>                     | <span data-ttu-id="21d01-177">25.71</span><span class="sxs-lookup"><span data-stu-id="21d01-177">25.71</span></span>                 | <span data-ttu-id="21d01-178">9.00</span><span class="sxs-lookup"><span data-stu-id="21d01-178">9.00</span></span>                | <span data-ttu-id="21d01-179">リットル</span><span class="sxs-lookup"><span data-stu-id="21d01-179">Liter</span></span>    | <span data-ttu-id="21d01-180">30.00</span><span class="sxs-lookup"><span data-stu-id="21d01-180">30.00</span></span>          |
| <span data-ttu-id="21d01-181">C</span><span class="sxs-lookup"><span data-stu-id="21d01-181">C</span></span>               | <span data-ttu-id="21d01-182">補償</span><span class="sxs-lookup"><span data-stu-id="21d01-182">Compensating</span></span>        | <span data-ttu-id="21d01-183">10</span><span class="sxs-lookup"><span data-stu-id="21d01-183">10</span></span>                     | <span data-ttu-id="21d01-184">14.72</span><span class="sxs-lookup"><span data-stu-id="21d01-184">14.72</span></span>                 |                     | <span data-ttu-id="21d01-185">リットル</span><span class="sxs-lookup"><span data-stu-id="21d01-185">Liter</span></span>    |                |
| <span data-ttu-id="21d01-186">D</span><span class="sxs-lookup"><span data-stu-id="21d01-186">D</span></span>               | <span data-ttu-id="21d01-187">充填剤</span><span class="sxs-lookup"><span data-stu-id="21d01-187">Filler</span></span>              | <span data-ttu-id="21d01-188">40</span><span class="sxs-lookup"><span data-stu-id="21d01-188">40</span></span>                     | <span data-ttu-id="21d01-189">39.57</span><span class="sxs-lookup"><span data-stu-id="21d01-189">39.57</span></span>                 |                     | <span data-ttu-id="21d01-190">リットル</span><span class="sxs-lookup"><span data-stu-id="21d01-190">Liter</span></span>    |                |

### <a name="none"></a><span data-ttu-id="21d01-191">None</span><span class="sxs-lookup"><span data-stu-id="21d01-191">None</span></span>

<span data-ttu-id="21d01-192">成分タイプが [なし] のときにバッチ バランシング プロセスを適用すると、バッチ注文の見積数量およびフォーミュラー明細行の残高数量は同じになります。</span><span class="sxs-lookup"><span data-stu-id="21d01-192">When you apply the batch balancing process when the ingredient type is **None**, the estimated quantity and the balanced quantity of the formula line in the batch order are the same.</span></span>

<span data-ttu-id="21d01-193">**例**</span><span class="sxs-lookup"><span data-stu-id="21d01-193">**Example**</span></span>

<span data-ttu-id="21d01-194">成分 A は [なし] のタイプの成分に割り当てられ、完成品のフォーミュラに追加されます。</span><span class="sxs-lookup"><span data-stu-id="21d01-194">Ingredient A is assigned to an ingredient of the **None** type and added to a formula for a finished product.</span></span> <span data-ttu-id="21d01-195">フォーミュラは、完成品 100 リットルにつき 10 リットルの成分 A を必要とします。</span><span class="sxs-lookup"><span data-stu-id="21d01-195">The formula requires 10 liters of ingredient A for every 100 liters of the finished product.</span></span> <span data-ttu-id="21d01-196">バッチ オーダーが 200 リットルを必要とする場合、見積数量および成分 A の残高数量はともに 20 リットルとして計算されます。</span><span class="sxs-lookup"><span data-stu-id="21d01-196">When a batch order requires 200 liters, both the estimated quantity and the balanced quantity of ingredient A are calculated as 20 liters.</span></span>

### <a name="compensating"></a><span data-ttu-id="21d01-197">補償</span><span class="sxs-lookup"><span data-stu-id="21d01-197">Compensating</span></span>

<span data-ttu-id="21d01-198">補償成分は、製品中の有効成分の効果を相殺または補完することができる。</span><span class="sxs-lookup"><span data-stu-id="21d01-198">A compensating ingredient can either offset or complement the effect of the active ingredient in a product.</span></span> <span data-ttu-id="21d01-199">そのため、消費される補償成分の量は、製品のポテンシーに依存します。</span><span class="sxs-lookup"><span data-stu-id="21d01-199">Therefore, the quantity of a compensating ingredient that is consumed depends on the potency of the product:</span></span>

-   <span data-ttu-id="21d01-200">**反対の効果** － 有効成分の量が予想より多い場合は、補償成分の追加量を少なくしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="21d01-200">**Opposing effect** – If the amount of the active ingredient is more than anticipated, you must add less of the compensating ingredient.</span></span>

-   <span data-ttu-id="21d01-201">**補助効果** － 有効成分の量が予想より少ない場合は、補償成分の追加量を多くしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="21d01-201">**Complementary effect** – If the amount of the active ingredient is less than anticipated, you must add more of the compensating ingredient.</span></span>

<span data-ttu-id="21d01-202">有効成分および補助効果の間の関係が [補償原則] ページで設定されています。</span><span class="sxs-lookup"><span data-stu-id="21d01-202">The relation between an active ingredient and a complementary ingredient is set up on the **Compensating principle** page.</span></span>

<span data-ttu-id="21d01-203">成分間の関係を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="21d01-203">Follow these steps to set up relations between ingredients.</span></span>

1.  <span data-ttu-id="21d01-204">[製品情報管] \> [表、部品およびフォーミュラ] \> [フォーミュラ] を選択し、フォーミュラ明細行を開きます。そして [補償原則] ページを開くために [成分] を選択します。</span><span class="sxs-lookup"><span data-stu-id="21d01-204">Select **Product information management** \> **Bills and materials and formulas** \> **Formulas**, open a formula line, and then select **Ingredients** to open the **Compensating principle** page.</span></span>

2.  <span data-ttu-id="21d01-205">補償原則を表す明細行を選択し、補正する有効成分を選択します。</span><span class="sxs-lookup"><span data-stu-id="21d01-205">Select the line that represents a compensating principle, and then select the active ingredient to compensate.</span></span>

>   <span data-ttu-id="21d01-206">補償原則では、正または負の補償係数を入力し、補償する量の指定および、その原則が反対であるか補完的であるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="21d01-206">In the compensating principle, you also enter a positive or negative compensating factor to specify how much to compensate for, and whether the principle should be opposing or complementary.</span></span> <span data-ttu-id="21d01-207">正の係数は補助効果を示し、負の係数は反対の効果を示す。</span><span class="sxs-lookup"><span data-stu-id="21d01-207">A positive factor indicates a complementary effect, and a negative factor indicates an opposing effect.</span></span>

<span data-ttu-id="21d01-208">**例**</span><span class="sxs-lookup"><span data-stu-id="21d01-208">**Example**</span></span>

<span data-ttu-id="21d01-209">成分 B は、基準属性 X および目標レベル 30 を有する有効成分である。</span><span class="sxs-lookup"><span data-stu-id="21d01-209">Ingredient B is an active ingredient that has base attribute X and a target level of 30.</span></span> <span data-ttu-id="21d01-210">それは 100 リットルの製品ごとに 30 リットルの成分 B を必要とするフォーミュラに含まれています。</span><span class="sxs-lookup"><span data-stu-id="21d01-210">It's included in a formula that requires 30 liters of ingredient B for every 100 liters of the product.</span></span> <span data-ttu-id="21d01-211">成分 C は補償成分であり、数量 10 が同じフォーミュラに含まれます。</span><span class="sxs-lookup"><span data-stu-id="21d01-211">Ingredient C is a compensating ingredient, and a quantity of 10 is included in the same formula.</span></span> <span data-ttu-id="21d01-212">補償原則 には 1.10 の補償係数が設定されています。</span><span class="sxs-lookup"><span data-stu-id="21d01-212">A compensating factor of 1.10 is set up for the compensating principle.</span></span> <span data-ttu-id="21d01-213">したがって、補償成分の残高数量は、有効成分の残高数量と推定必要量に 1.10 を掛けたものの差によって減少します。</span><span class="sxs-lookup"><span data-stu-id="21d01-213">Therefore, the balanced quantity of the compensating ingredient will be reduced by the difference between the active ingredient's balanced quantity and the estimated required quantity multiplied by 1.10.</span></span>

<span data-ttu-id="21d01-214">**有効**成分タイプの例では、必要な有効成分の残高数量は 25.71 として計算され、推定必要量は 30 として計算されました。</span><span class="sxs-lookup"><span data-stu-id="21d01-214">In the example for the **Active** ingredient type, the balanced quantity of the required active ingredient was calculated as 25.71, and the estimated required quantity was calculated as 30.</span></span> <span data-ttu-id="21d01-215">この場合、補償成分の残高数量は次のように計算されます。</span><span class="sxs-lookup"><span data-stu-id="21d01-215">In this case, the balanced quantity of the compensating ingredient will be calculated like this:</span></span>

1.  <span data-ttu-id="21d01-216">見積数量と残高数量との差が決定されます。</span><span class="sxs-lookup"><span data-stu-id="21d01-216">The difference between the estimated and the balanced quantity is determined:</span></span>

>   <span data-ttu-id="21d01-217">25.71 – 30 = –4.29</span><span class="sxs-lookup"><span data-stu-id="21d01-217">25.71 – 30 = –4.29</span></span>

2.  <span data-ttu-id="21d01-218">結果に補償係数が乗算されます。</span><span class="sxs-lookup"><span data-stu-id="21d01-218">The result is multiplied by the compensating factor:</span></span>

>   <span data-ttu-id="21d01-219">4.29 × 1.10 = –4.72</span><span class="sxs-lookup"><span data-stu-id="21d01-219">4.29 × 1.10 = –4.72</span></span>

3.  <span data-ttu-id="21d01-220">見積済の補償数量は、補償数量残高を決定するために –4.72 が差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="21d01-220">The estimated compensating quantity is reduced by –4.72 to determine the balanced compensating quantity:</span></span>

>   <span data-ttu-id="21d01-221">10 – (–4.72) = 14.72</span><span class="sxs-lookup"><span data-stu-id="21d01-221">10 – (–4.72) = 14.72</span></span>

<span data-ttu-id="21d01-222">1.10は正の補償係数であるため、この補償原則には補助的な効果があります。</span><span class="sxs-lookup"><span data-stu-id="21d01-222">Because 1.10 is a positive compensating factor, this compensating principle has a complementary effect.</span></span> <span data-ttu-id="21d01-223">この場合、有効成分は予想より強力です。</span><span class="sxs-lookup"><span data-stu-id="21d01-223">In this case, the active ingredient is more potent than anticipated.</span></span> <span data-ttu-id="21d01-224">したがって、1 つ以上の補償成分が必要です。</span><span class="sxs-lookup"><span data-stu-id="21d01-224">Therefore, more of the compensating ingredient is required.</span></span>

### <a name="filler"></a><span data-ttu-id="21d01-225">充填剤</span><span class="sxs-lookup"><span data-stu-id="21d01-225">Filler</span></span>

<span data-ttu-id="21d01-226">*充填成分*は、完成品の要求する出来高数量に達するために使用される中性成分です。</span><span class="sxs-lookup"><span data-stu-id="21d01-226">A *filler ingredient* is a neutral ingredient that is used to reach the desired output quantity of the finished product.</span></span> <span data-ttu-id="21d01-227">充填量の調整は、標準量と比較した有効成分および補償成分の変動に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="21d01-227">Adjustments to filler quantities are calculated based on variations in the active ingredient and the compensating ingredient compared to the standard quantity.</span></span>

<span data-ttu-id="21d01-228">**例**</span><span class="sxs-lookup"><span data-stu-id="21d01-228">**Example**</span></span>

<span data-ttu-id="21d01-229">100 リットルのフォーミュラ サイズの、成分 A、B、C、D を含む製品を作成しました。</span><span class="sxs-lookup"><span data-stu-id="21d01-229">You've formulated a product that includes ingredients A, B, C, and D for a formula size of 100 liters.</span></span> <span data-ttu-id="21d01-230">1 行に使用される**充填**成分タイプ以外のすべての成分タイプの残高数量を計算しました。</span><span class="sxs-lookup"><span data-stu-id="21d01-230">You've calculated the balanced quantity of all the ingredient types except the **Filler** ingredient type that is used on one line.</span></span>
<span data-ttu-id="21d01-231">充填成分の残高数量は、100 リットルのバッチ サイズと成分 A、B および C の合計との差として計算されます。</span><span class="sxs-lookup"><span data-stu-id="21d01-231">The balanced quantity of the filler ingredient is calculated as the difference between the batch size of 100 liters and the sum of ingredients A, B, and C:</span></span>

<span data-ttu-id="21d01-232">100 – (20 + 25.71 + 14.72) = 39.57</span><span class="sxs-lookup"><span data-stu-id="21d01-232">100 – (20 + 25.71 + 14.72) = 39.57</span></span>

<a name="the-batch-balancing-process"></a><span data-ttu-id="21d01-233">バッチ バランシング プロセス</span><span class="sxs-lookup"><span data-stu-id="21d01-233">The batch balancing process</span></span>
---------------------------

<span data-ttu-id="21d01-234">バッチ バランシング プロセスは、[バッチ バランシング] ページから実行されます。</span><span class="sxs-lookup"><span data-stu-id="21d01-234">The batch balancing process is performed from the **Batch balancing** page.</span></span>
<span data-ttu-id="21d01-235">[原価管理] \> [バッチ オーダー] を選択し、そして [プロセス] タブ上で [バッチ バランシング] を選択します。</span><span class="sxs-lookup"><span data-stu-id="21d01-235">Select **Cost management** \> **Batch orders**, and then, on the **Process** tab, select **Batch balancing**.</span></span> <span data-ttu-id="21d01-236">バッチ バランシングは、ステータスが**開始済**のバッチ オーダーで使用できます。</span><span class="sxs-lookup"><span data-stu-id="21d01-236">Batch balancing is available for batch orders that have a status of **Started**.</span></span>

<span data-ttu-id="21d01-237">一般的に、成分タイプが **有効**の少なくとも 1 つのフォーミュラ明細行を含む場合、バッチ バランシングをバッチ オーダーに適用することができます。</span><span class="sxs-lookup"><span data-stu-id="21d01-237">In general, batch balancing can be applied to batch orders if the formula has at least one formula line where the ingredient type is **Active**.</span></span> <span data-ttu-id="21d01-238">(このルールの例外については、このトピックの後半の「バッチ バランシングには適用されないバッチ オーダー」を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="21d01-238">(For the exception to this rule, see the "Batch orders that aren't applicable for batch balancing" section later in this topic.)</span></span>

<span data-ttu-id="21d01-239">バッチ バランシング プロセスは、2つのサブプロセスに分割することができます。</span><span class="sxs-lookup"><span data-stu-id="21d01-239">The batch balancing process can be divided into two subprocesses:</span></span>

1.  <span data-ttu-id="21d01-240">バッチ成分のバランス</span><span class="sxs-lookup"><span data-stu-id="21d01-240">Balance batch ingredients</span></span>

2.  <span data-ttu-id="21d01-241">フォーミュラの確認およびリリース</span><span class="sxs-lookup"><span data-stu-id="21d01-241">Confirm and release the formula</span></span>

### <a name="balance-batch-ingredients"></a><span data-ttu-id="21d01-242">バッチ成分のバランス</span><span class="sxs-lookup"><span data-stu-id="21d01-242">Balance batch ingredients</span></span>

<span data-ttu-id="21d01-243">バッチ成分のバランス サブプロセスでは、生産バッチに使用する成分の量が、有効成分を含む選択されたバッチに基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="21d01-243">In the Balance batch ingredients subprocess, the amount of ingredients to use for the production batch is calculated based on the selected batches that have active ingredients.</span></span> <span data-ttu-id="21d01-244">原則として、すべての成分を完全にカバーする場合にのみ計算を完了できます</span><span class="sxs-lookup"><span data-stu-id="21d01-244">As a rule, the calculation can be completed only if there is full coverage of all ingredients.</span></span> <span data-ttu-id="21d01-245">バッチ オーダーが生産のために設定されているバッチの一部だけをバランスさせることはできません。</span><span class="sxs-lookup"><span data-stu-id="21d01-245">You can't balance only part of the batch that the batch order is set up to produce.</span></span>

[!NOTE]
<span data-ttu-id="21d01-246">計算を保存し、後にバッチ バランシング プロセスを完了することはできません。</span><span class="sxs-lookup"><span data-stu-id="21d01-246">You can't save a calculation and then complete the batch balancing process later.</span></span> <span data-ttu-id="21d01-247">[バッチ バランシング] ページを閉じると、プロセスを完了するために計算を繰り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="21d01-247">If you close the **Batch balancing** page, you must repeat the calculation to complete the process.</span></span>

### <a name="confirm-and-release-the-formula"></a><span data-ttu-id="21d01-248">フォーミュラの確認およびリリース</span><span class="sxs-lookup"><span data-stu-id="21d01-248">Confirm and release the formula</span></span>

<span data-ttu-id="21d01-249">成分量が計算された後、フォーミュラを確認してリリースすることができます。</span><span class="sxs-lookup"><span data-stu-id="21d01-249">After the ingredient quantities have been calculated, you can confirm and release the formula.</span></span> <span data-ttu-id="21d01-250">リリース プロセスは、製品が倉庫管理プロセスに対して有効化されているかどうかに応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="21d01-250">The release process differs, depending on whether the products are enabled for the warehouse management processes:</span></span>

-   <span data-ttu-id="21d01-251">製品が倉庫管理プロセスに対して有効になっている場合、倉庫管理プロセスの原則に従って、フォーミュラ明細行が倉庫にリリースされます。</span><span class="sxs-lookup"><span data-stu-id="21d01-251">If a product is enabled for the warehouse management processes, the formula line is released to the warehouse according to the principles for the warehouse management processes.</span></span> <span data-ttu-id="21d01-252">フォーミュラ明細行が残高数量と一致する数量単位でリリースされ、有効成分に対して選択された、特定のバッチに対してリリースされます。</span><span class="sxs-lookup"><span data-stu-id="21d01-252">The formula line is released in quantities that match the balanced quantities, and it's released for the specific batches that are selected for the active ingredients.</span></span>

>   [!NOTE]
>   <span data-ttu-id="21d01-253">フォーミュラ明細行をバッチ バランシング プロセスの一部としてのみ倉庫にリリースすることができます。</span><span class="sxs-lookup"><span data-stu-id="21d01-253">Formula lines can be released to warehouse only as part of the batch balancing process.</span></span> <span data-ttu-id="21d01-254">生産用の材料を倉庫にリリースするためのオプションはありますが、これらのオプションはフォーミュラ明細行には使用できません。</span><span class="sxs-lookup"><span data-stu-id="21d01-254">Although there are other options for releasing materials for production to warehouse, those options can't be used for formula lines.</span></span>

-   <span data-ttu-id="21d01-255">製品が倉庫管理プロセスに対して有効になっていない場合は、フォーミュラを確認してリリースするときに、製品の生産ピッキング リストが製品に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="21d01-255">If a product isn't enabled for the warehouse management processes, a production picking list is created for the product when you confirm and release the formula.</span></span>

<span data-ttu-id="21d01-256">単一のフォーミュラで、倉庫管理プロセスで有効になっている製品と、倉庫管理プロセスでは有効になっていない製品を組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="21d01-256">In a single formula, you can combine products that are enabled for the warehouse management processes and products that aren't enabled for the warehouse management processes.</span></span> <span data-ttu-id="21d01-257">2 種類の製品が 1 つのフォーミュラに含まれている場合、倉庫管理プロセスで使用可能になっている製品は倉庫にリリースされます。</span><span class="sxs-lookup"><span data-stu-id="21d01-257">When the two types of products are included in one formula, the products that are enabled for the warehouse management processes are released to warehouse.</span></span> <span data-ttu-id="21d01-258">倉庫管理プロセスに対して有効になっていない製品に対しては、フォーミュラが確認およびリリースされたときにピッキング リストが作成されます。</span><span class="sxs-lookup"><span data-stu-id="21d01-258">For the products that aren't enabled for the warehouse management processes, a picking list is created when the formula is confirmed and released.</span></span>

### <a name="batch-orders-that-arent-applicable-for-batch-balancing"></a><span data-ttu-id="21d01-259">バッチ バランシングには適用されないバッチ注文</span><span class="sxs-lookup"><span data-stu-id="21d01-259">Batch orders that aren't applicable for batch balancing</span></span>

<span data-ttu-id="21d01-260">成分タイプが**有効**のフォーミュラ明細行を少なくとも 1 つ含む場合、バッチ オーダがバッチ バランシングに適用されるというルールに対して例外が 1 つあります。</span><span class="sxs-lookup"><span data-stu-id="21d01-260">There is one exception to the rule that batch orders are applicable for batch balancing if the formula has at least one formula line where the ingredient type is **Active**.</span></span>

<span data-ttu-id="21d01-261">倉庫管理プロセスに対して有効な製品の有効成分がフォーミュラに含まれていても、バッチ番号が引当階層の場所の下にある場合、バッチ注文はバッチ バランシングには適用されません。</span><span class="sxs-lookup"><span data-stu-id="21d01-261">If a formula contains an active ingredient for a product that is enabled for the warehouse management processes, but Batch number is below Location in the reservation hierarchy, the batch order isn't applicable for batch balancing.</span></span>

<span data-ttu-id="21d01-262">バッチ バランシングに適用できないバッチ オーダーは、バッチ オーダーのための通常のプロセス サイクルが実行されます。</span><span class="sxs-lookup"><span data-stu-id="21d01-262">A batch order that isn't applicable for batch balancing goes through the regular process cycle for batch orders.</span></span>
