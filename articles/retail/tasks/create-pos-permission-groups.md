---
title: POS アクセス許可グループの作成
description: この手順は、POS アクセス許可グループを作成する方法を示します。
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b30c9a1d7fe4598695423ba700ebc88a794a49c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566367"
---
# <a name="create-pos-permission-groups"></a>POS アクセス許可グループの作成

[!include[task guide banner](../includes/task-guide-banner.md)]

この手順は、POS アクセス許可グループを作成する方法を示します。 このタスクの作成に使用するデモ データの会社は USRT です。 このタスクは「小売工程マネージャー ロール」を対象としています。

1. アクセス許可グループに移動します。
2. [新規] をクリックします。
3. [POS アクセス許可グループ ID] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
5. [タイム レコーダー エントリの表示] フィールドで [はい] を選択します。
    * これで、POS アクセス許可グループのさまざまなアクセス許可を有効、または無効にすることができます。 複数のアクセス許可に対して、POS ユーザーが操作を実行することができるかどうか評価するために使用する値を設定することができます。  このタスク ガイドは、レジ担当者に支給される可能性があるいくつかのアクセス許可を有効にします。  
6. [注文の作成を許可] フィールドで [はい] を選択します。
7. [注文の編集を許可] フィールドで [はい] を選択します。
8. [注文の取得を許可] フィールドで [はい] を選択します。
9. [パスワードの変更を許可] フィールドで [はい] を選択します。
10. [ブラインド クローズを許可] フィールドで [はい] を選択します。
11. [保存] をクリックします。
    * 変更が保存された後、小売チャンネルへ変更をプッシュするために、スタッフ配送スケジュールを実行する必要があります。  
12. ページを閉じます。
13. ジョブに移動
    * 次に、ジョブに対して POS アクセス許可グループを割り当てます。  
14. 一覧で、目的のレコードを見つけ、選択します。
15. 一覧で、選択された行のリンクをクリックします。
16. [編集] をクリックします。
17. [ジョブ分類] セクションを展開します。
18. [POS アクセス許可グループ] フィールドで、値を入力または選択します。
    * 作業者のPOS アクセス許可が職位のレベルで上書きされない場合、このジョブの職位のすべての作業者は、このPOS アクセス許可グループの設定を使用します。  
19. [保存] をクリックします。
    * 変更が保存された後、小売チャンネルへ変更をプッシュするために、スタッフ配送スケジュールを実行する必要があります。  

