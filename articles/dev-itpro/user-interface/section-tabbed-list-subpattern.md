---
title: "セクション タブ付きリストのサブパターン"
description: "この記事では、セクション タブ付きリストのサブパターンに関する情報を提供します。 このサブパターンは、それぞれにデータのフィルタ処理されたリストを含む垂直タブセットが入ったパノラマ セクション専用の、運用ワークスペース パターンの一部として使用されます。"
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
ms.custom: 29291
ms.assetid: 3f8b00ff-54f0-4e32-bd7f-b94a74785537
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 61b0bd619eef4e20b68b08d338e6d2d31e76141d
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="section-tabbed-list-subpattern"></a><span data-ttu-id="b2454-104">セクション タブ付きリストのサブパターン</span><span class="sxs-lookup"><span data-stu-id="b2454-104">Section Tabbed List subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2454-105">この記事では、セクション タブ付きリストのサブパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="b2454-105">This article provides information about the Section Tabbed List subpattern.</span></span> <span data-ttu-id="b2454-106">このサブパターンは、それぞれにデータのフィルタ処理されたリストを含む垂直タブセットが入ったパノラマ セクション専用の、運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="b2454-106">This subpattern is used as part of the Operational Workspace pattern, specifically for a panorama section that contains a set of vertical tabs, each of which contains a filtered list of data.</span></span>

<a name="usage"></a><span data-ttu-id="b2454-107">用途</span><span class="sxs-lookup"><span data-stu-id="b2454-107">Usage</span></span>
-----

<span data-ttu-id="b2454-108">セクション タブ付きリストのサブパターンは、それぞれにデータのフィルタ処理されたリストを含む垂直タブセットが入ったパノラマ セクション専用の、運用ワークスペース パターンの一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="b2454-108">The Section Tabbed List subpattern is used as part of the Operational Workspace pattern, specifically for a panorama section that contains a set of vertical tabs, each of which contains a filtered list of data.</span></span>

## <a name="wireframe"></a><span data-ttu-id="b2454-109">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="b2454-109">Wireframe</span></span>
<span data-ttu-id="b2454-110">[![sectionTabbedListWireframe](./media/sectiontabbedlistwireframe.png)](./media/sectiontabbedlistwireframe.png)</span><span class="sxs-lookup"><span data-stu-id="b2454-110">[![sectionTabbedListWireframe](./media/sectiontabbedlistwireframe.png)](./media/sectiontabbedlistwireframe.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a><span data-ttu-id="b2454-111">Microsoft Dynamics AX のパータン変更</span><span class="sxs-lookup"><span data-stu-id="b2454-111">Pattern changes for Microsoft Dynamics AX</span></span>
<span data-ttu-id="b2454-112">このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="b2454-112">This pattern didn't exist for Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="b2454-113">モデル</span><span class="sxs-lookup"><span data-stu-id="b2454-113">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="b2454-114">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="b2454-114">High-level structure</span></span>

- <span data-ttu-id="b2454-115">TabPage</span><span class="sxs-lookup"><span data-stu-id="b2454-115">TabPage</span></span>
- <span data-ttu-id="b2454-116">TabbedList (タブ) (Style=VerticalTabs)</span><span class="sxs-lookup"><span data-stu-id="b2454-116">TabbedList (Tab) (Style=VerticalTabs)</span></span>

    - <span data-ttu-id="b2454-117">*TabbedListPage (TabPage)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="b2454-117">*TabbedListPage (TabPage) \[0..N\]*</span></span>

        - <span data-ttu-id="b2454-118">TargetForm (FormPart)</span><span class="sxs-lookup"><span data-stu-id="b2454-118">TargetForm (FormPart)</span></span>

<span data-ttu-id="b2454-119">各フォーム パーツでは、セクションの内容を含むフォームを指します。</span><span class="sxs-lookup"><span data-stu-id="b2454-119">Each Form Part points to a form that contains the content for the section.</span></span> <span data-ttu-id="b2454-120">これらのフォームはそれぞれ、Form Part Section List フォーム パターンの 1 つを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2454-120">Each of these forms should use one of the Form Part Section List form patterns.</span></span>

### <a name="core-components"></a><span data-ttu-id="b2454-121">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b2454-121">Core components</span></span>

<span data-ttu-id="b2454-122">セクション タブ付きリストをワークスペース内の適切なタブ ページに適用します。</span><span class="sxs-lookup"><span data-stu-id="b2454-122">Apply Section Tabbed List to the appropriate tab page in the workspace.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="b2454-123">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="b2454-123">Related container patterns</span></span>

-   [<span data-ttu-id="b2454-124">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="b2454-124">Operational Workspace</span></span>](workspace-form-pattern.md)
-   [<span data-ttu-id="b2454-125">フォーム パート セクション リスト</span><span class="sxs-lookup"><span data-stu-id="b2454-125">Form Part Section List</span></span>](section-list-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="b2454-126">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="b2454-126">UX guidelines</span></span>
<span data-ttu-id="b2454-127">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="b2454-127">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="b2454-128">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="b2454-128">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="b2454-129">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="b2454-129">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="b2454-130">少なくとも 1 つのリストはタブ付きリストのセクション内に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2454-130">At least one list should be present in the tabbed list section.</span></span>
-   <span data-ttu-id="b2454-131">各フォーム パーツ コントロールでは、いずれかの[フォーム パーツ セクション リスト](section-list-form-pattern.md)パターンを使用するフォームを指す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2454-131">Each Form Part Control should point to a form that uses one of the [Form Part Section List](section-list-form-pattern.md) patterns.</span></span>

## <a name="examples"></a><span data-ttu-id="b2454-132">例</span><span class="sxs-lookup"><span data-stu-id="b2454-132">Examples</span></span>
<span data-ttu-id="b2454-133">フォーム: **PurchOrderMaintainWorkspace** (**すべてのワークスペース** &gt; **発注書の準備**)</span><span class="sxs-lookup"><span data-stu-id="b2454-133">Form: **PurchOrderMaintainWorkspace** (**All workspaces** &gt; **Purchase order preparation**)</span></span> 

<span data-ttu-id="b2454-134">[![tabbedListSectionExample](./media/tabbedlistsectionexample.png)](./media/tabbedlistsectionexample.png)</span><span class="sxs-lookup"><span data-stu-id="b2454-134">[![tabbedListSectionExample](./media/tabbedlistsectionexample.png)](./media/tabbedlistsectionexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="b2454-135">付録</span><span class="sxs-lookup"><span data-stu-id="b2454-135">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="b2454-136">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="b2454-136">Frequently asked questions</span></span>

<span data-ttu-id="b2454-137">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="b2454-137">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="b2454-138">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="b2454-138">Open issues</span></span>

<span data-ttu-id="b2454-139">None</span><span class="sxs-lookup"><span data-stu-id="b2454-139">None</span></span>
