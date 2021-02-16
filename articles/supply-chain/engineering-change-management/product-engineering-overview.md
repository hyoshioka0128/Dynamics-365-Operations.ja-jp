---
title: エンジニアリング変更管理の概要
description: このトピックでは、製品のバージョン管理の計画と管理を支援し、製品のライフサイクルとエンジニアリング変更を管理するエンジニアリング変更管理の概要を説明します。
author: t-benebo
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: f1aa04b472eaef7ed398f08a05d46bac2d589561
ms.sourcegitcommit: 9f32389715b226c11e74c53547527e0a8b51e300
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514353"
---
# <a name="engineering-change-management-overview"></a>エンジニアリング変更管理の概要

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>機能の概要

今日のメーカーは、製品のライフサイクル、品質と信頼性の要件の高まり、および製品の安全性に重点をおいており、強力な製品データ管理、バージョン管理、およびエンジニアリング変更管理を必要としています。

エンジニアリング変更管理では、製品データ管理プロセスに構造と規範を提供し、ワークフローでサポートされている制御された方法で製品を定義、リリース、および改訂できるようにします。製品のライフサイクル全体にわたって、製品バージョンやエンジニアリング変更管理を通じて文書化、影響の評価、およびエンジニアリング変更の適用を行うことができます。

エンジニアリング変更管理は、製品のバージョン管理の計画と管理を支援し、製品のライフサイクルとエンジニアリング変更を管理するエンジニアリング変更管理に役立ちます。 主な機能を次に示します:

- 製品のバージョン管理
- 強化された製品リリース機能により、1 つの法人 (技術会社) で製品マスター データを管理し、すべてのリリース済製品を他の法人に公開することができます
- 製品バージョンを有効化する前に必要な情報が入力されていることを検証するためのルール (準備完了チェック)
- リリースされた製品を特定の業務プロセスで使用できる時期をきめ細かく制御することにより、製品ライフサイクル管理を強化
- ワークフローでサポートされているエンジニアリング変更要求
- ワークフローでサポートされているエンジニアリング変更指示

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

前のビデオ ([Dynamics 365 Supply Chain Management の変更管理機能](https://youtu.be/N313FqvRuBc)) は、YouTube で利用可能な [Finance and Operations 再生リスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)に含まれています。

## <a name="turn-on-engineering-change-management-for-your-system"></a>システムのエンジニアリング変更管理を有効にします

まず、次の手順に従ってエンジニアリング変更管理を有効にします。

1. [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) に移動します。
1. 更新プログラムを確認します。
1. **エンジニアリング変更管理** という機能を有効にします。

次に、次の手順に従って、**エンジニアリング変更管理** コンフィギュレーション キーを有効にします。

1. [メンテナンス モード](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、システムをメンテナンス モードにします。
1. **システム管理 \> 設定 \> ライセンス コンフィギュレーション** の順にクリックします。
1. **取引** ノードを展開し、**エンジニアリング変更管理** チェックボックスをオンにします。
1. [メンテナンス モード](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、メンテナンス モードをオフにします。