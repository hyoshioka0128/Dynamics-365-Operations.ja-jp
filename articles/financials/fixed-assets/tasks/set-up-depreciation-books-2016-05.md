---
title: 資産減価償却簿の設定 (2016 年 5 月)
description: このタスク ガイドでは、新しい減価償却簿が作成さし、固定資産グループに関連付けます。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6840e211847494598a81cd3228dbd3796447e18c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839860"
---
# <a name="set-up-depreciation-books-may-2016"></a>資産減価償却簿の設定 (2016 年 5 月)

[!include [task guide banner](../../includes/task-guide-banner.md)]

このタスク ガイドでは、新しい減価償却簿が作成さし、固定資産グループに関連付けます。  これは USMF の法人に対して経理担当ロールとデモ データを使用します。


## <a name="create-a-depreciation-book"></a>減価償却簿の作成
1. [固定資産] > [設定] > [減価償却簿] の順に移動します。
2. [新規] をクリックします。
3. [減価償却簿] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
5. [減価償却の計算] チェック ボックスをオンまたはオフにします。
6. [減価償却プロファイル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. 一覧で、目的の減価償却プロファイルを見つけ、選択します。
8. 一覧で、選択された行のリンクをクリックします。
9. [代替減価償却プロファイル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
10. 一覧で、目的の減価償却プロファイルを選択します。
11. 一覧で、選択された行のリンクをクリックします。
    * 特別減価償却プロファイルは、特殊な状況で資産の割増償却に使用されます。 たとえば、自然災害の結果の減価償却を記録する場合などに、このフィールドを使用できます。  
12. [基準調整を含む減価償却調整を作成する] チェック ボックスをオンまたはオフにします。
13. [カレンダー] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
14. 一覧で、選択された行のリンクをクリックします。

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a>減価償却簿を固定資産グループに関連付ける
1. [固定資産グループ] をクリックします。
2. [固定資産グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、目的のレコードを見つけ、選択します。
4. 一覧で、選択された行のリンクをクリックします。
5. [減価償却方法] フィールドで、オプションを選択します。
6. [耐用年数] フィールドに数値を入力します。
    * 耐用年数を設定した後に減価償却期間のフィールド値が計算されます。  

