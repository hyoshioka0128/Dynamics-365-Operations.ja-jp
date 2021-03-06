---
title: Lifecycle Services (LCS) でのオンプレミス プロジェクトの設定
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) でオンプレミス プロジェクトを設定するプロセスについて説明します。
author: manalidongre
manager: AnnBe
ms.date: 03/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 60373
ms.assetid: ''
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd4511e7f25c24e4b3ea08ec3c960281874a356c
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850667"
---
# <a name="set-up-on-premises-projects-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) でのオンプレミス プロジェクトの設定

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) を使用して、Microsoft Dynamics 365 for Finance and Operations (オンプレミス) のインスタンスを配置し更新する必要があります。 ボリューム ライセンス フローまたは Dynamics 価格リスト フローを通じてサーバーとユーザーのライセンスを購入した後は、「[Dynamics 365 for Finance and Operations (オンプレミス) の購入](../../fin-and-ops/get-started/purchase-on-premises.md)」を参照して、Azure AD アカウントを作成、または既存の Azure AD アカウントを使用してすべてのサインアップ手順を完了します。 ユーザーは LCS へリダイレクトされ、そこでオンプレミス実装プロジェクトがプロビジョニングされます。

 [![On-premises 実装プロジェクト](./media/lbd-proejcts-01.png)](./media/lbd-proejcts-01.png)

オンプレミス プロジェクトには、オンプレミス ソリューションの実装、保守、および運用に必要なすべてのツールがあります。 オンプレミス プロジェクトで使用可能なツールの一部を次に示します。

- **方法** – オンプレミスの方法は、顧客がオンプレミス プロジェクトを実装および管理するのに役立つベスト プラクティスを提供しています。
- **ビジネス プロセス モデラー** - ビジネス プロセス モデラー (BPM) は、要件をキャプチャし、ギャップ分析に適合するために使用されます。
- **クラウド ホスト環境** - クラウドホスト環境は、開発者の配置とトポロジの構築、およびオンプレミス ソリューションのための Dev Application Lifecycle Management(ALM) の完成に使用されます。
- **コードのアップグレード** - これらのツールを使用して、コードを新しいバージョンにアップグレードできます。
- **問題検索** – アプリケーションとプラットフォームの問題に関連する公開済の KB を検索します。
- **ローカライズおよび翻訳** – 資産のローカライズおよび翻訳。
- **サポート** – ファイルおよびトラック がインシデントをサポートします。
- **プロジェクト ユーザー** – プロジェクトにユーザーを割り当てます。
- **プロジェクト設定** – コネクタ、プロジェクト名、組織ユーザー、ライセンス番号などのプロジェクトレベルの設定を編集します。
- **アセット ライブラリ** - アセット ライブラリは、パッケージなどのさまざまなアセットのライブラリです。
- **SharePoint のオンライン ライブラリ** – オンラインの Microsoft SharePoint ライブラリに接続します。

オンプレミス実装を開始するには、プロジェクトを正しくセットアップし、開発者とビルド環境を展開してから、サンドボックス環境と実稼働環境を展開する方法の手順に従う必要があります。 展開に役立つように、2 つの環境スロットがオンプレミス プロジェクトにあらかじめ割り当てられています。 一方のスロットはサンドボックス環境用で、もう一方のスロットは実稼働環境用です。 これらのスロットは、サービス フロー中に使用され、パッケージが実稼働環境で適用される前にサンドボックス環境でテストされることを保証します。
