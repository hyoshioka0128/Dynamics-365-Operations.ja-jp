---
title: Finance and Operations から Field Service への倉庫の同期
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に倉庫を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ae99624076eecda2969961d0361d1adf42c6c5f3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835673"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Finance and Operations から Field Service への倉庫の同期

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に倉庫を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク
次のテンプレートと基本的なタスクは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に倉庫の同期を実行するために使用されます。

**データ統合でのテンプレート**
- 倉庫 (Finance and Operations から Field Service)

**データ統合プロジェクトのタスク**
- 倉庫

## <a name="entity-set"></a>エンティティ セット
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | 倉庫                             |

## <a name="entity-flow"></a>エンティティのフロー
Finance and Operations で作成および管理されている倉庫は、Common Data Service (CDS) データの統合プロジェクトを通して Field Service に同期することができます。 Field Service に同期する倉庫は、プロジェクトの高度なクエリおよびフィルター処理で制御することができます。 Finance and Operations から同期する倉庫は Field Service で作成され、**外部で管理**フィールドを**はい**に設定することにより、レコードは読み取り専用になります。

## <a name="field-service-crm-solution"></a>Field Service CRM ソリューション
Field Service および Finance and Operations の統合をサポートするために、Field Service CRM からの追加機能が必要です。 ソリューションとして、**外部で管理**フィールドが、**倉庫 (msdyn_warehouses)** エンティティに追加されました。 このフィールドは、倉庫が Finance and Operations から処理されているのか、または Field Service にのみ存在するのかを識別するのに役立ちます。 このフィールドの設定は以下のとおりです。
- **はい** – 倉庫は Finance and Operations に由来し、Sales では編集できません。
- **いいえ** – 倉庫は Field Service で直接入力されており、ここで管理されます。

**外部で管理**フィールドは、在庫レベル、調整、移動およびワーク オーダーの使用状況の同期を制御します。 **外部で管理**が**はい**に設定された倉庫のみ、その他のシステムの同じ倉庫に直接同期するのに使用されます。 

> [!NOTE]
> Field Service で複数の倉庫を作成し (**外部で管理** = いいえ)、Finance and Operations で高度なクエリおよびフィルター処理を使用して 1 つの倉庫にマッピングすることができます。 これは、Field service に詳細な在庫レベルを習得させ、Finance and Operations に更新を送信するだけの場合に使用されます。 この場合、Field service は、Finance and Operations からの在庫レベルの更新は受信しません。 追加情報については、「[Field Service から Finance and Operations への在庫調整の同期](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments)」および「[Field Service でのワーク オーダーを Finance and Operations のプロジェクトにリンクされている販売注文に同期](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)」を参照してください。

## <a name="prerequisites-and-mapping-setup"></a>前提条件およびマッピングの設定
### <a name="data-integration-project"></a>データ統合プロジェクト
倉庫を同期する前に、プロジェクト上で高度なクエリおよびフィルタリング処理を更新し、Finance and Operations から Field Service へ移動させる倉庫のみが含まれていることを確認してください。 Field Service の倉庫をワーク オーダー、調整、および移動に適用する必要があることに注意してください。  

**統合キー**が **msdyn_warehouses** に存在することを確認するには:
1. データ統合に移動します。
2. **接続設定**タブを選択します。
3. ワーク オーダー同期に使用される接続設定を選択します。
4. **統合キー** タブを選択します。
5. Msdyn_warehouses を検索し、キーの **msdyn_name (名前)** が追加されていることを確認します。 表示されていない場合は、**キーの追加**をクリックして追加してから、ページの上部にある**保存**をクリックします。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ統合のテンプレート マッピングを示します。

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a>倉庫 (Finance and Operations から Field Service): 倉庫

[![データ統合のテンプレートのマッピング](./media/Warehouse1.png)](./media/Warehouse1.png)
