---
title: 販売コミッションの登録
description: この手順は、販売コミッションを計算および登録する方法を示します。
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c0e63923d0cb9a4a2c2bed87cfb72edfb0d2741
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833909"
---
# <a name="register-sales-commissions"></a>販売コミッションの登録

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順は、販売コミッションを計算および登録する方法を示します。 この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。 このガイドを開始する前に、必要なすべてのコミッション計算の設定ができていることを確認するために、「販売コミッション ルールの設定」と呼ばれるガイドを実行します。

このコミッションのプロセスとして選択した顧客と品目をメモして、このガイドで販売注文を作成するように要求された時にそれらを使用してください。


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>販売担当者がコミッションを取得する販売注文の請求
1. [販売とマーケティング] > [販売注文] > [すべての販売注文] の順に移動します。
2. [新規] をクリックします。
3. [顧客口座] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、目的のレコードを見つけ、選択します。
5. 一覧で、選択された行のリンクをクリックします。
6. [OK] をクリックします。
7. [アクション] ウィンドウで、[オプション] をクリックします。
8. [ビューの変更] をクリックします。
9. [ヘッダーの表示] をクリックします。
10. [設定] セクションを展開します。
    * [売上グループ] フィールドの値は、1 人以上の販売担当者が割り当てられたグループを表します。 このグループのメンバーが、注文が請求された時に、事前定義されたレートおよび配分でコミッションを受け取ります。   値は顧客カードからコピーされますが、変更することもできます。  [売上] グループは販売注文明細行にもコピーされます。 ヘッダーおよび/または明細行間のものと異なるように変更できます。  
    * [コミッション グループ] フィールドの値は、コミッションを追跡するために、1 人以上の顧客に対して作成したグループを表します。   値は顧客カードからコピーされますが、変更することもできます。   
11. [アクション] ウィンドウで、[オプション] をクリックします。
12. [ビューの変更] をクリックします。
13. [明細行の表示] ] をクリックします。
14. [品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
15. 一覧で、コミッション用に設定した品目を選択します。 
16. [数量] フィールドに数値を入力します。
    * ラインの [正味金額] をご確認下さい。 これは、この例ではコミッション計算の基準となる、売上収益を表します。  
17. [保存] をクリックします。
18. アクション ウィンドウで、[請求書] をクリックします。
19. [請求書] をクリックします。
20. [パラメーター] セクションを展開します。
21. [数量] フィールドで、「すべて」を選択します。
22. [転記] フィールドで、[はい] を選択します。
23. [OK] をクリックします。
24. [OK] をクリックします。
    * トランザクションの転記には、1 分程度必要な場合があります。 処理が完了するまで、ページを閉じないで下さい。  

## <a name="review-the-registered-sales-commissions"></a>登録された販売コミッションの確認
1. アクション ウィンドウで、[請求書] をクリックします。
2. [請求書] をクリックします。
3. アクション ウィンドウで、[請求書] をクリックします。
4. [コミッション トランザクション] をクリックします。
    * 請求済の販売注文に関連付けられる販売担当者に支払うコミッションの金額を表す行が [概要] タブに表示されます。 詳細を確認しましょう。     
    * 「販売コミッション ルールの設定」ガイドを使用してコミッション売上グループを設定した場合、販売コミッションを受取る販売担当者は 2 人で、コミッションは、2 人に均等に分割されます。  
    * この例では、コミッションの合計金額は売上収益の割合 (注文明細行の正味金額) として計算されます。   
5. ページを閉じます。
6. [伝票] をクリックします。
    * 伝票トランザクションを確認すると、事前定義されたコミッション経費とコミッション支払勘定に転記されたコミッション金額が分かります。  

