---
title: "分析コード メンバーの共通設定に、原価要素の分析コード メンバーをマップします。"
description: "異なる原価要素分析コード メンバーに、原価要素分析コード メンバーの共通セットをマッピングすると、分析に使用する共通の形式でデータをマージします。"
author: YuyuScheller
manager: AnnBe
ms.date: 2016-11-01 13 - 45 - 07
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: a1e9817b6ee596ad516531d7597a2a39e115749c
ms.lasthandoff: 03/31/2017


---

# <a name="map-different-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>分析コード メンバーの共通設定に、原価要素の分析コード メンバーをマップします。

異なる原価要素分析コード メンバーに、原価要素分析コード メンバーの共通セットをマッピングすると、分析に使用する共通の形式でデータをマージします。

グローバル会社で、法律の会計要件に準拠している場合は、複数の勘定科目表を使用する必要があります。 さまざまな勘定科目表から原価要素分析コード メンバーをインポートすると、勘定の組み合わせが発生します。 ただし、これらの勘定は、実際に同じ性質を持ち、共通の形式を使用して原価を分析および割り当てる場合があります。

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>原価要素分析コード メンバーに共通の形式をマップします
次の例では、原価コントローラーとして、原価要素分析コード メンバーを米国の勘定科目表の構造やフランスの勘定科目表の構造から原価要素分析コード メンバーの共通のセットにマッピングする原価計算で、新しい原価要素分析コードを作成する方法を示します。 その後、原価要素分析コード メンバーの共通セットを使用して、原価会計元帳の 2 つの法人から原価データを分析することができます。

| ソース: 米国の勘定科目表                                          | ソース: フランスの勘定科目表                                          | 原価要素分析コード メンバーの新しい共通セット                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| 米国の勘定科目表からインポートされた原価要素分析コード メンバー | フランスの勘定科目表からインポートされた原価要素分析コード メンバー | 米国とフランスの原価要素分析コード メンバーの共通セットへのマッピング |
| 5001: 販売                                                           | 5001: 販売と広告                                               | 5000: 販売と広告                                             |
| 5030: 広告                                                     | 6390: 株式購入\*                                                    | 7000: クリーニング費用                                                 |
| 7001: クリーニング費用                                               | 7001: 旅費交通費                                                      | 7001: 旅費交通費                                                   |

\*株式購入フランスの原価要素の分析コードにマップされていません。

## <a name="currency-conversion"></a>通貨の換算
使用するさまざまな勘定科目表は、異なる通貨を使用するように設定されたかもしれません。 この場合に、必ず通貨換算を指定してください、原価データは、原価要素分析コード メンバーが使用した原価会計元帳で正しい通貨を使用して処理されます。 前の例では、原価会計元帳で米ドル (USD) が使用された場合、マップされた原価要素分析コード メンバーのトランザクションを処理するために USD からユーロ (EUR) の通貨換算を作成する必要があります。

## <a name="update-mappings-at-any-time"></a>いつでもマッピングを更新
いつでも原価要素分析コードのためのマッピングの定義を更新できます。 マッピングは、日付が有効ではないので、変更は次回原価トランザクションを処理、または原価計算を実行の時に適用されます。

