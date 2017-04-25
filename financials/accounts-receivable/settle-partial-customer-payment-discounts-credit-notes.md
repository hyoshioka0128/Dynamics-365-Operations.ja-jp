---
title: "貸方票の割引がある部分的な顧客支払を決済します。"
description: "この記事は、貸方票に現金割引が適用され、元の請求書にも現金割引がある場合のシナリオについて説明します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: e43bcea67d9c408c93258f9b64565560b59fbb88
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>貸方票の割引がある部分的な顧客支払を決済します。

この記事は、貸方票に現金割引が適用され、元の請求書にも現金割引がある場合のシナリオについて説明します。 

Fabrikam は、一部支払または貸方票 (クレジット メモ)で顧客が現金割引を使用できるようにしています。 現金割引は、顧客が現金割引を受ける請求書に対して貸方票が発行されたときに、貸方票に適用することができます。 総額の貸方を提供する代わりに、顧客が受けた現金割引の割合を除外した金額の顧客残高を貸方転記できます。 決済パラメータは**売掛金勘定パラメータ**ページにあります。

## <a name="invoice-and-credit-note"></a>請求書および貸方票
顧客 4035 には 1,000.00 の請求書と 100.00 の訂正票があります。 各ドキュメントは、14 日以内に支払われる場合、1 パーセントの割引があります。 アーニーはこの情報を**顧客トランザクション** ページで表示できます。

| 伝票番号    | トランザクション タイプ | 日      | 請求書  | トランザクション通貨での借方金額 | トランザクション通貨での貸方金額 | 残高  | 通貨 |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10050  | 請求書          | 6/28/2015 | 10050    | 1,000.00                             |                                       | 1,000.00 | USD)       |
| CCRN-10050 | 訂正票      | 6/28/2015 | CR-10050 |                                      | 100.00                                | -100.00  | USD)       |

## <a name="settle-a-credit-note-with-an-invoice"></a>請求書を含む訂正票の決済
アーニーは**顧客トランザクション**ページから**トランザクションの決済**ページを開きます。 **トランザクションの決済**ページを使用して、その請求書と貸方票を決済できます。 決済プロセスの一部として、現金割引の日付、金額を表示します。 その 2 通の文書にマークし、**転記**をクリックしてトランザクションを決済します。 Fabrikam が訂正票の割引を許可するため、訂正票の -1.00 の割引があります。

| マーク     | 現金割引の使用 | 伝票番号    | 口座 | 日      | 期日  | 請求書  | トランザクション通貨の金額 | 通貨 | 決済金額 |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| 選択済 | 標準            | FTI-10050  | 4035    | 6/28/2015 | 7/28/2015 | 10050    | 1,000.00                       | USD)       | 990.00           |
| オン | 標準            | CCRN-10050 | 4035    | 6/28/2015 | 7/28/2015 | CR-10050 | -100.00                        | USD)       | -99.00           |

割引の情報は [**トランザクションの決済**] ページの下部に表示されます。

|                              |           |
|------------------------------|-----------|
| 現金割引日           | 7/12/2015 |
| 現金割引金額         | -1.00     |
| 現金割引の使用            | 標準    |
| 適用される現金割引          | 0.00      |
| 適用する現金割引金額 | -1.00     |

決済は 100.00 で、99.00 の支払、1.00 の割引が含まれます。

