---
title: "ナビゲーション"
description: "この記事では、ダッシュボード、新しいナビゲーション検索機能、ナビゲーション ペイン、ワークスペース、タイルなどの主要なナビゲーションの概念について説明します。"
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
ms.custom: 105091
ms.assetid: 26f373fa-13b7-4f1b-ad16-95499d19874f
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1e56a103d1abf928ab18eea403c773dcd5e79093
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="navigation"></a><span data-ttu-id="89eba-103">ナビゲーション</span><span class="sxs-lookup"><span data-stu-id="89eba-103">Navigation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89eba-104">この記事では、ダッシュボード、新しいナビゲーション検索機能、ナビゲーション ペイン、ワークスペース、タイルなどの主要なナビゲーションの概念について説明します。</span><span class="sxs-lookup"><span data-stu-id="89eba-104">This articles describes the primary navigation concepts including the dashboard, the new navigation search feature, the navigation pane, workspaces, and tiles.</span></span>

<a name="navigation-concepts"></a><span data-ttu-id="89eba-105">ナビゲーション概念</span><span class="sxs-lookup"><span data-stu-id="89eba-105">Navigation concepts</span></span>
-------------------

<span data-ttu-id="89eba-106">プライマリ ナビゲーションの概念は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="89eba-106">The primary navigation concepts are:</span></span>

-   <span data-ttu-id="89eba-107">ダッシュボード</span><span class="sxs-lookup"><span data-stu-id="89eba-107">Dashboard</span></span>
-   <span data-ttu-id="89eba-108">ナビゲーション ウィンドウ</span><span class="sxs-lookup"><span data-stu-id="89eba-108">Navigation pane</span></span>
-   <span data-ttu-id="89eba-109">ワークスペース</span><span class="sxs-lookup"><span data-stu-id="89eba-109">Workspaces</span></span>
-   <span data-ttu-id="89eba-110">タイル</span><span class="sxs-lookup"><span data-stu-id="89eba-110">Tiles</span></span>
-   <span data-ttu-id="89eba-111">ナビゲーション検索</span><span class="sxs-lookup"><span data-stu-id="89eba-111">Navigation search</span></span>

<span data-ttu-id="89eba-112">ダッシュボードは新しい概念ですが、ナビゲーション ペインとワークスペースは既存の概念の更新です。</span><span class="sxs-lookup"><span data-stu-id="89eba-112">The dashboard is a new concept, whereas the navigation pane and workspaces are updates to existing concepts.</span></span> <span data-ttu-id="89eba-113">ナビゲーション概念を実装するために、ユーザー インターフェイス モデルではいくつかの標準的なページ タイプを使用しています。</span><span class="sxs-lookup"><span data-stu-id="89eba-113">To implement the navigation concepts, the user interface model uses several standard page types.</span></span> <span data-ttu-id="89eba-114">アプリケーションを作成するときは、ユーザーに一貫した体験を提供するために、これらのページの規則に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="89eba-114">When you create an application, you should follow the conventions for these pages to present a consistent experience for the user.</span></span> <span data-ttu-id="89eba-115">次の図は、標準のページ タイプの概要と、それらがどのように適合するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="89eba-115">The following diagram shows an overview of the standard page types and how they fit together.</span></span> <span data-ttu-id="89eba-116">[![1\_Nav](./media/1_nav.png)](./media/1_nav.png) 次のセクションではこれらの概念の基になるページに関する詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="89eba-116">[![1\_Nav](./media/1_nav.png)](./media/1_nav.png)The following sections provide more detail about the pages that underlie these concepts.</span></span> <span data-ttu-id="89eba-117">これらのページや他の種類のページのモデリングに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="89eba-117">They include information about the modeling of these and other types of pages.</span></span>

## <a name="dashboard"></a><span data-ttu-id="89eba-118">ダッシュボード</span><span class="sxs-lookup"><span data-stu-id="89eba-118">Dashboard</span></span>
<span data-ttu-id="89eba-119">ダッシュボードは、ユーザーがクライアントにアクセスしたときに最初に表示されるページです。</span><span class="sxs-lookup"><span data-stu-id="89eba-119">The dashboard is the first page that users see when they access the client.</span></span> <span data-ttu-id="89eba-120">ダッシュボードには、システムの重要な詳細を示すタイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="89eba-120">The dashboard contains tiles that show important details from the system.</span></span> <span data-ttu-id="89eba-121">以前に Microsoft Dynamics AX 2012 のロール センター ページのキューに表示されていたコンテンツは、ダッシュボードで利用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="89eba-121">Content that was previously displayed in Cues on Role Center pages in Microsoft Dynamics AX 2012 is now available on the dashboard.</span></span> <span data-ttu-id="89eba-122">アプリケーション フレームの上部にあるナビゲーション バーの **Dynamics 365** をクリックすることにより、いつでもダッシュボードに戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="89eba-122">You can return to the dashboard at any time by clicking **Dynamics 365** on the navigation bar at the top of the application frame.</span></span> 

<span data-ttu-id="89eba-123">[![dashboardExample](./media/dashboardexample-1024x622.png)](./media/dashboardexample.png)</span><span class="sxs-lookup"><span data-stu-id="89eba-123">[![dashboardExample](./media/dashboardexample-1024x622.png)](./media/dashboardexample.png)</span></span> 

<span data-ttu-id="89eba-124">ダッシュボードは、主にワークスペース タイルの大きなセクションで構成されています。</span><span class="sxs-lookup"><span data-stu-id="89eba-124">The dashboard primarily consists of a large section of workspace tiles.</span></span> <span data-ttu-id="89eba-125">また、前のスクリーンショットには表示されていない「はじめに」ツールもあります。</span><span class="sxs-lookup"><span data-stu-id="89eba-125">There might also be a Getting Started tool, which isn't shown in the preceding screenshot.</span></span> <span data-ttu-id="89eba-126">ダッシュボードのワークスペース タイル セクションは、**NavPaneMenu** メニューにルートを持つメニュー構造から構築されています。</span><span class="sxs-lookup"><span data-stu-id="89eba-126">The dashboard's workspace tile section is built from a menu structure that has its root in the **NavPaneMenu** menu.</span></span> <span data-ttu-id="89eba-127">メニューは一連のメニュー拡張機能によって変更され、それらの拡張機能には、ユーザーがそのセクションに表示するタイルに対応する 1 つ以上のタイルの参照が含まれます。</span><span class="sxs-lookup"><span data-stu-id="89eba-127">The menu is modified by a set of menu extensions, and those extensions contain one or more tile references that correspond to the tiles that users see in that section.</span></span>

## <a name="navigation-pane"></a><span data-ttu-id="89eba-128">ナビゲーション ウィンドウ</span><span class="sxs-lookup"><span data-stu-id="89eba-128">Navigation pane</span></span>
<span data-ttu-id="89eba-129">ナビゲーション ウィンドウは、ワークスペース、メイン メニュー要素、最近開いたフォーム、およびユーザー定義のお気に入りへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="89eba-129">The navigation pane provides access to workspaces, main menu elements, recently opened forms, and user-defined favorites.</span></span>  <span data-ttu-id="89eba-130">ユーザーは、ナビゲーション バーの **ナビゲーション ウィンドウの表示** ボタンをクリックしてナビゲーション ウィンドウを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="89eba-130">The user can open the navigation pane by clicking the **Show navigation pane** button under the navigation bar.</span></span> <span data-ttu-id="89eba-131">ナビゲーション ウィンドウは、折りたたみ可能な 4 つのセクションで構成されています。</span><span class="sxs-lookup"><span data-stu-id="89eba-131">The navigation pane consists of four collapsible sections.</span></span> <span data-ttu-id="89eba-132">**お気に入り** セクションでは、ユーザーが明示的にお気に入りとしてマークしたフォームの一覧にすばやくアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="89eba-132">The **Favorites** section provides quick access to the list of forms the user has explicitly marked as a favorite.</span></span> <span data-ttu-id="89eba-133">ナビゲーション ウィンドウでフォームの横にある星のアイコンをクリックすることで、お気に入りとしてフォームをマークします。</span><span class="sxs-lookup"><span data-stu-id="89eba-133">Marking a form as a favorite is accomplished by clicking the star icon next to the form in the navigation pane.</span></span> <span data-ttu-id="89eba-134">**最近** セクションには、ユーザーが最後にアクセスしたフォームが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="89eba-134">The **Recent** section lists the forms the user has most recently visited.</span></span> <span data-ttu-id="89eba-135">ユーザーがアクセスできるワークスペースのセットは、**ワークスペース** セクションに表示され、便利です。</span><span class="sxs-lookup"><span data-stu-id="89eba-135">The set of workspaces a user has access to is conveniently shown in the **Workspaces** section.</span></span> <span data-ttu-id="89eba-136">最後に、**モジュール**セクションは、モジュールの完全な一覧を提供します。</span><span class="sxs-lookup"><span data-stu-id="89eba-136">Finally, the **Modules** section provides the full list of modules.</span></span> <span data-ttu-id="89eba-137">モジュールをクリックすると、ユーザーがそのモジュール内の目的のページに移動できるナビゲーション ウィンドウの右側が開きます。</span><span class="sxs-lookup"><span data-stu-id="89eba-137">Clicking on a module will open the right side of the navigation pane, where the user can navigate to the desired page in that module.</span></span> <span data-ttu-id="89eba-138">**注記:** このスクリーン ショットでは、**すべての顧客**がお気に入りとしてマークされているため、**お気に入り**に表示されます。</span><span class="sxs-lookup"><span data-stu-id="89eba-138">**Note:** In this screenshot, **All customers** has been marked as a favorite, and therefore it will appear in the **Favorites** list.</span></span> 

<span data-ttu-id="89eba-139">[![navPaneExpanded](./media/navpaneexpanded-1024x532.png)](./media/navpaneexpanded.png)</span><span class="sxs-lookup"><span data-stu-id="89eba-139">[![navPaneExpanded](./media/navpaneexpanded-1024x532.png)](./media/navpaneexpanded.png)</span></span> 

<span data-ttu-id="89eba-140">ダッシュボードのワークスペース タイルと同様に、ナビゲーション ウィンドウで一覧表示される要素は、メニュー構造に基づいて実行時に生成されます。</span><span class="sxs-lookup"><span data-stu-id="89eba-140">Like the workspace tiles on the dashboard, the elements that are listed in the navigation pane are generated at runtime, based on a menu structure.</span></span> <span data-ttu-id="89eba-141">ダッシュボード上のワークスペースのセットを定義する同じルートメニュー (**NavPaneMenu**) は、ナビゲーション ペインも定義します。</span><span class="sxs-lookup"><span data-stu-id="89eba-141">The same root menu (**NavPaneMenu**) that defines the set of workspaces on the dashboard also defines the navigation pane.</span></span> <span data-ttu-id="89eba-142">ナビゲーション ウィンドウの論理構造の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="89eba-142">Here's an example of the logical structure for the navigation pane:</span></span>

-   <span data-ttu-id="89eba-143">NavPaneMenu (メニュー)</span><span class="sxs-lookup"><span data-stu-id="89eba-143">NavPaneMenu (menu)</span></span>
    -   <span data-ttu-id="89eba-144">NavPaneMenuFleet (メニューの拡張機能)</span><span class="sxs-lookup"><span data-stu-id="89eba-144">NavPaneMenuFleet (menu extension)</span></span>
        -   <span data-ttu-id="89eba-145">「予約管理」(タイルの参照)</span><span class="sxs-lookup"><span data-stu-id="89eba-145">"Reservation management" (tile reference)</span></span>

## <a name="workspaces"></a><span data-ttu-id="89eba-146">ワークスペース</span><span class="sxs-lookup"><span data-stu-id="89eba-146">Workspaces</span></span>
<span data-ttu-id="89eba-147">ワークスペースは活動志向のページで、対象ユーザーにとって最も急を要する活動に関連した質問に対して回答し、より頻繁に実行するタスクに関与できるようにすることにより、ユーザーの生産性を向上させるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="89eba-147">Workspaces are activity-oriented pages that are designed to increase a user's productivity by providing information that answers the targeted user's most pressing activity-related questions and allows the user to initiate their more frequent tasks.</span></span> <span data-ttu-id="89eba-148">さまざまなワークスペースへのアクセスは、ユーザーが組織で持つロールに依存します。</span><span class="sxs-lookup"><span data-stu-id="89eba-148">Access to the various workspaces depends on the roles that users have in the organization.</span></span> <span data-ttu-id="89eba-149">古いロール センター ページからのリストとビジネス インテリジェンス (BI) コンテンツの多くは、ワークスペースに公開されます。</span><span class="sxs-lookup"><span data-stu-id="89eba-149">Much of the list and business intelligence (BI) content from the old Role Center pages is exposed on workspaces.</span></span> <span data-ttu-id="89eba-150">ワークスペースに移動するには、ダッシュボード上のタイルをクリックするか、ナビゲーション ウィンドウでリンクをクリックするか、ナビゲーション検索機能 (次のセクションを参照) を使用してワークスペースを検索します。</span><span class="sxs-lookup"><span data-stu-id="89eba-150">To navigate to a workspace, you can click a tile on the dashboard, click a link in the navigation pane, or find the workspace using the navigation search feature (see the next section).</span></span> 

<span data-ttu-id="89eba-151">[![workspaceExample](./media/workspaceexample-1024x486.png)](./media/workspaceexample.png)</span><span class="sxs-lookup"><span data-stu-id="89eba-151">[![workspaceExample](./media/workspaceexample-1024x486.png)](./media/workspaceexample.png)</span></span>             

<span data-ttu-id="89eba-152">ワークスペースはモデル化されたフォームの異なるタイプにすぎません。</span><span class="sxs-lookup"><span data-stu-id="89eba-152">Workspaces are simply a different type of modeled forms.</span></span> <span data-ttu-id="89eba-153">システムは **Form.Design.Style**=**Workspace** (この値はワークスペース フォーム パターンの一部として定義) でワークスペースを区別します。</span><span class="sxs-lookup"><span data-stu-id="89eba-153">The system differentiates workspaces by **Form.Design.Style**=**Workspace** (this value is defined as part of the Workspace form pattern).</span></span> <span data-ttu-id="89eba-154">ワークスペースは、キャプション (**Form.Design.Caption** で定義される) とパノラマ (つまり、タブ コントロール) で構成されています。</span><span class="sxs-lookup"><span data-stu-id="89eba-154">A workspace consists of a caption (which is defined on **Form.Design.Caption**) and a panorama (that is, a tab control).</span></span> <span data-ttu-id="89eba-155">パノラマには、ワークスペースの対象となるタスクに関連するコンテンツのセクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="89eba-155">A panorama contains sections of content that are relevant to the task for which the workspace is intended.</span></span> <span data-ttu-id="89eba-156">これらのセクションは、タブ ページとしてモデル化されています。</span><span class="sxs-lookup"><span data-stu-id="89eba-156">These sections are modeled as tab pages.</span></span> <span data-ttu-id="89eba-157">最初のセクションは一般的に、ユーザーが新しいタスクを開始したり項目のリストにアクセスするためにクリックできるタイルのセットです。</span><span class="sxs-lookup"><span data-stu-id="89eba-157">The first section will generally be a set of tiles that users can click to begin new tasks or access lists of items.</span></span> <span data-ttu-id="89eba-158">2 番目のセクションには、アクティビティに関連する一連のリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="89eba-158">The second section contains a set of relevant lists for the activity.</span></span> <span data-ttu-id="89eba-159">最後のセクションには、このアクティビティでは重要であるが頻繁には使用されないページへの多数のリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="89eba-159">The last section contains a number of links to pages that are important but not frequently used for this activity.</span></span> <span data-ttu-id="89eba-160">リストおよびリンクのセクションの間には、チャートとグラフを含むオプションのセクションがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="89eba-160">In between the list and links section are a few optional sections that might contain charts and graphs.</span></span> <span data-ttu-id="89eba-161">ワークスペースの重要な違いの 1 つは、データ ソースがないことです。</span><span class="sxs-lookup"><span data-stu-id="89eba-161">One important distinction of workspaces is that they do not have a data source.</span></span> <span data-ttu-id="89eba-162">コンテンツ (リストまたはチャートなど) にデータソースが必要な場合は、**フォーム パーツ**という独立した形式でそのコンテンツをモデル化し、そのフォーム パーツをワークスペースで参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89eba-162">If the content (such as a list or chart) requires a data source, you must model that content on an independent form of type **Form part**, and then reference that form part on the workspace.</span></span> <span data-ttu-id="89eba-163">他のフォームでフォーム パーツをホストし、それぞれ独自のデータ ソースを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="89eba-163">Form parts can be hosted on other forms, and each can have its own data source.</span></span>

## <a name="tiles"></a><span data-ttu-id="89eba-164">タイル</span><span class="sxs-lookup"><span data-stu-id="89eba-164">Tiles</span></span>
<span data-ttu-id="89eba-165">Windows 8 ではタイルの概念が導入され、クライアントで使用されます。</span><span class="sxs-lookup"><span data-stu-id="89eba-165">Windows 8 introduced the concept of tiles, and you will see them used in the client.</span></span> <span data-ttu-id="89eba-166">タイルは、メニュー項目ボタンのように動作する長方形のボタンです。</span><span class="sxs-lookup"><span data-stu-id="89eba-166">A tile is a rectangular button that behaves like a menu item button.</span></span> <span data-ttu-id="89eba-167">ページを移動、または開くために使用されます。</span><span class="sxs-lookup"><span data-stu-id="89eba-167">It is used to navigate to or open pages.</span></span> <span data-ttu-id="89eba-168">さらに、タイルは、数や主要業績評価指標 (KPI) などの関連データを表示できます。</span><span class="sxs-lookup"><span data-stu-id="89eba-168">In addition, tiles can display relevant data, such as counts or key performance indicators (KPIs).</span></span> <span data-ttu-id="89eba-169">タイルは、追加の視覚コンテキストでユーザーに提供する画像を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="89eba-169">A tile can include images that provide the user with additional visual context.</span></span> <span data-ttu-id="89eba-170">次のタイプのタイルを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="89eba-170">You can create the following types of tiles.</span></span>

| <span data-ttu-id="89eba-171">種類</span><span class="sxs-lookup"><span data-stu-id="89eba-171">Type</span></span>     | <span data-ttu-id="89eba-172">例</span><span class="sxs-lookup"><span data-stu-id="89eba-172">Example</span></span>                                                                                                                                                           | <span data-ttu-id="89eba-173">説明</span><span class="sxs-lookup"><span data-stu-id="89eba-173">Description</span></span>                                                                                                                                  |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89eba-174">標準</span><span class="sxs-lookup"><span data-stu-id="89eba-174">Standard</span></span> |  <span data-ttu-id="89eba-175">[![5\_Nav\_テーブル](./media/5_nav_table.png)](./media/5_nav_table.png)</span><span class="sxs-lookup"><span data-stu-id="89eba-175">[![5\_Nav\_Table](./media/5_nav_table.png)](./media/5_nav_table.png)</span></span> | <span data-ttu-id="89eba-176">このタイプのタイルでは、ビジネス データは表示されません。</span><span class="sxs-lookup"><span data-stu-id="89eba-176">This type of tile does not show any business data.</span></span>                                                                                           |
| <span data-ttu-id="89eba-177">COUNT</span><span class="sxs-lookup"><span data-stu-id="89eba-177">Count</span></span>    |  <span data-ttu-id="89eba-178">[![6\_Nav\_テーブル](./media/6_nav_table.png)](./media/6_nav_table.png)</span><span class="sxs-lookup"><span data-stu-id="89eba-178">[![6\_Nav\_Table](./media/6_nav_table.png)](./media/6_nav_table.png)</span></span> | <span data-ttu-id="89eba-179">このタイプのタイルは、参照されたフォームのクエリ内のアイテムの数を示します。</span><span class="sxs-lookup"><span data-stu-id="89eba-179">This type of tile shows a count of the items in the referenced form’s query.</span></span> <span data-ttu-id="89eba-180">この例でのタイルは **ShortWide** サイズを使用することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="89eba-180">Note that the tile in this example uses the **ShortWide** size.</span></span> |
| <span data-ttu-id="89eba-181">KPI</span><span class="sxs-lookup"><span data-stu-id="89eba-181">KPI</span></span>      |  <span data-ttu-id="89eba-182">[![7\_Nav\_テーブル](./media/7_nav_table.png)](./media/7_nav_table.png)</span><span class="sxs-lookup"><span data-stu-id="89eba-182">[![7\_Nav\_Table](./media/7_nav_table.png)](./media/7_nav_table.png)</span></span> | <span data-ttu-id="89eba-183">このタイプのタイルは、KPI からのデータの要約を示します。</span><span class="sxs-lookup"><span data-stu-id="89eba-183">This type of tile shows a summary of data from a KPI.</span></span>                                                                                        |
| <span data-ttu-id="89eba-184">リンク</span><span class="sxs-lookup"><span data-stu-id="89eba-184">Link</span></span>     |  <span data-ttu-id="89eba-185">[![8\_Nav\_テーブル](./media/8_nav_table.png)](./media/8_nav_table.png)</span><span class="sxs-lookup"><span data-stu-id="89eba-185">[![8\_Nav\_Table](./media/8_nav_table.png)](./media/8_nav_table.png)</span></span> | <span data-ttu-id="89eba-186">このタイプのタイルは URL を指します。</span><span class="sxs-lookup"><span data-stu-id="89eba-186">This type of tile points to a URL.</span></span> <span data-ttu-id="89eba-187">タイルは**標準**タイプのタイルと同じ外観を持ちます。</span><span class="sxs-lookup"><span data-stu-id="89eba-187">The tile has the same appearance as a tile of the **Standard** type.</span></span>                                      |

<span data-ttu-id="89eba-188">モデリングについては、まず抽象要素であるタイル要素を作成します。</span><span class="sxs-lookup"><span data-stu-id="89eba-188">For modeling, you first create a tile element, which is an abstract element.</span></span> <span data-ttu-id="89eba-189">タイル要素は、フォーム上でタイル ボタン要素によって参照されます。</span><span class="sxs-lookup"><span data-stu-id="89eba-189">The tile element is then referenced on a form by a tile button element.</span></span> <span data-ttu-id="89eba-190">複数のタイル ボタン要素が、1 つのタイルを参照できます。</span><span class="sxs-lookup"><span data-stu-id="89eba-190">Multiple tile button elements can refer to a single tile.</span></span> <span data-ttu-id="89eba-191">タイルは、最初に**タイプ**プロパティ（**Standard**、**Count**、**KPI**、**Link** の有効な値を持つ）によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="89eba-191">Tiles are defined first by the **Type** property (which has valid values of **Standard**, **Count**, **KPI**, and **Link**).</span></span> <span data-ttu-id="89eba-192">タイプを指定した後は、各タイプごとに次の最小プロパティーを指定します。</span><span class="sxs-lookup"><span data-stu-id="89eba-192">After you specify the type, you specify the following minimum properties for each type:</span></span>

-   <span data-ttu-id="89eba-193">**標準** および **カウント**:</span><span class="sxs-lookup"><span data-stu-id="89eba-193">**Standard** and **Count**:</span></span>
    -   <span data-ttu-id="89eba-194">ラベル</span><span class="sxs-lookup"><span data-stu-id="89eba-194">Label</span></span>
    -   <span data-ttu-id="89eba-195">メニュー項目名</span><span class="sxs-lookup"><span data-stu-id="89eba-195">Menu Item Name</span></span>
    -   <span data-ttu-id="89eba-196">メニュー項目タイプ</span><span class="sxs-lookup"><span data-stu-id="89eba-196">Menu Item Type</span></span>
-   <span data-ttu-id="89eba-197">**KPI**:</span><span class="sxs-lookup"><span data-stu-id="89eba-197">**KPI**:</span></span>
    -   <span data-ttu-id="89eba-198">ラベル</span><span class="sxs-lookup"><span data-stu-id="89eba-198">Label</span></span>
    -   <span data-ttu-id="89eba-199">KPI</span><span class="sxs-lookup"><span data-stu-id="89eba-199">KPI</span></span>
-   <span data-ttu-id="89eba-200">**リンク**:</span><span class="sxs-lookup"><span data-stu-id="89eba-200">**Link**:</span></span>
    -   <span data-ttu-id="89eba-201">ラベル</span><span class="sxs-lookup"><span data-stu-id="89eba-201">Label</span></span>
    -   <span data-ttu-id="89eba-202">URL</span><span class="sxs-lookup"><span data-stu-id="89eba-202">URL</span></span>

<span data-ttu-id="89eba-203">これらのプロパティが定義された後、タイルが完了します。</span><span class="sxs-lookup"><span data-stu-id="89eba-203">After these properties are defined, your tile is complete.</span></span> <span data-ttu-id="89eba-204">ユーザー エクスペリエンスを豊かにするために、**標準**と**リンク**のタイプのタイルを画像に含めることができます。</span><span class="sxs-lookup"><span data-stu-id="89eba-204">To make the user experience richer, you can optionally extend tiles of the **Standard** and **Link** types so that they include images.</span></span> <span data-ttu-id="89eba-205">イメージを追加するには、次のプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="89eba-205">Use the following properties to add images.</span></span>

| <span data-ttu-id="89eba-206">プロパティ</span><span class="sxs-lookup"><span data-stu-id="89eba-206">Property</span></span>       | <span data-ttu-id="89eba-207">説明</span><span class="sxs-lookup"><span data-stu-id="89eba-207">Description</span></span>                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89eba-208">イメージの場所</span><span class="sxs-lookup"><span data-stu-id="89eba-208">Image Location</span></span> | <span data-ttu-id="89eba-209">[アクション](action-controls.md)で基本的なボタンの動作に関する情報を参照してください。</span><span class="sxs-lookup"><span data-stu-id="89eba-209">See the information about basic button behavior in [Actions](action-controls.md).</span></span> |
| <span data-ttu-id="89eba-210">通常のイメージ</span><span class="sxs-lookup"><span data-stu-id="89eba-210">Normal Image</span></span>   | <span data-ttu-id="89eba-211">[アクション](action-controls.md)で基本的なボタンの動作に関する情報を参照してください。</span><span class="sxs-lookup"><span data-stu-id="89eba-211">See the information about basic button behavior in [Actions](action-controls.md).</span></span> |
| <span data-ttu-id="89eba-212">タイル表示</span><span class="sxs-lookup"><span data-stu-id="89eba-212">Tile Display</span></span>   | <span data-ttu-id="89eba-213">画像がどのようにタイルに表示されるかを定義します。</span><span class="sxs-lookup"><span data-stu-id="89eba-213">Define how the image appears on the tile.</span></span>                                                                                          |

<span data-ttu-id="89eba-214">**Tile Display** プロパティの有効なオプションと対応する動作は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="89eba-214">The following are the valid options and corresponding behaviors for the **Tile Display** property.</span></span>

| <span data-ttu-id="89eba-215">先頭値</span><span class="sxs-lookup"><span data-stu-id="89eba-215">Value</span></span>           | <span data-ttu-id="89eba-216">説明</span><span class="sxs-lookup"><span data-stu-id="89eba-216">Description</span></span>                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89eba-217">自動</span><span class="sxs-lookup"><span data-stu-id="89eba-217">Auto</span></span>            | <span data-ttu-id="89eba-218">動作は、**TextAndImage**の動作と同じです。</span><span class="sxs-lookup"><span data-stu-id="89eba-218">The behavior is the same as the behavior for **TextAndImage**.</span></span>                                                                                                                                         |
| <span data-ttu-id="89eba-219">TextAndImage</span><span class="sxs-lookup"><span data-stu-id="89eba-219">TextAndImage</span></span>    | <span data-ttu-id="89eba-220">タイルは指定されたラベルとその上にある小さなコンテナーにイメージを表示します。</span><span class="sxs-lookup"><span data-stu-id="89eba-220">The tile shows the specified label and the image in a small container above it.</span></span> <span data-ttu-id="89eba-221">たとえば、**アプリのリンク**タイルは、この値を使用します。</span><span class="sxs-lookup"><span data-stu-id="89eba-221">For example, the **App links** tile uses this value.</span></span>                                                                   |
| <span data-ttu-id="89eba-222">TextOnly</span><span class="sxs-lookup"><span data-stu-id="89eba-222">TextOnly</span></span>        | <span data-ttu-id="89eba-223">その他の 2 つのイメージ関連のプロパティは無視され、ラベルのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="89eba-223">The other two image-related properties are ignored, and only the label is shown.</span></span>                                                                                                                       |
| <span data-ttu-id="89eba-224">ImageOnly</span><span class="sxs-lookup"><span data-stu-id="89eba-224">ImageOnly</span></span>       | <span data-ttu-id="89eba-225">ラベルは無視され、画像のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="89eba-225">The label is ignored, and only the image is shown.</span></span>                                                                                                                                                     |
| <span data-ttu-id="89eba-226">BackgroundImage</span><span class="sxs-lookup"><span data-stu-id="89eba-226">BackgroundImage</span></span> | <span data-ttu-id="89eba-227">指定されたイメージは、エッジからエッジまでタイルを塗りつぶすように展開され、ラベルは同じ場所のイメージにオーバーレイされます。</span><span class="sxs-lookup"><span data-stu-id="89eba-227">The specified image is expanded to fill the tile from edge to edge, and the label is overlaid on the image in the same location.</span></span> <span data-ttu-id="89eba-228">網かけは、読みやすさを維持するためにテキストの後ろに適用されます。</span><span class="sxs-lookup"><span data-stu-id="89eba-228">Shading is applied behind the text to ensure that it remains legible.</span></span> |

<span data-ttu-id="89eba-229">**注記:** **BackgroundImage** 値が使用されている場合、次の制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="89eba-229">**Note:** The following limitations apply when the **BackgroundImage** value is used:</span></span>

-   <span data-ttu-id="89eba-230">記号を使用している場合は表示されません。</span><span class="sxs-lookup"><span data-stu-id="89eba-230">If a symbol is used, it isn't displayed.</span></span>
-   <span data-ttu-id="89eba-231">指定したイメージのサイズはありません。</span><span class="sxs-lookup"><span data-stu-id="89eba-231">The image that you specify isn't resized.</span></span> <span data-ttu-id="89eba-232">そのため、適切なサイズのイメージを作成して、タイルが正しく塗りつぶされるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="89eba-232">Therefore, you must create an image of the appropriate size to guarantee that it fills the tile correctly.</span></span> <span data-ttu-id="89eba-233">現在、標準サイズタイルはそれぞれの側に 130 ピクセルの正方形です。</span><span class="sxs-lookup"><span data-stu-id="89eba-233">Currently, a standard-sized tile is a square that is 130 pixels on each side.</span></span>

## <a name="navigation-search"></a><span data-ttu-id="89eba-234">ナビゲーション検索</span><span class="sxs-lookup"><span data-stu-id="89eba-234">Navigation search</span></span>
<span data-ttu-id="89eba-235">ナビゲーション ウィンドウとダッシュボードに表示されるフォームやワークスペースを検索してナビゲートするための、便利な検索メカニズムがあります。</span><span class="sxs-lookup"><span data-stu-id="89eba-235">There is a convenient search mechanism for finding and navigating to forms and workspaces that appear in the navigation pane and on the dashboard.</span></span> <span data-ttu-id="89eba-236">たとえば、キーワード「すべての販売注文」の検索は、これらのキーワードに一致するナビゲーション要素の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="89eba-236">For example, a search on the keywords "all sales order" returns a list of navigation elements that match those keywords.</span></span> 

<span data-ttu-id="89eba-237">[![navSearchExample](./media/navsearchexample.png)](./media/navsearchexample.png)</span><span class="sxs-lookup"><span data-stu-id="89eba-237">[![navSearchExample](./media/navsearchexample.png)](./media/navsearchexample.png)</span></span> 

<span data-ttu-id="89eba-238">検索キーワードは、ナビゲーション要素のキャプションだけでなく、対応するパスにも一致します。</span><span class="sxs-lookup"><span data-stu-id="89eba-238">The search keywords are matched not only to the caption of the navigation elements but also to the corresponding path.</span></span> <span data-ttu-id="89eba-239">たとえば、キーワード「ven bal レポート」の検索は、キャプションで「仕入先残高」およびパスで「レポート」に一致する結果を返します。</span><span class="sxs-lookup"><span data-stu-id="89eba-239">For example, a search on the keywords "ven bal report" returns results that match "vendor balance" in the caption and "report" in the path.</span></span> 

<span data-ttu-id="89eba-240">[![navSearchExample2](./media/navsearchexample2.png)](./media/navsearchexample2.png)</span><span class="sxs-lookup"><span data-stu-id="89eba-240">[![navSearchExample2](./media/navsearchexample2.png)](./media/navsearchexample2.png)</span></span>



