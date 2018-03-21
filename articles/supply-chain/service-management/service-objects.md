---
title: "サービス対象"
description: "サービス対象とは、サービスを実行する顧客の製品および資産です。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: a69fd6a1b07683383d88c7f5c7986529c7bb1875
ms.contentlocale: ja-jp
ms.lasthandoff: 02/21/2018

---

# <a name="service-objects"></a><span data-ttu-id="20527-103">サービス対象</span><span class="sxs-lookup"><span data-stu-id="20527-103">Service objects</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="20527-104">サービス対象とは、サービスを実行する顧客の製品および資産です。</span><span class="sxs-lookup"><span data-stu-id="20527-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="20527-105">提供するサービスのタイプに応じて、有形または無形の対象を使用できます。</span><span class="sxs-lookup"><span data-stu-id="20527-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="20527-106">有形の対象は、機械や建物などの物です。有形の対象では、物理的なサービス作業を実行できます。</span><span class="sxs-lookup"><span data-stu-id="20527-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="20527-107">有形のサービス対象はさらに、[リリース済製品の詳細] フォームで作成する在庫品目にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="20527-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="20527-108">品目に関連付ける在庫分析コード グループに応じて、品目シリアル番号を含む詳細のレベルへのサービス対象を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="20527-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="20527-109">これは、サービス対象が表す正確な品目を追跡する必要がある場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="20527-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="20527-110">有形のサービス対象はさらに、会社の直接生産またはサプライ チェーンに直接関係しない品目とすることもできます。</span><span class="sxs-lookup"><span data-stu-id="20527-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="20527-111">たとえば、サービス注文の修復に使用されるツールキットは棚卸資産に含まれていないサービス対象とすることができます。</span><span class="sxs-lookup"><span data-stu-id="20527-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="20527-112">この場合、在庫品目として登録されません。</span><span class="sxs-lookup"><span data-stu-id="20527-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="20527-113">無形の対象は、勘定のセットや法的文書などの非物質的なもので、サービス作業は、これらの無形の対象に基づいて実行できます。</span><span class="sxs-lookup"><span data-stu-id="20527-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="20527-114">無形のサービス対象の例</span><span class="sxs-lookup"><span data-stu-id="20527-114">Example of an intangible service object</span></span>

<span data-ttu-id="20527-115">会社 A は複数の小規模な会社の財務レコードを管理します。</span><span class="sxs-lookup"><span data-stu-id="20527-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="20527-116">会社 A の顧客の 1 つはローカル フットボール チームで、それに対して、会社 A はクラブの口座の週次簿記および年次監査を行います。</span><span class="sxs-lookup"><span data-stu-id="20527-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="20527-117">クラブの口座は [サービス対象] フォームで設定され、対象としてサービス契約で指定されます。</span><span class="sxs-lookup"><span data-stu-id="20527-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="20527-118">対象には 2 つのサービス契約明細行があります。</span><span class="sxs-lookup"><span data-stu-id="20527-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="20527-119">行 1 は明細行に割り当てられている週次間隔の週次簿記で、行 2 はそれに割り当てられている年次間隔の年次監査です。</span><span class="sxs-lookup"><span data-stu-id="20527-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20527-120">関連トピック</span><span class="sxs-lookup"><span data-stu-id="20527-120">Related topics</span></span>

[<span data-ttu-id="20527-121">サービス対象の作成</span><span class="sxs-lookup"><span data-stu-id="20527-121">Create service objects</span></span>](create-service-objects.md)

