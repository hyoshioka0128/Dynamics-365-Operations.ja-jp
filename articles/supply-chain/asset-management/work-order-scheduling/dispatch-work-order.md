---
title: 作業指示の派遣
description: このトピックでは、資産管理で作業指示を派遣する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 026b34934d6527416a4632d8e1aee76a8836dcb0
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652014"
---
# <a name="dispatch-work-order"></a>作業指示の派遣

[!include [banner](../../includes/banner.md)]

 

**派遣**機能を使用して、1 つの作業指示または作業指示ジョブを 1 人の作業者にスケジュールできます。

1. **資産管理** > **共通** > **作業指示書** > **すべての作業指示書**または**有効な作業指示書**の順にクリックします。

2. 一覧で作業指示を選択します。

3. **一般**タブで、**派遣**をクリックします。

4. **作業指示のスケジュール** ダイアログで、**作業者**フィールドの作業者を選択します。

5. **スケジュール時間**フィールドでは、予定勤務時間と予測時間とが異なる場合に、予定勤務時間を挿入できます。

6. **開始予定**フィールドでは、必要に応じて開始日時を編集できます。

7. スケジュール プロセスで、他のジョブで既にスケジュールされているリソースに関する能力制限を遵守する必要がある場合は、**資産**、**ツール**、および**作業者**の各トグルボタンが**はい**に設定されていることを確認してください。 スケジューリング プロセスに関する詳細情報を表示するには、**詳細**トグル ボタンで**はい**を選択します。 これは、作業指示について計算されたスコアに関する詳細情報が、情報ログに表示されることを意味します。

8. **スケジュールの無視**トグル ボタンで**はい**を選択して、カレンダーの休業日を無視します (資産、作業者、およびツールに適用)。 **実行予定の無視**トグル ボタンで**はい**を選択すると、スケジューリングに関連する作業指示で選択された可能性のある制限を無視できます。 

    実行予定の設定に関する情報については、[実行予定](../setup-for-work-orders/scheduled-execution.md) セクションを参照してください。

9. **OK**をクリックします。 作業指示書のライフサイクル状態は、**資産管理** > **設定** > **作業指示** > **ライフサイクル モデル**の順で指定された**スケジュール済**ライフサイクル状態に自動的に更新されます。

次の図は、**作業指示のスケジュール** ダイアログでの派遣選択の例を示します。

![図 1](media/04-work-order-scheduling.png)

[!NOTE]
作業指示のスケジュールを削除する場合は、**すべての作業指示**で作業指示を選択し、**一般**タブの**スケジュールの削除**をクリックします。スケジュールを削除した場合、作業指示ライフサイクル状態を手動で更新することを忘れないでください。
