---
title: 半完成品の作成 (2016 年 2 月)
description: このタスクでは、半完成品の作成に重点を置きます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39fb652d704da33d24a206da2c18cc2a7a50e9e4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844516"
---
# <a name="create-a-semi-finished-product-february-2016"></a>半完成品の作成 (2016 年 2 月)

[!include [task guide banner](../../includes/task-guide-banner.md)]

このタスクでは、半完成品の作成に重点を置きます。 これは、BOM 計算シリーズの 2 番目のタスクです。 このタスクの作成に使用するデモ データの会社は USMF です。

1. [製品情報管理] > [製品] > [リリースされた製品] の順に移動します。
2. [新規] をクリックします。
3. [製品番号] フィールドに値を入力します。
    * この例では、「BOM_2」を入力します。  
4. [品目モデル グループ] フィールドで、値を入力または選択します。
    * [STD] を選択します。 STD は標準原価の意味であり、原価計算を行うときによく使用するモデルです。  
5. [品目グループ] フィールドで、値を入力または選択します。
    * たとえば、「AUDIO」を選択します。 これは原価計算には影響しません。  
6. [保管分析コード グループ] フィールドで、値を入力または選択します。
    * 「SiteWH」を選択します。 この例では、サイトと倉庫のみが使用されます。  
7. [追跡用分析コード グループ] フィールドで、値を入力または選択します。
    * 追跡用分析コードはこの例には使用されません。「なし」を選択してください。  
8. [OK] をクリックします。
9. [アクション] ウィンドウで [在庫の管理] をクリックします。
10. [既定の注文設定] をクリックします。
11. [既定の注文タイプ] フィールドで、「生産」を選択します。
    * これは生成される半完成品であるので、「生産」を選択します。  
12. [購買サイト] フィールドで、値を入力または選択します。
    * この例では、「サイト 1」を選択します。  
13. [在庫サイト] フィールドで、値を入力または選択します。
    * この例では、「サイト 1」を選択します。  
14. [販売サイト] フィールドで、値を入力または選択します。
    * この例では、「サイト 1」を選択します。  
15. ページを閉じます。
16. [アクション] ペインで [原価の管理] をクリックします。
17. 品目価格をクリックします。
18. [新規] をクリックします。
19. 一覧で、選択された行をマークします。
20. [バージョン] フィールドで、値を入力または選択します。
    * この例では、「バージョン 10」を選択します。  
21. [サイト] フィールドで値を入力または選択します。
    * この例では、「サイト 1」を選択します。  
22. 単価を「10」に設定します。
    * たとえば、原価価格 10 を入力します。  
23. [保存] をクリックします。
24. [保留中の価格の有効化] をクリックします。
25. ページを閉じます。
26. ページを閉じます。
27. [BOM_2] をクリックして開きます。
28. [原価の管理] セクションを展開します。
29. [原価グループ] フィールドで、値を入力または選択します。
    * この例では、原価グループ M1 を選択します。  
30. レコードを保存するショートカットを使用します。
31. ページを閉じます。

