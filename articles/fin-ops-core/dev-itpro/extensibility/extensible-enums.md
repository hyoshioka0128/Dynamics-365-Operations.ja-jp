---
title: 拡張可能列挙の書き込み
description: このトピックでは、拡張可能列挙を書き込む方法について説明します。
author: smithanataraj
manager: AnnBe
ms.date: 09/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: smithanataraj
ms.search.validFrom: 2018-09-09
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: 39bcee8e17d7b744a8f9ee49323b702183d12c0a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191632"
---
# <a name="write-extensible-enums"></a>拡張可能列挙の書き込み

[!include [banner](../includes/banner.md)]

列挙を拡張可能にするには、以下の列挙プロパティを設定します。

- Is Extensible = True
- UseEnumValue = No

これらのプロパティを設定する場合、下位の実装者がより多くの要素で列挙を拡張することができます。 要素の値は、展開時に決定され、システム間で同じになりません。 ただし、次の動作が確認されます。

+ データ アップグレード スクリプトは必要ありません。 列挙値は、拡張される列挙に関係なく、データベースに保存されます。 したがって、列挙が拡張可能になると、すべてのシステムで使用されている列挙が優先されます。
+ 列挙の最初の要素は、0 (ゼロ) の値を取得します。 したがって、拡張可能列挙は **not** 演算子にも使用できます。 唯一の例外は、列挙が拡張可能になる前に、列挙の最初の要素がゼロ以外の値を持っていた場合です。
    
## <a name="using-extensible-enums-in-code"></a>コードでの拡張可能列挙の使用
列挙値は開発者により制御されなくなったため、列挙値に関する確実性はありません。 コードで拡張可能列挙を使用する場合は、比較で拡張可能列挙を使用することはできない点に注意してください。 たとえば、**MyEnum::Value1 \> MyEnum::Value2** などです。

さらに、整数と列挙の間のすべての変換を探します。 たとえば、ビューとクエリのモデル化された範囲、比較を使用するか比較でハードコード化された整数値を使用してコードから作成したクエリ (**\<** や **\>** など) などです。

モデルと依存しているすべてのモデルをコンパイルすると、比較および整数への変換がコンパイラによってエラーとして検出されます。
    
列挙値が使用されているロジックがで**小さなメソッド**で抽出されることを確認します。 この方法により、コマンド チェーン (CoC) を使用する拡張が、追加された列挙値を処理できます。

インスタンス化が列挙値に基づいている**構築**メソッドの場合、可能な場合は必ず切り替えブロックを **SysExtension** に置き換えます。 それ以外の場合、既定のブロックが拡張可能であることを確認します。 例については、**PurchRFQCaseCopying** クラスを参照してください。

列挙が**切り替えブロック**で使用される場合、拡張可能ではないスローを持つか持たない既定のブロックを回避します。 列挙値に**長い切り替えケース ブロック**または **if...else ブロック**がある場合、列挙に関連する特定のロジックを処理するクラス階層を作成することを検討します。 例については、**PriceGroupTypeTradeAgreementMapping** クラス階層を参照してください。

列挙値を使用するクエリ範囲に **in** キーワードを使用し、**in** キーワードが使用するコンテナーを拡張可能にします。

## <a name="potential-issues"></a>潜在的な問題
いくつかの列挙では、要素が特定の順序または特定の値を持つ必要があり、拡張可能にすることはできません。 これは、ドラフト、承認済み、完了、またはアーカイブなど、値が論理的な連続する順序を表すステータス列挙の可能性があります。 別の列挙またはタブページ コントロールの番号など、別のコンポーネントと一致する固定整数値が値に必要な列挙の可能性もあります。   

いくつかの列挙には、多くの要素があります。 列挙は、最大 250 の要素をサポートします。 列挙に多くの要素がある場合 (100 を超えるなど)、列挙を拡張可能にするのではなく、ソリューションを再設計することを検討します。 列挙が拡張可能である場合、後で要素を追加すると、追加が制限を超える可能性があるため、顧客の結合ソリューションが壊れる可能性があります。