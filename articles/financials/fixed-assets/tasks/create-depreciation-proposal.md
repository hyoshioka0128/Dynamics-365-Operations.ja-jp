---
title: 償却提案を作成します
description: この手順では、減価償却のバッチ提案がどうのように機能するか、および固定資産の減価償却を提案する方法について説明します。
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07146adfe1ead2b6e06e3c323963f8c012381b76
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840004"
---
# <a name="create-depreciation-proposal"></a>償却提案を作成します

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、減価償却のバッチ提案がどうのように機能するか、および固定資産の減価償却を提案する方法について説明します。 このタスクでは USMF のデモ会社および経理担当者のロールを使用します。


## <a name="create-depreciation-proposal"></a>償却提案を作成します
1. [固定資産] > [仕訳入力] > [償却提案の作成] の順に移動します。
2. [仕訳帳名] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、選択された行のリンクをクリックします。
4. [終了日] フィールドで、日付を入力します。
    * 月間の減価償却を 1 つの仕訳帳明細行に集計する場合に、減価償却の集計オプションを選択します。  
    * たとえば、終了日の値が 2015 年 3 月 31 日の場合、次の説明: “2015 年 1 月 31 日以降の原価償却” が作成されます。 提案された仕訳帳明細行の [日付] フィールドは、2015 年 3 月 31 日に設定されます。  
    * 償却提案は資産、資産グループ、または他の検索条件別に、フィルター オプションを使用してフィルター処理できます。  
    * 固定資産のフォームの取得提案または償却提案を作成すると、減価償却をバッチで提案できます。 これは、より多くのシステム リソースを使用する大規模な提案に対して推奨されています。 バッチのオプションを選択した場合、その処理中に他のタスクも実行できます。 この方法で減価償却を提案する場合、減価償却は固定資産の価値モデルに対して計算されます。  
5. [仕訳帳の作成] をクリックします。

## <a name="review-depreciation-entries"></a>減価償却のエントリを確認します
1. [固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. [明細行] をクリックします。
4. [転記] をクリックします。

