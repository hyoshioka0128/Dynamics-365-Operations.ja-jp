---
title: "ウィザードのフォーム パターン"
description: "この記事では、ウィザードのフォーム パターンに関する情報を提供します。 ウィザードは、順序付けられた一連のタブ ページを使用して、ユーザーがタスクを実行するユーザー アシスタントの特別なフォームです。"
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
ms.custom: 14671
ms.assetid: 564b88d7-85f5-488a-bbbe-19eff7194321
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b6da7e67f1f4917d07d0405d3a05a30bd7b5da84
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="wizard-form-pattern"></a><span data-ttu-id="4ba59-104">ウィザードのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="4ba59-104">Wizard form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ba59-105">この記事では、ウィザードのフォーム パターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="4ba59-105">This article provides information about the Wizard form pattern.</span></span> <span data-ttu-id="4ba59-106">ウィザードは、順序付けられた一連のタブ ページを使用して、ユーザーがタスクを実行するユーザー アシスタントの特別なフォームです。</span><span class="sxs-lookup"><span data-stu-id="4ba59-106">A wizard is a special form of user assistance that takes the user through a task by using an ordered series of tab pages.</span></span>

<a name="usage"></a><span data-ttu-id="4ba59-107">用途</span><span class="sxs-lookup"><span data-stu-id="4ba59-107">Usage</span></span>
-----

<span data-ttu-id="4ba59-108">ウィザードは、順序付けられた一連のタブ ページを使用して、ユーザーがタスクを実行するユーザー アシスタントの特別なフォームです。</span><span class="sxs-lookup"><span data-stu-id="4ba59-108">A wizard is a special form of user assistance that takes the user through a task by using an ordered series of tab pages.</span></span> <span data-ttu-id="4ba59-109">ウィザードは、学習または実行が難しい複雑または頻度の低いタスクで、または頻繁に実行する面倒なタスクで特に便利です。</span><span class="sxs-lookup"><span data-stu-id="4ba59-109">Wizards are especially useful for complex or infrequent tasks that the user might have difficulty learning or doing, or for tedious, frequently performed tasks.</span></span>

## <a name="wireframe"></a><span data-ttu-id="4ba59-110">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="4ba59-110">Wireframe</span></span>

<span data-ttu-id="4ba59-111">[![ワイヤーフレーム](./media/wizard1-1024x574.png)](./media/wizard1.png)</span><span class="sxs-lookup"><span data-stu-id="4ba59-111">[![Wireframe](./media/wizard1-1024x574.png)](./media/wizard1.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="4ba59-112">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="4ba59-112">Pattern changes</span></span>
<span data-ttu-id="4ba59-113">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4ba59-113">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="4ba59-114">ウィザード ステップの 2 番目の指示は、そのステップの [タブ] ページのヘルプ テキスト プロパティですでに定義されていました。</span><span class="sxs-lookup"><span data-stu-id="4ba59-114">The secondary instruction for a wizard step was previously defined in the Help Text property of that step’s Tab Page.</span></span> <span data-ttu-id="4ba59-115">この指示はタブページで静的テキスト コントロールとしてモデル化されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4ba59-115">This instruction will now be modeled on the Tab Page as a Static Text control.</span></span>

## <a name="model"></a><span data-ttu-id="4ba59-116">モデル</span><span class="sxs-lookup"><span data-stu-id="4ba59-116">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="4ba59-117">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="4ba59-117">High-level structure</span></span>

- <span data-ttu-id="4ba59-118">デザイン (スタイル = ウィザード; キャプション =&lt;ウィザード タイトル&gt;)</span><span class="sxs-lookup"><span data-stu-id="4ba59-118">Design (Style=Wizard; Caption=&lt;wizard title&gt;)</span></span>

    - <span data-ttu-id="4ba59-119">WizardContent (Tab)</span><span class="sxs-lookup"><span data-stu-id="4ba59-119">WizardContent (Tab)</span></span>

        - <span data-ttu-id="4ba59-120">WizardContentPage (TabPage) *\[1..N 回繰り返し、任意の名前を付けることができます。キャプションはページ タイトルに設定します\]*</span><span class="sxs-lookup"><span data-stu-id="4ba59-120">WizardContentPage (TabPage) *\[repeats 1..N times, can be named anything; Caption set to page title\]*</span></span>

            - <span data-ttu-id="4ba59-121">MainInstruction (StaticText)</span><span class="sxs-lookup"><span data-stu-id="4ba59-121">MainInstruction (StaticText)</span></span>
            - <span data-ttu-id="4ba59-122">本文 (グループ)</span><span class="sxs-lookup"><span data-stu-id="4ba59-122">Body (Group)</span></span>

### <a name="core-components"></a><span data-ttu-id="4ba59-123">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="4ba59-123">Core components</span></span>

1.  <span data-ttu-id="4ba59-124">**Form.Design** にウィザード パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="4ba59-124">Apply the Wizard pattern on **Form.Design**.</span></span>
2.  <span data-ttu-id="4ba59-125">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="4ba59-125">Address BP Warnings:</span></span>
    1.  <span data-ttu-id="4ba59-126">**Design.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="4ba59-126">**Design.Caption** isn't empty.</span></span>
    2.  <span data-ttu-id="4ba59-127">このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ba59-127">The form must be referenced by at least one menu item.</span></span>
    3.  <span data-ttu-id="4ba59-128">**TabPage.Caption** は空ではありません (すべてのウィザードのコンテンツ ページで)。</span><span class="sxs-lookup"><span data-stu-id="4ba59-128">**TabPage.Caption** isn't empty (for all wizard content pages).</span></span>
    4.  <span data-ttu-id="4ba59-129">**MainInstruction.Text** が空ではありません(すべてのウィザードのコンテンツ ページ)。</span><span class="sxs-lookup"><span data-stu-id="4ba59-129">**MainInstruction.Text** isn't empty (for all wizard content pages).</span></span>

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="4ba59-130">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="4ba59-130">Commonly used subpatterns</span></span>

-   [<span data-ttu-id="4ba59-131">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="4ba59-131">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)
-   [<span data-ttu-id="4ba59-132">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="4ba59-132">Toolbar and List</span></span>](toolbar-list-subpattern.md)
-   [<span data-ttu-id="4ba59-133">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="4ba59-133">Toolbar and Fields</span></span>](toolbar-fields-subpattern.md)
-   [<span data-ttu-id="4ba59-134">リスト パネル</span><span class="sxs-lookup"><span data-stu-id="4ba59-134">List Panel</span></span>](list-panel-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="4ba59-135">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="4ba59-135">UX guidelines</span></span>
<span data-ttu-id="4ba59-136">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="4ba59-136">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="4ba59-137">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="4ba59-137">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="4ba59-138">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="4ba59-138">Open the form in the browser, and walk through these steps.</span></span> 

<span data-ttu-id="4ba59-139">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="4ba59-139">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="4ba59-140">標準フォーム ガイドラインは、Microsoft Dynamics AX の[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="4ba59-140">Standard form guidelines have been consolidated into the Microsoft Dynamics AX [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="4ba59-141">**ウィザード** **ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="4ba59-141">**Wizard** **guidelines:**</span></span>

-   <span data-ttu-id="4ba59-142">各タブ ページには、タイトルがあるべきです。</span><span class="sxs-lookup"><span data-stu-id="4ba59-142">Each tab page should have a title.</span></span>
-   <span data-ttu-id="4ba59-143">各タブ ページには、主な指示があるべきです。</span><span class="sxs-lookup"><span data-stu-id="4ba59-143">Each tab page should have a main instruction.</span></span>
-   <span data-ttu-id="4ba59-144">コンテンツは、ページあたりの論理グループに分割する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ba59-144">Content should be subdivided into logical groups per page.</span></span>
-   <span data-ttu-id="4ba59-145">ウィザードには、適切なページに **&lt; 次へ &gt;** および **&lt; 前へ &gt;** ボタンがあります。</span><span class="sxs-lookup"><span data-stu-id="4ba59-145">A wizard should have **&lt;Next&gt;** and **&lt;Previous&gt;** buttons on the appropriate pages.</span></span>
-   <span data-ttu-id="4ba59-146">ユーザーはウィザードをキャンセルすることもできます。キャンセルすると、ウィザードを開始する前の状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="4ba59-146">The user should also be able to cancel the wizard, and cancellation should return to the state that existed before the wizard was started.</span></span>
-   <span data-ttu-id="4ba59-147">各ウィザード ページ (タブ ページ) ごとに、質問が 1 つだけ尋ねられます。</span><span class="sxs-lookup"><span data-stu-id="4ba59-147">Only one question should be asked per wizard page (tab page).</span></span>
-   <span data-ttu-id="4ba59-148">一組の選択肢がユーザーに提示されたときは、チェック ボックスまたはコンボ ボックスが条件を満たしている場合でも、オプション ボタンを使用して代替を明確にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ba59-148">When a set of choices is presented to the user, radio buttons should be used to make the alternatives clear, even if a check box or combo box is otherwise acceptable.</span></span>
-   <span data-ttu-id="4ba59-149">ウィザード フォームには以下の要素を含め **ません**。</span><span class="sxs-lookup"><span data-stu-id="4ba59-149">Wizard forms must **not** have these elements:</span></span>
    -   <span data-ttu-id="4ba59-150">情報ボックス</span><span class="sxs-lookup"><span data-stu-id="4ba59-150">FactBoxes</span></span>
    -   <span data-ttu-id="4ba59-151">クイック タブ</span><span class="sxs-lookup"><span data-stu-id="4ba59-151">FastTabs</span></span>

## <a name="examples"></a><span data-ttu-id="4ba59-152">例</span><span class="sxs-lookup"><span data-stu-id="4ba59-152">Examples</span></span>
<span data-ttu-id="4ba59-153">フォーム: **WrkCtrBulkResReqEditWizard**</span><span class="sxs-lookup"><span data-stu-id="4ba59-153">Form: **WrkCtrBulkResReqEditWizard**</span></span> 

<span data-ttu-id="4ba59-154">[![wizardExample](./media/wizardexample.png)](./media/wizardexample.png)[](./media/wizard2.png)</span><span class="sxs-lookup"><span data-stu-id="4ba59-154">[![wizardExample](./media/wizardexample.png)](./media/wizardexample.png)[](./media/wizard2.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="4ba59-155">付録</span><span class="sxs-lookup"><span data-stu-id="4ba59-155">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="4ba59-156">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="4ba59-156">Frequently asked questions</span></span>

<span data-ttu-id="4ba59-157">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="4ba59-157">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="4ba59-158">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="4ba59-158">Open issues</span></span>

-   <span data-ttu-id="4ba59-159">None</span><span class="sxs-lookup"><span data-stu-id="4ba59-159">None</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="4ba59-160">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="4ba59-160">AX 2012 content</span></span>

#### <a name="ax-2012-links"></a><span data-ttu-id="4ba59-161">AX 2012 のリンク</span><span class="sxs-lookup"><span data-stu-id="4ba59-161">AX 2012 links</span></span>

-   <span data-ttu-id="4ba59-162">[Microsoft Dynamics AX での MSDN ウィザード \[AX 2012\]](http://msdn.microsoft.com/en-us/library/aa622644.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ba59-162">[MSDN Wizards in Microsoft Dynamics AX \[AX 2012\]](http://msdn.microsoft.com/en-us/library/aa622644.aspx)</span></span>
-   <span data-ttu-id="4ba59-163">[ウィザード開発のための MSDN ガイドライン \[AX 2012\]](http://msdn.microsoft.com/EN-US/library/aa853845.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ba59-163">[MSDN Guidelines for Wizard Development \[AX 2012\]](http://msdn.microsoft.com/EN-US/library/aa853845.aspx)</span></span>

#### <a name="ax-2012-example"></a><span data-ttu-id="4ba59-164">AX 2012 の例</span><span class="sxs-lookup"><span data-stu-id="4ba59-164">AX 2012 example</span></span>

<span data-ttu-id="4ba59-165">[![AX 2012 の例](./media/wizard3.png)](./media/wizard3.png)</span><span class="sxs-lookup"><span data-stu-id="4ba59-165">[![AX 2012 example](./media/wizard3.png)](./media/wizard3.png)</span></span>
