---
title: "リスト"
description: "リスト コントロール タイプ。"
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: 
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ce6d1bc2448424aab99431cb291768ed6c1d55de
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="list-type"></a><span data-ttu-id="202e6-103">List タイプ</span><span class="sxs-lookup"><span data-stu-id="202e6-103">List Type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="202e6-104">リスト コントロール タイプ。</span><span class="sxs-lookup"><span data-stu-id="202e6-104">List control type.</span></span>
<span data-ttu-id="202e6-105">リストは、任意の数の行を含むコントロールです。</span><span class="sxs-lookup"><span data-stu-id="202e6-105">A list is a control that contains any numbers of rows.</span></span>
<span data-ttu-id="202e6-106">各行は、任意の数のコントロールに対するレイアウト用テンプレートに従います。</span><span class="sxs-lookup"><span data-stu-id="202e6-106">Each row follows a template for the layout of any number of controls.</span></span>
<span data-ttu-id="202e6-107">リストには簡易とカードの 2 つのスタイルがあります。</span><span class="sxs-lookup"><span data-stu-id="202e6-107">Lists come in two styles: simple and card.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="202e6-108">階層</span><span class="sxs-lookup"><span data-stu-id="202e6-108">Hierarchy</span></span>

[<span data-ttu-id="202e6-109">ContainerControl</span><span class="sxs-lookup"><span data-stu-id="202e6-109">ContainerControl</span></span>](view-model-control-container-icontainercontrol-icontainercontrol.md) <br><span data-ttu-id="202e6-110">&nbsp;&nbsp;&nbsp;└─ リスト</span><span class="sxs-lookup"><span data-stu-id="202e6-110">&nbsp;&nbsp;&nbsp;└─ List</span></span> <br>

## <a name="index"></a><span data-ttu-id="202e6-111">指数</span><span class="sxs-lookup"><span data-stu-id="202e6-111">Index</span></span>

### <a name="properties"></a><span data-ttu-id="202e6-112">プロパティ</span><span class="sxs-lookup"><span data-stu-id="202e6-112">Properties</span></span>

* [<span data-ttu-id="202e6-113">$accessibility</span><span class="sxs-lookup"><span data-stu-id="202e6-113">$accessibility</span></span>](view-model-control-list-ilist-ilist.md#accessibility)
* [<span data-ttu-id="202e6-114">DefaultSearchColumn</span><span class="sxs-lookup"><span data-stu-id="202e6-114">DefaultSearchColumn</span></span>](view-model-control-list-ilist-ilist.md#defaultsearchcolumn)
* [<span data-ttu-id="202e6-115">コンテナー</span><span class="sxs-lookup"><span data-stu-id="202e6-115">container</span></span>](view-model-control-list-ilist-ilist.md#container)
* [<span data-ttu-id="202e6-116">emptyListMessage</span><span class="sxs-lookup"><span data-stu-id="202e6-116">emptyListMessage</span></span>](view-model-control-list-ilist-ilist.md#emptylistmessage)
* [<span data-ttu-id="202e6-117">enableMultiSelect</span><span class="sxs-lookup"><span data-stu-id="202e6-117">enableMultiSelect</span></span>](view-model-control-list-ilist-ilist.md#enablemultiselect)
* [<span data-ttu-id="202e6-118">ジェネリック</span><span class="sxs-lookup"><span data-stu-id="202e6-118">generic</span></span>](view-model-control-list-ilist-ilist.md#generic)
* [<span data-ttu-id="202e6-119">getDataSource</span><span class="sxs-lookup"><span data-stu-id="202e6-119">getDataSource</span></span>](view-model-control-list-ilist-ilist.md#getdatasource)
* [<span data-ttu-id="202e6-120">非表示</span><span class="sxs-lookup"><span data-stu-id="202e6-120">hidden</span></span>](view-model-control-list-ilist-ilist.md#hidden)
* [<span data-ttu-id="202e6-121">hideEmptyListMessage</span><span class="sxs-lookup"><span data-stu-id="202e6-121">hideEmptyListMessage</span></span>](view-model-control-list-ilist-ilist.md#hideemptylistmessage)
* [<span data-ttu-id="202e6-122">imageFields</span><span class="sxs-lookup"><span data-stu-id="202e6-122">imageFields</span></span>](view-model-control-list-ilist-ilist.md#imagefields)
* [<span data-ttu-id="202e6-123">performingRemoteSearch</span><span class="sxs-lookup"><span data-stu-id="202e6-123">performingRemoteSearch</span></span>](view-model-control-list-ilist-ilist.md#performingremotesearch)
* [<span data-ttu-id="202e6-124">searchQuery</span><span class="sxs-lookup"><span data-stu-id="202e6-124">searchQuery</span></span>](view-model-control-list-ilist-ilist.md#searchquery)

### <a name="methods"></a><span data-ttu-id="202e6-125">メソッド</span><span class="sxs-lookup"><span data-stu-id="202e6-125">Methods</span></span>

* [<span data-ttu-id="202e6-126">allowsNavigation</span><span class="sxs-lookup"><span data-stu-id="202e6-126">allowsNavigation</span></span>](view-model-control-list-ilist-ilist.md#allowsnavigation)
* [<span data-ttu-id="202e6-127">applyDesign</span><span class="sxs-lookup"><span data-stu-id="202e6-127">applyDesign</span></span>](view-model-control-list-ilist-ilist.md#applydesign)
* [<span data-ttu-id="202e6-128">applySearch</span><span class="sxs-lookup"><span data-stu-id="202e6-128">applySearch</span></span>](view-model-control-list-ilist-ilist.md#applysearch)
* [<span data-ttu-id="202e6-129">canPerformRemoteSearch</span><span class="sxs-lookup"><span data-stu-id="202e6-129">canPerformRemoteSearch</span></span>](view-model-control-list-ilist-ilist.md#canperformremotesearch)
* [<span data-ttu-id="202e6-130">clearSearch</span><span class="sxs-lookup"><span data-stu-id="202e6-130">clearSearch</span></span>](view-model-control-list-ilist-ilist.md#clearsearch)
* [<span data-ttu-id="202e6-131">dataContext</span><span class="sxs-lookup"><span data-stu-id="202e6-131">dataContext</span></span>](view-model-control-list-ilist-ilist.md#datacontext)
* [<span data-ttu-id="202e6-132">getColumnLabel</span><span class="sxs-lookup"><span data-stu-id="202e6-132">getColumnLabel</span></span>](view-model-control-list-ilist-ilist.md#getcolumnlabel)
* [<span data-ttu-id="202e6-133">getControl</span><span class="sxs-lookup"><span data-stu-id="202e6-133">getControl</span></span>](view-model-control-list-ilist-ilist.md#getcontrol)
* [<span data-ttu-id="202e6-134">getControlById</span><span class="sxs-lookup"><span data-stu-id="202e6-134">getControlById</span></span>](view-model-control-list-ilist-ilist.md#getcontrolbyid)
* [<span data-ttu-id="202e6-135">getControlMetadata</span><span class="sxs-lookup"><span data-stu-id="202e6-135">getControlMetadata</span></span>](view-model-control-list-ilist-ilist.md#getcontrolmetadata)
* [<span data-ttu-id="202e6-136">getControlMetadataById</span><span class="sxs-lookup"><span data-stu-id="202e6-136">getControlMetadataById</span></span>](view-model-control-list-ilist-ilist.md#getcontrolmetadatabyid)
* [<span data-ttu-id="202e6-137">getData</span><span class="sxs-lookup"><span data-stu-id="202e6-137">getData</span></span>](view-model-control-list-ilist-ilist.md#getdata)
* [<span data-ttu-id="202e6-138">getDesign</span><span class="sxs-lookup"><span data-stu-id="202e6-138">getDesign</span></span>](view-model-control-list-ilist-ilist.md#getdesign)
* [<span data-ttu-id="202e6-139">getListData</span><span class="sxs-lookup"><span data-stu-id="202e6-139">getListData</span></span>](view-model-control-list-ilist-ilist.md#getlistdata)
* [<span data-ttu-id="202e6-140">getRenderedRows</span><span class="sxs-lookup"><span data-stu-id="202e6-140">getRenderedRows</span></span>](view-model-control-list-ilist-ilist.md#getrenderedrows)
* [<span data-ttu-id="202e6-141">getRowNavigation</span><span class="sxs-lookup"><span data-stu-id="202e6-141">getRowNavigation</span></span>](view-model-control-list-ilist-ilist.md#getrownavigation)
* [<span data-ttu-id="202e6-142">getRowSelectionCount</span><span class="sxs-lookup"><span data-stu-id="202e6-142">getRowSelectionCount</span></span>](view-model-control-list-ilist-ilist.md#getrowselectioncount)
* [<span data-ttu-id="202e6-143">getRowSelections</span><span class="sxs-lookup"><span data-stu-id="202e6-143">getRowSelections</span></span>](view-model-control-list-ilist-ilist.md#getrowselections)
* [<span data-ttu-id="202e6-144">getRowTracking</span><span class="sxs-lookup"><span data-stu-id="202e6-144">getRowTracking</span></span>](view-model-control-list-ilist-ilist.md#getrowtracking)
* [<span data-ttu-id="202e6-145">getSearchColumn</span><span class="sxs-lookup"><span data-stu-id="202e6-145">getSearchColumn</span></span>](view-model-control-list-ilist-ilist.md#getsearchcolumn)
* [<span data-ttu-id="202e6-146">getSearchColumnLabel</span><span class="sxs-lookup"><span data-stu-id="202e6-146">getSearchColumnLabel</span></span>](view-model-control-list-ilist-ilist.md#getsearchcolumnlabel)
* [<span data-ttu-id="202e6-147">getSearchableColumns</span><span class="sxs-lookup"><span data-stu-id="202e6-147">getSearchableColumns</span></span>](view-model-control-list-ilist-ilist.md#getsearchablecolumns)
* [<span data-ttu-id="202e6-148">hideSearchBar</span><span class="sxs-lookup"><span data-stu-id="202e6-148">hideSearchBar</span></span>](view-model-control-list-ilist-ilist.md#hidesearchbar)
* [<span data-ttu-id="202e6-149">isEditable</span><span class="sxs-lookup"><span data-stu-id="202e6-149">isEditable</span></span>](view-model-control-list-ilist-ilist.md#iseditable)
* [<span data-ttu-id="202e6-150">loadMetaData</span><span class="sxs-lookup"><span data-stu-id="202e6-150">loadMetaData</span></span>](view-model-control-list-ilist-ilist.md#loadmetadata)
* [<span data-ttu-id="202e6-151">loadMore</span><span class="sxs-lookup"><span data-stu-id="202e6-151">loadMore</span></span>](view-model-control-list-ilist-ilist.md#loadmore)
* [<span data-ttu-id="202e6-152">メタデータ</span><span class="sxs-lookup"><span data-stu-id="202e6-152">metadata</span></span>](view-model-control-list-ilist-ilist.md#metadata)
* [<span data-ttu-id="202e6-153">親</span><span class="sxs-lookup"><span data-stu-id="202e6-153">parent</span></span>](view-model-control-list-ilist-ilist.md#parent)
* [<span data-ttu-id="202e6-154">performRemoteSearch</span><span class="sxs-lookup"><span data-stu-id="202e6-154">performRemoteSearch</span></span>](view-model-control-list-ilist-ilist.md#performremotesearch)
* [<span data-ttu-id="202e6-155">ルート</span><span class="sxs-lookup"><span data-stu-id="202e6-155">root</span></span>](view-model-control-list-ilist-ilist.md#root)
* [<span data-ttu-id="202e6-156">selectSearchColumn</span><span class="sxs-lookup"><span data-stu-id="202e6-156">selectSearchColumn</span></span>](view-model-control-list-ilist-ilist.md#selectsearchcolumn)
* [<span data-ttu-id="202e6-157">setRowSections</span><span class="sxs-lookup"><span data-stu-id="202e6-157">setRowSections</span></span>](view-model-control-list-ilist-ilist.md#setrowsections)

### <a name="events"></a><span data-ttu-id="202e6-158">イベント</span><span class="sxs-lookup"><span data-stu-id="202e6-158">Events</span></span>

* [<span data-ttu-id="202e6-159">onRowCreate</span><span class="sxs-lookup"><span data-stu-id="202e6-159">onRowCreate</span></span>](view-model-control-list-ilist-ilist.md#onrowcreate)
* [<span data-ttu-id="202e6-160">onRowSelect</span><span class="sxs-lookup"><span data-stu-id="202e6-160">onRowSelect</span></span>](view-model-control-list-ilist-ilist.md#onrowselect)

## <a name="properties"></a><span data-ttu-id="202e6-161">プロパティ</span><span class="sxs-lookup"><span data-stu-id="202e6-161">Properties</span></span>

### <a name="accessibility"></a><span data-ttu-id="202e6-162">$accessibility</span><span class="sxs-lookup"><span data-stu-id="202e6-162">$accessibility</span></span>

<span data-ttu-id="202e6-163">$accessibility: すべて</span><span class="sxs-lookup"><span data-stu-id="202e6-163">$accessibility: any</span></span>




### <a name="defaultsearchcolumn"></a><span data-ttu-id="202e6-164">DefaultSearchColumn</span><span class="sxs-lookup"><span data-stu-id="202e6-164">DefaultSearchColumn</span></span>

<span data-ttu-id="202e6-165">DefaultSearchColumn: 文字列</span><span class="sxs-lookup"><span data-stu-id="202e6-165">DefaultSearchColumn: string</span></span>




### <a name="container"></a><span data-ttu-id="202e6-166">コンテナー</span><span class="sxs-lookup"><span data-stu-id="202e6-166">container</span></span>

<span data-ttu-id="202e6-167">container: ブール値</span><span class="sxs-lookup"><span data-stu-id="202e6-167">container: boolean</span></span>

<span data-ttu-id="202e6-168">コントロールがコンテナーの場合は true です。</span><span class="sxs-lookup"><span data-stu-id="202e6-168">True if the control is a container.</span></span>

> <span data-ttu-id="202e6-169">[ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[container](view-model-control-container-icontainercontrol-icontainercontrol.md#container) から継承</span><span class="sxs-lookup"><span data-stu-id="202e6-169">Inherited from [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[container](view-model-control-container-icontainercontrol-icontainercontrol.md#container)</span></span>
> 
> <span data-ttu-id="202e6-170">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="202e6-170">Overrides [Control](view-model-control-basecontrol-icontrol-icontrol.md).[container](view-model-control-basecontrol-icontrol-icontrol.md#container)</span></span>


### <a name="emptylistmessage"></a><span data-ttu-id="202e6-171">emptyListMessage</span><span class="sxs-lookup"><span data-stu-id="202e6-171">emptyListMessage</span></span>

<span data-ttu-id="202e6-172">emptyListMessage: string</span><span class="sxs-lookup"><span data-stu-id="202e6-172">emptyListMessage: string</span></span>

<span data-ttu-id="202e6-173">既定の空のリスト メッセージを上書きする設定可能なプロパティ。</span><span class="sxs-lookup"><span data-stu-id="202e6-173">Settable property to override default empty list message.</span></span>


### <a name="enablemultiselect"></a><span data-ttu-id="202e6-174">enableMultiSelect</span><span class="sxs-lookup"><span data-stu-id="202e6-174">enableMultiSelect</span></span>

<span data-ttu-id="202e6-175">enableMultiSelect: boolean</span><span class="sxs-lookup"><span data-stu-id="202e6-175">enableMultiSelect: boolean</span></span>




### <a name="generic"></a><span data-ttu-id="202e6-176">generic</span><span class="sxs-lookup"><span data-stu-id="202e6-176">generic</span></span>

<span data-ttu-id="202e6-177">generic: boolean (省略可)</span><span class="sxs-lookup"><span data-stu-id="202e6-177">generic: boolean (optional)</span></span> 



> <span data-ttu-id="202e6-178">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic) から継承</span><span class="sxs-lookup"><span data-stu-id="202e6-178">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[generic](view-model-control-basecontrol-icontrol-icontrol.md#generic)</span></span>


### <a name="getdatasource"></a><span data-ttu-id="202e6-179">getDataSource</span><span class="sxs-lookup"><span data-stu-id="202e6-179">getDataSource</span></span>

<span data-ttu-id="202e6-180">getDataSource: function(): any</span><span class="sxs-lookup"><span data-stu-id="202e6-180">getDataSource: function(): any</span></span>



> <span data-ttu-id="202e6-181">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource) から継承</span><span class="sxs-lookup"><span data-stu-id="202e6-181">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDataSource](view-model-control-basecontrol-icontrol-icontrol.md#getdatasource)</span></span>


### <a name="hidden"></a><span data-ttu-id="202e6-182">hidden</span><span class="sxs-lookup"><span data-stu-id="202e6-182">hidden</span></span>

<span data-ttu-id="202e6-183">hidden: boolean</span><span class="sxs-lookup"><span data-stu-id="202e6-183">hidden: boolean</span></span>

<span data-ttu-id="202e6-184">コントロールが非常時の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="202e6-184">True if the control is hidden.</span></span>

> <span data-ttu-id="202e6-185">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden) から継承</span><span class="sxs-lookup"><span data-stu-id="202e6-185">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[hidden](view-model-control-basecontrol-icontrol-icontrol.md#hidden)</span></span>


### <a name="hideemptylistmessage"></a><span data-ttu-id="202e6-186">hideEmptyListMessage</span><span class="sxs-lookup"><span data-stu-id="202e6-186">hideEmptyListMessage</span></span>

<span data-ttu-id="202e6-187">hideEmptyListMessage: boolean</span><span class="sxs-lookup"><span data-stu-id="202e6-187">hideEmptyListMessage: boolean</span></span>

<span data-ttu-id="202e6-188">True で一覧が空である場合、メッセージが表示されません。</span><span class="sxs-lookup"><span data-stu-id="202e6-188">If true, no message is shown if the list is empty.</span></span>
<span data-ttu-id="202e6-189">このプロパティを設定するには、対応するメタデータ プロパティを configureControl で更新します。</span><span class="sxs-lookup"><span data-stu-id="202e6-189">To set this property, update the corresponding metadata property via configureControl.</span></span>


### <a name="imagefields"></a><span data-ttu-id="202e6-190">imageFields</span><span class="sxs-lookup"><span data-stu-id="202e6-190">imageFields</span></span>

<span data-ttu-id="202e6-191">imageFields: any [ ]</span><span class="sxs-lookup"><span data-stu-id="202e6-191">imageFields: any [ ]</span></span>




### <a name="performingremotesearch"></a><span data-ttu-id="202e6-192">performingRemoteSearch</span><span class="sxs-lookup"><span data-stu-id="202e6-192">performingRemoteSearch</span></span>

<span data-ttu-id="202e6-193">performingRemoteSearch: boolean</span><span class="sxs-lookup"><span data-stu-id="202e6-193">performingRemoteSearch: boolean</span></span>




### <a name="searchquery"></a><span data-ttu-id="202e6-194">searchQuery</span><span class="sxs-lookup"><span data-stu-id="202e6-194">searchQuery</span></span>

<span data-ttu-id="202e6-195">searchQuery: [value: string]: any</span><span class="sxs-lookup"><span data-stu-id="202e6-195">searchQuery: [value: string]: any</span></span>




## <a name="methods"></a><span data-ttu-id="202e6-196">メソッド</span><span class="sxs-lookup"><span data-stu-id="202e6-196">Methods</span></span>

### <a name="allowsnavigation"></a><span data-ttu-id="202e6-197">allowsNavigation</span><span class="sxs-lookup"><span data-stu-id="202e6-197">allowsNavigation</span></span>


<span data-ttu-id="202e6-198">allowsNavigation(): boolean</span><span class="sxs-lookup"><span data-stu-id="202e6-198">allowsNavigation(): boolean</span></span>



#### <a name="returns-boolean"></a><span data-ttu-id="202e6-199">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-199">Returns boolean</span></span>

### <a name="applydesign"></a><span data-ttu-id="202e6-200">applyDesign</span><span class="sxs-lookup"><span data-stu-id="202e6-200">applyDesign</span></span>


<span data-ttu-id="202e6-201">applyDesign(IDesign: [ListDesign](view-model-control-list-ilist-ilistdesign.md)): void</span><span class="sxs-lookup"><span data-stu-id="202e6-201">applyDesign(IDesign: [ListDesign](view-model-control-list-ilist-ilistdesign.md)): void</span></span>

<span data-ttu-id="202e6-202">付与されたデザインをコントロールのデザインに適用します。</span><span class="sxs-lookup"><span data-stu-id="202e6-202">Applies given design to the design on the control.</span></span>
<span data-ttu-id="202e6-203">デザインが既に存在する場合は、設計のプロトタイプ チェーンが保持されます。</span><span class="sxs-lookup"><span data-stu-id="202e6-203">If a design already exists, the prototype chain of the design will be preserved.</span></span>

> <span data-ttu-id="202e6-204">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="202e6-204">Overrides [Control](view-model-control-basecontrol-icontrol-icontrol.md).[applyDesign](view-model-control-basecontrol-icontrol-icontrol.md#applydesign)</span></span>


#### <a name="parameters"></a><span data-ttu-id="202e6-205">パラメーター</span><span class="sxs-lookup"><span data-stu-id="202e6-205">Parameters</span></span>

| <span data-ttu-id="202e6-206">氏名</span><span class="sxs-lookup"><span data-stu-id="202e6-206">Name</span></span> | <span data-ttu-id="202e6-207">種類</span><span class="sxs-lookup"><span data-stu-id="202e6-207">Type</span></span> | <span data-ttu-id="202e6-208">説明</span><span class="sxs-lookup"><span data-stu-id="202e6-208">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="202e6-209">IDesign</span><span class="sxs-lookup"><span data-stu-id="202e6-209">IDesign</span></span>|[<span data-ttu-id="202e6-210">ListDesign</span><span class="sxs-lookup"><span data-stu-id="202e6-210">ListDesign</span></span>](view-model-control-list-ilist-ilistdesign.md)|<span data-ttu-id="202e6-211">デザイン プロパティをキーとして含むオブジェクト</span><span class="sxs-lookup"><span data-stu-id="202e6-211">object containing design properties as keys</span></span>|

#### <a name="returns-void"></a><span data-ttu-id="202e6-212">void を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-212">Returns void</span></span>

### <a name="applysearch"></a><span data-ttu-id="202e6-213">applySearch</span><span class="sxs-lookup"><span data-stu-id="202e6-213">applySearch</span></span>


<span data-ttu-id="202e6-214">applySearch(): void</span><span class="sxs-lookup"><span data-stu-id="202e6-214">applySearch(): void</span></span>



#### <a name="returns-void"></a><span data-ttu-id="202e6-215">void を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-215">Returns void</span></span>

### <a name="canperformremotesearch"></a><span data-ttu-id="202e6-216">canPerformRemoteSearch</span><span class="sxs-lookup"><span data-stu-id="202e6-216">canPerformRemoteSearch</span></span>


<span data-ttu-id="202e6-217">canPerformRemoteSearch(): boolean</span><span class="sxs-lookup"><span data-stu-id="202e6-217">canPerformRemoteSearch(): boolean</span></span>



#### <a name="returns-boolean"></a><span data-ttu-id="202e6-218">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-218">Returns boolean</span></span>

### <a name="clearsearch"></a><span data-ttu-id="202e6-219">clearSearch</span><span class="sxs-lookup"><span data-stu-id="202e6-219">clearSearch</span></span>


<span data-ttu-id="202e6-220">clearSearch(): void</span><span class="sxs-lookup"><span data-stu-id="202e6-220">clearSearch(): void</span></span>



#### <a name="returns-void"></a><span data-ttu-id="202e6-221">void を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-221">Returns void</span></span>

### <a name="datacontext"></a><span data-ttu-id="202e6-222">dataContext</span><span class="sxs-lookup"><span data-stu-id="202e6-222">dataContext</span></span>


<span data-ttu-id="202e6-223">dataContext(): any</span><span class="sxs-lookup"><span data-stu-id="202e6-223">dataContext(): any</span></span>



> <span data-ttu-id="202e6-224">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext) から継承</span><span class="sxs-lookup"><span data-stu-id="202e6-224">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[dataContext](view-model-control-basecontrol-icontrol-icontrol.md#datacontext)</span></span>

#### <a name="returns-any"></a><span data-ttu-id="202e6-225">any を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-225">Returns any</span></span>

### <a name="getcolumnlabel"></a><span data-ttu-id="202e6-226">getColumnLabel</span><span class="sxs-lookup"><span data-stu-id="202e6-226">getColumnLabel</span></span>


<span data-ttu-id="202e6-227">getColumnLabel(id: string): string</span><span class="sxs-lookup"><span data-stu-id="202e6-227">getColumnLabel(id: string): string</span></span>




#### <a name="parameters"></a><span data-ttu-id="202e6-228">パラメーター</span><span class="sxs-lookup"><span data-stu-id="202e6-228">Parameters</span></span>

| <span data-ttu-id="202e6-229">氏名</span><span class="sxs-lookup"><span data-stu-id="202e6-229">Name</span></span> | <span data-ttu-id="202e6-230">種類</span><span class="sxs-lookup"><span data-stu-id="202e6-230">Type</span></span> | <span data-ttu-id="202e6-231">説明</span><span class="sxs-lookup"><span data-stu-id="202e6-231">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="202e6-232">id</span><span class="sxs-lookup"><span data-stu-id="202e6-232">id</span></span>|<span data-ttu-id="202e6-233">string</span><span class="sxs-lookup"><span data-stu-id="202e6-233">string</span></span>||

#### <a name="returns-string"></a><span data-ttu-id="202e6-234">文字列を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-234">Returns string</span></span>

### <a name="getcontrol"></a><span data-ttu-id="202e6-235">getControl</span><span class="sxs-lookup"><span data-stu-id="202e6-235">getControl</span></span>


<span data-ttu-id="202e6-236">getControl(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span><span class="sxs-lookup"><span data-stu-id="202e6-236">getControl(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>

<span data-ttu-id="202e6-237">コントロールの名前の場合、コントロール インスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="202e6-237">Given the name of a control, returns the control instance.</span></span>

> <span data-ttu-id="202e6-238">[ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[getControl](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrol) から継承</span><span class="sxs-lookup"><span data-stu-id="202e6-238">Inherited from [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[getControl](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrol)</span></span>


#### <a name="parameters"></a><span data-ttu-id="202e6-239">パラメーター</span><span class="sxs-lookup"><span data-stu-id="202e6-239">Parameters</span></span>

| <span data-ttu-id="202e6-240">氏名</span><span class="sxs-lookup"><span data-stu-id="202e6-240">Name</span></span> | <span data-ttu-id="202e6-241">種類</span><span class="sxs-lookup"><span data-stu-id="202e6-241">Type</span></span> | <span data-ttu-id="202e6-242">説明</span><span class="sxs-lookup"><span data-stu-id="202e6-242">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="202e6-243">controlName</span><span class="sxs-lookup"><span data-stu-id="202e6-243">controlName</span></span>|<span data-ttu-id="202e6-244">string</span><span class="sxs-lookup"><span data-stu-id="202e6-244">string</span></span>|<span data-ttu-id="202e6-245">コントロール名</span><span class="sxs-lookup"><span data-stu-id="202e6-245">control name</span></span>|

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd"></a><span data-ttu-id="202e6-246">[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-246">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>



### <a name="getcontrolbyid"></a><span data-ttu-id="202e6-247">getControlById</span><span class="sxs-lookup"><span data-stu-id="202e6-247">getControlById</span></span>


<span data-ttu-id="202e6-248">getControlById(id: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span><span class="sxs-lookup"><span data-stu-id="202e6-248">getControlById(id: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>

<span data-ttu-id="202e6-249">コントロールの ID の場合、コントロール インスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="202e6-249">Given the ID of a control, returns the control instance.</span></span>

> <span data-ttu-id="202e6-250">[ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[getControlById](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrolbyid) から継承</span><span class="sxs-lookup"><span data-stu-id="202e6-250">Inherited from [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[getControlById](view-model-control-container-icontainercontrol-icontainercontrol.md#getcontrolbyid)</span></span>


#### <a name="parameters"></a><span data-ttu-id="202e6-251">パラメーター</span><span class="sxs-lookup"><span data-stu-id="202e6-251">Parameters</span></span>

| <span data-ttu-id="202e6-252">氏名</span><span class="sxs-lookup"><span data-stu-id="202e6-252">Name</span></span> | <span data-ttu-id="202e6-253">種類</span><span class="sxs-lookup"><span data-stu-id="202e6-253">Type</span></span> | <span data-ttu-id="202e6-254">説明</span><span class="sxs-lookup"><span data-stu-id="202e6-254">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="202e6-255">id</span><span class="sxs-lookup"><span data-stu-id="202e6-255">id</span></span>|<span data-ttu-id="202e6-256">string</span><span class="sxs-lookup"><span data-stu-id="202e6-256">string</span></span>|<span data-ttu-id="202e6-257">コントロール ID</span><span class="sxs-lookup"><span data-stu-id="202e6-257">control ID</span></span>|

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd"></a><span data-ttu-id="202e6-258">[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-258">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>



### <a name="getcontrolmetadata"></a><span data-ttu-id="202e6-259">getControlMetadata</span><span class="sxs-lookup"><span data-stu-id="202e6-259">getControlMetadata</span></span>


<span data-ttu-id="202e6-260">getControlMetadata(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span><span class="sxs-lookup"><span data-stu-id="202e6-260">getControlMetadata(controlName: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>




#### <a name="parameters"></a><span data-ttu-id="202e6-261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="202e6-261">Parameters</span></span>

| <span data-ttu-id="202e6-262">氏名</span><span class="sxs-lookup"><span data-stu-id="202e6-262">Name</span></span> | <span data-ttu-id="202e6-263">種類</span><span class="sxs-lookup"><span data-stu-id="202e6-263">Type</span></span> | <span data-ttu-id="202e6-264">説明</span><span class="sxs-lookup"><span data-stu-id="202e6-264">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="202e6-265">controlName</span><span class="sxs-lookup"><span data-stu-id="202e6-265">controlName</span></span>|<span data-ttu-id="202e6-266">string</span><span class="sxs-lookup"><span data-stu-id="202e6-266">string</span></span>||

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd"></a><span data-ttu-id="202e6-267">[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-267">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>

### <a name="getcontrolmetadatabyid"></a><span data-ttu-id="202e6-268">getControlMetadataById</span><span class="sxs-lookup"><span data-stu-id="202e6-268">getControlMetadataById</span></span>


<span data-ttu-id="202e6-269">getControlMetadataById(id: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span><span class="sxs-lookup"><span data-stu-id="202e6-269">getControlMetadataById(id: string): [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>




#### <a name="parameters"></a><span data-ttu-id="202e6-270">パラメーター</span><span class="sxs-lookup"><span data-stu-id="202e6-270">Parameters</span></span>

| <span data-ttu-id="202e6-271">氏名</span><span class="sxs-lookup"><span data-stu-id="202e6-271">Name</span></span> | <span data-ttu-id="202e6-272">種類</span><span class="sxs-lookup"><span data-stu-id="202e6-272">Type</span></span> | <span data-ttu-id="202e6-273">説明</span><span class="sxs-lookup"><span data-stu-id="202e6-273">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="202e6-274">id</span><span class="sxs-lookup"><span data-stu-id="202e6-274">id</span></span>|<span data-ttu-id="202e6-275">string</span><span class="sxs-lookup"><span data-stu-id="202e6-275">string</span></span>||

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd"></a><span data-ttu-id="202e6-276">[Control](view-model-control-basecontrol-icontrol-icontrol.md) を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-276">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md)</span></span>

### <a name="getdata"></a><span data-ttu-id="202e6-277">getData</span><span class="sxs-lookup"><span data-stu-id="202e6-277">getData</span></span>


<span data-ttu-id="202e6-278">getData(): any [ ]</span><span class="sxs-lookup"><span data-stu-id="202e6-278">getData(): any [ ]</span></span>



#### <a name="returns-any--"></a><span data-ttu-id="202e6-279">any [ ] を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-279">Returns any [ ]</span></span>

### <a name="getdesign"></a><span data-ttu-id="202e6-280">getDesign</span><span class="sxs-lookup"><span data-stu-id="202e6-280">getDesign</span></span>


<span data-ttu-id="202e6-281">getDesign(): [Design](view-model-ipage-idesign.md)</span><span class="sxs-lookup"><span data-stu-id="202e6-281">getDesign(): [Design](view-model-ipage-idesign.md)</span></span>

<span data-ttu-id="202e6-282">このコントロールのデザイン オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="202e6-282">Returns the design object of this control.</span></span>

> <span data-ttu-id="202e6-283">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign) から継承</span><span class="sxs-lookup"><span data-stu-id="202e6-283">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[getDesign](view-model-control-basecontrol-icontrol-icontrol.md#getdesign)</span></span>

#### <a name="returns-designview-model-ipage-idesignmd"></a><span data-ttu-id="202e6-284">[Design](view-model-ipage-idesign.md) を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-284">Returns [Design](view-model-ipage-idesign.md)</span></span>



### <a name="getlistdata"></a><span data-ttu-id="202e6-285">getListData</span><span class="sxs-lookup"><span data-stu-id="202e6-285">getListData</span></span>


<span data-ttu-id="202e6-286">getListData(): any</span><span class="sxs-lookup"><span data-stu-id="202e6-286">getListData(): any</span></span>



#### <a name="returns-any"></a><span data-ttu-id="202e6-287">any を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-287">Returns any</span></span>

### <a name="getrenderedrows"></a><span data-ttu-id="202e6-288">getRenderedRows</span><span class="sxs-lookup"><span data-stu-id="202e6-288">getRenderedRows</span></span>


<span data-ttu-id="202e6-289">getRenderedRows(): [Row](view-model-control-list-ilist-irow.md) [ ]</span><span class="sxs-lookup"><span data-stu-id="202e6-289">getRenderedRows(): [Row](view-model-control-list-ilist-irow.md) [ ]</span></span>



#### <a name="returns-rowview-model-control-list-ilist-irowmd--"></a><span data-ttu-id="202e6-290">[Row](view-model-control-list-ilist-irow.md) [ ] を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-290">Returns [Row](view-model-control-list-ilist-irow.md) [ ]</span></span>

### <a name="getrownavigation"></a><span data-ttu-id="202e6-291">getRowNavigation</span><span class="sxs-lookup"><span data-stu-id="202e6-291">getRowNavigation</span></span>


<span data-ttu-id="202e6-292">getRowNavigation(row: [Row](view-model-control-list-ilist-irow.md)): Promise &lt;any&gt; &#124; any</span><span class="sxs-lookup"><span data-stu-id="202e6-292">getRowNavigation(row: [Row](view-model-control-list-ilist-irow.md)): Promise &lt;any&gt; &#124; any</span></span>




#### <a name="parameters"></a><span data-ttu-id="202e6-293">パラメーター</span><span class="sxs-lookup"><span data-stu-id="202e6-293">Parameters</span></span>

| <span data-ttu-id="202e6-294">氏名</span><span class="sxs-lookup"><span data-stu-id="202e6-294">Name</span></span> | <span data-ttu-id="202e6-295">種類</span><span class="sxs-lookup"><span data-stu-id="202e6-295">Type</span></span> | <span data-ttu-id="202e6-296">説明</span><span class="sxs-lookup"><span data-stu-id="202e6-296">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="202e6-297">行</span><span class="sxs-lookup"><span data-stu-id="202e6-297">row</span></span>|[<span data-ttu-id="202e6-298">Row</span><span class="sxs-lookup"><span data-stu-id="202e6-298">Row</span></span>](view-model-control-list-ilist-irow.md)||

#### <a name="returns-promise-ltanygt-124-any"></a><span data-ttu-id="202e6-299">Promise &lt;any&gt; &#124; any を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-299">Returns Promise &lt;any&gt; &#124; any</span></span>

### <a name="getrowselectioncount"></a><span data-ttu-id="202e6-300">getRowSelectionCount</span><span class="sxs-lookup"><span data-stu-id="202e6-300">getRowSelectionCount</span></span>


<span data-ttu-id="202e6-301">getRowSelectionCount(): number</span><span class="sxs-lookup"><span data-stu-id="202e6-301">getRowSelectionCount(): number</span></span>



#### <a name="returns-number"></a><span data-ttu-id="202e6-302">number を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-302">Returns number</span></span>

### <a name="getrowselections"></a><span data-ttu-id="202e6-303">getRowSelections</span><span class="sxs-lookup"><span data-stu-id="202e6-303">getRowSelections</span></span>


<span data-ttu-id="202e6-304">getRowSelections(): string [ ]</span><span class="sxs-lookup"><span data-stu-id="202e6-304">getRowSelections(): string [ ]</span></span>



#### <a name="returns-string--"></a><span data-ttu-id="202e6-305">string [ ] を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-305">Returns string [ ]</span></span>

### <a name="getrowtracking"></a><span data-ttu-id="202e6-306">getRowTracking</span><span class="sxs-lookup"><span data-stu-id="202e6-306">getRowTracking</span></span>


<span data-ttu-id="202e6-307">getRowTracking(row: any, index: string): string</span><span class="sxs-lookup"><span data-stu-id="202e6-307">getRowTracking(row: any, index: string): string</span></span>




#### <a name="parameters"></a><span data-ttu-id="202e6-308">パラメーター</span><span class="sxs-lookup"><span data-stu-id="202e6-308">Parameters</span></span>

| <span data-ttu-id="202e6-309">氏名</span><span class="sxs-lookup"><span data-stu-id="202e6-309">Name</span></span> | <span data-ttu-id="202e6-310">種類</span><span class="sxs-lookup"><span data-stu-id="202e6-310">Type</span></span> | <span data-ttu-id="202e6-311">説明</span><span class="sxs-lookup"><span data-stu-id="202e6-311">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="202e6-312">行</span><span class="sxs-lookup"><span data-stu-id="202e6-312">row</span></span>|<span data-ttu-id="202e6-313">any</span><span class="sxs-lookup"><span data-stu-id="202e6-313">any</span></span>||
| <span data-ttu-id="202e6-314">指数</span><span class="sxs-lookup"><span data-stu-id="202e6-314">index</span></span>|<span data-ttu-id="202e6-315">string</span><span class="sxs-lookup"><span data-stu-id="202e6-315">string</span></span>||

#### <a name="returns-string"></a><span data-ttu-id="202e6-316">文字列を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-316">Returns string</span></span>

### <a name="getsearchcolumn"></a><span data-ttu-id="202e6-317">getSearchColumn</span><span class="sxs-lookup"><span data-stu-id="202e6-317">getSearchColumn</span></span>


<span data-ttu-id="202e6-318">getSearchColumn(): string</span><span class="sxs-lookup"><span data-stu-id="202e6-318">getSearchColumn(): string</span></span>



#### <a name="returns-string"></a><span data-ttu-id="202e6-319">文字列を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-319">Returns string</span></span>

### <a name="getsearchcolumnlabel"></a><span data-ttu-id="202e6-320">getSearchColumnLabel</span><span class="sxs-lookup"><span data-stu-id="202e6-320">getSearchColumnLabel</span></span>


<span data-ttu-id="202e6-321">getSearchColumnLabel(): string</span><span class="sxs-lookup"><span data-stu-id="202e6-321">getSearchColumnLabel(): string</span></span>



#### <a name="returns-string"></a><span data-ttu-id="202e6-322">文字列を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-322">Returns string</span></span>

### <a name="getsearchablecolumns"></a><span data-ttu-id="202e6-323">getSearchableColumns</span><span class="sxs-lookup"><span data-stu-id="202e6-323">getSearchableColumns</span></span>


<span data-ttu-id="202e6-324">getSearchableColumns(): any [ ]</span><span class="sxs-lookup"><span data-stu-id="202e6-324">getSearchableColumns(): any [ ]</span></span>



#### <a name="returns-any--"></a><span data-ttu-id="202e6-325">any [ ] を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-325">Returns any [ ]</span></span>

### <a name="hidesearchbar"></a><span data-ttu-id="202e6-326">hideSearchBar</span><span class="sxs-lookup"><span data-stu-id="202e6-326">hideSearchBar</span></span>


<span data-ttu-id="202e6-327">hideSearchBar(): boolean</span><span class="sxs-lookup"><span data-stu-id="202e6-327">hideSearchBar(): boolean</span></span>



#### <a name="returns-boolean"></a><span data-ttu-id="202e6-328">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-328">Returns boolean</span></span>

### <a name="iseditable"></a><span data-ttu-id="202e6-329">isEditable</span><span class="sxs-lookup"><span data-stu-id="202e6-329">isEditable</span></span>


<span data-ttu-id="202e6-330">isEditable(): boolean</span><span class="sxs-lookup"><span data-stu-id="202e6-330">isEditable(): boolean</span></span>

<span data-ttu-id="202e6-331">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="202e6-331">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="202e6-332">コントロールまたはその親が編集可能でない場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="202e6-332">Returns false when either the control or it's parent is not editable.</span></span>
<span data-ttu-id="202e6-333">コントロールとその親の両方が編集可能な場合、true を返します。</span><span class="sxs-lookup"><span data-stu-id="202e6-333">Returns true when both the control and it's parent are editable.</span></span>
<span data-ttu-id="202e6-334">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="202e6-334">Returns true when either the control or it's parent is editable and the other is undefined.</span></span>
<span data-ttu-id="202e6-335">コントロールの編集機能と親の編集機能の両方が未定義の場合は undefined を返します。</span><span class="sxs-lookup"><span data-stu-id="202e6-335">Returns undefined if both the control's edit-ability and it's parent's edit-ability is undefined.</span></span>

> <span data-ttu-id="202e6-336">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable) から継承</span><span class="sxs-lookup"><span data-stu-id="202e6-336">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[isEditable](view-model-control-basecontrol-icontrol-icontrol.md#iseditable)</span></span>

#### <a name="returns-boolean"></a><span data-ttu-id="202e6-337">ブール値を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-337">Returns boolean</span></span>



### <a name="loadmetadata"></a><span data-ttu-id="202e6-338">loadMetaData</span><span class="sxs-lookup"><span data-stu-id="202e6-338">loadMetaData</span></span>


<span data-ttu-id="202e6-339">loadMetaData(): void</span><span class="sxs-lookup"><span data-stu-id="202e6-339">loadMetaData(): void</span></span>



#### <a name="returns-void"></a><span data-ttu-id="202e6-340">void を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-340">Returns void</span></span>

### <a name="loadmore"></a><span data-ttu-id="202e6-341">loadMore</span><span class="sxs-lookup"><span data-stu-id="202e6-341">loadMore</span></span>


<span data-ttu-id="202e6-342">loadMore(): void</span><span class="sxs-lookup"><span data-stu-id="202e6-342">loadMore(): void</span></span>



#### <a name="returns-void"></a><span data-ttu-id="202e6-343">void を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-343">Returns void</span></span>

### <a name="metadata"></a><span data-ttu-id="202e6-344">metadata</span><span class="sxs-lookup"><span data-stu-id="202e6-344">metadata</span></span>


<span data-ttu-id="202e6-345">metadata(): [ListMetadata](view-model-control-list-ilist-ilistmetadata.md)</span><span class="sxs-lookup"><span data-stu-id="202e6-345">metadata(): [ListMetadata](view-model-control-list-ilist-ilistmetadata.md)</span></span>

<span data-ttu-id="202e6-346">このコントロールのメタデータ オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="202e6-346">Returns the metadata object of this control.</span></span>

> <span data-ttu-id="202e6-347">[ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[metadata](view-model-control-container-icontainercontrol-icontainercontrol.md#metadata) をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="202e6-347">Overrides [ContainerControl](view-model-control-container-icontainercontrol-icontainercontrol.md).[metadata](view-model-control-container-icontainercontrol-icontainercontrol.md#metadata)</span></span>

#### <a name="returns-listmetadataview-model-control-list-ilist-ilistmetadatamd"></a><span data-ttu-id="202e6-348">[ListMetadata](view-model-control-list-ilist-ilistmetadata.md) を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-348">Returns [ListMetadata](view-model-control-list-ilist-ilistmetadata.md)</span></span>



### <a name="parent"></a><span data-ttu-id="202e6-349">parent</span><span class="sxs-lookup"><span data-stu-id="202e6-349">parent</span></span>


<span data-ttu-id="202e6-350">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="202e6-350">parent(): [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="202e6-351">このコントロールの親 (コントロールまたはページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="202e6-351">Returns the parent (control or page) of this control.</span></span>

> <span data-ttu-id="202e6-352">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent) から継承</span><span class="sxs-lookup"><span data-stu-id="202e6-352">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[parent](view-model-control-basecontrol-icontrol-icontrol.md#parent)</span></span>

#### <a name="returns-controlview-model-control-basecontrol-icontrol-icontrolmd-124-pageview-model-ipage-ipagemd"></a><span data-ttu-id="202e6-353">[Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-353">Returns [Control](view-model-control-basecontrol-icontrol-icontrol.md) &#124; [Page](view-model-ipage-ipage.md)</span></span>



### <a name="performremotesearch"></a><span data-ttu-id="202e6-354">performRemoteSearch</span><span class="sxs-lookup"><span data-stu-id="202e6-354">performRemoteSearch</span></span>


<span data-ttu-id="202e6-355">performRemoteSearch(): void</span><span class="sxs-lookup"><span data-stu-id="202e6-355">performRemoteSearch(): void</span></span>



#### <a name="returns-void"></a><span data-ttu-id="202e6-356">void を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-356">Returns void</span></span>

### <a name="root"></a><span data-ttu-id="202e6-357">root</span><span class="sxs-lookup"><span data-stu-id="202e6-357">root</span></span>


<span data-ttu-id="202e6-358">root(): [Page](view-model-ipage-ipage.md)</span><span class="sxs-lookup"><span data-stu-id="202e6-358">root(): [Page](view-model-ipage-ipage.md)</span></span>

<span data-ttu-id="202e6-359">このコントロールのルート フォーム インスタンス (ページ) を返します。</span><span class="sxs-lookup"><span data-stu-id="202e6-359">Returns the root form instance (page) of this control.</span></span>

> <span data-ttu-id="202e6-360">[Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root) から継承</span><span class="sxs-lookup"><span data-stu-id="202e6-360">Inherited from [Control](view-model-control-basecontrol-icontrol-icontrol.md).[root](view-model-control-basecontrol-icontrol-icontrol.md#root)</span></span>

#### <a name="returns-pageview-model-ipage-ipagemd"></a><span data-ttu-id="202e6-361">[Page](view-model-ipage-ipage.md) を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-361">Returns [Page](view-model-ipage-ipage.md)</span></span>



### <a name="selectsearchcolumn"></a><span data-ttu-id="202e6-362">selectSearchColumn</span><span class="sxs-lookup"><span data-stu-id="202e6-362">selectSearchColumn</span></span>


<span data-ttu-id="202e6-363">selectSearchColumn(column: string): void</span><span class="sxs-lookup"><span data-stu-id="202e6-363">selectSearchColumn(column: string): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="202e6-364">パラメーター</span><span class="sxs-lookup"><span data-stu-id="202e6-364">Parameters</span></span>

| <span data-ttu-id="202e6-365">氏名</span><span class="sxs-lookup"><span data-stu-id="202e6-365">Name</span></span> | <span data-ttu-id="202e6-366">種類</span><span class="sxs-lookup"><span data-stu-id="202e6-366">Type</span></span> | <span data-ttu-id="202e6-367">説明</span><span class="sxs-lookup"><span data-stu-id="202e6-367">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="202e6-368">column</span><span class="sxs-lookup"><span data-stu-id="202e6-368">column</span></span>|<span data-ttu-id="202e6-369">string</span><span class="sxs-lookup"><span data-stu-id="202e6-369">string</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="202e6-370">void を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-370">Returns void</span></span>

### <a name="setrowsections"></a><span data-ttu-id="202e6-371">setRowSections</span><span class="sxs-lookup"><span data-stu-id="202e6-371">setRowSections</span></span>


<span data-ttu-id="202e6-372">setRowSections(selections: string [ ]): void</span><span class="sxs-lookup"><span data-stu-id="202e6-372">setRowSections(selections: string [ ]): void</span></span>




#### <a name="parameters"></a><span data-ttu-id="202e6-373">パラメーター</span><span class="sxs-lookup"><span data-stu-id="202e6-373">Parameters</span></span>

| <span data-ttu-id="202e6-374">氏名</span><span class="sxs-lookup"><span data-stu-id="202e6-374">Name</span></span> | <span data-ttu-id="202e6-375">種類</span><span class="sxs-lookup"><span data-stu-id="202e6-375">Type</span></span> | <span data-ttu-id="202e6-376">説明</span><span class="sxs-lookup"><span data-stu-id="202e6-376">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="202e6-377">選択内容</span><span class="sxs-lookup"><span data-stu-id="202e6-377">selections</span></span>|<span data-ttu-id="202e6-378">string [ ]</span><span class="sxs-lookup"><span data-stu-id="202e6-378">string [ ]</span></span>||

#### <a name="returns-void"></a><span data-ttu-id="202e6-379">void を返します</span><span class="sxs-lookup"><span data-stu-id="202e6-379">Returns void</span></span>

## <a name="events"></a><span data-ttu-id="202e6-380">イベント</span><span class="sxs-lookup"><span data-stu-id="202e6-380">Events</span></span>

### <a name="onrowcreate"></a><span data-ttu-id="202e6-381">onRowCreate</span><span class="sxs-lookup"><span data-stu-id="202e6-381">onRowCreate</span></span>

<span data-ttu-id="202e6-382">onRowCreate: [EventHook](event-ievent-ieventhook.md) &lt;[Row](view-model-control-list-ilist-irow.md)&gt;</span><span class="sxs-lookup"><span data-stu-id="202e6-382">onRowCreate: [EventHook](event-ievent-ieventhook.md) &lt;[Row](view-model-control-list-ilist-irow.md)&gt;</span></span>




### <a name="onrowselect"></a><span data-ttu-id="202e6-383">onRowSelect</span><span class="sxs-lookup"><span data-stu-id="202e6-383">onRowSelect</span></span>

<span data-ttu-id="202e6-384">onRowSelect: [EventHook](event-ievent-ieventhook.md) &lt;[Row](view-model-control-list-ilist-irow.md)&gt;</span><span class="sxs-lookup"><span data-stu-id="202e6-384">onRowSelect: [EventHook](event-ievent-ieventhook.md) &lt;[Row](view-model-control-list-ilist-irow.md)&gt;</span></span>




