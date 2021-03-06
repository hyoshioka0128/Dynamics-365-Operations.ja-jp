---
title: 誰かの代わりに製品を注文するためのアクセス許可の設定
description: この手順では、他の作業者に代わって購買要求を作成するためのアクセス許可を作業者に付与する方法を示します。
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eea1577972879cc24a2295a0c5a8d7d3de5f4520
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837977"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>誰かの代わりに製品を注文するためのアクセス許可の設定

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、他の作業者に代わって購買要求を作成するためのアクセス許可を作業者に付与する方法を示します。 つまり、購買要求「作成者」が他の「要求者」の要求を作成できます。 この手順では、違う法人または作業単位で品目とサービスを注文する作業者のアクセス許可を付与する方法も示します。 通常、これらのタスクは、購買マネージャーが実行します。 USMF デモ会社または独自のデータでこの手順を使うことができます。


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>別の作業者の代わりに購買要求を入力するアクセス許可を付与します
1. [調達] > [設定] > [ポリシー] > [購買要求アクセス許可] の順に移動します。
    * [現在のビュー] フィールドが作成者によって設定されていることを確認します。  左ウィンドウの一覧は、他のユーザーに代わって要求を作成する許可を付与されるユーザーを示します。  
2. アクセス許可を付与する個人を選択します (作成者)。
3. [追加] をクリックします。
4. 依頼者として追加する個人を検索し選択します。
    * 依頼者は、作成者が代わりに要求を作成できる人物です。  
    * [認証] フィールドで、選択した作業者に代わって作成者が購買要求を作成できるよう [特定] を選択します。 作成者がその作業者に報告するすべての作業者に代わって購買要求を作成できるよう [レポート] を選択します。  
5. [有効開始] フィールドで、日付を入力します。
6. [有効期限] フィールドで、日付を入力します。

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>選択した作業者の購買要求を作成するためのアクセス許可を持つ作成者を表示します。
1. [現在のビュー] フィールドで、「依頼者」を選択します。
    * 選択した作業者の代わりに購買要求を作成するアクセス許可を与える作成者の一覧を表示します。  
2. [クイック フィルター] を使用して、依頼者としてちょうど追加したばかりの作業者を検索します。
3. 依頼者を選択します。
    * 作成者の一覧は、左ウィンドウで選択された要求者に代わって品目を注文するアクセス許可があるユーザーを表示します。   ここで追加の作成者を追加できます。   このビューは、そのユーザーの主要な法人および作業単位ではない場合の、法人および作業単位内で依頼人のアクセス許可を付与することができます。  

