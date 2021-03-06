---
title: 出荷配送業者の設定
description: この手順では、出荷の配送業者を設定し、サービス、出荷モード、輸送入札、輸送機関の制約、および出荷レートなどの詳細を定義する方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569105"
---
# <a name="set-up-shipping-carriers"></a>出荷配送業者の設定

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、出荷の配送業者を設定し、サービス、出荷モード、輸送入札、輸送機関の制約、および出荷レートなどの詳細を定義する方法について説明します。 配送コーディネーターは、出荷の配送業者を入荷または出荷に割り当てることができます。


## <a name="create-a-new-shipping-carrier"></a>新しい出荷の配送業者の作成
1. [輸送管理] > [設定] > [配送業者] > [出荷の配送業者] の順に移動します。
2. [新規] をクリックします。
3. [出荷の配送業者] フィールドに値を入力します。
4. [名前] フィールドに値を入力します。
5. [モード] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、目的のレコードを見つけ、選択します。
7. 一覧で、選択された行のリンクをクリックします。

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>出荷配送業者の一般情報を入力します。
1. [概要] セクションの展開を切り替えます。
2. [出荷配送業者の有効化] チェック ボックスをオンまたはオフにします。
3. [仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
    * 出荷配送業者の仕入先を選択します。  
4. 一覧で、目的のレコードを見つけ、選択します。
5. 一覧で、選択された行のリンクをクリックします。
6. [輸送業者タイプ] フィールドで、オプションを選択します。
    * マニュアルを選択して配送業者のページを使用するか、または EDI を選択して、電子データ交換 (EDI) で入金を更新できます。  
7. [配送業者の評価をアクティブ化] チェック ボックスをオンまたはオフにします。

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>出荷配送業者の必要なサービスを作成します。
1. [サービス] セクションの展開を切り替えます。
2. [新規] をクリックします。
3. 一覧で、選択された行をマークします。
4. [配送サービス] フィールドに値を入力します。
5. [名前] フィールドに値を入力します。
6. [輸送方法] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. 一覧で、目的のレコードを見つけ、選択します。
8. 一覧で、選択された行のリンクをクリックします。

## <a name="set-up-the-address-for-the-carrier-optional"></a>配送業者の住所の設定 (オプション)
1. [住所] セクションの展開を切り替えます。
2. [新規] をクリックします。
3. [名前または説明] フィールドに値を入力します。
4. [国/地域] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
5. 一覧で、選択された行のリンクをクリックします。
6. [配送先郵便番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. 一覧で、目的のレコードを見つけ、選択します。
8. 一覧で、選択された行のリンクをクリックします。
9. [番地] フィールドに値を入力します。
10. [OK] をクリックします。

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>出荷配送業者の評価プロファイルの設定
1. [評価プロファイル] セクションの展開を切り替えます。
2. [新規] をクリックします。
3. 一覧で、選択された行をマークします。
4. [評価プロファイル] フィールドに値を入力します。
5. [名前] フィールドに値を入力します。
6. [サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. 一覧で、目的のレコードを見つけ、選択します。
8. 一覧で、選択された行のリンクをクリックします。
9. [倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
10. 一覧で、目的のレコードを見つけ、選択します。
11. 一覧で、選択された行のリンクをクリックします。
12. [レート エンジン] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
    * 配送業者との契約に従ってレート エンジンを選択します。  
13. 一覧で、目的のレコードを見つけ、選択します。
14. 一覧で、選択された行のリンクをクリックします。
15. [レート マスター] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
16. 一覧で、目的のレコードを見つけ、選択します。
17. 一覧で、選択された行のリンクをクリックします。
18. [輸送時間エンジン] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
19. 一覧で、選択された行のリンクをクリックします。
20. [保存] をクリックします。

