---
title: 売上税所轄官庁の設定
description: 売上税所轄官庁とは、収集された売上税の報告先および支払先です。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb0b30be91e33cb50af0ae5c2e4dcd75bd12599b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846322"
---
# <a name="set-up-sales-tax-authorities"></a>売上税所轄官庁の設定

[!include [task guide banner](../../includes/task-guide-banner.md)]

売上税所轄官庁とは、収集された売上税の報告先および支払先です。 売上税を所轄官庁に直接支払うか、売上税所轄官庁用に作成した仕入先を介して支払うことができます。 設定すると、会社は通常の支払業務を行うことで予定どおりに売上税所轄官庁に対して支払を行うことができるようになります。 売上税所轄官庁を仕入先として設定しない場合は、適切な期日に売上税所轄官庁への手動支払を準備する必要があります。 このタスクでは、USMF というデモ会社を使用します。

1. [税] > [間接税] > [売上税] > [売上税所轄官庁] の順に移動します。
2. [新規] をクリックします。
3. [所轄官庁] フィールドに値を入力します。
4. [名前] フィールドに値を入力します。
5. [仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、目的のレコードを見つけ、選択します。
7. 一覧で、選択された行のリンクをクリックします。
8. 国/地域に合ったレポートのレイアウトを選択します (使用可能な場合)。 売上税所轄官庁の要件に合うレポートのレイアウトがない場合は、既定のレイアウトを使用します。
9. 支払う税の合計金額の丸め方法を指定するには、丸めフォームおよび丸めフィールドに値を入力します。 すべての丸め誤差は、総勘定元帳で設定した自動トランザクションの勘定に転記されます。
10. [丸め] フィールドに数値を入力します。
11. [保存] をクリックします。

