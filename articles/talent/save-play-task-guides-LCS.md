---
title: "LCS にタスク ガイドを保存し、それらを再生する"
description: "このトピックでは、タスク ガイドを Microsoft Dynamics Lifecycle Services (LCS) に保存し、それらを再生する方法について説明します。"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 40b4c3154a04a557b8a670e1f1ae3722c71122fe
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---

# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="3dccd-103">LCS にタスク ガイドを保存し、それらを再生する</span><span class="sxs-lookup"><span data-stu-id="3dccd-103">Save task guides to LCS and replay them</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3dccd-104">**環境の詳細**</span><span class="sxs-lookup"><span data-stu-id="3dccd-104">**Environment details**</span></span> 

<span data-ttu-id="3dccd-105">Microsoft Dynamics Lifecycle Services (LCS) 経由で配置された Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="3dccd-105">Microsoft Dynamics 365 for Talent, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="3dccd-106">**払出**</span><span class="sxs-lookup"><span data-stu-id="3dccd-106">**Issue**</span></span>

<span data-ttu-id="3dccd-107">顧客は自分の LCS プロジェクトに新しいタスクの記録を保存し、保存されているタスク ガイドを再生することを希望しています。</span><span class="sxs-lookup"><span data-stu-id="3dccd-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="3dccd-108">**解像度**</span><span class="sxs-lookup"><span data-stu-id="3dccd-108">**Resolution**</span></span>

<span data-ttu-id="3dccd-109">LCS にタスク記録を保存するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3dccd-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="3dccd-110">LCS にサインインして、プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="3dccd-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="3dccd-111">**ビジネス プロセス モデラー**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="3dccd-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="3dccd-112">「更新された BPM エクスペリエンス。」でページを表示する</span><span class="sxs-lookup"><span data-stu-id="3dccd-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="3dccd-113">ライブラリを選択してから、**コピー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3dccd-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="3dccd-114">ビジネス プロセス モデラー (BPM) モデルの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="3dccd-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="3dccd-115">LCS から Talent へサインインします。</span><span class="sxs-lookup"><span data-stu-id="3dccd-115">Sign in to Talent from LCS.</span></span>
7. <span data-ttu-id="3dccd-116">**検索**フィールドで、**ヘルプ**と入力します。</span><span class="sxs-lookup"><span data-stu-id="3dccd-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="3dccd-117">Lifecycle Services ヘルプが開きます。</span><span class="sxs-lookup"><span data-stu-id="3dccd-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="3dccd-118">Lifecycle Services のヘルプ構成の**更新**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="3dccd-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="3dccd-119">新しい有効な BPM ライブラリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3dccd-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="3dccd-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3dccd-120">Close the page.</span></span>
10. <span data-ttu-id="3dccd-121">タスク記録を作成します。</span><span class="sxs-lookup"><span data-stu-id="3dccd-121">Create a task recording.</span></span>
11. <span data-ttu-id="3dccd-122">完了したら、**Lifecycle Services に保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3dccd-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Lifecycle Services に保存](media/task-guides.png)

12. <span data-ttu-id="3dccd-124">タスク記録を保存する BPM ライブラリとノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="3dccd-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="3dccd-125">LCS からタスク ガイドを再生するにはこれらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3dccd-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="3dccd-126">タスク レコーダーを開始します。</span><span class="sxs-lookup"><span data-stu-id="3dccd-126">Start Task recorder.</span></span>
2. <span data-ttu-id="3dccd-127">**LCS から開く**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3dccd-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="3dccd-128">タスク ガイドが保存されているライブラリと BPM ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="3dccd-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="3dccd-129">タスク ガイドを開きます。</span><span class="sxs-lookup"><span data-stu-id="3dccd-129">Open the task guide.</span></span>
