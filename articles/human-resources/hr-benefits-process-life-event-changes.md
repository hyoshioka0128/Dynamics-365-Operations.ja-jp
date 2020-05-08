---
title: ライフ イベントの変更を処理
description: ライフ イベント変更における Microsoft Dynamics 365 Human Resourcesのライフ イベント 変更の処理を行います。
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae1aa74c7e463cd0d8c8d740394b998030c8498f
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229996"
---
# <a name="process-life-event-changes"></a>ライフ イベントの変更を処理

2 つのライフ イベント変更における Microsoft Dynamics 365 Human Resourcesのライフ イベント 変更の処理:

- 誕生日の変更
- 適格性ルールにより、有効期限の変更をオーバーライドする 

1. **給付金管理**ワークスペースにて、**処理**の下の**ライフ イベントの変更処理**を選択します。

2. **ライフ イベントの変更処理を実行**ダイアログ ボックスで、次のフィールドの値を指定します。

   | フィールド | 説明 |
   | --- | --- |
   | 登録期間 | ライフ イベントを処理する登録期間が変更されます。 |
   | 法人エンティティ | ライフ イベントを処理する法人が変更されます。 |

3. バックグラウンドで処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。

   1. 処理情報を入力します。

   2. 定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。

   3. ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。

   4. **OK** を選択します。 設定したパラメータで処理が実行されます。

4. **OK** を選択します。