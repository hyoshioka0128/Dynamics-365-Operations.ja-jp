---
title: "一部金額の支払"
description: "1 つの請求書の量より少ない支払いを仕入先に行う場合があります。 この記事は、この状況を処理するためのさまざまなオプションについて説明します。 利用できるオプションは、業務要件とコンフィギュレーションによって異なります。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 45d28110ca93875eb534c69886ac2074ea4fe737
ms.openlocfilehash: 191d1ee0b47da4930e10146ba164d601d038e81b
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2017

---

# <a name="vendor-payments-for-a-partial-amount"></a>一部金額の支払

[!include[banner](../includes/banner.md)]


1 つの請求書の量より少ない支払いを仕入先に行う場合があります。 この記事は、この状況を処理するためのさまざまなオプションについて説明します。 利用できるオプションは、業務要件とコンフィギュレーションによって異なります。 

<a name="cash-discount-amounts"></a>現金割引金額
---------------------

ベンダーは、期日までに請求書の支払いをする場合の現金割引を提供できます。 たとえば、請求書が 10 日以内に支払われた場合は 2% の現金割引が指定される 100.00 の請求書を入力します。 期日の条件は 30 日になります。 支払提案が、請求書を選択するための条件として現金割引を使用する場合、また提案が現金割引日かそれ以前に実行される場合、請求書が支払に選択され、98.00 の支払いが作成されます。 現金割引は、手動で作成された 1 回限りの支払にも適用できます。

## <a name="partial-payments-with-cash-discounts"></a>現金割引される一部支払
全額請求書を決済するために追加の一部支払を作成するつもりで、一部支払を行う場合があります。 一部支払の現金割引を適用するには、**買掛金勘定パラメーター** ページで **一部支払の現金割引を計算** オプションを、**はい** に設定する必要があります。 

たとえば、請求書が発行されてから 10 日以内に支払われた場合に、2% の割引が指定される現金割引を受け取ります。 請求書に 100.00 が転記されています。 10 日以内に 49.00 の支払を行う場合、支払仕訳に 49.00 の借方金額を入力します。 一部支払を **トランザクションの決済** ページで決済すると、**適用する現金割引金額** フィールドに **1.00** が表示されます。 

> [!NOTE] 
> 一部支払を入力して、[**決済金額**] フィールドに完全な請求金額を残す場合、[**適用する現金割引金額**] フィールドはトランザクションを転記するときに自動的に計算されます。

## <a name="credit-notes-with-cash-discounts"></a>現金割引の訂正票
請求書の品目の一部を返す場合、訂正票を受け取ります。 現金割引が元の請求書に適用された場合、割引の値を差し引き、正しい量の返金を受け取ります。 **買掛金管理パラメーター** ページの **訂正票に対する現金割引を計算** オプションが **はい** に設定されている場合、貸方票のために割引が自動的に計算されます。 

たとえば、請求書が発行されてから 10 日以内に支払われた場合に、2% の割引が指定される現金割引を受け取ります。 請求書に 100.00 が転記されています。 品目を返品して貸方票を受け取る場合、クレジット メモで定義された 2% の現金割引とともに、元の請求書の総額 100.00 の貸方票を入力できます。  貸方票を **未処理トランザクションの決済** ページで表示する場合、**98.00** は **決済金額** フィールドに表示され、**-2.00** は **現金割引金額** フィールドに表示されます。 割引量が現金割引勘定に転記されます。

## <a name="overpaymentunderpayment-amounts"></a>過剰支払/過少支払の量
一部支払い後に、決済する必要がある額がきわめて小さい場合があります。 たとえば、仕入先請求書が 1,000.00 で支払が 999.90 を支払うとします。 残りの金額が [**買掛金管理パラメーター**] ページの過剰支払または過小支払に指定される量より少ない場合、差額が過剰支払/過少支払の勘定科目に自動的に転記されます。


詳細については、[仕入先の支払概要](../cash-bank-management/tasks/vendor-payment-overview.md) を参照してください。
