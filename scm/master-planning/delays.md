---
title: "遅延"
description: "この記事は、マスタ プランの遅延日に関する情報を提供します。 遅延日は、マスター プランで計算される最も早い履行日が、要求日より後になる場合にトランザクションに設定される現実的な期日です。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9113c7728c5d23b70e3809bab31136aff63c6acf
ms.lasthandoff: 03/31/2017


---

# <a name="delays"></a>遅延

この記事は、マスタ プランの遅延日に関する情報を提供します。 遅延日は、マスター プランで計算される最も早い履行日が、要求日より後になる場合にトランザクションに設定される現実的な期日です。

マスター プランでは、リード タイム、材料の可用性、能力の利用可能性、計画のさまざまなパラメーターに基づいて、トランザクションの最も早い履行日を計算できます。 

マスター プランの計算で現在の日付より前の注文日付になった場合、注文を時間どおりに履行することはできません。 したがって、注文は遅延します。 この場合、マスター プランは、現在の日付からフォワード プランニングを行い、注文リード タイムを含むようにします。 これらのリード タイムは、任意の下位レベルのコンポーネント品目から開始されます。 その後、注文は、遅延日付を与えられます。 遅延日は、現在のデータに基づく実際的な期日です。 マスター プランは、遅延日数の計算も行います。 

代替の荷渡方法を選択してリード タイムを短縮できることをユーザーがわかっている場合など、状況によっては遅延を計算しないように選択することがあります。 

補充グループに対して、遅延の計算方法を設定できます。 その後、補充グループを品目に関連付けます。 

**マスター プランのパラメーター**ページで、遅延計算の開始時刻を設定できます。 この時刻以降に注文を履行する場合、注文の遅延日に 1 日が追加されます。 

**注記: 計算された、遅延が*futuresのmessages*として**以前のバージョンではした後、遅延している日付は*futuresのdate*として記述待時、形式のトランザクションは将来のset*の*aのトランザクションに言われました。

<a name="see-also"></a>参照
--------

[補充設定](coverage-settings.md)

