---
title: ワークフロー タイプのクエリの作成
description: このトピックでは、ワークフロー タイプのクエリを作成する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: 202694
ms.assetid: 33349e0d-d8ac-4d20-8f9b-5f85d4e01004
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 06b83be6e870f374433b278c2943d9a1d3e991ce
ms.sourcegitcommit: 4fd51830be21b95a1398dc80d5429a74bcec73fc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/09/2019
ms.locfileid: "1736965"
---
# <a name="create-a-query-for-a-workflow-type"></a>ワークフロー タイプのクエリの作成 

[!include [banner](../includes/banner.md)]

ワークフロー タイプを作成する前に、ワークフロー ドキュメントのテーブル フィールドにアクセスするクエリを作成する必要があります。 このトピックでは、ワークフロー タイプのクエリを作成する方法について説明します。

## <a name="create-a-query-for-a-workflow-type"></a>ワークフロー タイプのクエリの作成

1. 新しいクエリを作成するには、次のいずれかのステップを実行します

    + アプリケーション エクスプローラーで、 **クエリ** ノードを右クリックしてから、 **新しいクエリ** を選択します。 クエリ グループは、 **クエリ** ノードの下に表示されます。 新しいクエリを右クリックし、 **名前の変更** を選択します。 クエリの名前を入力します
    + **プロジェクト** メニューの **新しい項目の追加** を選択します。 **新しい項目の追加** ダイアログ ボックスで、 **クエリ** を選択します。 クエリ名を入力し、 **作成** を選択します。

2. 新しいクエリを展開し、 **データ ソース** ノードを右クリックして、 **新しいデータ ソース** を選択します。 データ ソースグ ループは、 **データ ソース** ノードの下に表示されます。
3. 新しいデータ ソース グループを右クリックし、 **プロパティ**  を選択します。
4. **プロパティ** シートで、ワークフローを定義しているドキュメント タイプのメイン テーブルに対して **テーブル** プロパティを設定します。
5. アプリケーション オブジェクト ツリー (AOT) で、新しいクエリを右クリックし、 **保存** を選択します。

クエリの作成方法の詳細については、 [AOTを使用したクエリの作成](https://docs.microsoft.com/dynamicsax-2012/developer/how-to-create-queries-by-using-the-aot) を参照してください。
