---
title: "リーン生産でのかんばん作業のスケジューリング"
description: "この記事は、かんばん作業のスケジューリングにおける視覚コントロールおよびさまざまな方法に関する情報を提供します。"
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 15 - 02 - 36
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 062cbbc8a4fd3b4dc738f24ee0606a3741736377
ms.lasthandoff: 03/29/2017


---

# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>リーン生産でのかんばん作業のスケジューリング

この記事は、かんばん作業のスケジューリングにおける視覚コントロールおよびさまざまな方法に関する情報を提供します。  

**かんばん作業のスケジューリング**ページでは、リーン生産の作業セルのスケジュールを視覚的にコントロールできます。 すべてのかんばん作業の概要が示されており、複数のフィルタ処理機能が用意されています。 このページから、かんばんコンフィギュレーションと実行に関連した他のすべてのページに移動できます。

## <a name="automatic-scheduling-of-kanban-jobs"></a>かんばん作業の自動スケジューリング
スケジューリングは、かんばんルールの**自動計画数量**パラメーターを設定することにより自動的に行われます。 **自動計画数量**を**1**に設定した場合、各かんばん作業は作成後すぐに計画されます。 結果は、一連の最初のプル、最初のサービス操作です。 **自動計画数量**に 1 を超える値をセットした場合、かんばん作業は計画前にグループ化されます。 このコンセプトにより、かんばんのサイズを実際の経済的なバッチサイズより低くすることができます。 たとえば、特定の品目 (または品目ファミリ) の経済的なバッチ サイズは 30 です。 製品数量を 30 にしてかんばんを作成する代わりに、かんばんルールを設定して製品数量を 10 にし、**自動計画数量**の値を**3**にすることができます。 3 つの予定外のジョブがある場合にのみ自動計画は、作業セルにかんばん作業をスケジュールしますが、スケジューリングをする人と作業現場の監督者には、2 つの予定外のジョブが実行待ちかもしれないことははっきりと分かります。 スケジューリングをする人やマネージャーは、手動でその作業をスケジュールするか、追加のかんばんを作成することでそれら 2 つの作業の生産を開始することができます。

## <a name="manual-scheduling"></a>手動のスケジューリング
手動のスケジューリングについては、Microsoft Dynamics AX 2012 では、かんばんスケジューリング ボードが導入されています。 手動スケジューリングは、自動スケジューリングと組み合わせることができます。 かんばんスケジューリング ボードでは、作業の計画や削除、順序の変更、または期間の変更などができます。 かんばんルールに基づく作業のうち、**自動計画**の値が **0** より大きい場合は、手動で計画の削除ができます。 ただし、これらの作業は、次の自動計画のイベントが発生したとき (つまり、新しいかんばんが作成されたとき) には変更されます。 次のオプションが手動スケジューリングで使用できます。

-   [**スケジュール**] 期日に従って、選択された作業がスケジュールされます。 (このオプションは自動計画に似ています)
-   [**日付から順方向でスケジュール**] 選択された作業を期日に従ってスケジュールしますが、指定された最も早い作業開始日を使用して結果を制御します。
-   [**バックワード**] 選択されたスケジュール作業順序を期間内でバックさせます。
-   [**フォワード**] 選択されたスケジュール作業順序を期間内で進めます。
-   [**前の期間**] 選択したスケジュール作業を前の期間の最初か最後に移動します。
-   [**次の期間**] 選択したスケジュール作業を次の期間の最初か最後に移動します。
-   [**計画**] &gt; [**ジョブ状態を元に戻す**] は、スケジュールされたジョブを取り消します。

## <a name="lean-scheduling-groups"></a>リーン スケジューリング グループ
各色は、リーン スケジューリング グループを表します。 リーン スケジューリング グループは、一般的なグループ、または 1 つの作業セルに属するグループとして自由に設定できます。 品目と分析コードはスケジューリング グループに自由に割り当てることができます。 たとえば、色付きのセルで、スケジュール グループは製品の色を表すことができます。 特定の工具が必要な作業には、品目は工具の要件によってグループ化できます。また、梱包の作業セルでは、梱包のテンプレートによって品目をグループ化できます。 リーン スケジューリング グループの色の使用はオプションで選択できますが、推奨されていません。 これにより、計画のステータスの可視性が向上します。 たとえば、どの色がどの日に製造されるかがすぐに分かり、その作業を最適化する方法が一目で分かります。

## <a name="work-cell-capacity-and-period-capacity"></a>作業セルの能力と期間能力
リーン作業セルの能力は常に並行な能力です。 つまり、複数のジョブを、作業セルで同時に有効にできます。 能力は、スループット モードと時刻モードで追跡できます。

### <a name="throughput"></a>スループット

作業セルの能力は、参照期間 (標準的な作業日、週、または月) の平均スループットの数量により定義されます。 1 日または週あたりの実際の能力は、作業セルに割り当てられたカレンダーの作業時間に基づいて計算されます。 ジョブによって読み込まれる能力は、作業セルの品目のスループットの割合によって調整されたジョブの数量です。

### <a name="hours"></a>時間

日または週単位に使用可能な能力は、作業セルに割り当てられたカレンダーによって定義されます。 ジョブによって読み込まれる能力は、数量 (デフォルトの活動数量対実際のジョブ数量) と作業セルの品目のスループットの割合によって調整された活動のサイクル時間です。

#### <a name="period-capacity-factbox"></a>期間能力情報ボックス

**かんばん作業スケジューリング** リスト ページには、選択した作業セルの使用可能な能力と予約された期間の能力を示す情報ボックスが含まれます。 生産フロー モデルの選択されたスケジュールの期間によって、期間の日数または週が表示されます。

<a name="see-also"></a>参照
--------

