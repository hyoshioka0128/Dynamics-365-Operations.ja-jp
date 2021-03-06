---
title: 画像が埋め込まれた Office 形式でレポートを生成するコンフィギュレーションのデザイン
description: このトピックの手順は、Microsoft Office (Excel および Word) の埋め込み画像を含む電子ドキュメントを生成する、電子申告 (ER) コンフィギュレーションの設計方法に関する情報を提供します。
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fb02e561f6792c57b924ba64a5ca3d3974289ee
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544406"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>画像が埋め込まれた Office 形式でレポートを生成するコンフィギュレーションのデザイン

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順にあるステップを完了するには、まず「ER コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」にある手順を完了します。 この手順では、電子申告 (ER) コンフィギュレーションを設計して、埋め込み画像を含む Microsoft Excel または Word の電子ドキュメントを生成する方法を説明します。 この手順では、サンプル会社 Litware, Inc. に必要な ER コンフィギュレーションを作成します。USMF データセットを使用してこれらの手順を完了できます。 この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザー用に作成されています。 始める前に、ヘルプ トピック [電子申告ツールで生成されるビジネス ドキュメントへの画像と図形の埋め込み](../electronic-reporting-embed-images-shapes.md) に一覧表示されたファイルをダウンロードして保存します。 ファイルは cheques.xml のモデル、format.xml を印刷する小切手、会社の logo.png、署名 image.png、署名画像 2.png、および小切手テンプレート Word.docx です。

## <a name="verify-prerequisites"></a>前提条件の確認  
 1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。  
 2. サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。 このコンフィギュレーション プロバイダーが表示されない場合は、「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」という手順のステップを完了する必要があります。   
 3. [コンフィギュレーションをレポートする] をクリックします。  
 
## <a name="add-a-new-er-model-configuration"></a>新しい ER モデル コンフィギュレーションの追加  
 1. 新しいモデルを作成する代わりに、以前に保存した ER モデル コンフィギュレーション ファイル (cheques.xml のモデル) を読み込むことができます。 このファイルには、支払小切手のサンプル データ モデルおよび Dynamics 365 for Operations アプリケーションのデータ コンポーネントへのデータ モデルのマッピングが含まれます。   
 2. [バージョン] クイック タブで、[交換] をクリックします。   
 3. [XML ファイルから読み込む] をクリックします。  
 4. [参照] をクリックし、cheques.xml のモデルを選択します。   
 5. [OK] をクリックします。  
 6. 読み込まれたモデルは、Excel と Word で画像を含むドキュメントを生成するための情報のデータ ソースとして使用されます。  

## <a name="add-a-new-er-format-configuration"></a>新しい ER 形式コンフィギュレーションを追加する  
 1. 新しい形式を作成する代わりに、以前に保存した ER 形式コンフィギュレーション ファイル (format.xml を印刷する小切手) を読み込むことができます。 このファイルには、事前に印刷されたフォームを使用して小切手を印刷する形式のサンプル レイアウトと、「小切手のモデル」データ モデルへのこの形式のマッピングが含まれています。   
 2. [交換] をクリックします。  
 3. [XML ファイルから読み込む] をクリックします。  
 4. [参照] をクリックして、format.xml ファイルを印刷する小切手を選択します。   
 5. [OK] をクリックします。  
 6. ツリーで、「小切手のモデル」を展開します。  
 7. ツリーで、「小切手のモデル\小切手の印刷形式」を選択します。  
 8. 読み込まれた形式は、Excel と Word で画像を含むドキュメントを生成するために使用されます。   

## <a name="configure-er-user-parameters"></a>ER ユーザー パラメーターのコンフィギュレーション  
 1. アクション ウィンドウで、[設定] をクリックします。  
 2. [ユーザー パラメーター] をクリックします。  
 3. [設定の実行] フィールドで、[はい] を選択します。  
  「ドラフトの実行」フラグをオンにして、完了したドラフト バージョンではなく、選択した形式のドラフト バージョンを開始します。  
 4. [OK] をクリックします。  

## <a name="configure-cash--bank-management-parameters"></a>現金 & 銀行管理パラメーターのコンフィギュレーション  
 1. [現金および銀行管理] > [銀行口座] > [銀行口座] の順に移動します。  
 2. クイック フィルターを使用して、値が「USMF OPER」である [銀行口座] フィールドをフィルター処理します。  
 3. アクション ペインで、[設定] をクリックします。  
 4. [小切手] をクリックします。  
 5. [設定] セクションを展開します。  
 6. [編集] をクリックします。  
 7. [会社のロゴ] フィールドで [はい] を選択します。  
 8. [会社のロゴ] をクリックします。  
 9. [変更] をクリックします。  
 10. [参照] をクリックして、以前にダウンロードしたファイル、会社の logo.png を選択します。   
 11. [保存] をクリックします。  
 12. ページを閉じます。  
 13. [署名] セクションを展開します。  
 14. [最初の署名を印刷] フィールドで、[はい] を選択します。  
 15. [変更] をクリックします。  
 16. [参照] をクリックして、以前にダウンロードしたファイル、署名 image.png を選択します。   
 17. [コピー] セクションを展開します。  
 18. [透かし] フィールドで、オプションを選択します。  
 19. [一般的な電子エクスポート形式] フィールドで [はい] を選択します。  
 20. [小切手の印刷フォーム] コンフィギュレーションを選択します。  
 21. これで、小切手を印刷するのに、選択された ER 形式が使用されます。  
 22. [添付] をクリックします。  
 23. [新規] をクリックします。  
 24. [ファイル] をクリックします。  
 25. [参照] をクリックして、以前にダウンロードしたファイル、署名画像 2.png を選択します。   
 26. ページを閉じます。  
 27. ページを閉じます。  
 28. ページを閉じます。  
 29. [現金および銀行管理] > [設定] > [現金および銀行管理パラメーター] の順に移動します。  
 30. [無効な銀行口座での事前通知の作成を許容] フィールドで [はい] を選択します。  
 31. [保存] をクリックします。  
 32. ページを閉じます。  
