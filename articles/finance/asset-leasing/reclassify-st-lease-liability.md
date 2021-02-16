---
title: リース負債の短期部分の再分類
description: このトピックでは、一部のリース負債を短期として再分類するための月次仕訳入力の作成方法について説明します。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 46bcd396c93bc1d2944241165d438f8ccc013e20
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445380"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>リース負債の短期部分の再分類

[!include [banner](../includes/banner.md)]

このトピックでは、一部のリース負債を短期として再分類するための月次仕訳入力の作成方法について説明します。 バッチ プロセスで選択されたスケジュールが **短期リース負債の再分類** の場合は、仕訳入力が作成されます。 このエントリは、月の最後の日にリース負債の現在の部分を転記するために使用されます。 同時に、次の月の最初の日の時点で、取消エントリが転記されます。

リース負債の短期の部分は、負債の償却スケジュールとして示されています。 仕訳入力が転記されると、**負債再分類の仕訳が生成済み** 列が使用可能になり、スケジュールにも仕訳 ID が入力されます。

短期負債の再登録仕訳入力を作成および転記するには、次のステップに従います。

1. **資産リース \> 定期 \> バッチ仕訳の生成** に移動します。
2. **バッチ仕訳作成** ダイアログ ボックスの **スケジュールの選択** フィールドで、**短期リース負債の再分類** を選択します。
3. **リース グループ゜** フィールドで、リース グループを選択します。 または、**帳簿 ID** フィールドで、帳簿 ID を選択します。
4. **転記** パラメータをオンにします。 または、エントリを作成するが転記されない場合は、このパラメータをオフのままにしておきます。
5. 転記の前に **転記の前にプレビュー** パラメータをオンにして、このエントリを表示します。
6. **OK** を選択します。