---
title: GroupMetadata
description: "グループ メタデータ タイプ。"
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: 
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 680865f02d8ac3714a8a7d91759ad0fc09e05b7e
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="groupmetadata-type"></a><span data-ttu-id="7fe55-103">GroupMetadata タイプ</span><span class="sxs-lookup"><span data-stu-id="7fe55-103">GroupMetadata Type</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="7fe55-104">グループ メタデータ タイプ。</span><span class="sxs-lookup"><span data-stu-id="7fe55-104">Group metadata type.</span></span>

### <a name="hierarchy"></a><span data-ttu-id="7fe55-105">階層</span><span class="sxs-lookup"><span data-stu-id="7fe55-105">Hierarchy</span></span>

[<span data-ttu-id="7fe55-106">ContainerControlMetadata</span><span class="sxs-lookup"><span data-stu-id="7fe55-106">ContainerControlMetadata</span></span>](view-model-control-container-icontainercontrol-icontainercontrolmetadata.md) <br><span data-ttu-id="7fe55-107">&nbsp;&nbsp;&nbsp;└─ GroupMetadata</span><span class="sxs-lookup"><span data-stu-id="7fe55-107">&nbsp;&nbsp;&nbsp;└─ GroupMetadata</span></span> <br>

## <a name="index"></a><span data-ttu-id="7fe55-108">指数</span><span class="sxs-lookup"><span data-stu-id="7fe55-108">Index</span></span>

### <a name="properties"></a><span data-ttu-id="7fe55-109">プロパティ</span><span class="sxs-lookup"><span data-stu-id="7fe55-109">Properties</span></span>

* [<span data-ttu-id="7fe55-110">BoundEntity</span><span class="sxs-lookup"><span data-stu-id="7fe55-110">BoundEntity</span></span>](view-model-control-group-igroup-igroupmetadata.md#boundentity)
* [<span data-ttu-id="7fe55-111">BoundField</span><span class="sxs-lookup"><span data-stu-id="7fe55-111">BoundField</span></span>](view-model-control-group-igroup-igroupmetadata.md#boundfield)
* [<span data-ttu-id="7fe55-112">子</span><span class="sxs-lookup"><span data-stu-id="7fe55-112">Children</span></span>](view-model-control-group-igroup-igroupmetadata.md#children)
* [<span data-ttu-id="7fe55-113">説明</span><span class="sxs-lookup"><span data-stu-id="7fe55-113">Description</span></span>](view-model-control-group-igroup-igroupmetadata.md#description)
* [<span data-ttu-id="7fe55-114">編集可能</span><span class="sxs-lookup"><span data-stu-id="7fe55-114">Editable</span></span>](view-model-control-group-igroup-igroupmetadata.md#editable)
* [<span data-ttu-id="7fe55-115">ExtType</span><span class="sxs-lookup"><span data-stu-id="7fe55-115">ExtType</span></span>](view-model-control-group-igroup-igroupmetadata.md#exttype)
* [<span data-ttu-id="7fe55-116">HelpText</span><span class="sxs-lookup"><span data-stu-id="7fe55-116">HelpText</span></span>](view-model-control-group-igroup-igroupmetadata.md#helptext)
* [<span data-ttu-id="7fe55-117">非表示</span><span class="sxs-lookup"><span data-stu-id="7fe55-117">Hidden</span></span>](view-model-control-group-igroup-igroupmetadata.md#hidden)
* [<span data-ttu-id="7fe55-118">ID</span><span class="sxs-lookup"><span data-stu-id="7fe55-118">Id</span></span>](view-model-control-group-igroup-igroupmetadata.md#id)
* [<span data-ttu-id="7fe55-119">ラベル</span><span class="sxs-lookup"><span data-stu-id="7fe55-119">Label</span></span>](view-model-control-group-igroup-igroupmetadata.md#label)
* [<span data-ttu-id="7fe55-120">名前</span><span class="sxs-lookup"><span data-stu-id="7fe55-120">Name</span></span>](view-model-control-group-igroup-igroupmetadata.md#name)
* [<span data-ttu-id="7fe55-121">注文</span><span class="sxs-lookup"><span data-stu-id="7fe55-121">Order</span></span>](view-model-control-group-igroup-igroupmetadata.md#order)
* <span data-ttu-id="7fe55-122">[[タイプ](view-model-control-group-igroup-igroupmetadata.md#type)]</span><span class="sxs-lookup"><span data-stu-id="7fe55-122">[Type](view-model-control-group-igroup-igroupmetadata.md#type)</span></span>

## <a name="properties"></a><span data-ttu-id="7fe55-123">プロパティ</span><span class="sxs-lookup"><span data-stu-id="7fe55-123">Properties</span></span>

### <a name="boundentity"></a><span data-ttu-id="7fe55-124">BoundEntity</span><span class="sxs-lookup"><span data-stu-id="7fe55-124">BoundEntity</span></span>

<span data-ttu-id="7fe55-125">BoundEntity: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="7fe55-125">BoundEntity: string (optional)</span></span> 

<span data-ttu-id="7fe55-126">コントロールがバインドされるエンティティ。</span><span class="sxs-lookup"><span data-stu-id="7fe55-126">The entity to which the control is bound.</span></span>

> <span data-ttu-id="7fe55-127">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundEntity](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity) から継承</span><span class="sxs-lookup"><span data-stu-id="7fe55-127">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundEntity](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundentity)</span></span>


### <a name="boundfield"></a><span data-ttu-id="7fe55-128">BoundField</span><span class="sxs-lookup"><span data-stu-id="7fe55-128">BoundField</span></span>

<span data-ttu-id="7fe55-129">BoundField: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="7fe55-129">BoundField: string (optional)</span></span> 



> <span data-ttu-id="7fe55-130">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundField](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield) から継承</span><span class="sxs-lookup"><span data-stu-id="7fe55-130">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[BoundField](view-model-control-basecontrol-icontrol-icontrolmetadata.md#boundfield)</span></span>


### <a name="children"></a><span data-ttu-id="7fe55-131">子</span><span class="sxs-lookup"><span data-stu-id="7fe55-131">Children</span></span>

<span data-ttu-id="7fe55-132">子: [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md) \[ \] (オプション)</span><span class="sxs-lookup"><span data-stu-id="7fe55-132">Children: [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md) \[ \] (optional)</span></span> 

<span data-ttu-id="7fe55-133">各子コントロールの管理メタデータのリスト。</span><span class="sxs-lookup"><span data-stu-id="7fe55-133">List of control metadata for each child control.</span></span>


### <a name="description"></a><span data-ttu-id="7fe55-134">説明</span><span class="sxs-lookup"><span data-stu-id="7fe55-134">Description</span></span>

<span data-ttu-id="7fe55-135">説明:文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="7fe55-135">Description: string (optional)</span></span> 

<span data-ttu-id="7fe55-136">コントロールの説明。</span><span class="sxs-lookup"><span data-stu-id="7fe55-136">Description of the control.</span></span>

> <span data-ttu-id="7fe55-137">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Description](view-model-control-basecontrol-icontrol-icontrolmetadata.md#description) から継承</span><span class="sxs-lookup"><span data-stu-id="7fe55-137">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Description](view-model-control-basecontrol-icontrol-icontrolmetadata.md#description)</span></span>


### <a name="editable"></a><span data-ttu-id="7fe55-138">編集可能</span><span class="sxs-lookup"><span data-stu-id="7fe55-138">Editable</span></span>

<span data-ttu-id="7fe55-139">編集可能: プール値 (省略可)</span><span class="sxs-lookup"><span data-stu-id="7fe55-139">Editable: boolean (optional)</span></span> 

<span data-ttu-id="7fe55-140">コントロールが編集可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7fe55-140">Boolean indicating if the control is editable.</span></span>
<span data-ttu-id="7fe55-141">コントロールまたはその親が編集可能でない場合は、False です。</span><span class="sxs-lookup"><span data-stu-id="7fe55-141">False when either the control or it's parent is not editable.</span></span>
<span data-ttu-id="7fe55-142">コントロールとその親の両方が編集可能な場合、true です。</span><span class="sxs-lookup"><span data-stu-id="7fe55-142">True when both the control and it's parent are editable.</span></span>
<span data-ttu-id="7fe55-143">コントロールまたはその親が編集可能で、もう一方が未定義の場合は true です。</span><span class="sxs-lookup"><span data-stu-id="7fe55-143">True when either the control or it's parent is editable and the other is undefined.</span></span>
<span data-ttu-id="7fe55-144">コントロールの編集機能と親の編集機能の両方が未定義の場合は未定義です。</span><span class="sxs-lookup"><span data-stu-id="7fe55-144">Undefined if both the control's edit-ability and it's parent's edit-ability is undefined.</span></span>

> <span data-ttu-id="7fe55-145">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Editable](view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable) から継承</span><span class="sxs-lookup"><span data-stu-id="7fe55-145">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Editable](view-model-control-basecontrol-icontrol-icontrolmetadata.md#editable)</span></span>


### <a name="exttype"></a><span data-ttu-id="7fe55-146">ExtType</span><span class="sxs-lookup"><span data-stu-id="7fe55-146">ExtType</span></span>

<span data-ttu-id="7fe55-147">ExtType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可)</span><span class="sxs-lookup"><span data-stu-id="7fe55-147">ExtType: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (optional)</span></span> 

<span data-ttu-id="7fe55-148">拡張されたコントロール タイプです。</span><span class="sxs-lookup"><span data-stu-id="7fe55-148">The extended control type.</span></span> <span data-ttu-id="7fe55-149">E.g.</span><span class="sxs-lookup"><span data-stu-id="7fe55-149">E.g.</span></span> <span data-ttu-id="7fe55-150">コントロール タイプ Input に、拡張タイプ Barcode が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="7fe55-150">a control of type Input might have an extended type of Barcode.</span></span>

> <span data-ttu-id="7fe55-151">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[ExtType](view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype) から継承</span><span class="sxs-lookup"><span data-stu-id="7fe55-151">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[ExtType](view-model-control-basecontrol-icontrol-icontrolmetadata.md#exttype)</span></span>


### <a name="helptext"></a><span data-ttu-id="7fe55-152">HelpText</span><span class="sxs-lookup"><span data-stu-id="7fe55-152">HelpText</span></span>

<span data-ttu-id="7fe55-153">HelpText: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="7fe55-153">HelpText: string (optional)</span></span> 

<span data-ttu-id="7fe55-154">コマンドのキーボード ショートカットです。</span><span class="sxs-lookup"><span data-stu-id="7fe55-154">The keyboard shortcut for a command.</span></span> <span data-ttu-id="7fe55-155">E.g.</span><span class="sxs-lookup"><span data-stu-id="7fe55-155">E.g.</span></span> <span data-ttu-id="7fe55-156">「(Shift + F5)」</span><span class="sxs-lookup"><span data-stu-id="7fe55-156">"(Shift+F5)"</span></span>

> <span data-ttu-id="7fe55-157">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[HelpText](view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext) から継承</span><span class="sxs-lookup"><span data-stu-id="7fe55-157">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[HelpText](view-model-control-basecontrol-icontrol-icontrolmetadata.md#helptext)</span></span>


### <a name="hidden"></a><span data-ttu-id="7fe55-158">非表示</span><span class="sxs-lookup"><span data-stu-id="7fe55-158">Hidden</span></span>

<span data-ttu-id="7fe55-159">非表示: ブール値 (オプション)</span><span class="sxs-lookup"><span data-stu-id="7fe55-159">Hidden: boolean (optional)</span></span> 

<span data-ttu-id="7fe55-160">コントロールを非表示にするかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7fe55-160">Boolean indicating if the control is hidden or not.</span></span>

> <span data-ttu-id="7fe55-161">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Hidden](view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden) から継承</span><span class="sxs-lookup"><span data-stu-id="7fe55-161">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Hidden](view-model-control-basecontrol-icontrol-icontrolmetadata.md#hidden)</span></span>


### <a name="id"></a><span data-ttu-id="7fe55-162">ID</span><span class="sxs-lookup"><span data-stu-id="7fe55-162">Id</span></span>

<span data-ttu-id="7fe55-163">Id: string (オプション)</span><span class="sxs-lookup"><span data-stu-id="7fe55-163">Id: string (optional)</span></span> 

<span data-ttu-id="7fe55-164">コントロールの ID 文字列です。</span><span class="sxs-lookup"><span data-stu-id="7fe55-164">Identification string for a control.</span></span>

> <span data-ttu-id="7fe55-165">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](view-model-control-basecontrol-icontrol-icontrolmetadata.md#id) から継承</span><span class="sxs-lookup"><span data-stu-id="7fe55-165">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Id](view-model-control-basecontrol-icontrol-icontrolmetadata.md#id)</span></span>


### <a name="label"></a><span data-ttu-id="7fe55-166">ラベル</span><span class="sxs-lookup"><span data-stu-id="7fe55-166">Label</span></span>

<span data-ttu-id="7fe55-167">ラベル: 文字列 (省略可)</span><span class="sxs-lookup"><span data-stu-id="7fe55-167">Label: string (optional)</span></span> 

<span data-ttu-id="7fe55-168">コントロールのラベル。</span><span class="sxs-lookup"><span data-stu-id="7fe55-168">Label for a control.</span></span> <span data-ttu-id="7fe55-169">E.g.</span><span class="sxs-lookup"><span data-stu-id="7fe55-169">E.g.</span></span> <span data-ttu-id="7fe55-170">個人の名を表すコントロールに「氏名」というラベルが付いている場合があります。</span><span class="sxs-lookup"><span data-stu-id="7fe55-170">a control representing a person's first name might have a label "First Name".</span></span>

> <span data-ttu-id="7fe55-171">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](view-model-control-basecontrol-icontrol-icontrolmetadata.md#label) から継承</span><span class="sxs-lookup"><span data-stu-id="7fe55-171">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Label](view-model-control-basecontrol-icontrol-icontrolmetadata.md#label)</span></span>


### <a name="name"></a><span data-ttu-id="7fe55-172">氏名</span><span class="sxs-lookup"><span data-stu-id="7fe55-172">Name</span></span>

<span data-ttu-id="7fe55-173">Name: 文字列 (省略可)</span><span class="sxs-lookup"><span data-stu-id="7fe55-173">Name: string (optional)</span></span> 

<span data-ttu-id="7fe55-174">コントロールの名前です。</span><span class="sxs-lookup"><span data-stu-id="7fe55-174">Name of a control.</span></span>

> <span data-ttu-id="7fe55-175">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](view-model-control-basecontrol-icontrol-icontrolmetadata.md#name) から継承</span><span class="sxs-lookup"><span data-stu-id="7fe55-175">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Name](view-model-control-basecontrol-icontrol-icontrolmetadata.md#name)</span></span>


### <a name="order"></a><span data-ttu-id="7fe55-176">注文</span><span class="sxs-lookup"><span data-stu-id="7fe55-176">Order</span></span>

<span data-ttu-id="7fe55-177">注文: 番号 (オプション)</span><span class="sxs-lookup"><span data-stu-id="7fe55-177">Order: number (optional)</span></span> 

<span data-ttu-id="7fe55-178">コントロールがページに表示される順序を示す番号。</span><span class="sxs-lookup"><span data-stu-id="7fe55-178">Number indicating the order in which a control will appear on a page.</span></span>

> <span data-ttu-id="7fe55-179">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](view-model-control-basecontrol-icontrol-icontrolmetadata.md#order) から継承</span><span class="sxs-lookup"><span data-stu-id="7fe55-179">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Order](view-model-control-basecontrol-icontrol-icontrolmetadata.md#order)</span></span>


### <a name="type"></a><span data-ttu-id="7fe55-180">種類</span><span class="sxs-lookup"><span data-stu-id="7fe55-180">Type</span></span>

<span data-ttu-id="7fe55-181">Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (省略可)</span><span class="sxs-lookup"><span data-stu-id="7fe55-181">Type: [ControlType](../modules/view-model-control-basecontrol-icontrol.md#controltype) (optional)</span></span> 

<span data-ttu-id="7fe55-182">コントロール タイプを示す文字列。</span><span class="sxs-lookup"><span data-stu-id="7fe55-182">String indicating the control type.</span></span>

> <span data-ttu-id="7fe55-183">[ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type) から継承</span><span class="sxs-lookup"><span data-stu-id="7fe55-183">Inherited from [ControlMetadata](view-model-control-basecontrol-icontrol-icontrolmetadata.md).[Type](view-model-control-basecontrol-icontrol-icontrolmetadata.md#type)</span></span>


