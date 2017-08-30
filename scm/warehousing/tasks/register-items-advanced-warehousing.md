--- 
title: "品目の着荷仕訳帳を使用した高度な倉庫管理に対応した品目の登録"
description: "この手順では、高度な倉庫管理プロセスを使用する場合に、着荷仕訳帳を使用して品目を登録する方法を示します。"
author: BibiSp
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 80f71f4ec5710ab257a45edbaee06d7c0e6a281e
ms.contentlocale: ja-jp
ms.lasthandoff: 07/28/2017

---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>品目の着荷仕訳帳を使用した高度な倉庫管理に対応した品目の登録

[!include[task guide banner](../../includes/task-guide-banner.md)]

この手順では、高度な倉庫管理プロセスを使用する場合に、着荷仕訳帳を使用して品目を登録する方法を示します。 これは通常、入荷係により行われます。 

この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。 このガイドを開始する前に、未処理の発注書明細行と共に確認済の発注書が必要です。 明細行の品目は在庫がある必要があり、製品バリアントの使用および追跡用分析コードの保有はできません。 その品目は、倉庫管理プロセスが有効化された保管分析コード グループと関連付けられている必要があります。 使用される倉庫は、倉庫管理プロセスに対して有効化されている必要があり、また受入場所は、ライセンス プレートにより制御されている必要があります。 USMF を使用している場合、会社コード 1001、倉庫 51、品目 M9200 を使用して発注書を作成できます。 

作成した発注書の数をメモし、品目番号と購買注文明細行に使用したサイトもメモします。


## <a name="create-an-item-arrival-journal-header"></a>着荷仕訳帳ヘッダーの作成
1. [品目到着] に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
    * USMF を使用している場合、「WHS」と入力できます。 他のデータを使用している場合、ユーザーが名前を選択した仕訳帳は次のプロパティを必要とします。[ピッキング場所の確認] は [いいえ] に設定し、[検査管理] は [いいえ] に設定する必要があります。  
4. [数] フィールドに値を入力します。
5. [サイト] フィールドに値を入力します。
    * 購買注文明細行に使用されているサイトを選択します。 これは、仕訳帳のすべての明細行の既定値として使用されます。 USMF で倉庫 51 を使用した場合、サイト 5 を選択します。  
6. [倉庫] フィールドに値を入力します。
    * 選択したサイトの有効な倉庫を選択します。 これは、仕訳帳のすべての明細行の既定値として使用されます。 USMF のサンプル値を使用している場合、51 を選択します。  
7. [場所] フィールドで、値を入力します。
    * 選択した倉庫の有効な場所を選択します。 場所は、ライセンス プレートにより制御されている、位置プロファイルと関連付けられている必要があります。 これは、仕訳帳のすべての明細行の既定値として使用されます。 USMF のサンプル値を使用している場合、Bulk-008 を選択します。  
8. [ライセンス プレート] フィールドのドロップダウン矢印を右クリックし、[詳細の表示] を選択します。
9. [新規] をクリックします。
10. [ライセンス プレート] フィールドで、値を入力します。
    * 値をメモします。  
11. [保存] をクリックします。
12. ページを閉じます。
13. [ライセンス プレート] フィールドで、値を入力します。
    * 作成したライセンス プレートの値を入力します。 これは、仕訳帳のすべての明細行の既定値として使用されます。  
14. [OK] をクリックします。

## <a name="add-a-line"></a>明細行の追加
1. [明細行の追加] をクリックします。
2. [品目番号] フィールドに値を入力します。
    * 購買注文明細行で使用した品目番号を入力します。  
3. [数量] フィールドに数値を入力します。
    * 登録する数量を入力します。  
    * [日付] フィールドは、この品目の手持在庫数量が在庫に登録される日付を決定します。  
    * ロット ID は、提供された情報から一意に識別される場合に、システムによって設定されます。 それ以外の場合は手動で追加する必要があります。 これは、特定の元伝票明細行にこの登録をリンクする必須のフィールドです。  

## <a name="complete-the-registration"></a>登録の完了
1. [検証] をクリックします。
    * これは、仕訳帳が転記できる状態かどうかをチェックします。 検証が失敗する場合、仕訳帳を転記する前にエラーを修正する必要があります。  
2. [OK] をクリックします。
    * [OK] をクリックしてから、メッセージを確認します。 仕訳帳が OK である、というメッセージが表示されるはずです。  
3. [転記] をクリックします。
4. [OK] をクリックします。
    * [OK] をクリックしてから、メッセージ バーを確認します。 操作完了というメッセージが表示されるはずです。  
5. ページを閉じます。

