---
title: 小売階層
description: この記事は、Microsoft Dynamics 365 for Retail の小売階層について説明します。
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 198c8da336f3e225c5d6da2eb02c86581dc9b4d6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568025"
---
# <a name="retail-hierarchies"></a>小売階層

[!include [banner](includes/banner.md)]

この記事は、Microsoft Dynamics 365 for Retail の小売階層について説明します。

小売カテゴリ階層を作成して、小売チャンネルを使用して販売する製品を整理することができます。 小売製品階層を使用して、製品を分類またはグループ化できます。 その後、これらの製品を使用して、製品の品揃えと顧客ロイヤルティ プログラムを作成できます。 また、製品の属性またはプロパティの割り当て、価格決定構造の割り当て、製品プロモーションへの製品の挿入、およびレポートでの製品の使用を行うこともできます。 1 つの小売カテゴリ階層を作成して組織のすべての製品およびカテゴリを表し、複数の目的にその小売カテゴリ階層を使用することができます。 また、製品のプロモーションなどの特殊な目的に複数の小売カテゴリ階層を作成できます。 小売製品階層を作成する際に、カテゴリ階層の目的を識別するためにカテゴリ階層タイプを割り当てる必要があります。 たとえば、**小売のナビゲーション階層**タイプが割り当てられている製品階層のみが、製品をカテゴリごとにオンラインで、または販売時点管理 (POS) で表示する場合に参照されます。

## <a name="retail-hierarchy-types"></a>小売階層のタイプ

次の表に、使用できる小売カテゴリ階層のタイプと各タイプの一般的な目的を示します。

| カテゴリ階層タイプ       | 目的 |
|-------------------------------|---------|
| 小売製品階層      | 組織の全体的な製品階層を定義するには、この階層タイプを使用します。 販売促進、価格決定とプロモーション、および品揃え計画にこの階層タイプを使用できます。 1 つの小売階層にのみこの製品グループ タイプを割り当てることができます。 |
| 補助小売階層 | 作成する追加の小売カテゴリ階層の場合には、このタイプを使用します。 たとえば、春に水着のプロモーションがあります。 したがって、別のカテゴリ階層に水着製品を追加し、さまざまな製品カテゴリにプロモーション用の価格決定を適用します。 |
| 小売ナビゲーション階層   | この階層タイプを使用すると、製品をグループ化してカテゴリに整理し、製品がオンラインまたは POS で閲覧できるようになります。 |

小売カテゴリ階層を使用して製品を構造化することで、製品の属性およびプロパティをカテゴリ レベルで設定および管理できます。 これらの属性およびプロパティには、製品分析コードおよび POS の設定が含まれます。 そのカテゴリに割り当てる製品は、定義するプロパティと属性を自動的に継承します。 また、選択したカテゴリの複数の製品に、製品のプロパティ設定を同時にコピーできます。
