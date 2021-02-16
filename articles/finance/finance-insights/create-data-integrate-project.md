---
title: データ インテグレーター プロジェクトの作成 (プレビュー版)
description: このトピックでは、データインテ グレータープロジェクトの作成方法について説明します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: fb17d5e82709a34ff088774d9e9034adb714b58c
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646256"
---
# <a name="create-a-data-integrator-project-preview"></a>データ インテグレーター プロジェクトの作成 (プレビュー版)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

このトピックでは、データインテ グレータープロジェクトの作成方法について説明します。

1. Microsoft Dynamics 365 Finance にサインインします。
2. **ワークスペース \> データ管理** に移動し、**データ エンティティ** を選択します。 すべてのデータ エンティティが更新されるまで待機し、次のステップに進みます。
3. [Power Appsポータル](https://make.powerapps.com/)を開き、次 の手順を実行します。

    1. 適切な環境を選択します。
    2. 左側のナビゲーション ペインで、**データ \> 接続** を選択します。
    3. 次の項目の適切なインスタンスに接続します :

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

4. [Power Apps 環境](https://admin.powerapps.com/environments)を開き、次の手順を実行します。

    1. **データ インテグレーター** を選択します。
    2. **接続設定** タブを選択します。
    3. **新規接続設定** を選択します。
    4. 接続の名前を入力します。
    5. 次の項目に対して適切な接続を選択します。

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

    6. 適切な組織のマッピングを選択します。
    7. **作成** を選択します。

5. [Power Apps 環境](https://admin.powerapps.com/environments)を開き、次の手順を実行します。  

    1. 作成した接続セットを使用して、次のテンプレートのデータ統合プロジェクトを作成します。

        - 顧客支払分析情報の結果 (CD から Fin と Ops)
        - キャッシュ フロー時系列の結果 (CD から Fin と Ops)
        - 予算時系列の結果 (CD から Fin と Ops)

    2. プロジェクトごとに適切なスケジューリングを設定します。

> [!NOTE]
> 必要なエンティティが CDS に表示されない場合は、**与信と回収 > 設定 > Finance insights > Finance insights パラメーター** に移動し、顧客支払予測機能を有効にし、**予測モデルの作成** ボタンをクリックします。 AI モデルの配置 (成功、失敗を問わない) が完了すると、統合の作成に必要な CDS エンティティが CDS にデプロイされます。

## <a name="privacy-notice"></a>プライバシー通知

プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。