---
title: "プレビュー サブスクリプションのサインアップ"
description: "このトピックでは、プレビュー/パートナー オファーをサブスクライブして環境を配置する方法について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 10/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 13211
ms.assetid: bd976311-f6e3-418b-a6c6-49bb568de130
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 111a6a4de622da281bb3d93e23b1a973974a43dc
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="sign-up-for-a-preview-subscription"></a><span data-ttu-id="45169-103">プレビュー サブスクリプションのサインアップ</span><span class="sxs-lookup"><span data-stu-id="45169-103">Sign up for a preview subscription</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45169-104">このトピックでは、プレビュー/パートナー オファーをサブスクライブして環境を配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="45169-104">This topic explains how to subscribe to the preview/partner offer and deploy an environment.</span></span> <span data-ttu-id="45169-105">サブスクリプションを作成すると、Microsoft Online Services のテストテナントと、環境を展開できる Microsoft Dynamics Lifecycle Services (LCS) プロジェクトが提供されます。</span><span class="sxs-lookup"><span data-stu-id="45169-105">The subscription that you create gives you a Microsoft Online Services test tenant and a Microsoft Dynamics Lifecycle Services (LCS) project where you can deploy an environment.</span></span> <span data-ttu-id="45169-106">このトピックでは、Microsoft Online Services テナントに追加ユーザーを設定し、サービス管理機能の経験を積むのにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="45169-106">This topic will also help you set up additional users in your Microsoft Online Services tenant and gain experience with service administration capabilities.</span></span> <span data-ttu-id="45169-107">学ぶスキルを次に示します。</span><span class="sxs-lookup"><span data-stu-id="45169-107">Here are the skills that you will learn:</span></span>

- <span data-ttu-id="45169-108">新しい Microsoft オンライン テスト テナントを購読して作成します。</span><span class="sxs-lookup"><span data-stu-id="45169-108">Subscribe, and create a new Microsoft Online test tenant.</span></span>
- <span data-ttu-id="45169-109">LCS プロジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="45169-109">Navigate to LCS projects.</span></span>
- <span data-ttu-id="45169-110">LCS の各種機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="45169-110">Use various features of LCS.</span></span>
- <span data-ttu-id="45169-111">Microsoft Azure Active Directory (Azure AD) とクライアントにユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="45169-111">Add users to Microsoft Azure Active Directory (Azure AD) and the client.</span></span>
- <span data-ttu-id="45169-112">サブスクリプション電子メールのリソースを表示します。</span><span class="sxs-lookup"><span data-stu-id="45169-112">View resources in your subscription email.</span></span>

## <a name="key-terms"></a><span data-ttu-id="45169-113">重要な用語</span><span class="sxs-lookup"><span data-stu-id="45169-113">Key terms</span></span>
- <span data-ttu-id="45169-114">**Microsoft Online Services テナント** – テナントは、組織のすべての定期売買とユーザーのグループです。</span><span class="sxs-lookup"><span data-stu-id="45169-114">**Microsoft Online Services tenant** – A tenant is the group of all subscriptions and users for your organization.</span></span> <span data-ttu-id="45169-115">テナントは、Microsoft Online Services の最初のサブスクリプションと同時に作成されます。</span><span class="sxs-lookup"><span data-stu-id="45169-115">The tenant is created at the same time as your first subscription in Microsoft Online Services.</span></span>
- <span data-ttu-id="45169-116">**定期売買** – 定期売買により、オンライン クラウドの環境と経験が得られます。</span><span class="sxs-lookup"><span data-stu-id="45169-116">**Subscription** – A subscription gives you an online cloud environment and experience.</span></span> <span data-ttu-id="45169-117">また、これにより、作成したカスタマイズをクラウドに配置する方法も確認できます。</span><span class="sxs-lookup"><span data-stu-id="45169-117">It also lets you see how customizations that you develop can be deployed to the cloud.</span></span>
- <span data-ttu-id="45169-118">**Microsoft Azure Active Directory** – クラウド環境には、Azure AD が含まれます。</span><span class="sxs-lookup"><span data-stu-id="45169-118">**Microsoft Azure Active Directory** – The cloud environment includes Azure AD.</span></span> <span data-ttu-id="45169-119">オンプレミス環境の管理と同様、Azure AD はオンライン アプリケーションのユーザー、グループ、セキュリティ ロール、およびライセンスを管理するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="45169-119">Azure AD helps you manage users, groups, security roles, and licenses for online applications, much as you manage them for on-premise environments.</span></span>
- <span data-ttu-id="45169-120">**ユーザー** – 組織がサブスクリプションしているサービスのユーザーは Azure AD で管理されます。</span><span class="sxs-lookup"><span data-stu-id="45169-120">**Users** – Users of the services that your organization has subscribed to are managed in Azure AD.</span></span> <span data-ttu-id="45169-121">テナント内のすべてのユーザーを追加して、セキュリティ ロールに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="45169-121">Any users in your tenant can be added and assigned to security roles.</span></span>
- <span data-ttu-id="45169-122">**開発者と管理者** - 開発者と管理者は、プロジェクトや環境を管理できる LCS にもアクセスできるユーザーです。</span><span class="sxs-lookup"><span data-stu-id="45169-122">**Developers and administrators** – Developers and administrators are users who also have access to LCS that lets them manage projects and environments.</span></span> <span data-ttu-id="45169-123">これらのユーザーは、エンド ユーザーでもあります。</span><span class="sxs-lookup"><span data-stu-id="45169-123">These users are also end users.</span></span>
- <span data-ttu-id="45169-124">**組織アカウント** – ユーザーは Azure AD 資格情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="45169-124">**Organizational account** – Users receive Azure AD credentials.</span></span> <span data-ttu-id="45169-125">これらの資格情報は、他のデスクトップまたは企業の資格情報とは異なります。</span><span class="sxs-lookup"><span data-stu-id="45169-125">These credentials are separate from other desktop or corporate credentials.</span></span> <span data-ttu-id="45169-126">Azure AD 資格情報は、Microsoft Office 365 およびその他の Microsoft クラウド サービスへのログインに使用されます。</span><span class="sxs-lookup"><span data-stu-id="45169-126">The Azure AD credentials are used to sign in to Microsoft Office 365 and other Microsoft cloud services.</span></span> <span data-ttu-id="45169-127">ユーザーは組織のアカウントを使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="45169-127">Users sign in by using their organizational account.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="45169-128">今回のリリースでは、Office 365 または Microsoft Dynamics CRM Online などの他のオンライン サービスに関連付けられている、既存の資格情報を使用しないようお勧めします。</span><span class="sxs-lookup"><span data-stu-id="45169-128">For this release, we ask that you not use any existing credentials that are associated with other online services, such as Office 365 or Microsoft Dynamics CRM Online.</span></span>

- <span data-ttu-id="45169-129">**Microsoft アカウント** – Microsoft アカウントは、以前は Passport アカウントまたは Windows Live ID アカウントと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="45169-129">**Microsoft account** – Microsoft accounts were formerly known as Passport accounts or Windows Live ID accounts.</span></span> <span data-ttu-id="45169-130">現在、Microsoft Dynamics 365 for Finance and Operations、Microsoft Dynamics 365 for Retail、またはその他の Microsoft オンライン サービスで Microsoft アカウントを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="45169-130">Currently, Microsoft accounts can't be used with Microsoft Dynamics 365 for Finance and Operations, Microsoft Dynamics 365 for Retail, or other Microsoft Online Services.</span></span> <span data-ttu-id="45169-131">ただし、Microsoft アカウントは、CustomerSource、PartnerSource、ソース情報、および Microsoft Dynamics コミュニティなどの Microsoft Connect および他の Microsoft Business Solutions サイトに対して必要です。</span><span class="sxs-lookup"><span data-stu-id="45169-131">However, Microsoft accounts are still required for Microsoft Connect and other Microsoft Business Solutions sites, such as CustomerSource, PartnerSource, Information Source, and Microsoft Dynamics Community.</span></span> <span data-ttu-id="45169-132">これらのサービスにアクセスするには、Microsoft アカウントを引き続き使用します。</span><span class="sxs-lookup"><span data-stu-id="45169-132">You will continue to use your Microsoft account to access these services.</span></span>
- <span data-ttu-id="45169-133">**Microsoft Office 365 管理者センター** – Office 365 管理者センターは、Office 365 が管理者に提供する定期売買管理ポータルです。</span><span class="sxs-lookup"><span data-stu-id="45169-133">**Microsoft Office 365 admin center** – Office 365 admin center is the subscription management portal that Office 365 provides for administrators.</span></span> <span data-ttu-id="45169-134">Office 365 管理者センターを使用して、ユーザーおよび定期売買の管理機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="45169-134">Office 365 admin center is used to provide management functions for users and subscriptions.</span></span>
- <span data-ttu-id="45169-135">**環境** - 必要に応じて、仮想マシン (VM) の単一インスタンスをいくつでも配置できます。</span><span class="sxs-lookup"><span data-stu-id="45169-135">**Environments** – You can deploy as many single instances of a virtual machine (VM) as you require.</span></span> <span data-ttu-id="45169-136">これらのインスタンスを *環境* と呼び出ます。</span><span class="sxs-lookup"><span data-stu-id="45169-136">We call these instances *environments*.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="45169-137">前提条件</span><span class="sxs-lookup"><span data-stu-id="45169-137">Prerequisites</span></span>
1. <span data-ttu-id="45169-138">プレビューへの参加を招待する電子メールを受信しました。</span><span class="sxs-lookup"><span data-stu-id="45169-138">You've received an email that invites you to participate in the preview.</span></span>
2. <span data-ttu-id="45169-139">会社に Microsoft Online Services 付きの組織アカウントがあり、サインインしている場合、続行する前にサインアウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="45169-139">If your company has an organizational account with Microsoft Online Services, and you're signed in, you must sign out before you continue.</span></span> <span data-ttu-id="45169-140">または、**InPrivate ブラウズ**モードを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="45169-140">Alternatively, you can use **InPrivate Browsing** mode.</span></span>
3. <span data-ttu-id="45169-141">ログオンしているかどうか分からない場合は、ブラウザーのクッキーを削除し、続行する前にブラウザーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="45169-141">If you aren't sure whether you're signed in, delete your browser cookies, and then close your browser before you continue.</span></span>

## <a name="subscribe"></a><span data-ttu-id="45169-142">サブスクライブ</span><span class="sxs-lookup"><span data-stu-id="45169-142">Subscribe</span></span>
> [!IMPORTANT]
> <span data-ttu-id="45169-143">組織内で 1 人 (テナント管理者) だけ、このタスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45169-143">Only one person (tenant administrator) in an organization must perform this task.</span></span> <span data-ttu-id="45169-144">このリリースをサブスクライブしていない場合は、組織がサインアップし、ユーザーの資格情報を受信するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="45169-144">If you aren't the person who is subscribing to this release, wait until your organization has been signed up and you've received your user credentials.</span></span> <span data-ttu-id="45169-145">その後、手順を続行します。</span><span class="sxs-lookup"><span data-stu-id="45169-145">Then continue with the procedure.</span></span>

1. <span data-ttu-id="45169-146">Finance and Operations および Retail は、既存の Microsoft Dynamics 365 のチャネル パートナーおよび Business Ready 拡張プラン (BREP) サービス プランに現在登録されている顧客にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="45169-146">Finance and Operations and Retail are available only to existing Microsoft Dynamics 365 channel partners and customers who are currently enrolled in the Business Ready Enhancement Plan (BREP) service plan.</span></span> <span data-ttu-id="45169-147">既存の顧客は、[CustomerSource](https://mbs.microsoft.com/customersource/global/AX/news-events/news/Microsoft_Dynamics_AX_Public_Preview) の試用版にアクセスする詳細方法を検索できます。</span><span class="sxs-lookup"><span data-stu-id="45169-147">Existing customers can find details about how to access trials on [CustomerSource](https://mbs.microsoft.com/customersource/global/AX/news-events/news/Microsoft_Dynamics_AX_Public_Preview).</span></span> <span data-ttu-id="45169-148">パートナーは、[PartnerSource](https://mbs.microsoft.com/partnersource/global/news-events/news/Microsoft_Dynamics_AX_Public_Preview) で詳細を参照できます。</span><span class="sxs-lookup"><span data-stu-id="45169-148">Partners can find the details on [PartnerSource](https://mbs.microsoft.com/partnersource/global/news-events/news/Microsoft_Dynamics_AX_Public_Preview).</span></span>
2. <span data-ttu-id="45169-149">**アカウント設定**ページの、**国または地域**フィールドで、国または地域の選択をします。</span><span class="sxs-lookup"><span data-stu-id="45169-149">On the **Account setup** page, in the **Country or region** field, select the country or region.</span></span>
3. <span data-ttu-id="45169-150">最後のステップに到達するまで、サインアップを完了するウィザードおよびプロンプトに従います。</span><span class="sxs-lookup"><span data-stu-id="45169-150">Follow the wizard and prompts to complete the sign-up, until you reach the last step.</span></span>

    <span data-ttu-id="45169-151">[![準備ができました](./media/wizardprompt.png)](./media/wizardprompt.png)</span><span class="sxs-lookup"><span data-stu-id="45169-151">[![You're ready to go](./media/wizardprompt.png)](./media/wizardprompt.png)</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="45169-152">LCS で新しいプロジェクトを開始</span><span class="sxs-lookup"><span data-stu-id="45169-152">Start a new project in LCS</span></span>
<span data-ttu-id="45169-153">LCS を使用して環境を管理するには、新しいプロジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45169-153">To use LCS to manage your environments, you must create a new project.</span></span>

1. <span data-ttu-id="45169-154"><https://lcs.dynamics.com/Logon/Index> に移動します。</span><span class="sxs-lookup"><span data-stu-id="45169-154">Go to <https://lcs.dynamics.com/Logon/Index>.</span></span>
2. <span data-ttu-id="45169-155">**サインイン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="45169-155">Select **Sign in**.</span></span>
3. <span data-ttu-id="45169-156">サブスクライブするために使用したアカウントを使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="45169-156">Sign in by using the account that you used to subscribe.</span></span>
4. <span data-ttu-id="45169-157">プラス記号 (**+**) を選択して新しいプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="45169-157">Select the plus sign (**+**) to create a new project.</span></span>

    <span data-ttu-id="45169-158">[![プロジェクトの作成](./media/11-1024x473.jpg)](./media/11.jpg)</span><span class="sxs-lookup"><span data-stu-id="45169-158">[![Create a project](./media/11-1024x473.jpg)](./media/11.jpg)</span></span>

5. <span data-ttu-id="45169-159">プロジェクト タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="45169-159">Select the project type.</span></span>
6. <span data-ttu-id="45169-160">プロジェクト情報を入力し、**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="45169-160">Enter the project information, and then select **Create**.</span></span>

    <span data-ttu-id="45169-161">Retail を評価する予定がある場合は、**製品名**フィールドで **Microsoft Dynamics 365 for Retail** を必ず選択します。</span><span class="sxs-lookup"><span data-stu-id="45169-161">If you plan to evaluate Retail, be sure to select **Microsoft Dynamics 365 for Retail** in the **Product name** field.</span></span>

    <span data-ttu-id="45169-162">インスタンスを管理するための新しいプロジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="45169-162">The new project for managing your instance is created.</span></span>

    ![新規プロジェクト](./media/projectworkspace.jpg)

## <a name="add-users-to-lcs"></a><span data-ttu-id="45169-164">LCS へのユーザーの追加</span><span class="sxs-lookup"><span data-stu-id="45169-164">Add users to LCS</span></span>
<span data-ttu-id="45169-165">LCS プロジェクトのユーザーとして既に設定しています。</span><span class="sxs-lookup"><span data-stu-id="45169-165">You're already set up as a user of your LCS project.</span></span> <span data-ttu-id="45169-166">他の Office 365 ユーザーも追加した場合、このプロジェクトに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45169-166">If you've also added other Office 365 users, you must add them to this project.</span></span> <span data-ttu-id="45169-167">他の管理者や開発者は、独自の環境の配置できるようになります。</span><span class="sxs-lookup"><span data-stu-id="45169-167">Other administrators and developers will then be able to deploy their own environments.</span></span> <span data-ttu-id="45169-168">これらの LCS ユーザーは、実装に積極的に取り組むチーム メンバーです。</span><span class="sxs-lookup"><span data-stu-id="45169-168">These LCS users are team members who will actively work on the implementation.</span></span> <span data-ttu-id="45169-169">エンド ユーザーと混同しないでください。</span><span class="sxs-lookup"><span data-stu-id="45169-169">Don't confuse them with end users.</span></span> <span data-ttu-id="45169-170">LCS でプロジェクト ページを開始します。</span><span class="sxs-lookup"><span data-stu-id="45169-170">Start on the project page in LCS.</span></span>

1. <span data-ttu-id="45169-171">右にスクロールし、**追加ツール** セクションで、**プロジェクト ユーザー** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="45169-171">Scroll to the right, and then, in the **More tools** section, select the **Project users** tile.</span></span>
2. <span data-ttu-id="45169-172">左上で、プラス記号 (**+**) を選択して新しいユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="45169-172">In the upper left, select the plus sign (**+**) to add a new user.</span></span>
3. <span data-ttu-id="45169-173">**電子メール** フィールドに、追加するユーザーの電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="45169-173">In the **Email** field, enter the email address of the user that you're adding.</span></span> <span data-ttu-id="45169-174">この電子メール アドレスは、以前作成した Office 365 組織の電子メール アドレスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="45169-174">This email address should be the Office 365 organization email address that you created earlier.</span></span>
4. <span data-ttu-id="45169-175">**プロジェクトのロール** フィールドで、**プロジェクト所有者**を選択します。</span><span class="sxs-lookup"><span data-stu-id="45169-175">In the **Project role** field, select **Project Owner**.</span></span>
5. <span data-ttu-id="45169-176">**招待** を選択します。</span><span class="sxs-lookup"><span data-stu-id="45169-176">Select **Invite**.</span></span>
6. <span data-ttu-id="45169-177">組織内のすべてのユーザーに対して手順 2 ～ 5 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="45169-177">Repeat steps 2 through 5 for all users in your organization.</span></span>

## <a name="deploy-environments"></a><span data-ttu-id="45169-178">環境の配置</span><span class="sxs-lookup"><span data-stu-id="45169-178">Deploy environments</span></span>
<span data-ttu-id="45169-179">環境では、既存の Azure サブスクリプションを配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45169-179">Environments should be deployed to an existing Azure subscription.</span></span>

> [!NOTE]
> <span data-ttu-id="45169-180">それぞれの環境開発者は、Azure に自身のシステムを導入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45169-180">Each developer of an environment must deploy his or her own system to Azure.</span></span> <span data-ttu-id="45169-181">ただし、最初のプロジェクト ユーザーのみが配置の Azure サブスクリプションを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45169-181">However, only the first project user must set up the Azure subscription for deployment.</span></span>

<span data-ttu-id="45169-182">2 種類の方法で環境を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="45169-182">You can create environments in two ways:</span></span>

- <span data-ttu-id="45169-183">Microsoft クラウド サービス (Azure) に配置します。</span><span class="sxs-lookup"><span data-stu-id="45169-183">Deploy to Microsoft cloud services (Azure).</span></span>
- <span data-ttu-id="45169-184">ローケル仮想ハード ディスク (VHD) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="45169-184">Download a local virtual hard disk (VHD).</span></span>

<span data-ttu-id="45169-185">LCS でプロジェクト ページを開始します。</span><span class="sxs-lookup"><span data-stu-id="45169-185">Start on the project page in LCS.</span></span>

1. <span data-ttu-id="45169-186">**環境**セクションで、プラス記号 (**+**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="45169-186">In the **Environments** section, select the plus sign (**+**).</span></span> <span data-ttu-id="45169-187">**Microsoft Azure 設定** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="45169-187">The **Microsoft Azure setup** dialog box appears.</span></span>
2. <span data-ttu-id="45169-188">Azure サブスクリプション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="45169-188">Enter your Azure subscription ID.</span></span> <span data-ttu-id="45169-189">Azure サブスクリプション ID は Azure Portal (<https://ms.portal.azure.com/>) の、左下の **設定** で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="45169-189">You can find your Azure subscription ID in Azure Portal (<https://ms.portal.azure.com/>), under **Settings** in the lower left.</span></span>
3. <span data-ttu-id="45169-190">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="45169-190">Select **Next**.</span></span>
4. <span data-ttu-id="45169-191">Azure Management Certificate をコンピューターのローカル フォルダーにダウンロードし、**設定** &gt; **管理証明書**にアクセスして Azure Management Portal を更新します。</span><span class="sxs-lookup"><span data-stu-id="45169-191">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** &gt; **Management Certificates**.</span></span> <span data-ttu-id="45169-192">この証明書は、自分の代わりに LCS が Azure と通信できるようにします。</span><span class="sxs-lookup"><span data-stu-id="45169-192">This certificate will enable LCS to communicate with Azure on your behalf.</span></span>
5. <span data-ttu-id="45169-193">LCS に戻り、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="45169-193">Return to LCS, and select **Next**.</span></span>
6. <span data-ttu-id="45169-194">配置する Azure リージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="45169-194">Select the Azure region to deploy in.</span></span> <span data-ttu-id="45169-195">**米国西部** 地域は展開が最も速くなっていますが、このシステムを使用する場所に近いデータ センターを選択することが重要です。</span><span class="sxs-lookup"><span data-stu-id="45169-195">The **West US** region will have the fastest deployments, but it's important that you select a data center that is close to where you plan to use this system.</span></span>
7. <span data-ttu-id="45169-196">**接続** を選択します。</span><span class="sxs-lookup"><span data-stu-id="45169-196">Select **Connect**.</span></span>
8. <span data-ttu-id="45169-197">使用可能なトポロジの一覧で、配置するトポロジを選択します。</span><span class="sxs-lookup"><span data-stu-id="45169-197">In the list of available topologies, select the topology to deploy.</span></span> <span data-ttu-id="45169-198">VHD をダウンロードする **ダウンロード** リンク、または Azure 上に展開する **次へ** のいずれかを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="45169-198">You can select either the **Download** link to download the VHD or **Next** to deploy on Azure.</span></span> <span data-ttu-id="45169-199">Azure は優先されるパスです。</span><span class="sxs-lookup"><span data-stu-id="45169-199">Azure is the preferred path.</span></span>
9. <span data-ttu-id="45169-200">環境名を入力します。</span><span class="sxs-lookup"><span data-stu-id="45169-200">Enter the name of the environment.</span></span>
10. <span data-ttu-id="45169-201">価格決定およびライセンス条件を読み、チェック ボックスをオンにして理解したことを示します。</span><span class="sxs-lookup"><span data-stu-id="45169-201">Read the pricing and licensing terms, and then select the check box to indicate that you understand them.</span></span>
11. <span data-ttu-id="45169-202">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="45169-202">Select **Next**.</span></span>
12. <span data-ttu-id="45169-203">詳細を確認し、**配置**を選択します。</span><span class="sxs-lookup"><span data-stu-id="45169-203">Confirm the details, and then select **Deploy**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="45169-204">独自の環境を使用する開発者および管理者は、サインインしてこれらの手順を繰り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="45169-204">Developers and administrators who will use their own environments must sign in and repeat these steps.</span></span>
    
    <span data-ttu-id="45169-205">環境を配置した後、**環境**セクションは使用可能です。</span><span class="sxs-lookup"><span data-stu-id="45169-205">After you deploy your environment, it's available in the **Environments** section.</span></span>

    <span data-ttu-id="45169-206">[![環境セクションにある新規環境](./media/pic7.jpg)](./media/pic7.jpg)</span><span class="sxs-lookup"><span data-stu-id="45169-206">[![New environment in the Environments section](./media/pic7.jpg)](./media/pic7.jpg)</span></span>

13. <span data-ttu-id="45169-207">配置のステータスに関する詳細を表示するための環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="45169-207">Select the environment to view details about the deployment status.</span></span> <span data-ttu-id="45169-208">最初の配置には数時間かかりますが、その後の配置はずっと高速になります。</span><span class="sxs-lookup"><span data-stu-id="45169-208">The first deployment will require a few hours, but each subsequent deployment will be much faster.</span></span>
14. <span data-ttu-id="45169-209">配置状態が **配置済み** に変わったときに、**ログイン** を選択してクライアントに接続するか、または VM の名前を選択して、リモート デスクトップを使用して開発マシンに接続します。</span><span class="sxs-lookup"><span data-stu-id="45169-209">When the deployment status changes to **Deployed**, select **Login** to connect to the client, or select the name of the VM to connect to the development machine by using Remote Desktop.</span></span> <span data-ttu-id="45169-210">配置が完了した後、リモート デスクトップ経由で環境に接続するために必要な基本 URL と情報を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="45169-210">After the deployment is completed, you can find the base URL and the information that you require to connect to the environment via Remote Desktop.</span></span>

## <a name="use-the-features-of-lcs"></a><span data-ttu-id="45169-211">LCS 機能の使用</span><span class="sxs-lookup"><span data-stu-id="45169-211">Use the features of LCS</span></span>
<span data-ttu-id="45169-212">LCS は、オンライン管理アクティビティを実行するための出発点です。</span><span class="sxs-lookup"><span data-stu-id="45169-212">LCS is the starting point for performing online administrative activities.</span></span> <span data-ttu-id="45169-213">これらの活動例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="45169-213">Here are some of these activities:</span></span>

- <span data-ttu-id="45169-214">Azure に VM を配置します。</span><span class="sxs-lookup"><span data-stu-id="45169-214">Deploy VMs on Azure.</span></span>
- <span data-ttu-id="45169-215">アクセスの材料。</span><span class="sxs-lookup"><span data-stu-id="45169-215">Access materials.</span></span>
- <span data-ttu-id="45169-216">ツールとリソースのダウンロードにアクセス。</span><span class="sxs-lookup"><span data-stu-id="45169-216">Access downloads of tools and resources.</span></span>

### <a name="explore-the-lcs-project"></a><span data-ttu-id="45169-217">LCS プロジェクトを検証</span><span class="sxs-lookup"><span data-stu-id="45169-217">Explore the LCS project</span></span>
1. <span data-ttu-id="45169-218">方法を確認し、ライフ サイクルを通過するときにタスクとフェーズを完了します。</span><span class="sxs-lookup"><span data-stu-id="45169-218">Review the methodology, and complete the tasks and phases as you progress through the life cycle.</span></span>

    <span data-ttu-id="45169-219">[![フェーズおよびタスク](./media/pic8.jpg)](./media/pic8.jpg)[](./media/methodologyreview.png)</span><span class="sxs-lookup"><span data-stu-id="45169-219">[![Phases and tasks](./media/pic8.jpg)](./media/pic8.jpg)[](./media/methodologyreview.png)</span></span>
    
    <span data-ttu-id="45169-220">フェーズとタスクの情報により、エンタープライズ リソース プランニング (ERP) エクスペリエンスの全体を通して使用できるツールとリソースを表示できます。</span><span class="sxs-lookup"><span data-stu-id="45169-220">The phases and task information lets you view tools and resources that are available throughout your enterprise resource planning (ERP) experience.</span></span>

2. <span data-ttu-id="45169-221">右にスクロールし、タイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="45169-221">Scroll to the right, and review the tiles.</span></span>

    <span data-ttu-id="45169-222">[![タイル](./media/pic9.jpg)](./media/pic9.jpg)</span><span class="sxs-lookup"><span data-stu-id="45169-222">[![Tiles](./media/pic9.jpg)](./media/pic9.jpg)</span></span>

    <span data-ttu-id="45169-223">使用可能なタイルには、LCS のさまざまなツールとサービスがあります。</span><span class="sxs-lookup"><span data-stu-id="45169-223">The available tiles include various tools and services in LCS.</span></span> <span data-ttu-id="45169-224">次の追加のタイトルも含まれます。</span><span class="sxs-lookup"><span data-stu-id="45169-224">They also include the following additional tiles:</span></span>

    - <span data-ttu-id="45169-225">**自分の定期売買** – Office 365 定期売買の管理ポータルでは、オンライン定期売買を表示して操作できます。</span><span class="sxs-lookup"><span data-stu-id="45169-225">**My subscription** – The Office 365 subscription management portal is where you can view and work with your online subscriptions.</span></span> <span data-ttu-id="45169-226">ページの左側のナビゲーション セクションで**ユーザーとグループ**を選択することにより、オンライン ユーザーを管理することもできます。</span><span class="sxs-lookup"><span data-stu-id="45169-226">By selecting **User and Groups** in the left navigation section of the page, you can also manage your online users.</span></span>

        > [!NOTE]
        > <span data-ttu-id="45169-227">このページにアクセスするには、組織の Microsoft Online Services テナントにおいて**グローバル管理者** ロールのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="45169-227">To access the page, you must be a member of the **Global Administrator** role for your organization's Microsoft Online Services tenant.</span></span>

    - <span data-ttu-id="45169-228">**フィードバックとバグ** – このタイルは Microsoft Connect の**全般フィードバック**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="45169-228">**Feedback and bugs** – This tile opens the **General Feedback** page in Microsoft Connect.</span></span> <span data-ttu-id="45169-229">バグの記録や、設計変更要求、機能要求、提案を行うには、このページを使用します。</span><span class="sxs-lookup"><span data-stu-id="45169-229">Use this page to record bugs, and to design change requests, feature requests, and suggestions.</span></span>
    - <span data-ttu-id="45169-230">**Office 365 ユーザー** – このタイルは Office 365 管理者センターの**ユーザーおよびグループ**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="45169-230">**Office 365 users** – This tile opens the **Users and groups** page in Office 365 admin center.</span></span> <span data-ttu-id="45169-231">他のサービスのためにユーザーを追加、更新、および削除し、パスワードをリセットし、ライセンスを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="45169-231">You can add, update, and remove users, reset passwords, and assign licenses for other services.</span></span>

        > [!NOTE]
        > <span data-ttu-id="45169-232">このページにアクセスするには、組織の Microsoft Online Services テナントにおいて**グローバル管理者** ロールのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="45169-232">To access the page, you must be a member of the **Global Administrator** role for your organization's Microsoft Online Services tenant.</span></span> <span data-ttu-id="45169-233">インストール ユーザーは常にグローバル管理者ですが、他のユーザーをこのロールに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45169-233">The installing user is always a global administrator, but other users must be added to this role.</span></span>

        <span data-ttu-id="45169-234">[![Office 365 管理者センターの有効なユーザー](./media/activeusersadmin.png)](./media/activeusersadmin.png)</span><span class="sxs-lookup"><span data-stu-id="45169-234">[![Active users in Office 365 admin center](./media/activeusersadmin.png)](./media/activeusersadmin.png)</span></span>
