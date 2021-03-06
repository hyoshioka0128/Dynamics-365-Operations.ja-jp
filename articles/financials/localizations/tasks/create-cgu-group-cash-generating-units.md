---
title: CGU グループおよび資産グループの作成
description: 日本では、固定資産の減損は、個々の固定資産または資産グループに基づき決定することができます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetImpairmentCashGenUnitGroup_JP, SysQueryForm, AssetImpairmentCashGenUnit_JP
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca2482da21d9bbb9d8a333a0a3b1b3149fd149fa
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848980"
---
# <a name="create-cgu-group-and-cash-generating-units"></a>CGU グループおよび資産グループの作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

日本では、固定資産の減損は、個々の固定資産または資産グループに基づき決定することができます。 資産グループに基づき減損を評価する場合の最初のステップは、固定資産を資産グループにグループ化することです。 



最適な CGU を選択できるよう、キャッシュ生成単位の複数のセットが許可されています。 これは、CGU グループを作成することで達成されます。 



この手順では、CGU グループと資産グループの作成について説明します。 また、固定資産の資産グループへの割当方法と、共有資産および営業権の CGU グループへの割当方法も確認することができます。 



このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



この手順は、デモ データ会社 JPMF を使用して作成されました。


## <a name="create-a-cgu-group"></a>CGU グループの作成
1. [固定資産] > [設定] > [減損] > [CGU グループ] の順に移動します。
2. [新規] をクリックします。
    * 固定資産と資産グループの適切な組み合わせが不明な場合は、テスト用に複数の CGU グループを作成できます。  
3. [CGU グループ] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
5. [営業権と共有資産の減損] フィールドで、オプションを選択します。
    * 会社のポリシーに従って方法を選択します。  
6. [保存] をクリックします。

## <a name="create-cash-generating-units-under-the-cgu-group"></a>CGU グループ下での資産グループの作成
1. [新規] をクリックします。
2. [名前] フィールドに値を入力します。
3. 後で参照できるよう、[資産グループ番号] フィールドの値をメモします。
    * 資産グループをコンフィギュレーションする場合は、この値を参照する必要があります。  
4. [新規] をクリックします。
5. [名前] フィールドに値を入力します。
6. 後で参照できるよう、[資産グループ番号] フィールドの値をメモします。
    * 資産グループをコンフィギュレーションする場合は、この値を参照する必要があります。  

## <a name="assign-shared-assets-and-goodwill-to-the-cgu-group"></a>共有資産と営業権の CGU グループへの割り当て
1. [共有資産と営業権] のセクションを展開します。
2. [一括インポート] をクリックします。
    * その条件と一致するすべての資産を一度に追加する条件を指定することをお勧めします。   グリッドに、資産を 1 つずつ入力することもできます。  
3. [基準] フィールドに値を入力します。
4. [OK] をクリックします。

## <a name="configure-cash-generating-units"></a>資産グループのコンフィギュレーション
1. [固定資産の割り当て] をクリックします。
2. [クイック フィルター] を使用して編集する CGU を検索します。
    * 以前にメモした最初の資産グループ番号を入力します。  
3. [一括インポート] をクリックします。
    * その条件と一致するすべての資産を一度に追加する条件を指定することをお勧めします。   グリッドに、資産を 1 つずつ入力することもできます。  
4. [基準] フィールドに値を入力します。
    * 例: 場所 = 福岡  
5. [OK] をクリックします。
6. [割引前キャッシュ フロー] フィールドに数値を入力します。
7. [回収可能価額] フィールドに数値を入力します。
8. [保存] をクリックします。
9. [クイック フィルター] を使用して編集する資産グループを検索します。
    * 以前にメモした 2 番目の資産グループ番号を入力します。  
10. [一括インポート] をクリックします。
11. [基準] フィールドに値を入力します。
    * 例: 場所 = 大阪  
12. [OK] をクリックします。
13. [割引前キャッシュ フロー] フィールドに数値を入力します。
14. [回収可能価額] フィールドに数値を入力します。
15. [保存] をクリックします。

## <a name="activate-the-cgu-group"></a>CGU グループの有効化
1. [有効化] をクリックします。
    * 認識テストの実行に使用できるのは、有効な CGU グループだけです。  
2. [はい] をクリックします。

