---
title: 事前定義された製品バリアントの製品番号の分類の作成
description: この手順では、事前定義済製品バリアントの製品番号の分類を設定する方法、および適切な製品分析コード グループに割り当てる方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a2e61fd99cb80a1a9cc3d8e985fb0f14e3c2fc2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844684"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>事前定義された製品バリアントの製品番号の分類の作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、事前定義済製品バリアントの製品番号の分類を設定する方法、および適切な製品分析コード グループに割り当てる方法を示します。 この手順の作成に使用するデモ データの会社は USMF です。 新しい製品番号に関する分類は、色やサイズの製品分析コード グループに割り当てられます。 このタスクは、通常、製品デザイナーが行います。


## <a name="create-a-product-number-nomenclature"></a>[製品番号の分類] を作成します。
1. [製品バリアント モデルの定義] をクリックします。
2. [製品の分類] をクリックします。
3. [新規] をクリックします。
4. [名前] フィールドに、目標の製品分析コード グループ、たとえば、ColorSize を特定する用語の名前を入力します。
5. [説明] フィールドに値を入力します。
6. [追加] をクリックします。
7. [製品マスター番号] をクリックします。
8. [追加] をクリックします。
9. [テキスト定数] をクリックします。
10. [テキスト] フィールドに値を入力します。
11. [追加] をクリックします。
12. [色] をクリックします。
13. [追加] をクリックします。
14. [テキスト定数] をクリックします。
15. [テキスト] フィールドに値を入力します。
16. [追加] をクリックします。
17. [サイズ] をクリックします。
18. ページを閉じます。

## <a name="assign-the-nomenclature-to-a-product-master"></a>製品マスターに用語を割り当て
1. [製品分析コード グループ] をクリックします。
2. [SizeCol 製品分析コード グループ] を選択します。
3. [編集] をクリックします。
4. [分類の使用] フィールドで、[はい] を選択します。
5. [製品バリアント番号の分類] フィールドに、値を入力または選択します。
6. ページを閉じます。

