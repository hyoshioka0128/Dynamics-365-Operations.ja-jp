---
title: Lifecycle Services (LCS) 内での構成マネージャー
description: Microsoft Dynamics Lifecycle Services の構成マネージャー (ベータ) 機能を使用すると、Microsoft Dynamics AX 2012 R3 の 1 つのインスタンスから他のインスタンスに構成をコピーすることができます。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012, Operations
ms.custom: 62753
ms.assetid: fab3f6cf-03db-47c7-90fb-f8bc03dacf49
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 3ed0d85e7c95205781b2e5dc418b4117b8c8ed35
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850685"
---
# <a name="configuration-manager-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) 内での構成マネージャー

[!include [banner](../includes/banner.md)]

構成マネージャーを使用すると、以下の条件を満たす Dynamics AX 2012 R3 環境間で相互にコピーを実行することができます。
-   Lifecycle Services プロジェクトの一部として管理
-   システム診断の実行
-   データのインポート/エクスポート フレームワークの実行中

| **重要**                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| この機能は、運用上の用途ではサポートされて**いません**。  構成マネージャー (ベータ) は、環境内のデータのインポート/エクスポート フレームワークからのエンティティに依存します。 これらのエンティティには現在 AX 2012 R3 のすべての機能が含まれていないため、一部の構成データは環境間でコピーされません。 |

詳細については、以下を参照してください。
-   [構成マネージャーの設定 (Lifecycle Services、LCS)](set-up-configuration-manager-lcs.md)
-   [コンフィギュレーションのコピー (Lifecycle Services、LCS)](copy-configuration-lcs.md)





