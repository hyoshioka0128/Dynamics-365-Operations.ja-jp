---
title: 小売明細書の店舗のコンフィギュレーション
description: この手順では、小売明細書の作成される影響を及ぼす、転記または小売店舗のコンフィギュレーションを説明します。
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fddeb8434d916df1613d61da88110dec8fb4465
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563647"
---
# <a name="store-configurations-for-retail-statements"></a>小売明細書の店舗のコンフィギュレーション

[!include[task guide banner](../includes/task-guide-banner.md)]

この手順では、小売明細書の作成される影響を及ぼす、転記または小売店舗のコンフィギュレーションを説明します。 小売店舗の財務分析コードは別の手順に含まれます。 この手順では、USMF というデモ会社を使用します。

1. [小売とコマース] > [チャンネル] > [小売店舗] > [すべての小売店舗] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. 一覧で、選択された行のリンクをクリックします。
    * [明細書/決済] セクションの設定は、明細書の作成、検証、店舗の転記に影響します。  [明細書/決算] セクションを開きます。  
    * 明細行のグループ化に使用する方法を選択します。  
    * 明細書を作成するバッチ ジョブから明細書を作成するとき、1 日あたり一つの明細書のみが作成されるようにするには、「はい」を選択します。  
    * [支払/入金申告の計算] フィールドは、支払/入金申告を一緒に追加するか、または最後の一つを使用するかどうかを定義します。  
    * 丸め差額を転記する [勘定科目] を選択します。  
    * [最大丸め金額] フィールドでは、許可されている最大丸め誤差を入力できます。  
    * [転記] フィールドでは、明細書で許可される最大転記差額の合計を入力できます。  
    * [シフト] フィールドでは、明細書のシフトの最大差額の合計を入力できます。  
    * [トランザクション] フィールドでは、明細行の最大差額の合計を入力できます。  
    * [決済方法] フィールドで、明細書に含まれているトランザクションが終了したシフトの一部であるか、または定義済みの日時範囲内のトランザクションであるかどうかを定義できます。  
    * 午前 0 時より後に前日に転記される必要のあるトランザクションが発生した場合、[営業日の終了] フィールドに時間を入力できます。  
    * 午前 0 時より後に、前日に転記される必要のあるトランザクションが発生した場合は、「はい」を選択します。  
    * 定義された各明細書の方法で明細書が作成されるようにする場合は、「はい」を選択します。 これは、並列処理できる小さな明細書が大量に作成されるため、店舗の大量のトランザクションの転記のパフォーマンスを改善する必要がある場合に役立ちます。  
    * [既定の顧客] フィールドで、飛び込みの顧客への販売に使用する顧客口座を選択できます。  

