---
title: 支払仕訳帳を使用した仕入先月次締め請求書の決済
description: 日本では、支払は月次締め請求書に対して行われ決済されます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendConsInvoice_JP, LedgerJournalTable, LedgerJournalTransVendPaym, VendPaymProposalEdit
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dcd6cf011343519735c4cc02398162d044a3e781
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848661"
---
# <a name="settle-vendor-consolidated-invoices-by-using-a-payment-journal"></a>支払仕訳帳を使用した仕入先月次締め請求書の決済

[!include [task guide banner](../../includes/task-guide-banner.md)]

日本では、支払は月次締め請求書に対して行われ決済されます。



この手順では、支払仕訳帳と支払提案機能を使用した月次締め請求書の決済について説明します。 



この手順を完了する前に、月次締め請求書が作成され確定済であることを確認します。 



この手順は、デモ データ会社 JPMF を使用して作成されました。

1. [買掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。
2. 後で参照するために、[締め ID] フィールドの値をメモします。
    * デモ データ会社 JPMF の JPMF-000002 を使用できます。  
3. [買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。
4. [新規] をクリックします。
5. [名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、選択された行のリンクをクリックします。
7. [明細行] をクリックします。
8. [支払提案] をクリックします。
9. [支払提案の作成] をクリックします。
10. [詳細パラメーター] セクションを展開または折りたたみます。
11. [締め ID] フィールドに値を入力します。
    * [月次締め請求書] ページで、事前にメモした値を使用できます。  
12. [OK] をクリックします。
13. [支払の作成] をクリックします。
    * 支払明細行が提案に基づいて生成されていること、および転記日付を提供していることを確認します。  
    * 1 件の月次締め請求書に関連付けられている請求書が複数ある場合は、支払仕訳帳に複数の明細行を生成することができます。  
14. [転記] をクリックします。
15. [買掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。
    * 月次締め請求書のステータスが [決済済] に更新されていることを確認します。  

