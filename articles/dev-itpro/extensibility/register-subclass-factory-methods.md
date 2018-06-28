---
title: "ファクトリ メソッドのサブクラスの登録"
description: "このトピックでは、独自のバリエーションを工場に登録する方法について説明します。"
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 07/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: 
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c6fec3b784c0baee21fe7a08b34e5ec14f99ad5f
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="register-a-subclass-for-factory-methods"></a><span data-ttu-id="9c119-103">ファクトリ メソッドのサブクラスの登録</span><span class="sxs-lookup"><span data-stu-id="9c119-103">Register a subclass for factory methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c119-104">クラス継承は、他のオブジェクト指向言語と同様に、X++ の中心的概念です。</span><span class="sxs-lookup"><span data-stu-id="9c119-104">Class inheritance is a central concept in X++, as in other object-oriented languages.</span></span> <span data-ttu-id="9c119-105">オブジェクト指向戦略パターンは、X++ ビジネス ロジック全体で使用されます。</span><span class="sxs-lookup"><span data-stu-id="9c119-105">The object-oriented strategy pattern is used throughout the X++ business logic.</span></span> <span data-ttu-id="9c119-106">このパターンでは、動作のバリエーションをサブクラスでカプセル化することができ、業務プロセスが抽象基本クラスまたはインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="9c119-106">In this pattern, variations in behavior can be encapsulated by subclasses, and the business process uses an abstract base class or interface.</span></span> <span data-ttu-id="9c119-107">ファクトリ メソッドは、特定のサブクラスのインスタンスを作成することによって、使用されるバリエーションを決定します。</span><span class="sxs-lookup"><span data-stu-id="9c119-107">A factory method determines the variation that is used, by creating an instance of a specific subclass.</span></span>

<span data-ttu-id="9c119-108">このトピックでは、独自のバリエーションを工場に登録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9c119-108">This topic describes how to register your own variations for the factories.</span></span>

<span data-ttu-id="9c119-109">X++ では、ファクトリはリフレクションを使用して、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="9c119-109">In X++, the factories use reflection to perform the following tasks:</span></span>

+ <span data-ttu-id="9c119-110">正しいサブクラスを検索します。</span><span class="sxs-lookup"><span data-stu-id="9c119-110">Find the correct subclass.</span></span> <span data-ttu-id="9c119-111">ファクトリは、拡張フレームワークを使用して、階層内のすべてのサブクラスで特定の属性セットを検索します。</span><span class="sxs-lookup"><span data-stu-id="9c119-111">The factory uses an extension framework to search all subclasses in a hierarchy for a specific set of attributes.</span></span> <span data-ttu-id="9c119-112">サブクラスを修飾する属性がファクトリに渡されたパラメータと一致する場合、その特定のクラスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="9c119-112">If the attributes that decorate a subclass match the parameters that were passed to the factory, that specific class is used.</span></span>
+ <span data-ttu-id="9c119-113">インスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c119-113">Create an instance.</span></span> <span data-ttu-id="9c119-114">正しいタイプが識別された後、リフレクションを使用してクラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c119-114">After the right type is identified, reflection is used to create an instance of the class.</span></span>

<span data-ttu-id="9c119-115">次の図は、一般的な装飾階層を示しています。</span><span class="sxs-lookup"><span data-stu-id="9c119-115">The following illustrations shows a typical decorated hierarchy.</span></span>

![各サブクラスが属性で装飾されている、3 つのサブクラスを持つクラス階層](media/hierarchy.png)

<span data-ttu-id="9c119-117">X++ では、2 つの拡張フレームワークは同じ目的で機能します。</span><span class="sxs-lookup"><span data-stu-id="9c119-117">In X++, two extension frameworks serve the same purpose.</span></span> <span data-ttu-id="9c119-118">ファクトリ メソッドの実装担当者は、使用する拡張フレームワークを決定します。</span><span class="sxs-lookup"><span data-stu-id="9c119-118">The implementer of the factory method determines which extension framework should be used:</span></span>

+ [<span data-ttu-id="9c119-119">SysExtension</span><span class="sxs-lookup"><span data-stu-id="9c119-119">SysExtension</span></span>](https://blogs.msdn.microsoft.com/mfp/2013/06/12/sysextension-framework-to-the-rescue/)

  - <span data-ttu-id="9c119-120">この拡張フレームワークは、利用しやすくするためにカスタム属性を使用します。</span><span class="sxs-lookup"><span data-stu-id="9c119-120">This extension framework uses custom attributes that make it easier to consume.</span></span>
  - <span data-ttu-id="9c119-121">同じインスタンスが繰り返し作成されるときに、パフォーマンスを多少節約する単一をサポートします。</span><span class="sxs-lookup"><span data-stu-id="9c119-121">It supports singletons that save a little performance when the same instance is created repeatedly.</span></span> <span data-ttu-id="9c119-122">この拡張フレームワークは、ステートレスなサブクラスに特に便利です。</span><span class="sxs-lookup"><span data-stu-id="9c119-122">This extension framework is especially useful for stateless subclasses.</span></span>
  - <span data-ttu-id="9c119-123">バリアントを決定するために頻繁に使用される拡張可能な列挙をシームレスにサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9c119-123">It seamlessly supports extensible enums that are often used to determine the variant.</span></span>

+ <span data-ttu-id="9c119-124">SysPlugin</span><span class="sxs-lookup"><span data-stu-id="9c119-124">SysPlugin</span></span>

  - <span data-ttu-id="9c119-125">この拡張フレームワークは、Managed Extension Framework に基づいています。</span><span class="sxs-lookup"><span data-stu-id="9c119-125">This extension framework is based on the Managed Extension Framework.</span></span> <span data-ttu-id="9c119-126">マネージ拡張フレームワークは、SysPlugin 拡張フレームワークを非 X++ コードで使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="9c119-126">The Managed Extension Framework makes the SysPlugin extension framework available to non-X++ code.</span></span>
  - <span data-ttu-id="9c119-127">**ExportMetadataAttribute** 属性を使用してバリアントを修飾し、文字列ベースとなります。</span><span class="sxs-lookup"><span data-stu-id="9c119-127">It uses the **ExportMetadataAttribute** attribute to decorate the variants and is string-based.</span></span>
  - <span data-ttu-id="9c119-128">**ExportAttribute** 属性を使用してバリアントを見つけやすくします。</span><span class="sxs-lookup"><span data-stu-id="9c119-128">It uses the **ExportAttribute** attribute to make the variant discoverable.</span></span>

## <a name="introduce-a-new-variant"></a><span data-ttu-id="9c119-129">新しいバリアントの導入</span><span class="sxs-lookup"><span data-stu-id="9c119-129">Introduce a new variant</span></span>

1. <span data-ttu-id="9c119-130">実装する必要があるバリアントの基本クラス (またはインタフェース) を特定します。</span><span class="sxs-lookup"><span data-stu-id="9c119-130">Identify the base class (or interface) of the variant that you must implement.</span></span>
2. <span data-ttu-id="9c119-131">基本クラスの新しいサブクラスを作成し、バリエーションを実装します。</span><span class="sxs-lookup"><span data-stu-id="9c119-131">Create a new subclass of the base class, and implement your variation.</span></span>
3. <span data-ttu-id="9c119-132">クラスを登録するために必要となる属性を識別します。</span><span class="sxs-lookup"><span data-stu-id="9c119-132">Identify which attribute is required in order to register your class.</span></span> <span data-ttu-id="9c119-133">次の 2 つのアプローチがあります。</span><span class="sxs-lookup"><span data-stu-id="9c119-133">There are two approaches:</span></span>

    + <span data-ttu-id="9c119-134">階層内のその他のサブクラスで定義されている属性を検索します。</span><span class="sxs-lookup"><span data-stu-id="9c119-134">Look for attributes that are defined on other subclasses in the hierarchy.</span></span>
    + <span data-ttu-id="9c119-135">ファクトリ メソッドの実装を確認します。</span><span class="sxs-lookup"><span data-stu-id="9c119-135">Look at the implementation of the factory method.</span></span> <span data-ttu-id="9c119-136">その実装には、ファクトリ メソッドが検索する属性が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9c119-136">That implementation will contain the attributes that the factory method is searching for.</span></span>

4. <span data-ttu-id="9c119-137">バリエーションに一致するために使用された属性でサブクラスを修飾します。</span><span class="sxs-lookup"><span data-stu-id="9c119-137">Decorate your subclass with the attribute that was used to match your variation.</span></span>

<span data-ttu-id="9c119-138">**SysExtension 例**</span><span class="sxs-lookup"><span data-stu-id="9c119-138">**SysExtension example**</span></span>

    [WHSWorkExecuteMode(WHSWorkExecuteMode::About)]
    class WHSWorkExecuteDisplayAbout extends WHSWorkExecuteDisplay
    {
        // Your code here.
    }

<span data-ttu-id="9c119-139">**SysPlugin 例**</span><span class="sxs-lookup"><span data-stu-id="9c119-139">**SysPlugin example**</span></span>

    [ExportMetadataAttribute('CaseIAssociation', 'Lead'),
    ExportAttribute('Dynamics.AX.Application.CaseIAssociation')]
    class smmLeadCaseAssociationProvider implements CaseIAssociation
    {
        // Your code here.
    }
