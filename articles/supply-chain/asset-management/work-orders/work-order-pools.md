---
title: 作業指示書プール
description: このトピックでは資産管理でワーク オーダー プールを操作する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 161244cb4451ddc7b13b579fd02e828a61adeea4
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626365"
---
# <a name="work-order-pools"></a>作業指示書プール

[!include [banner](../../includes/banner.md)]


ワーク オーダー プールを使用して、共通点があるワーク オーダーをグループ化できます。 ワーク オーダー プールを作成できる要素の例を以下に示します。

- メンテナンス作業者 A またはメンテナンス作業者 B、などの作業者  

- 電気技師または配管工などの専門的なスキル  

- 物理的場所  

- 週またはその他の期間などのタイム スケジュール  

必要に応じて、1 つのワーク オーダーを複数のワーク オーダー プールに追加できます。


## <a name="create-a-work-order-pool"></a>ワーク オーダー プールの作成

**すべてのワーク オーダー プール**または**有効なワーク オーダー プール** リスト ページでは、ワーク オーダー プールの概要を取得し、新しいプールを作成できます。

1. **資産管理** > **共通** > **ワーク オーダー プール** > **すべてのワーク オーダー プール**または**有効なワーク オーダー プール**の順に選択します。

2. **新規** を選択します。

3. **プール** フィールドに、ワーク オーダー プールの ID を入力します。

4. **名前**フィールドに、名前を入力します。

5. **有効**オプションを**はい**に設定して、ワーク オーダー プールが有効であることを示します。

6. ワーク オーダーをワーク オーダー プールから自動的に削除する場合は、**ワーク オーダー リレーションの削除**オプションを**はい**に設定します。

7. **ライフサイクル状態の削除**フィールドで、ワーク オーダーのライフサイクル状態を選択します。 たとえば、ワーク オーダーを完了するためのワーク オーダー ライフサイクル状態は、ワーク オーダー プールへのリレーションを自動的に削除するように設定できます。

    ワーク オーダーをワーク オーダー プールにすぐに追加できます。

8. **ワーク オーダー** クイック タブの、**明細行の追加**を選択します。

9. **ワーク オーダー** フィールドで、ワーク オーダーを選択します。 関連フィールドは、自動的に更新されます。

10. 手順 8～9 を繰り返してワーク オーダーを追加します。

11. 追加したワーク オーダーを特定の順序で実行する必要がある場合は、**並べ替え順序**フィールドで、**1**、**2**、**3** などの番号を入力して、順序を指定できます。

12. ワーク オーダー プールに含まれるすべてのワーク オーダーの一覧を表示するには、**関連するワーク オーダー プールの表示**グループの、**ワーク オーダー プール** タブの、アクション ウィンドウで、**ワーク オーダー**を選択して、**すべてのワーク オーダー**一覧ページを開きます。

13. メンテナンス スケジュール、スケジュールされていないワーク オーダーおよびスケジュールされたワーク オーダーの最大能力負荷を計算および表示するには、**関連するワーク オーダー プールの表示**グループの、**ワーク オーダー プール** タブの、アクション ウィンドウで、**最大能力負荷**を選択して、**最大能力負荷の計算**ダイアログを開きます。

14. メンテナンス スケジュール、スケジュールされていないワーク オーダーおよびスケジュールされたワーク オーダーに関連する品目 (予備部品やその他必要な品目) の予測を計算および表示するには、**関連するワーク オーダー プールの表示**グループの、**ワーク オーダー プール** タブの、アクション ウィンドウで、**品目予測**を選択して、**品目予測の計算**ダイアログを開きます。

15. ワーク オーダー プールのワーク オーダーに関連する購買要求の一覧を表示するには、**調達**グループの、**ワーク オーダー プール** タブの、アクション ウィンドウで、**ワーク オーダー購買要求**を選択して、**ワーク オーダー購買要求**一覧ページを開きます。

16. ワーク オーダー プールのワーク オーダーに関連する発注書の一覧を表示するには、**調達**グループの、**ワーク オーダー プール** タブの、アクション ウィンドウで、**ワーク オーダー購買**を選択して、**ワーク オーダー購買**一覧ページを開きます。

>[!NOTE]
>作業計画がワーク オーダー プールに関連しなくなった場合は、**ワーク オーダー プール**ページのリスト ビューで、そのプールの**有効**オプションを、**いいえ**に設定します。

すべてのワーク オーダー明細行を削除するには、**ワーク オーダー リレーションの削除**オプションを**はい**に設定します。 このオプションは、後で他のワーク オーダーに使用できる空のプールを作成する場合などに役立ちます。 ワーク オーダー プールを使用して、後で新しいワーク オーダー リレーションを作成する場合は、**ワーク オーダー リレーションの削除**オプションを**いいえ**に設定する必要があります。

次の図は、**ワーク オーダー プール**の一覧ページの例を示しています。

![図 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a>ワーク オーダーをワーク オーダー プールに追加する

前のセクションで説明したように、プールを作成するときに、ワーク オーダーをワーク オーダー プールに追加できます。 **すべてのワーク オーダー**または**有効なワーク オーダー**一覧ページで、ワーク オーダーをワーク オーダー プールに追加することもできます。

1. ワーク オーダーを選択してから、アクション ウィンドウで**ワーク オーダー**タブ (**管理**グループ内) で、**ワーク オーダー プール**を選択します。

2. リストからワーク オーダーを選択し、**ワーク オーダー プール**をクリックします。

3. **ワーク オーダー プールの管理**ダイアログの、**追加/削除**フィールドで、**追加**を選択します。

4. **プール** フィールドで、ワーク オーダー プールを選択します。

5. **OK** を選択します。

6. ワーク オーダー プールに特定の順序で追加したワーク オーダーを追加するには、**すべてのワーク オーダー プール**または**有効なワーク オーダー プール**一覧ページで、そのプールを選択してから**編集**を選択します。 その後、**ワーク オーダー** クイック タブの**ワーク オーダー プール** ページで、**並べ替え順序**フィールドを試用して、プールに含まれるワーク オーダーの並べ替え順序を調整します。

ワーク オーダーをワーク オーダー プールから削除する場合は、これらの手順を繰り返して、手順 3 で**削除**を選択します。
