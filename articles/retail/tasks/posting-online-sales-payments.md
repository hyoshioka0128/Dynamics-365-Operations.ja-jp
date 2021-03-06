---
title: オンラインの販売と支払の転記
description: この手順では、オンライン ストアのトランザクションの販売注文と支払を作成する反復バッチ ジョブを構成および実行する方法を説明します。
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13839bbe6ca03f3cfc7036fce87477bf7d5af2a7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550211"
---
# <a name="posting-of-online-sales-and-payments"></a>オンラインの販売と支払の転記

[!include[task guide banner](../includes/task-guide-banner.md)]

この手順では、オンライン ストアのトランザクションの販売注文と支払を作成する反復バッチ ジョブを構成および実行する方法を説明します。 この手順では、デモ データの会社 USRT を使用します。

1. [すべてのワークスペース] > [小売店舗の財務] に移動します。
2. [注文の同期] をクリックします。
3. [組織階層] のフィールドで、「地域ごとの小売店舗」を選択します。
    * 店舗グループのバッチ ジョブを作成する場合は、特定のオンライン ストアまたはノードを選択します。  
    * 選択した項目を追加するには、矢印をクリックします。  
4. [バックグラウンドで実行] タブをクリックします。
5. [バッチ処理] チェック ボックスをオンまたはオフにします。
6. [再実行] をクリックします。
7. [終了日なし] のオプションを選択します。
8. [カウント] フィールドに数値を入力します。
9. [OK] をクリックします。
10. [OK] をクリックします。

