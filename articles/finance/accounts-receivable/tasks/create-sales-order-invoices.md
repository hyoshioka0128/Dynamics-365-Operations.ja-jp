---
title: 販売注文請求書の作成
description: このタスク ガイドでは、販売注文の請求操作について説明します。請求書の結合やバッチ処理も含みます。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a41524c773284812aa6eebddcd832c78bd29166
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178700"
---
# <a name="create-sales-order-invoices"></a>販売注文請求書の作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

このタスク ガイドでは、販売注文の請求操作について説明します。請求書の結合やバッチ処理も含みます。 この手順では、USMF というデモ会社を使用します。


## <a name="create-an-invoice-from-a-sales-order"></a>販売注文から請求書を作成します。
1. **ナビゲーション ウィンドウ > モジュール > 売掛金勘定 > 注文 > 出荷済で未請求の販売注文**の順に移動します。
2. 一覧で販売注文を選択します。 
3. **アクション ウィンドウ**で、**請求書 > 生成 > 請求書**をクリックします。 この販売注文に関連付けられる複数の梱包明細があることに注意してください。 この場合、梱包明細番号ではなく <multiple> という表示になります。  
4. **パラメーター** セクションを展開します。
    - 請求書に転記するには、転記を「オン」に設定する必要があります。 また、転記をオフにし、請求書の印刷のみを行うことができます。 ただし、請求書のほかに、見積請求書の作成でも同じ操作を実行できます。  
    - このオプションはバッチ ジョブに使用されます。 クエリは、バッチ ジョブの実行時に実行されます。
5. **印刷**フィールドで、「変更後」を選択します。
6. **請求書の印刷**に対して**オン**を選択します。 印刷管理では、請求書を複数印刷できます。また、請求書を PDF ファイルとして電子メールで送信することもできます。  
7. **請求金額の印刷**フィールドで、「集計」を選択します。
8. **小切手の与信限度額**フィールドで、「残高」を選択します。
9. **キャンセル**をクリックします。

## <a name="combine-orders-into-a-single-invoice"></a>注文を 1 つの請求書に連結します。
1. **ナビゲーション ウィンドウ > モジュール > 売掛金勘定 > 注文 > すべての販売注文**の順に移動します。
2. 未処理請求書が複数ある顧客を検索します。
3. 同じ顧客からの複数の未処理販売注文を選択します。
4. **アクション ウィンドウ**で、**請求書 > 生成 > 請求書**をクリックします。
5. **パラメーター** セクションを展開します。
6. **数量**フィールドで「すべて」を選択します。 概要セクションに 2 つの請求書が表示されることに注意してください。 ここでは、それらを 1 つの請求書にマージします。  
7. **集計更新**フィールドで、「請求元仕入先」を選択します。
8. **調整**をクリックすると、販売注文を 1 つの請求書にマージします。 2 つの販売注文が 1 つの請求書にマージされました。   
9. **キャンセル**をクリックします。
10. **はい** をクリックします。

## <a name="post-invoices-in-a-batch"></a>バッチの請求書転記
1. **ナビゲーション ウィンドウ > モジュール > 売掛金勘定 > 請求書 > バッチ請求 > 請求書**の順に移動します。
2. **選択** をクリックします。
3. **OK**をクリックします。
4. **バッチ**をクリックします。
5. **バッチ処理**で、**はい**を選択します。
6. **再実行**をクリックします。
7. **日数**を選択します。
8. **OK**をクリックします。
9. **OK**をクリックします。
10. **キャンセル**をクリックします。
11. **はい** をクリックします。
