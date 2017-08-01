---
title: "キャッシュの概要 Power BI コンテンツ"
description: "このトピックでは、キャッシュの概要 Microsoft Power BI コンテンツについて説明します。 コンテンツに含まれているレポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。"
author: saraschi2
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: e969c2033463d565ce782c7dc8cfc4b458349289
ms.contentlocale: ja-jp
ms.lasthandoff: 06/20/2017

---

# <a name="cash-overview-power-bi-content"></a>キャッシュの概要 Power BI コンテンツ

[!include[banner](../includes/banner.md)]

このトピックでは、**キャッシュの概要** Microsoft Power BI content について説明します。 コンテンツに含まれているレポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。

## <a name="overview"></a>概要

**キャッシュの概要** Power BI コンテンツは、組織内で現金を担当する方のために作成されました。 **キャッシュの概要** Power BI コンテンツは、キャッシュ フローの可視性を提供します。 適切な意志決定を支援するための予測も提供し、キャッシュ フローの正常性が向上します。 黒字額と不足分を把握するために、法人、通貨、および銀行口座ごとにキャッシュを分析できます。

## <a name="accessing-the-power-bi-content"></a>Power BI コンテンツへのアクセス

Dynamics 365 for Finance and Operations, Enterprise Edition 2017 年 7 月の更新プログラムを使用している場合、**キャッシュの概要** Power BI content コンテンツからのレポートは**キャッシュの概要**および**銀行管理**ワークスペースで表示されます。

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI コンテンツに含まれるレポート
次の表は、**キャッシュの概要** Power BI コンテンツの各レポート ページに表示されるメトリックスの詳細について説明しています。

| レポート                                 | コンテンツ |
|---------------------------------------|----------|
| 現金の概要 – すべての会社         | <ul><li>システム通貨の現金収支</li><li>予測される通貨残高</li><li>システム通貨での銀行預金残高の合計</li><li>法人ごとの残高</li><li>銀行口座通貨での、現在の実績対予測残高</li></ul> |
| 現金の概要 – 現在の会社       | <ul><li>会計通貨の現金収支</li><li>予測される通貨残高</li><li>会計通貨での銀行預金残高の合計</li><li>銀行口座通貨での、現在の実績対予測残高</li></ul> |
| 予測されるキャッシュ フロー – すべての会社    | <ul><li>システム通貨の現金収支</li><li>日次予測の集計</li><li>予測の詳細</li></ul> |
| キャッシュ フロー予測 – 会社通貨 | <ul><li>会計通貨の現金収支</li><li>日次予測の集計</li><li>予測の詳細</li></ul> |
| 通貨予測                     | <ul><li>予測される通貨残高</li><li>日次通貨集計</li><li>予測の詳細</li></ul> |
| 銀行預金残高                         | <ul><li>システム通貨での銀行預金残高の合計</li><li>法人ごとの残高</li><li>銀行口座通貨での、現在の実績対予測残高</li><li>銀行口座ごとの残高</li><li>通貨別残高</li></ul> |

## <a name="extending-the-power-bi-content"></a>Power BI コンテンツの拡張
Lifecycle Services (LCS) で利用できるコンテンツ パックを使用して、Dynamics 365 にログインしない人に優れた分析を提供できます。 他のレポートまたはビジュアルを含めるよう、これらのコンテンツ パックを変更できます。次いで分析のためにコンテンツ パックを Power BI.com テナントに発行します。 

LCS の共有資産ライブラリに **現金の概要** Power BI コンテンツがあります。 コンテンツのダウンロード方法および組織で実装する方法の詳細については、「[Microsoft およびパートナーからの LCS での Power BI コンテンツ](/dynamics365/unified-operations/dev-itpro/analytics/power-bi-content-microsoft-partners)」を参照してください。 Power BI コンテンツの実装方法を示すデモを視聴するには、「[Microsoft の Power BI コンテンツおよび Dynamics Lifecycle Services のパートナー](https://mix.office.com/watch/9puyb1b2xs1w)」の Office Mix を参照してください。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解

次の表に、**現金の概要** Power BI コンテンツが基づいているエンティティを示します。

| エンティティ                                                                          | コンテンツ |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | レポートをフィルター処理する会社 |
| LedgerCovLiquidityMeasurement\_Date                                             | レポートをフィルター処理する日付 |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | 実際の口座残高対最後に予測した銀行預金残高 |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | 予測トランザクションの詳細 |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | 各会社の会計通貨を使用したキャッシュ インフロー、アウトフロー、および残高 |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | 全ての会社に関して、システム通貨を使用したキャッシュ インフロー、アウトフロー、および残高 |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | トランザクション通貨を使用した、トランザクション正味金額および通貨残高の集計 |

これらのエンティティは、データ モデルの計算メジャーを作成するために使用されました。 これらの計算メジャーは、**現金の概要** Power BI コンテンツで使用するためのグラフやレポートの計算に使用されます。 レポートおよびダッシュボードに追加の計算を含めるには、LCS から Power BI ファイルをダウンロードして変更できます。 このファイルはコンテンツを作成するために使用された既定のデータ モデルです。 変更後に、追加した情報を含む組織のコンテンツとダッシュボードを作成できます。

