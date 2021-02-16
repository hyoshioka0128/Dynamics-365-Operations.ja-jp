---
title: 出荷先住所モジュール
description: このトピックでは、支払いモジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: aeaa410fde29b285fdbbdd6acac19b0c4e917aa5
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2020
ms.locfileid: "4413914"
---
# <a name="shipping-address-module"></a>発送先住所モジュール

[!include [banner](includes/banner.md)]

このトピックでは、支払いモジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。

## <a name="overview"></a>概要

出荷先住所モジュールにより、顧客がチェックアウト フロー中に注文の出荷先住所を追加または選択できます。 顧客がサインインしている場合、その顧客用に以前に保存されたすべての住所が表示され、そこから選ぶことができます。 顧客は、新しい住所を追加することもできます。 出荷先住所モジュールは、出荷を必要とする注文のすべての品目に対して使用されます。

Commerce 本社では、国や地域ごとに送付先住所の形式を定義することができます。その後、送付先住所モジュールは、国/地域に固有のルールを適用します。

顧客がチェックアウト フロー中に送付先住所を入力する場合、オプションでその住所を基本住所として保存することができます。 このオプションは、顧客がログインしている場合にのみ表示されます。

送付先住所モジュールでは住所検証はおこないませんが、この機能はカスタマイズを通じて実装できます。

以下の図は、精算ページのす新規送付先住所モジュールの例を示しています。

![精算ページの出荷先住所モジュールの例](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>モジュール プロパティ

| プロパティ名 | 値 | 説明 |
|---------------|--------|-------------|
| ヘッダー | ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**) | 出荷先住所モジュールのオプション ヘッダー。 |
| 住所タイプを表示する | **True** または **False** | このオプションのプロパティが **True** に設定されている場合は、**自宅** や **勤務先** などの住所タイプが表示されます。 住所タイプが指定されていない場合、住所は **タイプ**=**その他** として自動的に保存され ます。 |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>精算ページに出荷先住所モジュールを追加して必要なプロパティを設定する

出荷先住所モジュールは、精算モジュールにのみ追加できます。 出荷先住所モジュールをコンフィギュレーションして精算ページに追加する方法の詳細については、[精算モジュール](add-checkout-module.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[買い物カゴ モジュール](add-cart-module.md)

[カート アイコン モジュール](cart-icon-module.md)

[チェックアウト モジュール](add-checkout-module.md)

[支払モジュール](payment-module.md)

[配送オプション モジュール](delivery-options-module.md)

[集荷情報モジュール](pickup-info-module.md)

[注文詳細のモジュール](order-confirmation-module.md)

[ギフト カード モジュール](add-giftcard.md)