---
title: 発生主義スキーマの作成
description: このタスク ガイドは、発生主義スキーマの作成について説明します。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0ae55000a5cf1593d057d940dc3dbbf9e5cb3f3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834891"
---
# <a name="create-accrual-schemes"></a>発生主義スキーマの作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

このタスク ガイドは、発生主義スキーマの作成について説明します。 このタスクでは、USMF というデモ会社を使用します。

1. [総勘定元帳] > [仕訳帳の設定] > [発生主義スキーマ] の順に移動します。
2. [新規] をクリックします。
3. [発生主義スキーマ ID] フィールドに値を入力します。
4. [発生主義スキーマの説明] フィールドに値を入力します。
5. [借方] フィールドで、任意の値を指定します。
    * 定義した主勘定は、仕訳帳伝票の明細行の借方主勘定と置き換えられ、元帳計上トランザクションに基づく繰延の取消にも使用されます。  
6. [貸方] フィールドで、任意の値を指定します。
    * 定義した主勘定は、仕訳帳伝票の明細行の貸方主勘定と置き換えられ、元帳計上トランザクションに基づく繰延の取消にも使用されます。  
7. トランザクションの転記時に、どのように伝票を判別するかを [伝票] フィールドで選択します。
8. [説明] フィールドに、転記されるトランザクションを説明する値を入力します。
9. [期間の頻度] フィールドで、トランザクションの発生頻度を選択します。
10. [期間別の発生数] フィールドに数値を入力します。
11. [トランザクションの転記] フィールドで、トランザクションを転記する時期 (「毎月」など) を選択します。

