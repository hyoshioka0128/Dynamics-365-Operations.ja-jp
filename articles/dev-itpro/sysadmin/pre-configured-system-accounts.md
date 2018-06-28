---
title: "コンフィギュレーション済みのシステム アカウント"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations 環境で事前設定されているシステム アカウントについて説明します。"
author: manalidongre
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: 
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2017-11-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fdf9a55dc3f528ed5ad726c315a1c97fd5b568ca
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="pre-configured-system-accounts"></a><span data-ttu-id="6d79e-103">コンフィギュレーション済みのシステム アカウント</span><span class="sxs-lookup"><span data-stu-id="6d79e-103">Pre-configured system accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d79e-104">構成済みのシステム アカウントは、Microsoft が Dynamics 365 for Finance and Operations サービスを管理および運用し、特定の機能をユーザーに提供できるように、配置された環境に含まれます。</span><span class="sxs-lookup"><span data-stu-id="6d79e-104">Pre-configured system accounts are included on deployed environments so that Microsoft can manage and operate the Dynamics 365 for Finance and Operations service and provide specific features to customers.</span></span> <span data-ttu-id="6d79e-105">次のテーブルは、アカウントの目的とユース ケースを含む、各アカウントに関する情報を示しています。</span><span class="sxs-lookup"><span data-stu-id="6d79e-105">The following table provides information about each account, including the purpose and use case for the account.</span></span>  

> [!IMPORTANT] 
> <span data-ttu-id="6d79e-106">システム アカウントを削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="6d79e-106">Do not delete these system accounts.</span></span> <span data-ttu-id="6d79e-107">これらの勘定を削除すると、Microsoft が提供する主要な機能が中断されます。</span><span class="sxs-lookup"><span data-stu-id="6d79e-107">Deleting these accounts will cause a disruption in key functionality provided by Microsoft.</span></span>

|                               <span data-ttu-id="6d79e-108">口座の詳細</span><span class="sxs-lookup"><span data-stu-id="6d79e-108">Account detail</span></span>                               |                                                                    <span data-ttu-id="6d79e-109">アカウントの目的/ユース ケース</span><span class="sxs-lookup"><span data-stu-id="6d79e-109">Purpose/use case of the account</span></span>                                                                    |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                  <span data-ttu-id="6d79e-110">Axrunner</span><span class="sxs-lookup"><span data-stu-id="6d79e-110">Axrunner</span></span>                                  |                                   <span data-ttu-id="6d79e-111">このアカウントは、環境の稼働状態を監視し、必要に応じて警告を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d79e-111">This account is used to monitor the health of the environment and provide alerts when necessary.</span></span>                                    |
|                               <span data-ttu-id="6d79e-112">FRServiceUser</span><span class="sxs-lookup"><span data-stu-id="6d79e-112">FRServiceUser</span></span>                                | <span data-ttu-id="6d79e-113">これは、財務諸表サービスのユーザー アカウントで、Management Reporter アプリケーションが Dynamics 365 for Unified Operations に使用します。</span><span class="sxs-lookup"><span data-stu-id="6d79e-113">This is the Financial Reporting service user account, which is used by the Management Reporter application for integrations with Dynamics 365 for Unified Operations.</span></span> |
|                            <span data-ttu-id="6d79e-114">RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="6d79e-114">RetailServiceAccount</span></span>                            |                              <span data-ttu-id="6d79e-115">このアカウントは、Retail サービスで Dynamics 365 for Unified Operations 環境に接続するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d79e-115">This account is used for Retail services to connect to the Dynamics 365 for Unified Operations environment.</span></span>                              |
| <span data-ttu-id="6d79e-116">SysHealthServiceUser または Axping (展開された製品バージョンによって異なる)</span><span class="sxs-lookup"><span data-stu-id="6d79e-116">SysHealthServiceUser or Axping (depending on the deployed product version)</span></span> |                           <span data-ttu-id="6d79e-117">このアカウントは、環境の可用性と稼働状態を監視し、必要に応じて警告を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d79e-117">This account is used to monitor the availability and health of the environment and provide alerts when necessary.</span></span>                           |

