---
title: 仕入先の支払手数料の定義
description: 仕入先支払手数料を設定します。
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e9e723ec54b6f34082c422ce4c8e48bf52d2e3e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835469"
---
# <a name="define-vendor-payment-fees"></a>仕入先の支払手数料の定義

[!include [task guide banner](../../includes/task-guide-banner.md)]

仕入先支払手数料を設定します。 このタスクでは、USMF というデモ会社を使用します。

1. [買掛金勘定] > [支払の設定] > [支払手数料] の順に移動します。
2. [新規] をクリックします。
3. [手数料 ID] フィールドに値を入力します。
    * 手数料 ID は、「EFT_Fee」などの手数料が使用される日を定義します。  
4. [名前] フィールドに値を入力します。
5. [手数料説明] フィールドに値を入力します。
    * 手数料の算定日に関する詳細情報を追加します。  
6. [請求] フィールドで、「仕入先」または「元帳」を選択します。
    * 手数料が自分の組織で処理されるとき、元帳が使用されます。  手数料が仕入先で算定されるとき、仕入先が使用されます。  
7. 手数料が経費で処理される主勘定を入力します。
    * このオプションは、元帳を [請求] オプションとして選択する場合にのみ使用できます。  
8. この手数料が使用できる仕訳帳を選択します。 
    * 仕入先支払手数料に関しては、「仕入先出金」仕訳帳を選択します。　  
9. [保存] をクリックします。
10. [支払手数料の設定] をクリックします。
    * 手数料が選択した仕訳帳の既定値としていつ設定されるかを定義する [支払手数料の設定] に進みます。  
11. 「テーブル」、「グループ」または「全て」を選択します。
    * 「テーブル」は一つの銀行口座を選択するために使用され、「グループ」は銀行グループを選択するために使用され、「すべて」はすべての銀行口座にこの費用の設定を適用するために使用されます。  
12. 銀行グループまたは銀行口座を選択します。
    * 「グループ」を選択した場合、ルックアップには銀行グループが表示され、「テーブル」を選択した場合、銀行口座が表示されます。  
13. 支払手数料が評価される時に使用する支払方法を選択します。
14. 選択した支払方法の支払詳細を選択します。
    * 支払仕様は、電子資金振替に使用されます。  
15. 手数料が割合、金額、または間隔であるかどうかを選択します。
16. 手数料の金額の割合を入力します。
    * 手数料が割合である場合、割合を入力します。 手数料が金額である場合、金額を入力します。 手数料が間隔である場合、階層化された手数料を定義する [間隔] タブを使用します。  
17. [手数料の通貨] フィールドで、算定される手数料の通貨を選択します。
    * この通貨はこの手数料に適用されます。 支払通貨は、支払通貨に基づいて手数料に関するルールをいつ評価するかを定義するために使用されます。 たとえば、支払が EUR で行われた場合、銀行は手数料を請求しますが、その他の支払手数料はすべて算定されません。  
18. [保存] をクリックします。

