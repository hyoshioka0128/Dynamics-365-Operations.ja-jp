---
title: 裏書済受取手形の取消
description: このタスクは、裏書きされた為替手形の取消について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustBillOfExchangeEndorseListPage, CustBillOfExchangeEndorseReverse, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 73da319a08a5a64dd4a7f21dab865cb08e5d9e65
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848759"
---
# <a name="reverse-an-endorsed-bill-of-exchange"></a>裏書済受取手形の取消

[!include [task guide banner](../../includes/task-guide-banner.md)]

このタスクは、裏書きされた為替手形の取消について説明します。



このタスクを完了するには、少なくとも 1 つの裏書きされた為替手形が必要です。 

このタスクは デモ データ会社 JPMF を使用して作成されました。

1. [買掛金勘定] > [支払] > [裏書為替手形] に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * ステータスが「裏書済」の為替手形を選択します。  仕入先トランザクションが既に決済されている場合、為替手形を引き当てるられないことに注意してください。 裏書を引き当てる前に決済を元に戻す必要があります。  
3. [裏書の取消] をクリックしてドロップ ダイアログを開きます。
4. [裏書の取消] をクリックします。
    * 引当日は、必要に応じて変更できます。  
5. [照会] をクリックします。
6. [伝票] をクリックします。
    * 会計伝票が取消に対して生成されていることを確認します。  

