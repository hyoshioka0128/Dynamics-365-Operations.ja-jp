---
title: "Visual Studio でのメタデータの検索"
description: "この記事では、メタデータ検索を使用して、任意のパターンやコンテンツのコードとメタデータを検索する方法について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 83303
ms.assetid: 4d686948-a78d-48fa-bbf8-28da7880eec7
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 05e4f558cb72c3fca162ce0c0a6325e5905a3cc5
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="metadata-search-in-visual-studio"></a><span data-ttu-id="9a349-103">Visual Studio でのメタデータの検索</span><span class="sxs-lookup"><span data-stu-id="9a349-103">Metadata search in Visual Studio</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a349-104">この記事では、メタデータ検索を使用して、任意のパターンやコンテンツのコードとメタデータを検索する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9a349-104">This article describes how to use metadata search to search your code and metadata for arbitrary patterns and content.</span></span> 

<span data-ttu-id="9a349-105">大量のコード ベースおよびメタデータを考えると、多くの場合特定の基準を満たすコード内のものを検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a349-105">Given the large volume of the code base and metadata, it is often necessary to find things in the code that meet a certain criteria.</span></span> <span data-ttu-id="9a349-106">パターンを含んでいるまたは基準を満たしているメタデータ要素の名前が分からない場合がよくあります。</span><span class="sxs-lookup"><span data-stu-id="9a349-106">Often times you may not know the name of the metadata element that contains the pattern or meets the criteria.</span></span> <span data-ttu-id="9a349-107">メタデータ検索は、メタデータ検索ツール ウィンドウと移動先ウィンドウの 2 つのユーザー インターフェイスを通じて Visual Studio で公開されます。</span><span class="sxs-lookup"><span data-stu-id="9a349-107">Metadata search is exposed in Visual Studio through two user interfaces: the Metadata Search tool window and the Navigate To window.</span></span>

## <a name="metadata-search-tool-window"></a><span data-ttu-id="9a349-108">メタデータ検索ツール ウィンドウ</span><span class="sxs-lookup"><span data-stu-id="9a349-108">Metadata search tool window</span></span>
<span data-ttu-id="9a349-109">メタデータ検索ツール ウィンドウには **Dynamics 365 &gt; メタデータ検索** メニュー コマンドからアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="9a349-109">You can access the Metadata search tool window from the **Dynamics 365 &gt; Metadata Search** menu command.</span></span> <span data-ttu-id="9a349-110">検索クエリを入力して検索を開始します。</span><span class="sxs-lookup"><span data-stu-id="9a349-110">Enter your search query to start the search.</span></span> <span data-ttu-id="9a349-111">結果は、入力と同時にウィンドウへの入力が非同期で開始されます。</span><span class="sxs-lookup"><span data-stu-id="9a349-111">Results will start populating in the window asynchronously as you type.</span></span> <span data-ttu-id="9a349-112">任意の結果行をダブルクリックして、検索クエリに一致する、対応する X++ コードまたはメタデータに移動することができます。</span><span class="sxs-lookup"><span data-stu-id="9a349-112">You can double-click any result line to navigate to the corresponding X++ code or metadata that matches your search query.</span></span>   

<span data-ttu-id="9a349-113">[![Posted\_MetaSearch](./media/posted_metasearch.png)](./media/posted_metasearch.png)</span><span class="sxs-lookup"><span data-stu-id="9a349-113">[![Posted\_MetaSearch](./media/posted_metasearch.png)](./media/posted_metasearch.png)</span></span> 

<span data-ttu-id="9a349-114">また、1 つまたは複数の結果を選択して、右クリックし、これらの要素をプロジェクトに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="9a349-114">You can also select one or more results, right-click, and then add these elements to a project.</span></span> <span data-ttu-id="9a349-115">検索結果とやりとりを開始するまで、検索の完了を待機する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9a349-115">You don’t need to wait for the search to complete before you start interacting with the search results.</span></span> 

<span data-ttu-id="9a349-116">[![AddNewProject\_MetaSearch](./media/addnewproject_metasearch.png)](./media/addnewproject_metasearch.png)</span><span class="sxs-lookup"><span data-stu-id="9a349-116">[![AddNewProject\_MetaSearch](./media/addnewproject_metasearch.png)](./media/addnewproject_metasearch.png)</span></span>

## <a name="navigate-to-window"></a><span data-ttu-id="9a349-117">ウィンドウへの移動</span><span class="sxs-lookup"><span data-stu-id="9a349-117">Navigate To window</span></span>
<span data-ttu-id="9a349-118">**移動先** ウィンドウは、**Ctrl + ','** (コンマ区切り記号) ショートカット キーを使用して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9a349-118">The **Navigate To** window is invoked using the **Ctrl+‘,’** (the comma character) shortcut keys.</span></span> <span data-ttu-id="9a349-119">**Ctrl+","** キーを押すと、Visual Studio の主要なドキュメント ウィンドウの右上隅にクエリ エントリ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a349-119">Pressing **Ctrl+‘,’** displays the query entry box in top right corner of the Visual Studio main document window.</span></span> <span data-ttu-id="9a349-120">また、Visual Studio の **編集** メニューから **移動先** ウィンドウにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="9a349-120">You can also access the **Navigate To** window from the Visual Studio **Edit** menu.</span></span> <span data-ttu-id="9a349-121">クエリを検索し、入力時に結果が表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a349-121">Enter you search query and see the results appear as you type.</span></span> <span data-ttu-id="9a349-122">検索が完了したら、進行状況インジケーターが停止します。</span><span class="sxs-lookup"><span data-stu-id="9a349-122">A progress indicator will stop when the search is complete.</span></span> <span data-ttu-id="9a349-123">結果とやりとりを開始するために、検索の完了を待機する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9a349-123">You don’t need to wait for the search to complete to start interacting with the results.</span></span> 

<span data-ttu-id="9a349-124">[![TypeForm\_MetaSearch](./media/typeform_metasearch.png)](./media/typeform_metasearch.png)</span><span class="sxs-lookup"><span data-stu-id="9a349-124">[![TypeForm\_MetaSearch](./media/typeform_metasearch.png)](./media/typeform_metasearch.png)</span></span>

## <a name="search-query-syntax"></a><span data-ttu-id="9a349-125">クエリ構文を検索</span><span class="sxs-lookup"><span data-stu-id="9a349-125">Search query syntax</span></span>
<span data-ttu-id="9a349-126">ここでは、検索クエリの構文について説明し、クエリの例を示します。</span><span class="sxs-lookup"><span data-stu-id="9a349-126">This section describes the search query syntax and provides example queries.</span></span>

### <a name="syntax"></a><span data-ttu-id="9a349-127">構文</span><span class="sxs-lookup"><span data-stu-id="9a349-127">Syntax</span></span>

<span data-ttu-id="9a349-128">検索クエリは、この一般的な形式の一連のフィルターで構成される検索文字列です。*&lt;filter\_1&gt;:&lt;filter\_1\_value&gt; \[&lt;filter\_2&gt;:&lt;filter\_2\_value&gt;… \[ &lt;filter\_N&gt;:&lt;filter\_N\_value&gt;\]\]*、ここで *&lt;filter\_i&gt;* は許容されるフィルター名の 1 つで、*&lt;filter\_i\_value&gt;* はカンマ区切り (クォーテーションの場合もあり) のフィルタリング値です。</span><span class="sxs-lookup"><span data-stu-id="9a349-128">The search query is a search string that consists of a set of filters in this general form: *&lt;filter\_1&gt;:&lt;filter\_1\_value&gt; \[&lt;filter\_2&gt;:&lt;filter\_2\_value&gt;… \[ &lt;filter\_N&gt;:&lt;filter\_N\_value&gt;\]\]* Where *&lt;filter\_i&gt;* is one of the acceptable filter names, and *&lt;filter\_i\_value&gt;* are comma separated (and possibly quoted) filtering values.</span></span>

### <a name="filter-names"></a><span data-ttu-id="9a349-129">フィルター名</span><span class="sxs-lookup"><span data-stu-id="9a349-129">Filter names</span></span>

-   <span data-ttu-id="9a349-130">**名前**: 要素名ごとのフィルター処理。</span><span class="sxs-lookup"><span data-stu-id="9a349-130">**Name**: Filter by element name.</span></span> <span data-ttu-id="9a349-131">これは既定のフィルターです。つまり、フィルター値を入力するだけで要素名とみなされます。</span><span class="sxs-lookup"><span data-stu-id="9a349-131">This is the default filter, meaning if you just type a filter value, it is assumed to be an element name.</span></span> <span data-ttu-id="9a349-132">各コンマ区切り値は、許容可能な要素名です。</span><span class="sxs-lookup"><span data-stu-id="9a349-132">Each comma-separated value is an acceptable element name.</span></span>
-   <span data-ttu-id="9a349-133">**タイプ**: 要素タイプでフィルター処理してください。</span><span class="sxs-lookup"><span data-stu-id="9a349-133">**Type**: Filter by element type.</span></span> <span data-ttu-id="9a349-134">各コンマ区切り値は、要素またはサブ要素タイプ (ルート タイプまたはサブタイプ) (テーブル、クラス、フィールドなど) にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a349-134">Each comma-separated value should be the name of an element or sub-element type (root type or subtype) (i.e. table, class, field).</span></span> <span data-ttu-id="9a349-135">フィルター処理のロジックは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9a349-135">Logic of filtering is:</span></span>

<!-- -->

-   <span data-ttu-id="9a349-136">**(roottype\_1 OR roottype\_2 OR … OR roottype\_N) および (subtype\_1 OR subtype\_2 OR … OR subtype\_N)**</span><span class="sxs-lookup"><span data-stu-id="9a349-136">**(roottype\_1 OR roottype\_2 OR … OR roottype\_N) AND (subtype\_1 OR subtype\_2 OR … OR subtype\_N)**</span></span>



-   <span data-ttu-id="9a349-137">**モデル**: モデル名ごとのフィルター。</span><span class="sxs-lookup"><span data-stu-id="9a349-137">**Model**: Filter by model name.</span></span> <span data-ttu-id="9a349-138">各コンマ区切り値は、アプリケーションのモデル名にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a349-138">Each comma-separated value should be the name of a model in your application.</span></span>
-   <span data-ttu-id="9a349-139">**プロパティ**: プロパティ フィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="9a349-139">**Property**: Apply property filters.</span></span> <span data-ttu-id="9a349-140">各コンマ区切り値は、フォームの *property\_name=property\_value* にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a349-140">Each comma-separated value should be in the form *property\_name=property\_value*</span></span>
-   <span data-ttu-id="9a349-141">**コード**: コード スニペットを使用してフィルタ処理し、コード スニペットを引用符で囲みます。</span><span class="sxs-lookup"><span data-stu-id="9a349-141">**Code**: Filter using code snippets, use quotes around code snippets.</span></span> <span data-ttu-id="9a349-142">一致するソース コードは、指定されたコード スニペットを含む要素です。</span><span class="sxs-lookup"><span data-stu-id="9a349-142">The matching source code is the elements that contain the specified code snippet.</span></span>

<span data-ttu-id="9a349-143">検索ボックスで使用可能なドロップダウンリスト メニューを開いて、フィルターおよびフィルター構文の使用に関するヘルプを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="9a349-143">You can get help about using filter and filter syntax by opening the drop-down menu available in the search box.!</span></span>

[<span data-ttu-id="9a349-144">metadatasearchfilter</span><span class="sxs-lookup"><span data-stu-id="9a349-144">metadatasearchfilter</span></span>](./media/metadatasearchfilter.jpg)

## <a name="examples"></a><span data-ttu-id="9a349-145">例</span><span class="sxs-lookup"><span data-stu-id="9a349-145">Examples</span></span>

|                               <span data-ttu-id="9a349-146"><strong>クエリ文字列</strong></span><span class="sxs-lookup"><span data-stu-id="9a349-146"><strong>Query string</strong></span></span>                               |                                                        <span data-ttu-id="9a349-147"><strong>目的</strong></span><span class="sxs-lookup"><span data-stu-id="9a349-147"><strong>What it does</strong></span></span>                                                         |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
|                                        <span data-ttu-id="9a349-148">TrvExpTable</span><span class="sxs-lookup"><span data-stu-id="9a349-148">TrvExpTable</span></span>                                        | <span data-ttu-id="9a349-149">トークンが単独である場合は、それは名前と見なされます。</span><span class="sxs-lookup"><span data-stu-id="9a349-149">If the token is by itself, it is assumed to be the name.</span></span> <span data-ttu-id="9a349-150">したがって、名前に 'TrvExpTable' を持つアプリケーションのすべてのものが検出されます。</span><span class="sxs-lookup"><span data-stu-id="9a349-150">So this will find everything in the application that has ‘TrvExpTable’ in the name.</span></span> |
|                                     <span data-ttu-id="9a349-151">type:form ccount</span><span class="sxs-lookup"><span data-stu-id="9a349-151">type:form ccount</span></span>                                      |                                              <span data-ttu-id="9a349-152">その名前の「アカウント」を持つすべてのフォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="9a349-152">Finds all forms that have ‘ccount’ in their names.</span></span>                                              |
|                         <span data-ttu-id="9a349-153">type:form property:formtemplate=listpage</span><span class="sxs-lookup"><span data-stu-id="9a349-153">type:form property:formtemplate=listpage</span></span>                          |                                <span data-ttu-id="9a349-154">「ListPage」に等しい「FormTemplate」のプロパティを含む、すべてのフォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="9a349-154">Finds all forms that contain the property ‘FormTemplate’ equal to ‘ListPage’.</span></span>                                 |
|              <span data-ttu-id="9a349-155">type:table,formDesign property:"WorkflowDataSource=TrvExpTable"</span><span class="sxs-lookup"><span data-stu-id="9a349-155">type:table,formDesign property:"WorkflowDataSource=TrvExpTable"</span></span>              |                                         <span data-ttu-id="9a349-156">テーブルの下で formDesign ノードを検索しますが、何も見つかりません。</span><span class="sxs-lookup"><span data-stu-id="9a349-156">Finds formDesign nodes under tables, nothing would be found.</span></span>                                         |
|             <span data-ttu-id="9a349-157">type:form,formmenufunctionbuttoncontrol property:Text=@SYS311998</span><span class="sxs-lookup"><span data-stu-id="9a349-157">type:form,formmenufunctionbuttoncontrol property:Text=@SYS311998</span></span>              |                       <span data-ttu-id="9a349-158">(ラベル) 「@SYS311998」に等しいテキスト プロパティを含むすべてのメニュー機能ボタン コントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="9a349-158">Finds all menu function button controls with the Text property equal to (a label) ‘@SYS311998’.</span></span>                        |
|                               <span data-ttu-id="9a349-159">type:table,method name:insert</span><span class="sxs-lookup"><span data-stu-id="9a349-159">type:table,method name:insert</span></span>                               |                                      <span data-ttu-id="9a349-160">メソッドの名前に「挿入」を含むメソッドで、テーブルを検索します。</span><span class="sxs-lookup"><span data-stu-id="9a349-160">Finds tables with a method containing ‘insert’ in the method name.</span></span>                                      |
|                             <span data-ttu-id="9a349-161">type:table,tableindex name:Export</span><span class="sxs-lookup"><span data-stu-id="9a349-161">type:table,tableindex name:Export</span></span>                             |                                        <span data-ttu-id="9a349-162">「エクスポート」の単語を含むインデックス名で、テーブルを検索します。</span><span class="sxs-lookup"><span data-stu-id="9a349-162">Finds tables with an index name containing the word ‘Export.’</span></span>                                         |
|                           <span data-ttu-id="9a349-163">type:table,tableindexfield name:xpNum</span><span class="sxs-lookup"><span data-stu-id="9a349-163">type:table,tableindexfield name:xpNum</span></span>                           |                                          <span data-ttu-id="9a349-164">インデックス フィールド名の「xpNum」で、テーブル インデックスを検索します。</span><span class="sxs-lookup"><span data-stu-id="9a349-164">Finds table indexes with ‘xpNum’ in the index field name.</span></span>                                           |
|                           <span data-ttu-id="9a349-165">type:table,tablefieldgroup name:EPNew</span><span class="sxs-lookup"><span data-stu-id="9a349-165">type:table,tablefieldgroup name:EPNew</span></span>                           |                                       <span data-ttu-id="9a349-166">その名前内で「EPNew」を含む FieldGroups (テーブル内) を検索します。</span><span class="sxs-lookup"><span data-stu-id="9a349-166">Finds FieldGroups (in tables) containing ‘EPNew’ in their names.</span></span>                                       |
|             <span data-ttu-id="9a349-167">type:form,formgridcontrol property:allowedit=no,heightmode=column</span><span class="sxs-lookup"><span data-stu-id="9a349-167">type:form,formgridcontrol property:allowedit=no,heightmode=column</span></span>             |                     <span data-ttu-id="9a349-168">「いいえ」に等しい allowedit のプロパティおよび「列」に等しい heightmode を持つ、グリッド コントロールのフォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="9a349-168">Finds form grid controls, with properties allowedit equal to ‘no’ and heightmode equal to ‘column’.</span></span>                      |
| <span data-ttu-id="9a349-169">type:form,formtabcontrol property:arrangeMethod=Vertical,ViewEditMode=view,WidthMode=Auto</span><span class="sxs-lookup"><span data-stu-id="9a349-169">type:form,formtabcontrol property:arrangeMethod=Vertical,ViewEditMode=view,WidthMode=Auto</span></span> |  <span data-ttu-id="9a349-170">「垂直」に等しい arrangeMethod、「ビュー」に等しい ViewEditMode および「自動」に等しい WidthMode のプロパティを持つ、タブ コントロールのフォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="9a349-170">Finds form tab controls, with properties arrangeMethod equal to ’Vertical’ and ViewEditMode equal to ‘view’ and WidthMode equal to ‘Auto.'</span></span>  |
|              <span data-ttu-id="9a349-171">type:form,formDesign property:"WorkflowDataSource=TrvExpTable"</span><span class="sxs-lookup"><span data-stu-id="9a349-171">type:form,formDesign property:"WorkflowDataSource=TrvExpTable"</span></span>               |                <span data-ttu-id="9a349-172">「TrvExpTable」の値に設定する FormDesign ノードで「WorkflowDataSource」プロパティを持つ、すべてのフォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="9a349-172">Finds all forms with the 'WorkflowDataSource" property in the FormDesign node set to the value "TrvExpTable."</span></span>                 |
|         <span data-ttu-id="9a349-173">model:”Application Suite” type:formdesign property:style=simplelistdetail</span><span class="sxs-lookup"><span data-stu-id="9a349-173">model:”Application Suite” type:formdesign property:style=simplelistdetail</span></span>         |            <span data-ttu-id="9a349-174">FormDesign ノードで simpleListDetail に設定するスタイル プロパティを持つ、アプリケーション スイート モデル内のすべてのフォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="9a349-174">Find all forms in Application Suite model that has the style property set to simpleListDetail in the FormDesign node.</span></span>             |
|                                    <span data-ttu-id="9a349-175">code:”return null”</span><span class="sxs-lookup"><span data-stu-id="9a349-175">code:”return null”</span></span>                                     |                                       <span data-ttu-id="9a349-176">「Null を返す」を含むソース コード内で、すべての場所を検索します。</span><span class="sxs-lookup"><span data-stu-id="9a349-176">Finds all places in the source code that contains “return null”.</span></span>                                       |
|                              <span data-ttu-id="9a349-177">code:"element.lock()" type:form</span><span class="sxs-lookup"><span data-stu-id="9a349-177">code:"element.lock()" type:form</span></span>                              |                             <span data-ttu-id="9a349-178">スニペット 「element.lock()」を含むソース コードのフォームで、すべての場所を検索します。</span><span class="sxs-lookup"><span data-stu-id="9a349-178">Finds all places in the forms source code that contain the snippet ‘element.lock()’.</span></span>                             |
|                               <span data-ttu-id="9a349-179">code:"insert" type:table,form</span><span class="sxs-lookup"><span data-stu-id="9a349-179">code:"insert" type:table,form</span></span>                               |                             <span data-ttu-id="9a349-180">「挿入」を含むフォームまたはテーブルのいずれかのソース コード内で、すべての場所を検索します。</span><span class="sxs-lookup"><span data-stu-id="9a349-180">Finds all places in the source code of either forms or tables that contain ‘insert’.</span></span>                             |
|                          <span data-ttu-id="9a349-181">code:"public display" type:form,method</span><span class="sxs-lookup"><span data-stu-id="9a349-181">code:"public display" type:form,method</span></span>                           |                                        <span data-ttu-id="9a349-182">「公開表示」のコードを含む、すべてのフォーム メソッドを検索します。</span><span class="sxs-lookup"><span data-stu-id="9a349-182">Finds all form methods that contain the code ‘public display’.</span></span>                                        |
|                           <span data-ttu-id="9a349-183">type:formbuttoncontrol property:text=</span><span class="sxs-lookup"><span data-stu-id="9a349-183">type:formbuttoncontrol property:text=</span></span>                           |                               <span data-ttu-id="9a349-184"><strong>空</strong>テキスト プロパティを持つ、すべてのフォームのボタン コントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="9a349-184">Finds all form Button Controls that have <strong>empty</strong> text properties.</span></span>                               |

