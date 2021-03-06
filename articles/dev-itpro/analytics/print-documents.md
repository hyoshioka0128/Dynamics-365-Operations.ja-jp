---
title: ドキュメント印刷
description: Microsoft Dynamics 365 for Finance and Operations では、ローカル プリンターまたはネットワークに接続されたデバイスのいずれかを使用してドキュメントを印刷できます。 この記事では、ドキュメントの印刷方法の概要を提供します。
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbc45865b55b4794202408ca19a0776440382fdd
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850074"
---
# <a name="document-printing"></a>ドキュメント印刷

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations では、ローカル プリンターまたはネットワークに接続されたデバイスのいずれかを使用してドキュメントを印刷できます。 この記事では、ドキュメントの印刷方法の概要を提供します。

## <a name="printing-overview"></a>印刷の概要

Microsoft Dynamics 365 for Finance and Operations は、事業活動をサポートするドキュメントの生成、保存、配布を簡単にする統合サービスおよびクライアント アプリケーションを提供します。 Finance and Operations では、ローカル プリンターまたはネットワークに接続されたデバイスのいずれかを使用してドキュメントを印刷できます。 さらに、PDF ファイルまたは Microsoft Office ドキュメントとして、Finance and Operations ページおよびクライアントから直接レポートをエクスポートできます。 最後に、作業負荷の分散は、ネットワーク リソースを使用して、モバイル デバイスから直接ビジネス ドキュメントを印刷できるようにします。 印刷要件が異なる場合がありますが、すべての業界は通常 Finance and Operations を使用してビジネス ドキュメントのハード コピーを作成する必要があります。 ホストされているアプリケーションからネットワーク デバイスでドキュメントを印刷すると、課題の一意のセットが表示されます。 次にいくつか例を挙げます。

- プリント ドライバーは、ユーザーのデバイスで使用できない場合があります。
- ユーザーのデバイスは、会社のネットワークに接続していない可能性があります。

専用のホストを使用して簡単な手順に従うことにより、ユーザーがネットワーク デバイス上のビジネス アプリケーションから直接印刷できるように、システム管理者は配置をコンフィギュレーションすることができます。

### <a name="printing-scenarios-in-finance-and-operations-applications"></a>Finance and Operations アプリケーションでの印刷シナリオ

次の表では、Finance and Operations アプリケーションでの、3 つの主な印刷シナリオについて説明します。

| シナリオ                        | 目標                                                      | ソリューション |
|---------------------------------|-----------------------------------------------------------|----------|
| 1. 表示される内容の印刷        | 現在ブラウザに表示されている内容を印刷します。             | Web ページの「プリント フレンドリー」バージョンがブラウザーで生成されます。 |
| 2. 対話型の印刷         | ローカルに接続されたデバイスで正確なドキュメントを印刷します。 | レポートの PDF 形式をエクスポートし、ブラウザーにダウンロードできます。 |
| 3. ネットワーク デバイスで印刷 | ドメイン プリンター デバイスに正確なドキュメントを送信します。     | 正確なドキュメントは、顧客のドメイン内でホストされるサーバーで実行するクライアント アプリケーションに送信されます。 |

シナリオによってソリューションが異なるため、Finance and Operations アプリケーションは組み込みサービスおよびユーザーがその目標を達成するのためのツールを提供します。

- **シナリオ 1** は HTML5 クライアントのブラウザーの表示によってサポートされています。
- **シナリオ 2** はクライアント アプリケーションおよび Microsoft Office 365 サービスを使用します。
- **シナリオ 3** には、クライアント アプリケーションからおよび Microsoft Azure でホストされているサービスからのサポートが必要です。

Azure サブスクリプションに配置されているプラットフォームに加えて、Finance and Operations アプリケーションは顧客に、統合された、ドキュメントを印刷するためドメインでホストされるデバイスをより使いやすくする当事者 Azure アプリケーションを提供します。

## <a name="service-overview"></a>サービスの概要
ホストされるアプリケーションによって生成されるドキュメントが、ネットワークに接続されたデバイスで印刷されるのを待機している間に、Azure BLOB ストレージに保存されます。 [ドキュメント回覧エージェント](install-document-routing-agent.md) は Azure 認証を使用して、Azure サービスへのセキュリティで保護されたチャネルを確立します。

**実行順序**

1. レポートは Microsoft SQL Server Reporting Services (SSRS) によって生成され、Azure BLOB ストレージに保存されます。 関連付けられているプリンター設定は、ドキュメントと共に保存されます。
2. ドキュメント回覧エージェントは、有効なジョブの Azure サービス バス キューを問い合わせます。
3. ドキュメントがドキュメント回覧エージェントによってダウンロードされ、そのネットワーク プリンターにスプールされます。

クライアント ベースのソリューションは、顧客が印刷ニーズに合わせてスケールを管理できるようにします。 重いボリュームの印刷作業負荷を持つ顧客は、多くのドキュメント回覧エージェントをインストールして、同時印刷操作の数を増やすことができます。 または、一部の顧客は、予想される印刷ニーズに対応するため、ドキュメント回覧エージェントの極めて少ないインストールを必要とします。

### <a name="service-components-for-network-printing"></a>ネットワーク印刷のサービス コンポーネント

次の図は、ネットワーク印刷操作のサポートに役立つ基本的なコンポーネントを示します。

[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)

複数のドキュメント回覧エージェントを使用して単一のプリンターを登録できることに注意してください。 プリンターの基本設定を解決するため、ホストされているサービスは、すべてのネットワーク プリンターを一意に識別するネットワーク パスを使用します。 その結果、プリンターが複数のクライアントにより登録されている場合でも、Finance and Operations アプリケーションで使用可能なプリンターの一覧で単一の選択として表示されます。
