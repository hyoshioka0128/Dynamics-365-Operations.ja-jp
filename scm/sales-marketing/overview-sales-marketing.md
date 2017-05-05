---
title: "販売とマーケティング"
description: "販売およびマーケティングを使用して、販売フローのさまざまなタイプのデータを取得、保存、および使用できます。 このデータには、元の販売戦略、将来のフォローアップ アクション、および追加販売が含まれます。"
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92303
ms.assetid: 65ca9992-bbfa-4224-bf0e-067a25c7e6a4
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f9e79b5dad120e057193b97d9c87665c54fea023
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-marketing"></a>販売とマーケティング

[!include[banner](../includes/banner.md)]


販売およびマーケティングを使用して、販売フローのさまざまなタイプのデータを取得、保存、および使用できます。 このデータには、元の販売戦略、将来のフォローアップ アクション、および追加販売が含まれます。

<a name="marketing"></a>マーケティング
---------

マーケティング キャンペーンや活動を使用して、潜在的な顧客との関係を模索して構築し、初期の相互作用を販売関係へと発展させることができます。 次のプロセス フローは、マーケティングの業務プロセスを表しています。 [![マーケティングの業務プロセス](./media/marketing01.jpg)](./media/marketing01.jpg)

### <a name="relationships"></a>リレーションシップ

販売およびマーケティングでは、潜在的な顧客との初期の相互作用がさまざまな状況で発生します。 たとえば、トレード ショーに参加しているとき見込みのある顧客を見つけたり、組織が大量のキャンペーン メールの送信を実行した後、可能性のある潜在顧客を獲得するかもしれません。 その相手が顧客になる前に、相手のエンティティの流れを理解することが重要です。 次の図は、潜在的な顧客が実際の顧客になる場合の、エンティティの関連付けのフローを示します。 [![SalesandMarketing01](./media/salesandmarketing01.jpg)](./media/salesandmarketing01.jpg)

### <a name="campaigns"></a>キャンペーン

キャンペーンは、見込顧客、潜在顧客、営業案件、およびキャンペーンに参加するように選択されているお客様の連絡先をターゲットとします。 Microsoft Dynamics 365 for Operations では、潜在的な顧客を最大化するため、テレマーケティング、メーリングおよびメールでのキャンペーンなどのキャンペーンのいくつかの種類を作成できます。 キャンペーンが進行して積極的な反応を受け取ると、キャンペーンに積極的に反応したこれらの受信者への営業プロセスを開始できます。

## <a name="sales"></a>販売注文
販売機能を使用して、見積、新規および既存のお客様のアップセル/クロスセルを作成し、販売注文の作成および顧客の売上請求書を作成します。 次のプロセス フローは、販売の業務プロセスを表しています。 [![販売の業務プロセス](./media/sales01.jpg)](./media/sales01.jpg)

### <a name="sales-quotations"></a>販売見積

お客様に提供する商品やサービスの、提示するサービスの販売見積を作成します。 お客様は、見積書を要求する可能性があります。または潜在的なまたは既存の顧客からの要求に対する応答として見積書を作成する場合があります。 お客様が販売見積を承認すると、販売注文に変換できます。

### <a name="up-sellcross-sell"></a>アップセル/クロスセル

アップセル/クロスセルは、顧客の注文を入力するときに製品を販売するための手法です。 アップセルでは、現在の製品ではなく別の製品を推奨します。 クロスセルでは、現在の製品に加えて別の製品を推奨します。 製品リストを設定するときは、クロスセルまたはアップセル製品としての製品の提案を示すために特定の規則を作成できます。

### <a name="sales-orders"></a>販売注文

新しい販売注文を作成する際には、作成する注文タイプを選択する必要があります。 5 つのオプションがあります。 **注:** 販売注文を作成した後、任意の注文タイプは変更できますが、販売注文が [**出荷済**] のステータスの場合は、[**要件の項目**] を変更することはできません。

| 販売注文タイプ  | 説明                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 仕訳帳           | 販売注文の下書きとしてこのタイプを使用します。 このタイプは在庫数量に影響を与えることはなく、品目トランザクションの生成も行われません。                                                                                                                                                                    |
| 定期売買      | このタイプを繰返し注文に対して使用します。 注文の請求を行うと、注文のステータスが自動的にオープン注文に設定されます。 出荷済の数量が請求され、残りの出荷が更新されます。 倉庫管理機能を使用する場合、この販売注文タイプは使用できません。 |
| 販売注文       | 顧客が配置または注文を確認するときは、このタイプを使用します。                                                                                                                                                                                                                                        |
| 返品済注文    | 顧客が品目を戻す場合にこのタイプを使用します。 返品品目番号 (RMA 番号) が自動的に割り当てられます。                                                                                                                                                                                            |
| 在庫品目要求 | プロジェクトを使用して品目の販売を行うときにこのタイプが自動的に作成されます。                                                                                                                                                                                                                       |

### <a name="sales-agreements"></a>販売契約書

販売契約書は、特定の数量または特定の量の製品を、一定期間に特別価格と割引で購入することを顧客と約束する契約です。 販売契約書の価格と割引により、存在する売買契約で指定された価格や割引は却下されます。 販売契約書は、定義された期間有効です。 [**販売注文**] ページの販売用に指定されている要求された出荷日が有効な期間である必要があります。 既定では、販売契約書は保留中です。 [**有効**] に設定されている場合にのみ販売契約書から注文できます。

### <a name="backorders"></a>オーダー残

注文を入力および検証する際、販売の完了時になる前に、オーダー残と例外を管理する必要があります。 オーダー残とは、仕入先から未出荷の購買注文、または顧客に対して未出荷の販売注文です。 受注残のフォローアップは重要です。 たとえば、仕入先からの製品が遅延すると、顧客への出荷日を変更し、遅延について顧客に通知する必要が生じる場合があります。 品目、顧客、または仕入先別オーダー残を表示できます。

#### <a name="viewing-backorders-by-item"></a>品目別受注残の表示

オーダー残を品目ごとに表示すると、特定の品目のトランザクションの今後の流れをフォローアップできます。 たとえば、以下の情報を確認できます。

-   品目に対する販売注文数
-   仕入先からの品目の納入がまだ紛失中
-   適切なタイミングですべての販売注文を出荷できるようにするためには追加の品目を注文すべきかどうか

このチェックを行うと、アイテムの配信のタイミングに関する顧客からの要求に応答できます。 さらに、販売のオーダー残に優先順位を付けたり、手持在庫の品目を注文間で分割することもできます。

#### <a name="viewing-backorders-by-customer"></a>顧客別受注残の表示

顧客ごとのオーダー残を表示すれば、顧客の残りの注文の状態を見ることができます。 このチェックは、遅延している項目を待機しているお客様に対応する必要がある場合に便利です。

#### <a name="viewing-backorders-by-vendor"></a>仕入先別受注残の表示

仕入先別オーダー残を表示すると、配送漏れおよび納期予定日をフォローアップできます。 このチェックは、仕入先から製品が到着し、販売注文をピッキングして出荷する際のオーダー残の優先順位付けにも役立ちます。

### <a name="invoices"></a>請求書

販売プロセス中に次の 3 つのタイプの請求書を作成できます。

-   顧客請求書
-   自由書式の請求書
-   見積送り状

#### <a name="customer-invoice"></a>顧客請求書

顧客請求書は、組織が売上について顧客に提供する請求書です。 ヘッダーおよび品目またはサービスの 1 つまたは複数の明細行を含む販売注文に基づいて、このような顧客請求書を作成します。 顧客請求書は、販売注文、梱包明細、および売上請求書サイクルを終了します。  

販売注文または梱包明細および日付に基づいて、1 つの顧客請求書を転記し、印刷できます。 梱包明細と日付に基づく複数の顧客請求書を一緒に転記および印刷することもできます。 販売注文を使用して 1 つの請求書を転記すると、各品目の [**請求残金**] の数量は、選択した販売注文の請求された数量の合計で更新されます。  

販売注文のすべての品目の [**請求残金**] の数量と [**出荷更新待ち**] の数量が両方とも 0 (ゼロ) の場合、販売注文のステータスが [**請求済**] に変更されます。 どちらかのフィールドの数量がゼロでない場合は、販売注文のステータスが変更されず、追加の請求書を入力できます。 梱包明細に基づく、1 つまたは複数の顧客請求書を転記し印刷する場合は、各販売注文の梱包明細を少なくとも 1 つがすでに転記されている必要があります。 それらの梱包明細に基づいて顧客請求書が作成され、一覧表示された数量が反映されます。  

特定の販売注文の品目がまだすべて出荷されていなくても、それまでに出荷された梱包明細行の品目に基づいて顧客請求書を作成することができます。 たとえば、法人で各顧客に対してその月のすべての出荷を網羅した 1 つの請求書を月ごとに発行する場合などにこの機能を使用できます。 各梱包明細は、販売注文の品目の一部またはすべての出荷を表します。  

請求書を転記すると、各品目の [**請求残金**] の数量は、選択した梱包明細の出荷された数量の合計で更新されます。 販売注文のすべての品目の [**請求残金**] の数量と [**出荷更新待ち**] の数量が両方とも 0 (ゼロ) の場合、販売注文のステータスが [**請求済**] に変更されます。 数量がゼロでない場合は、販売注文のステータスが変更されず、追加の請求書を入力できます。 在庫トランザクションが請求書番号で更新され、販売注文の行のステータスが [**請求済**] に変更されます。

#### <a name="free-text-invoice"></a>自由書式の請求書

自由書式の請求とは、販売注文に関連付けられていない請求書のことです。 この請求書には、勘定科目、自由書式の説明、および売上金額の注文明細行が含まれています。 このような請求書の品目番号を入力することはできず、適切な売上税情報を入力する必要があります。 販売のメインのアカウントは、各請求書の明細行に示されます。 顧客残高は自由書式の請求書に使用される転記プロファイルの集計勘定に転記されます。

#### <a name="pro-forma-invoice"></a>見積送り状

見積送り状は、請求書が転記される前に実際の請求金額の見積として準備される請求書です。 顧客請求書用または自由書式の請求書用の見積送り状を印刷できます。



