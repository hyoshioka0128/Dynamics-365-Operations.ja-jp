---
title: 業務プロセスの形式化
description: このトピックでは、業務プロセス機能を使用して、組織内で完了する必要のあるプロセス用の業務プロセス テンプレートを作成する方法を説明します。
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.openlocfilehash: 85950a1413cfd8745bb78a52eb9f7c81b8976605
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518449"
---
# <a name="formalize-business-processes"></a>業務プロセスの形式化

[!include[banner](includes/banner.md)]

業務プロセス機能を使用すると、組織内で完了する必要のある業務プロセス用の業務プロセス テンプレートを作成できます。 たとえば、会社が毎年人事管理 (HR) 監査を完了するとします。 この場合、監査プロセスを構成するすべてのタスクを追跡するテンプレートを作成することができます。 このテンプレートにより、監査が行われるたびにすべてのタスクが行われたことを保証できます。 また、タスクが特定の順序で行われる必要がある場合、テンプレートにより、それらが正しい順序で行われたことも保証できます。

テンプレートは、定期的なプロセスに再利用できます。 コピーしたものに基づいて新しいテンプレートを作成することもできます。

業務プロセス テンプレートを作成した後、業務プロセスは、**業務プロセス** ワークスペースで開始および追跡することができます。 業務プロセスが開始されると、タスクは適切な人物に割り当てられ、期日が含められます。

## <a name="business-process-templates"></a>業務プロセス テンプレート
業務プロセス テンプレートは、業務プロセスを構成するタスクのグループを一覧表示します。 既定では、HR マネージャーおよびアシスタントがビジネス プロセスを作成できます。 ただし、セキュリティ コンフィギュレーションの**一般的な業務プロセスのメンテナンス**業務を変更することにより、業務プロセスを作成できるロールを変更できます。

各業務プロセスに対して、プロセスの所有者を定義できます。 プロセス所有者は、プロセスのすべてのタスクへの可視性があり、タスクの再割り当てや期日の変更を行うことができます。 たとえば、HR 取締役が、給付金確認用の業務プロセス テンプレートを作成し、プロセスの所有者として、報酬と給付金マネージャーを指定するとします。 これにより、報酬と給付金マネージャーには、確認の一部として完了する必要があるタスクへの可視性があります。

プロセスの所有者は、新しい業務プロセスまたは業務プロセス テンプレートを作成したり、有効な業務プロセスまたは業務プロセス テンプレートを削除することはできません。

## <a name="tasks"></a>仕事
多くの場合、業務プロセスは、複数のタスクで構成されます。 内部コースの案内の確認など、Microsoft Dynamics 365 for Talent[?] でいくつかのタスクを完了することができます。 この場合、**タスク リンク** フィールドでオプションが選択されます。 他のタスクには、Web サイト上のページのレビューやページの完了が含まれることがあります。 この場合、**タスク リンク** フィールドで **URL** が選択され、それから Web アドレスを入力することができます。 外部サイトと内部サイトの両方の URL を入力できます。 すべての構造のアクセシビリティの確認など、手動で完了する活動のタスクを作成することもできます。 この場合、タスク リンクは必要ではありません。 この柔軟性により、複数の種類のタスクを包括的なプロセスで追跡できます。

タスクは、特定の作業者または職位のいずれかに割り当てることができます。 たとえば、保険料の確認を行うのは常に報酬と給付金マネージャーです。 したがって、このタスクを作成するときは、**割り当てタイプ**の**職位**を選択し、**職位**の一覧から**報酬と給付金マネージャー**を選択します。 業務プロセスが開始されると、タスクは、**報酬と給付金マネージャー**の職位にある作業者に割り当てられます。 特定の作業者にタスクを割り当てるには、**割り当てタイプ** フィールドで**作業者**を選択し、適切な人を選択します。

タスクの期日は、業務プロセスの開始時に入力された目標期日によって異なります。 目標期日より前に完了しなければならないタスクがありますが、他のタスクは目標期日の後に完了できる場合あります。 **目標期日からの期日のオフセット** フィールドのタスクを定義するときは、目標期日を基準とする期日を指定します。 たとえば、HR 監査が完了する 10 日前に、報酬と給付金マネージャーが保険料のレビューを行わなければならないとします。 この場合、確認用に作成されるタスクの**目標期日からの期日のオフセット**の値は **-10** となります。 したがって、業務プロセスが 5 月 13 日に開始された場合、タスクの期日は 5 月 3 日になります。

> [!NOTE]
> 期日は、業務プロセスが開始された後にも調整できます。

複雑なタスクには、複数のステップが必要な場合や、タスクを実行する人が追加情報を提供する必要のある場合があります。 これらのシナリオについては、タスクに指示を追加できます。 手順は、タスクを完了するように割り当てられた担当者に、そのタスクを完了する方法に関する追加情報を提供できます。 指示にリッチ テキスト形式を組み込むこともできます。

## <a name="starting-a-business-process"></a>業務プロセスの開始
業務プロセス テンプレートにおいて、**プロセス開始**を選択することによって、業務プロセスが開始されます。 プロセスが開始されると、選択された作業者、またはテンプレートに含まれるタスクで定義された職位にタスクが作成されます。 「タスク」内で説明されているように、期日は目標期日からオフセットの日数を加算または減算することにより、各タスクにも割り当てられます。 有効な業務プロセスは、**業務プロセス** ワークスペースで確認できます。

## <a name="employee-self-service"></a>従業員セルフサービス
従業員にタスクが割り当てられた後、その従業員は**従業員セルフ サービス** ページ上で、そのタスクおよびその他の割り当てられたタスクを確認できます。 割り当てられた各業務プロセス タスクについて、従業員はその名前、タスクの説明、完了するための指示、および連絡担当者を参照できます。 **従業員セルフ サービス**ページから、従業員は Microsoft Dynamics 365 内の関連付けられたページまたは関連付けられた Web ページを開くこともでき、タスクを進行中、キャンセル済、または完了としてマークすることもできます。

## <a name="business-process-workspace"></a>業務プロセス ワークスぺース
人事担当者は、**業務プロセス** ワークスペースで有効な業務プロセスを表示できます。 このワークスペースには、すべての有効なプロセスと、それぞれに関連付けられているタスクが一覧表示されます。 包括的なタスクの一覧を、期日でフィルター処理できます ワークスペースには、期限超過のタスク、および人事担当者向けに特別に割り当てられたタスクも一覧表示されています。 人事担当者はすべてのタスクのステータスを更新することもでき、必要に応じてタスクを再割り当てして、全体的な業務プロセスを続行させることができます。

## <a name="my-business-processes-workspace"></a>個人用業務プロセス ワークスぺース
プロセスの所有者は、**個人用業務プロセス** ワークスぺースにおいて割り当てられている有効な業務プロセスを表示できます。 このワークスペースには、そのユーザーが所有するすべての有効なプロセス、および関連するタスクが一覧表示されます。 包括的なタスクの一覧を、期日でフィルター処理できます ワークスペースには、プロセスの所有者に特別に割り当てられたタスクも一覧表示されています。 プロセスの所有者は、すべてのタスクのステータスを更新したり、すべてのタスクの再割り当てをすることもできます。

## <a name="navigating-business-processes"></a>業務プロセスに移動
業務プロセス テンプレートを作成またはコピーするため、また業務プロセスを開始するため、業務プロセス - リンク - 業務プロセス管理に移動します。 実行できるアクションは次のとおりです。

- **新規**を選択して、新しい業務プロセス テンプレートを作成します。
- **テンプレートからコピー**を選択して、選択したテンプレートを新しいテンプレートにコピーします。
- **プロセスの開始**を選択して、選択した業務プロセスを開始し、タスクを割り当て、期日を計算します。

有効なプロセスおよび関連するタスクを表示するには、**業務プロセス** ワークスペースを開きます。

