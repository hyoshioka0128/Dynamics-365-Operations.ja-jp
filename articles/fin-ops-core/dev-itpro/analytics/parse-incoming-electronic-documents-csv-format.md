---
title: CSV 形式で受信したドキュメントを解析する
description: このトピックでは、受信した CSV 形式のドキュメントを解析するように電子報告 (ER) 形式を設定する方法について説明します。
author: nickselin
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2017-11-10
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d6a8439463c22033b4dfce3b7796959f50b5c195
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249345"
---
# <a name="parse-incoming-documents-in-csv-format"></a>CSV 形式で受信したドキュメントを解析する
[!include [banner](../includes/banner.md)]

電子申告 (ER) 書式をデザインして、プレーン テキスト内 (CSV 形式のファイル) の表形式データを表す受信した電子ドキュメントを解析し、これらのドキュメントからの内容を使用してアプリケーション データを更新することができます。 次のアプローチを使用できます。

+ 解析ファイル内の各明細行は別々のレコードとみなすように指定して、新しいルート シーケンス要素を追加することによりフォーマットのデザインを開始します。

    + 追加されたシーケンス要素で、適切な値を選択します。たとえば、**シーケンス要素の区切り記号**フィールド グループの**特殊文字**フィールドの**改行 - Windows (CR LF)**。

+ 追加されたルート シーケンス要素の入れ子になった順序要素を追加して、解析ファイル内の各行が一連のフィールドとみなされるように指定して、フォーマットのデザインを続行します。

    + 解析明細行でフィールド区切りとして認識される **区切り記号** フィールドで、文字列を指定することができます。

        > [!NOTE]
        > - 異なるシーケンス要素に異なるフィールド区切りを定義して、フィールドが異なる文字で区切られている特定のファイルの明細行を解析することができます。
        > - **カスタム区切り記号** フィールドは、特定のシーケンス要素では空白のままにできます。 空のフィールドは、この順序を使用して解析されるファイル行が .txt (固定長テキスト) ファイル行のように解析されることを意味します。

    + **見積申請**フィールドで、このシーケンス要素で解析される明細行の一部のフィールドが特定の文字で囲まれることが期待される場合は値を選択します。  次のオプションを使用できます。

        + **すべて** – 任意のデータ型の任意のフィールドについて、解析明細行の引用文字を含めます。 これを選択した場合、フィールド見積に使用される**引用符**フィールドで目的の文字を定義します。 たとえば、二重引用符文字。
        + **テキストのみ** – は **文字列** データ型の任意のフィールドの解析行に引用符を含めます。 これを選択した場合、フィールド見積に使用される**引用符**フィールドで目的の文字を定義します。
        + **親のみから派生** – 親シーケンス要素に定義されている、同じ**見積申請**フィールド設定を使用します。 **引用符**フィールドの設定も親シーケンス要素の設定から取得されることに注意してください。
        + **なし** – 任意のデータ型の任意のフィールドについて、解析明細行の引用文字を除外します。

+ 解析明細行のフィールド セットを表す、追加されたシーケンス要素の入れ子になった要素を追加して、フォーマットのデザインを完成させます。 **文字列**、**DateTime**、**数値**のような**テキスト** グループの必要な要素を追加して、異なるデータ型の個々のフィールドのセットとして解析行の構造を記述することができます。

    + 解析の明細行の個々のフィールドを表す形式要素については、既定では、**多様性**フィールドでは何も選択されません。 これは、解析行のフィールドの値が必須と見なされることを意味します。 **多様性**フィールドで、**ゼロ、1 つ**を選択してオプションとして解析明細行のこのフィールドの値を検討します。

        > [!NOTE]
        > データソースの品目 **isMatch** は、**多様性**フィールドで**ゼロ、1 つ**が選択されている場合、この形式を各**文字列**、**日時**、または**数値**形式要素の ER データモデルにマップすると使用できます。 このフィールドに値が含まれているときは、**isMatch** は **True** を返します。 フィールドに値がない場合は、**False** が返されます。

この機能の詳細については、**ER 外部 CSV ファイルからデータをインポートするフォーマット構成を作成する**(「IT サービス/ソリューション コンポーネントの取得/開発 (10677)」の一部) タスク ガイドを再生してください。これは、ER フォーマットを使用して、受信した CSV ファイルを解析してアプリケーション データを更新する方法について説明しています。

上記のタスクガイドを完成させるには、次のファイルをダウンロードしてください。

| 肩書き                                  | ファイル名                                                            |
|----------------------------------------|----------------------------------------------------------------------|
| ER フォーマット構成                | [1099formatcsv.xml](https://go.microsoft.com/fwlink/?linkid=862266)  |
| .csv 形式の受信ファイルのサンプル | [1099entriescsv.csv](https://go.microsoft.com/fwlink/?linkid=862266) |

タスク ガイドを再生していない場合は、上記のタスク ガイドを完了するために必要な次のファイルをダウンロードしてください。現在の Finance and Operations アプリケーションの **外部ファイルから電子申告にデータをインポートするのに必要なコンフィギュレーションの ER 作成**。

| 肩書き                  | ファイル名                                                       |
|------------------------|-----------------------------------------------------------------|
| ER モデル構成 | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |