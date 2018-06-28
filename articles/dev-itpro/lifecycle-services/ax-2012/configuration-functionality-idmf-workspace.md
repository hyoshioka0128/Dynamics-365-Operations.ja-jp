---
title: "構成"
description: "このトピックでは、Microsoft Dynamics AX のインテリジェント データ管理フレームワーク (IDMF) 機能について説明します。"
author: kfend
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 17661
ms.assetid: b8e04a6f-a206-4faa-84e5-6cd45c9b5257
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d569968b4796330bf0eceac62591a404af6b6f80
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="configuration-in-the-intelligent-data-management-framework-ax-2012"></a><span data-ttu-id="d8fc8-103">Intelligent Data Management Framework (AX 2012) でのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d8fc8-103">Configuration in the Intelligent Data Management Framework (AX 2012)</span></span>

[!include [banner](../../includes/banner.md)]

<a name="purge-and-archive-functionality"></a><span data-ttu-id="d8fc8-104">機能の削除とアーカイブ</span><span class="sxs-lookup"><span data-stu-id="d8fc8-104">Purge and archive functionality</span></span>
-------------------------------

<span data-ttu-id="d8fc8-105">Microsoft Dynamics AX アプリケーションは、トランザクションのリアルタイム更新を提供します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-105">The Microsoft Dynamics AX application provides real-time updates for a transaction.</span></span> <span data-ttu-id="d8fc8-106">たとえば、ユーザーが注文を入力、変更、または削除する場合、Microsoft Dynamics AX は、メイン テーブルと関連するテーブルのいくつかを更新します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-106">For example, when users enter, modify, or delete orders, Microsoft Dynamics AX updates a main table and some of its related tables.</span></span> <span data-ttu-id="d8fc8-107">時間の経過と共に、データベース内のデータの量が大きくなります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-107">Over time, the volume of data in the database grows.</span></span> <span data-ttu-id="d8fc8-108">IDMF を使用すると、データベースを分析し、最適なデータベース サイズを維持できます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-108">IDMF lets you analyze the database and maintain an optimal database size.</span></span> <span data-ttu-id="d8fc8-109">データベース・サイズを維持するために、IDMF ではパージ機能とアーカイブ機能が提供されています。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-109">To maintain the database size, IDMF provides the purge and archive functions.</span></span> <span data-ttu-id="d8fc8-110">削除機能で、実稼働データベースの関連するエンティティまたはテーブルのセットから、データを削除します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-110">The purge function removes or deletes data from a set of related entities, or tables, from the production database.</span></span> <span data-ttu-id="d8fc8-111">アーカイブ機能により、実稼働データベースにある一連の関連テーブルから、アーカイブ データベースと呼ばれるスタンバイ データベースへデータが移動されます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-111">The archive function moves data from a set of related tables from the production database to a standby database called the archive database.</span></span> <span data-ttu-id="d8fc8-112">ユーザーは、アーカイブ データベースをレポートに使用できますが、その更新を許可しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-112">Users can use the archive database for reporting, but we recommend that they not be allowed to update it.</span></span> <span data-ttu-id="d8fc8-113">IDMF とこの文書では、オフラインという用語をアーカイブという用語と交互に使用し、パージまたは削除操作と交互にリサイクルします。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-113">IDMF and this document use the term offlining interchangeably with the term archiving, and recycling interchangeably with purge or delete operation.</span></span> <span data-ttu-id="d8fc8-114">削除とアーカイブ操作は、Microsoft Dynamics AX のメタデータに基づいて慎重に判別された関連テーブルの階層関係ツリーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-114">Both the purge and archive operations depend on a carefully determined hierarchical relationship tree of related tables based on the Microsoft Dynamics AX metadata.</span></span> <span data-ttu-id="d8fc8-115">たとえば、ユーザーが販売注文を作成、更新、または削除する際に、**SalesTable** テーブルおよび **SalesTable** に関連付けられているその他のテーブルが更新されます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-115">For example, when a user creates, updates, or deletes a sales order, the **SalesTable** table and other tables that are related to **SalesTable** are updated.</span></span> <span data-ttu-id="d8fc8-116">SalesTable などのテーブルのデータをアーカイブまたは削除するときは、そのメイン テーブルに関連付けられているすべてのテーブルのデータをアーカイブまたは削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-116">When you archive or purge data from a main table, such as SalesTable, you must archive or purge data from all the tables that are related to that main table.</span></span> <span data-ttu-id="d8fc8-117">アーカイブおよび削除の操作は常に、関連するテーブルのセットで実行されます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-117">The archive and purge operations always work on a set of related tables.</span></span> <span data-ttu-id="d8fc8-118">この関連テーブルのセットは、リレーションシップを形成します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-118">This set of related tables forms a hierarchical relationship.</span></span> <span data-ttu-id="d8fc8-119">各階層関係は、階層ツリーのレベル 0 であるルート レベルで、ドライバー テーブルと呼ばれるメイン テーブルから始まります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-119">Each hierarchical relationship starts with the main table, called a driver table, at the root level, level 0, of the hierarchical tree.</span></span> <span data-ttu-id="d8fc8-120">ドライバー テーブルに関連付けられたすべての子テーブルは次のレベル、レベル 1 にあります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-120">All the child tables that are related to the driver table are at the next level, level 1.</span></span> <span data-ttu-id="d8fc8-121">レベル 1 テーブル内にあるすべての子テーブルは次のレベル、レベル 2 にあります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-121">All the child tables of tables in level 1 are at the next level, level 2.</span></span> <span data-ttu-id="d8fc8-122">親子関係の入れ子になった階層は、最下位レベルのテーブルの子テーブル表がなくなるまで続きます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-122">The nested hierarchy of parent-child relationships continues until there are no more child tables for the lowest level of tables.</span></span> <span data-ttu-id="d8fc8-123">階層関係の理解に役立つように、IDMF にはサンプルの階層関係を示すテンプレートがいくつか含まれています。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-123">To help you understand the hierarchical relationships, IDMF includes some templates that show sample hierarchical relationships.</span></span> <span data-ttu-id="d8fc8-124">アーカイブ機能のテンプレートは、アーカイブ テンプレートと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-124">Templates for the archive function are called archive templates.</span></span> <span data-ttu-id="d8fc8-125">削除機能のテンプレートは、削除テンプレートと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-125">Templates for the purge function are called purge templates.</span></span> <span data-ttu-id="d8fc8-126">各テンプレートは、カスタマイズされていない標準インストールに基づくサンプル階層を提供します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-126">Each template provides a sample hierarchy based on a standard installation without any customizations.</span></span> <span data-ttu-id="d8fc8-127">これらのテンプレートを直接使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-127">You cannot use these templates directly.</span></span> <span data-ttu-id="d8fc8-128">アーカイブまたは削除機能に使用する前に、これらのテンプレートを開き、環境内の適合性を確認して保存してください。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-128">You must open these templates, review them to verify applicability in your environment, and then save them before you can use them for the archive or purge function.</span></span> <span data-ttu-id="d8fc8-129">テンプレートを開いたとき、リレーションシップの階層に、Microsoft Dynamics AX の実装からの関連するすべてのテーブルが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-129">When you open a template, verify that the relationship hierarchy contains all the relevant tables from your implementation of Microsoft Dynamics AX.</span></span> <span data-ttu-id="d8fc8-130">テンプレートの階層ツリーは、いくつかの理由で実装と一致しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-130">The hierarchical tree in the template may not match your implementation for several reasons.</span></span> <span data-ttu-id="d8fc8-131">以下の一覧は、Microsoft Dynamics AX の実装におけるテンプレートとリレーションシップとの違いの理由の一部について示しています。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-131">The following list provides some of the reasons for a difference between a template and the relationships in your implementation of Microsoft Dynamics AX:</span></span>

-   <span data-ttu-id="d8fc8-132">ご使用の実装には、実装のカスタマイズ、コンフィギュレーション、およびライセンスに基づいて、テンプレート内の特定のテーブルが含まれない場合があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-132">Your implementation may not have certain tables that are in the template, depending on the customization, configuration, and licensing of your implementation.</span></span>
-   <span data-ttu-id="d8fc8-133">テンプレート内のテーブルの一部のフィールドは、実装では使用できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-133">Certain fields in the tables in the template might not be available in your implementation.</span></span>
-   <span data-ttu-id="d8fc8-134">テンプレートに含まれていないカスタム テーブルを作成している場合があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-134">You may have created custom tables that are not contained in the templates.</span></span>

<span data-ttu-id="d8fc8-135">階層関係が実装で関連するすべてのテーブルを含んでいることが非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-135">It is very important that your hierarchical relationship include all relevant tables in your implementation.</span></span> <span data-ttu-id="d8fc8-136">正しくない階層に基づく削除またはアーカイブ操作は、データの破損を引き起こします。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-136">A purge or archive operation that is based on an incorrect hierarchy causes data corruption.</span></span> <span data-ttu-id="d8fc8-137">したがって、実装に完全で正確なリレーションシップ ツリーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-137">Therefore, you must create a relationship tree that is complete and accurate for your implementation.</span></span> <span data-ttu-id="d8fc8-138">各実装の一意性のため、アーカイブまたは削除機能でテンプレートを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-138">Because of the uniqueness of each implementation, you cannot use a template in the archive or purge function.</span></span> <span data-ttu-id="d8fc8-139">代わりに、実装に関連するすべての関係を含む削除オブジェクトやアーカイブ オブジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-139">Instead, you must create a Purge Object or an Archive Object that encompasses all relevant relationships for your implementation.</span></span> <span data-ttu-id="d8fc8-140">削除オブジェクトまたはアーカイブ オブジェクトを作成するには、2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-140">There are two ways you can create a Purge Object or an Archive Object:</span></span>

-   <span data-ttu-id="d8fc8-141">テンプレートで作業します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-141">Work with a template.</span></span> <span data-ttu-id="d8fc8-142">IDMF に含まれているテンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-142">Open a template that is included with IDMF.</span></span> <span data-ttu-id="d8fc8-143">テンプレートを確認し、実装に合うようにテーブルおよびルールを追加または削除します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-143">Review the template, and then add or remove tables and rules to match your implementation.</span></span> <span data-ttu-id="d8fc8-144">リレーションシップ ツリーが実装のために完成していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-144">Verify that the relationship tree is complete for your implementation.</span></span> <span data-ttu-id="d8fc8-145">テンプレートを保存します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-145">Save the template.</span></span> <span data-ttu-id="d8fc8-146">アーカイブ テンプレートはアーカイブ オブジェクトとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-146">An archive template is saved as an Archive Object.</span></span> <span data-ttu-id="d8fc8-147">削除テンプレートは、削除オブジェクトとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-147">A purge template is saved as a Purge Object.</span></span>
-   <span data-ttu-id="d8fc8-148">IDMF に含まれているテンプレートを使用する代わりに、独自のオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-148">Create an object on your own instead of using the template that is included with IDMF.</span></span> <span data-ttu-id="d8fc8-149">ライセンス、コンフィギュレーション、およびカスタマイズによっては、実装の階層リレーションシップが IDMF に含まれるテンプレートと大きく異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-149">Depending on the licensing, configuration, and customization, the hierarchical relationship in your implementation may significantly differ from the templates that are included with IDMF.</span></span> <span data-ttu-id="d8fc8-150">この場合、リレーションシップ ツリーのルートを形成する親テーブルとなっているドライバー テーブルを選択できる検出プロセスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-150">In this case, you must use the discovery process, which lets you select a driver table that is the parent table that forms the root of the relationship tree.</span></span> <span data-ttu-id="d8fc8-151">選択したドライバー テーブルと Microsoft Dynamics AX のメタデータに基づいて、IDMF は階層リレーションシップ ツリーを生成します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-151">Based on the driver table that you select, and the Microsoft Dynamics AX metadata, IDMF generates the hierarchical relationship tree.</span></span> <span data-ttu-id="d8fc8-152">IDMF では、例外一覧を確認し、例外リストに含まれるテーブルを無視します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-152">IDMF checks an exception list and ignores tables that are contained in the exception list.</span></span>

<span data-ttu-id="d8fc8-153">テンプレートを開くまた保存する代わりに、検索プロセスを使用して削除オブジェクトまたはアーカイブ オブジェクトを作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-153">We recommend that you create a Purge Object or an Archive Object through the discovery process instead of opening and saving a template.</span></span> <span data-ttu-id="d8fc8-154">同様のテンプレートが存在する場合は、テンプレートとオブジェクトを比較して、テンプレートに含まれているテーブルがオブジェクトに存在しないかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-154">Compare your object with the template, if a similar template exists, to see whether your object is missing any tables that the template contains.</span></span> <span data-ttu-id="d8fc8-155">比較と検証に応じて、適切なオブジェクトにテーブルを追加するか、オブジェクトからテーブルを削除します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-155">Depending on the comparison and verification, add tables to or remove tables from your object, as appropriate.</span></span> <span data-ttu-id="d8fc8-156">各アーカイブ オブジェクトまたは削除オブジェクトには、アーカイブまたはデータの削除を管理する特定のルールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-156">Each Archive Object or Purge Object contains certain rules that govern the archiving or purging of data.</span></span> <span data-ttu-id="d8fc8-157">ルールを使用して、削除またはアーカイブする対象となるデータを選択するために使用する選択基準を指定できます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-157">Rules let you specify the selection criteria that are used to select the data that is qualified for purging or archiving.</span></span> <span data-ttu-id="d8fc8-158">自分のアーカイブガイドラインおよび削除ガイドラインと一致するように、これらのルールを追加、削除、または修正することができます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-158">You can add, remove, or modify these rules to match your archive and purge guidelines.</span></span> <span data-ttu-id="d8fc8-159">削除タスクまたはアーカイブ タスクで使用する前に、アーカイブ オブジェクトまたは削除オブジェクトを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-159">You must save an Archive Object or a Purge Object before you can use it in a purge or archive task.</span></span> <span data-ttu-id="d8fc8-160">DMF は、次の図に示すサンプルに類似した削除オブジェクトまたはアーカイブ オブジェクトのグラフィカル表示を提供します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-160">IDMF provides a graphical view of your Purge Object or Archive Object that resembles the sample that is shown in the following diagram.</span></span> <span data-ttu-id="d8fc8-161">アーカイブ オブジェクトおよび削除オブジェクトを簡単に理解して検証できるように、凡例を確認します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-161">Familiarize yourself with the legend, so that you can easily understand and validate your Archive Objects and Purge Objects.</span></span> 

![IDMF アーカイブ オブジェクト](./media/idmfarchiveobject.png) 

<span data-ttu-id="d8fc8-163">次のテーブルでは、オブジェクトまたはテンプレートのリレーションシップ ツリーに表示される凡例について説明します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-163">The following table explains the legend that is shown in a relationship tree of an object or a template.</span></span>

| <span data-ttu-id="d8fc8-164">テキスト</span><span class="sxs-lookup"><span data-stu-id="d8fc8-164">Text</span></span>                                                                  | <span data-ttu-id="d8fc8-165">説明</span><span class="sxs-lookup"><span data-stu-id="d8fc8-165">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8fc8-166">テーブルが削除されました</span><span class="sxs-lookup"><span data-stu-id="d8fc8-166">Table removed</span></span>                                                         | <span data-ttu-id="d8fc8-167">このテーブルは、操作しているオブジェクトから削除されています。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-167">This table has been removed from the object you are working with.</span></span> <span data-ttu-id="d8fc8-168">削除オブジェクトまたはアーカイブ オブジェクトは、このテーブルからデータを削除したりアーカイブしたりしません。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-168">The Purge Object or Archive Object does not purge or archive data from this table.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="d8fc8-169">テーブルが、生産データベースにありません。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-169">Table is missing from the production database</span></span>                         | <span data-ttu-id="d8fc8-170">このテーブルは、操作しているテンプレートまたはオブジェクトにはありますが、実稼働データベースにはありません。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-170">This table exists in the template or object you are working with, but is not found in your production database.</span></span> <span data-ttu-id="d8fc8-171">このオブジェクトを保存する前に、次の表をリレーションシップから削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-171">You must remove this table from the relationship before you can save this object.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d8fc8-172">無構成キーが無効になっているフィールド</span><span class="sxs-lookup"><span data-stu-id="d8fc8-172">Fields with disabled configuration keys</span></span>                               | <span data-ttu-id="d8fc8-173">Microsoft Dynamics AX では、各フィールドがセキュリティ キーおよびコンフィギュレーション キーによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-173">In Microsoft Dynamics AX, each field is governed by the security key and a configuration key.</span></span> <span data-ttu-id="d8fc8-174">使用するライセンス、セキュリティ キー、およびコンフィギュレーションに応じて、各フィールドは有効または無効のフィールドにすることができます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-174">Depending on the licensing, security keys, and configuration you use, each field can be an enabled or a disabled field.</span></span> <span data-ttu-id="d8fc8-175">この文書では、無効なフィールドは、コンフィギュレーション キーを介して無効にされるフィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-175">For the purpose of this document, a disabled field refers to a field that is disabled via the configuration key.</span></span> <span data-ttu-id="d8fc8-176">無効なフィールドを使用するルールを含むドライバー テーブル、または無効なフィールドを使用する任意のリレーションシップを持つ子テーブルは黄色の境界線で表示されます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-176">A driver table with any rules that use a disabled field, or a child table with any relationships that use a disabled field, appears with a yellow border.</span></span> <span data-ttu-id="d8fc8-177">オブジェクトを保存する前に、無効なフィールドのルールとリレーションシップを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-177">You must resolve the rules and relationships with disabled fields before you can save the object.</span></span> |
| <span data-ttu-id="d8fc8-178">選択されたテーブル</span><span class="sxs-lookup"><span data-stu-id="d8fc8-178">Selected table</span></span>                                                        | <span data-ttu-id="d8fc8-179">このテーブルを選択しています。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-179">You have selected this table.</span></span> <span data-ttu-id="d8fc8-180">複数のテーブルを選択してから、選択したテーブルのすべての発生を削除、または選択したテーブルをデータ アプリケーション フィーチャーに追加などのアクションを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-180">You can select multiple tables, and then perform actions such as remove all occurrences of the selected tables or add selected tables to the data replication feature.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="d8fc8-181">テーブル グループ プロパティは、ワークシート ヘッダーです</span><span class="sxs-lookup"><span data-stu-id="d8fc8-181">Table group property is worksheet header</span></span>                              | <span data-ttu-id="d8fc8-182">このテーブルには、**WorksheetHeader** の **TableGroup** 値が格納されています。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-182">This table has a **TableGroup** value of **WorksheetHeader**.</span></span> <span data-ttu-id="d8fc8-183">このようなテーブルを右クリックして、関連する子テーブルを再検出することができます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-183">You can right-click such tables and rediscover related child tables.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="d8fc8-184">関連するアーカイブ オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d8fc8-184">Related Archive Object</span></span>                                                | <span data-ttu-id="d8fc8-185">これは、関連するアーカイブ オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-185">This is a Related Archive Object.</span></span> <span data-ttu-id="d8fc8-186">複雑さを避けるため、多数の入れ子になったリレーションシップを持つ子テーブルを追加する代わりに、関連するアーカイブ オブジェクトを自分のアーカイブ オブジェクトに追加できます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-186">To avoid complexity, you can add a Related Archive Object to your Archive Object, instead of adding a child table with many levels of nested relationships.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d8fc8-187">関連するアーカイブ オブジェクト: テーブルが生産データベースにありません</span><span class="sxs-lookup"><span data-stu-id="d8fc8-187">Related Archive Object: Table is missing from the production database</span></span> | <span data-ttu-id="d8fc8-188">この関連アーカイブ オブジェクトは、生産データベースに存在しません。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-188">This Related Archive Object does not exist in the production database.</span></span> <span data-ttu-id="d8fc8-189">現在のオブジェクトを保存する前に、関連するアーカイブ オブジェクトからこのテーブルを削除して保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-189">You must remove this table from the Related Archive Object and save it before you can save your current object.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="d8fc8-190">関連するアーカイブ オブジェクト: 無効になったコンフィギュレーション キーを持つフィールド</span><span class="sxs-lookup"><span data-stu-id="d8fc8-190">Related Archive Object: Fields with disabled configuration keys</span></span>       | <span data-ttu-id="d8fc8-191">この関連するアーカイブ オブジェクトには、構成キーが無効になっている関係またはルールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-191">This Related Archive Object contains relationships or rules with disabled configuration keys.</span></span> <span data-ttu-id="d8fc8-192">このオブジェクトで使用できるようにするには、構成キーを有効にするか、または無効なフィールドに基づくリレーションシップとルールを削除し、それから関連するアーカイブ オブジェクトを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-192">You must enable the configuration keys, or remove the relationships and rules based on disabled fields, and then save the Related Archive Object before you can use it in this object.</span></span>                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="d8fc8-193">親 Archive Object のドライバー デーブル</span><span class="sxs-lookup"><span data-stu-id="d8fc8-193">Driver table of the parent Archive Object</span></span>                             | <span data-ttu-id="d8fc8-194">これは、この関連アーカイブ オブジェクトの親オブジェクトであるアーカイブ オブジェクトのドライバー テーブルです。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-194">This is the driver table of the Archive Object that is the parent object of this Related Archive Object.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="introduction-to-the-discovery-process"></a><span data-ttu-id="d8fc8-195">検出プロセスの概要</span><span class="sxs-lookup"><span data-stu-id="d8fc8-195">Introduction to the discovery process</span></span>
<span data-ttu-id="d8fc8-196">検出プロセスは、削除オブジェクトまたはアーカイブ オブジェクの階層リレーションシップ ツリーを作成します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-196">The discovery process creates a hierarchical relationship tree for a Purge Object or an Archive Object.</span></span> <span data-ttu-id="d8fc8-197">新しい削除オブジェクトまたはアーカイブ オブジェクトを作成するときは、ドライバー テーブルと呼ばれる親テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-197">When you create a new Purge Object or Archive Object, you select a parent table, called the driver table.</span></span> <span data-ttu-id="d8fc8-198">IDMF では、発見と呼ばれるプロセスを使用して、選択したドライバー テーブルに基づく階層関係ツリーを作成します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-198">IDMF uses a process called discovery to create a hierarchical relationship tree based on the driver table you select.</span></span> <span data-ttu-id="d8fc8-199">次の手順では、WMSOrder テーブルをドライバー テーブルとして選択したと仮定して、検出プロセスの詳細を説明します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-199">The following steps provide a high-level walkthrough of the discovery process, assuming that you selected the WMSOrder table as the driver table:</span></span>
1.  <span data-ttu-id="d8fc8-200">親子階層のルート親であるドライバー テーブルとしてテーブルを選択すると、検出プロセスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-200">The discovery process starts when you select a table as the driver table that is the root parent in a parent-child hierarchy.</span></span> <span data-ttu-id="d8fc8-201">ただし、IDMF は、例外リストの一部であるドライバー テーブル リストにはテーブルを表示しません。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-201">However, IDMF does not display tables in the driver table list that are part of an exception list.</span></span> <span data-ttu-id="d8fc8-202">**WMSOrder** テーブルは、例外パラメーター リスト内にないためリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-202">The **WMSOrder** table appears in the list, because it is not in the exception parameters list.</span></span>
2.  <span data-ttu-id="d8fc8-203">Microsoft Dynamics AX の **xRefTableRelation** テーブルには、2 つのテーブル間の関係と、関係により使用されるフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-203">The **xRefTableRelation** table in Microsoft Dynamics AX contains relationships between two tables, and the fields that are used by the relationship.</span></span> <span data-ttu-id="d8fc8-204">IDMF は、**xRefTableRelation** テーブルを照会して、親の子テーブル **WMSOrder** のテーブル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-204">IDMF queries the **xRefTableRelation** table to retrieve the names of the tables that are child tables of the parent, **WMSOrder**.</span></span> <span data-ttu-id="d8fc8-205">**xRefTableRelation** フィールドの説明は、このトピックの範囲を超えています。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-205">Explanation of the **xRefTableRelation** field is beyond the scope of this topic.</span></span> <span data-ttu-id="d8fc8-206">詳細については、[xRefTableRelation テーブル](https://msdn.microsoft.com/en-us/library/aa860828.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-206">For more information, see [xRefTableRelation table](https://msdn.microsoft.com/en-us/library/aa860828.aspx).</span></span>
3.  <span data-ttu-id="d8fc8-207">子テーブルがなくなるまで、すべてのテーブルについて前の手順を続行します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-207">Continue the previous step for every table, until there are no child tables left.</span></span> <span data-ttu-id="d8fc8-208">場合によっては、子テーブルがこれらの条件のリレーションシップ ツリーから除外されます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-208">In certain cases, a child table is excluded from the relationship tree in these conditions:</span></span>
    -   <span data-ttu-id="d8fc8-209">子テーブルには、**メイン**、**パラメーター**、または**グループ**の **TableGroup** 値があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-209">The child table has a **TableGroup** value of **Main**, **Parameter**, or **Group**.</span></span>
    -   <span data-ttu-id="d8fc8-210">子テーブルは例外パラメーター リストにあり、**削除検出**フィールドが選択されています。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-210">The child table is in the exception parameters list, with the **Purge discovery** field selected.</span></span> <span data-ttu-id="d8fc8-211">この場合、子テーブルは、削除オブジェクトのリレーションシップ ツリーから除外されます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-211">In this case, the child table is excluded from the relationship tree of the Purge Object.</span></span>
    -   <span data-ttu-id="d8fc8-212">子テーブルは例外パラメーター リストにあり、**アーカイブ検出**フィールドが選択されています。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-212">The child table is in the exception parameters list, with the **Archive discovery** field selected.</span></span> <span data-ttu-id="d8fc8-213">この場合、子テーブルは、アーカイブ オブジェクトのリレーションシップ ツリーから除外されます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-213">In this case, the child table is excluded from the relationship tree of the Archive Object.</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d8fc8-214"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="d8fc8-214"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d8fc8-215"><strong><span class="ui">Table Group</span></strong> 値が <strong><span class="ui">WorksheetHeader</span></strong> のテーブルは、ドライバー テーブルに最適な候補であり、子テーブルとして検出されると関係ツリーに黒色の境界線で表示されます。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-215">Tables with a <strong><span class="ui">Table Group</span></strong> value of <strong><span class="ui">WorksheetHeader</span></strong> are ideal candidates for driver tables, and appear with a black border in the relationship tree when they are discovered as child tables.</span></span> <span data-ttu-id="d8fc8-216">検出プロセスでは、これらのテーブルが子テーブルとして表示されますが、子テーブルはツリーに表示されません。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-216">The discovery process shows these tables as child tables, but does not show their child tables in the tree.</span></span> <span data-ttu-id="d8fc8-217">削除およびアーカイブ戦略にこれらのテーブルを組み込むには、次の一覧のどのオプションを使用するのが最適かを判断します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-217">Determine which option in the following list is the best way to incorporate these tables in your purge and archive strategy:</span></span>
<ul>
<li><span data-ttu-id="d8fc8-218">リレーションシップ ツリーでこれらのテーブルを保持し、その子テーブルを追加しません。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-218">Keep these tables in the relationship tree, but do not add their child tables.</span></span></li>
<li><span data-ttu-id="d8fc8-219">リレーションシップ ツリーでこれらのテーブルを保持し、その子テーブルを追加します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-219">Keep these tables in the relationship tree, and add their child tables.</span></span> <span data-ttu-id="d8fc8-220">テーブルを右クリックし、<strong><span class="ui">検出</span></strong> を選択して、テーブルの親子階層を形成する子テーブルを検出または追加します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-220">Right-click a table, and then select <strong><span class="ui">Discover</span></strong> to discover, or add, the child tables that form the parent-child hierarchy for the table.</span></span></li>
<li><span data-ttu-id="d8fc8-221">アーカイブ オブジェクトの場合、リレーションシップ ツリーからこれらのテーブルを削除し、関連するアーカイブ オブジェクトとして追加するか、独立したアーカイブ オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-221">In the case of an Archive Object, remove these tables from the relationship tree, and either add them as Related Archive Objects or create independent Archive Objects.</span></span></li>
<li><span data-ttu-id="d8fc8-222">削除オブジェクトの場合、これらのテーブルを削除し、ドライバー テーブルとしてこれらのテーブルを使用して新しい削除オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-222">In the case of a Purge Object, remove these tables, and create new Purge Objects by using these tables as the driver tables.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

| <span data-ttu-id="d8fc8-223">**注意**</span><span class="sxs-lookup"><span data-stu-id="d8fc8-223">**Caution**</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8fc8-224">例外パラメーターの一覧やアーカイブ オブジェクト、削除オブジェクトに対して操作を開始する前に、Microsoft Dynamics AX のメタデータとアプリケーションについて理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-224">You must understand the Microsoft Dynamics AX metadata and application before you start working with the exception parameters list, Archive Objects, or Purge Objects.</span></span> <span data-ttu-id="d8fc8-225">データベースとアプリケーションとの整合性を維持するには、削除オブジェクトまたはアーカイブ オブジェクトの機能を検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8fc8-225">You must functionally validate the Purge Object or Archive Object to maintain database and application integrity.</span></span> |





