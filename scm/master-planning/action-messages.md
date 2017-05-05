---
title: "記載されていない"
description: "アクション メッセージは、既存の計画オーダーまたは確定オーダーの変更についてシステムで生成される提案です。"
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 21 - 54
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f2ac69ddf485139b057dafa20e5f1a961fc32067
ms.lasthandoff: 03/29/2017


---

# <a name="undocumented"></a>記載されていない

アクション メッセージは、既存の計画オーダーまたは確定オーダーの変更についてシステムで生成される提案です。

### <a name="introduction"></a>はじめに

マスター プランの計算によって、要件の変更に応じたアクション メッセージが生成されます。 たとえば、出荷日または数量が、すでに要求を満たす発注書を作成した販売注文で変更される場合があります。 この場合、発注書を更新するために、1 つまたは複数のアクション メッセージがマスター プランの計算によって生成されます。 提示される変更を行うかどうかを選択します。

品目に関連付ける補充グループに対しアクション メッセージが計算される方法を設定できます。

 <a name="selecting-action-messages"></a>アクション メッセージの選択
==========================

**補充グループ** ページで、システムが生成するアクション メッセージ、およびメッセージが適用される品目または補充グループを選択できます。 次のアクション メッセージを選択できます。

| メッセージ             | 説明                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **繰り上げ**         | このメッセージを選択した場合は、以前の日付に注文を移動する必要があるときに、システムによってアクション メッセージが生成されます。 [**要求日前受入許容日数**] フィールドで、入庫から出庫までの最大日数 (前金アクションなし) を指定することもできます。 |
| **延期**        | このメッセージを選択した場合は、後の日付に注文を移動する必要があるときに、システムによってアクション メッセージが生成されます。 [**延期日数**] フィールドで、入庫から出庫までの最大日数 (延期金アクションなし) を指定することができます。       |
| **減少**        | このメッセージを選択した場合は、製造オーダー、発注書、およびそのほかの受入トランザクションが、過剰な在庫レベルを防ぐために差し引かれる必要があります。                                                                                                   |
| **増加**        | このメッセージを選択した場合は、製造オーダー、発注書、およびそのほかの受入トランザクションが、在庫不足を防ぐために増加される必要があります。                                                                                                    |
| **派生アクション** | このメッセージを選択した場合は、生産を満たすコンポーネントの注文に対するアクションなど派生要件に対して、アクション メッセージが作成されます。                                                                                                   |



