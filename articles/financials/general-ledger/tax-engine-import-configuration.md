---
title: 税エンジン インポート コンフィギュレーション
description: このトピックでは、輸入税エンジンのコンフィギュレーションについて説明します。
author: yijialuan
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, GTE
audience: IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: India
ms.author: riluan
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e6b963eb00027da73bd89791ef9f22e7472a9657
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369796"
---
# <a name="import-tax-engine-configurations"></a><span data-ttu-id="cd4d3-103">輸入税エンジン コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="cd4d3-103">Import tax engine configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd4d3-104">このトピックでは、輸入税エンジンのコンフィギュレーションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cd4d3-104">This topic provides information about import tax engine configuration.</span></span>

### <a name="create-a-lifecycle-services-lcs-configuration-repository"></a><span data-ttu-id="cd4d3-105">Lifecycle Services (LCS) のコンフィギュレーション リポジトリの作成</span><span class="sxs-lookup"><span data-stu-id="cd4d3-105">Create a Lifecycle Services (LCS) configuration repository</span></span>
1. <span data-ttu-id="cd4d3-106">**組織管理** > **ワークスペース** > **電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cd4d3-106">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="cd4d3-107">**コンフィギュレーション プロバイダー**セクションで、**Microsoft** プロバイダー タイルの**リポジトリ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd4d3-107">In the **Configuration providers** section, click **Repositories** on the **Microsoft** provider tile.</span></span>

![コンフィギュレーションの読み込み](media/gte-extension-repositories.png)

3. <span data-ttu-id="cd4d3-109">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd4d3-109">Click **Add**.</span></span> 
4. <span data-ttu-id="cd4d3-110">**LCS** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd4d3-110">Select the **LCS** option.</span></span> 
5. <span data-ttu-id="cd4d3-111">**リポジトリの作成**をクリックして、LCS コンフィギュレーション リポジトリを作成します。</span><span class="sxs-lookup"><span data-stu-id="cd4d3-111">Click **Create repository** to create an LCS configuration repository.</span></span>
6. <span data-ttu-id="cd4d3-112">リポジトリの名前と説明を入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd4d3-112">Enter a name and description for the repository and then click **OK**.</span></span>

### <a name="import-configurations-from-lcs"></a><span data-ttu-id="cd4d3-113">LCS からコンフィギュレーションをインポートする</span><span class="sxs-lookup"><span data-stu-id="cd4d3-113">Import configurations from LCS</span></span>
1. <span data-ttu-id="cd4d3-114">**組織管理** > **ワークスペース** > **電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cd4d3-114">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="cd4d3-115">**コンフィギュレーション プロバイダー**セクションで、**Microsoft** プロバイダー タイルの**リポジトリ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd4d3-115">In the **Configuration providers** section, click **Repositories** on the **Microsoft** provider tile.</span></span>
3. <span data-ttu-id="cd4d3-116">作成したコンフィギュレーション リポジトリを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd4d3-116">Select the configuration repository that you just created.</span></span> 
4. <span data-ttu-id="cd4d3-117">**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd4d3-117">Click **Open**.</span></span>
5. <span data-ttu-id="cd4d3-118">ツリーで、最新の税務書類を選択します (たとえば、**税 (インド GST)** を選択)。</span><span class="sxs-lookup"><span data-stu-id="cd4d3-118">In the tree, select the latest tax document (for example, select **Tax (India GST)**).</span></span>
6. <span data-ttu-id="cd4d3-119">**バージョン**セクションで、**インポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd4d3-119">In the **Versions** section, click **Import**.</span></span>

![コンフィギュレーションの読み込み](media/gte-extension-import-configurations.png)

7. <span data-ttu-id="cd4d3-121">**はい**をクリックして、インポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="cd4d3-121">Click **Yes** to confirm the import.</span></span>