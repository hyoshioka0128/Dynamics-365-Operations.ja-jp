---
title: ワーク オーダーのライフサイクル状態
description: このトピックでは、資産管理におけるワーク オーダーのライフサイクル状態について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f531f51d7f42f88e4da2d046e61313e9ada2b259
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569803"
---
# <a name="work-order-lifecycle-states"></a>ワーク オーダーのライフサイクル状態


[!include [banner](../../includes/banner.md)]

 

ワーク オーダーのライフサイクル状態によって、ワーク オーダーを実行できる状態が定義されます。 例には、**作成済**、**スケジュール済**、**処理中**および**終了済**が含まれます。 ワーク オーダーのライフサイクル状態は、ワーク オーダーで手動で更新することも、自動で更新することもできます (たとえば、ワーク オーダーのスケジューリング中など)。

ワーク オーダーに必要なワーク オーダーのライフサイクル状態は、**プロジェクト管理および会計パラメーター** ページで一致するプロジェクト ステージに関連付ける必要があります (**プロジェクト管理および会計** \> **プロジェクト管理および会計パラメーター**)。 最初に、プロジェクト管理および会計にプロジェクト ステージを設定します。 次に、資産管理に、ワーク オーダーのライフサイクル状態とワーク オーダーのライフサイクル モデルを設定します。

次のテーブルは、**ワーク オーダーのライフスタイル状態**ページの**一般**クイック タブの **ワーク オーダー**および**スケジュール** セクションのオプションについて説明しています (**資産管理** \> **設定** \> **ワーク オーダー** \> **ライフスタイル状態**)。

![ワーク オーダーのライフサイクルの状態ページ](media/09-setup-for-work-orders.png)

| オプションの名前                   | 説明 |
|-------------------------------|-------------|
| 使用可能                        | このライフサイクル状態にあるときにワーク オーダーを有効にする必要がある場合は、このオプションを**はい**に設定します。 |
| 行の追加                      | このライフサイクル状態のワーク オーダーにワーク オーダー ジョブを追加できる場合は、このオプションを**はい**に設定します。 |
| 消去                        | このライフサイクル状態にあるときにワーク オーダーを削除できる場合は、このオプションを**はい**に設定します。 |
| 行の削除                   | このライフサイクル状態のワーク オーダーからワーク オーダー ジョブを削除できる場合は、このオプションを**はい**に設定します。 |
| スケジューリングを許可              | このライフサイクル状態にあるときにワーク オーダーをスケジュールできる場合は、このオプションを**はい**に設定します。 |
| 実際の開始の設定              | このライフサイクル状態に更新されたときに、ワーク オーダーの実際の開始日時を選択するようにユーザーに求める場合は、このオプションを**はい**に設定します。 |
| 実際の終了の設定                | このライフサイクル状態に更新されたときに、ワーク オーダーの実際の終了日時を選択するようにユーザーに求める場合は、このオプションを**はい**に設定します。 |
| 仕訳帳の転記                 | ワーク オーダーがこのライフサイクル状態に更新されたときに、ワーク オーダー仕訳帳が自動的に転記される場合は、このオプションを**はい**に設定します。 仕訳帳の転記中にエラーが発生した場合は、メッセージが表示され、ワーク オーダーのライフサイクル状態の更新はキャンセルされます。 ワーク オーダーの仕訳帳明細行を表示するには、**資産管理**\>**共通**\>**ワーク オーダ**\>**すべてのワーク オーダー**、**有効なワーク オーダー**、または**自分の有効なワーク オーダー**を選択し、リストにあるワーク オーダーから選択し、**仕訳帳**を選択します。 特定のライフスタイル状態での自動ワーク オーダー仕訳帳転記のこの設定は、**ワーク オーダー仕訳帳**ページで**仕訳帳の転記**を選択した場合と同じです。<p>**注記 :** このオプションを**はい**に設定すると、承認ワークフローが設定されていない場合、仕訳帳は自動的に転記されます。 会社が**仕訳帳の承認**ページでコンフィギュレーションされている仕訳帳承認設定を使用している場合、(**プロジェクト管理および会計** \> **設定** \> **仕訳帳** \> **仕訳帳承認**) マネージャーまたは担当者は、消費登録を検証し転記する必要があります。</p> |
| メンテナンス チェックリストの処理 | ワーク オーダーがこのライフサイクル状態に更新されたときに、添付されているメンテナンス チェックリストを処理する必要がある場合は、このオプションを**はい**に設定します。 この処理の一部として、メンテナンス チェックリストで行われたすべてのカウンター登録が転記され、メンテナンス チェックリスト全体の結果が評価されます。 **合格**と**不合格**の結果を持つメンテナンス チェックリストの明細行が評価され、少なくとも 1 つの明細行が**失敗**した場合、資産管理でメンテナンス チェックリスト全体が「失敗」 としてマークされます。 |
| 準備完了                         | ワーク オーダーがこのライフサイクル状態に更新されたときに、ワーク オーダーで作成されたすべてのワーク オーダー ジョブのワーク オーダー ジョブのスケジュール状態が自動的に**準備完了**に更新される場合、このオプションを**はい**に設定します。 |
| 開始                         | ワーク オーダーがこのライフサイクル状態に更新されたときに、ワーク オーダーで作成されたすべてのワーク オーダー ジョブのワーク オーダー ジョブのスケジュール状態が自動的に**開始済**に更新される場合、このオプションを**はい**に設定します。 |
| 終了                           | ワーク オーダーがこのライフサイクル状態に更新されたときに、ワーク オーダーで作成されたすべてのワーク オーダー ジョブのワーク オーダー ジョブのスケジュール状態が自動的に**終了済**に更新される場合、このオプションを**はい**に設定します。 |
| スケジュール行を削除         | ワーク オーダーがこのライフサイクル状態に更新されたときに、既にスケジュールされているワーク オーダーで作成されたすべてのワーク オーダー ジョブのスケジュールを削除する場合は、このオプションを**はい**に設定します。 つまり、資産、関連する管理作業者、および関連するツールの確保済能力は削除されます。 たとえば、**見積済**という名前のワーク オーダーのライフサイクル状態で、このオプションを**はい**に設定します。 その後、再スケジューリングが必要なためにワーク オーダーがこのライフサイクル状態にロールバックされると、そのワーク オーダーでスケジュールを削除できるようになります。 |

## <a name="set-up-project-stages-and-work-order-lifecycle-states"></a>プロジェクト ステージとワーク オーダーのライフサイクル状態の設定

1. **プロジェクト管理と会計** \> **設定** \> **プロジェクト管理および会計パラメーター**の順に選択します。
2. **プロジェクト ステージ** タブで、使用するステージごとに、ワーク オーダーに必要なすべてのプロジェクト タイプのチェック ボックスをオンにします。 プロジェクト タイプは、許可される財務タスクに関するルールを定義します。 財務タスクの例としては、予測の作成、見積の作成、期首残高の作成などがあります。

    > [!IMPORTANT]
    > プロジェクト タイプにプロジェクト ステージが選択されておらず、プロジェクト ステージがワーク オーダーのライフサイクル状態に使用されている場合、ワーク オーダー プロジェクトは適切な方法で更新されません。

3. **プロジェクト管理および会計パラメーター** ページを閉じます。
4. **資産管理** \> **設定** \> **ワーク オーダー** \> **ライフサイクル状態**を選択します。
5. **新規**を選択して、新しいワーク オーダー ライフサイクル状態を作成します。
6. **ライフサイクルの状態**フィールドに、ライフサイクルの状態 ID を入力します。
7. **名前**フィールドに、名前を入力します。

    **詳細**クイック タブで、**ライフサイクル モデル** フィールドには、このライフサイクルの状態を使用するワーク オーダーのライフサイクル モデルの数が表示されます。

8. **一般** クイックタブの**ワーク オーダー** セクションで、関連するオプションを**はい**に設定して、このライフサイクル状態で使用できる機能を選択します。 オプションについては、このトピックの前の部分で示したテーブルを参照してください。
9. **プロジェクト** セクションの**ステージ** フィールドで、このライフサイクル状態に関連付ける必要があるプロジェクト ステージを選択します。
10. **プロジェクト** セクションで、ワーク オーダーがこのライフスタイル状態にあるときに各ワーク オーダー ジョブに関連するプロジェクト活動を自動的に終了する必要がある場合、**活動を終了する**のオプションを**はい**に設定します。

    > [!NOTE]
    > ワーク オーダー ジョブに関連するプロジェクト活動の数を確認するには、**資産管理**\>**共通**\>**ワーク オーダー**\>**すべてのワーク オーダー**、**有効なワーク オーダー**、または**自分の有効なワーク オーダー**の順に選択します。 ワーク オーダーを開き、次に、ワーク オーダー ジョブを選択します。 活動番号は、**明細行の詳細**クイック タブの**一般**タブの**プロジェクト** セクションの**活動番号**フィールドに表示されます。

11. ワーク オーダーがこのライフサイクル状態にあるときに、ワーク オーダー プロジェクト予測をワーク オーダー仕訳帳に自動的にコピーする必要がある場合、**予測**セクションで、**時間予測のコピー**、**品目予測のコピー**、および/または**経費予測のコピー** オプションを**はい**に設定します。
12. **スケジュール** セクションで、ワーク オーダーがこのライフスタイル状態にあるときにワーク オーダー ジョブのスケジュール状態を更新する必要のある場合、オプションの 1 つを**はい**に設定します。 **準備完了**、**開始**、**終了**、および**スケジュール明細行の削除**オプションについては、このトピックの前の部分で示したテーブルを参照してください。

    > [!NOTE]
    > ワーク オーダー ジョブに関連するスケジュール明細行を表示するには、**資産管理**\>**共通**\>**ワーク オーダー**\>**すべてのワーク オーダー**、**有効なワーク オーダー**、または**自分の有効なワーク オーダー**の順に選択します。 ワーク オーダーを開き、**ワーク オーダー ジョブ** クイック タブでワーク オーダー ジョブを選択し、**明細行詳細**クイック タブで関連情報を表示します。 **スケジュール** タブの**状態**フィールドには、ワーク オーダー ジョブの状態が表示されます。 **状態**フィールドには、**スケジュール済**、**準備完了**、**"開始済**、**停止**、**終了済**のいずれかの値を設定できます。

13. **メンテナンス要求**セクション、**ライフサイクル状態**フィールドで、関連するメンテナンス要求の更新先となるメンテナンス要求のライフサイクル状態を選択します。 この更新は自動的に行われます。 これは、メンテナンス要求のライフサイクル状態が、メンテナンス要求に使用されるメンテナンス要求ライフサイクル モデルで選択されている場合にのみ実行できます。
14. ワークオーダーがこのライフスタイル状態に更新されたときに、ワークオーダーで使用されるすべての品目が **資産 BOM** ページで自動的に更新される場合、**資産**セクションで、**資産 BOM の更新**オプションを**はい**に設定します。 この設定は、たとえば、ワーク オーダーのライフサイクル状態が、完了または終了済としてワーク オーダーを定義している場合に関連します。
15. このライフスタイル状態にあるワーク オーダーを、ワーク オーダー プールから自動的に削除する場合は、**ワーク オーダー プール** セクションで、**プール参照を削除**オプションを**はい**に設定します。
16. **検証**クイック タブで、関連するオプションを **"はい"** に設定して、このライフサイクル状態で有効化する検証タイプを選択します。 次に、選択した各検証タイプの**タイプ** フィールドで、検証タイプに関連する必須フィールドが検証されていない場合に表示するメッセージのタイプを選択します。 **エラー**を選択した場合、関連する必須フィールドがワーク オーダーで更新されるまで、ワーク オーダーのライフサイクル状態の更新はキャンセルされます。

    - **メンテナンス ダウンタイム**、**メンテナンス チェックリスト**、**エラー現象**、**エラー原因**、および**エラーの救済**オプションは、**ワーク オーダー タイプ** ページの**必須**セクションのオプションに関連しています (**資産管理** \> **設定** \> **ワーク オーダー** \> **ワーク オーダー タイプ**)。 これらの検証を有効にするには、ワーク オーダーに使用されるワーク オーダー タイプで、関連するオプションを**はい**に設定する必要があります。
    - ワーク オーダーが更新されるライフサイクル状態で、**メンテナンス チェックリスト** オプションが**はい**に設定されている場合、**必須**とマークされているメンテナンス チェックリストの明細行が、**チェック済**または**該当なし**として登録されているかを検証します。 これらの登録がどちらも必須明細行で行われていない場合、ワーク オーダーがこのライフサイクル状態に更新されるときに、情報、エラー、警告のいずれかのメッセージが表示されます。
    - ワーク オーダーが更新されるライフサイクル状態で**確定済み費用**オプションが**はい**に設定されている場合、確定済み費用の合計金額 (つまり、法人が支払を確定した経費の合計金額) が各ワーク オーダー ジョブに対して計算されます。 確定済み費用金額が 0 (ゼロ) より大きい場合は、メッセージが表示されます。 **プロジェクト管理および会計パラメーター** ページの**原価管理**タブで**費用の確定**クイック タブに含まれる費用の確定タイプを選択します (**プロジェクト管理および会計** \> **設定** \> **プロジェクト管理および会計パラメーター**)。
    - ワーク オーダーが更新されるライフサイクル状態で、**メンテナンス ダウンタイム** オプションが**はい**に設定されている場合、ワーク オーダーに関連する資産でメンテナンス ダウンタイムの検証が行われます。 メンテナンス ダウンタイム登録がされても、**終了済**の登録がない場合、ワーク オーダーがこのライフスタイル状態に更新されるときにメッセージが表示されます。
    - 標準プロジェクト設定に、資産管理設定に必要なすべてのステージが含まれていない場合は、**プロジェクト管理および会計パラメーター** ページの**プロジェクト ステージ** タブでユーザー定義のプロジェクト ステージを設定できます。 次の図は、**プロジェクト管理および会計パラメーター** ページの**プロジェクト ステージ**のタブを示しています。

    ![各種プロジェクト タイプ ページのプロジェクト ステージを設定します](media/10-setup-for-work-orders.png)

> [!NOTE]
> ワーク オーダーを更新するライフサイクル状態が無効な場合、そのワーク オーダーに関連付けられているがまだ転記されていない仕訳帳は自動的に削除されます。 この動作は、未使用データの自動クリーンアップを保証するのに役立ちます。 (ライフサイクル状態は、**ワーク オーダーのライフスタイル状態**ページの**一般**クイック タブで**有効化**オプションが**いいえ**に設定されている場合は無効です。)
>
> ただし、ワーク オーダーを無効にするように設定した場合、そのワーク オーダーに関連付けられているがまだ転記されていない仕訳帳は自動的に削除**されません**。 (手動でワーク オーダーを無効にするには、**資産管理**\>**共通**\>**ワーク オーダー**\>**すべてのワーク オーダー**または**有効なワーク オーダー**の順に選択します。 ワーク オーダーを開き、**ヘッダー** ビューに切り替えます。 **一般**クイック タブで**編集**を選択し、**有効**オプションを**いいえ**に設定します。)

## <a name="relations-among-work-order-lifecycle-models-work-order-types-and-work-order-lifecycle-states"></a>ワーク オーダーのライフサイクル モデル、ワーク オーダー タイプ、およびワーク オーダーのライフサイクル状態間の関係

ライフサイクル モデルはワークフローを参照し、ライフサイクル状態は、ライフサイクル モデルで順番に選択されます。 ライフサイクル モデルは、ワーク オーダー タイプで設定されます。 ワーク オーダー タイプは、ワークフローおよび作業プロセスのサイズまたは範囲を決定します。 たとえば、**メンテナンス**は標準のワーク オーダー タイプであり、多くのライフサイクル状態を持つワーク オーダーのライフサイクル モデルに関連している場合があります。 これに対して、**修正**ワーク オーダー タイプは、スケジュールされていないワーク オーダーまたは緊急の状況によりワーク オーダーが作成される前にジョブが完了したワーク オーダーに使用される場合があります。 このワーク オーダー タイプは、数個のライフサイクル状態しかないワーク オーダー ライフサイクル モデルに関連している場合があります。

タイプを使用する理由は、タイプがワーク オーダーまたは資産などで定義されている場合に、関連する作業プロセス (ライフサイクル状態) が自動的に定義されるためです。 ワーク オーダー タイプの設定方法の詳細については、[ワーク オーダー タイプ](../setup-for-work-orders/work-order-types.md)参照してください。

> [!NOTE]
> ライフサイクル状態、ライフサイクル モデル、およびタイプは、ワーク オーダーに加えて、機能上の場所、資産、およびメンテナンス要求に適用されます。

次の図は、ワーク オーダー タイプ、ライフサイクル モデル、およびライフサイクル状態の関係を示しています。

![ワーク オーダー タイプ ページとワーク オーダー ライフサイクル モデル ページの比較](media/11-setup-for-work-orders.png)

## <a name="work-order-lifecycle-models"></a>作業指示書ライフサイクル モデル

ワーク オーダーに必要なワーク オーダー ライフサイクル状態を作成したら、ワーク オーダー ライフサイクル モデルに分割できます。 少なくとも、1 つの標準ライフサイクル モデルを作成する必要があります。

1. **資産管理** \> **設定** \> **ワーク オーダー** \> **ライフサイクル モデル**を選択します。
2. **新規**を選択して、新しいワーク オーダー ライフサイクル モデルを作成します。
3. **ライフサイクル モデル**フィールドに、ライフサイクル モデルの ID を入力します。
4. **名前**フィールドに、名前を入力します。

    **詳細**クイック タブで、**ライフサイクルの状態**フィールドには、ライフサイクル モデルで選択されているライフサイクルの状態の数が表示されます。 **ワーク オーダー タイプ**のフィールドには、ライフサイクル モデルを使用するワーク オーダー タイプの数が表示されます。

5. **ライフサイクルの状態**クイック タブで、ライフサイクル モデルに含める必要があるライフサイクル状態を選択します。

    - ライフサイクル モデルにライフサイクルの状態を含めるには、**残りのライフサイクル状態**セクションでそれを選択し、右矢印ボタン![右矢印](media/12-setup-for-work-orders.png) を選択して**選択されたライフサイクルの状態**セクションに移動します。
    - ライフサイクル モデルに使用可能なすべてのライフサイクルの状態を含めるには、**使用可能なすべてのステージを選択**ボタン![使用可能なすべてのステージを選択](media/13-setup-for-work-orders.png)を選択します。 すべてのライフサイクルの状態は、**選択されたライフサイクルの状態**セクションに移動されます。
    - ライフサイクル モデルからライフサイクルの状態を削除するには、**選択されたライフサイクルの状態**セクションでそれを選択し、左矢印ボタン![左矢印](media/14-setup-for-work-orders.png) を選択して**残りのライフサイクルの状態**セクションに移動します。

6. **ライフサイクル状態の更新プログラム**を選択して、選択したライフサイクル状態に従うことができるライフサイクル状態を定義します。
7. **更新** クイックタブの**スケジュールされた状態**フィールドで、ワーク オーダーの以前のライフサイクル状態に関係なく、ワーク オーダーのスケジューリングを完了したワーク オーダーに対して常に選択されるライフサイクル状態を選択します。
8. **未スケジュールのライフサイクル状態**フィールドで、ワーク オーダーのスケジューリングが削除された場合に、ワーク オーダーに対して常に選択されるライフサイクル状態を選択します。
9. ワーク オーダー ライフサイクル モデルを保存します。

![ワーク オーダー ライフサイクル モデル ページ](media/15-setup-for-work-orders.png)