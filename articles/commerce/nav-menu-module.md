---
title: ナビゲーション メニュー モジュール
description: このトピックでは、ナビゲーション メニュー モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: eee3523be26369aecdb36c0143a6ee3dab4b7966
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2020
ms.locfileid: "4413889"
---
# <a name="navigation-menu-module"></a>ナビゲーション メニュー モジュール

[!include [banner](includes/banner.md)]

このトピックでは、ナビゲーション メニュー モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。

## <a name="overview"></a>概要

ナビゲーション メニュー モジュールの主な目的は、Dynamics 365 Commerce 本社で定義されているチャンネル ナビゲーション階層に従って、サイトのユーザーが商品やサイトのページを参照できるようにすることです。 ナビゲーション メニュー モジュールでコンフィギュレーションされた品目は、サイトのヘッダーのナビゲーションとして表示されます。 ナビゲーション メニュー モジュールは、電子商取引サイトの他のページにリンクする静的メニュー項目もサポートします。

ナビゲーション メニュー モジュールは、ページのヘッダー モジュールに追加できます。 Fabrikam テーマでは、ナビゲーション メニューは既定では 2 つのレベルで表示されます。 Starter テーマでは、ナビゲーション メニューは既定では 3 つのレベルで表示されます。 レベル数を変更するには、テーマにビュー拡張機能が必要です。

次の図は、カテゴリ階層の 2 つのレベルと、いくつかの静的メニュー項目を含む、Fabrikam サイトのナビゲーション メニューの例を示しています。
![ナビゲーション メニュー モジュールの例](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>ナビゲーション メニュー モジュールのプロパティ

| プロパティ名             | 先頭値                 | 説明 |
|---------------------------|-----------------------|-------------|
| 配賦元                  | **Retail**、**手動による作成**、**Retail と手動作成** | **Retail** の値を使用すると、Commerce 本社のチャンネル ナビゲーション階層がナビゲーション メニューに表示されます。 **手動作成** の値によって、静的なメニュー項目を選別できます。 **Retail および手動作成** 値により、両方を組み合わせることができます。 |
| カテゴリ イメージの表示 | **True** または **False**    | このプロパティを有効にすると、カテゴリごとのカテゴリ イメージがナビゲーション メニューに表示されます。 Commerce リリース 10.0.14 に追加されました。 |
| 複数レベルのナビゲーション メニューの有効化 | **True** または **False** | このプロパティを有効にすると、ナビゲーション メニューに複数のレベルのナビゲーション階層を表示できます。 この機能は Dynamics 365 Commerce 10.0.15 リリースで使用できます。 |
| レベルの数 | integer | このプロパティは、**複数レベルのナビゲーション メニューの有効化** プロパティが、**True** に設定されている場合に表示されるレベルの数を定義します。 |
| 静的メニュー項目| 値の配列| メニュー項目名を静的サイトページへのリンクに関連付ける静的メニュー項目。 その他のメニュー項目以下にメニュー項目を作成できます。 既定では、静的メニューはルート レベルで表示され、存在する場合はチャンネル ナビゲーション階層に追加されます。 |
| ルート メニューを表示 | **True** または **False** | このプロパティを有効にすると、ナビゲーション メニューをカスタム ルート (例えば **今すぐ購入**) で定義できます。 この機能は Dynamics 365 Commerce 10.0.15 リリースで使用できます。 |
| ルート メニュー | 文字列 | **ルート メニューを表示** プロパティが **True** に設定されている場合、このプロパティを使用してカスタム ルートのテキストを定義できます。 |

次の図は、Fabrikam サイトのナビゲーション メニューに表示されるカテゴリ イメージの例を示しています。
![カテゴリ イメージを含むナビゲーション メニュー モジュールの例](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>ヘッダー モジュールへのナビゲーション メニュー モジュールの追加

ナビゲーション メニュー モジュールをヘッダー モジュールに追加する方法の詳細については、[ヘッダー モジュール](author-header-module.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[階層リンク モジュール](add-breadcrumb.md)

[サイト セレクター モジュール](site-selector.md)

[購入ボックス モジュール](add-buy-box.md)

[Cookie のコンプライアンス](cookie-compliance.md)

[ヘッダー モジュール](author-header-module.md)