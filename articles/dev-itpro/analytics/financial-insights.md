---
title: "財務インサイト"
description: "財務インサイトは、Microsoft Power BIを使用して、財務の主要業績評価指標 (KPI)、グラフ、および財務諸表を結び付けます。"
author: kweekley
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 8075abccdcdde21df967dcc9948a738895f35cef
ms.openlocfilehash: 3da5344ec6edec0af28aa21d45af962307231e67
ms.contentlocale: ja-jp
ms.lasthandoff: 01/25/2018

---

# <a name="financial-insights"></a><span data-ttu-id="e2ace-103">財務インサイト</span><span class="sxs-lookup"><span data-stu-id="e2ace-103">Financial Insights</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e2ace-104">**財務インサイト** は、Microsoft Power BIを使用して、財務の主要業績評価指標 (KPI)、グラフ、および財務諸表を結び付けます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-104">**Financial Insights** uses Microsoft Power BI to bring together financial key performance indicators (KPIs), charts, and financial statements.</span></span> <span data-ttu-id="e2ace-105">Microsoft Dynamics 365 Finance and Operations Enterprise Edition に埋め込まれている Power BI。</span><span class="sxs-lookup"><span data-stu-id="e2ace-105">Power BI is embedded in Microsoft Dynamics 365 Finance and Operations, Enterprise edition.</span></span>
<span data-ttu-id="e2ace-106">**財務インサイト** のフォーカスは分析レポートです。</span><span class="sxs-lookup"><span data-stu-id="e2ace-106">The focus of **Financial Insights** is analytical reporting.</span></span> <span data-ttu-id="e2ace-107">組織全体にわたる役割として、表示、研究、理解、および実行できます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-107">Personas across an organization can view, research, understand, and act.</span></span> 

<span data-ttu-id="e2ace-108">**財務インサイト** は、組織の財務の健全性をより完全に把握できるよう、総勘定元帳および補助元帳からのデータを結合します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-108">**Financial Insights** combines data from the general ledger and subledgers to give a more complete picture of the financial health of an organization.</span></span>

> [!NOTE] 
> <span data-ttu-id="e2ace-109">このドキュメントは、次の Power BI 用語を使用します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-109">This document uses the following Power BI terminology:</span></span>                                                                           
<span data-ttu-id="e2ace-110">**レポート** – すべてのタブですべてのビジュアルが保存されている単一の .pbix ファイル。</span><span class="sxs-lookup"><span data-stu-id="e2ace-110">**Report** – A single .pbix file that all the visuals on all tabs are saved to.</span></span>                                                          
<span data-ttu-id="e2ace-111">**ページ** – 単一の .pbix ファイル内のタブ。</span><span class="sxs-lookup"><span data-stu-id="e2ace-111">**Page** – A tab in a single .pbix file.</span></span> <span data-ttu-id="e2ace-112">各ページには、1 つ以上のビジュアルを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-112">Each page can contain one or more visuals.</span></span>                                                     
<span data-ttu-id="e2ace-113">**ビジュアル** – カード、KPI、チャート、グラフ、マトリックス、または財務諸表などの単一のデータのソース。</span><span class="sxs-lookup"><span data-stu-id="e2ace-113">**Visual** – A single source of data, such as a card, KPI, chart, graph, matrix, or financial statement.</span></span> <span data-ttu-id="e2ace-114">ビジュアルとして財務諸表のあるページは、報告されているデータのサイズがあるため、その他のビジュアルを持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-114">A page that has a financial statement as a visual can have no other visuals, because of the size of the data that is being reported on.</span></span>


<span data-ttu-id="e2ace-115">現在、**財務インサイト** は、有効な法人またはすべての法人のいずれかのデータを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-115">Currently, **Financial Insights** is used to view data for either the active legal entity or all legal entities.</span></span> <span data-ttu-id="e2ace-116">将来のリリースでは、ワークスペースは編集およびビジュアルを作成する Power BI を使用できるところにまで進歩します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-116">In future releases, the workspace will evolve into the place where you can use Power BI to edit and create visuals.</span></span>

<span data-ttu-id="e2ace-117">**CFO の概要** ワークスペースは **財務インサイト** として同じビジュアルを表示しますが、既存のレポートでデータを表示およびフィルター処理することに焦点を合わせています。</span><span class="sxs-lookup"><span data-stu-id="e2ace-117">The **CFO overview** workspace shows the same visuals as **Financial Insights**, but is focused on letting you view and filter the data on existing reports.</span></span> <span data-ttu-id="e2ace-118">将来のリリースでは、**財務インサイト** ワークスペースに新しいビジュアルを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-118">In future releases, you will be able to add new visuals to the **Financial Insights** workspace.</span></span> <span data-ttu-id="e2ace-119">新しいビジュアルは、プロジェクト マネージャーまたは買掛金勘定マネージャーなどの、他のロールに焦点を合わせているワークスペースでも使用できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-119">The new visuals might also be available in workspaces that are focused on other roles, such as project managers or accounts payable managers.</span></span> <span data-ttu-id="e2ace-120">**CFO の概要** ワークスペースは、ロールがアクセスする法人に関係なく、すべての法人のデータを表示し続けます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-120">The **CFO overview** workspace continues to show data for all legal entities, regardless of the legal entities that the role has access to.</span></span>

## <a name="finance-and-operations-setup"></a><span data-ttu-id="e2ace-121">Finance and Operations 設定</span><span class="sxs-lookup"><span data-stu-id="e2ace-121">Finance and Operations setup</span></span>
<span data-ttu-id="e2ace-122">**一般会計**</span><span class="sxs-lookup"><span data-stu-id="e2ace-122">**General ledger**</span></span>

<span data-ttu-id="e2ace-123">主勘定タイプおよび主勘定カテゴリは、**財務インサイト** の **賃借対照表** 財務諸表およびさまざまな **損益計算書** 財務諸表で、適切な既定の主勘定を入力して使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-123">The main account type and the main account categories are used to fill in appropriate default main accounts on the **Balance sheet** financial statement and the various **Income statement** financial statements in **Financial Insights**.</span></span>

<span data-ttu-id="e2ace-124">**主勘定** ページで、次のいずれかのタイプを割り当てるよう、勘定を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-124">On the **Main accounts** page, you must define your main account so that one of the following types is assigned to it:</span></span>

<span data-ttu-id="e2ace-125">•   収益</span><span class="sxs-lookup"><span data-stu-id="e2ace-125">•   Revenue</span></span>

<span data-ttu-id="e2ace-126">•   経費</span><span class="sxs-lookup"><span data-stu-id="e2ace-126">•   Expense</span></span>

<span data-ttu-id="e2ace-127">•   資産</span><span class="sxs-lookup"><span data-stu-id="e2ace-127">•   Assets</span></span>

<span data-ttu-id="e2ace-128">•   負債</span><span class="sxs-lookup"><span data-stu-id="e2ace-128">•   Liabilities</span></span>

<span data-ttu-id="e2ace-129">•   株主資本</span><span class="sxs-lookup"><span data-stu-id="e2ace-129">•   Equity</span></span>

<span data-ttu-id="e2ace-130">主要な勘定に、**賃借対照表** または **損益** など他の主勘定タイプを割り当てないでください。</span><span class="sxs-lookup"><span data-stu-id="e2ace-130">Do not assign any other main account type, such as **Balance sheet** or **Profit and Loss**, to your main accounts.</span></span> <span data-ttu-id="e2ace-131">他の主勘定タイプが割り当てられると、十分な細かさがないため、レポートは主勘定のタイプを決定することができません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-131">Reporting can’t determine the type of main account when other main account types are assigned, because they aren’t granular enough.</span></span> <span data-ttu-id="e2ace-132">財務諸表で正の金額として負債および収益を表示するため、主勘定のタイプを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-132">The type of main account must be determined to show liabilities and revenue as positive amounts on financial reports.</span></span>

<span data-ttu-id="e2ace-133">財務諸表に表示して、KPI など他のさまざまなビジュアルに含まれるには、各主勘定が主勘定カテゴリに割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-133">To appear on the financial statements and to be included in various other visuals, such as KPIs, each main account must be assigned a main account category.</span></span> <span data-ttu-id="e2ace-134">表示順序が含まれるよう、主勘定カテゴリが強化されました。</span><span class="sxs-lookup"><span data-stu-id="e2ace-134">The main account categories have been enhanced so that they include a display order.</span></span> <span data-ttu-id="e2ace-135">表示順序は、**財務インサイト** の財務諸表で詳細に使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-135">The display order is used specifically on financial statements in **Financial Insights**.</span></span> <span data-ttu-id="e2ace-136">編集または新しい主勘定カテゴリを追加した後に、主勘定カテゴリが財務諸表に表示されるべき注文を定義する、**表示順序** 値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-136">After you edit or add a new main account category, you can change the **Display order** value to define the order that the main account categories should be shown in on a financial statement.</span></span> <span data-ttu-id="e2ace-137">多くの主勘定カテゴリの表示順序を変更する必要がある場合は、変更をすばやく編集および公開して Finance and Operations に戻すよう、[Excel で開く] 機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-137">If you must change the display order for many main account categories, you can use the Open in Excel feature to quickly edit and publish the changes back to Finance and Operations.</span></span>


## <a name="entity-store"></a><span data-ttu-id="e2ace-138">エンティティ格納</span><span class="sxs-lookup"><span data-stu-id="e2ace-138">Entity store</span></span>
<span data-ttu-id="e2ace-139">**財務インサイト** のデータは、エンティティ格納 (**システム管理** > **設定** > **エンティティ格納**) から収集されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-139">The data for **Financial Insights** is pulled from the Entity store (**System administration** > **Setup** > **Entity store**).</span></span> <span data-ttu-id="e2ace-140">**CFO の概要** または **財務インサイト** ワークスペースを開く場合、および次の警告メッセージがビジュアルで表示される場合、エンティティを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-140">If you open the **CFO overview** or **Financial Insights** workspace, and the following warning message appears in the visuals, you must update the entities.</span></span>
 
![警告](./media/Cantdisplay.png)

<span data-ttu-id="e2ace-142">**財務インサイト** および **CFO の概要** ワークスペースでデータを表示するため、次のエンティティを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-142">You must update the following entities to see data in the **Financial Insights** and **CFO overview** workspaces:</span></span>

<span data-ttu-id="e2ace-143">•   CustCollectionsBIMeasurements</span><span class="sxs-lookup"><span data-stu-id="e2ace-143">•   CustCollectionsBIMeasurements</span></span>

<span data-ttu-id="e2ace-144">•   FinancialReportingOtherData</span><span class="sxs-lookup"><span data-stu-id="e2ace-144">•   FinancialReportingOtherData</span></span>

<span data-ttu-id="e2ace-145">•   FinancialReportingReferenceData</span><span class="sxs-lookup"><span data-stu-id="e2ace-145">•   FinancialReportingReferenceData</span></span>

<span data-ttu-id="e2ace-146">•   FinancialReportingTransactionData</span><span class="sxs-lookup"><span data-stu-id="e2ace-146">•   FinancialReportingTransactionData</span></span>

<span data-ttu-id="e2ace-147">•   LedgerCovLiquidityMeasurement</span><span class="sxs-lookup"><span data-stu-id="e2ace-147">•   LedgerCovLiquidityMeasurement</span></span>

<span data-ttu-id="e2ace-148">•   購買キューブ</span><span class="sxs-lookup"><span data-stu-id="e2ace-148">•   Purchase cube</span></span>

<span data-ttu-id="e2ace-149">•   売上キューブ</span><span class="sxs-lookup"><span data-stu-id="e2ace-149">•   Sales cube</span></span>

<span data-ttu-id="e2ace-150">以前のリリースでは、LedgerActivityMeasure および VendPaymentBIMeasure エンティティが **CFO の概要** ワークスペースでデータに対して使用されていました。</span><span class="sxs-lookup"><span data-stu-id="e2ace-150">In the previous release, the LedgerActivityMeasure and VendPaymentBIMeasure entities were used for data in the **CFO overview** workspace.</span></span> <span data-ttu-id="e2ace-151">ただし、それらは現在のリリースで使用されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="e2ace-151">However, they are no longer used in the current release.</span></span>

<span data-ttu-id="e2ace-152">エンティティでデータを定期的に更新するため、定期実行されるバッチを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-152">You can define a recurring batch to regularly update the data in the entities.</span></span> <span data-ttu-id="e2ace-153">なぜなら各エンティティは、更新時に完全に再構築されるため、エンティティ更新の時間と頻度を慎重に選択します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-153">Because each entity is completely rebuilt during an update, select the time and frequency of entity updates carefully.</span></span> <span data-ttu-id="e2ace-154">財務諸表に使用される基本エンティティは、FinancialReportingTransactionData エンティティです。</span><span class="sxs-lookup"><span data-stu-id="e2ace-154">The primary entity that is used for financial statements is the FinancialReportingTransactionData entity.</span></span> <span data-ttu-id="e2ace-155">したがって、そのエンティティをより頻繁に更新するよう決定するかもしれません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-155">Therefore, you might decide to update that entity more often.</span></span>

## <a name="security"></a><span data-ttu-id="e2ace-156">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="e2ace-156">Security</span></span>
<span data-ttu-id="e2ace-157">現在、埋め込み Power BI レポートのデータは、ユーザーがアクセスする法人に限定することはできません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-157">Currently, the data on embedded Power BI reports can’t be limited to the legal entities that the user has access to.</span></span> <span data-ttu-id="e2ace-158">したがって、埋め込み Power BI レポートは、セキュリティ設定での職務によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-158">Therefore, the embedded Power BI reports are controlled through duties in the security setup.</span></span> <span data-ttu-id="e2ace-159">定義されている職務は、すべての法人または有効な会社のみのいずれかのデータへのアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-159">The duties that are defined allow access to data for either all legal entities or only the active company.</span></span> <span data-ttu-id="e2ace-160">次の表で、既存の職務および割り当てられているロールを示します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-160">The following table shows the duties that exist and the roles that they are assigned to.</span></span> <span data-ttu-id="e2ace-161">組織の要求に基づいて、この職務は削除されたり、またはさまざまなロールに割り当てられたりします。</span><span class="sxs-lookup"><span data-stu-id="e2ace-161">The duties can be removed or assigned to different roles, based on your organization’s requirements.</span></span>

| <span data-ttu-id="e2ace-162">**関税**</span><span class="sxs-lookup"><span data-stu-id="e2ace-162">**Duty**</span></span>                     | <span data-ttu-id="e2ace-163">**ロール**</span><span class="sxs-lookup"><span data-stu-id="e2ace-163">**Roles**</span></span>                                       | <span data-ttu-id="e2ace-164">説明</span><span class="sxs-lookup"><span data-stu-id="e2ace-164">Decription</span></span>                     |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="e2ace-165">CFO の概要ワークスペースの表示</span><span class="sxs-lookup"><span data-stu-id="e2ace-165">View CFO Overview workspace</span></span>  | <span data-ttu-id="e2ace-166">最高財務責任者</span><span class="sxs-lookup"><span data-stu-id="e2ace-166">Chief Financial Officer</span></span>                         | <span data-ttu-id="e2ace-167">•    この職務は、CFO の概要ワークスペースへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-167">•    This duty provides access to the CFO overview workspace.</span></span> <span data-ttu-id="e2ace-168">•  既定では、有効な会社はフィルタとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-168">•  By default, the active company is used as a filter.</span></span> <span data-ttu-id="e2ace-169">ただし、ユーザーが他の法人へのアクセスできるかどうかに関係なく、すべての法人を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-169">However, you can add all legal entities, regardless of whether the user has access to the other legal entities.</span></span>               |
| <span data-ttu-id="e2ace-170">現在の会社間の財務インサイトの表示</span><span class="sxs-lookup"><span data-stu-id="e2ace-170">View financial insights current company</span></span> | <span data-ttu-id="e2ace-171">•   経理担当 •    会計マネージャー •    会計監修者 • 監査担当者 •   予算マネージャー •    最高経営責任者 •   最高財務責任者 •   財務コントローラー</span><span class="sxs-lookup"><span data-stu-id="e2ace-171">•   Accountant •    Accounting manager •    Accounting supervisor • Auditor •   Budget manager •    Chief executive officer •   Chief financial officer •   Financial controller</span></span>  |   <span data-ttu-id="e2ace-172">• この職務は、財務インサイトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-172">• This duty provides access to Financial Insights.</span></span> <span data-ttu-id="e2ace-173">•  既定では、有効な会社はフィルタとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-173">•  By default, the active company is used as a filter.</span></span> <span data-ttu-id="e2ace-174">他の法人を追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-174">You can’t add other legal entities.</span></span>            |
| <span data-ttu-id="e2ace-175">会社間の財務インサイトの表示</span><span class="sxs-lookup"><span data-stu-id="e2ace-175">View financial insights cross company</span></span>   | <span data-ttu-id="e2ace-176">•   Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 で、この職務はロールに割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-176">•   In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, this duty isn’t assigned to a role.</span></span> <span data-ttu-id="e2ace-177">• 次のリリースで、最高財務責任者ロールにこの職務が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-177">• In the next release, this duty will be assigned to the Chief financial officer role.</span></span> | <span data-ttu-id="e2ace-178">•    この職務は、CFO の概要ワークスペースのメニュー項目にアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-178">•    This duty provides access to the menu item for the CFO overview workspace.</span></span> <span data-ttu-id="e2ace-179">•    既定では、有効な会社はフィルタとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-179">•    By default, the active company is used as a filter.</span></span> <span data-ttu-id="e2ace-180">ただし、ユーザーが他の法人へのアクセスできるかどうかに関係なく、すべての法人を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-180">However, you can add all legal entities, regardless of whether the user has access to the other legal entities.</span></span>             |


## <a name="how-financial-statements-work"></a><span data-ttu-id="e2ace-181">財務諸表の機能</span><span class="sxs-lookup"><span data-stu-id="e2ace-181">How financial statements work</span></span>
<span data-ttu-id="e2ace-182">**財務インサイト** は財務諸表を含んでいますが、Finance and Operations での財務報告に代わるものはありません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-182">Although **Financial Insights** does contain financial statements, it isn’t a replacement for Financial reporting in Finance and Operations.</span></span> <span data-ttu-id="e2ace-183">**財務インサイト** での既定の財務諸表は、範囲がスコープで制限されており財務諸表のすべてのタイプを含みません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-183">The default financial statements in **Financial Insights** are limited in scope and don’t include all types of financial statements.</span></span> <span data-ttu-id="e2ace-184">財務報告は、法的財務諸表のデザイン、作成、および生成に対する主要なツールです。</span><span class="sxs-lookup"><span data-stu-id="e2ace-184">Financial reporting is still the primary tool for designing, creating, and generating statutory financial statements.</span></span>

<span data-ttu-id="e2ace-185">元の **CFO の概要** ワークスペースからのビジュアルに加えて、新しい KPI、チャート、および財務諸表が使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e2ace-185">In addition to the visuals from the original **CFO overview** workspace, new KPIs, charts, and financial statements are now available.</span></span> <span data-ttu-id="e2ace-186">次の財務諸表を使用できます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-186">The following financial statements are available:</span></span>

<span data-ttu-id="e2ace-187">•   試算表</span><span class="sxs-lookup"><span data-stu-id="e2ace-187">•   Trial balance</span></span>

<span data-ttu-id="e2ace-188">•   貸借対照表</span><span class="sxs-lookup"><span data-stu-id="e2ace-188">•   Balance sheet</span></span>

<span data-ttu-id="e2ace-189">•   地域ごとの損益計算書</span><span class="sxs-lookup"><span data-stu-id="e2ace-189">•   Income statement by region</span></span>

<span data-ttu-id="e2ace-190">•   損益計算書 (実績と予算)</span><span class="sxs-lookup"><span data-stu-id="e2ace-190">•   Income statement actual vs budget</span></span>

<span data-ttu-id="e2ace-191">•   損益計算書の差異</span><span class="sxs-lookup"><span data-stu-id="e2ace-191">•   Income statement with variances</span></span>

<span data-ttu-id="e2ace-192">•   12 か月トレンド損益計算書</span><span class="sxs-lookup"><span data-stu-id="e2ace-192">•   12 month trend income statement</span></span>

<span data-ttu-id="e2ace-193">•   経費の 3 年間トレンド</span><span class="sxs-lookup"><span data-stu-id="e2ace-193">•   Expenses three-year trend</span></span>

<span data-ttu-id="e2ace-194">•   経費 (仕入先別)</span><span class="sxs-lookup"><span data-stu-id="e2ace-194">•   Expenses by vendor</span></span>

<span data-ttu-id="e2ace-195">•   顧客ごとの販売</span><span class="sxs-lookup"><span data-stu-id="e2ace-195">•   Sales by customer</span></span>

## <a name="edit-visuals"></a><span data-ttu-id="e2ace-196">ビジュアルの編集</span><span class="sxs-lookup"><span data-stu-id="e2ace-196">Edit visuals</span></span>
<span data-ttu-id="e2ace-197">**財務インサイト** の初期リリースでは、ビジュアルはいずれも編集できません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-197">In the initial release of **Financial Insights**, none of the visuals can be edited.</span></span> <span data-ttu-id="e2ace-198">将来のリリースでは、適切なセキュリティを持つユーザーが新しいビジュアルを作成し、既存のビジュアルをコピーし、およびビジュアルを編集できます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-198">In future releases, users who have the appropriate security will be able to create new visuals, copy existing visuals, and edit visuals.</span></span> <span data-ttu-id="e2ace-199">レポートを含む .pbix ファイルがリソースとして使用できますが、既定のレポートを編集することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-199">Although the .pbix files that contain the reports are available as resources, we don’t recommend that you edit the default reports.</span></span> <span data-ttu-id="e2ace-200">カスタムの財務諸表の作成に使用されるデータ モデル、既定のレポート、および財務諸表ビジュアルへの追加の変更が行われます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-200">Additional changes will be made to the data model, default reports, and custom financial statement visual that are used to create the financial statements.</span></span> <span data-ttu-id="e2ace-201">したがって、次のリリースのデータ モデルに対する新しい機能および変更を活用するには、Microsoft Power BI Desktop を通して既定のレポートに当てはめた変更を再実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-201">Therefore, to take advantage of new features and changes to the data model in the next release, you will have to redo any changes that you made to the default reports through Microsoft Power BI Desktop.</span></span>


## <a name="filtering"></a><span data-ttu-id="e2ace-202">フィルター処理</span><span class="sxs-lookup"><span data-stu-id="e2ace-202">Filtering</span></span>
<span data-ttu-id="e2ace-203">ユーザーは、左側の **フィルター** ウィンドウを使用して、レポートをフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-203">Users can filter the report by using the **Filter** pane on the left.</span></span> <span data-ttu-id="e2ace-204">このウィンドウは、Power BI Desktop を通して利用可能な同じウィンドウです。</span><span class="sxs-lookup"><span data-stu-id="e2ace-204">This pane is the same pane that is available through Power BI Desktop.</span></span>
<span data-ttu-id="e2ace-205">フィルタリングのさまざまなレベルがあります。そのうちの幾つかは使用できない場合があり、ユーザーがページ (タブ) で何を選択したか、またはドリルスルー機能を使用しているかどうかに依存します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-205">There are various levels of filtering, some of which might not be available, depending on what you’ve selected on a page (tab) or whether you’re using the drill-through capabilities:</span></span>

<span data-ttu-id="e2ace-206">•   **レポート レベルのフィルター** – すべてのページ (タブ) ですべてのビジュアルに対して、これらのフィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-206">•   **Report-level filters** – These filters are applied to all visuals on all pages (tabs).</span></span>

<span data-ttu-id="e2ace-207">•   **ページ レベルのフィルター** – アクティブなタブのすべてのビジュアルに対して、これらのフィルターが適用されます。レポート レベルのフィルターの上部で、これらのフィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-207">•   **Page-level filters** – These filters are applied to all visuals on the active tab. These filters are applied on top of the report-level filters.</span></span>

<span data-ttu-id="e2ace-208">•   **ビジュアル レベルのフィルター** – これらのフィルターは、選択したビジュアルにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-208">•   **Visual-level filters** – These filters are applied only to the selected visual.</span></span> <span data-ttu-id="e2ace-209">これらのフィルターは、ページ レベルのフィルターの上部で適用されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-209">These filters are applied on top of the page level filters.</span></span>

<span data-ttu-id="e2ace-210">•   **ドリルスルーのフィルター** – このフィルターは、ソース ビジュアルから現在のビジュアルにドリルスルーする際、現在のビジュアルに適用される「ソース」ビジュアルからフィルター処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-210">•   **Drill-through filter** – This filter filters from a “source” visual that is applied to the current visual when you drill through from the source visual to the current visual.</span></span>

![フィルター](./media/filter.png)


<span data-ttu-id="e2ace-212">特定のフィルター値を削除するには、横にある消去記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-212">To remove a specific filter value, select the eraser symbol next to it.</span></span> <span data-ttu-id="e2ace-213">X を選択することで、フィルタを削除しないでください。X を選択すると、フィルター オプションとして、フィルター処理しているフィールドが削除されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-213">Don’t remove a filter by selecting the X. If you select the X, the field that you’re filtering on is removed as a filter option.</span></span> <span data-ttu-id="e2ace-214">誤ってフィルターからフィールドを削除してしまった場合は、ワークスペースを閉じて再オープンします。</span><span class="sxs-lookup"><span data-stu-id="e2ace-214">If you accidently remove a field from the filter, close the workspace, and then reopen it.</span></span> <span data-ttu-id="e2ace-215">既定のフィルター設定を再適用します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-215">The default filter settings will be reapplied.</span></span>

<span data-ttu-id="e2ace-216">既定では、ワークスペースを初めて開いたときは、有効な法人がレポート レベルのフィルターとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-216">By default, when you first open workspaces, the active legal entity is used as the report-level filter.</span></span> <span data-ttu-id="e2ace-217">セキュリティによっては、ユーザーは他の法人を追加したり、またはフィルターで選択されている既定の法人を変更できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-217">Depending on their security, users might be able to add other legal entities or change the default legal entity that is selected in the filter.</span></span>

<span data-ttu-id="e2ace-218">**会計カレンダー** フィルターは、ビジュアルに対して正しいカレンダーが使用されるために必要になります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-218">The **Fiscal calendar** filter is required so that the correct calendar is used for the visual.</span></span> <span data-ttu-id="e2ace-219">既定では、レポート レベルのフィルターは、有効な法人の会計カレンダーに設定されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-219">By default, the report-level filter is set to the active legal entity’s fiscal calendar.</span></span> <span data-ttu-id="e2ace-220">別の開始または終了日がある会計カレンダーにフィルターを変更する場合、期首残高は含まれません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-220">If you change the filter to a fiscal calendar that has a different start or end date, the beginning balances won’t be included.</span></span> <span data-ttu-id="e2ace-221">したがって、**賃借対照表** 財務諸表は正確な残高を表示しません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-221">Therefore, your **Balance sheet** financial statements won’t show the correct balances.</span></span> <span data-ttu-id="e2ace-222">フィルタで追加の会計カレンダーを選択した場合は、列の追加のセットがあります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-222">If you select an additional fiscal calendar in the filter, you will have an additional set of columns.</span></span> <span data-ttu-id="e2ace-223">列の各追加のセットは、異なる会計カレンダーの金額を表示します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-223">Each additional set of columns shows the amounts for a different fiscal calendar.</span></span>

<span data-ttu-id="e2ace-224">**転記階層** フィルターも必要になります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-224">The **Posting layer** filter is also required.</span></span> <span data-ttu-id="e2ace-225">既定では、フィルターが [現行] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-225">By default, the filter is set to Current.</span></span> <span data-ttu-id="e2ace-226">フィルターで追加の転記階層を選択して、総額を表示できます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-226">You can select additional posting layers in the filter to show the aggregated amounts.</span></span>

<span data-ttu-id="e2ace-227">フィルターは **日付** および **会計年度** フィールドに対しても利用可能です。</span><span class="sxs-lookup"><span data-stu-id="e2ace-227">Filters are also available for the **Date** and **Fiscal year** fields.</span></span> <span data-ttu-id="e2ace-228">通常、これらのフィルターはページ レベルで適用されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-228">Typically, these filters are applied at the page level.</span></span> <span data-ttu-id="e2ace-229">既定では、**日付** フィルターは、変更できるリレーショナル日付を使用します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-229">By default, the **Date** filter uses a relational date that you can change.</span></span> <span data-ttu-id="e2ace-230">リレーショナル日付のフィルターを削除して、代わりに **会計年度** フィルターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-230">You can also remove the relational date filter and use the **Fiscal year** filter instead.</span></span>

## <a name="currency"></a><span data-ttu-id="e2ace-231">通貨</span><span class="sxs-lookup"><span data-stu-id="e2ace-231">Currency</span></span>

<span data-ttu-id="e2ace-232">総勘定元帳のデータで報告するすべてのビジュアルは、会計通貨で金額を表示します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-232">All visuals that report on general ledger data show amounts in the accounting currency.</span></span> <span data-ttu-id="e2ace-233">したがって、法人でフィルター処理する場合、同じ会計通貨がある法人のみを含めるよう注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-233">Therefore, when you filter on the legal entity, you must be careful to include only legal entities that have the same accounting currency.</span></span> <span data-ttu-id="e2ace-234">それ以外の場合、異なる通貨でデータが集計されてしまいます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-234">Otherwise, you will aggregate data in different currencies.</span></span>

<span data-ttu-id="e2ace-235">**キャッシュ フロー予測** および **上位 10** ビジュアルなどの、補助元帳データでレポートするすべてのビジュアルは、システム通貨で金額を表示します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-235">All visuals that report on subledger data, such as the **Cash flow forecast** and **Top 10** visuals, show amounts in the system currency.</span></span> <span data-ttu-id="e2ace-236">システム通貨およびシステム為替レート タイプは、**システム パラメーター** ページで定義されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-236">The system currency and system exchange rate type are defined on the **System parameters** page.</span></span>

<span data-ttu-id="e2ace-237">**銀行口座ごとの残高** ビジュアルは、銀行口座の通貨で金額を使用します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-237">The **Balance by bank account** visual uses amounts in the bank accounts’ currency.</span></span>

## <a name="dimensions"></a><span data-ttu-id="e2ace-238">分析コード</span><span class="sxs-lookup"><span data-stu-id="e2ace-238">Dimensions</span></span>

<span data-ttu-id="e2ace-239">既定の財務諸表は、任意の財務分析コードを含みませんが、主勘定でのみ焦点を当てています。</span><span class="sxs-lookup"><span data-stu-id="e2ace-239">The default financial statements don’t include any financial dimensions but are focused only on the main account.</span></span> <span data-ttu-id="e2ace-240">レポートが編集可能になるとき、将来のリリースで財務分析コードに対するサポートが利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-240">Support for financial dimensions will be available in future releases, when the reports become editable.</span></span> <span data-ttu-id="e2ace-241">それにより組織は、財務分析コード値でフィルター処理ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-241">Organizations will then be able to filter on financial dimension values.</span></span>

<span data-ttu-id="e2ace-242">一部の財務諸表は、補助元帳トランザクションの基準となる分析コードを含みます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-242">Some financial statements contain dimensions that are based on subledger transactions.</span></span> <span data-ttu-id="e2ace-243">新しい財務諸表の目的は、財務分析コードとして設定されていない分析コードでフィルター処理を有効にすることです。</span><span class="sxs-lookup"><span data-stu-id="e2ace-243">The goal of the new financial statements it to enable filtering on dimensions that aren’t set up as financial dimensions.</span></span> <span data-ttu-id="e2ace-244">たとえば、仕入先レポートによる既定の [経費] は、仕入先によって分割された残高を表示できるよう、主勘定を超えて下方展開できるようにします。</span><span class="sxs-lookup"><span data-stu-id="e2ace-244">For example, the default Expenses by vendor report lets you expand down beyond the main account, so that you can see the balances broken down by vendor.</span></span> <span data-ttu-id="e2ace-245">仕入先は、財務分析コードとして設定されていません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-245">The vendor isn’t set up as a financial dimension.</span></span> <span data-ttu-id="e2ace-246">代わりに、システムは、仕入先を検索する元の補助元帳トランザクションを返します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-246">Instead, the system returns to the originating subledger transaction to find the vendor.</span></span>

<span data-ttu-id="e2ace-247">次の分析コードは、既定のレポートで使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-247">The following dimensions are used on the default reports.</span></span> <span data-ttu-id="e2ace-248">これらの分析コードのどれも財務分析コードではありません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-248">None of these dimensions are financial dimensions.</span></span>

<span data-ttu-id="e2ace-249">•   仕入先</span><span class="sxs-lookup"><span data-stu-id="e2ace-249">•   Vendor</span></span>

<span data-ttu-id="e2ace-250">•   仕入先グループ</span><span class="sxs-lookup"><span data-stu-id="e2ace-250">•   Vendor group</span></span>

<span data-ttu-id="e2ace-251">•   顧客</span><span class="sxs-lookup"><span data-stu-id="e2ace-251">•   Customer</span></span>

<span data-ttu-id="e2ace-252">•   顧客グループ</span><span class="sxs-lookup"><span data-stu-id="e2ace-252">•   Customer group</span></span>

<span data-ttu-id="e2ace-253">•   国/地域</span><span class="sxs-lookup"><span data-stu-id="e2ace-253">•   Country/region</span></span>

<span data-ttu-id="e2ace-254">•   都道府県</span><span class="sxs-lookup"><span data-stu-id="e2ace-254">•   State/province</span></span>

<span data-ttu-id="e2ace-255">•   市町村</span><span class="sxs-lookup"><span data-stu-id="e2ace-255">•   City</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="e2ace-256">財務仕訳帳を使用して複数の仕入先または顧客のトランザクションを単一伝票に集計する場合、データは正確ではありません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-256">If you summarize transactions for multiple vendors or customers in a single voucher by using the financial journals, the data will be incorrect.</span></span> <span data-ttu-id="e2ace-257">どの仕入先または顧客が、仕訳帳入力で特定の勘定科目に関連するかを決定する報告をすることはできません。その情報は任意の場所で管理されていないためです。</span><span class="sxs-lookup"><span data-stu-id="e2ace-257">Reporting can’t determine which vendor or customer is related to a specific ledger account in a journal entry, because that information isn’t maintained anywhere.</span></span> <span data-ttu-id="e2ace-258">したがって、単一伝票に複数の仕入先、顧客、固定資産、またはプロジェクトを入力することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-258">Therefore, we do not recommend that you enter multiple vendors, customers, fixed assets, or projects in a single voucher.</span></span>

## <a name="drill-on-data"></a><span data-ttu-id="e2ace-259">データの表示</span><span class="sxs-lookup"><span data-stu-id="e2ace-259">Drill on data</span></span>

<span data-ttu-id="e2ace-260">Power BI を通して表示のさまざまなレベルが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="e2ace-260">Various levels of drilling are available through Power BI.</span></span> <span data-ttu-id="e2ace-261">各レベルには、異なる名前および機能があります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-261">Each level has a different name and different functionality.</span></span> <span data-ttu-id="e2ace-262">行および列で表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-262">You can also drill on rows and columns.</span></span> <span data-ttu-id="e2ace-263">このセクションでは、**試算表** 財務諸表を例として使用してさまざまなオプションについて説明し、行に表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-263">This section discusses the various options by using the **Trial balance** financial statement as an example and showing how you can drill on the rows.</span></span> <span data-ttu-id="e2ace-264">列に対して同じ機能が存在します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-264">The same functionality exists for columns.</span></span> <span data-ttu-id="e2ace-265">**ドリル オン** 設定を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-265">You just have to change the **Drill on** setting.</span></span>

<span data-ttu-id="e2ace-266">次の図では、**試算表** 明細書は、行階層、主勘定タイプの最上位レベルに折りたたまれています。</span><span class="sxs-lookup"><span data-stu-id="e2ace-266">In the following illustration, the **Trial balance** statement is collapsed to the highest level of the row hierarchy, the main account type.</span></span>

![試算表](./media/trial-balance.png)

 
<span data-ttu-id="e2ace-268">階層、主勘定カテゴリの次のレベルを表示するには、**ドリル オン** フィールドを **行** に設定し、**展開** ボタン ([ドリル オン] フィールド後の 3 番目のボタン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-268">To view the next level of the hierarchy, the main account categories, you can set the **Drill on** field to **Rows** and then select the **Expand** button (the third button after the Drill on field).</span></span> <span data-ttu-id="e2ace-269">展開されたすべての勘定カテゴリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-269">You now see all the main account categories expanded.</span></span> <span data-ttu-id="e2ace-270">現在、Power BI は、1 つの行または列のみを展開できるようにはしませんが、他のすべての行または列を表示します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-270">Currently, Power BI doesn’t let you expand only one row or column but still see all the other rows or columns.</span></span>
 
![試算表](./media/trial-balance2.png)
 
  
<span data-ttu-id="e2ace-272">すべての行の主勘定を展開するには **展開** ボタンをもう一度使用できます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-272">To expand to the main accounts for all rows, you can again use the **Expand** button.</span></span> <span data-ttu-id="e2ace-273">ただし、1 つの行のみに対する主勘定にドリルダウンする場合、まず **ドリルダウン** ボタン (ウィンドウの右側にある単一の下向きの矢印) を選択し、ドリルダウンする行を選択します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-273">However, to drill down to the main accounts for only one row, first select the **Drill down** button (the single downward-pointing arrow on the right side of the window), and then select the row to drill down on.</span></span> <span data-ttu-id="e2ace-274">次の図は、**ドリルダウン** ボタンが選択された後に **販売** 行が選択される場合の結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-274">The following illustration shows the result when the **Sales** row is selected after the **Drill down** button is selected.</span></span>

![試算表](./media/trial-balance3.png)

<span data-ttu-id="e2ace-276">単一行にドリルダウンした後に、完全な試算表を返すために複数回のクリックが必要です。</span><span class="sxs-lookup"><span data-stu-id="e2ace-276">After you drill down on a single row, multiple clicks are required in order to return to the full trial balance.</span></span> <span data-ttu-id="e2ace-277">**ドリルアップ** ボタン (フィールドの **ドリル** 後の最初のボタン ) は、次の図に示すように **販売** カテゴリのコンテキストでのみドリルアップします。</span><span class="sxs-lookup"><span data-stu-id="e2ace-277">The **Drill up** button (the first button after the **Drill** on field) drills up only in the context of the **Sales** category, as shown in the following illustration.</span></span>
 
![試算表](./media/trial-balance4.png)
 
 
<span data-ttu-id="e2ace-279">行の集計の最上位レベルを返すため、**ドリルアップ** ボタンを使用し続けることができます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-279">You can continue to use the **Drill up** button to return to the highest level of summarization for the rows.</span></span>

<span data-ttu-id="e2ace-280">Power BI には、階層 (**ドリル オン** フィールド後の 2 番目のボタン) の次のレベルに移動することができるボタンもあります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-280">Power BI also has a button that lets you go to the next level in the hierarchy (the second button after the **Drill on** field).</span></span> <span data-ttu-id="e2ace-281">このボタンの効果は、階層を展開するのに使用される **展開** ボタン (**ドリル オン** フィールド後の3番目のボタン) の効果とは違います。</span><span class="sxs-lookup"><span data-stu-id="e2ace-281">The effect of this button differs from the effect of the **Expand** button (the third button after the **Drill on** field), which is used to expand the hierarchy.</span></span> <span data-ttu-id="e2ace-282">階層を展開すると、階層はレポートで管理されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-282">When you expand the hierarchy, the hierarchy is maintained on the report.</span></span> <span data-ttu-id="e2ace-283">たとえば、以前に表示したように、主勘定タイプを展開すると、レポートで引き続き主勘定タイプを表示できます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-283">For example, as was shown earlier, if you expand on the main account type, you still see the main account type on the report.</span></span> <span data-ttu-id="e2ace-284">ただし、階層で次のレベルに移動すると、次の図に示すようにレポートは階層内で親を表示しなくなります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-284">However, when you go to the next level in the hierarchy, the report no longer shows the parent in the hierarchy, as shown in the following illustration.</span></span>

![試算表](./media/trial-balance5.png)

 
<span data-ttu-id="e2ace-286">集計された残高の背後にあるトランザクション詳細を表示するため、Financial and Operations にドリルバックする一部の金額を選択できます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-286">To see the transaction details behind the summarized balances, you can select some amounts to drill back into Financial and Operations.</span></span>

<span data-ttu-id="e2ace-287">財務諸表からのドリルバックは、伝票トランザクションにではなく、会計のソース エクスプローラー (ASE) に移動します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-287">The drill-back from the financial statements takes you to the Accounting source explorer (ASE), not to the voucher transactions.</span></span> <span data-ttu-id="e2ace-288">ASE は、総勘定元帳で勘定項目のみを表示しません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-288">The ASE doesn’t show just the accounting entries in the general ledger.</span></span> <span data-ttu-id="e2ace-289">代わりに、補助元帳トランザクションの詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-289">Instead, it shows the details of the subledger transaction.</span></span> <span data-ttu-id="e2ace-290">したがって、元のトランザクションに関するかなりの詳細を取得し、それを分析のために使用できます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-290">Therefore, you get much more detail about the originating transaction and can use it for analysis.</span></span> <span data-ttu-id="e2ace-291">たとえば、仕入先または顧客が誰であったか、顧客が何を購入しまたは仕入先が何を販売したか、およびトランザクションにどんなプロジェクトがあったかなども表示できます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-291">For example, you can see who the vendor or customer was, what the customer bought or the vendor sold, and even what project was on the transaction.</span></span>

<span data-ttu-id="e2ace-292">財務諸表からの次のフィルターは ASE に送信され、集計されたトランザクションを ASE が表示できるようにします。</span><span class="sxs-lookup"><span data-stu-id="e2ace-292">The following filters from the financial statements are sent to the ASE, so that the ASE shows the transactions that are aggregated:</span></span>

<span data-ttu-id="e2ace-293">フィルター処理するための必須フィールド。</span><span class="sxs-lookup"><span data-stu-id="e2ace-293">Required fields for filtering:</span></span>

  - <span data-ttu-id="e2ace-294">個法</span><span class="sxs-lookup"><span data-stu-id="e2ace-294">Legal entity</span></span>
 
  - <span data-ttu-id="e2ace-295">会計カレンダー</span><span class="sxs-lookup"><span data-stu-id="e2ace-295">Fiscal calendar</span></span>
 
  - <span data-ttu-id="e2ace-296">年</span><span class="sxs-lookup"><span data-stu-id="e2ace-296">Year</span></span>
 
  - <span data-ttu-id="e2ace-297">主勘定 ID</span><span class="sxs-lookup"><span data-stu-id="e2ace-297">Main account ID</span></span>

<span data-ttu-id="e2ace-298">フィルター処理するためのオプション フィールド。</span><span class="sxs-lookup"><span data-stu-id="e2ace-298">Optional fields for filtering:</span></span>

  - <span data-ttu-id="e2ace-299">四半期</span><span class="sxs-lookup"><span data-stu-id="e2ace-299">Quarter</span></span>

  - <span data-ttu-id="e2ace-300">月</span><span class="sxs-lookup"><span data-stu-id="e2ace-300">Month</span></span>

  - <span data-ttu-id="e2ace-301">期間</span><span class="sxs-lookup"><span data-stu-id="e2ace-301">Period</span></span>

<span data-ttu-id="e2ace-302">行でできる限り下方展開しないと、ドリルダウンは機能しません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-302">If you don’t expand down far enough on a row, the drill-down doesn’t work.</span></span> <span data-ttu-id="e2ace-303">たとえば、主勘定カテゴリにのみ下方展開する場合、残高で ASE にドリルダウンすることはできません。主勘定が、ASE 内でフィルター処理の必須フィールドであるためです。</span><span class="sxs-lookup"><span data-stu-id="e2ace-303">For example, if you expand down only to the main account category, you can’t drill down into the ASE on the balance, because the main account is a required field for filtering in the ASE.</span></span>

<span data-ttu-id="e2ace-304">行で展開しすぎると、財務諸表の追加のフィルターは ASE に送信されません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-304">If you expand down too far on a row, the additional filters on the financial statements aren’t sent to the ASE.</span></span> <span data-ttu-id="e2ace-305">そのため、番号の違いに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-305">Therefore, you might see a difference in your numbers.</span></span> <span data-ttu-id="e2ace-306">たとえば、財務諸表の地域ごとに、損益計算書の行で国または地域に下方展開する場合は、国または地域は ASE でのフィルターとして含まれません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-306">For example, if you expand down to the country or region on the rows of the Income statement by region financial statement, the country or region isn’t be included as a filter in the ASE.</span></span>

> [!NOTE]
> <span data-ttu-id="e2ace-307">フィルター処理するために ASE が現在サポートしているよりも、財務諸表の行または列でさらにドリルダウンできます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-307">You can drill further down on the financial statement rows or columns than the ASE currently supports for filtering.</span></span> <span data-ttu-id="e2ace-308">したがって、場合によっては、ASE での詳細トランザクションの合計は、ドリルバックしている残高と一致しません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-308">Therefore, in some situations, the sum of detailed transactions in the ASE won’t match the balance that you’re drilling back on.</span></span> <span data-ttu-id="e2ace-309">この機能は、将来に向けて改善され続けます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-309">This functionality will continue to be enhanced in the future.</span></span>

## <a name="hierarchies"></a><span data-ttu-id="e2ace-310">階層</span><span class="sxs-lookup"><span data-stu-id="e2ace-310">Hierarchies</span></span>

<span data-ttu-id="e2ace-311">既定の財務諸表は、データで表示または展開するため 2 つの階層を使用します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-311">The default financial statements use two hierarchies to drill and expand on the data.</span></span> <span data-ttu-id="e2ace-312">1 つの階層は行に対するもので、もう 1 つの階層は列に対するものです。</span><span class="sxs-lookup"><span data-stu-id="e2ace-312">One hierarchy is for the rows, and the other hierarchy is for the columns.</span></span> <span data-ttu-id="e2ace-313">両方の階層は、財務諸表のデザインであらかじめ定義されています。</span><span class="sxs-lookup"><span data-stu-id="e2ace-313">Both hierarchies are predefined in the design of the financial statement.</span></span> <span data-ttu-id="e2ace-314">ほとんどの財務諸表で、行階層は **主勘定タイプ** > **主勘定カテゴリ** > **主勘定** の順になっています。</span><span class="sxs-lookup"><span data-stu-id="e2ace-314">For most financial statements, the row hierarchy is **Main account type** > **Main account categories** > **Main account**.</span></span> <span data-ttu-id="e2ace-315">ただし、一部のレポートには、国や地域などの追加のフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-315">However, some reports have additional fields, such as Country and Region.</span></span> <span data-ttu-id="e2ace-316">階層の追加ノードは、各トランザクションの補助元帳データに基づいています。</span><span class="sxs-lookup"><span data-stu-id="e2ace-316">The additional nodes of the hierarchy are based on subledger data for each transaction.</span></span>

<span data-ttu-id="e2ace-317">列に対して、階層は法人および会計年度期間に重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="e2ace-317">For the columns, the hierarchy is focused on the legal entities and the fiscal periods.</span></span> <span data-ttu-id="e2ace-318">ほとんどの財務諸表で、列階層は **法人** > **会計カレンダー** > **会計年度** > **四半期** > **期間** の順になっています。</span><span class="sxs-lookup"><span data-stu-id="e2ace-318">For most financial statements, the column hierarchy is **Legal entity** > **Fiscal calendar** > **Fiscal year** > **Quarter** > **Period**.</span></span>

<span data-ttu-id="e2ace-319">現在、財務諸表は組織階層をサポートしておらず、データを集計できるようにします。</span><span class="sxs-lookup"><span data-stu-id="e2ace-319">Currently, the financial statements don’t support the organizational hierarchies, which let you aggregate data.</span></span>

## <a name="data-limitations"></a><span data-ttu-id="e2ace-320">データ制限</span><span class="sxs-lookup"><span data-stu-id="e2ace-320">Data limitations</span></span>
<span data-ttu-id="e2ace-321">財務諸表ビジュアルには、表示される行の数に制限があります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-321">The financial statement visuals have a limit on the number of rows that can be shown.</span></span> <span data-ttu-id="e2ace-322">現在、制限が 30,000 に設定されています。</span><span class="sxs-lookup"><span data-stu-id="e2ace-322">Currently, the limit is set to 30,000.</span></span> <span data-ttu-id="e2ace-323">この制限を超過した場合、ビジュアルには、この状況に関してユーザーに通知する警告記号があります。</span><span class="sxs-lookup"><span data-stu-id="e2ace-323">If you exceed this limit, the visual will have a warning symbol to notify you about this situation.</span></span>
 
![データ制限](./media/data-limit.png)


<span data-ttu-id="e2ace-325">最大値を超過した場合、財務諸表に表示される合計は正確ではありません。すべての行がビジュアルに読み込まれた訳ではないためです。</span><span class="sxs-lookup"><span data-stu-id="e2ace-325">If the maximum is exceeded, the totals that appear on the financial statement will be incorrect, because not all the rows were loaded into the visual.</span></span>

### <a name="empty-rows"></a><span data-ttu-id="e2ace-326">空の行</span><span class="sxs-lookup"><span data-stu-id="e2ace-326">Empty rows</span></span>
<span data-ttu-id="e2ace-327">Power BI は、空の行を表示または非表示するオプションを提供していません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-327">Power BI doesn’t provide an option to hide and show empty rows.</span></span> <span data-ttu-id="e2ace-328">行に任意のデータがない場合、ビジュアルで行は表示されません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-328">If a row doesn’t have any data, the row won’t appear in the visual.</span></span>

## <a name="what-is-coming-in-future-releases"></a><span data-ttu-id="e2ace-329">将来のリリースには何がありますか。</span><span class="sxs-lookup"><span data-stu-id="e2ace-329">What is coming in future releases?</span></span>
<span data-ttu-id="e2ace-330">Power BI を使用する新しいワークスペースおよび財務諸表は、改善され続けます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-330">The new workspaces and financial statements that use Power BI will continue to be enhanced.</span></span> <span data-ttu-id="e2ace-331">将来のリリースとして考慮されている新しい機能について紹介します。</span><span class="sxs-lookup"><span data-stu-id="e2ace-331">Here are some of the new features that are being considered for future releases:</span></span>

 - <span data-ttu-id="e2ace-332">財務諸表でもコピー、編集、削除、およびビジュアルの作成ができる機能</span><span class="sxs-lookup"><span data-stu-id="e2ace-332">The ability to copy, edit, delete, and create visuals, even the financial statements</span></span>                                                  
 - <span data-ttu-id="e2ace-333">追加の既定のレポート</span><span class="sxs-lookup"><span data-stu-id="e2ace-333">Additional default reports</span></span>                                                                                                            
    - <span data-ttu-id="e2ace-334">追加の補助元帳データのサポート</span><span class="sxs-lookup"><span data-stu-id="e2ace-334">Support for additional subledger data</span></span>                                                                                            
 - <span data-ttu-id="e2ace-335">レポート通貨のためのサポート</span><span class="sxs-lookup"><span data-stu-id="e2ace-335">Support for a reporting currency</span></span>                                                                                                      
 - <span data-ttu-id="e2ace-336">行および列のカスタム計算の追加</span><span class="sxs-lookup"><span data-stu-id="e2ace-336">Add custom calculations for rows and columns</span></span>                                                                                          
 - <span data-ttu-id="e2ace-337">財務諸表を Microsoft Excel へエクスポートする機能</span><span class="sxs-lookup"><span data-stu-id="e2ace-337">The ability to export the financial statements to Microsoft Excel</span></span>                                                                     
   - <span data-ttu-id="e2ace-338">エクスポート中の財務諸表のフォーマットの管理</span><span class="sxs-lookup"><span data-stu-id="e2ace-338">Maintain the format of the financial statement during export.</span></span>                                                                          
   - <span data-ttu-id="e2ace-339">ビジュアルで情報を使用するピボット テーブルを作成することによる Excel でのデータの分析</span><span class="sxs-lookup"><span data-stu-id="e2ace-339">Analyze data in Excel by creating a Pivot Table that uses the information on the visual.</span></span>                                              
 - <span data-ttu-id="e2ace-340">ロケール サポート</span><span class="sxs-lookup"><span data-stu-id="e2ace-340">Locale support</span></span>                                                                                                                        
 - <span data-ttu-id="e2ace-341">財務諸表でデザイン、フィルター処理、およびセキュリティ用に使用できる、主勘定階層または組織階層を定義できるようにするための、レポート階層を定義する機能。</span><span class="sxs-lookup"><span data-stu-id="e2ace-341">The ability to define reporting hierarchies, so that you can define main account hierarchies or an organizational hierarchy that can be used on financial statements for design, filtering, and security.</span></span>                                                                    
 - <span data-ttu-id="e2ace-342">印刷のサポート</span><span class="sxs-lookup"><span data-stu-id="e2ace-342">Support for printing</span></span>

<span data-ttu-id="e2ace-343">新機能は、機能が開始する際、ロードマップ Web サイトから通知されます: https://roadmap.dynamics.com/。</span><span class="sxs-lookup"><span data-stu-id="e2ace-343">The new features will be communicated through the roadmap website as work is started: https://roadmap.dynamics.com/.</span></span>

## <a name="additional-resources-for-power-bi"></a><span data-ttu-id="e2ace-344">Power BI の追加リソース</span><span class="sxs-lookup"><span data-stu-id="e2ace-344">Additional resources for Power BI</span></span>

<span data-ttu-id="e2ace-345">次のリソースでの情報は、実稼動環境での **CFO の概要** または **財務インサイト** ワークスペースに対する埋め込みレポートを有効にするために必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="e2ace-345">The information in the following resources isn’t required in order to enable the embedded reports for the **CFO overview** or **Financial Insights** workspace in a production environment.</span></span> <span data-ttu-id="e2ace-346">代わりに、これらは開発ボックスや、Finance and Operations に独自の Power BI レポートを埋め込む際に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="e2ace-346">Instead, they are helpful for dev boxes and if you want to embed your own Power BI reports into Finance and Operations.</span></span>

<span data-ttu-id="e2ace-347">https://blogs.msdn.microsoft.com/dynamicsaxbi/2017/07/29/accessing-analytical-workspaces-on-1box-environment/</span><span class="sxs-lookup"><span data-stu-id="e2ace-347">https://blogs.msdn.microsoft.com/dynamicsaxbi/2017/07/29/accessing-analytical-workspaces-on-1box-environment/</span></span>

<span data-ttu-id="e2ace-348">https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/add-analytics-tab-workspaces</span><span class="sxs-lookup"><span data-stu-id="e2ace-348">https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/add-analytics-tab-workspaces</span></span>
