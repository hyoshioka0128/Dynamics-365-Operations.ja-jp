---
title: RCS で使用するアプリケーション メタデータを準備する
description: このトピックの手順では、Regulatory Configuration Service (RCS) の ER モデル マッピング コンフィギュレーションを設計するための Finance and Operations アプリケーションのメタデータを含む、新しい電子レポート (ER) コンフィギュレーションの作成方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1bd2298240fa789762a350e90888201c5a7ce45
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726986"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a>RCS で使用するアプリケーション メタデータを準備する
[!include [task guide banner](../../includes/task-guide-banner.md)]

次の手順では、システム管理者または電子報告開発者ロールのユーザーが、Regulatory Configuration Service (RCS) の ER モデル マッピング コンフィギュレーションを設計するための Microsoft Dynamics 365 for Finance and Operations アプリケーションのメタデータを含む、新しい電子レポート (ER) コンフィギュレーションを作成する方法について説明します。 このコンフィギュレーションは、対外貿易トランザクションにアクセスするためのサンプル ER モデル マッピング コンフィギュレーションを設計するために使用されます。 この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。これらの手順はすべての会社で実行することができます。 これらの手順を完了するには、まず [コンフィギュレーション プロバイダーを作成し、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) のトピックにある手順を完了する必要があります。

## <a name="prerequisites"></a>必要条件
1.  **組織管理** > **ワークスペース** > **電子申告**の順に移動します。 
2.  サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、**アクティブ**としてマークされていることを確認します。 このコンフィギュレーション プロバイダーが表示されない場合は、[コンフィギュレーション プロバイダーを作成し、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) という手順のステップを完了する必要があります。 
3.  **メタデータ コンフィギュレーション**をクリックします。 
4.  対外貿易ビジネスのドメインからの情報を含む電子ドキュメントを生成する Finance and Operation アプリケーションの ER ソリューションを設計するために RCS を使用することを想定しています。 ER データ モデルと必要なデータ ソース間のマッピングを指定するには、RCS で Finance and Operation アプリケーションのメタデータにアクセスできる必要があります。 そのため、ER ソリューション設計の一部として、選択したビジネス ドメインに対する生成 ER レポートに現在必要とされるすべてのメタデータを含む、新しい ER メタデータ コンフィギュレーションを構成します。 

## <a name="add-metadata-configuration"></a>メタデータ コンフィギュレーションの追加 
1.  **コンフィギュレーションの作成**をクリックして、ドロップ ダイアログを開きます。 
2.  **名前**フィールドに、「対外貿易メタデータ」と入力します。 
3.  **コンフィギュレーションの作成**をクリックします。 
4.  **デザイナー** をクリックします。 
5.  **追加**をクリックします。 
  
> [!NOTE]
> アプリケーション全体、選択したモデル、または選択したモジュールのすべてのメタデータを選択することができます。 この場合、レコードのテーブル、列挙体、および拡張データ型のメタデータが自動的に追加されことに注意してください。 メタデータの追加のタイプが必要な場合、手動で追加する必要があります。 
 
メタデータ項目を手動で選択することにより、一部の対外貿易トランザクションがメタデータに関連付けられています。 
  
6.  **データ ソースの追加**をクリックします。 
7.  **テーブルのレコード**をクリックします。 
8.  クイック フィルターを使用し、「Intrastat」の値で**名前**フィールドをフィルターします。 
9.  **イントラスタット** テーブル レコードを選択します。 
10. **OK**をクリックします。
  
Intrastat のレコード テーブルに関するメタデータ情報を追加しました。 
  
11. ツリーで、**テーブルのレコード Intrastat**\>**Relations** を展開します。 
12. ツリーで、**テーブルのレコード Intrastat**\>**Relations\IntrastatCommodity (テーブル レコード EcoResCategory)** を選択します。   
13. **メタデータの追加**をクリックします。 
  
> [!NOTE]
> 選択したレコード テーブルに必要な関係に関するメタデータは、手動で追加する必要があります。 
  
16. **データ ソースの追加**をクリックします。 
17. **列挙**をクリックします。 
18. クイック フィルターを使用し、「IntrastatDirection」の値で**名前**フィールドをフィルターします。 
19. **IntrastatDirection の列挙**レコードを選択します。 
20. **OK**をクリックします。 
21. **保存**をクリックします。  
22. ページを閉じます。 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a>メタデータ コンフィギュレーションのドラフト バージョンの完了
1.  **状態の変更**をクリックします。 
2.  **完了**をクリックします。 
3.  **OK**をクリックします。 
4.  完了したバージョン **1** の選択 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a>完了したバージョンのメタデータ コンフィギュレーションをアプリケーションから XML ファイルとしてエクスポートする
1.  **交換**をクリックします。 
2.  **XML ファイルとしてエクスポート**をクリックします。 
3.  **OK**をクリックします。 
    
作成された ER メタデータ コンフィギュレーションは、RCS にインポートすることができ、Finance and Operations の対外取引ビジネス ドメインのメタデータに関する情報のソースとして使用することのできる XML ファイルとして保存されています。 この情報に基づいて、アプリケーション メタデータと ER データ モデルとの間のマッピングを指定することができます。
