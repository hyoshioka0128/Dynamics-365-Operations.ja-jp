---
title: Microsoft Flow 内のビジネス イベント
description: このトピックでは、Finance and Operations コネクタを介して Microsoft Flow での消費に使用可能なビジネス イベントに関する情報を提供します。
author: Sunil-Garg
manager: AnnBe
ms.date: 07/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: sunilg
ms.search.validFrom: Platform update 24
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: 09d3d4013b960be87f12e227ff6c2ae95efabe62
ms.sourcegitcommit: 739a4f4f7dcfbdbe47e2bcf35db24ccbf6336b35
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/19/2019
ms.locfileid: "1773834"
---
# <a name="business-events-in-microsoft-flow"></a>Microsoft Flow 内のビジネス イベント

[!include[banner](../includes/banner.md)]

ビジネス イベントは Microsoft Finance and Operations コネクタを介して Microsoft Flow で消費することができます。  Finance and Operations コネクタには **ビジネス イベントが発生した場合** という名前のトリガーがあります。 このトリガーは、Microsoft Dynamics 365 for Finance and Operations のターゲット インスタンスで使用可能なビジネス イベントの購読に使用することができます。

## <a name="prerequisite"></a>前提条件

ビジネス イベントについて理解することは重要です。 詳細については[ビジネス イベント](home-page.md) のドキュメントを参照してください。

> [!IMPORTANT]
> ビジネス イベントは以前のプラットフォーム リリースでは使用可能でないため、**ビジネス イベント発生時** トリガーは、Platform update 24 またはそれ以降を実行する Finance and Operations インスタンスでのみ動作します。

## <a name="subscribing-to-business-events-and-unsubscribing-from-them"></a>ビジネス イベントの購読および購読解除

**ビジネス イベント発生時** トリガーをフローに追加した後、以下の情報を提供する必要があります。

- **インスタンス** - ビジネス イベントが発生する Finance and Operations インスタンスのホスト名を指定します。 環境インスタンスは指定されたドロップダウン メニューで利用可能である必要がありますが、環境が一覧表示されていない場合はカスタム値として入力することができます。
- **カテゴリ** - ビジネス イベントのカテゴリを選択します。 **ビジネス イベント** フィールドにそのカテゴリのビジネス イベントが表示されます。
- **ビジネス イベント** - 選択したカテゴリで利用可能なビジネス イベント。
- **法人** - ビジネス イベントが購読されている法人を指定します。 フローは Finance and Operations 内の法人でビジネス イベントが発生するときにトリガーされます。 既定では、このフィールドは空白で、ビジネス イベントは **すべて** の法人で購読されます。

フローが保存されると、選択したビジネス イベントに対するサブスクリプションが環境インスタンスに追加されます。 サブスクリプション プロセスの一部として、必要なエンドポイントが設定され、対応するビジネス イベントが有効にされます。

トリガーまたはフローのいずれかを削除または無効化すると、ビジネス イベントは自動的に購読解除されます。

複数のフローは、同一もしくは異なる法人内の同じビジネス イベントを購読することができます。

> [!NOTE]
> Finance and Operationsでは、Finance and OperationsのFlow エンドポイントを手動で構成しないでください。 上記の説明に従って、エンドポイントはフローから自動的に作成されます。

Microsoft Flow でビジネス イベントを使用する方法については [Microsoft Flow でビジネス イベントを消費する](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/how-to/how-to-flow) を参照してください。 

## <a name="other-ways-to-consume-business-events-in-microsoft-flow"></a>Microsoft Flow 内のビジネス イベントを消費する他の方法

前のセクションでは、Finance and Operations 内でトリガーを使用することにより Microsoft Flow から直接ビジネス イベントを購読する方法について説明しました。 ただし、[Microsoft Flow 用イベント グリッド コネクタ](https://docs.microsoft.com/connectors/azureeventgrid/) を使用することにより、Microsoft Azure Event Grid から Microsoft Flow 内のビジネス イベントを消費することもできます。

実装内の他の統合で既に使用されている場合、イベント グリッドは Microsoft Flow 内のビジネス イベントを消費するための実行可能なアプローチである可能性があります。 同じ法人内のビジネス イベントが複数のフローをトリガする必要がある場合、イベント グリッドからビジネス イベントを消費することを検討する必要があります。

このアプローチは、コネクタが Microsoft Flow 内のビジネス イベントで使用可能である場合、ビジネス イベントのエンドポイントとして使用されるメッセージングまたはイベント プラットフォームに対して適用することができます。
