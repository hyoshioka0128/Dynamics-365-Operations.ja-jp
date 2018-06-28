---
title: "サービス エンドポイント"
description: "このトピックでは、使用できるサービス エンドポイントについて説明します。"
author: Sunil-Garg
manager: AnnBe
ms.date: 11/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 80710faa3bc0f1f7f165968e60c36a5d9b325958
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="service-endpoints"></a><span data-ttu-id="27cc2-103">サービス エンドポイント</span><span class="sxs-lookup"><span data-stu-id="27cc2-103">Service endpoints</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27cc2-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations で使用できるサービス エンドポイントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-104">This topic describes the service endpoints that are available in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="27cc2-105">また、Microsoft Dynamics AX 2012 で使用できるエンドポイントと比較します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-105">It also provides a comparison to the endpoints that are available in Microsoft Dynamics AX 2012.</span></span> 

## <a name="list-of-services"></a><span data-ttu-id="27cc2-106">サービスのリスト</span><span class="sxs-lookup"><span data-stu-id="27cc2-106">List of services</span></span>
<span data-ttu-id="27cc2-107">次のテーブルでは、すべてのサービス エンドポイントを一覧表示し、Finance and Operations、および AX 2012 で使用可能なエンドポイントを比較しています。</span><span class="sxs-lookup"><span data-stu-id="27cc2-107">The following table lists all the service endpoints, and compares the endpoints available for Finance and Operations, and AX 2012.</span></span>

| <span data-ttu-id="27cc2-108">サービス エンドポイント</span><span class="sxs-lookup"><span data-stu-id="27cc2-108">Service endpoint</span></span>            | <span data-ttu-id="27cc2-109">AX 2012</span><span class="sxs-lookup"><span data-stu-id="27cc2-109">AX 2012</span></span> | <span data-ttu-id="27cc2-110">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27cc2-110">Finance and Operations</span></span>     |
|-----------------------------|------------------|--------------------------------|
| <span data-ttu-id="27cc2-111">ドキュメント サービス (AXDs)</span><span class="sxs-lookup"><span data-stu-id="27cc2-111">Document services (AXDs)</span></span>    | <span data-ttu-id="27cc2-112">有</span><span class="sxs-lookup"><span data-stu-id="27cc2-112">Yes</span></span>              | <span data-ttu-id="27cc2-113">いいえ – データ エンティティに置き換えられます</span><span class="sxs-lookup"><span data-stu-id="27cc2-113">No – Replaced by data entities</span></span> |
| <span data-ttu-id="27cc2-114">SOAP ベースのメタデータ サービス</span><span class="sxs-lookup"><span data-stu-id="27cc2-114">SOAP-based metadata service</span></span> | <span data-ttu-id="27cc2-115">有</span><span class="sxs-lookup"><span data-stu-id="27cc2-115">Yes</span></span>              | <span data-ttu-id="27cc2-116">いいえ – REST メタデータに置き換えられます</span><span class="sxs-lookup"><span data-stu-id="27cc2-116">No – Replaced by REST metadata</span></span> |
| <span data-ttu-id="27cc2-117">SOAP ベースのクエリ サービス</span><span class="sxs-lookup"><span data-stu-id="27cc2-117">SOAP-based query service</span></span>    | <span data-ttu-id="27cc2-118">有</span><span class="sxs-lookup"><span data-stu-id="27cc2-118">Yes</span></span>              | <span data-ttu-id="27cc2-119">いいえ – OData に置き換えられます</span><span class="sxs-lookup"><span data-stu-id="27cc2-119">No – Replaced by OData</span></span>         |
| <span data-ttu-id="27cc2-120">OData クエリ サービス</span><span class="sxs-lookup"><span data-stu-id="27cc2-120">OData query service</span></span>         | <span data-ttu-id="27cc2-121">有</span><span class="sxs-lookup"><span data-stu-id="27cc2-121">Yes</span></span>              | <span data-ttu-id="27cc2-122">いいえ – OData に置き換えられます</span><span class="sxs-lookup"><span data-stu-id="27cc2-122">No – Replaced by OData</span></span>         |
| <span data-ttu-id="27cc2-123">SOAP ベース顧客サービス</span><span class="sxs-lookup"><span data-stu-id="27cc2-123">SOAP-based custom service</span></span>   | <span data-ttu-id="27cc2-124">有</span><span class="sxs-lookup"><span data-stu-id="27cc2-124">Yes</span></span>              | <span data-ttu-id="27cc2-125">有</span><span class="sxs-lookup"><span data-stu-id="27cc2-125">Yes</span></span>                            |
| <span data-ttu-id="27cc2-126">JSON ベース顧客サービス</span><span class="sxs-lookup"><span data-stu-id="27cc2-126">JSON-based custom service</span></span>   | <span data-ttu-id="27cc2-127">無</span><span class="sxs-lookup"><span data-stu-id="27cc2-127">No</span></span>               | <span data-ttu-id="27cc2-128">有</span><span class="sxs-lookup"><span data-stu-id="27cc2-128">Yes</span></span>                   |
| <span data-ttu-id="27cc2-129">OData サービス</span><span class="sxs-lookup"><span data-stu-id="27cc2-129">OData Service</span></span>               | <span data-ttu-id="27cc2-130">無</span><span class="sxs-lookup"><span data-stu-id="27cc2-130">No</span></span>               | <span data-ttu-id="27cc2-131">有</span><span class="sxs-lookup"><span data-stu-id="27cc2-131">Yes</span></span>                   |
| <span data-ttu-id="27cc2-132">REST メタデータ サービス</span><span class="sxs-lookup"><span data-stu-id="27cc2-132">REST Metadata Service</span></span>       | <span data-ttu-id="27cc2-133">無</span><span class="sxs-lookup"><span data-stu-id="27cc2-133">No</span></span>               | <span data-ttu-id="27cc2-134">有</span><span class="sxs-lookup"><span data-stu-id="27cc2-134">Yes</span></span>                   |

<span data-ttu-id="27cc2-135">このトピックは、サービスと、REST メタデータ サービスの認証について説明します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-135">This topic describes authentication for services, and the REST Metadata service.</span></span> <span data-ttu-id="27cc2-136">次のリンクでは、以下のための詳細なドキュメントを提供します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-136">The following links provide detailed documentation for:</span></span> 
- [<span data-ttu-id="27cc2-137">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="27cc2-137">Custom services</span></span>](custom-services.md)
- [<span data-ttu-id="27cc2-138">OData サービス</span><span class="sxs-lookup"><span data-stu-id="27cc2-138">OData service</span></span>](odata.md)

## <a name="authentication"></a><span data-ttu-id="27cc2-139">認証</span><span class="sxs-lookup"><span data-stu-id="27cc2-139">Authentication</span></span>
<span data-ttu-id="27cc2-140">OData サービス、JSON ベース顧客サービス、および REST メタデータ サービスは、標準の OAuth 2.0 認証をサポートします。</span><span class="sxs-lookup"><span data-stu-id="27cc2-140">OData services, JSON-based custom services, and the REST metadata service support standard OAuth 2.0 authentication.</span></span> 

<span data-ttu-id="27cc2-141">現在のところ、[承認コード付与フロー](https://msdn.microsoft.com/en-us/library/azure/dn645542.aspx)と[クライアントの資格情報 (共有シークレットまたは証明書) を使用したサービス間の呼び出し](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-protocols-oauth-service-to-service)の両方をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="27cc2-141">We currently support both [Authorization Code Grant flow](https://msdn.microsoft.com/en-us/library/azure/dn645542.aspx) and [Service to service calls using client credentials (shared secret or certificate)](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-protocols-oauth-service-to-service).</span></span> 

<span data-ttu-id="27cc2-142">Microsoft Azure Active Directory (AAD) では、次の 2 種類のアプリケーションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="27cc2-142">Two kinds of application are supported in Microsoft Azure Active Directory (AAD):</span></span>

-   <span data-ttu-id="27cc2-143">**ネイティブ クライアント アプリケーション** – このフローでは、認証と承認にユーザー名とパスワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-143">**Native client application** – This flow uses a user name and password for authentication and authorization.</span></span>
-   <span data-ttu-id="27cc2-144">**Web アプリケーション (機密クライアント)** – 機密クライアントとは、クライアントのパスワードを世界に対して秘密にするアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="27cc2-144">**Web application (Confidential client)** – A confidential client is an application that can keep a client password confidential to the world.</span></span> <span data-ttu-id="27cc2-145">承認サーバーは、このクライアント パスワードをクライアント アプリケーションに割り当てています。</span><span class="sxs-lookup"><span data-stu-id="27cc2-145">The authorization server assigned this client password to the client application.</span></span> 

<span data-ttu-id="27cc2-146">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="27cc2-146">For more information, see:</span></span> 
- [<span data-ttu-id="27cc2-147">OAuth 2.0 および Azure Active Directory を使用して web アプリケーションへのアクセスを許可する</span><span class="sxs-lookup"><span data-stu-id="27cc2-147">Authorize access to web applications using OAuth 2.0 and Azure Active Directory</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn645545.aspx)
- [<span data-ttu-id="27cc2-148">サービス認証のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="27cc2-148">Troubleshoot service authentication</span></span>](troubleshoot-service-authentication.md)

<span data-ttu-id="27cc2-149">次の図は、認証コードの付与フローに対して認証を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-149">The following illustration describes how authorization must be configured for Authorization code grant flow.</span></span> 

![認証コードの付与フロー](./media/services-authentication.png)


<span data-ttu-id="27cc2-151">以下の図では、クライアントの資格情報 (共有秘密または証明書) を使用したサービス間の呼び出し承認の仕組みを説明します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-151">And below is the illustration describes how authorization works for Service to service calls using client credentials (shared secret or certificate).</span></span>

![クライアント資格情報を使用したサービス間呼び出し](./media/S2SAuth.jpg)

### <a name="register-a-native-application-with-aad"></a><span data-ttu-id="27cc2-153">AAD にネイティブ アプリケーションを登録する</span><span class="sxs-lookup"><span data-stu-id="27cc2-153">Register a native application with AAD</span></span>

<span data-ttu-id="27cc2-154">クライアントがサービスと通信するには、事前に AAD に登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27cc2-154">Before any clients can communicate with the services, they must be registered in AAD.</span></span> <span data-ttu-id="27cc2-155">これらの手順を使用すると、AAD でアプリケーションに登録できます。</span><span class="sxs-lookup"><span data-stu-id="27cc2-155">These steps will help you register an application with AAD.</span></span> 

> [!NOTE]
> <span data-ttu-id="27cc2-156">これらの手順は、組織内のすべての人が完了する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="27cc2-156">These steps don't have to be completed by all the people in your organization.</span></span> <span data-ttu-id="27cc2-157">Azure サービスの管理者ユーザーのみがアプリケーションを追加し、その開発者とクライアント ID を共有することができます。</span><span class="sxs-lookup"><span data-stu-id="27cc2-157">Only one Azure Service Administrator user can add the application and share the client ID with the developers.</span></span> <span data-ttu-id="27cc2-158">**前提条件:** Azure サブスクリプションと Active Directory への管理者権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="27cc2-158">**Prerequisite:** You must have an Azure subscription and admin access to Active Directory.</span></span>

1. <span data-ttu-id="27cc2-159">Microsoft Dynamics Lifecycle Services (LCS) の適切なプロジェクトから Azure ポータルを開きます。</span><span class="sxs-lookup"><span data-stu-id="27cc2-159">From the appropriate project in Microsoft Dynamics Lifecycle Services (LCS), open Azure portal.</span></span>

    ![Azure ポータルを開きます](./media/odata_azure1.png)

2. <span data-ttu-id="27cc2-161">Azure ポータルの **Azure Active Directory** タブで、**プロパティ**を選択して**ディレクトリ ID** フィールドのテナント ID を記録します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-161">In Azure portal, on the **Azure Active Directory** tab, select **Properties**, and make a note of the tenant ID in the **Directory ID** field.</span></span> <span data-ttu-id="27cc2-162">Azure Active Directory (Azure AD) 認証トークンを取得するには、後で、テナント ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="27cc2-162">You will require the tenant ID later to retrieve an Azure Active Directory (Azure AD) authentication token.</span></span>
3. <span data-ttu-id="27cc2-163">**Azure Active Directory** タブで、**アプリの登録**を選択し、**新しいアプリケーションの登録**を選択します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-163">On the **Azure Active Directory** tab, select **App registrations**, and then select **New application registration**.</span></span>
4. <span data-ttu-id="27cc2-164">登録している外部アプリケーションを識別する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-164">Enter a name that identifies the external application that you're registering.</span></span> <span data-ttu-id="27cc2-165">共有機密情報を使用して認証するアプリケーションについては、**Web アプリ/API** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-165">For an application that will authenticate by using a shared secret, select **Web app / API**.</span></span> <span data-ttu-id="27cc2-166">このコンテキストでは、サインオン URL は関係ありません。</span><span class="sxs-lookup"><span data-stu-id="27cc2-166">In this context, the sign-on URL doesn't matter.</span></span> <span data-ttu-id="27cc2-167">したがって、**localhost** を使用します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-167">Therefore, use **localhost**.</span></span>
5. <span data-ttu-id="27cc2-168">新しいアプリケーションを選択し、アプリケーション ID をコピーします。</span><span class="sxs-lookup"><span data-stu-id="27cc2-168">Select the new application, and copy the application ID.</span></span> <span data-ttu-id="27cc2-169">Azure AD 認証トークンを要求するには、後で、アプリケーション ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="27cc2-169">You will require the application ID later to request an Azure AD authentication token.</span></span> <span data-ttu-id="27cc2-170">**必要なアクセス許可** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-170">Select **Required permissions**.</span></span>
6. <span data-ttu-id="27cc2-171">**追加** を選択し、**API を選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-171">Select **Add**, and then select **Select an API**.</span></span>
7. <span data-ttu-id="27cc2-172">**Microsoft Dynamics ERP** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-172">Select **Microsoft Dynamics ERP**.</span></span>
8. <span data-ttu-id="27cc2-173">**委任アクセス権** で、少なくとも次のオプションを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27cc2-173">Under **Delegated permissions**, you must select, at a minimum, the following options:</span></span>

    - <span data-ttu-id="27cc2-174">Dynamics AX カスタム サービスへのアクセス</span><span class="sxs-lookup"><span data-stu-id="27cc2-174">Access Dynamics AX Custom Service</span></span>
    - <span data-ttu-id="27cc2-175">Dynamics AX データへのアクセス</span><span class="sxs-lookup"><span data-stu-id="27cc2-175">Access Dynamics AX data</span></span>
    - <span data-ttu-id="27cc2-176">組織ユーザーとしての Dynamics AX オンラインへのアクセス</span><span class="sxs-lookup"><span data-stu-id="27cc2-176">Access Dynamics AX online as organization users</span></span>

9. <span data-ttu-id="27cc2-177">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-177">Select **Done**.</span></span>
10. <span data-ttu-id="27cc2-178">**キー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-178">Select **Keys**.</span></span> <span data-ttu-id="27cc2-179">表示されるダイアログ ボックスで、説明を入力し、**有効期限**の値を**無期限**に設定してから**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-179">In the dialog box that appears, enter a description, set the **Expires** value to **Never expires**, and then select **Save**.</span></span>

    <span data-ttu-id="27cc2-180">新しいキーを保存した後、**値**列に値が示されます。</span><span class="sxs-lookup"><span data-stu-id="27cc2-180">After you've saved the new key, a value appears in the **Value** column.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="27cc2-181">再度、表示することはないため、必ずこの値をコピーします。OAuth 認証を完了し、Azure AD トークンを受け取るには、この秘密キーが必要になります。</span><span class="sxs-lookup"><span data-stu-id="27cc2-181">Make sure that you copy this value, because you won't see it again, and you will require this secret key to complete your OAuth authentication and receive an Azure AD token.</span></span>

### <a name="register-your-external-application-in-finance-and-operations"></a><span data-ttu-id="27cc2-182">Finance and Operations で外部のアプリケーションを登録する</span><span class="sxs-lookup"><span data-stu-id="27cc2-182">Register your external application in Finance and Operations</span></span>

1. <span data-ttu-id="27cc2-183">Finance and Operations で、**システム管理** &gt; **セットアップ** &gt; **Azure Active Directory アプリケーション** に移動します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-183">In Finance and Operations, go to **System administration** &gt; **Setup** &gt; **Azure Active Directory applications**.</span></span>
2. <span data-ttu-id="27cc2-184">**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-184">Select **New**.</span></span>
3. <span data-ttu-id="27cc2-185">新しいレコード用のフィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-185">Fill in the fields for the new record:</span></span>

   - <span data-ttu-id="27cc2-186">**クライアント Id** フィールドで、Azure AD に登録したアプリケーション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-186">In the **Client Id** field, enter the application ID that you registered in Azure AD.</span></span>
   - <span data-ttu-id="27cc2-187">**名前**フィールドに、アプリケーションの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-187">In the **Name** field, enter a name for the application.</span></span>
   - <span data-ttu-id="27cc2-188">**ユーザー ID** フィールドで、適切なサービス アカウントのユーザー ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-188">In the **User ID** field, select an appropriate service account user ID.</span></span> <span data-ttu-id="27cc2-189">この例では、**管理者**ユーザーを選択しました。</span><span class="sxs-lookup"><span data-stu-id="27cc2-189">For this example, we have selected the **Admin** user.</span></span> <span data-ttu-id="27cc2-190">ただし、実行する必要がある操作に対して適切なアクセス許可を持つ、専用のサービス アカウントをプロビジョニングすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="27cc2-190">However, as a better practice, you should provision a dedicated service account that has the correct permissions for the operations that must be performed.</span></span>
    
     <span data-ttu-id="27cc2-191">完了したら、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-191">When you've finished, select **Save**.</span></span>

<span data-ttu-id="27cc2-192">これで、前提条件の設定を完了しました。</span><span class="sxs-lookup"><span data-stu-id="27cc2-192">You've now finished setting up the prerequisites.</span></span> <span data-ttu-id="27cc2-193">外部のアプリケーションが Azure AD Authentication トークンを取得した後、認証 HTTP ヘッダーのトークンを使用して、OData や SOAP などの後続のサービスの呼び出しを行うことができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="27cc2-193">After the external application retrieves an Azure AD authentication token, it should now be able to use the token in an authorization HTTP header to make subsequent service calls via OData or SOAP, for example.</span></span>


### <a name="client-sample-code"></a><span data-ttu-id="27cc2-194">クライアント サンプル コード</span><span class="sxs-lookup"><span data-stu-id="27cc2-194">Client sample code</span></span>

<span data-ttu-id="27cc2-195">次は、AAD からトークンを取得するための C# サンプル コードです。</span><span class="sxs-lookup"><span data-stu-id="27cc2-195">The following is C# sample code for getting a token from AAD.</span></span> <span data-ttu-id="27cc2-196">このフローで、同意フォーム (テナント間アプリケーション用) およびサインイン フォームがユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="27cc2-196">In this flow, the user will be presented with a consent form (for cross-tenant application) and a sign-in form.</span></span>

```
 UriBuilder uri = new UriBuilder ("https://login.windows.net/contoso2ax.onmicrosoft.com");
               
    AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

    //request token for the resource - which is the URI for your organization. NOTE: Important do not add a trailing slash at the end of the URI
    AuthenticationResult authenticationResult = authenticationContext.AcquireToken("https://axdynamics1001aos.cloud.dynamics.com", clientId, redirectURI);
                
    //this gets the authorization token, which needs to be passed in the Header of the HTTP Requests
    string authenticationHeader = authenticationResult.CreateAuthorizationHeader();
```

<span data-ttu-id="27cc2-197">ポップアップを表示せずにユーザー名とパスワードを渡すには、**AcquireToken** の次のオーバーロードを使用します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-197">To pass the user name and password without showing a pop-up, you can use the following overload of **AcquireToken**.</span></span>

```
    UserCredential userCred = new UserCredential (username, password);
    authenticationContext.AcquireToken("https://axdynamics1001aos.cloud.dynamics.com", clientId, userCred);
```

## <a name="rest-metadata-service"></a><span data-ttu-id="27cc2-198">REST メタデータ サービス</span><span class="sxs-lookup"><span data-stu-id="27cc2-198">REST Metadata Service</span></span>
<span data-ttu-id="27cc2-199">REST メタデータ サービスは、読み取り専用サービスです。</span><span class="sxs-lookup"><span data-stu-id="27cc2-199">The REST metadata service is a read-only service.</span></span> <span data-ttu-id="27cc2-200">つまり、ユーザーは GET 要求のみ生成できます。</span><span class="sxs-lookup"><span data-stu-id="27cc2-200">In other words, users can make only GET requests.</span></span> <span data-ttu-id="27cc2-201">このエンドポイントの主な目的は、要素のメタデータ情報を提供することです。</span><span class="sxs-lookup"><span data-stu-id="27cc2-201">The main purpose of this endpoint is to provide metadata information for elements.</span></span> <span data-ttu-id="27cc2-202">OData 実装です。</span><span class="sxs-lookup"><span data-stu-id="27cc2-202">It is an OData implementation.</span></span> 

<span data-ttu-id="27cc2-203">このエンドポイントは、`http://\[baseURI\]/Metadata` でホストされています。</span><span class="sxs-lookup"><span data-stu-id="27cc2-203">This endpoint is hosted at `http://\[baseURI\]/Metadata`.</span></span>

<span data-ttu-id="27cc2-204">現在、このエンドポイントは、次の要素のメタデータを提供します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-204">Currently, this endpoint provides metadata for the following elements:</span></span>

-   <span data-ttu-id="27cc2-205">**ラベル** – システムからラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-205">**Labels** – Returns labels from the system.</span></span> <span data-ttu-id="27cc2-206">ラベルには言語と ID のデュアル ペア キーがあり、ラベルの値を取得できます。</span><span class="sxs-lookup"><span data-stu-id="27cc2-206">Labels have a dual pair key of language and ID, so that you can retrieve the value of the label.</span></span> 

    <span data-ttu-id="27cc2-207">**例:** `https://[baseURI\]/metadata/Labels(Id='@SVC\_ODataLabelFile:Label1',Language='en-us')`</span><span class="sxs-lookup"><span data-stu-id="27cc2-207">**Example:** `https://[baseURI\]/metadata/Labels(Id='@SVC\_ODataLabelFile:Label1',Language='en-us')`</span></span>

-   <span data-ttu-id="27cc2-208">**データ エンティティ** - システム内のすべてのデータ エンティティの JSON 形式の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="27cc2-208">**Data entities** – Returns a JSON-formatted list of all the data entities in the system.</span></span> 

    <span data-ttu-id="27cc2-209">**例:** `https://[baseURI\]/Metadata/DataEntities`</span><span class="sxs-lookup"><span data-stu-id="27cc2-209">**Example:** `https://[baseURI\]/Metadata/DataEntities`</span></span>
