---
title: 積荷テンプレート
description: このトピックでは、積荷テンプレートの設定方法と、新しい積荷に積荷テンプレートを関連付ける方法について説明します。
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1ea7f5244b483a1b9d6c55227c676a3878a71d83
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646408"
---
# <a name="load-templates"></a>積荷テンプレート

新しい積荷を作成する場合は、積荷テンプレートを割り当てることができます。 積荷テンプレートには、機器に関する情報、および積荷の高さ、幅、深さ、容積などの測定値に関する情報が含まれています。

このトピックでは、積荷テンプレートの設定方法と、新しい積荷に積荷テンプレートを関連付ける方法について説明します。

## <a name="set-up-a-load-template"></a>積荷テンプレートの設定

1. **輸送管理 \> 設定 \> 積荷構築 \> 積荷テンプレート** に移動します。
1. アクション ウィンドウで **新規** を選択し新しいテンプレートを追加するか、**編集** をクリックして既存のテンプレートを編集します。
1. 新規または既存のテンプレートの行で、次のフィールドを設定します。

    - **積荷テンプレート ID** – 積荷テンプレートの一意識別子 (ID) を入力します。
    - **設備** – 積荷の出荷に使用する設備を選択します。
    - **積荷の高さ**、**積荷の幅**、および **積荷の奥行き** – 積荷の寸法を入力します。
    - **最大積載容積** と **最大積載重量** – 積荷の最大積載容積と重量を入力します。
    - **最大積載総重量** ー 積荷の最大積載総重量を入力します。 積荷の総重量には、風袋重量と積載重量の両方が含まれます。
    - **貨物の最大個数** – 積荷に含めることができる貨物の最大個数を入力します。
    - **貨物を床積みにする** – 床積みを使用するには、このチェックボックスをオンにします。 床積みのシナリオでは、ボックスをコンテナー内に床から天井まで床一面に積み重ねて、収容能力を最大限にします。

1. アクション ウィンドウで、**保存** を選択します。

## <a name="associate-a-load-template-with-a-new-load"></a>新しい積荷に積荷テンプレートを関連付け

1. **配送管理 \> 計画 \> 積荷計画ワークベンチ** の順に移動します。
1. ページの上部で、積荷を作成するソース ドキュメントのタイプに応じて、**出荷**、**販売明細行**、**移動明細行**、または **購買注文明細行** のタブのいずれかを選択します。 
1. 積荷を計画する特定のドキュメントを選択します。
1. アクション ウィンドウの、**供給と需要** タブの **追加** グループで、**新しい積荷へ** を選択します。
1. **積荷テンプレートの割り当て** ダイアログ ボックスの、**積荷テンプレート ID** フィールドで、適用するテンプレートを選択します。
1. テンプレートを適用するには、**OK** を選択します。