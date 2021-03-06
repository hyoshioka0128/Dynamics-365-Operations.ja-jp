---
title: 仕訳帳の詳細なルールの作成
description: この手順は、仕訳帳の詳細なルールの作成について説明します。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ec0db1bc5018649acaca05c71a510880b415777
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846682"
---
# <a name="create-advanced-rules-for-journals"></a>仕訳帳の詳細なルールの作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順は、仕訳帳の詳細なルールの作成について説明します。 これには、仕訳帳のコントロールおよびユーザーの転記制限の設定が含まれます。 この手順では、デモ データの会社 USMF を使用します。


## <a name="set-up-journal-control"></a>仕訳帳コントロールの設定
1. [総勘定元帳] > [仕訳帳の設定] > [仕訳帳名] に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. [仕訳帳コントロール] をクリックします。
4. [追加] をクリックします。
5. [会社コード] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、目的のレコードを見つけ、選択します。
7. 一覧で、選択された行のリンクをクリックします。
8. [追加] をクリックします。
9. [勘定構造] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
10. 一覧で、目的のレコードを見つけ、選択します。
11. 一覧で、選択された行のリンクをクリックします。
12. [区分] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
13. 一覧で、選択された行のリンクをクリックします。
14. [開始値] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
15. 一覧で、目的のレコードを見つけ、選択します。
16. 一覧で、選択された行のリンクをクリックします。
17. [終了値] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
18. 一覧で、目的のレコードを見つけ、選択します。
19. 一覧で、選択された行のリンクをクリックします。

## <a name="set-up-posting-restrictions"></a>転記制限の設定
1. ページを閉じます。
2. [転記制限] をクリックします。
3. [転記制限をどのように設定しますか ?] で、[ユーザー グループ別] を選択します。
4. ツリーで、「この仕訳帳名で転記を許可するグループ」をチェックします。
5. [OK] をクリックします。

