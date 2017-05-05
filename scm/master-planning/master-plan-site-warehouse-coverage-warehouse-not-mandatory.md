---
title: "マスター プラン - サイトと倉庫の補充、倉庫は必須ではない"
description: "このトピックでは、サイトおよび倉庫の補充分析コードを持つ品目の計画方法について説明します。 倉庫分析コードが必須ではありません。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3671024dc097c94638b1579d7cacc8447c49e97b
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>マスター プラン - サイトと倉庫の補充、倉庫は必須ではない

[!include[banner](../includes/banner.md)]


このトピックでは、サイトおよび倉庫の補充分析コードを持つ品目の計画方法について説明します。 倉庫分析コードが必須ではありません。

このマスター計画シナリオの前提条件を次に示します。

-   サイト分析コードが必須に設定され、需要トランザクションで入力されている。 この設定は変更できません。
-   倉庫分析コードが必須に設定されていない。 倉庫は既知である場合もあるが、マスタ 計画計算には使用されない。
-   サイト分析コードおよび倉庫分析コードが補充計画に対して設定されている。 他の分析コードが補充計画に対して設定されている場合もある。 ただし、これらはマルチサイト機能の影響を受けない。

次の図は、マスター計画がどのように進行するかを示しています。 図の中で使用されているパラメータとその設定場所を次に示します。
-   倉庫は [手動] に設定されています。 [**在庫管理] &gt; [設定] &gt; [在庫詳細] &gt; [倉庫**] の順にクリックします。 [**マスター計画**] クイック タブに、[**手動**] フィールドが表示されます。
-   品目に対して品目補充が定義されています。 [**製品情報管理] &gt; [製品] &gt; [リリースされた製品**] の順にクリックします。 品目を選択し、[アクション ウィンドウ] の [**計画**] タブで、[**品目補充**] をクリックします。
-   倉庫に対して補充関係が定義されています。 [**在庫管理] &gt; [設定] &gt; [在庫詳細] &gt; [倉庫**] の順にクリックします。 [**マスター計画**] クイック タブに、[**主要倉庫**] フィールド グループが表示されます。
-   既定の注文タイプには [生産]、[発注書] または [かんばん] が設定されます。 [**製品情報管理] &gt; [製品] &gt; [リリースされた製品**] の順にクリックします。 品目を選択し、[アクション ウィンドウ] の [**計画**] タブで、[**既定の注文設定**] をクリックします。 [**既定の注文設定**] フォームの [**既定の注文タイプ**] を参照してください。

![サイトと倉庫の補充が必要、倉庫は必須ではない    ](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)

 
-



<a name="see-also"></a>参照
--------

[マスター プランとマルチサイト機能](master-plan-multisite-functionality.md)

[マスター プラン - サイトと倉庫の補充、倉庫は必須](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[マスター プラン - サイトの補充、倉庫は必須](master-plan-site-coverage-warehouse-mandatory.md)

[マスター プラン - サイトの補充、倉庫は必須ではない](master-plan-site-coverage-warehouse-not-mandatory.md)

[マスター プラン - BOM バージョンを決定する方法](master-plan-bom-version-determined.md)



