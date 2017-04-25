---
title: "展開Excelを使用します。"
description: "[このトピックでは、Microsoft Excelデータの取得を開き、展開Excel、Microsoft Dynamicsの会社を使用してデータを表示および更新および編集する方法を説明します。 データの取得を開き、工程のExcelやMicrosoft Dynamics 365から開始できます。"
author: ChrisGarty
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: af7e7288f741b3c519227e2778c4c4311c3a2012
ms.openlocfilehash: 8af663b47117759ed3b2e2ed8eee85ae4df100d1
ms.lasthandoff: 03/31/2017


---

# <a name="use-the-excel-add-in"></a>展開Excelを使用します。

[このトピックでは、Microsoft Excelデータの取得を開き、展開Excel、Microsoft Dynamicsの会社を使用してデータを表示および更新および編集する方法を説明します。 データの取得を開き、工程のExcelやMicrosoft Dynamics 365から開始できます。

Microsoft Excelデータの取得の開始によって、展開Excel、Microsoft Dynamicsの会社を使用して、迅速かつ簡単にデータを表示および編集できます。 この展開はMicrosoft Excel 2016が必要です。 **注記: ** Microsoft AzureのActive Directory (Azureの広告) テナントがActive Directoryのフェデレーション サービス (広告FS) を使用するようにコンフィギュレーションするExcelの展開集計が正しく署名が5年1月2016日の更新が適用されていることを確かめなければがあります。

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Dynamics 365 for Operationsで始まるとExcelデータの取得を開きます。
1.  、Microsoft Dynamics 365]ページで、をクリックして** Microsoft Office、未**します。 ページのルート データ ソース (テーブル) はすべてのエンティティのルート データ ソース、既定値を** Excelでのページに未処理オプション**生成される同じ場合。 ** Excel **オプションで未処理の頻繁に使用するページで、など) を見つけることができる**すべての仕入先** **およびすべての顧客**。
2.  ** Excelで開きます。**オプションをクリックし、生成されるファイルを開きます。 このファイルに環境のエンティティ、ポインタ、展開Excelにポインターの情報バインディングがあります。
3.  Excelで、展開実行することをExcelを有効にします**有効の編集**。 Excelのウィンドウの右側ウィンドウのExcelの展開します。
4.  展開Excelを初めて実行する場合は、をクリックして展開**このを信頼**します。
5.  署名することを満たすよう求められた場合は**署名して**クリックし、[Dynamics 365 for Operationsに署名するため、常にで同じ資格情報を使用して署名します。 Excelを展開して、Internet Explorerの前のサインインのコンテキストを使用して、自動的に署名する。 したがって、展開Excelの右上隅のユーザー名を確認します。

展開Excelが自動的に選択したエンティティのデータを読み取ります。 展開Excelが、またまでファイルにデータが存在しないことに注意してください。

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Excelから起動時にExcelデータの取得を開きます。
1.  のExcelで、**挿入**、**アドイン**グループ、会社の店舗を開くには、[**店舗**を記録します。
2.  会社の店舗で、キーワード「Dynamicsで検索する場合は、[」**追加します。**の横に、**展開Microsoft Dynamicsのオフィス** (展開Excel)。
3.  展開Excelを初めて実行した場合、展開実行することをExcelを有効にします**このを展開して、信頼**。 Excelのウィンドウの右側ウィンドウのExcelの展開します。
4.  **オプション**ウィンドウを開くには、[**サーバーの情報を追加します。**。
5.  工程のターゲット、Dynamics 365 for OperationsのブラウザURLを作成するには、挙げましたり貼り付けます、それを**サーバーURL **フィールドにつき、[削除ホスト名の後にすべてのコピー (たとえば、削除の**/か。cmp=usmf&mi=CustTableListPage **)。 結果のURLでホスト名があるべきされます (たとえば、** https://xxx.dynamics.com**)です。
6.  [**見込み** **、[はい変更を確認する**クリックします。 Excelの追加および再開負荷メタデータ。 **デザイン**ボタンは、なりました。 展開Excelにリンクがある場合は**負荷のアプレット**は、署名される適切なユーザーとしてボタン グリッド。 詳細については、「負荷のアプレット、このトピックの「トラブルシューティング」にある」を表示するしてください。
7.  [デザイン** **。 展開Excel形式は、事業体メタデータを検索します。
8.  [**テーブルを追加します。**。 エンティティの一覧が表示されます。 エンティティは「名前に一覧表示されます (」フォームを分類します。
9.  **顧客-顧客など、リストのエンティティを、**、[クロスドッキング** [**選択します。
10. のフィールドを追加するには、**使用できるフィールドに** **選択したフィールド**一覧表示し、フィールドをクリックし、サイド リンク表示します。** **追加します。 また、フィールドをダブルクリックします。
11. **選択したフィールド**リストに必要なフィールドを追加した後、カーソルをワークシートの適切な場所 (たとえば、セルA1)、確認、[クリックします。を**される**。 [デザイナーを終了するに**される**クリックします。
12. データセットを引き込む[**更新**。

## <a name="view-and-update-entity-data-in-excel"></a>Excelの表示と更新のデータの取得
展開Excelのブックにデータの取得を読込んだと、**更新クリックして**展開Excelのデータはいつでも更新できます。

## <a name="edit-entity-data-in-excel"></a>Excelデータの取得を編集します。
**発行クリックして**展開Excelを必要として公開するデータの取得を変更できます。 レコードを編集するには、ワークシートのセルを選択し、セルの値を変更します。 新しいレコードを追加するには、次の手順の一つを実行します:

-   手順でワークシートをクリックし、**展開Excelでは**新規]をクリックします。
-   カーソルが、その行の最後の列を終了し、新しい行を作成するまでワークシートの最後の行をクリックし、Tabキーを押します。
-   行で、ワークシート]をクリックし、セルでのデータ入力を開始します。 このセルにフォーカスを移動すると新しい行を含める場合は、ワークシートを展開します。

レコードを削除するには、次の手順の一つを実行します:

-   削除する行番号をワークシートの行の横の右クリックし、[]をクリックすると**削除**。
-   削除する場合は、ワークシートの行を右クリックし、[**削除** ** &gt; テーブル行を**クリックします。

## <a name="add-or-remove-columns"></a>列の追加または削除
ワークシートに自動的に追加する列を調整する場合でも、デザイナーを使用できます。

1.  **オプション**ボタンをギヤ記号 () クリックし、**有効デザイン**このチェック ボックスをオンにして展開Excelデータ ソース デザイナを開始します。
2.  [デザイン** **展開Excelの日付。 すべてのデータ ソースが表示されます。
3.  データ ソースの横に、**編集を行います**ボタン (鉛筆の記号) をクリックします。
4.  必要になるように**選択したフィールド**リストの一覧を調整します:
    -   のフィールドを追加するには、**使用できるフィールドに** **選択したフィールド**一覧表示し、フィールドをクリックし、サイド リンク表示します。** **追加します。 また、フィールドをダブルクリックします。
    -   のフィールドを削除するには、**選択したフィールド**一覧表示し、フィールドをクリックして、[]をクリックします。**削除するには、**。 また、フィールドをダブルクリックします。
    -   フィールドの順序を変更するには、のフィールドを**選択したフィールド**一覧表示し、サイド リンク** **をクリックして** **。

5.  [データ ソースに変更を加えて** **更新します。 [デザイナーを終了するに**される**クリックします。 フィールド (列) を追加する場合は、更新データセットを取り込むように、**更新**クリックします。

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Troubleshooting
ある簡単なステップによって決済されるいくつかの問題があります。

-   **負荷のアプレット ボタンが表示されます。** 展開Excelにリンクがある場合は**負荷のアプレット**サインイン、後で、署名される適切なユーザーとしてボタン グリッド。 適切なユーザー名を展開Excelの右上隅に表示されることをこの問題を解決するために、確認します。 誤ったユーザー名が現われたら、それをクリックし、署名し、署名します。
-   ** 「の」されたメッセージが表示されます。** 展開Excelのメタデータの読み込み中「の」されたメッセージが表示された場合は、展開Excelに署名する勘定の対象としたサービス、インスタンス、またはデータベースを使用するためのアクセス許可がありません。 適切なユーザー名を展開Excelの右上隅に表示されることをこの問題を解決するために、確認します。 誤ったユーザー名が現われたら、それをクリックし、署名し、署名します。
-   **、WebページからExcelに表示されます。** 空白Webページのサインイン プロセス中に開くと、勘定では、広告FS必要がありますが、サインイン]ダイアログ ボックスを行うには展開を実行するExcelのバージョンが完全に反映されません。 この問題を解決するには、使用しているExcelのバージョンを更新します。 延期されたチャネルである企業に属するExcelのバージョンを更新するには、使用して、会社の配置[ツール] (https://technet.microsoft.com/library/jj219422.aspx) [延期されたチャネルから現在のチャンネル] (https://technet.microsoft.com/library/mt455210.aspx)に移。


