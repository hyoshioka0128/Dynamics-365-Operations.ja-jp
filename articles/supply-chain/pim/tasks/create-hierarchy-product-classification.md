---
title: 製品分類の階層の作成
description: この手順では、新しいカテゴリ階層を作成し、商品コード階層タイプを割り当てる方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: faf43eb15283ffd7e36ad38728f166884dddcd85
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844828"
---
# <a name="create-a-hierarchy-of-product-classification"></a>製品分類の階層の作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、新しいカテゴリ階層を作成し、商品コード階層タイプを割り当てる方法を示します。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は、カテゴリ マネージャーを対象としています。


## <a name="create-the-new-category-hierarchy"></a>新しいカテゴリ階層の作成
1. **ナビゲーション ウィンドウ > モジュール > 製品情報管理 > 設定 > カテゴリと属性 > カテゴリ階層**の順に移動します。
2. **新規** をクリックします。
3. **名前**フィールドに値を入力します。
4. **説明**フィールドで、値を入力します。
5. **作成** をクリックします。

## <a name="build-the-hierarchy"></a>階層の構築
1. **新規**カテゴリ ノードをクリックします。
2. **名前**フィールドに値を入力します。
3. **コード** フィールドに値を入力します。
4. **フレンドリ名**フィールドで、値を入力します。
5. **新規**カテゴリ ノードをクリックします。
6. **名前**フィールドに値を入力します。
7. **コード** フィールドに値を入力します。
8. **フレンドリ名**フィールドで、値を入力します。
9. **新規**カテゴリ ノードをクリックします。
10. **名前**フィールドに値を入力します。
11. **コード** フィールドに値を入力します。
12. **フレンドリ名**フィールドで、値を入力します。
13. **新規**カテゴリ ノードをクリックします。
14. **名前**フィールドに値を入力します。
15. **コード** フィールドに値を入力します。
16. **フレンドリ名**フィールドで、値を入力します。
17. ページを閉じます。

## <a name="classify-the-hierarchy"></a>階層の分類
1. 一覧で、目的のレコードを見つけ、選択します。
2. **アクション ウィンドウ**で、**カテゴリ階層**をクリックします。
3. **階層タイプの関連付け**をクリックします。
4. **新規** をクリックします。
5. **カテゴリ階層タイプ** フィールドで、オプションを選択します。 **製品分類で商品コードのカテゴリ階層タイプ**を選択します。  
6. **カテゴリ階層**フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. 一覧で、目的のレコードを見つけ、選択します。
8. 一覧で、選択された行のリンクをクリックします。
9. ページを閉じます。

