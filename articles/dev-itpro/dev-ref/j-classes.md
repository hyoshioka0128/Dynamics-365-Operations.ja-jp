---
title: "J クラス"
description: "文字 J で始まるシステム API クラス。"
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
ms.custom: 58702
ms.assetid: e932e25e-b72a-428a-830a-20160e81e334
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f2d5274d69ebd39821d5647dae6bb6c70a0ce2b9
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="j-classes"></a><span data-ttu-id="959bc-103">J クラス</span><span class="sxs-lookup"><span data-stu-id="959bc-103">J Classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="959bc-104">文字 J で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="959bc-104">System API classes that start with the letter J.</span></span>

<a name="class-job"></a><span data-ttu-id="959bc-105">クラス ジョブ</span><span class="sxs-lookup"><span data-stu-id="959bc-105">Class Job</span></span>
---------

    class Job extends TreeNode

<span data-ttu-id="959bc-106">Job クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="959bc-106">The Job class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="959bc-107">備考</span><span class="sxs-lookup"><span data-stu-id="959bc-107">Remarks</span></span>

<span data-ttu-id="959bc-108">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="959bc-108">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="959bc-109">例</span><span class="sxs-lookup"><span data-stu-id="959bc-109">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="959bc-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="959bc-110">Methods</span></span>

| <span data-ttu-id="959bc-111">方法</span><span class="sxs-lookup"><span data-stu-id="959bc-111">Method</span></span>                                                     | <span data-ttu-id="959bc-112">説明</span><span class="sxs-lookup"><span data-stu-id="959bc-112">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="959bc-113">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="959bc-113">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="959bc-114">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="959bc-114">Returns the source code of this node.</span></span>                                                                                                         |
| <span data-ttu-id="959bc-115">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="959bc-115">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="959bc-116">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="959bc-116">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="959bc-117">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="959bc-117">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="959bc-118">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="959bc-118">Gets or sets the date that an application object was last changed.</span></span>                                                                            |
| <span data-ttu-id="959bc-119">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="959bc-119">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="959bc-120">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="959bc-120">Gets or sets the time that an application object was last changed.</span></span>                                                                            |
| <span data-ttu-id="959bc-121">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="959bc-121">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="959bc-122">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="959bc-122">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="959bc-123">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="959bc-123">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="959bc-124">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="959bc-124">Gets or sets the date that an application object was created.</span></span>                                                                                 |
| <span data-ttu-id="959bc-125">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="959bc-125">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                               |
| <span data-ttu-id="959bc-126">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="959bc-126">public str name(\[str value\])</span></span>                             | <span data-ttu-id="959bc-127">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="959bc-127">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="959bc-128">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="959bc-128">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                               |
| <span data-ttu-id="959bc-129">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="959bc-129">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="959bc-130">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="959bc-130">Sets the source code of this node.</span></span>                                                                                                            |
| <span data-ttu-id="959bc-131">public void AOTrun()</span><span class="sxs-lookup"><span data-stu-id="959bc-131">public void AOTrun()</span></span>                                       | <span data-ttu-id="959bc-132">Finance and Operations アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="959bc-132">Compiles this node and its subtree in the Finance and Operations Application Object Tree (AOT).</span></span>                                                |
| <span data-ttu-id="959bc-133">public void AOTedit(\[int Line\], \[int Column\])</span><span class="sxs-lookup"><span data-stu-id="959bc-133">public void AOTedit(\[int Line\], \[int Column\])</span></span>          | <span data-ttu-id="959bc-134">このノードの適切なエディタを開きます。</span><span class="sxs-lookup"><span data-stu-id="959bc-134">Opens the appropriate editor for this node.</span></span>                                                                                                   |

### <a name="method-aotgetsource"></a><span data-ttu-id="959bc-135">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="959bc-135">Method AOTgetSource</span></span>

<span data-ttu-id="959bc-136">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="959bc-136">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="959bc-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="959bc-137">Return Value</span></span>

<span data-ttu-id="959bc-138">ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="959bc-138">A string that contains the source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="959bc-139">備考</span><span class="sxs-lookup"><span data-stu-id="959bc-139">Remarks</span></span>

<span data-ttu-id="959bc-140">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="959bc-140">This function is overridden by nodes that have source code.</span></span>

### <a name="method-changedby"></a><span data-ttu-id="959bc-141">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="959bc-141">Method changedBy</span></span>

<span data-ttu-id="959bc-142">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="959bc-142">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="959bc-143">パラメーター</span><span class="sxs-lookup"><span data-stu-id="959bc-143">Parameters</span></span>

<span data-ttu-id="959bc-144">値</span><span class="sxs-lookup"><span data-stu-id="959bc-144">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="959bc-145">戻り値</span><span class="sxs-lookup"><span data-stu-id="959bc-145">Return Value</span></span>

<span data-ttu-id="959bc-146">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="959bc-146">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="959bc-147">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="959bc-147">Method changedDate</span></span>

<span data-ttu-id="959bc-148">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="959bc-148">Gets or sets the date that an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="959bc-149">パラメーター</span><span class="sxs-lookup"><span data-stu-id="959bc-149">Parameters</span></span>

<span data-ttu-id="959bc-150">値</span><span class="sxs-lookup"><span data-stu-id="959bc-150">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="959bc-151">戻り値</span><span class="sxs-lookup"><span data-stu-id="959bc-151">Return Value</span></span>

<span data-ttu-id="959bc-152">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="959bc-152">The date that an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="959bc-153">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="959bc-153">Method changedTime</span></span>

<span data-ttu-id="959bc-154">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="959bc-154">Gets or sets the time that an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="959bc-155">パラメーター</span><span class="sxs-lookup"><span data-stu-id="959bc-155">Parameters</span></span>

<span data-ttu-id="959bc-156">値</span><span class="sxs-lookup"><span data-stu-id="959bc-156">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="959bc-157">戻り値</span><span class="sxs-lookup"><span data-stu-id="959bc-157">Return Value</span></span>

<span data-ttu-id="959bc-158">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="959bc-158">The time that an application object was last changed.</span></span>

### <a name="method-createdby"></a><span data-ttu-id="959bc-159">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="959bc-159">Method createdBy</span></span>

<span data-ttu-id="959bc-160">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="959bc-160">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="959bc-161">パラメーター</span><span class="sxs-lookup"><span data-stu-id="959bc-161">Parameters</span></span>

<span data-ttu-id="959bc-162">値</span><span class="sxs-lookup"><span data-stu-id="959bc-162">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="959bc-163">戻り値</span><span class="sxs-lookup"><span data-stu-id="959bc-163">Return Value</span></span>

<span data-ttu-id="959bc-164">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="959bc-164">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="959bc-165">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="959bc-165">Method creationDate</span></span>

<span data-ttu-id="959bc-166">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="959bc-166">Gets or sets the date that an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="959bc-167">パラメーター</span><span class="sxs-lookup"><span data-stu-id="959bc-167">Parameters</span></span>

<span data-ttu-id="959bc-168">値</span><span class="sxs-lookup"><span data-stu-id="959bc-168">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="959bc-169">戻り値</span><span class="sxs-lookup"><span data-stu-id="959bc-169">Return Value</span></span>

<span data-ttu-id="959bc-170">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="959bc-170">The date that an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="959bc-171">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="959bc-171">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="959bc-172">パラメーター</span><span class="sxs-lookup"><span data-stu-id="959bc-172">Parameters</span></span>

<span data-ttu-id="959bc-173">値</span><span class="sxs-lookup"><span data-stu-id="959bc-173">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="959bc-174">戻り値</span><span class="sxs-lookup"><span data-stu-id="959bc-174">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="959bc-175">メソッド名</span><span class="sxs-lookup"><span data-stu-id="959bc-175">Method name</span></span>

<span data-ttu-id="959bc-176">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="959bc-176">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="959bc-177">パラメーター</span><span class="sxs-lookup"><span data-stu-id="959bc-177">Parameters</span></span>

<span data-ttu-id="959bc-178">値</span><span class="sxs-lookup"><span data-stu-id="959bc-178">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="959bc-179">戻り値</span><span class="sxs-lookup"><span data-stu-id="959bc-179">Return Value</span></span>

<span data-ttu-id="959bc-180">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="959bc-180">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="959bc-181">備考</span><span class="sxs-lookup"><span data-stu-id="959bc-181">Remarks</span></span>

<span data-ttu-id="959bc-182">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="959bc-182">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="959bc-183">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="959bc-183">Begins with a letter.</span></span>
-   <span data-ttu-id="959bc-184">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="959bc-184">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="959bc-185">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="959bc-185">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="959bc-186">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="959bc-186">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="959bc-187">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="959bc-187">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-origin"></a><span data-ttu-id="959bc-188">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="959bc-188">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="959bc-189">パラメーター</span><span class="sxs-lookup"><span data-stu-id="959bc-189">Parameters</span></span>

<span data-ttu-id="959bc-190">値</span><span class="sxs-lookup"><span data-stu-id="959bc-190">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="959bc-191">戻り値</span><span class="sxs-lookup"><span data-stu-id="959bc-191">Return Value</span></span>

### <a name="method-aotsetsource"></a><span data-ttu-id="959bc-192">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="959bc-192">Method AOTsetSource</span></span>

<span data-ttu-id="959bc-193">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="959bc-193">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="959bc-194">パラメーター</span><span class="sxs-lookup"><span data-stu-id="959bc-194">Parameters</span></span>

<span data-ttu-id="959bc-195">ソース</span><span class="sxs-lookup"><span data-stu-id="959bc-195">source</span></span>  
<span data-ttu-id="959bc-196">メソッドが静的かどうかを指定する値、オプション。</span><span class="sxs-lookup"><span data-stu-id="959bc-196">A value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="959bc-197">isStatic</span><span class="sxs-lookup"><span data-stu-id="959bc-197">isStatic</span></span>  
<span data-ttu-id="959bc-198">メソッドが静的かどうかを指定する値、オプション。</span><span class="sxs-lookup"><span data-stu-id="959bc-198">A value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="959bc-199">備考</span><span class="sxs-lookup"><span data-stu-id="959bc-199">Remarks</span></span>

<span data-ttu-id="959bc-200">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="959bc-200">This method is overridden by nodes that have source code.</span></span>

### <a name="method-aotrun"></a><span data-ttu-id="959bc-201">メソッド AOTrun</span><span class="sxs-lookup"><span data-stu-id="959bc-201">Method AOTrun</span></span>

<span data-ttu-id="959bc-202">Finance and Operations アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="959bc-202">Compiles this node and its subtree in the Finance and Operations Application Object Tree (AOT).</span></span>

    public void AOTrun()

### <a name="method-aotedit"></a><span data-ttu-id="959bc-203">メソッド AOTedit</span><span class="sxs-lookup"><span data-stu-id="959bc-203">Method AOTedit</span></span>

<span data-ttu-id="959bc-204">このノードの適切なエディタを開きます。</span><span class="sxs-lookup"><span data-stu-id="959bc-204">Opens the appropriate editor for this node.</span></span>

    public void AOTedit([int Line], [int Column])

#### <a name="parameters"></a><span data-ttu-id="959bc-205">パラメーター</span><span class="sxs-lookup"><span data-stu-id="959bc-205">Parameters</span></span>

<span data-ttu-id="959bc-206">明細行</span><span class="sxs-lookup"><span data-stu-id="959bc-206">Line</span></span>  
<span data-ttu-id="959bc-207">カーソル位置の列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="959bc-207">The column of the cursor position; optional.</span></span>

<!-- -->

<span data-ttu-id="959bc-208">円柱</span><span class="sxs-lookup"><span data-stu-id="959bc-208">Column</span></span>  
<span data-ttu-id="959bc-209">カーソル位置の列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="959bc-209">The column of the cursor position; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="959bc-210">備考</span><span class="sxs-lookup"><span data-stu-id="959bc-210">Remarks</span></span>

<span data-ttu-id="959bc-211">ノードがメソッドである場合は、コード エディタが開きます。</span><span class="sxs-lookup"><span data-stu-id="959bc-211">If the node is a method, the code editor opens.</span></span> <span data-ttu-id="959bc-212">ノードがドキュメンテーションの対象である場合は、ヘルプ エディタが開きます。</span><span class="sxs-lookup"><span data-stu-id="959bc-212">If the node is a documentation object, the Help editor opens.</span></span>



