---
title: コード別消費税支払レポートの印刷
description: このトピックでは、会計または税コードの通貨でコード別消費税支払レポートを印刷するために必要な設定とアクションについて説明します。
author: anasyash
manager: AnnBe
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 3c3b251aadfa997f453e60b0842f89a6f09eb9cb
ms.sourcegitcommit: 88347d0f0ac862a77f269a05f1801d30dc93586e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2020
ms.locfileid: "3260258"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>コード別消費税支払レポートの印刷 

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

**コード別消費税支払** レポートを印刷するには、**税** \> **照会およびレポート** \> **消費税レポート** \> **コード別消費税支払** に移動します。 既定では、レポート金額は、**消費税レポート コード** ページで設定されたすべてのレポート コードについて法人の会計通貨で生成されます。

また、このレポートを生成して、**消費税コード** ページで消費税コードに割り当てられているすべてのレポート コードについて、消費税コードの通貨で消費税支払額を表示することもできます。

## <a name="turn-on-the-feature"></a>機能をオンにする

**機能管理** ワークスペースで、次の機能を有効にします: **コード別消費税支払レポートを消費税コードの通貨で生成する**。

## <a name="run-the-report"></a>レポートの実行

1. **税** \> **照会およびレポート** \> **消費税レポート** \> **コード別消費税支払** の順に移動します。
2. **レポート通貨** フィールドで、次のいずれかの値を選択します:

    - **会計通貨** – レポート金額を会計通貨で印刷します。
    - **消費税コードの通貨** – 消費税コードの通貨でレポート金額を印刷します。

    ![コード別消費税支払ダイアログ ボックス](media/Sales-tax-payment-by-code.png)

次の図で、生成されるレポートの例を示します。 レポート コードが割り当てられている消費税コードに対して **消費税通貨** フィールドが **EUR** に設定されている場合、レポート コード **101** が通貨 **EUR** であることがレポートに表示されます。

![コード別消費税支払レポートの例](media/Sales-tax-payment-by-code-2.png)