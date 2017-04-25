---
title: "Lifecycle Services の電子申告コンフィギュレーションのダウンロード"
description: "このトピックでは、Microsoft Dynamics Lifecycle Services (LCS)の(ER)電子申告のコンフィギュレーションをダウンロードする方法を説明します。"
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 9dca5dec846670da25926826f59d7bce0fa0dcea
ms.lasthandoff: 03/31/2017


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Lifecycle Services の電子申告コンフィギュレーションのダウンロード

このトピックでは、Microsoft Dynamics Lifecycle Services (LCS)の(ER)電子申告のコンフィギュレーションをダウンロードする方法を説明します。

このチュートリアル ガイドは Microsoft Dynamics Lifecycle Services (LCS) から Electronic reporting (ER) コンフィギュレーションの最新バージョンをダウンロードするプロセスを説明します。

1.  次のロールの 1 つを使用して Dynamics 365 for Operations にサインインします。
    -   電子申告開発者
    -   電子申告機能コンサルタント
    -   システム管理者

2.  **コンフィギュレーション** ** ** &gt; 電子管理レポートが実行されます。
3.  [**コンフィギュレーション プロバイダー**] セクションで、[**Microsoft**] タイルを選択します。
4.  [**Microsoft**] タイルで [**リポジトリ**] をクリックします。 [![更新]ーからlcsに対してMR開MRリポジトリ リスト] (。/media/updateからのーlcsに対してMR開MRリポジトリList.png) ] (。/media/updateからのーlcsに対してMR開MRリポジトリlist.png) 
5.  **コンフィギュレーション リポジトリ** ページのグリッドで、**LCS** タイプの既存のリポジトリを選択します。 このリポジトリがグリッドに表示されない場合は、次の手順に従います。
    1.  [**追加**] をクリックして新しいリポジトリを追加します。
    2.  リポジトリ タイプとして、[**LCS**] を選択します。
    3.  [**リポジトリの作成**] をクリックします。
    4.  リポジトリの名前と説明を入力します。
    5.  [**OK**] をクリックして、新しいリポジトリ エントリを確認します。
    6.  グリッドで、[**LCS**] タイプの新しいリポジトリを選択します。

6.  [**開く**] をクリックして、選択したリポジトリの ER コンフィギュレーションの一覧を表示します。 [![更新]ーからlcsに対してMRコンフィギュレーションlcsリポジトリ] (。/media/updateからのーlcsに対してMRコンフィギュレーションlcs repository.png) ] (。/media/updateからのーlcsに対してMRコンフィギュレーションlcs repository.png) 
7.  左ウィンドウのコンフィギュレーション ツリーで必要な ER コンフィギュレーションを選択します。
8.  [**バージョン**] クイック タブで、選択した ER コンフィギュレーションの必要なバージョンを選択します。
9.  [**インポート**] をクリックして、LCS から現在の Dynamics 365 for Operations インスタンスに選択したバージョンをダウンロードします。 **注: ** [**インポート**] ボタンは、現在の Dynamics 365 for Operations インスタンスにある ER コンフィギュレーション バージョンでは使用できません。 ![[更新]ーからlcsに対してMRダウンロード コンフィギュレーション] (。/media/updateからのーlcsに対してMRダウンロードConfiguration.png) ] (。/media/updateからのーlcsに対してMRダウンロードconfiguration.png) 

**注:** ER の設定に応じて、コンフィギュレーションはインポートされた後に検証されます。 不整合の問題が検出されると、通知を受け取る場合があります。 インポートしたコンフィギュレーションのバージョンを使用する前に、それらの問題を解決する必要があります。 詳細については、このトピックについては、関連記事の一覧を表示します。

<a name="see-also"></a>参照
--------

[電子申告の概要](general-electronic-reporting.md)

