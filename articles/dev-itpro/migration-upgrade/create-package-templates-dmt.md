---
title: AX 2009 の移行 － テンプレートの作成
description: このトピックでは、Microsoft Dynamics AX 2009 から Microsoft Dynamics 365 for Finance and Operations へデータを移行するために使用できるパッケージ テンプレートを作成する方法について説明します。
author: kfend
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.openlocfilehash: 8d9ccf2cf1bc060fe519c1857bc1f1854696d7f4
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851748"
---
# <a name="ax-2009-migration--create-package-templates"></a>AX 2009 の移行 － パッケージ テンプレートの作成

[!include [banner](../includes/banner.md)]

パッケージを作成するには、事前に定義された順序に従います。 この順序は、データ エンティティが互いに持つ依存関係に基づいています。 これらの依存関係のため、Microsoft Dynamics 365 for Finance and Operations にデータ エンティティをインポートするときは、定義されている順序でデータ エンティティをインポートする必要があります。 そうしないと、インポートおよびコンフィギュレーション中に問題が発生する可能性があります。

データ移行ツール (DMT) には、次の図に示すように、20 の事前に定義されたテンプレートが用意されています。

[![データ エンティティ インポート テンプレートの一覧](./media/data-entity-templates.png)](./media/data-entity-templates.png)

既存のテンプレートをカスタマイズできます。または、必要に応じて、独自のテンプレートを作成することができます。

この手順に従って、移行用のテンプレートで使用されるエンティティの一覧を表示して選択します。

1. Microsoft Dynamics AX 2009 で、**データ移行** \> **共通フォーム** \> **エンティティ リスト**を順にクリックしてから、**順序の適用** をクリックします。 メッセージ ボックスを閉じます。
2. 正しい法人が選択されていることを確認し、**表示** フィールドで、すべてのエンティティまたは移行のために考慮すべきエンティティのみのいずれを表示するかを選択します。
3. **テンプレート名** フィールドで、テンプレートを選択します。
4. **選択されているモジュール** ウィンドウで、移行するデータ エンティティを含むモジュールを選択します。
5. **エンティティの詳細** タブで、移行するすべてのエンティティ行の **移行対象として選択** チェック ボックスをオンにします。
6. **順序の適用** をクリックします。
7. カスタマイズされたテンプレートを作成するには、アプリケーション オブジェクト ツリーで、**リソース** に移動し、XML 形式で新しいテンプレートを作成します。
