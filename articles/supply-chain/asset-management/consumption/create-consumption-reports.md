---
title: 消費レポートの作成
description: このトピックでは、資産管理で消費レポートを作成する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eecfb101af9a91f515aab221181c54d53e358a68
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652428"
---
# <a name="create-consumption-reports"></a>消費レポートの作成

[!include [banner](../../includes/banner.md)]

 

資産管理の作業指示書で消費登録を作成および転記すると、消費の詳細を表示する 2 つのレポートが使用できるようになります。


## <a name="asset-consumption-report"></a>資産消費レポート

作業指示書で消費を転記した場合、資産消費レポートを印刷できます。 このレポートには、時間、時間原価、品目原価、および資産に転記された経費が表示されます。

1. **資産管理** > **レポート** > **資産** > **資産消費**の順にクリックします。

2. **資産消費**ダイアログでは、該当するトグル ボタンで**はい**を選択して表示するパラメータおよび詳細レベルを選択し、**表示**セクションで機能的な場所レベルを挿入します。
    - **レベル** フィールドを使用すると、機能の場所に関する資産明細行の詳細度を指定できます。 
    
        たとえば、フィールドに数値 "1" を入力し、複数レベルの機能的な場所の構造がある場合、機能的な場所に対するすべての資産が最上位レベルに表示されます。そのため、明細行が下位レベルにある機能的な場所から追加されます。 
        
        **レベル** フィールドに数値 "0" を入力すると、関連するすべての機能の場所レベルのすべての資産を示す詳細結果が表示されます。 
        
    - **すべての下位資産の合計**トグル ボタンで**はい**を選択すると、レポート内の各下位資産の合計が表示されます。

3. **日付**セクションで日付範囲を選択します。

4. **宛先**クイック タブで、レポートを画面に表示するか、印刷するか、またはファイルまたは電子メールとして保存するかを選択します。

5. 必要に応じて、特定の資産を選択してレポートに表示できます。 **対象に含めるレコード** クイック タブで、**フィルター**をクリックし、レポートに含める資産を追加します。

6. **OK** をクリックしてレポートを生成します。


## <a name="work-order-consumption-report"></a>作業指示書の消費レポート

作業指示書で消費を転記した場合、作業指示書の消費レポートを印刷できます。 このレポートには、時間、時間原価、品目原価、および作業指示書に転記された経費が表示されます。

1. **資産管理** > **レポート** > **作業指示書** > **作業指示書消費**の順にクリックします。

2. **作業指示書消費**ダイアログで、**表示**セクションの該当するトグル ボタンで**はい**を選択することにより、レポートに含めるパラメーターを選択します。

3. **日付**セクションで日付範囲を選択します。

4. **宛先**クイック タブで、レポートを画面に表示するか、印刷するか、またはファイルまたは電子メールとして保存するかを選択します。

5. 必要に応じて、特定の作業指示書を選択してレポートに表示できます。 **対象に含めるレコード** クイック タブで、**フィルター**をクリックし、レポートに含める作業指示を追加します。

6. **OK** をクリックしてレポートを生成します。


>[!NOTE]
>また、[作業指示書レポート](../work-orders/work-order-report.md) を生成することもできます。これにはより多くの作業指示の詳細が含まれます。
