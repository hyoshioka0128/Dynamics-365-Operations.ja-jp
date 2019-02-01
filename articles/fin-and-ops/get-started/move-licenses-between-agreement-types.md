---
title: "契約タイプ間でライセンスを移動する"
description: "このトピックでは、契約タイプの間のライセンスを移動する方法について説明します。"
author: ClaudiaBetz-Haubold
manager: AnnBe
ms.date: 06/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-05-30
ms.dyn365.ops.version: AX 7.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 5399ec3afd19fbb48ca9a2d7bdd7b4cafa62265d
ms.contentlocale: ja-jp
ms.lasthandoff: 12/18/2018

---

# <a name="move-licenses-between-agreement-types"></a><span data-ttu-id="c5892-103">契約タイプ間でライセンスを移動する</span><span class="sxs-lookup"><span data-stu-id="c5892-103">Move licenses between agreement types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5892-104">場合によっては、もともと Microsoft クラウド サービス プロバイダー (CSP) 契約を通じて定期売買を購入した顧客は、Microsoft Dynamics Lifecycle Services (LCS) 実装プロジェクトが作成された後に、Microsoft との Microsoft ボリューム ライセンス契約に変更することを決定します。</span><span class="sxs-lookup"><span data-stu-id="c5892-104">Sometimes, a customer who originally purchased subscriptions through a Microsoft Cloud Service Provider (CSP) agreement decides to change to a Microsoft Volume Licensing agreement with Microsoft after the Microsoft Dynamics Lifecycle Services (LCS) Implementation project has been created.</span></span> <span data-ttu-id="c5892-105">顧客は、本番稼働でプロジェクトが稼動した後でもこの変更を実行できます。</span><span class="sxs-lookup"><span data-stu-id="c5892-105">The customer can make this change even after the project has gone live in production.</span></span>

<span data-ttu-id="c5892-106">ごくまれに、もともと Microsoft とのボリューム ライセンス契約を通して定期売買を購入した顧客は CSP 契約への変更することを決めます。</span><span class="sxs-lookup"><span data-stu-id="c5892-106">Less often, a customer who originally purchased the subscriptions through a Volume Licensing agreement with Microsoft decides to change to a CSP agreement.</span></span> <span data-ttu-id="c5892-107">この場合、ボリューム ライセンス契約の更新日に合わせて変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5892-107">In this case, the change must align with the renewal date of the Volume Licensing agreement.</span></span>

<span data-ttu-id="c5892-108">契約の 1 つのタイプから別のタイプへの定期売買契約の移動のプロセスは、主に商業プロセスです。</span><span class="sxs-lookup"><span data-stu-id="c5892-108">The process of moving subscriptions from one type of agreement to another is primarily a commercial process.</span></span> <span data-ttu-id="c5892-109">LCS 実装プロジェクトの技術的影響は最小限に抑えられています。</span><span class="sxs-lookup"><span data-stu-id="c5892-109">The technical implications for the LCS Implementation project are minimal.</span></span>

> [!NOTE]
> <span data-ttu-id="c5892-110">契約タイプ間の定期売買の移動は、Azure Active Directory (Azure AD) テナントの移動と同じではありません。</span><span class="sxs-lookup"><span data-stu-id="c5892-110">The movement of subscriptions between agreement types isn't the same as the movement of an Azure Active Directory (Azure AD) tenant.</span></span> <span data-ttu-id="c5892-111">契約の契約上の変更により、Azure AD テナントを移動する必要がある場合は、[LCS 実装プロジェクトを別の Azure Active Directory テナントに移動する](move-lcs-implementation-project-tenant.md)に記載されているプロセスにも従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5892-111">If the contractual changes in the agreements require that an Azure AD tenant be moved, you must also follow the process that is described in [Move an LCS Implementation project to another Azure Active Directory Tenant](move-lcs-implementation-project-tenant.md).</span></span>

<span data-ttu-id="c5892-112">3 つの標準環境に付属している定期売買: 製造環境、レベル 2 スタンダード承認テスト環境、およびレベル 1 開発者環境。</span><span class="sxs-lookup"><span data-stu-id="c5892-112">Subscriptions come with three standard environments: one production environment, one Tier-2 Standard Acceptance Test environment, and one Tier-1 developer environment.</span></span> <span data-ttu-id="c5892-113">これらの環境は、契約タイプ間のサブスクリプションの移動の影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="c5892-113">These environments aren't affected by the movement of subscriptions between agreement types.</span></span> <span data-ttu-id="c5892-114">アクションは、顧客が追加アドオン環境を持っている場合にのみ、LCS で必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="c5892-114">Action might be required in LCS only if the customer has additional add-on environments.</span></span> <span data-ttu-id="c5892-115">この場合、アドオン環境に関連付けられているアクションには、パートナーまたは顧客リソースの側で最小限の作業量が必要になります。</span><span class="sxs-lookup"><span data-stu-id="c5892-115">In this case, action that is related to the add-on environments requires minimal effort on the part of partner or customer resources.</span></span> <span data-ttu-id="c5892-116">環境間でデータの移動を効率化するには、最適な順序を決定するために前もって計画を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5892-116">To streamline the movement of data between environments, you should plan in advance to determine the best sequence.</span></span>

## <a name="the-customer-has-only-default-environments"></a><span data-ttu-id="c5892-117">顧客には既定の環境のみがあります</span><span class="sxs-lookup"><span data-stu-id="c5892-117">The customer has only default environments</span></span>

<span data-ttu-id="c5892-118">顧客が Microsoft が管理するサブスクリプションに付属している 3 つの標準環境のみを持ち、元の CPS 契約またはボリューム ライセンス契約でアドオン環境を購入していない場合、必要な活動は純粋に商業的なものです。</span><span class="sxs-lookup"><span data-stu-id="c5892-118">If the customer has only the three standard environments that come with the Microsoft-managed subscription, and didn't purchase any add-on environments through the original CSP agreement or Volume Licensing agreement, the activities that are required are purely commercial.</span></span>

1. <span data-ttu-id="c5892-119">顧客は、ボリューム ライセンスの再販業者または CSP との新しい契約の下で定期売買を注文します。</span><span class="sxs-lookup"><span data-stu-id="c5892-119">The customer places the order for subscriptions under the new agreement with the Volume Licensing reseller or the CSP.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="c5892-120">元の契約で使用される同じ Azure AD テナントに対して定期売買が購入されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c5892-120">Make sure that the subscriptions are purchased against the same Azure AD tenant that is used on the original agreement.</span></span>

2. <span data-ttu-id="c5892-121">顧客によって定期売買が有効化されます。</span><span class="sxs-lookup"><span data-stu-id="c5892-121">The customer activates the subscriptions.</span></span>
3. <span data-ttu-id="c5892-122">Microsoft Office 365 管理センターで、顧客は新規と定期売買の両方および既存の定期売買が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c5892-122">In Microsoft Office 365 Admin center, the customer verifies that both the new and subscriptions and the existing subscriptions are active.</span></span>
4. <span data-ttu-id="c5892-123">新しいサブスクリプションが有効になると、顧客は、ボリューム ライセンスの再販業者または CSP が既存のサブスクリプションを中断することを要求します。</span><span class="sxs-lookup"><span data-stu-id="c5892-123">When the new subscriptions are active, the customer requests that the Volume Licensing reseller or the CSP suspend the existing subscriptions.</span></span> <span data-ttu-id="c5892-124">通常、継続性を保証し、サービスの中断を回避するために重複があります。</span><span class="sxs-lookup"><span data-stu-id="c5892-124">Typically, there is an overlap to help guarantee continuity and avoid disruption of service.</span></span>

## <a name="the-customer-has-add-on-environments"></a><span data-ttu-id="c5892-125">顧客にはアドオン環境があります</span><span class="sxs-lookup"><span data-stu-id="c5892-125">The customer has add-on environments</span></span>

<span data-ttu-id="c5892-126">顧客が、元の CSP 契約またはボリューム ライセンス契約を通じてアドオン環境を購入した場合、それらの環境を再配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5892-126">If the customer purchased add-on environments through the original CSP agreement or Volume Licensing agreement, those environments must be redeployed.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c5892-127">前提条件</span><span class="sxs-lookup"><span data-stu-id="c5892-127">Prerequisites</span></span>

<span data-ttu-id="c5892-128">移動を開始する前に、次のタスクを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5892-128">Before you begin the move, you must complete the following tasks:</span></span>

- <span data-ttu-id="c5892-129">既存の環境からデータを保存します。</span><span class="sxs-lookup"><span data-stu-id="c5892-129">Save the data from your existing environments.</span></span>

    - <span data-ttu-id="c5892-130">**Microsoft SQL Server に基づくレベル 1 環境データベース:** データベースのバックアップを作成します。</span><span class="sxs-lookup"><span data-stu-id="c5892-130">**Tier 1 environment database that is based on Microsoft SQL Server:** Make a backup of the database.</span></span>
    - <span data-ttu-id="c5892-131">**Azure SQL データベースに基づくレベル 2 およびそれ以上の環境:** 次のオプションのいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="c5892-131">**Tier 2 and higher environments that are based on Azure SQL Database:** Use one of the following options:</span></span>

        - <span data-ttu-id="c5892-132">**オプション 1:** [Azure SQL データベースから SQL Server 環境に Finance and Operations データベースをコピー](../../dev-itpro/database/copy-database-from-azure-sql-to-sql-server.md)に記載されている手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c5892-132">**Option 1:** Follow the process that is described in [Copy a Finance and Operations database from Azure SQL Database to a SQL Server environment](../../dev-itpro/database/copy-database-from-azure-sql-to-sql-server.md).</span></span>
        - <span data-ttu-id="c5892-133">**オプション 2:** Azure サブスクリプションを持っている場合、サブスクリプションの下に Azure SQL データベースのコピーを保存してください。</span><span class="sxs-lookup"><span data-stu-id="c5892-133">**Option 2:** If you have an Azure subscription, save a copy of the Azure SQL database under that subscription.</span></span>
        - <span data-ttu-id="c5892-134">**オプション 3:** Azure SQL データベース環境を複数持ってる場合、1 つの環境を再配置し、古い環境をデータ センターに残してから、環境間でデータベース更新の要求をします。</span><span class="sxs-lookup"><span data-stu-id="c5892-134">**Option 3:** If you have multiple Azure SQL database environments, redeploy one environment, leave the remaining environments in the old data center, and then request a database refresh between the environments.</span></span>
        - <span data-ttu-id="c5892-135">**オプション 4:** データ パッケージとしてデータを保存し、再配置が完了した後にパッケージをインポートします。</span><span class="sxs-lookup"><span data-stu-id="c5892-135">**Option 4:** Save data as data packages, and then import the packages after the redeployment is completed.</span></span>

- <span data-ttu-id="c5892-136">コードのすべてのパッケージが LCS で共有アセット ライブラリにアップロードされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c5892-136">Verify that all code packages have been uploaded to the Shared asset library in LCS.</span></span>

### <a name="commercial-activities"></a><span data-ttu-id="c5892-137">商業活動</span><span class="sxs-lookup"><span data-stu-id="c5892-137">Commercial activities</span></span>

1. <span data-ttu-id="c5892-138">顧客は、ボリューム ライセンスの再販業者または CSP との新しい契約の下で定期売買を注文します。</span><span class="sxs-lookup"><span data-stu-id="c5892-138">The customer places the order for the subscriptions under the new agreement with the Volume Licensing reseller or the CSP.</span></span> <span data-ttu-id="c5892-139">これらのサブスクリプションには、アドオン環境のサブスクリプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c5892-139">These subscriptions include the subscriptions for the add-on environments.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="c5892-140">既存の Azure AD テナントに対して定期売買が購入されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c5892-140">Make sure that the subscriptions are purchased against the existing Azure AD tenant.</span></span>

2. <span data-ttu-id="c5892-141">顧客によって定期売買が有効化されます。</span><span class="sxs-lookup"><span data-stu-id="c5892-141">The customer activates the subscriptions.</span></span>
3. <span data-ttu-id="c5892-142">Office 365 管理センターで、顧客は新規の定期売買および既存の定期売買の両方が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c5892-142">In Office 365 Admin center, the customer verifies that both the new subscriptions and the existing subscriptions are active.</span></span>

### <a name="deploy-new-environments"></a><span data-ttu-id="c5892-143">新しい環境の配置</span><span class="sxs-lookup"><span data-stu-id="c5892-143">Deploy new environments</span></span>

1. <span data-ttu-id="c5892-144">新しいサブスクリプションが有効になると、コンフィグレーション可能な追加のアドオン環境が LCS に表示されます。</span><span class="sxs-lookup"><span data-stu-id="c5892-144">When the new subscriptions are active, additional add-on environments that you can configure appear in LCS.</span></span> <span data-ttu-id="c5892-145">アドオン環境を配置し、適切に構成します。</span><span class="sxs-lookup"><span data-stu-id="c5892-145">Deploy the add-on environments, and configure them as appropriate.</span></span>
2. <span data-ttu-id="c5892-146">配置可能なパッケージを適用して、データを復元します。</span><span class="sxs-lookup"><span data-stu-id="c5892-146">Apply the deployable packages, and restore the data.</span></span>

### <a name="delete-environments-under-the-obsolete-agreement"></a><span data-ttu-id="c5892-147">廃止された契約下の環境の削除</span><span class="sxs-lookup"><span data-stu-id="c5892-147">Delete environments under the obsolete agreement</span></span>

<span data-ttu-id="c5892-148">古い契約下で配置されたすべての環境で、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c5892-148">Follow these steps for every environment that was deployed under the old agreement.</span></span> <span data-ttu-id="c5892-149">環境を削除した後、再び使用したり再配置したりしないでください。</span><span class="sxs-lookup"><span data-stu-id="c5892-149">After you've deleted the environments, don't use or redeploy them again.</span></span>

1. <span data-ttu-id="c5892-150">LCS の、**環境の詳細**ページで、**完全な詳細**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5892-150">In LCS, on the **Environment details** page, select **Full details**.</span></span>
2. <span data-ttu-id="c5892-151">環境を停止してから、環境が停止した時に、**割り当て解除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5892-151">Stop the environment, and when the environment has stopped, select **Deallocate**.</span></span>
3. <span data-ttu-id="c5892-152">割り当て解除が完了したとき、**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5892-152">When the deallocation is completed, select **Delete**.</span></span>
4. <span data-ttu-id="c5892-153">環境が削除されたら、**コンフィグレーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5892-153">When the environment has been deleted, select **Configure**.</span></span>

### <a name="update-environments"></a><span data-ttu-id="c5892-154">環境の更新</span><span class="sxs-lookup"><span data-stu-id="c5892-154">Update environments</span></span>

1. <span data-ttu-id="c5892-155">ボリューム ライセンスの再販業者または CSP は、既存の定期売買を中断します。</span><span class="sxs-lookup"><span data-stu-id="c5892-155">The Volume Licensing reseller or the CSP suspends the existing subscriptions.</span></span>
2. <span data-ttu-id="c5892-156">元のアドオン環境は、LCS に表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="c5892-156">Any original add-on environments no longer appear in LCS.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5892-157">アドオン環境の物理的な再配置が完了するまでは、有効な状態にで既存の定期売買と新しい定期売買の両方をアクティブな状態に保つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5892-157">Until physical redeployment of the add-on environments is completed, both existing subscriptions and new subscriptions must be kept in an active state.</span></span>

> [!NOTE]
> - <span data-ttu-id="c5892-158">サンド ボックス環境では、Azure BLOB ストレージに格納されているファイルの移動はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c5892-158">The movement of files that are stored in Azure Blob storage isn't supported in sandbox environments.</span></span>
> - <span data-ttu-id="c5892-159">小売顧客は、移動後に小売コンポーネントが正常に機能するため追加の手順が必要であることに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5892-159">Retail customers should be aware that extra steps are required in order for Retail components to work correctly after the move.</span></span> <span data-ttu-id="c5892-160">詳細については、[データ管理](../../dev-itpro/data-entities/data-entities-data-packages.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c5892-160">For more information, see [Data management](../../dev-itpro/data-entities/data-entities-data-packages.md).</span></span>
