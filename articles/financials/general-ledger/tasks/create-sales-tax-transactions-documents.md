---
title: ドキュメントの売上税トランザクションの作成
description: ドキュメントの売上税は、ドキュメント明細行の売上税グループと品目売上税グループを指定することにより計算されます。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 653b93744f5b891655cade0cb669d34179fca9cd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846538"
---
# <a name="create-sales-tax-transactions-on-documents"></a>ドキュメントの売上税トランザクションの作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

ドキュメントの売上税は、ドキュメント明細行の売上税グループと品目売上税グループを指定することにより計算されます。 これらはマスター データから既定値が取得されますが、必要に応じて手動で変更できます。 計算済売上税は、明細行とドキュメント レベルで確認できます。 このタスクでは、USMF というデモ会社を使用します。

1. [売掛金勘定] > [注文] > [すべての販売注文] の順に移動します。
2. [新規] をクリックします。
3. [顧客口座] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、目的のレコードを見つけ、選択します。
5. 一覧で、選択された行のリンクをクリックします。
6. [OK] をクリックします。
7. 一覧で、選択された行をマークします。
8. [品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
9. 一覧で、選択された行のリンクをクリックします。
10. [単価] フィールドに数値を入力します。
11. [明細行の詳細] セクションを展開または折りたたみます。
12. [設定] タブをクリックします。
13. [品目売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
14. 一覧で、目的のレコードを見つけ、選択します。
15. 一覧で、選択された行のリンクをクリックします。
16. [財務] をクリックします。
17. [売上税] をクリックします。
18. [OK] をクリックします。
19. [明細行の追加] をクリックします。
20. 一覧で、選択された行をマークします。
21. [品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
22. 一覧で、目的のレコードを見つけ、選択します。
23. 一覧で、選択された行のリンクをクリックします。
24. [単価] フィールドに数値を入力します。
25. [品目売上税グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
26. 一覧で、目的のレコードを見つけ、選択します。
27. 一覧で、選択された行のリンクをクリックします。
28. [アクション] ペインで [販売] をクリックします。
29. [売上税] をクリックします。
30. [OK] をクリックします。

