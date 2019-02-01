---
title: "詳細トランザクション フォーム パターン"
description: "このトピックでは、詳細トランザクション フォームのパターンについて説明します。 このパターンを使用するフォームには、ユーザーが切り替えることができる2 つの詳細ビューがあります - ヘッダー ビューおよび明細行ビュー"
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 16281
ms.assetid: 016c8e36-0abe-4b55-a575-5696761959a5
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f4ebe8877d91cf9552f7fc80bb999da47503aeb4
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="details-transaction-form-pattern"></a><span data-ttu-id="87bd1-104">詳細トランザクション フォーム パターン</span><span class="sxs-lookup"><span data-stu-id="87bd1-104">Details Transaction form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87bd1-105">このトピックでは、詳細トランザクション フォームのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="87bd1-105">This topic provides information about the Details Transaction form pattern.</span></span> <span data-ttu-id="87bd1-106">このパターンを使用するフォームには、ユーザーが切り替えることができる2 つの詳細ビューがあります - ヘッダー ビューおよび明細行ビュー</span><span class="sxs-lookup"><span data-stu-id="87bd1-106">Forms that use this pattern can have two details views that the user can switch between - a Header view and a Line view.</span></span>

<a name="usage"></a><span data-ttu-id="87bd1-107">用途</span><span class="sxs-lookup"><span data-stu-id="87bd1-107">Usage</span></span>
-----

<span data-ttu-id="87bd1-108">明細行 (フォームの詳細トランザクション) を含む詳細フォームは、ユーザーが切り替えることができる 2 つの詳細ビューを持てる 1 つのフォームで構成されます。</span><span class="sxs-lookup"><span data-stu-id="87bd1-108">A details form with lines (Details Transaction form) consists of one form that can have two details views that the user can switch between.</span></span> <span data-ttu-id="87bd1-109">ヘッダー ビューには、ヘッダーに関連付けられているか一部となっているすべてのフィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="87bd1-109">The Header view contains all fields that are related to or part of the header.</span></span> <span data-ttu-id="87bd1-110">行ビューには、行グリッド、行の詳細、および最も重要なヘッダー フィールドのコレクションを含むセクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="87bd1-110">The Line view contains the lines grid, line details, and a section that contains a collection of the most important header fields.</span></span>

## <a name="wireframe"></a><span data-ttu-id="87bd1-111">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="87bd1-111">Wireframe</span></span>
### <a name="line-view"></a><span data-ttu-id="87bd1-112">明細行の表示</span><span class="sxs-lookup"><span data-stu-id="87bd1-112">Line view</span></span>

<span data-ttu-id="87bd1-113">[![ワイヤーフレーム: 行の表示](./media/detailstransaction1-1024x575.png)](./media/detailstransaction1.png)</span><span class="sxs-lookup"><span data-stu-id="87bd1-113">[![Wireframe: Line view](./media/detailstransaction1-1024x575.png)](./media/detailstransaction1.png)</span></span>

### <a name="header-view"></a><span data-ttu-id="87bd1-114">ヘッダーの表示</span><span class="sxs-lookup"><span data-stu-id="87bd1-114">Header view</span></span>

<span data-ttu-id="87bd1-115">[![ワイヤーフレーム: ヘッダー表示](./media/detailstransaction2-1024x576.png)](./media/detailstransaction2.png)</span><span class="sxs-lookup"><span data-stu-id="87bd1-115">[![Wireframe: Header view](./media/detailstransaction2-1024x576.png)](./media/detailstransaction2.png)</span></span>

### <a name="grid-view"></a><span data-ttu-id="87bd1-116">グリッド ビュー</span><span class="sxs-lookup"><span data-stu-id="87bd1-116">Grid view</span></span>

<span data-ttu-id="87bd1-117">[![ワイヤーフレーム: グリッド ビュー](./media/detailstransaction3-1024x575.png)](./media/detailstransaction3.png)</span><span class="sxs-lookup"><span data-stu-id="87bd1-117">[![Wireframe: Grid view](./media/detailstransaction3-1024x575.png)](./media/detailstransaction3.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="87bd1-118">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="87bd1-118">Pattern changes</span></span>
<span data-ttu-id="87bd1-119">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="87bd1-119">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="87bd1-120">リスト スタイル グリッド が詳細ビュー コンテンツの左側に追加されました。ヘッダー ビューまた行ビューのいずれかに表示されます。</span><span class="sxs-lookup"><span data-stu-id="87bd1-120">A List style grid has been added to the left of the Details view content, which is shown in either Header view or Line view.</span></span>
-   <span data-ttu-id="87bd1-121">リスト ページと詳細マスターは、1 つのフォームにマージされました。</span><span class="sxs-lookup"><span data-stu-id="87bd1-121">List Page and Details Master have been merged into a single form.</span></span> <span data-ttu-id="87bd1-122">この変更では、次の利点があります。</span><span class="sxs-lookup"><span data-stu-id="87bd1-122">This change has the following benefits:</span></span>
    -   <span data-ttu-id="87bd1-123">ユーザーが一覧と詳細の間を移動するときのパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="87bd1-123">It improves performance when users move between the list and details.</span></span>
    -   <span data-ttu-id="87bd1-124">初期一覧で一括編集できます。</span><span class="sxs-lookup"><span data-stu-id="87bd1-124">It enables bulk editing in the initial list.</span></span>
    -   <span data-ttu-id="87bd1-125">これはリスト ページのプレビュー ウィンドウの消去に使用できます。</span><span class="sxs-lookup"><span data-stu-id="87bd1-125">It allows for elimination of the list page preview pane.</span></span>
-   <span data-ttu-id="87bd1-126">表示/編集、新規作成、削除、保存、最新の情報に更新、添付、および Excel にエクスポートの各アクションはすべてファンデーションによって提供され、ファンデーションによって提供されたボタンが削除されない限り、各アクションに明示的なアプリ ボタンを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="87bd1-126">View/Edit, New, Delete, Save, Refresh, Attachments, and Export to Excel actions are all provided by the foundation and should not have explicit app buttons unless the foundation-provided button is removed.</span></span>

## <a name="model"></a><span data-ttu-id="87bd1-127">モデル</span><span class="sxs-lookup"><span data-stu-id="87bd1-127">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="87bd1-128">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="87bd1-128">High-level structure</span></span>

- <span data-ttu-id="87bd1-129">デザイン</span><span class="sxs-lookup"><span data-stu-id="87bd1-129">Design</span></span>

    - <span data-ttu-id="87bd1-130">ActionPane (ActionPane)</span><span class="sxs-lookup"><span data-stu-id="87bd1-130">ActionPane (ActionPane)</span></span>
    - <span data-ttu-id="87bd1-131">SidePanel (グループ)</span><span class="sxs-lookup"><span data-stu-id="87bd1-131">SidePanel (Group)</span></span>

        - <span data-ttu-id="87bd1-132">QuickFilter</span><span class="sxs-lookup"><span data-stu-id="87bd1-132">QuickFilter</span></span>
        - <span data-ttu-id="87bd1-133">*CustomFilters (グループ\] \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="87bd1-133">*CustomFilters (Group\] \[Optional\]*</span></span>
        - <span data-ttu-id="87bd1-134">NavigationList (グリッド、スタイル = リスト)</span><span class="sxs-lookup"><span data-stu-id="87bd1-134">NavigationList (Grid, Style=List)</span></span>

    - <span data-ttu-id="87bd1-135">PanelTab (Tab ShowTabs=No)</span><span class="sxs-lookup"><span data-stu-id="87bd1-135">PanelTab (Tab ShowTabs=No)</span></span>

        - <span data-ttu-id="87bd1-136">DetailsPanel (TabPage)</span><span class="sxs-lookup"><span data-stu-id="87bd1-136">DetailsPanel (TabPage)</span></span>

            - <span data-ttu-id="87bd1-137">TitleGroup (グループ)</span><span class="sxs-lookup"><span data-stu-id="87bd1-137">TitleGroup (Group)</span></span>

                - <span data-ttu-id="87bd1-138">HeaderTitle (文字列)</span><span class="sxs-lookup"><span data-stu-id="87bd1-138">HeaderTitle (String)</span></span>
                - <span data-ttu-id="87bd1-139">*EntityStatus (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="87bd1-139">*EntityStatus (Group) \[Optional\]*</span></span>

                    - <span data-ttu-id="87bd1-140">StatusFields (1..N)</span><span class="sxs-lookup"><span data-stu-id="87bd1-140">StatusFields (1..N)</span></span>

            - <span data-ttu-id="87bd1-141">HeaderLinePanels (Tab ShowTabs=No)</span><span class="sxs-lookup"><span data-stu-id="87bd1-141">HeaderLinePanels (Tab ShowTabs=No)</span></span>

                - <span data-ttu-id="87bd1-142">LinePanel (TabPage PanelStyle=Line)</span><span class="sxs-lookup"><span data-stu-id="87bd1-142">LinePanel (TabPage PanelStyle=Line)</span></span>

                    - <span data-ttu-id="87bd1-143">LineViewTab (Tab Style=FastTabs)</span><span class="sxs-lookup"><span data-stu-id="87bd1-143">LineViewTab (Tab Style=FastTabs)</span></span>

                        - <span data-ttu-id="87bd1-144">LineViewHeader (TabPage)</span><span class="sxs-lookup"><span data-stu-id="87bd1-144">LineViewHeader (TabPage)</span></span>
                        - <span data-ttu-id="87bd1-145">LineViewLines (TabPage)</span><span class="sxs-lookup"><span data-stu-id="87bd1-145">LineViewLines (TabPage)</span></span>
                        - <span data-ttu-id="87bd1-146">LineViewLineDetails (TabPage)</span><span class="sxs-lookup"><span data-stu-id="87bd1-146">LineViewLineDetails (TabPage)</span></span>

                            - <span data-ttu-id="87bd1-147">LineDetailsTab (Tab Style=Standard)</span><span class="sxs-lookup"><span data-stu-id="87bd1-147">LineDetailsTab (Tab Style=Standard)</span></span>

                                - <span data-ttu-id="87bd1-148">LineDetailsTabPages (TabPages 1..N)</span><span class="sxs-lookup"><span data-stu-id="87bd1-148">LineDetailsTabPages (TabPages 1..N)</span></span>

                - <span data-ttu-id="87bd1-149">HeaderPanel (TabPage PanelStyle=Header)</span><span class="sxs-lookup"><span data-stu-id="87bd1-149">HeaderPanel (TabPage PanelStyle=Header)</span></span>

                    - <span data-ttu-id="87bd1-150">HeaderViewTab (Tab Style=FastTabs)</span><span class="sxs-lookup"><span data-stu-id="87bd1-150">HeaderViewTab (Tab Style=FastTabs)</span></span>

                        - <span data-ttu-id="87bd1-151">HeaderViewTabPages (TabPages 1..N)</span><span class="sxs-lookup"><span data-stu-id="87bd1-151">HeaderViewTabPages (TabPages 1..N)</span></span>

        - <span data-ttu-id="87bd1-152">GridPanel (TabPage PanelStyle=Grid)</span><span class="sxs-lookup"><span data-stu-id="87bd1-152">GridPanel (TabPage PanelStyle=Grid)</span></span>

            - <span data-ttu-id="87bd1-153">CustomFilterGroup (グループ)</span><span class="sxs-lookup"><span data-stu-id="87bd1-153">CustomFilterGroup (Group)</span></span>

                - <span data-ttu-id="87bd1-154">QuickFilter</span><span class="sxs-lookup"><span data-stu-id="87bd1-154">QuickFilter</span></span>
                - <span data-ttu-id="87bd1-155">*OtherFilters ($ フィールド)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="87bd1-155">*OtherFilters ($Field) \[0..N\]*</span></span>

            - <span data-ttu-id="87bd1-156">MainGrid (グリッド)</span><span class="sxs-lookup"><span data-stu-id="87bd1-156">MainGrid (Grid)</span></span>
            - <span data-ttu-id="87bd1-157">MainGridDefaultAction (CommandButton)</span><span class="sxs-lookup"><span data-stu-id="87bd1-157">MainGridDefaultAction (CommandButton)</span></span>

### <a name="core-components"></a><span data-ttu-id="87bd1-158">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="87bd1-158">Core components</span></span>

1.  <span data-ttu-id="87bd1-159">**Form.Design** に DetailsTransaction パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="87bd1-159">Apply the DetailsTransaction pattern on **Form.Design**.</span></span>
2.  <span data-ttu-id="87bd1-160">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="87bd1-160">Address BP Warnings:</span></span>
    1.  <span data-ttu-id="87bd1-161">**Design.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="87bd1-161">**Design.Caption** isn't empty.</span></span>
    2.  <span data-ttu-id="87bd1-162">このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="87bd1-162">The form must be referenced by at least one menu item.</span></span>
    3.  <span data-ttu-id="87bd1-163">**TabPage.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="87bd1-163">**TabPage.Caption** isn't empty.</span></span>
    4.  <span data-ttu-id="87bd1-164">**TabPage.DataSource** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="87bd1-164">**TabPage.DataSource** isn't empty.</span></span>

### <a name="related-patterns"></a><span data-ttu-id="87bd1-165">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="87bd1-165">Related patterns</span></span>

-   [<span data-ttu-id="87bd1-166">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="87bd1-166">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="87bd1-167">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="87bd1-167">Simple List and Details</span></span>](simple-list-details-form-pattern.md)

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="87bd1-168">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="87bd1-168">Commonly used subpatterns</span></span>

-   [<span data-ttu-id="87bd1-169">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="87bd1-169">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)
-   [<span data-ttu-id="87bd1-170">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="87bd1-170">Toolbar and List</span></span>](toolbar-list-subpattern.md)
-   [<span data-ttu-id="87bd1-171">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="87bd1-171">Toolbar and Fields</span></span>](toolbar-fields-subpattern.md)
-   [<span data-ttu-id="87bd1-172">入れ子になった簡易リストおよび詳細</span><span class="sxs-lookup"><span data-stu-id="87bd1-172">Nested Simple List and Details</span></span>](nested-simple-list-details-subpattern.md)
-   [<span data-ttu-id="87bd1-173">カスタム フィルター グループ</span><span class="sxs-lookup"><span data-stu-id="87bd1-173">Custom Filter Group</span></span>](custom-filter-group-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="87bd1-174">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="87bd1-174">UX guidelines</span></span>
<span data-ttu-id="87bd1-175">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="87bd1-175">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="87bd1-176">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="87bd1-176">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="87bd1-177">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="87bd1-177">Open the form in the browser, and walk through these steps.</span></span> <span data-ttu-id="87bd1-178">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="87bd1-178">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="87bd1-179">標準フォーム ガイドラインは、Microsoft Dynamics AX の[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="87bd1-179">Standard form guidelines have been consolidated into the Microsoft Dynamics AX [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="87bd1-180">**詳細トランザクション ガイドライン**</span><span class="sxs-lookup"><span data-stu-id="87bd1-180">**Detail Transaction guidelines:**</span></span>

-   <span data-ttu-id="87bd1-181">**新規** ボタンおよび **削除** ボタンは重複してはいけません。</span><span class="sxs-lookup"><span data-stu-id="87bd1-181">There should not be any duplicate **New** and **Delete** buttons.</span></span>
-   <span data-ttu-id="87bd1-182">**ActionPane** ガイドラインは、ActionPane ガイドライン セクションの[フォームの全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="87bd1-182">**ActionPane** guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document, in the ActionPane guidelines section.</span></span>
-   <span data-ttu-id="87bd1-183">**既定**の状態で、最初のクイック タブのコンテンツはスクロールせずに完全に表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="87bd1-183">In its **default** state, the content of the first FastTab should be fully visible without scrolling.</span></span>
-   <span data-ttu-id="87bd1-184">**クイック タブ**ガイドラインは、[フォームの全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="87bd1-184">**FastTabs** guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>
-   <span data-ttu-id="87bd1-185">**ページ タイトル エリア**</span><span class="sxs-lookup"><span data-stu-id="87bd1-185">**Page title area**:</span></span>
    -   <span data-ttu-id="87bd1-186">**&lt;ID&gt; : &lt;Description&gt;** という形式を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87bd1-186">The following format should be used: **&lt;ID&gt; : &lt;Description&gt;**</span></span>
    -   <span data-ttu-id="87bd1-187">リスト ページが詳細ページにマージされてから、詳細ページへのリンクをメイン メニューで提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87bd1-187">A link to the Details page should be provided on the Main Menu after the List page has been merged into the Details page.</span></span>
    -   <span data-ttu-id="87bd1-188">ページ タイトルは、複数フォームの形式にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="87bd1-188">The page title should be in a plural form.</span></span>
-   <span data-ttu-id="87bd1-189">**ナビゲーション リスト グリッド**</span><span class="sxs-lookup"><span data-stu-id="87bd1-189">**Navigation list grid**:</span></span>
    -   <span data-ttu-id="87bd1-190">リスト スタイル グリッドは、グリッド行内に行が 3 行以上にまたがるフィールドはありません。</span><span class="sxs-lookup"><span data-stu-id="87bd1-190">The list style grid should not have fields within a grid row that spans more than three lines.</span></span>
        -   <span data-ttu-id="87bd1-191">通常は IDと説明だけで十分です。</span><span class="sxs-lookup"><span data-stu-id="87bd1-191">Typically, just the ID and Description are sufficient.</span></span>
        -   <span data-ttu-id="87bd1-192">2 つ以上のフィールドが必要です。</span><span class="sxs-lookup"><span data-stu-id="87bd1-192">There should be at least two fields.</span></span>
    -   <span data-ttu-id="87bd1-193">最後のフィールドは、トランザクションの合計でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="87bd1-193">The last field should be the total of the transaction.</span></span>
-   <span data-ttu-id="87bd1-194">**グリッド ビュー**</span><span class="sxs-lookup"><span data-stu-id="87bd1-194">**Grid view**:</span></span>
    -   <span data-ttu-id="87bd1-195">グリッドには 2 〜 15 個のフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="87bd1-195">The grid has 2 to 15 fields.</span></span> <span data-ttu-id="87bd1-196">通常はすべての必須フィールドが含まれているので、グリッド内にレコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="87bd1-196">Typically, all mandatory fields are included, so that records can be created in the grid.</span></span>
    -   <span data-ttu-id="87bd1-197">リンクされているフィールドを使用すると、ユーザーは選択したレコードの詳細を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="87bd1-197">A linked field lets the user open the details for the selected record.</span></span>
    -   <span data-ttu-id="87bd1-198">既定では、クイック フィルターはフィルター シナリオに最も可能性が高いフィールドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87bd1-198">By default, the Quick Filter should use the most likely field for a filter scenario.</span></span>
    -   <span data-ttu-id="87bd1-199">リスト ページを開いたときに、フォーカスがクイック フィルターにある必要があります。</span><span class="sxs-lookup"><span data-stu-id="87bd1-199">Focus should be in the Quick Filter when the list page is opened.</span></span>
    -   <span data-ttu-id="87bd1-200">**グリッド**</span><span class="sxs-lookup"><span data-stu-id="87bd1-200">**Grid**:</span></span>
        -   <span data-ttu-id="87bd1-201">**ID** フィールドが最初の列になり、次がマスタ エンティティ **ID** および **名前** フィールドになる必要があります。</span><span class="sxs-lookup"><span data-stu-id="87bd1-201">The **ID** field should be the first column, followed by the master entity **ID** and **Name** fields.</span></span>
        -   <span data-ttu-id="87bd1-202">追加のグリッド ガイドラインは、グリッド ガイドライン セクションの [全般的なフォームのガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="87bd1-202">Additional grid guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document, in the Grid guidelines section.</span></span>
    -   <span data-ttu-id="87bd1-203">**情報ボックス**ガイドラインは、[情報ボックスのフォーム パターン](factbox-form-patterns.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="87bd1-203">**FactBox** guidelines have been consolidated into the [FactBox Form Patterns](factbox-form-patterns.md) document.</span></span>

## <a name="example"></a><span data-ttu-id="87bd1-204">例</span><span class="sxs-lookup"><span data-stu-id="87bd1-204">Example</span></span>
<span data-ttu-id="87bd1-205">フォーム: **SalesTable**</span><span class="sxs-lookup"><span data-stu-id="87bd1-205">Form: **SalesTable**</span></span>

#### <a name="line-view"></a><span data-ttu-id="87bd1-206">明細行の表示</span><span class="sxs-lookup"><span data-stu-id="87bd1-206">Line view</span></span>

<span data-ttu-id="87bd1-207">[![詳細トランザクションの例: 明細行の表示](./media/detailstransaction4-1024x508.png)](./media/detailstransaction4.png)</span><span class="sxs-lookup"><span data-stu-id="87bd1-207">[![Details Transaction example: Line view](./media/detailstransaction4-1024x508.png)](./media/detailstransaction4.png)</span></span>

#### <a name="header-view"></a><span data-ttu-id="87bd1-208">ヘッダーの表示</span><span class="sxs-lookup"><span data-stu-id="87bd1-208">Header view</span></span>

<span data-ttu-id="87bd1-209">[![詳細トランザクションの例: ヘッダーの表示](./media/detailstransaction5-1024x509.png)](./media/detailstransaction5.png)</span><span class="sxs-lookup"><span data-stu-id="87bd1-209">[![Details Transaction example: Header view](./media/detailstransaction5-1024x509.png)](./media/detailstransaction5.png)</span></span>

#### <a name="grid-view"></a><span data-ttu-id="87bd1-210">グリッド ビュー</span><span class="sxs-lookup"><span data-stu-id="87bd1-210">Grid view</span></span>

<span data-ttu-id="87bd1-211">[![詳細トランザクションの例: グリッド ビュー](./media/detailstransaction6-1024x509.png)](./media/detailstransaction6.png)</span><span class="sxs-lookup"><span data-stu-id="87bd1-211">[![Details Transaction example: Grid view](./media/detailstransaction6-1024x509.png)](./media/detailstransaction6.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="87bd1-212">付録</span><span class="sxs-lookup"><span data-stu-id="87bd1-212">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="87bd1-213">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="87bd1-213">Frequently asked questions</span></span>

<span data-ttu-id="87bd1-214">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="87bd1-214">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

-   <span data-ttu-id="87bd1-215">**なぜヘッダーの表示は義務付けられているのですか?**</span><span class="sxs-lookup"><span data-stu-id="87bd1-215">**Why is the Header view compulsory?**</span></span>
    -   <span data-ttu-id="87bd1-216">ヘッダー ビューは、詳細トランザクション パターンに必須です。</span><span class="sxs-lookup"><span data-stu-id="87bd1-216">The Header view is compulsory for the Details Transaction pattern.</span></span> <span data-ttu-id="87bd1-217">最初、ヘッダーの表示には行の表示ヘッダーの概要情報以外にない場合があります。</span><span class="sxs-lookup"><span data-stu-id="87bd1-217">Initially, the Header view might not have more than the Line view header summary information.</span></span> <span data-ttu-id="87bd1-218">ただし、時間経過に伴い、アプリケーション チーム、国際化チーム、パートナー、および顧客によりそれが追加されます。</span><span class="sxs-lookup"><span data-stu-id="87bd1-218">However, over time, it will be extended by application teams, internationalization teams, partners, and customers.</span></span> <span data-ttu-id="87bd1-219">ヘッダーの表示が今後の変更で使用できることが重要です。</span><span class="sxs-lookup"><span data-stu-id="87bd1-219">It's important that the Header view be available for future modifications.</span></span> <span data-ttu-id="87bd1-220">さらに、一貫した信頼性の高いフォーム構造には、使い勝手とアップグレード上のメリットがあります。</span><span class="sxs-lookup"><span data-stu-id="87bd1-220">In addition, a consistent and dependable form structure has benefits for usability and upgrade reasons.</span></span>

### <a name="open-issues"></a><span data-ttu-id="87bd1-221">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="87bd1-221">Open issues</span></span>

<span data-ttu-id="87bd1-222">現在ありません。</span><span class="sxs-lookup"><span data-stu-id="87bd1-222">None currently.</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="87bd1-223">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="87bd1-223">AX 2012 content</span></span>

#### <a name="ax-2012-links"></a><span data-ttu-id="87bd1-224">AX 2012 のリンク</span><span class="sxs-lookup"><span data-stu-id="87bd1-224">AX 2012 links</span></span>

-   <span data-ttu-id="87bd1-225">[ユーザー エクスペリエンス ガイドライン明細を含む MSDN 詳細フォーム \[AX 2012\]](http://msdn.microsoft.com/EN-US/library/gg886601.aspx)</span><span class="sxs-lookup"><span data-stu-id="87bd1-225">[MSDN Details Form with Lines User Experience Guidelines \[AX 2012\]](http://msdn.microsoft.com/EN-US/library/gg886601.aspx)</span></span>
-   <span data-ttu-id="87bd1-226">[MSDN 詳細フォーム \[AX 2012\]](http://msdn.microsoft.com/EN-US/library/hh397318.aspx)</span><span class="sxs-lookup"><span data-stu-id="87bd1-226">[MSDN Details Form \[AX 2012\]](http://msdn.microsoft.com/EN-US/library/hh397318.aspx)</span></span>

#### <a name="ax-2012-example"></a><span data-ttu-id="87bd1-227">AX 2012 の例</span><span class="sxs-lookup"><span data-stu-id="87bd1-227">AX 2012 example</span></span>

##### <a name="line-view"></a><span data-ttu-id="87bd1-228">明細行の表示</span><span class="sxs-lookup"><span data-stu-id="87bd1-228">Line view</span></span>

<span data-ttu-id="87bd1-229">[![AX 2012 の例: 明細行の表示](./media/detailstransaction7-1024x727.png)](./media/detailstransaction7.png)</span><span class="sxs-lookup"><span data-stu-id="87bd1-229">[![AX 2012 example: Line view](./media/detailstransaction7-1024x727.png)](./media/detailstransaction7.png)</span></span>

##### <a name="header-view"></a><span data-ttu-id="87bd1-230">ヘッダーの表示</span><span class="sxs-lookup"><span data-stu-id="87bd1-230">Header view</span></span>

<span data-ttu-id="87bd1-231">[![AX 2012 の例: ヘッダーの表示](./media/detailstransaction8-1024x727.png)](./media/detailstransaction8.png)</span><span class="sxs-lookup"><span data-stu-id="87bd1-231">[![AX 2012 example: Header view](./media/detailstransaction8-1024x727.png)](./media/detailstransaction8.png)</span></span>

##### <a name="grid-view"></a><span data-ttu-id="87bd1-232">グリッド ビュー</span><span class="sxs-lookup"><span data-stu-id="87bd1-232">Grid view</span></span>

<span data-ttu-id="87bd1-233">[![AX 2012 の例: グリッド ビュー](./media/detailstransaction9-1024x727.png)](./media/detailstransaction9.png)</span><span class="sxs-lookup"><span data-stu-id="87bd1-233">[![AX 2012 example: Grid view](./media/detailstransaction9-1024x727.png)](./media/detailstransaction9.png)</span></span>



