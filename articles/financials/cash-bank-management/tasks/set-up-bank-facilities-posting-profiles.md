---
title: 信用保証状についての銀行融資と転記プロファイルの設定
description: このタスクは、信用保証状を処理するために必要な銀行融資と転記プロファイルを作成します。
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 427159048ffbb17749e813d67a900622900a7f21
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841924"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>信用保証状についての銀行融資と転記プロファイルの設定

[!include [task guide banner](../../includes/task-guide-banner.md)]

このタスクは、信用保証状を処理するために必要な銀行融資と転記プロファイルを作成します。



このタスクでは、USMF というデモ会社を使用します。 




## <a name="general-ledger-parameter"></a>一般会計パラメーター
1. [現金および銀行管理] > [設定] > [現金および銀行管理パラメーター] の順に移動します。
2. [銀行ドキュメント] セクションを展開します。
3. [信用保証状の有効化] オプションを選択します。
4. [トランザクション仕訳帳] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
5. 一覧で、目的のレコードを見つけ、選択します。
6. 一覧で、選択された行のリンクをクリックします。
7. [番号順序] タブをクリックします。
    * 信用保証状の番号と信用保証状トランザクションの参照の番号順序コードを定義します。  
8. [保存] をクリックします。
9. ページを閉じます。

## <a name="create-bank-facility"></a>銀行融資の作成
1. [現金および銀行管理] > [設定] > [銀行融資] の順に移動します。
2. [新規] をクリックします。
3. [融資グループ] フィールドに、信用保証状トランザクションの銀行融資グループ名を入力します。
4. [説明] フィールドに値を入力します。
5. [保存] をクリックします。
6. [融資タイプ] タブをクリックします。
7. [新規] をクリックします。
8. [融資タイプ] フィールドに、銀行融資契約に関連する銀行融資タイプの名前を入力します。
9. [説明] フィールドで値を入力します。
10. [融資グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
11. 一覧で、目的のレコードを見つけ、選択します。
12. 一覧で、選択された行のリンクをクリックします。
13. [融資の種類] フィールドで、オプションを選択します。
14. [保存] をクリックします。
15. ページを閉じます。

## <a name="bank-posting-profile"></a>銀行転記プロファイル
1. [現金および銀行管理] > [設定] > [銀行ドキュメントの転記プロファイル] の順に移動します。
2. [新規] をクリックします。
3. [アカウント/グループ番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、目的のレコードを見つけ、選択します。
5. 一覧で、選択された行のリンクをクリックします。
6. [決済勘定] フィールドで、決済の主勘定を選択します。
7. [手数料勘定] フィールドで、経費トランザクションの勘定を選択します。
8. [保証金勘定] フィールドで、マージン トランザクションの勘定を選択します。
9. [清算勘定] フィールドで、信用保証状トランザクションの清算勘定を選択します。 
10. [保存] をクリックします。
11. ページを閉じます。

