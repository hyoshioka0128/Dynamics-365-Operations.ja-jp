---
title: "継続的ビルドとテストの自動化を使用した配置"
description: "このトピックでは、継続的なビルドとテストの自動化をサポートする開発者トポロジを配置する方法について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 02/22/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 13171
ms.assetid: 
ms.search.region: Global
ms.author: shailesn
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fd772e81f59cb53ec6dbfaedef55b097d4d1480e
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="deployment-with-continuous-build-and-test-automation"></a><span data-ttu-id="0b0ac-103">継続的ビルドとテストの自動化を使用した配置</span><span class="sxs-lookup"><span data-stu-id="0b0ac-103">Deployment with continuous build and test automation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b0ac-104">このトピックでは、継続的なビルドとテストの自動化をサポートする開発者トポロジを配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-104">This topic describes how to deploy a developer topology that supports continuous build and test automation.</span></span>

<span data-ttu-id="0b0ac-105">前提条件: クラウド VM 展開には Visual Studio Team Services (VSTS) アカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-105">Prerequisite: This requires a Visual Studio Team Services (VSTS) account for cloud VM deployment.</span></span>

## <a name="workflow"></a><span data-ttu-id="0b0ac-106">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="0b0ac-106">Workflow</span></span>
<span data-ttu-id="0b0ac-107">Lifecycle Services (LCS) で VSTS サブスクリプションを設定した後、開発者トポロジの配置をトリガーして開発者およびビルド VM の設定をすることができます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-107">After you have configured a VSTS subscription in Lifecycle Services (LCS), you can trigger Developer Topology Deployment to set up Developer and Build VMs.</span></span> <span data-ttu-id="0b0ac-108">この配置では、開発者用 VM は VSTS プロジェクトに対して開発するためにワークスペース マッピングで構成されます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-108">In this deployment, the Developer VM is configured with workspace mapping to develop against a VSTS project.</span></span> <span data-ttu-id="0b0ac-109">ビルド VM は、モジュール VSTS プロジェクトを構築し、検証用の外部エンドポイントを使用して自動テストを実行するために、ビルド エージェント/コントローラーを使用して自動構成されます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-109">The Build VM is auto-configured with the build agent/controller to build modules  VSTS project and to execute automated tests with external endpoint for validation.</span></span> <span data-ttu-id="0b0ac-110">カスタム テスト コードの記述またはビルド インフラストラクチャと統合する自動テスト コードを生成する方法については、[テストと検証](testing-validation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-110">For more information on writing custom test code or generating automated test code to integrate with build infrastructure, see [Testing and validations](testing-validation.md).</span></span> <span data-ttu-id="0b0ac-111">一般的なワークフローまたは使用シナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-111">A typical workflow or usage scenario is shown below.</span></span> 

<span data-ttu-id="0b0ac-112">[![build12](./media/build12-1024x693.jpg)](./media/build12.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-112">[![build12](./media/build12-1024x693.jpg)](./media/build12.jpg)</span></span>

## <a name="set-up-visual-studio-team-services-vsts"></a><span data-ttu-id="0b0ac-113">Visual Studio Team Services (VSTS) の設定</span><span class="sxs-lookup"><span data-stu-id="0b0ac-113">Set up Visual Studio Team Services (VSTS)</span></span>
<span data-ttu-id="0b0ac-114">組織の必要な VSTS 機能を比較します。<https://www.visualstudio.com/products/visual-studio-team-services-feature-matrix-vs></span><span class="sxs-lookup"><span data-stu-id="0b0ac-114">Compare VSTS features required for your organization: <https://www.visualstudio.com/products/visual-studio-team-services-feature-matrix-vs></span></span>

-   <span data-ttu-id="0b0ac-115">**TFVC 対 GIT**: RTW では、LCS に接続された VSTS プロジェクトで構成できるソース コントロール リポジトリとして TFVC のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-115">**TFVC vs GIT**: For RTW, we only support TFVC as source control repository that can be configured in VSTS project connected to LCS.</span></span> <span data-ttu-id="0b0ac-116">Git はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-116">Git is not supported.</span></span>
-   <span data-ttu-id="0b0ac-117">**現在のビルドの中断:** 既にビルド定義が作成されている既存の VSTS プロジェクトにビルド エージェントを展開している場合、ビルドをキューに入れるための有効なトリガーがないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-117">**Suspend current builds:** If you are deploying the build agent on an existing VSTS project which already has build definition created, please ensure you do not have any active triggers to queue the build.</span></span> <span data-ttu-id="0b0ac-118">また、ビルド プールに対して、スケジュールされた/キューに格納されたビルドがないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-118">Additionally, make sure there are no builds scheduled / queued against the build pool.</span></span> 

    <span data-ttu-id="0b0ac-119">[![BuildTriggers](./media/buildtriggers.jpg)](./media/buildtriggers.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-119">[![BuildTriggers](./media/buildtriggers.jpg)](./media/buildtriggers.jpg)</span></span>

-   <span data-ttu-id="0b0ac-120">**無料の VSTS アカウントには、ビルド エージェントが 1 つだけ用意されています**。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-120">**Free VSTS account provides only one build agent**.</span></span> <span data-ttu-id="0b0ac-121">アカウントは複数のビルド エージェントに対してプロビジョニングされていないので、フリーの VSTS アカウントを使用して、別のビルド エージェントで新しいビルド VM を配置することは失敗します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-121">Using free VSTS account and deploying new build VM with another build agent will fail as your account is not provisioned for more than one build agent.</span></span>


<span data-ttu-id="0b0ac-122">複数のビルド エージェントを使用するには、Azure 請求 [[アカウントの請求を設定する](/vsts/billing/set-up-billing-for-your-account-vs)] で VSTS アカウントを設定します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-122">To use more than one build agents, setup your VSTS account with Azure billing: [Set up billing for your account](/vsts/billing/set-up-billing-for-your-account-vs)</span></span> 

<span data-ttu-id="0b0ac-123">[![VSTS1](./media/vsts1-300x155.jpg)](./media/vsts1.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-123">[![VSTS1](./media/vsts1-300x155.jpg)](./media/vsts1.jpg)</span></span>

-   <span data-ttu-id="0b0ac-124">アカウントが Azure サブスクリプションとリンクされた後。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-124">After your account is linked with the Azure subscription.</span></span> <span data-ttu-id="0b0ac-125">さらにビルド エージェントを繰り入れるため、Azure 管理ポータルで指示に従います - [ロード テストの購入](/vsts/billing/buy-load-testing-vs)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-125">Follow the instructions in the Azure management portal to provision more build agents - [Buy load testing](/vsts/billing/buy-load-testing-vs)</span></span>


<span data-ttu-id="0b0ac-126">[![VSTS2](./media/vsts2-300x151.jpg)](./media/vsts2.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-126">[![VSTS2](./media/vsts2-300x151.jpg)](./media/vsts2.jpg)</span></span> 

> [!NOTE]
> <span data-ttu-id="0b0ac-127">支払済オプションで、「プライベート エージェント」を増やしてください。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-127">Make sure you increase “Private Agents” under PAID option.</span></span> 

<span data-ttu-id="0b0ac-128">[![VSTS3](./media/vsts3-300x191.jpg)](./media/vsts3.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-128">[![VSTS3](./media/vsts3-300x191.jpg)](./media/vsts3.jpg)</span></span>

-   <span data-ttu-id="0b0ac-129">**ビルド エージェント プールのロールとアクセス許可:**<https://msdn.microsoft.com/library/vs/alm/build/agents/admin#agent-pools></span><span class="sxs-lookup"><span data-stu-id="0b0ac-129">**Build Agent Pool role and permissions:** <https://msdn.microsoft.com/library/vs/alm/build/agents/admin#agent-pools></span></span>

<span data-ttu-id="0b0ac-130">ビルド エージェントが追加されたら、ユーザー (LCS から VM を配置構築) を「エージェント プール管理者」ロールにします。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-130">Once build agents are added, add user (who will be deploying build VM from LCS) to “Agent Pool Administrators” role.</span></span> 

<span data-ttu-id="0b0ac-131">[![VSTS4](./media/vsts4.jpg)](./media/vsts4.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-131">[![VSTS4](./media/vsts4.jpg)](./media/vsts4.jpg)</span></span>

-   <span data-ttu-id="0b0ac-132">**管理エージェント:** 複数のエージェントがコンフィギュレーションされていて、1 つを削除する場合は、エージェントを選択し、ステータス列の右側にある削除ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-132">**Manage agent:** If you have multiple agents configured and want to delete one, select the agent and use the delete button to the right of the status column.</span></span>

    <span data-ttu-id="0b0ac-133">[![build14](./media/build14.jpg)](./media/build14.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-133">[![build14](./media/build14.jpg)](./media/build14.jpg)</span></span>

-   <span data-ttu-id="0b0ac-134">**既定のプールの削除:** 何らかの理由でデフォルト プールを削除した場合は、「既定」という名前の新しいプールを作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-134">**Deleting Default Pool:** If for some reason you have deleted the default pool, please do not create a new pool with the name "Default".</span></span> <span data-ttu-id="0b0ac-135">代わりに、別の名前で新しい管理グループを作成し、配置の際に LCS の「詳細設定」のカスタマイズから管理グループ名を渡します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-135">Instead create a new pool with the different name and pass the pool name from the "Advanced Settings" customization from LCS during deployment.</span></span>
-   <span data-ttu-id="0b0ac-136">**個人用アクセス トークン:** このトークンは、アップグレードおよび配置を含む Lifecycle Services (LCS) のバックグラウンド アクションで使用されます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-136">**Personal access token:** This token is used for all Lifecycle Services (LCS) background actions, including upgrade and deployment.</span></span> <span data-ttu-id="0b0ac-137">ユーザーが LCS からアクションを起動すると、LCS はユーザーが VSTS に追加されることを期待しています。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-137">When a user initiates actions from LCS, LCS expects that users will be added to VSTS.</span></span> <span data-ttu-id="0b0ac-138">ユーザーは、ユーザーの代わりに VSTS への LCS アクセスを認可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-138">The user must authorize LCS access to VSTS on behalf of the user.</span></span> <span data-ttu-id="0b0ac-139">プロジェクトのユーザーが VSTS で承認されるまで、アクション センターに以下のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-139">Until the projects users authorize with VSTS, you will see the below message in action center:</span></span> 

<span data-ttu-id="0b0ac-140">[![LCS の VSTS 設定\_5 月 27 日](./media/vsts-setup-in-lcs_may27-300x216.jpg)](./media/vsts-setup-in-lcs_may27.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-140">[![VSTS setup in LCS\_May27](./media/vsts-setup-in-lcs_may27-300x216.jpg)](./media/vsts-setup-in-lcs_may27.jpg)</span></span>

## <a name="deploy-developer-topology-from-lcs"></a><span data-ttu-id="0b0ac-141">LCS から開発者トポロジを配置する</span><span class="sxs-lookup"><span data-stu-id="0b0ac-141">Deploy Developer topology from LCS</span></span>
<span data-ttu-id="0b0ac-142">LCS では、開発トポロジ環境を配置するオプションが提供されます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-142">LCS provides an option to deploy a Development topology environment.</span></span> <span data-ttu-id="0b0ac-143">このオプションでは、Visual Studio Team System (VSTS) プロジェクトに接続されたクラウド内に、開発者を配置して VM をビルドすることができます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-143">With this option, you can deploy developer and build VMs in the cloud that are connected to your Visual Studio Team System  (VSTS) project.</span></span>

### <a name="vsts-credential-setup-and-linking-to-lcs-project"></a><span data-ttu-id="0b0ac-144">VSTS 資格情報の設定と LCS プロジェクトへのリンク</span><span class="sxs-lookup"><span data-stu-id="0b0ac-144">VSTS credential setup and linking to LCS project</span></span>

1. <span data-ttu-id="0b0ac-145">[https://lcs.dynamics.com/](https://lcs.dynamics.com/)で LCS ポータルにログインして、VSTS および LCS プロジェクトに接続します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-145">Login to the LCS portal to connect to VSTS and your LCS project at [https://lcs.dynamics.com/](https://lcs.dynamics.com/).</span></span>
2. <span data-ttu-id="0b0ac-146">作業しているプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-146">Select a project that you are working on.</span></span>
3. <span data-ttu-id="0b0ac-147">**プロジェクト設定**タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-147">Click the **Project Settings** tile.</span></span>
4. <span data-ttu-id="0b0ac-148">**Visual Studio Team Services** を選択し、モジュール プロジェクトのソース コードが保管されている VSTS URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-148">Select **Visual Studio Team Services** and enter the VSTS URL where the source code for your module project is located.</span></span>
5. <span data-ttu-id="0b0ac-149">VSTS リンクを指定して、承認し、**既定のプロジェクトを選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-149">Specify the VSTS link, authorize, and then click **Choose default project**.</span></span>
   > [!NOTE]
   > <span data-ttu-id="0b0ac-150">現在のところ、VSTF をソース コントロールとしてサポートしていますが、Git をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-150">We currently support VSTF as source control and do not support Git.</span></span> 

<span data-ttu-id="0b0ac-151">[![VSTS](./media/vsts-1024x792.jpg)](./media/vsts.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-151">[![VSTS](./media/vsts-1024x792.jpg)](./media/vsts.jpg)</span></span>

### <a name="check-in-migrated-or-new-module-code-into-vsts"></a><span data-ttu-id="0b0ac-152">VSTS に移行または新しいモジュールコードをチェックイン</span><span class="sxs-lookup"><span data-stu-id="0b0ac-152">Check-in migrated or new module code into VSTS</span></span>

<span data-ttu-id="0b0ac-153">コードの移行プロセスまたは開発活動の一環として、モデル ソース ファイルと関連するテスト モデル ソース ファイルを VSTS にチェックインすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-153">As part of code Migration process or development activities, we expect you to check-in your model source files and the associated test model source files into VSTS.</span></span> <span data-ttu-id="0b0ac-154">LCS 移行サービスを使用してコードを移行した場合、自動的に行われます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-154">If you have migrated your code using the LCS migration service, this is automatically done for you.</span></span> <span data-ttu-id="0b0ac-155">VSTS にコードをチェックインせずに直接チェックインする場合は、VSTS フォルダ構造の特定のガイドラインに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-155">If you have not checked in any code into VSTS and work on direct check-in, you must follow certain guidelines for the VSTS folder structure.</span></span> <span data-ttu-id="0b0ac-156">これは、適切なビルド定義の設定に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-156">This will help with setting up correct build definition.</span></span> <span data-ttu-id="0b0ac-157">すべてのモジュールをルート フォルダー**メタデータ**に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-157">All modules should be added to root folder **Metadata**.</span></span> <span data-ttu-id="0b0ac-158">各モジュールにはフォルダーが 2 つ必要です。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-158">Under each module, there should be two folders.</span></span> <span data-ttu-id="0b0ac-159">1 つのフォルダーには、すべてのモデルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-159">One folder contains all models.</span></span> <span data-ttu-id="0b0ac-160">他のフォルダーには、そのモジュールの記述子 XML が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-160">The other folder should contain descriptor XML for that module.</span></span> 

![VSTS フォルダー構造](media/build-trunk-main-metadata.png)

### <a name="deploy-developer-topology-developer-and-build-vm"></a><span data-ttu-id="0b0ac-162">開発者トポロジの配置 (開発者とビルド VM)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-162">Deploy developer topology (Developer and Build VM)</span></span>

1. <span data-ttu-id="0b0ac-163">LCS ポータルで、VSTS に接続されているプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-163">In the LCS portal, select the project that is connected to VSTS.</span></span>
2. <span data-ttu-id="0b0ac-164">**環境**ウィンドウで、**+** をクリックして新しい環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-164">In the **Environments** pane, click **+** to deploy a new environment.</span></span>

   ![Azure の設定](media/azure-settings.png)

3. <span data-ttu-id="0b0ac-166">**環境のトポロジの選択**ウィンドウで、**Azure** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-166">In the **Select environment topology** pane, select **Azure**.</span></span>

   ![環境のトポロジの選択](media/select-environment-topology.png)

4. <span data-ttu-id="0b0ac-168">DEV/TEST 環境の展開に進みます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-168">Proceed to deploy a DEV/TEST environment.</span></span>
   -   <span data-ttu-id="0b0ac-169">LCS プロジェクトのタイプによっては、以下に説明する配置ステップの一部が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-169">Depending on your LCS project type, some deployment steps described below may vary.</span></span>

5. <span data-ttu-id="0b0ac-170">**環境の配置**ウィンドウで、配置のための環境名を入力し、**開発者** VM のインスタンスの番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-170">On the **Deploy environment** pane, enter the environment name for the deployment, and select the number of instances for **Developer** VMs.</span></span>
   > [!NOTE]
   > <span data-ttu-id="0b0ac-171">1 つのビルド VM および 1 つの開発者向け VM のみを展開することができます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-171">You can only deploy one Build VM and one Developer VM.</span></span> <span data-ttu-id="0b0ac-172">開発者 VM を導入しない場合、インスタンスの数をゼロに設定します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-172">If you don’t want to deploy a Developer VM, then set instances count to zero.</span></span> 

   <span data-ttu-id="0b0ac-173">複数の開発者 VM が必要な場合、開発者 VM ごとに新しい環境を展開します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-173">If you want multiple Developer VMs then deploy new environment per developer VM.</span></span>

   <span data-ttu-id="0b0ac-174">[![配置](./media/deploy-1024x669.jpg)](./media/deploy.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-174">[![Deploy](./media/deploy-1024x669.jpg)](./media/deploy.jpg)</span></span>

6. <span data-ttu-id="0b0ac-175">**詳細設定**をクリックし、**Visual Studio Team Services** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-175">Click **Advanced settings**, select **Visual Studio Team Services**</span></span>
   1.  <span data-ttu-id="0b0ac-176">ビルド エージェント名: VSTS ビルド エージェントのフレンドリ名</span><span class="sxs-lookup"><span data-stu-id="0b0ac-176">Build Agent Name: Friendly name for build agent on VSTS</span></span>
   2.  <span data-ttu-id="0b0ac-177">ビルド エージェント プール: ビルド マシンの配置に使用するビルド エージェント プール名を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-177">Build Agent Pool: specify build agent pool name which should be used for build machine deployment.</span></span> <span data-ttu-id="0b0ac-178">VSTS に少なくとも 1 つのエージェント プールが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-178">Make sure VSTS contains at least one agent pool.</span></span> <span data-ttu-id="0b0ac-179">既定では、既定のプールがあります。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-179">By default, there will be the default pool.</span></span> <span data-ttu-id="0b0ac-180">既定のプールを削除した場合は、ビルド配置は失敗します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-180">If you have deleted the default pool then build deployment will fail.</span></span>
   3.  <span data-ttu-id="0b0ac-181">分岐名: ビルド VM の既定のソース コード同期場所になる VSTS ソース コード ブランチを指定します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-181">Branch Name: Specify your VSTS source code branch which will be default source code sync location for the build VM.</span></span> <span data-ttu-id="0b0ac-182">既定の分岐は、「メイン」です。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-182">Default branch is "Main".</span></span>

   ![設定](media/settings.jpg)

7. <span data-ttu-id="0b0ac-184">設定が確認されたら、**次へ**をクリックして展開を開始します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-184">After the settings are verified, click **Next** to start the deployment.</span></span> <span data-ttu-id="0b0ac-185">展開の進捗状況は **環境** の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-185">You can see progress of deployment under **Environments**.</span></span>
8. <span data-ttu-id="0b0ac-186">配置が完了したら、リモート デスクトップを使用して、開発者とビルド VMを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-186">After the deployment is complete, you can use Remote Desktop to view Developer and Build VM.</span></span>

## <a name="use-a-developer-vm-environment"></a><span data-ttu-id="0b0ac-187">開発者 VM 環境の使用</span><span class="sxs-lookup"><span data-stu-id="0b0ac-187">Use a Developer VM environment</span></span>
<span data-ttu-id="0b0ac-188">開発者 VM が配置されると、ソース管理 (VSTS) からのコードの同期に使用されるワークスペースで開発者 VM が自動構成されます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-188">When a Developer VM gets deployed, it’s auto-configured with a workspace that will be used to synchronize your code from source control (VSTS).</span></span> <span data-ttu-id="0b0ac-189">この開発者 VM には Microsoft Dynamics 365 for Finance and Operations が配置されているため、テスト VM として使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-189">As this Developer VM has Microsoft Dynamics 365 for Finance and Operations deployed on it, it can also be used as a test VM.</span></span>

### <a name="configure-visual-studio-to-connect-to-vsts"></a><span data-ttu-id="0b0ac-190">VSTS に接続するように Visual Studio をコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="0b0ac-190">Configure Visual Studio to connect to VSTS</span></span>

<span data-ttu-id="0b0ac-191">開発者 VM で初めて Visual Studio を開くときは、自分の資格情報を使用して VSTS に接続します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-191">When you open Visual Studio the first time on a Developer VM, connect to VSTS using your credentials.</span></span>

1.  <span data-ttu-id="0b0ac-192">**チーム エクスプローラー**を開き、**チーム プロジェクトの選択**を開きます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-192">Open **Team explorer** and click **Select Team projects**.</span></span>
2.  <span data-ttu-id="0b0ac-193">VSTS URL を入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-193">Enter the VSTS URL and click **OK**.</span></span> <span data-ttu-id="0b0ac-194">VSTS ユーザー名とパスワードを求められます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-194">You will be prompted for your VSTS username and password.</span></span>
3.  <span data-ttu-id="0b0ac-195">VSTS にログインした後、開発に使用する**既定のワークスペース**。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-195">After you are logged into the VSTS, your **Default workspace** that you will use for your development.</span></span>

    ![ワークスペースの管理](media/manage-workspaces.png)

## <a name="test-integration-with-the-build"></a><span data-ttu-id="0b0ac-197">ビルドとのテスト統合</span><span class="sxs-lookup"><span data-stu-id="0b0ac-197">Test integration with the build</span></span>
<span data-ttu-id="0b0ac-198">テストと検証のためのビルド プロセスの一部としてテストを統合するには、2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-198">There are two ways to integrate test as part of build process for testing and validation:</span></span>

-   <span data-ttu-id="0b0ac-199">単位とコンポーネントのレベル テストに基づく SysTest フレームワーク。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-199">SysTest framework based unit and component level tests.</span></span>
-   <span data-ttu-id="0b0ac-200">自動化されたテストの実行の XML を記録するタスク レコーダーから、コードを生成します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-200">Generate code from Task Recorder recording XML for automated test execution.</span></span>

<span data-ttu-id="0b0ac-201">これら 2 つの方法の詳細については、[テストと検証](testing-validation.md) を参照してください。テストおよび検証の戦略についてはこの記事を確認してください。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-201">The details of these two approaches are mentioned in the [Testing and validation. ](testing-validation.md)Review this article for testing and validation strategy.</span></span>

## <a name="use-the-build-vm-environment"></a><span data-ttu-id="0b0ac-202">ビルド VM 環境の使用</span><span class="sxs-lookup"><span data-stu-id="0b0ac-202">Use the Build VM environment</span></span>
<span data-ttu-id="0b0ac-203">LCS を通じて開発者トポロジにビルド VM が配置されると、それは事前に構成され、ビルドを開始する準備ができます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-203">When a Build VM is deployed in Developer topology through LCS, it is pre-configured and ready to start a build.</span></span> <span data-ttu-id="0b0ac-204">Visual Studio IDE または VSTS インターフェイスから、いつでも既定の構成を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-204">You can change the default configuration at any time from the Visual Studio IDE or the VSTS interface.</span></span> <span data-ttu-id="0b0ac-205">ビルド VM では、簡単なビルドのセットアップのために、モジュール ソース コードがビルド コンピューターに同期されます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-205">On a Build VM, the module source code is synchronized to the build machine for easy build setup.</span></span> <span data-ttu-id="0b0ac-206">ビルド マシンは、ビルド エージェント、ビルド コントローラー、ビルド プロセス テンプレート、ビルド定義のデフォルト設定で自動構成されています。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-206">The build machine is also auto-configured with default settings for build agent, build controller, build process template, and build definition.</span></span> <span data-ttu-id="0b0ac-207">ビルドに成功したら、ビルド定義と統合されているテストが実行されます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-207">Tests that are integrated with build definition are executed after the build is successful.</span></span>

### <a name="review-a-pre-configured-customizable-build-environment"></a><span data-ttu-id="0b0ac-208">定義済みのカスタマイズ可能なビルド環境を確認</span><span class="sxs-lookup"><span data-stu-id="0b0ac-208">Review a pre-configured customizable build environment</span></span>

<span data-ttu-id="0b0ac-209">ビルド VM には、TFS 2015 の一部としてリリースされた vNext ビルド エージェントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-209">The build VM contains the vNext build agent which was released as part of TFS 2015.</span></span> <span data-ttu-id="0b0ac-210">ビルド VM を配置するときは、既定では VSTS プロジェクトと接続して同期するようにビルド エージェントが構成されます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-210">When you deploy the Build VM, the build agent is configured by default to connect and sync with the VSTS project.</span></span> <span data-ttu-id="0b0ac-211">ビルド VM 構成の一部として、以下に示すようにデフォルトのビルド定義も作成および構成されます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-211">As a part of the Build VM configuration, the default build definition is also created and configured, as shown below.</span></span> 

<span data-ttu-id="0b0ac-212">[![Build1](./media/build1-1024x488.jpg)](./media/build1.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-212">[![Build1](./media/build1-1024x488.jpg)](./media/build1.jpg)</span></span> 

<span data-ttu-id="0b0ac-213">既定のビルド定義には、以下で説明するように、特定の操作を実行する複数のタスクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-213">Default build definition contains multiple tasks to perform specific operation, as described below.</span></span>

1.  <span data-ttu-id="0b0ac-214">ビルドに渡す事前定義済の変数パラメータをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-214">Configure the predefined variables parameters that will be passed to the build.</span></span> <span data-ttu-id="0b0ac-215">ビルド実行ごとにクリーンなデータベースを設定するには、**DatabaseBackupToRestore**変数のデータベース バックアップ ファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-215">To set up a clean database for every build execution, provide the name of the database backup file for the **DatabaseBackupToRestore** variable.</span></span> <span data-ttu-id="0b0ac-216">パッケージ フォルダーは、すべてのビルド時にクリーン パッケージ フォルダーのコピーで復元されます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-216">The packages folder is restored at every build with a copy of a clean package folder.</span></span>

    <span data-ttu-id="0b0ac-217">[![build2](./media/build2-1024x678.jpg)](./media/build2.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-217">[![build2](./media/build2-1024x678.jpg)](./media/build2.jpg)</span></span>

2.  <span data-ttu-id="0b0ac-218">以下のように、「トランク/メイン」ブランチにあるすべてのモジュールを検出して構築するためにソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-218">Build the solution to discover and build all modules under "Trunk/Main" branch as shown below.</span></span>

    <span data-ttu-id="0b0ac-219">[![Build3](./media/build3-1024x456.jpg)](./media/build3.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-219">[![Build3](./media/build3-1024x456.jpg)](./media/build3.jpg)</span></span>

3.  <span data-ttu-id="0b0ac-220">「レポートの展開」タスクを使用して、レポートを生成し、ビルド VM に展開します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-220">Use "Deploy Report" task to generate reports and deploy on build VM.</span></span>
4.  <span data-ttu-id="0b0ac-221">「データベース同期」タスクを使用して、データベースをビルド VM 上のローカル SQL に同期させます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-221">Use "Database Sync" task to synchronize the database to local SQL on build VM.</span></span>
5.  <span data-ttu-id="0b0ac-222">ビルドが成功した後、サンドボックス/ステージング環境を更新するために使用できる配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-222">After the build is successful, create a deployable package that can be used to update sandbox/ staging environment.</span></span>

    <span data-ttu-id="0b0ac-223">[![Build4](./media/build4-1024x462.jpg)](./media/build4.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-223">[![Build4](./media/build4-1024x462.jpg)](./media/build4.jpg)</span></span>

6.  <span data-ttu-id="0b0ac-224">「ビルド コンポーネントのコピーと発行」は、配置可能パッケージを VSTS コンポーネントの場所にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-224">"Copy and publish build artifacts" uploads the deployable package to VSTS artifacts location.</span></span>

    <span data-ttu-id="0b0ac-225">[![build5](./media/build5-1024x439.jpg)](./media/build5.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-225">[![build5](./media/build5-1024x439.jpg)](./media/build5.jpg)</span></span>

7.  <span data-ttu-id="0b0ac-226">テストの実行については、3 つの既定のタスク「テスト設定」、「テストの実行」、および「テストの終了」があります。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-226">For test execution, there are three default tasks "Test Setup", "Execute Test" and "Test End".</span></span>

    <span data-ttu-id="0b0ac-227">[![build7](./media/build7-1024x457.jpg)](./media/build7.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-227">[![build7](./media/build7-1024x457.jpg)](./media/build7.jpg)</span></span>

8.  <span data-ttu-id="0b0ac-228">既定のビルドでは毎日午後 5 時に開始される予定です。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-228">The default build is scheduled to trigger start every day at 5 P.M.</span></span> <span data-ttu-id="0b0ac-229">チームの必要性に従って、各チェックインでトリガーを「継続」に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-229">You can change trigger as per your team's need to "Continuous" for each check-in.</span></span>

    <span data-ttu-id="0b0ac-230">[![build8](./media/build8-1024x491.jpg)](./media/build8.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-230">[![build8](./media/build8-1024x491.jpg)](./media/build8.jpg)</span></span>

<span data-ttu-id="0b0ac-231">既定の構成に変更を加えて、そのビルド VM がビルドをトリガーできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-231">You can make changes to the default configuration, and the build VM will be ready to trigger a build.</span></span>

## <a name="start-a-build-and-verify-the-build-and-test-execution-results"></a><span data-ttu-id="0b0ac-232">ビルドを開始し、ビルドとテストの実行結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-232">Start a build and verify the build and test execution results</span></span>
<span data-ttu-id="0b0ac-233">既定のビルド構成を確認した後は、Visual Studio IDE または VSTS Web インターフェイスからビルドを手動でトリガーできます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-233">After you review the default build configuration, you can manually trigger a build from Visual Studio IDE or VSTS web interface.</span></span>

1.  <span data-ttu-id="0b0ac-234">ブラウザーを開き、VSTS URL に接続します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-234">Open your browser and connect to the VSTS URL.</span></span>
2.  <span data-ttu-id="0b0ac-235">資格情報を使用してをログインします。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-235">Login using your credentials.</span></span>
3.  <span data-ttu-id="0b0ac-236">ホーム ページの**最近のプロジェクトとソリューション**で、プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-236">On the home page, under **Recent projects and solutions**, select a project.</span></span>
4.  <span data-ttu-id="0b0ac-237">上部リンク オプションから、**ビルド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-237">From top links options, select **BUILD**.</span></span>
5.  <span data-ttu-id="0b0ac-238">左側のパネルで、既定のビルド定義インスタンスを選択します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-238">On the left panel, select the default build definition instance.</span></span>
6.  <span data-ttu-id="0b0ac-239">右クリックし、**キュー ビルド** を選択して VSTS ソース管理に既にチェックインしているモジュールおよびテスト モジュールのビルドをトリガーします。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-239">Right-click and select **Queue Build** to trigger a build for your module and test module that is already checked into the VSTS source control.</span></span>

<span data-ttu-id="0b0ac-240">[![image045](./media/image045.png)](./media/image045.png)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-240">[![image045](./media/image045.png)](./media/image045.png)</span></span> 

<span data-ttu-id="0b0ac-241">次の例に示すように、ビルドの成功または失敗が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-241">Success or failure for the build will display, as shown by the following examples.</span></span> <span data-ttu-id="0b0ac-242">すべてのビルドを表示します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-242">View all builds.</span></span> 

<span data-ttu-id="0b0ac-243">[![build9](./media/build9-1024x443.jpg)](./media/build9.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-243">[![build9](./media/build9-1024x443.jpg)](./media/build9.jpg)</span></span> 

<span data-ttu-id="0b0ac-244">特定の完了したビルドとビューの成功/失敗の詳細を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-244">Select specific completed build and view success/ failure details.</span></span> 

<span data-ttu-id="0b0ac-245">[![build10](./media/build10-1024x446.jpg)](./media/build10.jpg) テストリンクをクリックして、テスト実行の失敗を視覚化します。</span><span class="sxs-lookup"><span data-stu-id="0b0ac-245">[![build10](./media/build10-1024x446.jpg)](./media/build10.jpg) Click on Test link to visualize test execution failure.</span></span> 

<span data-ttu-id="0b0ac-246">[![build11](./media/build11-1024x455.jpg)](./media/build11.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b0ac-246">[![build11](./media/build11-1024x455.jpg)](./media/build11.jpg)</span></span>
