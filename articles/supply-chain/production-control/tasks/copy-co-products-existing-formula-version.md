---
title: 既存のフォーミュラ バージョンから連産品をコピー
description: この手順では、既存のフォーミュラ バージョンから、リリース済製品の別のフォーミュラ バージョンに連産品をコピーする方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 626c0fc8a60eeb84060d7279833de583d55a95a2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838754"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a>既存のフォーミュラ バージョンから連産品をコピー

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、既存のフォーミュラ バージョンから、リリース済製品の別のフォーミュラ バージョンに連産品をコピーする方法を示します。 連産品と関連付けられている少なくとも 1 つのフォーミュラ バージョンがあることが前提条件です。 この手順の作成に使用するデモ データの会社は USP2 です。


## <a name="find-a-released-product"></a>リリース済製品の検索
1. [リリースされた製品] に進みます。
2. [フィルターの表示] をクリックします。
    * フィルターのダイアログ ボックスで [生産] タイプのフィールドを追加しようとしています。  
3. [生産] タイプのフィールドを追加するために [フィルター フィールドの追加] をクリックします。
    * 次の手順で、[適用] を選択する前に手動で [生産タイプ] フィールドに式を入力する必要があります。 これは、リリース済製品一覧のフィルターを設定します。  
4. 手動で [生産タイプ] フィールドに式を入力します。
5. [適用] をクリックします。

## <a name="select-a-released-product"></a>リリース済製品の選択
1. 一覧で、目的のレコードを見つけ、選択します。
2. [フォーミュラ バージョン] をクリックします。
    * [技術アクション ペイン] で、[フォーミュラ バージョン] をクリックします。  

## <a name="copy-co-products"></a>連産物のコピー
1. [アクション ペイン] で、[フォーミュラ バージョン] をクリックします。
2. [連産品 (複数)] をクリックします。
3. [コピー] をクリックします。
4. [品目番号] フィールドで、値を入力または選択します。
5. [フォーミュラ バージョン] フィールドで、値を入力または選択します。
6. [OK] をクリックします。
7. ページを閉じます。

