---
title: 原価計算レベル
description: このトピックでは、原価計算レベルを指定した部品表 (BOM) のレベルについて説明します。 このBOMレベルでは、計算から生産およびバッチ注文は計算から除外されます。
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 52b77e794ee38add556ac01d62c973b38c48a548
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431874"
---
# <a name="cost-calculation-level"></a>原価計算レベル

**原価計算レベル** が指定された部品表 (BOM) レベルでは、計算から製造注文とバッチ注文が除外されます。 このシステムは、原価計算のバージョンで原価計算を実行する際に、このレベルを使用します。 再計算や在庫原価計算などのプロセスでは、システムは代わりに **原価計算レベル** の BOM レベルを使用します。

以下の簡単なシナリオでは、**原価計算レベル** の  BOM レベルと **原価レベル** の BOM レベルの違いを示しています。

ここでは、A、B、C の 3 つの製品が使用されます。製品 C は製品 B のコンポーネントで、製品 B は製品 A のコンポーネントです。

- **原価レベル** では、次の BOM レベルが割り当てられます :

    - **製品 A :** 0
    - **製品 B :** 1
    - **製品 C :** 2

- **原価計算レベル** では、次の BOM レベルが割り当てられます :

    - **製品 A :** 0
    - **製品 B :** 1
    - **製品 C :** 2

製品 C の製造オーダーが作成され、製品 A が製造オーダー BOM に追加されます。 注文の見積後、BOM レベルは次のように更新されます :

- **原価レベル** では、次の BOM レベルが割り当てられます :

    - **製品 B :** 1
    - **製品 C :** 2
    - **製品 A :** 3

- **原価計算レベル** では、次の BOM レベルが割り当てられます :

    - **製品 A :** 0
    - **製品 B :** 1
    - **製品 C :** 2

この動作により、製造オーダー BOM に対する変更が後続の原価計算に影響を与えることがなくなります。