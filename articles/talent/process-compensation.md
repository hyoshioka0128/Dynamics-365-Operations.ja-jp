---
title: 報酬処理
description: 報酬処理では、賃金調整、昇給目標、およびパフォーマンスに基づいて、従業員の新しい基本報酬金額を計算することができます。
author: andreabichsel
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 30b09f09875e37a6a909d0aad04117e577c5cd98
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518463"
---
# <a name="process-compensation"></a>報酬処理

[!include [banner](includes/banner.md)]

報酬処理では、賃金調整、昇給目標、およびパフォーマンスに基づいて、従業員の新しい基本報酬金額を計算することができます。 このトピックでは、従業員のパフォーマンスを考慮しない固定報酬プランの報酬処理の基本フローについて説明します。

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>新しい報酬金額と予算を計画する
従業員に昇給目標を与えるには、報酬管理 > リンク > 昇給目標の順に移動し、各部門の固定昇給予算を設定する必要があります。 (または、部門: 組織 > 部門を介してこのフォームを開くこともできます。) ここでは、特定の労働組合または場所の従業員が異なる増加率を得るべきかどうかをさらに指定することができます。 **予算**および**通貨**フィールドは情報的なもので、予算の通貨金額に注意するために使用できます。

## <a name="set-up-the-compensation-process"></a>報酬プロセスの設定
プロセス イベントでは、報酬処理のためのパラメータを指定できます。 これには、報酬金額、および新しい報酬金額が有効になる日付を決定するための評価期間が含まれます。

任意の固定報酬プランのいずれかがパーセンテージの採用ルールを使用している場合は、採用日付で比例配分される固定支払を含めることができます。 これらの計画では、サイクル開始日以降、固定支払比例配分の採用日付前に雇用された人は、計算された昇給または一般昇給の 100 ％ を受け取ります。 固定支払比例配分の採用日付後でサイクル終了日前に雇用された人は、雇用された総サイクル日数のうち何日が経過したかに基づいて計算された昇給の一部を受け取ることになります。 たとえば、当社のサイクルが 1 月 1 日から 12 月 31 日までで、および 4 月 1 日の固定支払比例配分の採用日付がある場合、3 月に雇用された従業員は計算された昇給の満額を受け取り、7 月 1 日に雇用された従業員は計算された昇給の約半分を受け取ります。

プロセス イベント**特定の時点**の日付は、特定の変動報酬プランの処理にのみ使用され、ここではカバーされません。 **期限の確認**は、すべての報酬認定を作成する期限であり、新しい報酬金額を従業員のレコードに読み込むことができます。 期限の確認は、情報のみを目的としています。

プロセス イベントのパラメータが保存されたら、**設定**ボタンをクリックして、このプロセスが実行される時に含めるプランおよび各プランに対してどの固定補償アクションを実行するかを指定できます。

プロセス イベントに報酬プランを追加するには、**プラン**タブの**追加**ボタンをクリックします。 **他のレバレッジを使用**、**レバレッジ係数**、および**レバレッジの説明**列は、変動報酬プランに対してのみ使用し、このトピックではカバーされません。

レコードを保存し、次に**アクション**タブの**追加**ボタンをクリックして、選択したプランの固定補償アクションを追加します。 アクションの計算されたガイドラインの昇給とは異なる金額を入力するには、**推奨事項の有効化**オプションを使用します。 以前のアクションの結果に基づいたアクションを計算して複数の報酬アクションをリンクさせるには、説明的な名前を付けることができる補償ロジックのタイプである**前回の結果を使用する**オプション、固定報酬アクションにマークを付けます。 等級およびバンド プランの場合、以下のタイプの固定補償アクションのみを追加することができます:

| 固定報酬アクションのタイプ | 機能                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 株主資本                        | 株主資本のアクションでは、従業員のジョブに示されている最低基準地点と、サイクル終了日の従業員の賃金率を比較します。 従業員の支払レートが最低基準点設定を下回っている場合、従業員をその範囲内の最小点にするために必要な昇給が計算されます。                                                                                |
| メリット                         | 昇給アクションでは、サイクル終了日の従業員の支払レートに基づいて昇給を計算し、従業員の部門、労働組合、および場所の固定昇給予算内の昇給を計算します。                                                                                                                                                                                         |
| 一般                       | 一般的なアクションでは、パーセンテージに基づいて昇給を計算するか、または従業員に均一の金額を与えます。 これは、**一般**タブの**固定報酬**の設定に基づいて決定されます。                                                                                                                                                                                                                        |
| プロモーション                     | プロモーション アクションでは、昇給を与えることができる名前付きの場所を提供するため、**推奨事項の有効化**オプションをマークして、プロモーションを受け取る従業員の推奨事項を入力できるようにしてください。  推奨される昇給のない従業員は、固定報酬レコードに**プロモーション**アクションはありません。                                                                       |
| その他のレベル変更            | 前の例では、**降給**は、**その他のレベル変更**タイプの**固定報酬**アクションの名称です。 従業員の支払レートを調整する報酬認定額を入力できるように、0 (ゼロ変更) 規定昇給が生成されます。 (**推奨事項の有効化**オプションにマークを付けてください。) 推薦されない従業員は、このアクションを固定報酬レコードに追加することはありません。 |

ステップのタイプと**固定報酬**アクションのみをステップ プランに追加することができます。

| 固定報酬アクションのタイプ | 機能                                                                                                                                                                                           |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ステップ                           | [一般] タブでは、このステップ アクションに従業員を 0 ステップ、1 ステップ、または 2 ステップ進める必要があるかどうかを指定します。                                                                                  |
|                                | **0 ステップ** - 従業員は、現在のステップの支払レートを受け取ります。                                                                                                                      |
|                                | **1 ステップ** - システムでは、従業員がすでにそのレベルの最後の基準点にあるかどうかが確認されます。                                                                                             |
|                                | **2 ステップ** - システムでは、従業員を現在のレベルで 2 ステップずつ進めます。 レベルの最後の基準点に達すると、システムは従業員を 1 ステップまたは 0 ステップだけ移動することができるかもしれません。 |

## <a name="run-the-compensation-process"></a>報酬プロセスの実行
プロセス イベントが必要な日付フィールド、プランおよびアクションで設定された後、**プロセス イベント**ページで**プロセスの実行**をクリックすることができます。 これを行うと、**報酬プロセス イベントの実行**ダイアログが開きます。 このダイアログで、**処理結果の表示**オプションをクリックすると、各従業員の報酬金額の計算方法を確認できます。 **OK** をクリックすると、選択した報酬プランのサイクル終了日のすべての従業員の報酬プロセスが実行されます。

## <a name="view-the-process-results"></a>プロセス結果の表示
プロセス結果を表示するには、**プロセス結果**ページを開きます。 新しい報酬イベントは、プロセス イベントが実行されるたびに作成されます。 このようにして試行を行い、調整を行い、および報酬イベントを複数回実行して、さまざまな変更が従業員の報酬にどのような影響を与えるかを確認することができます。

**プロセスの結果**ページには、実行された日時、プロセスを実行したユーザー、プロセスの実行時にエラーが発生したかどうかなどプロセスの実行に関する情報が含まれています。 **ロック済**オプションをマークして**報酬の読み込み**ボタンを無効にし、誰でも報酬イベントを従業員レコードに読み込まないようにすることもできます。 **従業員の結果**ボタンをクリックすると、実行に含まれる従業員の一覧が表示されます。

**従業員結果**オプションは、プロセス自体についての情報だけでなく、そのプロセスで実行されたすべての報酬アクションも表示します。 **固定報酬**セクションには、報酬プランのプロセス イベントに含まれる各アクションについてのレコードが含まれます。 **現在のガイドライン** および **推奨事項** 列には、 **固定報酬** セクションで選択したアクションに関する詳細情報が表示されます。 **報酬認定の有効化**がアクションに対してマークされている場合は、[認定] フィールドで編集できます。 これにより、従業員の金額を手動で調整することができます。 注記: プロセス イベントのアクションに**前回の結果を使用**とマークした場合は、依存アクションの金額を手動で更新する必要があります。

報酬金額が従業員のために見直され、および推奨値が調整されたら、**従業員イベント**で**ステータス**を変更してそのイベントが承認されているか無視されているかを示します。 オプションで、**再計算**ボタンをクリックし、従業員の推奨事項に対する変更を消去することができます。 これにより、既存の従業員イベントは [無視] というステータスでマークされ、再計算された値を持つ新しい従業員イベントが作成されます。

## <a name="loading-approved-compensation-changes"></a>承認済み報酬の変更を読み込む
1 つ以上の従業員イベントのステータスが [承認済み] に更新されると、従業員の固定報酬レコードを読み込むことができます。 これは、一度に 1 つずつ従業員イベントを選択し、**従業員の結果**ページで**従業員の報酬の読み込み**ボタンをクリックするか、または**プロセスの結果**ページで**報酬の読み込み**をクリックし、承認されたすべての従業員イベントを一度に読み込むことによって行うことができます。

**報酬の読み込み**ダイアログで **OK** をクリックすると、**従業員の固定報酬**ページにゼロ以外の報酬アクション行が追加されます。
