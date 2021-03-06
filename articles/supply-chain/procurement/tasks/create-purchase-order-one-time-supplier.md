---
title: 一時仕入先に対する発注書の作成
description: この手順では、一時仕入先向けの発注書の作成方法を説明します。
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26c62aa72a7919c780bb709b185b48c97066c538
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836315"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>一時仕入先に対する発注書の作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、一時仕入先向けの発注書の作成方法を説明します。 仕入先は、手動での仕入先アカウントの作成が必要というより、むしろ発注書で自動的に作成されます。 通常、発注書は購買担当者が作成します。 このガイドで示されている例は、デモ データの会社 USMF で使用できます。 一時仕入先勘定は [買掛金勘定パラメーター] ページで設定しておく必要があります。


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>一時仕入先に対する発注書の作成
1. [調達] > [発注書] > [すべての発注書] の順に移動します。
2. [新規] をクリックします。
3. [一時仕入先] フィールドで [はい] を選択します。
    * 仕入先は自動的に作成され、発注書に割り当てられます。 仕入先は、買掛金勘定パラメーター ページで一般タブで指定したテンプレートに基づいて作成されます。  
4. [名前] フィールドには、仕入先の名前を入力します。
5. [OK] をクリックします。
    * これで他のすべての注文と同様に、発注書を完了し、処理できます。 この実行方法に関する特殊な属性はありません。 請求書では、注文に伴い作成し、その後支払いの処理を実行する仕入先のトランザクションの期日が計上されます。 これが完了すると、仕入先を削除できます。 これは通常、買掛金勘定部門により実行されます。  

