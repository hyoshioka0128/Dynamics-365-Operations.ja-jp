---
title: サイトのスケジュールの作成
description: この手順は、サイトでまだ開始されていない製造オーダーをスケジュールする方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51c9ca8c402880f93a5998605d946b881d5ccdf5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835881"
---
# <a name="create-a-schedule-for-a-site"></a>サイトのスケジュールの作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順は、サイトでまだ開始されていない製造オーダーをスケジュールする方法を示します。  この手順を完了するのにデモ データの会社 USMF が使用されています。


## <a name="identify-production-orders-that-are-not-started"></a>開始されていない製造オーダーを識別します
1. [生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、「1」という値で [サイト] フィールドをフィルター処理します。
    * 1 では USMF 内のサイトを表します。 USMF を使用していない場合は、自分の会社からサイトを選択します。  
3. [ステータス列フィルター] を開きます。
4. [次の値と完全に一致する] フィルター演算子を使用して、[ステータス] フィールドに値 [スケジュール済] でフィルターを適用します。

## <a name="create-a-schedule"></a>スケジュールの作成
1. 一覧で、すべての行のマークを設定または解除します。
2. [アクション ペイン] で、[スケジュール] をクリックします。
3. [ジョブのスケジュール] をクリックします。
4. [スケジューリング指示] フィールドで、[出荷日からバックワード] をクリックします。
5. [有限能力] フィールドで [いいえ] を選択します。
6. [有限原材料] フィールドで [いいえ] を選択します。
7. [OK] をクリックします。
    * しばらく時間がかかる場合があります  

## <a name="view-the-result-of-scheduled-production-orders"></a>スケジュールされた製造オーダーの結果を表示します
1. 一覧で、選択された行をマークします。
    * どの行でもマークできます。  
2. アクション ウィンドウで、[製造オーダー] をクリックします。
3. [すべてのジョブ] をクリックします。
    * このページで、ジョブのリストを表示できます。 [スケジューリング] タブで、ジョブの開始日と終了日を表示できます。  
4. [材料] をクリックします。
    * このページで、製造オーダー工程用の材料消費見積、および現在利用可能な在庫を確認できます。  

