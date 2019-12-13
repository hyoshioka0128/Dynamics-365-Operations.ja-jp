---
title: AX 2012 からのアップグレード - 機能テスト パス
description: このトピックでは、機能テスト パスを実行して、アップグレードされた Finance and Operations と環境を検証する方法について説明します。
author: tariqbell
manager: AnnBe
ms.date: 01/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 39622bb696c0b4a1e5f508241fe832a364f23d6b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191874"
---
# <a name="upgrade-from-ax-2012---functional-test-passes"></a>AX 2012 からのアップグレード - 機能テスト パス

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

データのアップグレードが完了した後、すべての業務プロセスの完全な機能テスト パスを完了しておくことをお勧めします。 完全な機能テスト パスでは、Finance and Operations を使用して実行されるすべての業務プロセスの広範な再テストを実行します。 テストには、Microsoft Dynamics AX 2012 から引き継がれたプロセスと Finance and Operations の機能を使用する新しいプロセスの両方を含める必要があります。

コードの品質によっては、バグ修正と再テストのために機能テスト パスを何回か繰り返さなければならない可能性があります。 バグが修正された後、関係するすべてのプロセスを再テストするために注意し、変更によって下流または上流プロセスが影響を受けないようにします。

## <a name="old-data-vs-new-data"></a>新しいデータ対古いデータ

実行するテストの一覧を作成するときは、新しいデータと対比して古いデータの影響を考慮します。 このタイプのテストは、データ関連のバグを発見するのに役立ちます。 古いデータと新しいデータを作成したコードは非常に異なっている可能性があります。この違いは、バグの共通の根本原因になる可能性があります。

たとえば、テストしている業務プロセスが発注書の取消である場合、新しいシステムにアップグレードされる前に開始された発注書を取消できますか。 新しいシステムへのアップグレード後に開始された発注書もキャンセルすることができますか。 

ここでは非常に単純な例を使用しましたが、システム内では多くのビジネス プロセスが連結していて、古いデータに対する新しいデータの効果が累積されるため、テスト要件がより複雑になることがあります。

たとえば、生産テスト フローのステージを紹介します。

1. 品目マスターは設計され、法人にリリースされます。
2. 在庫品目要求が作成されます。
3. 製造オーダーが生成されます。
4. 発注書が生成されます。
5. 製造オーダーの処理が発生します (作業現場)。
6. 仕入先支払 (発注書の支払) などが発生します。

この生産テスト フローでは、新しいレコードまたは古いレコードのいずれかを入力として使用することで各ステージを実行することができます。 結果は、古いデータと新しいデータのすべての組み合わせをカバーする一連のテストです。 いくつかのプロセスでは、テスト マトリックスは過剰に思われますし、実際に過剰である可能性があります。 したがって、最も多く使用されると予測される特定の組み合わせに焦点を当てることができます。 ただし、何に対応していないかを把握することも役立ちます。 所持しているもの、テストで最も焦点を当てるもの、焦点を当てないものを把握する場合に、連続した意思決定を行います。
