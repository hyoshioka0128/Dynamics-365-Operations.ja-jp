---
title: "仕入先コラボレーションの設定と管理"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations においてベンダー コラボレーションをセットアップする方法について説明します。 また、新しい仕入先コラボレーション ユーザーのプロビジョニング方法およびそれらのユーザーのセキュリティ ロールの管理方法についても説明します。"
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirExternalRole, SysUserRequestListPage, VendVendorPortalUsers, WorkflowTableListPageRnr
audience: IT Pro
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 220774
ms.assetid: 69d05e8b-7dc2-48ea-bc24-bea9ac963579
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: c4cb46ea351fb12ec93169789546911c7859793a
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---
<span data-ttu-id="54df4-104">.md</span><span class="sxs-lookup"><span data-stu-id="54df4-104">.md</span></span>
# <a name="set-up-and-maintain-vendor-collaboration"></a><span data-ttu-id="54df4-105">仕入先コラボレーションの設定と管理</span><span class="sxs-lookup"><span data-stu-id="54df4-105">Set up and maintain vendor collaboration</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="54df4-106">仕入先コラボレーション インターフェイスは、発注書、請求書、委託販売在庫に関する限られた情報を外部仕入先ユーザーに公開します。</span><span class="sxs-lookup"><span data-stu-id="54df4-106">The vendor collaboration interface exposes a limited set of information about purchase orders, invoices, and consignment stock to external vendor users.</span></span> <span data-ttu-id="54df4-107">このインターフェイスから、仕入先も見積依頼 (RFQ) に返信でき、会社の基本情報を表示および編集できます。</span><span class="sxs-lookup"><span data-stu-id="54df4-107">From this interface, a vendor can also reply to requests for quotation (RFQs), and view and edit basic company information.</span></span>

<span data-ttu-id="54df4-108">このトピックでは、Microsoft Dynamics 365 for Finance and Operations においてベンダー コラボレーションをセットアップする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="54df4-108">This topic explains how to set up vendor collaboration in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="54df4-109">また、新しい仕入先コラボレーション ユーザーをプロビジョニングするワークフローの設定方法およびそれらのユーザーのセキュリティ ロールの管理方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="54df4-109">It also explains how to set up a workflow to provision new vendor collaboration users, and how to manage the security roles for those users.</span></span>

> [!NOTE]
> <span data-ttu-id="54df4-110">仕入先コラボレーションのセキュリティ ロールの設定に関する情報は、Finance and Operations の現在のバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="54df4-110">The information about the setup of security roles for vendor collaboration applies only to the current version of Finance and Operations.</span></span> <span data-ttu-id="54df4-111">Microsoft Dynamics AX 7.0 (2016 年 2 月) および Microsoft Dynamics AX アプリケーション バージョン 7.0.1 (2016 年 5 月) で、**仕入先ポータル** モジュールを使用して仕入先との共同作業を行います。</span><span class="sxs-lookup"><span data-stu-id="54df4-111">In Microsoft Dynamics AX 7.0 (February 2016) and Microsoft Dynamics AX application version 7.0.1 (May 2016), you collaborate with vendors by using the **Vendor portal** module.</span></span> <span data-ttu-id="54df4-112">Microsoft Dynamics AX で仕入先ポータルのユーザーのアクセス許可の詳細については、[仕入先ポータルのユーザー セキュリティ](configure-security-vendor-portal-users.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54df4-112">For information about user permissions for the Vendor portal in Microsoft Dynamics AX, see [Vendor portal user security](configure-security-vendor-portal-users.md).</span></span>

## <a name="set-up-vendor-collaboration-security-roles"></a><span data-ttu-id="54df4-113">仕入先コラボレーション セキュリティ ロールの設定</span><span class="sxs-lookup"><span data-stu-id="54df4-113">Set up vendor collaboration security roles</span></span>

<span data-ttu-id="54df4-114">調達担当者または十分なアクセス許可を持つ仕入先は、連絡担当者レコードの**仕入先ユーザーのプロビジョニング**を有効にすることによって、連絡担当者をユーザーとしてプロビジョニングするように要求できます。</span><span class="sxs-lookup"><span data-stu-id="54df4-114">A procurement professional or a vendor that has enough permissions can request that a contact person be provisioned as a user by enabling **Provision vendor user** on the contact person record.</span></span> <span data-ttu-id="54df4-115">プロセスのプロビジョニング中に、新しい外部ユーザーに対してユーザーのアクセス許可が選択され、新しい仕入先ユーザーの要求が送信されます。</span><span class="sxs-lookup"><span data-stu-id="54df4-115">During the provisioning process, user permissions are selected for the new external user, and the new vendor user request is submitted.</span></span> <span data-ttu-id="54df4-116">仕入先ユーザーの要求での選択に使用できるユーザーのアクセス許可を正しく設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54df4-116">It's important that you correctly set up the user permissions that are available for selection in the vendor user request.</span></span> <span data-ttu-id="54df4-117">それ以外の場合、仕入先には、Finance and Operations にアクセスできない情報へのアクセスが許可される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="54df4-117">Otherwise, vendors might be granted access to information that they should not have access to in Finance and Operations.</span></span>

### <a name="set-up-the-security-roles-that-are-available-for-selection-when-a-new-user-request-is-used-for-a-contact-person"></a><span data-ttu-id="54df4-118">連絡担当者に新しいユーザー要求が使用される場合に選択に使用できるセキュリティ ロールを設定</span><span class="sxs-lookup"><span data-stu-id="54df4-118">Set up the security roles that are available for selection when a new user request is used for a contact person</span></span>

1. <span data-ttu-id="54df4-119">**システム管理** &gt; **セキュリティ** &gt; **外部ロール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54df4-119">Select **System administration** &gt; **Security** &gt; **External roles**.</span></span>
2. <span data-ttu-id="54df4-120">**新規** を選択してセキュリティ ロールと **仕入先** 関係者ロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="54df4-120">Select **New**, and then select a security role and the **Vendor** party role.</span></span>

<span data-ttu-id="54df4-121">Finance and Operations で提供される **仕入先管理者 (外部)** および **仕入先 (外部)** を追加する場合があります。</span><span class="sxs-lookup"><span data-stu-id="54df4-121">You might want to add the **Vendor admin (external)** and **Vendor (external)** roles that are provided in Finance and Operations.</span></span> <span data-ttu-id="54df4-122">または、会社が作成したセキュリティ ロールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="54df4-122">Alternatively, you can use security roles that your company has created.</span></span>

<span data-ttu-id="54df4-123">仕入先が新しい連絡先を作成でき、新規ユーザーとユーザー情報の変更に関してユーザーが要求する仕入先コラボレーションを送信でき、ワークフローを通じてそのような要求に対応できる場合にのみ、**仕入先管理者 (外部)** ロールを有効にしてください。</span><span class="sxs-lookup"><span data-stu-id="54df4-123">You should make the **Vendor admin (external)** role available only if vendors should be able to create new contacts, submit vendor collaboration user requests for new users and changes to user information, and handle those requests via a workflow.</span></span>

<span data-ttu-id="54df4-124">仕入先の連絡先とユーザーを手動で設定する場合は、**仕入先 (外部) ロール**のみを利用可能にすることができます。</span><span class="sxs-lookup"><span data-stu-id="54df4-124">If you plan to manually set up vendor contacts and users, you can make just the **Vendor (external) role** available.</span></span> <span data-ttu-id="54df4-125">このロールは、仕入先のユーザー要求によって要求できる唯一のロールになります。</span><span class="sxs-lookup"><span data-stu-id="54df4-125">This role will then be the only role that can be requested through a vendor user request.</span></span>

> [!NOTE]
> <span data-ttu-id="54df4-126">Finance and Operations で新しいユーザー アカウントを手動で作成するとき、**SystemUser** ロールが自動的に付与されます。</span><span class="sxs-lookup"><span data-stu-id="54df4-126">The **SystemUser** role is automatically granted when you manually create a new user account in Finance and Operations.</span></span> <span data-ttu-id="54df4-127">したがって、そのロールを削除して **SystemExternalUser** ロールを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="54df4-127">Therefore, you must remove that role and assign the **SystemExternalUser** role.</span></span> <span data-ttu-id="54df4-128">仕入先ユーザー要求によって開始されるワークフロー経由で新しいユーザー アカウントを作成した場合、共同作業に対して設定した 1 つ以上の仕入先のロールおよび **SystemExternalUser** ロールが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="54df4-128">If new user accounts are created via the workflow that is initiated by a vendor user request to provision a new user, one or more of the roles that you've set up for vendor collaboration and the **SystemExternalUser** role will be assigned.</span></span>

#### <a name="vendor-admin-external-security-role"></a><span data-ttu-id="54df4-129">仕入先管理者 (外部) のセキュリティ ポリシー</span><span class="sxs-lookup"><span data-stu-id="54df4-129">Vendor admin (external) security role</span></span>

<span data-ttu-id="54df4-130">**仕入先管理者 (外部)** ロールは、仕入先の連絡先情報を管理し、新しい仕入先の共同作業ユーザーのプロビジョニング要求を行う外部仕入先に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="54df4-130">The **Vendor admin (external)** role can be used for external vendors that maintain vendor contact information and make requests to provision new vendor collaboration users.</span></span> <span data-ttu-id="54df4-131">このセキュリティ ロールを持つ外部ユーザーは、次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="54df4-131">External users who have this security role can perform the following tasks:</span></span>

- <span data-ttu-id="54df4-132">個人のタイトル、電子メール アドレス、および電話番号などの連絡担当者の情報を表示および変更します。</span><span class="sxs-lookup"><span data-stu-id="54df4-132">View and modify contact person information, such as the person's title, email address, and telephone number.</span></span>
- <span data-ttu-id="54df4-133">連絡先となっている仕入先勘定に新規または既存の連絡担当者を追加します。</span><span class="sxs-lookup"><span data-stu-id="54df4-133">Add a new or existing contact person to the vendor accounts that they are a contact for.</span></span>
- <span data-ttu-id="54df4-134">作成した担当者を削除します。</span><span class="sxs-lookup"><span data-stu-id="54df4-134">Delete any contact person that they have created.</span></span>
- <span data-ttu-id="54df4-135">連絡担当者と仕入先勘定の関連付けを有効化または無効化します。</span><span class="sxs-lookup"><span data-stu-id="54df4-135">Activate or inactivate the association between a contact person and a vendor account.</span></span> <span data-ttu-id="54df4-136">連絡担当者と仕入先勘定の関連付けが無効にされた後、連絡担当者は新しい発注書またはその他のドキュメントで参照することはできません。</span><span class="sxs-lookup"><span data-stu-id="54df4-136">After the association between a contact person and a vendor account is inactivated, the contact person can't be referred to on new purchase orders or other documents.</span></span>
- <span data-ttu-id="54df4-137">仕入先に固有の仕入先コラボレーション インターフェイス上のドキュメントへの連絡担当者のアクセスを拒否または許可する。</span><span class="sxs-lookup"><span data-stu-id="54df4-137">Deny or allow a contact person's access to documents on the vendor collaboration interface that are specific to the vendor account.</span></span> <span data-ttu-id="54df4-138">連絡担当者と仕入先勘定の関連付けを無効化した後、仕入先勘定への固有のドキュメントのアクセスは、常に拒否されます。</span><span class="sxs-lookup"><span data-stu-id="54df4-138">After the association between a contact person and a vendor account is inactivated, access to documents that are specific to the vendor account is always denied.</span></span>
- <span data-ttu-id="54df4-139">**ユーザーのプロビジョニング** アクションを使用することで、連絡担当者の新しいユーザー アカウントをリクエストします。</span><span class="sxs-lookup"><span data-stu-id="54df4-139">Request a new user account for a contact person by using the **Provision user** action.</span></span>
- <span data-ttu-id="54df4-140">連絡担当者のユーザー アカウントを無効にすることを要求します。</span><span class="sxs-lookup"><span data-stu-id="54df4-140">Request that a contact person's user account be inactivated.</span></span>
- <span data-ttu-id="54df4-141">セキュリティ ロールを追加または削除するために連絡担当者のユーザー アカウントを変更することを要求します。</span><span class="sxs-lookup"><span data-stu-id="54df4-141">Request that a contact person's user account be modified to add or remove security roles.</span></span>
- <span data-ttu-id="54df4-142">RFQ を表示します。</span><span class="sxs-lookup"><span data-stu-id="54df4-142">View RFQs.</span></span>

#### <a name="vendor-external-security-role"></a><span data-ttu-id="54df4-143">仕入先 (外部) のセキュリティ ポリシー</span><span class="sxs-lookup"><span data-stu-id="54df4-143">Vendor (external) security role</span></span>

<span data-ttu-id="54df4-144">**仕入先 (外部) ロール**は、発注書を操作する外部仕入先に使用できます。</span><span class="sxs-lookup"><span data-stu-id="54df4-144">The **Vendor (external) role** can be used for external vendors that will work with purchase orders.</span></span> <span data-ttu-id="54df4-145">このセキュリティ ロールを持つ外部ユーザーは、次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="54df4-145">External users who have this security role can perform the following tasks:</span></span>

- <span data-ttu-id="54df4-146">発注書に関する情報に応答して表示します。</span><span class="sxs-lookup"><span data-stu-id="54df4-146">Respond to and view information about purchase orders.</span></span>
- <span data-ttu-id="54df4-147">仕入先コラボレーション請求書を管理します。</span><span class="sxs-lookup"><span data-stu-id="54df4-147">Maintain vendor collaboration invoices.</span></span>
- <span data-ttu-id="54df4-148">委託販売在庫を表示します。</span><span class="sxs-lookup"><span data-stu-id="54df4-148">View consignment inventory.</span></span>
- <span data-ttu-id="54df4-149">RFQ を表示し、それに対して回答します。</span><span class="sxs-lookup"><span data-stu-id="54df4-149">View and respond to RFQs.</span></span>
- <span data-ttu-id="54df4-150">仕入先情報を表示する。</span><span class="sxs-lookup"><span data-stu-id="54df4-150">View vendor information.</span></span>

## <a name="set-up-security-roles-that-are-used-when-prospective-vendors-are-onboarded"></a><span data-ttu-id="54df4-151">見込み仕入先がオンボーディングされたときに使用されるセキュリティ ロールの設定</span><span class="sxs-lookup"><span data-stu-id="54df4-151">Set up security roles that are used when prospective vendors are onboarded</span></span>

<span data-ttu-id="54df4-152">見込み仕入先の登録要求によって開始されるオンボードの仕入先には、外部のセキュリティ ロールを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54df4-152">To onboard vendors that are initiated via a prospective vendor registration request, you must set up an external security role.</span></span> <span data-ttu-id="54df4-153">このロールは、**ユーザー リクエスト ワークフロー (プラットフォーム)** タイプのワークフローによって制御されるプロビジョニングのプロセス中に新規ユーザーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="54df4-153">This rolle will be assigned to new users during the provisioning process that is controlled by the workflow of the **User request workflow (platform)** type.</span></span> <span data-ttu-id="54df4-154">詳細については、このトピックで後述の [仕入先コラボレーションのユーザー要求を処理するワークフローの設定](#Set-up-workflows-to-process-vendor-collaboration-user-requests) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54df4-154">For more information, see the [Set up workflows to process vendor collaboration user requests](#Set-up-workflows-to-process-vendor-collaboration-user-requests) section later in this topic.</span></span>

<span data-ttu-id="54df4-155">見込み仕入先のオンボードを行う方法の詳細については、[仕入先のオンボーディング](vendor-onboarding.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54df4-155">For information about how to onboard prospective vendors, see [Vendor onboarding](vendor-onboarding.md).</span></span>

### <a name="set-up-a-security-role-that-is-used-when-a-new-prospective-vendor-user-request-is-submitted"></a><span data-ttu-id="54df4-156">新しい見込み仕入先ユーザー要求が送信されたときに使用されるセキュリティ ロールの設定</span><span class="sxs-lookup"><span data-stu-id="54df4-156">Set up a security role that is used when a new prospective vendor user request is submitted</span></span>

1. <span data-ttu-id="54df4-157">**システム管理** > **セキュリティ** > **外部ロール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54df4-157">Select **System administration** > **Security** > **External roles**.</span></span>
2. <span data-ttu-id="54df4-158">**新規** を選択してセキュリティ ロールと **見込み仕入先** 関係者ロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="54df4-158">Select **New**, and then select a security role and the **Prospective vendor** party role.</span></span>

<span data-ttu-id="54df4-159">Finance and Operations で提供されている **仕入先見込顧客 (外部)** ロールを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54df4-159">You should add the **Vendor prospect (external)** role that is provided in Finance and Operations.</span></span>

<span data-ttu-id="54df4-160">セキュリティ ロールは、新しい仕入先登録ウィザードへのアクセスのみを許可します。</span><span class="sxs-lookup"><span data-stu-id="54df4-160">The security role will grant access only to the new vendor registration wizard.</span></span>

## <a name="set-up-workflows-to-process-vendor-collaboration-user-requests"></a><span data-ttu-id="54df4-161">仕入先コラボレーション ユーザーの要求を処理するワークフローの設定</span><span class="sxs-lookup"><span data-stu-id="54df4-161">Set up workflows to process vendor collaboration user requests</span></span>

<span data-ttu-id="54df4-162">関連するすべてのタスクが完了し、適切な承認が与えられることを保証するために、仕入先コラボレーション ユーザーの要求を処理するワークフローを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54df4-162">To help guarantee that all the relevant tasks are completed, and that the appropriate approvals are given, you must set up workflows to handle vendor collaboration user requests.</span></span>

<span data-ttu-id="54df4-163">仕入先コラボレーションのユーザー要求は、**仕入先管理者 (外部)** セキュリティ ロールまたは類似のアクセス許可を持つ外部仕入先か、自社の調達担当者が提出します。</span><span class="sxs-lookup"><span data-stu-id="54df4-163">Vendor collaboration user requests are submitted either by external vendors that have the **Vendor admin (external)** security role or similar permissions, or by procurement professionals in your company.</span></span> <span data-ttu-id="54df4-164">また、仕入先のオンボーディング プロセス中の仕入先登録要求から生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="54df4-164">They can also be generated from prospective vendor registration requests during the vendor onboarding process.</span></span>

<span data-ttu-id="54df4-165">リクエストには次の 3 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="54df4-165">There are three types of requests:</span></span>

- <span data-ttu-id="54df4-166">新しいユーザーをプロビジョニングする要求</span><span class="sxs-lookup"><span data-stu-id="54df4-166">Requests to provision a new user</span></span>
- <span data-ttu-id="54df4-167">既存ユーザーを無効にする要求</span><span class="sxs-lookup"><span data-stu-id="54df4-167">Requests to inactivate an existing user</span></span>
- <span data-ttu-id="54df4-168">既存のユーザーのセキュリティ ロールを変更する要求</span><span class="sxs-lookup"><span data-stu-id="54df4-168">Requests to modify the security roles of an existing user</span></span>

<span data-ttu-id="54df4-169">仕入先コラボレーション ユーザー要求の詳細については、「[仕入先コラボレーション ユーザーの管理](manage-vendor-collaboration-users.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54df4-169">For more information about vendor collaboration user requests, see [Manage vendor collaboration users](manage-vendor-collaboration-users.md).</span></span>

<span data-ttu-id="54df4-170">仕入先コラボレーション ユーザー要求の 3 つのタイプすべてを処理するには、2 つ以上のワークフローを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54df4-170">You must create two or more workflows to process all three types of vendor collaboration user requests.</span></span> <span data-ttu-id="54df4-171">新しいワークフローは、**ユーザー ワークフロー** ページで作成されます。</span><span class="sxs-lookup"><span data-stu-id="54df4-171">New workflows are created on the **User workflows** page.</span></span>

### <a name="example-of-a-workflow-for-provisioning-new-users-and-modifying-security-roles"></a><span data-ttu-id="54df4-172">新しいユーザーをプロビジョニングおよびセキュリティ ロールを変更するためのワークフロー例</span><span class="sxs-lookup"><span data-stu-id="54df4-172">Example of a workflow for provisioning new users and modifying security roles</span></span>

<span data-ttu-id="54df4-173">新しいユーザーを作成してセキュリティ ロールを変更する仕入先ユーザーの要求を処理するために、ワークフローの先頭に分岐条件を設定できます。</span><span class="sxs-lookup"><span data-stu-id="54df4-173">To handle vendor user requests to create new users and modify security roles, you can put a branching condition at the beginning of the workflow.</span></span> <span data-ttu-id="54df4-174">この方法では、要求が新しいユーザーの作成または既存のユーザーの変更であるかどうかに応じて、ワークフローの異なる分岐を使用します。</span><span class="sxs-lookup"><span data-stu-id="54df4-174">In this way, a different branch of the workflow is used, depending on whether the request is to create a new user or modify an existing user.</span></span>

<span data-ttu-id="54df4-175">この分岐を設定するには、**ユーザー要求ワークフロー (プラットフォーム)** タイプの新しいワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="54df4-175">To set up this branching, create a new workflow of the **User Request Workflow (Platform)** type.</span></span> <span data-ttu-id="54df4-176">このワークフローの分岐には、次の要素を含めることがあります。</span><span class="sxs-lookup"><span data-stu-id="54df4-176">The branches of this workflow might contain the following elements.</span></span>

#### <a name="branch-to-provision-new-users"></a><span data-ttu-id="54df4-177">新しいユーザーをプロビジョニングするための分岐</span><span class="sxs-lookup"><span data-stu-id="54df4-177">Branch to provision new users</span></span>

1. <span data-ttu-id="54df4-178">新しいユーザーに仕入先コラボレーション情報へのアクセスを許可することを承諾する担当者に、承認タスクを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="54df4-178">Assign an approval task to the person who is responsible for approving that new users should be granted access to vendor collaboration information.</span></span>
2. <span data-ttu-id="54df4-179">Azure ポータルで新しい Microsoft Azure Active Directory (Azure AD) ユーザー アカウントを要求する担当者にタスクを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="54df4-179">Assign a task to the person who is responsible for requesting new Microsoft Azure Active Directory (Azure AD) user accounts in Azure portal.</span></span> <span data-ttu-id="54df4-180">この手順では、事前に定義された **Azure B2B ユーザー招待状の送信**タスクを使用します。</span><span class="sxs-lookup"><span data-stu-id="54df4-180">Use the predefined **Send Azure B2B user invitation** task for this step.</span></span> <span data-ttu-id="54df4-181">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 では、B2B ユーザーを自動的に Azure AD にエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="54df4-181">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, B2B users can be automatically exported to Azure AD.</span></span> <span data-ttu-id="54df4-182">詳細については、[Azure AD に B2B ユーザーをエクスポート](../../dev-itpro/sysadmin/implement-b2b.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54df4-182">For more information, see [Export B2B users to Azure AD](../../dev-itpro/sysadmin/implement-b2b.md).</span></span>
3. <span data-ttu-id="54df4-183">承認タスクを Azure にアップロードするユーザーに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="54df4-183">Assign an approval task to the person who uploads to Azure.</span></span> <span data-ttu-id="54df4-184">勘定が正常に作成されていない場合、このユーザーはタスクを却下し、ワークフローを終了します。</span><span class="sxs-lookup"><span data-stu-id="54df4-184">If an account isn't successfully created, this person rejects the task and ends the workflow.</span></span> <span data-ttu-id="54df4-185">この承認タスクは、B2B アプリケーション プログラミング インターフェイス (API) を使用して Azure に新しいユーザー アカウントを自動的にエクスポートするステップを含めるとスキップできます。</span><span class="sxs-lookup"><span data-stu-id="54df4-185">This approval task can be skipped if you've included the step that automatically exports new user accounts to Azure via the B2B application programming interface (API).</span></span>
4. <span data-ttu-id="54df4-186">Finance and Operations で新しいユーザーをプロビジョニングする自動化タスクを追加します。</span><span class="sxs-lookup"><span data-stu-id="54df4-186">Add an automated task that provisions a new user in Finance and Operations.</span></span> <span data-ttu-id="54df4-187">この手順では、事前に定義された**ユーザーの自動プロビジョニング**タスクを使用します。</span><span class="sxs-lookup"><span data-stu-id="54df4-187">Use the predefined **Automated provision user** task for this step.</span></span>
5. <span data-ttu-id="54df4-188">新しいユーザーに通知するタスクを追加します。</span><span class="sxs-lookup"><span data-stu-id="54df4-188">Add a task that notifies the new user.</span></span> <span data-ttu-id="54df4-189">Finance and Operations の URL を含むようこそ電子メールを新しいユーザーに送信する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="54df4-189">You might want to send the new user a welcome email that includes a URL for Finance and Operations.</span></span> <span data-ttu-id="54df4-190">このメールでは、**電子メール メッセージ**ページで作成したテンプレートを使用して、**ユーザー ワークフロー パラメーター**ページを選択できます。</span><span class="sxs-lookup"><span data-stu-id="54df4-190">This email can use a template that you create on the **Email messages** page and then select on the **User workflow parameters** page.</span></span> <span data-ttu-id="54df4-191">テンプレートには、**%portal URL%** タグを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="54df4-191">The template can include the **%portal URL%** tag.</span></span> <span data-ttu-id="54df4-192">ようこそ電子メールが生成されると、このタグは Finance and Operations のテナントの URL に置き換わります。</span><span class="sxs-lookup"><span data-stu-id="54df4-192">When the welcome email is generated, this tag which will be replaced by the URL of the Finance and Operations tenant.</span></span>

    > [!NOTE]
    > <span data-ttu-id="54df4-193">このワークフローは、ユーザー オンボードを含む複数のシナリオで使用できます。</span><span class="sxs-lookup"><span data-stu-id="54df4-193">This workflow can be used in multiple scenarios that involve user onboarding.</span></span> <span data-ttu-id="54df4-194">たとえば、見込み仕入先または連絡担当者に仕入先コラボレーション アカウントを必要とする場合、使用できます。</span><span class="sxs-lookup"><span data-stu-id="54df4-194">For example, it can be used when prospective vendors or contact persons require a vendor collaboration account.</span></span> <span data-ttu-id="54df4-195">したがって、複数の目的に使用できる一般的なステートメントとしてメールを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54df4-195">Therefore, you should phrase the email as a general statement that can be used for multiple purposes.</span></span>

#### <a name="branch-to-modify-security-roles"></a><span data-ttu-id="54df4-196">セキュリティ ロールを変更するための分岐</span><span class="sxs-lookup"><span data-stu-id="54df4-196">Branch to modify security roles</span></span>

1. <span data-ttu-id="54df4-197">セキュリティ ロールへの変更を承諾する担当者に承認タスクを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="54df4-197">Assign an approval task to the person who is responsible for approving changes to security roles.</span></span>
2. <span data-ttu-id="54df4-198">関連するセキュリティ ロールを追加または削除する自動化タスクを追加します。</span><span class="sxs-lookup"><span data-stu-id="54df4-198">Add an automated task that adds or removes the relevant security roles.</span></span> <span data-ttu-id="54df4-199">この手順では、**ユーザーの自動プロビジョニング**タスクを使用します。</span><span class="sxs-lookup"><span data-stu-id="54df4-199">Use the **Automated provision user** task for this step.</span></span>

### <a name="example-of-a-workflow-for-inactivating-a-user"></a><span data-ttu-id="54df4-200">ユーザーを無効にする方法のワークフロー例</span><span class="sxs-lookup"><span data-stu-id="54df4-200">Example of a workflow for inactivating a user</span></span>

<span data-ttu-id="54df4-201">**ユーザー要求ワークフロー プラットフォームの無効化**タイプのワークフローを作成し、次のタスクを追加します。</span><span class="sxs-lookup"><span data-stu-id="54df4-201">Create a workflow of the **Inactivate user request workflow platform** type, and then add the following tasks.</span></span>

1. <span data-ttu-id="54df4-202">ユーザーを無効にする要求を承諾する担当者に承認タスクを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="54df4-202">Assign an approval task to the person who is responsible for accepting requests to inactivate users.</span></span> <span data-ttu-id="54df4-203">この承認ステップを自動化する条件を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="54df4-203">You can add conditions to automate this approval step.</span></span>
2. <span data-ttu-id="54df4-204">ユーザーを無効化する自動化タスクを追加します。</span><span class="sxs-lookup"><span data-stu-id="54df4-204">Add an automated task that inactivates the user.</span></span> <span data-ttu-id="54df4-205">この手順では、**ユーザーの自動無効化**タスクを使用します。</span><span class="sxs-lookup"><span data-stu-id="54df4-205">Use the **Automated user inactivation** task for this step.</span></span>
3. <span data-ttu-id="54df4-206">必要なクリーンアップ タスクを追加します。</span><span class="sxs-lookup"><span data-stu-id="54df4-206">Add any clean-up tasks that are required.</span></span> <span data-ttu-id="54df4-207">たとえば、Azure ポータルでディレクトリからアカウントを削除するタスクを追加できます。</span><span class="sxs-lookup"><span data-stu-id="54df4-207">For example, you can add a task that removes the account from your directory in Azure portal.</span></span>

## <a name="enable-vendor-collaboration-for-a-specific-vendor"></a><span data-ttu-id="54df4-208">特定仕入先の仕入先コラボレーションの有効化</span><span class="sxs-lookup"><span data-stu-id="54df4-208">Enable vendor collaboration for a specific vendor</span></span>

<span data-ttu-id="54df4-209">仕入先コラボレーションを使用するユーザー アカウントを作成する前に、仕入先コラボレーションを使用するための仕入先を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54df4-209">Before you create a user account for someone who will use vendor collaboration, you must set up the vendor so that it can use vendor collaboration.</span></span> <span data-ttu-id="54df4-210">**仕入先** ページの **一般** タブで、**コラボレーションの有効化** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="54df4-210">On the **Vendors** page, on the **General** tab, set the **Collaboration activation** field.</span></span> <span data-ttu-id="54df4-211"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="54df4-211">The following options are available:</span></span>

- <span data-ttu-id="54df4-212">**有効 (発注書は自動で確認されます)** - 仕入先が変更を要求せずに受理した場合、発注書は自動的に確認されます。</span><span class="sxs-lookup"><span data-stu-id="54df4-212">**Active (PO is auto-confirmed)** – Purchase orders are automatically confirmed if the vendor accepts them without requesting changes.</span></span>
- <span data-ttu-id="54df4-213">**有効 (発注書は自動確認されません)** - 仕入先が受理した後、組織によって手動で発注書を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54df4-213">**Active (PO is not auto-confirmed)** – Your organization must manually confirm purchase orders after the vendor has accepted them.</span></span>

> [!NOTE]
> <span data-ttu-id="54df4-214">社内の調達担当者は、このタスクも完了できます。</span><span class="sxs-lookup"><span data-stu-id="54df4-214">Procurement professionals in your company can also complete this task.</span></span>

## <a name="troubleshoot-the-provisioning-of-new-vendor-collaboration-users"></a><span data-ttu-id="54df4-215">新しい仕入先の共同作業ユーザーのプロビジョニングのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="54df4-215">Troubleshoot the provisioning of new vendor collaboration users</span></span>

<span data-ttu-id="54df4-216">新しい仕入先コラボレーション ユーザーは、**仕入先ユーザーのプロビジョニング** タイプの仕入先コラボレーション ユーザーの要求を処理するために設定したワークフロー経由でプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="54df4-216">New vendor collaboration users are provisioned via the workflow that you set up to process vendor collaboration user requests of the **Provision vendor user** type.</span></span>

<span data-ttu-id="54df4-217">新しいベンダー コラボレーション ユーザーの電子メール アドレスが、テナントとして Azure に登録されているドメインに属している場合 (つまり、管理対象ドメイン アカウントの場合)、電子メール アドレスは既存の Azure AD アカウントである必要があります。</span><span class="sxs-lookup"><span data-stu-id="54df4-217">If the email address of a new vendor collaboration user belongs to a domain that is registered with Azure as a tenant (that is, if it's a managed domain account), the email address must be an existing Azure AD account.</span></span> <span data-ttu-id="54df4-218">それ以外の場合、プロビジョニング プロセスを実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="54df4-218">Otherwise, the provisioning process can't be completed.</span></span>

<span data-ttu-id="54df4-219">Azure AD アカウント管理のワークフローでの **Azure B2B ユーザー招待の送信**タスクで使用されるプロセスの詳細については、[Azure Active Directory B2B コラボレーション](https://azure.microsoft.com/en-us/documentation/articles/active-directory-b2b-collaboration-overview/) を参照してください</span><span class="sxs-lookup"><span data-stu-id="54df4-219">For more information about the process that is used in the **Send Azure B2B user invitation** task in the workflow for Azure AD account management, see [Azure Active Directory B2B collaboration](https://azure.microsoft.com/en-us/documentation/articles/active-directory-b2b-collaboration-overview/).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="54df4-220">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="54df4-220">Additional resources</span></span>

[<span data-ttu-id="54df4-221">外部仕入先との作業のために仕入先コラボレーションを使用する</span><span class="sxs-lookup"><span data-stu-id="54df4-221">Using vendor collaboration to work with external vendors</span></span>](vendor-collaboration-work-external-vendors.md)
