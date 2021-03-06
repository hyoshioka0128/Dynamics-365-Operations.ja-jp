---
title: 現金の概要 Power BI コンテンツ
description: このトピックでは、現金の概要 Power BI コンテンツについて説明します。 コンテンツに含まれているレポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。
author: saraschi2
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 553a4a5d25e126923576569b48414c46aab991ec
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842692"
---
# <a name="cash-overview-power-bi-content"></a>現金の概要 Power BI コンテンツ

[!include [banner](../includes/banner.md)]

このトピックでは、**現金の概要** Microsoft Power BI コンテンツについて説明します。 コンテンツに含まれているレポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。

## <a name="overview"></a>概要

**現金の概要** Power BI コンテンツは、組織内で現金を担当する方のために作成されました。 **現金の概要** Power BI コンテンツは、キャッシュ フローの可視性を提供します。 適切な意志決定を支援するための予測も提供し、キャッシュ フローの正常性が向上します。 黒字額と不足分を把握するために、法人、通貨、および銀行口座ごとにキャッシュを分析できます。

## <a name="setup-needed-to-view-power-bi-content"></a>Power BI コンテンツを表示するための設定

**現金の概要**および**銀行管理** Power BI のビジュアルにデータを表示するには、次の設定を完了する必要があります。

1. **システム管理 > 設定 > システム パラメーター**に移動して、**システム通貨**および**システム為替レート**を設定します。
2. **総勘定元帳 > 設定 > 元帳**に移動して、**会計通貨**および**為替レート タイプ**を設定します。
2. トランザクション通貨と会計通貨、会計通貨とシステム通貨、および会計通貨と銀行通貨の間の為替レートを定義します。 これを行うには、**総勘定元帳 > 通貨 > 通貨の為替レート**に移動します。
3. キャッシュ フロー予測をコンフィギュレーションおよび実行します。 キャッシュ フロー予測の設定方法の詳細については、<a href="https://docs.microsoft.com/dynamics365/unified-operations/financials/cash-bank-management/cash-flow-forecasting
">キャッシュ フロー予測</a>を参照してください。 
4. **システム管理 > 設定 > エンティティ格納**に移動して、**LedgerCovLiquidityMeasurement** 集計測定を更新します。

## <a name="accessing-the-power-bi-content"></a>Power BI コンテンツへのアクセス

**現金の概要** Power BI コンテンツからのレポートが、**現金の概要**および**銀行管理**ワークスペースで表示されます。

データでキャッシュ フロー予測レポートを表示するには、まず、現金および銀行管理領域から**キャッシュ フロー予測の計算** 機能を使用して、予測計算プロセスを実行する必要があります。  これは、予測に含める会社ごとに完了する必要があります。  **エンティティ格納** ページで LedgerCovLiquidityMeasurement 集計の測定を更新する必要があります。  

説明するには、**データの生成** ページをデモ データ モジュールから使用し、キャッシュ フロー予測デモ データを追加できます。  このスクリプトは、キャッシュ フロー予測テーブルにデータを挿入して、レポートに必要な情報をすばやく入力します。  このモジュールは、デモ データ スイート モデルが環境に展開されている場合にのみ使用できます。 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI コンテンツに含まれるレポート

次の表は、**現金の概要** Power BI コンテンツコンテンツの各レポート ページに表示されるメトリックスの詳細について説明しています。

| レポート                                 | コンテンツ |
|---------------------------------------|----------|
| 現金の概要 – すべての会社         | <ul><li>システム通貨の現金収支</li><li>予測される通貨残高</li><li>システム通貨での銀行預金残高の合計</li><li>法人ごとの残高</li><li>銀行口座通貨での、現在の実績対予測残高</li></ul> |
| 現金の概要 – 現在の会社       | <ul><li>会計通貨の現金収支</li><li>予測される通貨残高</li><li>会計通貨での銀行預金残高の合計</li><li>銀行口座通貨での、現在の実績対予測残高</li></ul> |
| 予測されるキャッシュ フロー – すべての会社    | <ul><li>システム通貨の現金収支</li><li>日次予測の集計</li><li>予測の詳細</li></ul> |
| キャッシュ フロー予測 – 会社通貨 | <ul><li>会計通貨の現金収支</li><li>日次予測の集計</li><li>予測の詳細</li></ul> |
| 通貨予測                     | <ul><li>予測される通貨残高</li><li>日次通貨集計</li><li>予測の詳細</li></ul> |
| 銀行預金残高                         | <ul><li>システム通貨での銀行預金残高の合計</li><li>法人ごとの残高</li><li>銀行口座通貨での、現在の実績対予測残高</li><li>銀行口座ごとの残高</li><li>通貨別残高</li></ul> |


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
