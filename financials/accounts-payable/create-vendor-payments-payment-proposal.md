---
title: "仕入先支払を使用して仕入先請求書を作成"
description: "このトピックでは、支払提案オプションの概要および支払提案の機能を示す例をいくつか提供します。 多くの場合、支払提案は仕入先支払の作成に使用されます。これは、クエリを使用すると、支払の仕入先請求書を期日および現金割引などの基準に基づいて支払の仕入先請求書を素早く選択することができるためです。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14312
ms.assetid: 585d5b0b-1b79-4a03-ab18-528918070377
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: b46037b9509f329e18f0da69d530f6b1f88c8888
ms.lasthandoff: 03/31/2017


---

# <a name="create-vendor-payments-by-using-a-payment-proposal"></a>仕入先支払を使用して仕入先請求書を作成

このトピックでは、支払提案オプションの概要および支払提案の機能を示す例をいくつか提供します。 多くの場合、支払提案は仕入先支払の作成に使用されます。これは、クエリを使用すると、支払の仕入先請求書を期日および現金割引などの基準に基づいて支払の仕入先請求書を素早く選択することができるためです。 

多くの組織では、仕入先支払の作成に支払提案を使用します。これは、支払提案のクエリを使用すると、支払の仕入先請求書を期日、現金割引、その他の基準に基づいて素早く選択することができるためです。 

支払提案のクエリにはさまざまなタブが表示され、それぞれに支払する請求書を選択するためのさまざまなオプションがあります。 **パラメータ**タブは、使用の大部分は、通常はオプションがあります。 定義によって支払に含めることがあるか**含めるレコード** FastTabで、請求書または仕入先がさまざまな特性に指定できます。 たとえば、特定の仕入先支払範囲のみ場合は、仕入先の範囲のフィルタを定義できます。 この機能は、頻繁に使用される支払方法の詳細に請求書を選択する。 たとえば、のみフィルタを**支払方法を** = **チェック**、クエリで指定されるそのほかの条件を満たす場合、定義すると、支払方法がある請求書が支払に選択されます。 **詳細パラメーター** タブには、追加オプションが含まれます。一部の組織には関連しない場合があります。 たとえば、このタブには、集中支払の請求書の支払オプションが含まれています。

## <a name="parameters"></a>パラメーター
-   ** [選択した請求– **はによって指定された日付範囲内に請求書**日付から、および** ** **フィールドは、期日と現金割引日、またはも選択できます。 現金割引日を使用して、まず、とその日の日付までの現金割引日を持つ請求書が検索されます。 その後システムにより、セッションの日付を使用して現金割引日が過ぎていないことが確認され、現金割引の適用対象となるかどうか判断されます。
-   **開始日**と**終了日** – この日付範囲内に期日または現金割引日を持つ請求書が支払のために選択されます。
-   **支払期日** – 日付が定義されている場合、すべての支払はこの日付で作成されます。 **最短支払期日**フィールドは無視されます。
-   **最短支払期日** – 最短支払期日を入力します。 たとえば、**日付から**と** [**このフィールドは9年1月1日から9年1月10日の範囲を指定し、最小支払額日付は9.月5日です。 この場合、しか金を9年1月1日から9年1月5日の開始されるすべての請求書は9.月5日の支払日があります。 ただし、しか金を9年1月5日から9年1月10日の開始されるすべての請求書は請求の期日から支払日があります。
-   **金額限度** – すべての支払についての最大合計金額を入力します。
-   **このオプションが設定された請求書は** – **されていない支払をはい**、支払がすぐに作成されます**仕入先支払**ページ作成します。 **支払提案**ページはスキップされます。 したがって、支払はより迅速に作成されます。 支払は、**仕入先支払**ページから変更できます。 また、**選択した支払の請求書を編集**ボタンを使用して、**支払提案**ページに戻ることができます。

## <a name="advanced-options"></a>詳細オプション
-   **仕入先残高の確認** – このオプションが**あり**に設定されている場合、請求書の支払が行われる前に、仕入先に借方残高がないことがシステムによって確認されます。 仕入先の借方残高がある場合、支払は作成されません。 たとえば、仕入先は貸方転記済だがまだ決済されていないメモ、または支払があるかもしがあります。 このような場合、仕入先に対する支払は行いません。 代わりに、未払の請求書に対してクレジット メモまたは支払を決済する必要があります。
-   **負の支払の削除** – このオプションは、支払が個別の請求書に対して行われたか、支払の基準を満たす請求書の合計に対して行われたかによって機能が異なります。 この動作は支払方法で定義されます。
-   **各請求書の支払** – **負の支払の削除**オプションで**あり**が選択され、かつ仕入先に未決済の請求書や支払がある場合、請求書のみが支払対象として選択されます。 既存の支払は、請求書に対して決済されません。 **負の支払の削除**オプションで**なし**が選択され、請求書と支払が未決済の場合、請求書と支払の両方が支払対象として選択されます。 支払は、その支払に対して作成され、払戻 (負の支払) はその支払に対して作成されます。
-   **請求書の合計の支払** – **負の支払の削除**オプションで**あり**が設定され、仕入先に未決済の請求書や支払がある場合、未決済の請求書や支払が支払対象として選択され、金額を合算して合計支払額にします。 唯一の例外は、合計が払戻になった場合に発生します。 この場合、請求書も支払も選択されません。 **削除の負の支払**オプションが設定されている** **、請求書が決済されていない支払、請求、支払は支払し、支払金額合計金額を生産する一つに追加されます。
-   **レポートの印刷のみ** – このオプションを**あり**に設定すると、支払提案の結果を表示するのみで、支払は作成しません。
-   **他の法人からの仕入先請求書を含める** – 組織に支払の集中支払提案プロセスがあり、検索基準に含まれる他の法人からの請求書を支払提案に含める必要がある場合は、このオプションを**あり**に設定します。
-   **法人ごとに個別の仕入先支払を提案** – このオプションが**あり**に設定されている場合、仕入先ごとに各法人に対して個別の支払が作成されます。 支払にある仕入先は、各法人からの請求書の仕入先です。 このオプションで**なし**が設定され、同じ仕入先に複数の法人の請求書がある場合は、選択された請求書の合計金額について単一の支払が作成されます。 支払の仕入先には、現在の法人の仕入先が使用されます。 現在の法人に仕入先勘定が存在しない場合は、支払対象の最初の請求書の仕入先勘定が使用されます。
-   **支払通貨**すべての支払が作成されます。–、このフィールドは、通貨を指定します。 通貨が定義されていない場合、各、請求書の通貨に支払われます。
-   **支払が行われる平日** – 支払を行う曜日を入力します。 このフィールドは、特定の曜日に支払う請求書を合計する支払方法が設定されている場合にのみ使用されます。
-   **相手勘定のタイプと** **相手勘定** –特定の勘定タイプ (**などの元帳**または**銀行**) と相手勘定を指定するには、次のフィールドを設定します (その銀行口座など)。 請求書の支払方法は既定の相手勘定タイプと相手勘定を指定し、既定値を上書きする、これらのフィールドを使用できます。
-   **追加のフィルタ** – **含めるレコード** FastTabの条件の追加の範囲を定義できます。 たとえば、仕入先の範囲は支払場合は、仕入先の範囲のフィルタを定義できます。 この機能は、頻繁に使用される支払方法の詳細に請求書を選択する。 たとえば、のみフィルタを**支払方法を** = **チェック**、クエリで指定されるそのほかの条件を満たす場合、定義すると、支払方法がある請求書が支払に選択されます。

## <a name="scenarios"></a>シナリオ
| ベンダー | 請求書 | 請求日 | 請求金額 | 期日 | 現金割引日 | 現金割引金額 |
|--------|---------|--------------|----------------|----------|--------------------|----------------------|
| 3050   | 1001    | 6 月 15 日      | 500.00         | 7 月 15 日  | 6 月 29 日            | 10.00                |
| 3050   | 1002    | 6 月 20 日      | 600.00         | 7 月 20 日  | 7 月 4 日             | 12.00                |
| 3075   | 1003    | 6 月 15 日      | 250.00         | 6 月 29 日  |                    | 0.00                 |
| 3100   | 1004    | 6 月 17 日      | 100.00         | 7 月 17 日  | 7 月 1 日             | 1.00                 |

7 月 1 日に、エイプリルは仕入先に支払います。 彼女は、このタスクをより効率的に完了するために役立つ支払提案を使用します。

### <a name="option-1-by-cash-discount"></a>オプション 1: 現金割引適用

エイプリルは**現金割引**を提案タイプとして選択します。 彼女は6年1月26日から7年1月10.日の日付範囲を入力します。 次の請求書提案に含まれます:

-   1002、7 月 4 日の割引日が支払日の範囲内にあるためです。
-   1004、7 月 1 日の割引日が支払日の範囲内にあるためです。

次の請求書は提案に含まれません。

-   1001、6 月 29 日の割引日が既に期限切れで、この請求書は現金割引の対象外になっているためです。
-   1003、請求書に割引日がないためです。

### <a name="option-2-by-due-date"></a>オプション 2: 期日別

エイプリルは **期日別** を提案タイプとして選択します。 彼女は6年1月26日から7年1月10.日の日付範囲を入力します。 次の請求書提案に含まれます:

-   1003、6 月 29 日の期日が支払日の範囲内にあるためです。

次の請求書は提案に含まれません。

-   1001、7 月 15 日の期日が支払日の範囲外にあるためです。
-   1002、7 月 20 日の期日が支払日の範囲外にあるためです。
-   1004、7 月 17 日の期日が支払日の範囲外にあるためです。

### <a name="option-3-by-due-date-and-cash-discount"></a>オプション 3: 期日別および現金割引

エイプリルは **期日および現金割引** を提案タイプとして選択します。 彼女は6年1月26日から7年1月10.日の日付範囲を入力します。 次の請求書提案に含まれます:

-   1003、6 月 29 日の期日が支払日の範囲内にあるためです。
-   1002、7 月 4 日の割引日が支払日の範囲内にあるためです。
-   1004、7 月 1 日の割引日が支払日の範囲内にあるためです。

次の請求書は提案に含まれません。

-   1001、6 月 29 日の割引日が既に期限切れで、この請求書は現金割引の対象外になっていて、7 月 15 日の期日もこの日付範囲の外にあるためです。

## <a name="country-specific-considerations"></a>国固有の考慮事項
### <a name="norway"></a>ノルウェー

#### <a name="dimension-control"></a>分析コードのコントロール

分析コードのコントロールは支払提案によって生成された明細行のグループ化を制御し、また請求書に適用する財務分析コードに基づいて既定の分析コードを設定することができます。 支払方法ごとのノルウェーの国コンテキストで、分析コードのコントロールの有効および各分析コードのグループ化を有効にする財務分析コードタブがあります。 選択できるオプションは次のとおりです。

-   [**分析コードのコントロール**] フィールドは無効になります。 支払提案は他の国と同じように機能します。
-   [**分析コードのコントロール**] フィールドは、詳細な分析コードを定義しなくても有効になります。 支払提案は、分析コードを考慮しなくても作成されます。 作成されたトランザクションは適用されるエントリから分析コードを継承しません。
-   [**分析コードのコントロール**] フィールドは有効化されており、詳細な分析コードも有効になっています。 ここでは、分析コードが仕訳帳にコピーされる方法を定義します。 例: • 支払方法の業務単位あたりの支払提案を作成するにBusinessUnit ** **チェック ボックスをオンにします。• 支払方法の原価部門ごとの支払提案を作成するにCostCenter ** **チェック ボックスをオンにします。

**注記:** 3 番目のオプションで複数の分析コードを選択すると、分析コードの組み合わせに対して支払提案が作成されます。

#### <a name="bank-account-selection"></a>銀行口座の選択

国コンテキストに関係なく、支払方法ごとに標準の借方支払勘定を定義できます。 これは、提案によって生成された支払明細行で設定されます。 銀行口座機能を使用すると、分析コードおよび通貨で、または異なる借方銀行口座を使用するこれらの組み合わせでその組み合わせに応じて、複数の借方銀行口座の管理を定義できます。 **使用して銀行口座**ボタンをクリックして**転記勘定タイプ** = **銀行に使用できる**の各支払方法を、これらの組み合わせの** **ページの支払方法を設定できます。

