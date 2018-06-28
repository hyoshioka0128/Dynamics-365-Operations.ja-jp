---
title: "電子申告フレームワークのコンフィギュレーション"
description: "このトピックでは、電子レポート (ER) フレームワークのパラメーターを構成する方法について説明します。"
author: NickSelin
manager: AnnBe
ms.date: 05/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace, ERParameters, ERFormatDestinationTable
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 3c1291de-230c-4e31-96c4-ba69a310690a
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 93d11c6cfd8aa6a10b6f0932e09cf25746e5db0a
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="configure-the-electronic-reporting-framework"></a><span data-ttu-id="6f627-103">電子申告フレームワークのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6f627-103">Configure the Electronic reporting framework</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f627-104">このトピックでは、電子申告 (ER) の基本機能を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6f627-104">This topic explains how to set up the basic functionality for Electronic reporting (ER).</span></span> <span data-ttu-id="6f627-105">また、ER を設定する前に完了する必要のある手順も説明します。</span><span class="sxs-lookup"><span data-stu-id="6f627-105">It also describes the steps that you must complete before you can set up ER.</span></span>

## <a name="prerequisites-for-er-setup"></a><span data-ttu-id="6f627-106">ER セットアップの前提条件</span><span class="sxs-lookup"><span data-stu-id="6f627-106">Prerequisites for ER setup</span></span>
<span data-ttu-id="6f627-107">ER を設定する前に、ドキュメント管理で必要なドキュメント タイプを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f627-107">Before you can set up ER, you must set up the required document types in Document management:</span></span>

- <span data-ttu-id="6f627-108">ER レポート テンプレートとして使用される Microsoft Office ドキュメントのドキュメント タイプ。</span><span class="sxs-lookup"><span data-stu-id="6f627-108">A document type for Microsoft Office documents that are used as templates for ER reports.</span></span>
- <span data-ttu-id="6f627-109">ジョブ アーカイブに ER レポートの出力を保存するために使用するドキュメント タイプ。</span><span class="sxs-lookup"><span data-stu-id="6f627-109">A document type that is used to store the output of ER reports in the jobs archive.</span></span>
- <span data-ttu-id="6f627-110">他のプログラムで表示できるように、ER レポートの出力を保存するために使用するドキュメント タイプ。</span><span class="sxs-lookup"><span data-stu-id="6f627-110">A document type that is used to store the output of ER reports so that they can be viewed in other programs.</span></span>
- <span data-ttu-id="6f627-111">その他のすべての目的で、ER フレームワーク内のファイルを処理するために使用されるドキュメント タイプ。</span><span class="sxs-lookup"><span data-stu-id="6f627-111">A document type that is used to handle files in the ER framework for all other purposes.</span></span>

<span data-ttu-id="6f627-112">各ドキュメント タイプについては、次の属性値を選択できます。</span><span class="sxs-lookup"><span data-stu-id="6f627-112">For each document type, the following attribute values can be selected.</span></span>

<span data-ttu-id="6f627-113">属性名</span><span class="sxs-lookup"><span data-stu-id="6f627-113">Attribute name</span></span> | <span data-ttu-id="6f627-114">属性値</span><span class="sxs-lookup"><span data-stu-id="6f627-114">Attribute value</span></span>
---------------|----------------
<span data-ttu-id="6f627-115">クラス</span><span class="sxs-lookup"><span data-stu-id="6f627-115">Class</span></span> | <span data-ttu-id="6f627-116">**ファイルの添付**</span><span class="sxs-lookup"><span data-stu-id="6f627-116">**Attach file**</span></span>
<span data-ttu-id="6f627-117">グループ化</span><span class="sxs-lookup"><span data-stu-id="6f627-117">Group</span></span> | <span data-ttu-id="6f627-118">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="6f627-118">**File**</span></span>
<span data-ttu-id="6f627-119">保管場所</span><span class="sxs-lookup"><span data-stu-id="6f627-119">Location</span></span> | <span data-ttu-id="6f627-120">**Azure ストレージ**または **SharePoint**</span><span class="sxs-lookup"><span data-stu-id="6f627-120">**Azure storage** or **SharePoint**</span></span>

## <a name="set-up-er"></a><span data-ttu-id="6f627-121">ER の設定</span><span class="sxs-lookup"><span data-stu-id="6f627-121">Set up ER</span></span>
<span data-ttu-id="6f627-122">すべての法人に対して ER の基本機能を設定するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="6f627-122">Use the following procedure to set up the basic functionality of ER for all legal entities.</span></span>

1.  <span data-ttu-id="6f627-123">**電子申告のパラメーター**ページの、**添付ファイル**タブで、ER フレームワークのファイルの記憶域に使用する必要があるドキュメントのタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="6f627-123">On the **Electronic reporting parameters** page, on the **Attachments** tab, define the types of documents that should be used for file storage in the ER framework.</span></span>
2. <span data-ttu-id="6f627-124">**LCS** タブで、Microsoft Dynamics Lifecycle Services (LCS) のリポジトリから ER コンフィギュレーションの読み込みに使用する必要がある並列スレッドの数を定義し、最も効率的な方法でコンフィギュレーションが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="6f627-124">On the **LCS** tab, define the number of parallel threads that should be used to load an ER configuration from repositories in Microsoft Dynamics Lifecycle Services (LCS), so that the configurations are loaded in the most efficient manner.</span></span> <span data-ttu-id="6f627-125">値は、現在のプログラムで使用可能なリソースによって、**1** ～ **15** のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="6f627-125">The value can vary from **1** to **15**, depending on the available resources of the current program.</span></span> <span data-ttu-id="6f627-126">スレッドの実際の数は、この設定およびおよびその他のタスクの数とその優先度に基づいて自動的に定義されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6f627-126">Note that the real number of threads will be defined automatically, based on this setting, and on the number of other tasks and their priorities.</span></span>
3.  <span data-ttu-id="6f627-127">**コンフィギュレーション プロバイダー テーブル**ページで、ER プロバイダー レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="6f627-127">On the **Configuration provider table** page, create ER provider records.</span></span> <span data-ttu-id="6f627-128">各プロバイダーは、**有効**としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="6f627-128">Each provider can be marked as **Active**.</span></span> <span data-ttu-id="6f627-129">有効なプロバイダーの名前およびインターネット アドレスは、構成の所有者の属性として ER 構成に格納されます。</span><span class="sxs-lookup"><span data-stu-id="6f627-129">The active provider’s name and Internet address are stored in an ER configuration as attributes of the owner of the configuration.</span></span>

## <a name="optional-setup-for-er"></a><span data-ttu-id="6f627-130">ER のオプションの設定</span><span class="sxs-lookup"><span data-stu-id="6f627-130">Optional setup for ER</span></span>
<span data-ttu-id="6f627-131">基本機能に加えて、ER に設定できる他の機能があります。</span><span class="sxs-lookup"><span data-stu-id="6f627-131">In addition to the basic functionality, ER has other functionality that you can set up.</span></span>

- <span data-ttu-id="6f627-132">**電子申告の送信先**ページで、各 ER 形式コンフィギュレーションの各ファイル出力の ER 出力先を定義します。</span><span class="sxs-lookup"><span data-stu-id="6f627-132">On the **Electronic reporting destination** page, define the ER output destinations for each file output of each ER format configuration.</span></span> <span data-ttu-id="6f627-133">前に設定したドキュメント管理フレームワークのドキュメント タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="6f627-133">Use the document types of the Document management framework that you set up earlier.</span></span> <span data-ttu-id="6f627-134">また、各法人に対して ER のオプション機能を設定するためにこのページを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6f627-134">You can also use this page to set up the optional functionality of ER for each legal entity.</span></span> <span data-ttu-id="6f627-135">詳細については、このトピックの「その他のリソース」セクションにリンクされている ER 宛先に関するトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f627-135">For more information, see the topic about ER destinations that is linked in the "Additional resources" section of this topic.</span></span>
- <span data-ttu-id="6f627-136">新しいアプリケーション オブジェクト ツリー (AOT) のコンポーネントを追加するたびに、または ER でデータ ソース (テーブル、ビュー、またはデータ エンティティ) として使用される既存の AOT コンポーネントを更新するたびに、**テーブル参照の再構築**メニュー項目 (**組織管理** > **電子申告** > **テーブル参照の再構築**) 、AOT の変更を ER メタデータに反映します。</span><span class="sxs-lookup"><span data-stu-id="6f627-136">Whenever you add new Application Object Tree (AOT) artifacts or update existing AOT artifacts that are used as data sources (tables, views, or data entities) in ER, use the **Rebuild table references** menu item (**Organization administration** > **Electronic reporting** > **Rebuild table references**) to bring your AOT changes into the ER metadata.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="6f627-137">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="6f627-137">Frequently asked questions</span></span>
<span data-ttu-id="6f627-138">**質問:** LCS から ER コンフィギュレーションを読み込むのに最適な並列スレッド数はどれくらいですか。</span><span class="sxs-lookup"><span data-stu-id="6f627-138">**Question:** What is the optimal number of parallel threads to use to load an ER configuration from LCS?</span></span>

<span data-ttu-id="6f627-139">**回答:** 最適な並行スレッドの数を計算するには、次の経験式を使用します。コア ÷ 2 + 1(2)。</span><span class="sxs-lookup"><span data-stu-id="6f627-139">**Answer:** To calculate the optimal number of parallel threads, use the following empirical formula: Cores ÷ 2 + 1(2).</span></span> <span data-ttu-id="6f627-140">たとえば、プログラムが 2 つの CPU を持つ仮想マシン (VM) を実行する場合、各 CPU には 4 つのコアが含まれ、最適な数は 5 または 6 の並列スレッドです。</span><span class="sxs-lookup"><span data-stu-id="6f627-140">For example, if the program runs on a virtual machine (VM) that has two CPUs, and each CPU contains four cores, the optimal number is five or six parallel threads.</span></span>

<span data-ttu-id="6f627-141">**質問:** AOT にカスタム テーブルを追加しました。</span><span class="sxs-lookup"><span data-stu-id="6f627-141">**Question:** I have added a custom table to the AOT.</span></span> <span data-ttu-id="6f627-142">ER データ モデルの新しい ER モデル マッピング コンフィギュレーションを作成しました。</span><span class="sxs-lookup"><span data-stu-id="6f627-142">I created a new ER model mapping configuration for my ER data model.</span></span> <span data-ttu-id="6f627-143">モデルのマッピングの設計中に、個人のテーブルを指す、新しいデータ ソース タイプ**テーブル レコード**を追加しようとします。</span><span class="sxs-lookup"><span data-stu-id="6f627-143">During the design of the model mapping, I tried to add a new data source type, **Table records**, that refers to my table.</span></span> <span data-ttu-id="6f627-144">テーブル名を**テーブル** ルックアップに手動で追加し、ER モデル マッピングではエラーまたは警告なしで承認されました。</span><span class="sxs-lookup"><span data-stu-id="6f627-144">I could manually add my table name to the **Table** lookup, and the ER model mapping accepted it without errors or warnings.</span></span> <span data-ttu-id="6f627-145">ただし、個人のテーブル名は、このデータ ソースの**テーブル**ルックアップが提供する利用可能な選択肢の一覧に含まれていません。</span><span class="sxs-lookup"><span data-stu-id="6f627-145">However, my table’s name isn't included in the list of available choices that the **Table** lookup of this data source offers.</span></span> <span data-ttu-id="6f627-146">テーブルの名前をどのように含めますか。</span><span class="sxs-lookup"><span data-stu-id="6f627-146">How do I include the name of my table?</span></span>

<span data-ttu-id="6f627-147">**回答:** カスタムテーブルの名前を **テーブル**ルックアップに含めるには、このトピックの前半の **ER のオプション設定**セクションで説明されているように、**テーブル参照の再構築**メニュー項目を使用してください。</span><span class="sxs-lookup"><span data-stu-id="6f627-147">**Answer:** To include the name of your custom table in the **Table** lookup, use the **Rebuild table references** menu item as described in the **Optional setup for ER"** section earlier in this topic.</span></span>

<span data-ttu-id="6f627-148">**質問:** 実稼動環境の**電子申告**ワークスペースで、Microsoft プロバイダーを**有効**としてマークできないのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="6f627-148">**Question:** Why can’t I mark the Microsoft provider as **Active** in the **Electronic reporting** workspace in my production environment?</span></span>

<span data-ttu-id="6f627-149">**回答:** Microsoft プロバイダーは、Microsoft が設計および管理している ER コンフィギュレーションをマークするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6f627-149">**Answer:** The Microsoft provider is used to mark ER configurations that have been designed and maintained by Microsoft.</span></span> <span data-ttu-id="6f627-150">Microsoft は、今後、構成の新しいバージョンをリリースすることを考えてています。</span><span class="sxs-lookup"><span data-stu-id="6f627-150">We expect that Microsoft will release new versions of the configurations in the future.</span></span> <span data-ttu-id="6f627-151">Microsoft プロバイダーを **有効** とマークしないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6f627-151">We recommend that you not mark the Microsoft provider as **Active**.</span></span> <span data-ttu-id="6f627-152">それ以外の場合、構成を更新できます。</span><span class="sxs-lookup"><span data-stu-id="6f627-152">Otherwise, you can update the configurations.</span></span> <span data-ttu-id="6f627-153">(たとえば、コンテンツを変更して新しいバージョンを登録することができます。) これらのアップデートにより、Microsoft がコンフィギュレーションの新しいバージョンを提供するときに、今後問題が発生します。これらの新しいバージョンをインポートして採用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f627-153">(For example, you can change the content and register new versions.) These updates will cause issues in the future, when Microsoft provides new versions of the configurations, and those new versions must be imported and adopted.</span></span> <span data-ttu-id="6f627-154">代わりに、会社の新しい ER プロバイダーを登録し、ER 構成の管理に使用します。</span><span class="sxs-lookup"><span data-stu-id="6f627-154">Instead, register a new ER provider for your company, and use it for your ER configurations maintenance.</span></span> <span data-ttu-id="6f627-155">Microsoft 構成を再利用するには、派生コピーのベースとして選択します。</span><span class="sxs-lookup"><span data-stu-id="6f627-155">To reuse a Microsoft configuration, select it as the base for your derived copy.</span></span> <span data-ttu-id="6f627-156">Microsoftによって提供される変更を組み込むには、構成が新しいバージョンの Microsoft 構成に使用可能になったときに、その構成をリベースします。</span><span class="sxs-lookup"><span data-stu-id="6f627-156">To incorporate changes that are provided by Microsoft, rebase your configuration to a new version of the Microsoft configuration when it becomes available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f627-157">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="6f627-157">Additional resources</span></span>

- [<span data-ttu-id="6f627-158">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="6f627-158">Electronic reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="6f627-159">電子申告の送信先</span><span class="sxs-lookup"><span data-stu-id="6f627-159">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)
