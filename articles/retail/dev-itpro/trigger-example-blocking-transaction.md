---
title: "トリガーを使用してトランザクションをブロックする"
description: "このトピックでは、トリガーを使用して請求書またはクレジット取引をブロックする方法を示します。"
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 65893
ms.assetid: 605f5986-f84f-4b18-b94e-b0912cb367a1
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9a826c0fcffe1f13a2fde344fc3a696aa883fc03
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="block-a-transaction-using-triggers"></a><span data-ttu-id="71db7-103">トリガーを使用してトランザクションをブロックする</span><span class="sxs-lookup"><span data-stu-id="71db7-103">Block a transaction using triggers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71db7-104">このトピックでは、トリガーを使用して請求書またはクレジット取引をブロックする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="71db7-104">This topic shows how you can use a trigger to block an invoice or credit transaction.</span></span>

<span data-ttu-id="71db7-105">このトピックでは、請求書またはクレジット取引をブロックする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="71db7-105">This topic shows how you can block an invoice or credit transaction.</span></span>

1.  <span data-ttu-id="71db7-106">管理者として Visual Studio を開きます。</span><span class="sxs-lookup"><span data-stu-id="71db7-106">Open Visual Studio as an administrator.</span></span> <span data-ttu-id="71db7-107">新しい Visual C\# クラス ライブラリ (ポータブル) プロジェクトを作成し、CRTTriggerExtension という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="71db7-107">Create a new Visual C\# Class Library (Portable) project and name it CRTTriggerExtension.</span></span> <span data-ttu-id="71db7-108">選択内容によってこのプロジェクトが Visual Studio 2010 と互換性がなくなるというメッセージが表示される場合、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71db7-108">If you get a message that the selection makes this project incompatible with Visual Studio 2010, click **OK**.</span></span>
2.  <span data-ttu-id="71db7-109">ソリューション エクスプローラーで、既定の class1.cs を GetCustomersServiceRequestTrigger.cs に名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="71db7-109">In Solution Explorer, rename default class1.cs to GetCustomersServiceRequestTrigger.cs.</span></span>
3.  <span data-ttu-id="71db7-110">プロジェクトで **参照** ノードを右クリックし、次の参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="71db7-110">Right-click the **Reference** node in the project and add the following references.</span></span> <span data-ttu-id="71db7-111">参照の場所は、配置トポロジによって異なります。</span><span class="sxs-lookup"><span data-stu-id="71db7-111">The location of the references will depend on the deployment topology.</span></span>
    -   <span data-ttu-id="71db7-112">Microsoft.Dynamics.Commerce.Runtime.Entities.dll</span><span class="sxs-lookup"><span data-stu-id="71db7-112">Microsoft.Dynamics.Commerce.Runtime.Entities.dll</span></span>
    -   <span data-ttu-id="71db7-113">Microsoft.Dynamics.Commerce.Runtime.Framework.dll</span><span class="sxs-lookup"><span data-stu-id="71db7-113">Microsoft.Dynamics.Commerce.Runtime.Framework.dll</span></span>
    -   <span data-ttu-id="71db7-114">Microsoft.Dynamics.Commerce.Runtime.Services.Messages.dll</span><span class="sxs-lookup"><span data-stu-id="71db7-114">Microsoft.Dynamics.Commerce.Runtime.Services.Messages.dll</span></span>

4.  <span data-ttu-id="71db7-115">GetCustomersServiceRequestTrigger.cs ファイルに、次の明細書を**使用して**追加します。</span><span class="sxs-lookup"><span data-stu-id="71db7-115">Add the following **using** statement to the GetCustomersServiceRequestTrigger.cs file.</span></span>

        using Microsoft.Dynamics.Commerce.Runtime.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;
        using Microsoft.Dynamics.Commerce.Runtime;

5.  <span data-ttu-id="71db7-116">コードの class1.cs の名前を GetCustomersServiceRequestTrigger に変更し、IRequestTrigger インターフェイス宣言を追加します。</span><span class="sxs-lookup"><span data-stu-id="71db7-116">Rename class1.cs in the code to GetCustomersServiceRequestTrigger and then add the IRequestTrigger interface declaration.</span></span>

        using System;
        using System.Collections.Generic;
        using System.Linq;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;

        namespace CRTTriggerExtension
        public class GetCustomersServiceRequestTrigger : IRequestTrigger
        {

6.  <span data-ttu-id="71db7-117">IRequestTrigger インターフェイス トリガーを実装します。</span><span class="sxs-lookup"><span data-stu-id="71db7-117">Implement the IRequestTrigger interface trigger.</span></span> <span data-ttu-id="71db7-118">IRequestTrigger クラスを右クリックして、**クイック アクション** をクリックし、**インターフェイスの実装** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71db7-118">Right-click the IRequestTrigger class, select **Quick Actions**, and then click **Implement Interface**.</span></span> <span data-ttu-id="71db7-119">Visual Studio はインターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="71db7-119">Visual Studio will implement the interface.</span></span> <span data-ttu-id="71db7-120">また、カーソルを IRequestTrigger の上に配置して、**Ctrl+** を押し、**インターフェイスの実装** を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="71db7-120">You can also place the cursor on IRequestTrigger, press **Ctrl+**, and select **Implement Interface**.</span></span>
7.  <span data-ttu-id="71db7-121">空のインターフェイス メンバー SupportedRequestTypes、OnExecuted、および OnExecuting メソッドを次のコード例に示します。</span><span class="sxs-lookup"><span data-stu-id="71db7-121">The empty interface members SupportedRequestTypes, OnExecuted, and OnExecuting methods are shown in the following code example.</span></span>

        public class GetCustomersServiceRequestTrigger : IRequestTrigger
        {
            public IEnumerable<Type> SupportedRequestTypes
            {
                get
                {
                    throw new NotImplementedException();
                }
            }

            public void OnExecuted(Request request, Response response)
            {
                throw new NotImplementedException();
            }

            public void OnExecuting(Request request)
            {
                throw new NotImplementedException();
            } 
        }

8.  <span data-ttu-id="71db7-122">Retail Server は、GetCustomersServiceRequest オブジェクトを使用して Commerce Runtime (CRT) から顧客詳細を取得し、GetCustomersServiceRequest オブジェクトを使用して顧客をトランザクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="71db7-122">Retail Server uses the GetCustomersServiceRequest object to get the customer details from Commerce Runtime (CRT) and uses the GetCustomersServiceRequest object to add the customer to the transaction.</span></span> <span data-ttu-id="71db7-123">トランザクションに顧客を追加する前に、顧客がブロックされているかどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71db7-123">Before adding the customer to the transaction you need to check whether the customer is blocked.</span></span> <span data-ttu-id="71db7-124">これを行うには、この要求の転記トリガーを実装し、顧客がブロックされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="71db7-124">To do this, implement a post trigger for this request and check whether the customer is blocked.</span></span> <span data-ttu-id="71db7-125">顧客がブロックされている場合、MPOS によって例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="71db7-125">If the customer is blocked, then throw the exception to MPOS.</span></span>
9.  <span data-ttu-id="71db7-126">SupportedRequestTypes メソッドで、GetCustomersServiceRequest のトリガーを追加することを CRT に通知します。</span><span class="sxs-lookup"><span data-stu-id="71db7-126">In the SupportedRequestTypes method tell the CRT that you are going to add the trigger for GetCustomersServiceRequest.</span></span> <span data-ttu-id="71db7-127">次のコード例は、GetCustomersServiceRequest をサポートされている型として追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="71db7-127">The following code example shows how to add GetCustomersServiceRequest as a supported type.</span></span>

        public IEnumerable<Type> SupportedRequestTypes
        {
            get
            {
                return new[] { typeof(GetCustomersServiceRequest) };       
            }
        }

10. <span data-ttu-id="71db7-128">顧客が次のコードで OnExecuted (転記トリガー) メソッドでブロックされているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="71db7-128">Check if the customer is blocked in the OnExecuted (post trigger) method with the following code.</span></span>

        public void OnExecuted(Request request, Response response)
        {
            if (response == null)
            {
            throw new ArgumentNullException("request");
            }

            var getCustomersServiceResponse = (GetCustomersServiceResponse)response;
            if(getCustomersServiceResponse.Customers.FirstOrDefault().Blocked == true)
            {
                string message = string.Format("Failed to add customer '{0}' to cart. Blocked customers are not allowed for transactions.",
                    getCustomersServiceResponse.Customers.FirstOrDefault().AccountNumber);
                throw new CartValidationException(DataValidationErrors.Microsoft_Dynamics_Commerce_Runtime_CustomerAccountIsBlocked, message);
            }
        }

11. <span data-ttu-id="71db7-129">最後に、次のコードで OnExecuting メソッドを更新します。</span><span class="sxs-lookup"><span data-stu-id="71db7-129">Finally, update the OnExecuting method with the following code.</span></span>

        public void OnExecuting(Request request) 
        {
            if (request == null)
            {
                throw new ArgumentNullException("request");
            }
        }

12. <span data-ttu-id="71db7-130">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71db7-130">Click **Save**.</span></span>




