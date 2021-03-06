---
title: RFQ を使用する要求の作成
description: このガイドでは、価格および仕入先情報を RFQ プロセスから購買要求へ追加する方法を示します。
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d80f84c148ff26bf008a97b06098bfd18c9062d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844157"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>RFQ を使用する要求の作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

このガイドでは、価格および仕入先情報を RFQ プロセスから購買要求へ追加する方法を示します。 このガイドで表示される例は USMF のデモ データ会社で使用でき、すべての手順を完了するためには管理者としてログインする必要があります。 このガイドのタスクは、調達担当者によって通常実行されます。


## <a name="create-a-requisition"></a>要求の作成
1. [調達] > [購買要求] > [自分自身が作成した購買要求] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [要求日] フィールドに日付を入力します。
5. [会計日] フィールドに日付を入力します。
6. [OK] をクリックします。
7. [理由] フィールドで、値を入力または選択します。
8. [明細行の追加] をクリックします。
9. [調達カテゴリー] フィールドで、ツリーのカテゴリーを選択し、[OK] をクリックします。
10. [製品名] フィールドに値を入力します。
11. [数量] フィールドに数値を入力します。
12. [単位] フィールドで、値を入力または選択します。
13. [保存] をクリックします。
14. [ワークフロー] をクリックすると、ドロップ ダイアログを開きます。
15. [送信] をクリックします。
16. ページを閉じます。
17. [送信] をクリックします。

## <a name="reassign-a-workflow-task"></a>ワークフロー タスクの再割り当て
    * 次のタスクは、RFQ を作成し、製品の仕入先から入札を取得します。 USMF のデモ データでは、要求ワークフローとルールが共に設定されているため、仕入先が選択されていない場合、または単価が明細行に対して 0 の場合でも、RFQ を作成する特定の作業者にタスクが割り当てられます。 このガイドで続行するには、別のユーザー (自分自身) にそのタスクを再度割り当てる必要があります。 自分が管理者としてログインしている場合にのみこれを行うことができます。  
1. [ワークフロー] をクリックすると、ドロップ ダイアログを開きます。
2. [履歴の表示] をクリックします。
3. ページを更新します。
4. [追跡の詳細] セクションを展開します。
5. ツリーで、「『行ワークフローが有効化された』から始まる行」を選択します。
6. [ワークフローの詳細の表示] をクリックします。
7. 作業項目セクションを展開します。
8. [再割り当て] をクリックします。
9. [ユーザー] フィールドで、[管理者] を選択します。
10. [再割り当て] をクリックします。
11. ページを閉じます。
12. ページを閉じます。

## <a name="create-an-rfq"></a>RFQ の作成
1. ページを更新します。
2. [見積依頼] をクリックします。
3. [購買組織] フィールドで、「USMF」を選択します。
    * 要求明細行で同じ法人を選択する必要があります。  
4. 一覧で、選択された行をマークします。
    * 自分の購買要求に複数の明細行がある場合は、RFQ に追加するすべての明細行を選択します。  
5. [OK] をクリックします。
6. ページを更新します。
7. 情報ボックスを開き、関連ドキュメントのセクションを展開します。
    * 既に情報ボックスが開いている場合があります。 [行/ヘッダー] 切り替えボタンの右側にある矢印がついたアイコンを探します。 矢印が右を指している場合は、情報ボックスが既に開いています。 矢印が左を指している場合は、矢印をクリックし情報ボックスを開きます。  
8. [見積依頼] フィールドのリンクをクリックし、先ほど作成した RFQ を開きます。
9. [ヘッダー] をクリックします。
10. [追加] をクリックします。
11. [仕入先] フィールドで、値を入力または選択します。
12. [追加] をクリックします。
13. [仕入先] フィールドで、値を入力または選択します。
14. [送信] をクリックします。
15. [OK] をクリックします。
16. [入力] をクリックして回答します。
17. [アクション ペイン] で、[返信] をクリックします。
18. [データのコピー] をクリックして返信します。
    * これにより、数量や日付などのデータが RFQ から返信へコピーされます。  
19. [単価] フィールドに数値を入力します。
    * これは、仕入先から受け取った価格です。 仕入先からの追加情報を入力することもできます。  
20. [承認] をクリックします。
21. [OK] をクリックします。

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>仕入先および価格が請求に転送されていることを確認します。
1. ページを閉じます。
2. [明細行] をクリックします。
3. [関連情報] をクリックします。
4. [購買要求] をクリックします。
5. RFQ の移動明細行を選択します。
    * 価格および仕入先が要求書にコピーされていることを確認します。  
6. [ワークフロー] をクリックすると、ドロップ ダイアログを開きます。
7. [完了] をクリックします。
8. ページを閉じます。
9. [完了] をクリックします。

