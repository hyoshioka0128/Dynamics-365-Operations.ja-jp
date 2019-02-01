---
title: "Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 9 月 17 日)"
description: "このトピックでは、Microsoft Dynamics 365 for Talent Core HR の新機能または変更された機能について説明します。"
author: Darinkramer
manager: AnnBe
ms.date: 09/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-14
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 1aae5797e37b846a38f957b02870e213da528a2d
ms.openlocfilehash: 6586761fc62c13c701e8a8f61e15eedc66e2f751
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-17-2018"></a><span data-ttu-id="3ce4c-103">Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 9 月 17 日)</span><span class="sxs-lookup"><span data-stu-id="3ce4c-103">What's new or changed in Dynamics 365 for Talent Core HR (September 17, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3ce4c-104">**ビルド 8.1.154.0**</span><span class="sxs-lookup"><span data-stu-id="3ce4c-104">**Build 8.1.154.0**</span></span>

<span data-ttu-id="3ce4c-105">このトピックでは、Core HR の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="3ce4c-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="leave-and-absence--accrue-time-based-on-hours-worked"></a><span data-ttu-id="3ce4c-106">休暇と欠勤 – 作業時間に基づく見越計上時間</span><span class="sxs-lookup"><span data-stu-id="3ce4c-106">Leave and Absence – Accrue time based on hours worked</span></span>

<span data-ttu-id="3ce4c-107">新しい見越計上タイプが休暇計画に追加されました。</span><span class="sxs-lookup"><span data-stu-id="3ce4c-107">A new accrual type has been added to Leave plans.</span></span> <span data-ttu-id="3ce4c-108">見越計上スケジュールは、勤続月数または作業時間に基づくようになりました。</span><span class="sxs-lookup"><span data-stu-id="3ce4c-108">The accrual schedule can now be based on months of service or hours worked.</span></span> <span data-ttu-id="3ce4c-109">詳細については、[作業時間に基づいて休暇を見越計上する](leave-accrue-hours-worked.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ce4c-109">For more information, see [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

## <a name="platform-update-18"></a><span data-ttu-id="3ce4c-110">プラットフォーム update 18</span><span class="sxs-lookup"><span data-stu-id="3ce4c-110">Platform update 18</span></span>

<span data-ttu-id="3ce4c-111">プラットフォーム更新プログラム 18 は Talent リリースの一部になりました。</span><span class="sxs-lookup"><span data-stu-id="3ce4c-111">Platform update 18 is now part of the Talent release.</span></span> 

-   <span data-ttu-id="3ce4c-112">必須フィールドおよびその他のフィールドは、個人用設定により非表示にすることができます。</span><span class="sxs-lookup"><span data-stu-id="3ce4c-112">Mandatory and other fields can be hidden via personalization.</span></span> <span data-ttu-id="3ce4c-113">これによりユーザーは、ビジネス ロジックにより既定に設定されている必須フィールドが表示されない、簡略化された経験を作成できます。</span><span class="sxs-lookup"><span data-stu-id="3ce4c-113">This allows a user to create a simplified experience where mandatory fields that are defaulted by business logic are not shown.</span></span> <span data-ttu-id="3ce4c-114">非表示の必須フィールドは、保存しようとするときに空の場合には一時的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ce4c-114">Hidden mandatory fields are also temporarily made visible if they are empty when a save is attempted.</span></span>

-   <span data-ttu-id="3ce4c-115">プラットフォーム更新プログラム 18 では、Talent の Web クライアントは Microsoft Fluent Design とのビジュアルに対応するようになります。</span><span class="sxs-lookup"><span data-stu-id="3ce4c-115">In Platform update 18, the Talent web client now aligns its visuals with Microsoft Fluent Design.</span></span>

    -   <span data-ttu-id="3ce4c-116">フィールドが “読み取りモード“ である場合、単にフィールドで編集オプションを選択して、編集するフォームを切り替えます。</span><span class="sxs-lookup"><span data-stu-id="3ce4c-116">When fields are in “read mode”, you can simply select the edit option in the fields to switch the form to edit.</span></span>

    -   <span data-ttu-id="3ce4c-117">読み取りモードでのフィールドの表示方法を変更します。</span><span class="sxs-lookup"><span data-stu-id="3ce4c-117">Changes in how fields display when in read mode.</span></span>

    -   <span data-ttu-id="3ce4c-118">ワークスペースとページのヘッダーは太字です。</span><span class="sxs-lookup"><span data-stu-id="3ce4c-118">Headings in workspaces and pages are bold.</span></span>

-   <span data-ttu-id="3ce4c-119">非置き換えルックアップの動作が改良されました。</span><span class="sxs-lookup"><span data-stu-id="3ce4c-119">The behavior of non-replacing lookups has been improved.</span></span> <span data-ttu-id="3ce4c-120">詳細については、[非置き換えルックアップの動作の改良](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ce4c-120">For more information, see [Improved behavior for non-replacing lookups](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).</span></span>

## <a name="bug-fixes"></a><span data-ttu-id="3ce4c-121">バグ修正</span><span class="sxs-lookup"><span data-stu-id="3ce4c-121">Bug fixes</span></span>

<span data-ttu-id="3ce4c-122">このリリースには ACA、ADA、および I9 への参照を含むいくつかの追加のバグ修正が含まれ、米国企業でのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="3ce4c-122">This release includes several additional bug fixes, including references to ACA, ADA, and I9 now will only be enabled in US companies.</span></span>
