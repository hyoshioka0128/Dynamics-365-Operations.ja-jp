---
title: "ワークフロー要素"
description: "この記事は、ワークフローを構成するさまざまな要素について説明します。"
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ee20b567b402bf638a54f6394159f7f8a9f02da6
ms.lasthandoff: 03/31/2017


---

# <a name="workflow-elements"></a>ワークフロー要素

[!include[banner](../includes/banner.md)]


この記事は、ワークフローを構成するさまざまな要素について説明します。

ワークフローは "要素" から構成されます。 次のセクションでは、要素の各タイプについて説明します。

## <a name="tasks"></a>タスク
*タスク*とは、実行する必要のある作業単位です。 ワークフローに追加できるタスクには、手動タスクと自動化タスクの 2 種類があります。

### <a name="manual-task"></a>手動タスク

*手動タスク*は、ユーザーが実行する必要がある作業単位です。 たとえば、経費精算書ワークフローの手動タスクの場合、担当ユーザーは、次のアクションを完了する必要があります。

-   経費精算書と共に提出された領収書の確認。
-   従業員の管理者への電話。

### <a name="automated-task"></a>自動化タスク

*自動化タスク*は、システムが実行する必要がある作業単位です。 ユーザーの介在を必要としません。 たとえば、販売注文ワークフローには、システムが完了しなければならない次のような自動化タスクがあります。

-   与信チェックの実行。
-   顧客の顧客レコードの作成 (レコードがまだ存在しない場合)。

## <a name="approval-processes"></a>承認プロセス
*承認プロセス*は、複数のステップから構成されるプロセスです。 各承認ステップで、ユーザーは次の操作を行うことができます:

-   ドキュメントの承認。
-   ドキュメントの否認。
-   ドキュメントに対する変更依頼。
-   別のユーザーへの承認対象ドキュメントの割り当て。

## <a name="lineitem-workflow-elements"></a>行項目ワークフローの要素
ワークフローを作成して、ドキュメントやドキュメントの行項目を処理できます。 たとえば、タイムシートの承認ワークフローが作成済みであるとします。 (このワークフローを*ドキュメント ワークフロー*と呼びます。) そのドキュメント ワークフローには、*行項目 ワークフロー* 要素を追加できます。 行項目要素の実行時には、ドキュメントの各行項目が処理のために送信されます。 すべての行項目を同じ行項目ワークフローで処理することも、各行項目を異なる行項目ワークフローで処理することもできます。 従業員が、次の図のようなタイム シートを提出したとします。 ![行項目を含むワークフロー](./media/workflow_lineitemworkflow.gif) このシナリオでは、次の行項目ワークフローを作成する場合があります:

-   **行項目ワークフロー 1** – このワークフローは、プロジェクト ID が 1111 の行項目の処理に使用されます。
-   **行項目ワークフロー 2** – このワークフローは、プロジェクト ID が 2222 の行項目の処理に使用されます。
-   **行項目ワークフロー 3** – このワークフローは、プロジェクト ID が 3333 の行項目の処理に使用されます。

## <a name="flowcontrol-elements"></a>フロー制御要素
次の要素を使用すると、同時に実行される代替分岐または分岐があるワークフローを設計できます。

### <a name="manual-decision"></a>手動決定

*手動決定*は、ワークフローが 2 つの分岐に分かれるポイントです。 ユーザーが判断を行い、その判断によって、提出済のドキュメントをどちらの分岐で処理するかが決定されます。

### <a name="conditional-decision"></a>条件付き意思決定

*条件判断*も、ワークフローが 2 つの分岐に分かれるポイントです。 ただし、送信されたドキュメントを処理するのにどちらの分岐を使用するかはシステムが決定します。 この決定をするために、システムは文書を評価し、特定の条件を満たしているかどうかを判定します。

### <a name="parallel-activity"></a>並列活動

*並列活動*とは、同時に実行する 2 つ以上のワークフロー分岐を含むワークフロー要素です。

### <a name="subworkflow"></a>サブワークフロー

*サブワークフロー*は、他のワークフローのコンテキストで実行するワークフローです。



