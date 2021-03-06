---
title: 消費税コードを設定します
description: このトピックでは、Dynamics 365 for Finance and Operations で売上税コードを設定する方法について説明します。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3419c6b569093d717158e80bd9bc01054d82bff9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834833"
---
# <a name="set-up-sales-tax-codes"></a>消費税コードを設定します

[!include [task guide banner](../../includes/task-guide-banner.md)]

このトピックでは、Dynamics 365 for Finance and Operations で売上税コードを設定する方法について説明します。 売上税コードは、法人が計算、収集、税務当局への支払いの義務のあるそれぞれの間接税または関税について作成されます。

このタスクでは、USMF というデモ会社を使用します。

1. **ナビゲーション ウィンドウ > 税 > 間接税 > 売上税 > 売上税コード**の順に移動します。
2. **新規** を選択します。
3. **売上税コード** フィールドで、値を入力します。
4. **名前**フィールドに値を入力します。
5. プルダウン リストを開いて**決済期間**を選択すると、この売上税の報告と支払いを行う売上税所轄官庁の指定や、その間隔の指定ができます。
6. 総勘定元帳に売上税を転記する主勘定を指定するには、**元帳転記グループ**を選択します。
7. **計算**クイック タブを展開します。 これには、売上税額の計算方法を制御する複数のフィールドがあります。 必要に応じて、これらのフィールドに入力します。  
8. インターフェイスの上部にある**アクション ウィンドウ**で、**売上税コード**を選択します。
9. **値**を選択します。
10. この税コードの値を**値**列に入力します。
    - **計算**クイック タブの発生元フィールドで、単位あたりの金額がオンの場合、売上税金額の計算では、値にトランザクションの数量が乗算されます。  税コードが単位に基づく税でない場合、値は、売上税金額を計算するためにこの税コードの発生元に適用される割合を示す値になります。     
11. **保存** を選択します。
12. ページを閉じます。
13. **保存** を選択します。

