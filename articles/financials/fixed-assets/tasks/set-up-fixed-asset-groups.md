---
title: 固定資産グループを設定します
description: この手順では、新しい固定資産グループを作成する方法を説明します。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8f52b73c07aad1047d6e6e7caf80daecc9c26e7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839788"
---
# <a name="set-up-fixed-asset-groups"></a>固定資産グループを設定します

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、新しい固定資産グループを作成する方法を説明します。 これは USMF の法人に対して経理担当ロールとデモ データを使用します。

1. [固定資産] > [設定] > [固定資産グループ] の順に移動します。
2. [新規] をクリックします。
3. [固定資産グループ] フィールドに値を入力します。
4. [名前] フィールドに値を入力します。
    * 固定資産グループにおける固定資産の自動採番と番号順序コードは、固定資産のパラメータの設定より優先されます。 この固定資産グループの資産に他のグループからの異なる番号付けがある場合、ここでこれを変更できます。  
5. [帳簿] をクリックします。
6. [帳簿] フィールドで値を入力または選択します。
    * [減価償却の計算] フィールドが [はい] に設定されている場合、資産帳簿は償却提案に含まれます。 減価償却の計算が [いいえ] に設定されている場合、資産は自動的に償却されません。  
7. 資産の耐用年数を設定します。
    * 耐用年数を設定した後に減価償却期間のフィールド値が計算されることに注意してください。  
8. [減価償却方法] フィールドで、オプションを選択します。
9. ページを閉じます。

