---
title: 個別資産の減損インジケーターの管理
description: このタスクを使用して、個別資産の減損インジケーターの管理方法を把握します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetImpairmentIndicator_JP, AssetImpairmentReview_JP, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b7c33948a7805358b4b3bcd7e5fffa5c72a7fec3
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848778"
---
# <a name="maintain-impairment-indicators-on-individual-assets"></a>個別資産の減損インジケーターの管理

[!include [task guide banner](../../includes/task-guide-banner.md)]

このタスクを使用して、個別資産の減損インジケーターの管理方法を把握します。



この手順を実行する前に、「減損会計の共通パラメーターの設定」タスクを実行します。 



この手順では、JPMF デモ会社のデータを使用します。


## <a name="update-impairment-indicator-on-a-single-fixed-asset"></a>単一の固定資産の減損インジケーターを更新
1. [固定資産] > [固定資産] > [固定資産] に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * 例: TOOLM-000006  
3. [帳簿] をクリックします。
4. [機能] をクリックします。
5. [減損インジケーターの更新] をクリックします。
6. [新規] をクリックします。
7. [日付の変更] フィールドに、日付を入力します。
    * 例: 2013-04-01  
8. [説明] フィールドに値を入力します。
9. [割引前キャッシュ フロー] フィールドに数値を入力します。
    * この例では、フィールドに「3900000」を入力します。  
10. [回収可能金額] フィールドに、数値を入力します。
    * この例では、フィールドに「3350226」を入力します。  
11. [保存] をクリックします。

## <a name="update-impairment-indicator-on-the-impairment-management-form"></a>減損管理フォームの減損のインジケーターを更新
1. 次の順に移動します: [固定資産] > > .. > [減損管理]。
2. [クエリ] をクリックします。
3. 固定資産グループの行の、[基準] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. [OK] をクリックします。
5. 一覧で、目的のレコードを見つけ、選択します。
    * TOOLM-000007  
6. 一覧で、目的のレコードを見つけ、選択します。
    * TOOLM-000008  
7. [減損インジケーターの更新] をクリックします。
8. 一覧で、選択された行をマークします。
    * 固定資産番号「TOOLM-000007」を持つレコードを選択します。  
9. [日付の変更] フィールドに、日付を入力します。
    * 日付を定義 = 2013-04-01  
10. [説明] フィールドに値を入力します。
11. [割引前キャッシュ フロー] フィールドに数値を入力します。
    * 2500000.00 を入力します。  
12. [回収可能金額] フィールドに、数値を入力します。
    * 入力 = 2000000.00。  
13. 一覧で、目的のレコードを見つけ、選択します。
    * 固定資産番号「TOOLM-000008」を持つ行を選択します。  
14. [日付の変更] フィールドに、日付を入力します。
15. [説明] フィールドに値を入力します。
16. [割引前キャッシュ フロー] フィールドに数値を入力します。
    * 2000000.00 を入力します。  
17. [回収可能金額] フィールドに、数値を入力します。
    * 1500000.00 を入力します。  
18. [インジケーターの更新] をクリックします。

