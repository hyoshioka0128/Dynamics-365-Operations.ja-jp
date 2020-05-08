---
title: 分散型注文管理 (DOM)
description: このトピックでは、Dynamics 365 Commerce の分散型注文管理 (DOM) の機能について説明します。
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7a584953b0f4961e25b59bca51aa3928b87b2c7c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004323"
---
# <a name="distributed-order-management-dom"></a>分散型注文管理 (DOM)

[!include [banner](includes/banner.md)]

コマース業のあり方が変化する中で、小売企業は、パーソナライズされた顧客エンゲージメント、オムニチャネルのエクスペリエンス、スムーズなやり取りを実現するために力を尽くしています。 選択肢が非常に多くなっているため、消費者は最も快適に利用できるところで買い物をするようになっています。 多くの場合、もはや消費者が購入を決定する決め手は、価格と商品ではなくなっています。

カスタマー エクスペリエンスを向上させるには、すべてのチャネルの在庫をリアルタイムに確認できる必要があります。 すべての在庫を 1 か所で包括的に確認できれば、注文のフルフィルメント、配賦、流通の最適化に役立ちます。 そのため、分散型注文管理 (DOM) システムの採用と導入は、小売企業にとって必要不可欠になりつつあります。

DOM により、複雑にネットワーク化されたシステムやプロセスの全体を通じて、注文のフルフィルメントを最適化できます。 DOM では、組織全体の在庫を単一のグローバルなビューにまとめることで、インテリジェントに注文を管理できます。それにより、正確に、しかもコスト効率よく注文のフルフィルメントを行うことができます。 DOM は、小売企業のサプライ チェーンの効率を改善することにより、顧客の期待に応えられるよう支援します。

次の図は、DOM システムにおける販売注文のライフサイクルを示しています。

![DOM のコンテキストにおける販売注文のライフサイクル](./media/flow.png "DOM のコンテキストにおける販売注文のライフサイクル")

## <a name="set-up-dom"></a>DOM を設定する

1. **システム管理 \> 設定 \> ライセンス コンフィギュレーション** の順にクリックします。
2. **コンフィギュレーション キー** タブで **コマース** ノードを展開し、**配分済み注文の管理** チェック ボックスをオンにします。
3. **Retail と Commerce \> 配分済み注文の管理 \> 設定 \> DOM パラメーター** の順にクリックします。
4. **一般** タブで、次の値を設定します。

    - **配分済み注文の管理を有効化する** – このオプションでは **はい** を設定します。
    - **DOM に対する Bing 地図の使用状況を確認する** – このオプションでは **はい** を設定します。

        > [!NOTE]
        > このオプションを **はい** に設定できるのは、**コマース共有パラメーター** ページの **Bing 地図** タブにある **Bing 地図を有効化** オプション (**Retail と Commerce \> 本社の設定 \> パラメーター \> マース共有パラメーター** の順にクリックします) も **はい** になっていて、かつ、**Bing 地図キー** に有効なキーが入力されている場合のみです。

    - **留保期間 (日)** – DOM 実行で生成されるフルフィルメント計画を、システム内で保持する期間を指定します。 **DOM フルフィルメント データ削除ジョブの設定**のバッチ ジョブでは、ここで指定した日数を経過したフルフィルメント計画がすべて削除されます。
    - **拒否期間 (日)** – ここで指定した期間を経過すると、否認済の注文明細行を同じ場所に割り当てられるようになります。

5. **ソルバー** タブで、次の値を設定します。

    - **最大自動フルフィルメント試行回数** – DOM エンジンが注文明細行の場所に対する仲介を試行する回数を指定します。 指定された試行回数で、DOM エンジンが注文明細行を場所に対して仲介できない場合、注文明細行に例外のフラグが設定されます。 フラグが設定された明細行は、手動でステータスがリセットされない限り、その後の実行ではスキップされます。
    - **ローカル店舗地域半径** – 値を入力します。 このフィールドは、場所をどのようにグループ化するか、距離的に同等と見なすかを判断するために使用されます。 たとえば、**100**と入力した場合、フルフィルメントの住所から半径 100 マイル以内の店舗または物流センターは、距離的に同等と見なされます。
    - **ソルバー タイプ** – 値を選択します。 Commerce では、**本番ソルバー**と**簡易ソルバー**の 2 種類のソルバー タイプがあります。 DOM を実行するすべてのマシン (DOMBatch グループに含まれるすべてのサーバー) で、**本番ソルバー** を選択する必要があります。 本番ソルバーでは、実稼働環境に既定でライセンスされ、配置される特別なライセンス キーが必要です。 非実稼働環境では、このライセンス キーは手動で配置する必要があります。 ライセンス キーを手動で配置するには、次の手順を実行します。

        1. Microsoft Dynamics Lifecycle Services で、共有アセット ライブラリを開き、アセット タイプとして **モデル** を選択して、**DOM ライセンス** ファイルをダウンロードします。
        2. Microsoft インターネット インフォメーション サービス (IIS) マネージャーを起動し、**AOSService Web サイト** を右クリックし、**エクスプローラ** を選択します。 エクスプローラー ウィンドウが開き、**\<AOS サービスのルート\>\\webroot** が表示されます。 \<AOS サービスのルート\> のパスをメモしておいてください。このパスは次の手順で使用します。
        3. **\<AOS Service root\>\\PackagesLocalDirectory\\DOM\\bin** ディレクトリにある構成ファイルをコピーします。
        4. Headquarters クライアントで、**DOM パラメーター** ページを開きます。 **ソルバー** タブの **ソルバー タイプ** フィールドで、**本番ソルバー** を選択し、エラー メッセージが表示されないことを確認します。

        > [!NOTE]
        > 簡易ソルバーは、特別なライセンスを配置せずに DOM 機能を試すことができるように、用意されています。 実稼働環境では、簡易ソルバーを使用しないようにしてください。
        >
        > 簡易ソルバーには、本番ソルバーと同じ機能がありますが、パフォーマンス (1 回の実行で処理できる注文および注文明細行の数) および結果の範囲 (注文をバッチ処理するとシナリオによっては最適な結果が出ない場合があります) について制限があります。
     
6. **Retail と Commerce \> 配分済み注文の管理 \> 設定 \> DOM パラメーター** の順にクリックして戻ります。
7. **番号順序** タブで、さまざまな DOM エンティティに必要な番号順序を割り当てます。

    > [!NOTE]
    > エンティティに番号順序を割り当てるには、**番号順序** ページ (**組織管理 \> 番号順序 \> 番号順序** の順にクリックします) で定義しておく必要があります。

8. DOM 機能では、さまざまなタイプの DOM ルールの定義がサポートされており、企業のビジネス ニーズに応じて、複数のルールを構成することができます。 DOM ルールは、場所のグループまたは個々の場所ごと、および、特定の製品カテゴリ、製品、バリアントに対して定義することができます。 DOM ルールに使用する必要がある場所のグループを作成するには、次の手順を実行します。

    1. **Retail と Commerce \> チャネル設定 \> フルフィルメント グループ** の順にクリックします。
    2. **新規** を選択し、新しいグループの新しい名前と説明を入力します。
    3. **保存** を選択します。
    4. **行の追加** を選択して、単一の場所をグループに追加します。 または、**行の追加** を選択して、複数の場所を追加します。

9. ルールを定義するには、**Retail と Commerce \> 配分済み注文の管理 \> 設定 \> ルールを管理する** の順にクリックします。 次の DOM ルールが現在サポートされています。

    - **最小在庫ルール** – このルール タイプでは、一定量の製品を注文のフルフィルメント以外の目的で確保しておくことができます。 たとえば、店舗にある在庫のすべてを、DOM で注文のフルフィルメントに使用されると困る場合があります。 一定の在庫は、来店する顧客用に確保しておく必要があるためです。 このルール タイプを使用すると、1 つの場所または場所のグループごとに、製品のカテゴリ、個別の製品、または製品バリアントについて、確保しておく必要がある最小限の在庫を定義できます。
    - **フルフィルメント場所優先順位ルール** – このルール タイプでは、場所の階層を定義して、DOM エンジンが特定の製品についてフルフィルメント場所を特定する際の優先順位を指定できます。 優先順位の有効な範囲は 1 ～ 10 で、1 が最も優先度が高く、10 が最も優先度が低くなります。 優先順位の高い場所が、優先順位の低い場所よりも先に検討対象となります。 ルールが厳格な制約として定義されている場合、注文は、優先順位が定義されている場所にのみ仲介されます。
    - **部分注文ルール** – このルールでは、注文または注文明細行の部分的なフルフィルメントを許可するかどうかを定義できます。 次のパラメーターを使用できます。

        - **部分注文をフルフィルメントしますか。** – このオプションを **はい** に設定すると、注文明細行の数量の一部のみのフルフィルメントが可能になります。 この部分フルフィルメントは、注文明細行を分割して行われます。
        - **部分明細行をフルフィルメントしますか。** – このオプションを **はい** に設定すると、注文明細行の数量の一部のフルフィルメントが可能になります。 この部分フルフィルメントは、注文明細行を分割して行われます。
        - **1 つの場所からのみ注文をフルフィルメントしますか** – このオプションを **はい** に設定すると、注文のすべての明細行のフルフィルメントが単一の場所から行われます。


        次の表は、これらのパラメーターを組み合わせて定義した場合の動作を説明したものです。

        |      | 部分注文をフルフィルメント | 部分明細行をフルフィルメント | 1 つの場所からのみ注文をフルフィルメント | 説明 |
        |------|------------------------|-----------------------|--------------------------------------|-------------|
        | 1    | はい                    | はい                   | はい                                  | 注文の一部の明細行のフルフィルメントができ、個々の明細行の部分的なフルフィルメントもできますが、すべての明細行は、DOM が実行されているインスタンスの同じ場所からである必要があります  (この組み合わせは、現在サポートされていません)。 |
        | 2    | はい                    | いいえ                    | はい                                  | 注文の一部の明細行のフルフィルメントができますが、個々の明細行の部分的なフルフィルメントはできません。フルフィルメントされる明細行はすべて、DOM が実行されているインスタンスの同じ場所からである必要があります。  (この組み合わせは、現在サポートされていません)。 |
        | 3    | はい                    | はい                   | いいえ                                   | 注文の一部の明細行のフルフィルメントができ、個々の明細行の部分的なフルフィルメントもできます。各明細行のフルフィルメントは、DOM が実行されているインスタンスの複数の場所から行うことができます。 |
        | 4\*  | いいえ                     | 適用できません        | いいえ                                   | 注文明細行はすべてフルフィルメントする必要があり、個々の明細行を部分的にフルフィルメントすることはできません。各注文明細行は、複数の場所からフルフィルメントすることができます。 |
        | 5\*  | いいえ                     | 適用できません        | はい                                  | 注文明細行はすべてフルフィルメントする必要があり、個々の明細行を部分的にフルフィルメントすることはできません。すべての注文明細行は、1 つの場所からのみ配送できます。 |
        | 6\*  | いいえ                     | 適用できません        | いいえ                                   | この組み合わせは、4 の組み合わせと同じように機能します。**部分注文をフルフィルメントしますか** が **いいえ** に設定されている場合、**部分明細行をフルフィルメントしますか** を **はい** に設定できないためです。 |
        | 7\*  | いいえ                     | 適用できません        | はい                                  | この組み合わせは、5 の組み合わせと同じように機能します。**部分注文をフルフィルメントしますか** が **いいえ** に設定されている場合、**部分明細行をフルフィルメントしますか** を **はい** に設定できないためです。 |
        | 8    | はい                    | いいえ                    | いいえ                                   | 注文の一部の明細行のフルフィルメントができますが、個々の明細行の部分的なフルフィルメントはできません。さまざまな明細行のフルフィルメントを、DOM が実行されているインスタンスの複数の場所から行うことができます。 |
        | 9\*  | いいえ                     | 適用できません        | はい                                  | 注文明細行はすべてフルフィルメントする必要があり、すべての注文明細行は、1 つの場所からのみフルフィルメントを行う必要があります。 |

        \*たとえば、**部分注文をフルフィルメントしますか** が **いいえ** に設定されている場合、**部分明細行をフルフィルメントしますか** は、実際の設定にかかわらず、必ず **いいえ** に設定されているものと見なされます。

        > [!NOTE]
        > Retail バージョン 10.0.5 では、パラメーターの **1 か所のみで注文をフルフィルメントする** は、**フルフィルメントする場所の最大化**に変更されました。 1 か所のみでか、可能な限り多くの場所で注文のフルフィルメントを行うかどうかをユーザーが構成できるようにするのではなく、確実な場所 (最大 5 つ) からか、可能な限り多くの場所からフルフィルメントするかをユーザーが指定できるようになりました。 これにより、注文をフルフィルメントできる場所の数をより柔軟に指定できます。

   - **オフライン フルフィルメント場所ルール** – このルールでは、場所または場所のグループをオフライン、または DOM から利用不可として指定できます。指定された場所または場所のグループには、フルフィルメントを行うよう注文をこれらの場所に割り当てることはできません。
    - **最大拒否回数ルール** – このルールにより、組織は拒否のしきい値を定義できます。 このしきい値に達すると、DOM プロセッサは注文または注文明細行に例外のマークを付け、その後の処理から除外します。

        注文明細行が場所に割り当てられた後、何らかの理由でその場所ではその明細行のフルフィルメントができないことがあるため、場所は割り当てられた注文明細行を拒否することができます。 拒否された明細行には例外のマークが付けられ、次回の実行時に処理されるように、プールに戻されます。 次回実行時に、DOM は、拒否された明細行を別の場所に割り当てます。 新しい場所でも、割り当てられた注文明細行を拒否することができます。 この割り当てと拒否のサイクルが、複数回発生することもありえます。 この拒否の回数が、定義されているしきい値に達すると、DOM はその注文明細行に永続的な例外のマークを付けます。その明細行は、それ以上割り当てが試行されません。 ユーザーがその注文明細行のステータスを手動でリセットした場合に限り、DOM でその注文明細行が再割り当ての対象となります。

   - **最大距離ルール** – このルールでは、注文のフルフィルメントを行える、場所または場所のグループの距離の最大値を定義できます。 1 つの場所に対して、最大距離ルールが重複して定義されている場合、DOM では、その場所に対して定義されている中で最も値の小さい最大距離が適用されます。
    - **最大注文数ルール** – このルールでは、場所または場所のグループで 1 カレンダー日に処理できる注文の最大数を定義できます。 ある 1 日に、場所に対して最大数の注文が割り当てられた場合、そのカレンダー日には、その場所に対してそれ以上、注文が割り当てられなくなります。

   以下に、共通の属性をいくつか示します。ここまでに記載したすべての種類のルールで、これらの属性を定義できます。

   - **開始日** および **終了日** – どのルールでも、これらのフィールドを使用することで、日付を指定して有効期間を設けることができます。
   - **無効** – このフィールドに **いいえ** の値が設定されているルールのみが、DOM の実行時に考慮されます。
   - **厳格な制約** – ルールが厳格な制約であるか、厳格な制約でないかを指定することができます。 DOM を実行すると、2 回の処理が実行されます。 1 周目の処理では、このフィールドの設定にかかわらず、すべてのルールが厳格な制約のルールとして扱われます。 つまり、すべてのルールが適用されます。 **場所優先順位** のルールのみが唯一の例外となります。 2 周目の処理では、厳格な制約のルールとして定義されていないルールは削除されます。すべてのルールを適用したときに場所が割り当てられなかった注文または注文明細行に場所が割り当てられます。

10. フルフィルメント プロファイルは、ルール、法人、販売注文元、配送モードのコレクションをグループ化するために使用されます。 1 つのフルフィルメント プロファイルに対して 1 回の DOM が実行されます。 このようにして、一連の法人に対する、特定の販売注文元および配送モードが設定されている注文についてのルールのセットを定義し、実行することができます。 そのため、販売注文元または配送モードが異なる別のセットについて、別のルールのセットを実行する必要がある場合は、それに応じてフルフィルメント プロファイルを定義することができます。 フルフィルメント プロファイルを設定するには、次の手順を実行します。  

    1. **Retail と Commerce \> 配分済み注文の管理 \> 設定 \> フルフィルメント プロファイル** の順にクリックします。
    2. **新規** を選択します。
    3. **プロファイル** および **内容** のフィールドに値を入力します。
    4. **結果を自動適用する** オプションを設定します。 このオプションを **はい** に設定すると、プロファイルに対する DOM の実行結果が販売注文明細行に自動的に適用されます。 このオプションを **いいえ** に設定すると、結果はフルフィルメント計画にのみ表示されます。 結果は販売注文明細行に適用されません。
    5. 販売注文元が未定義の注文についても、すべての販売注文元を持つ注文に対して、DOM プロファイルを実行するには、**販売元が指定されていない注文を処理する** オプションを **はい** に設定します。 一部の販売注文元についてのみプロファイルを実行するには、後で説明するように、**販売元** ページでその販売注文元を定義することができます。
    6. **法人** クイック タブで、**追加** を選択して、法人を選択します。
    7. **ルール** クイック タブで、**追加** を選択して、プロファイルにリンクするルールを選択します。
    8. 必要なルールがすべてプロファイルに関連付けられるまで、前の 2 つのステップを繰り返します。
    9. **保存** を選択します。
    10. アクション ペインの **設定** タブで、**配送モード** を選択します。
    11. **配送モード** ページで、**新規** を選択します。
    12. **法人** フィールドで、法人を選択します。 法人のリストは、ユーザーが前に追加した法人に限定されます。
    13. **配送モード** フィールドで、このプロファイルに関連付ける配送モードを選択します。 1 つの配送モードを複数のアクティブなプロファイルに関連付けることはできません。
    14. 必要な配送モードがすべてプロファイルに関連付けられるまで、前の 2 つのステップを繰り返します。
    15. **配送モード** ページを閉じます。
    16. アクション ペインの **設定** タブで、**販売注文元** を選択します。
    17. **販売元** ページで、**新規** を選択します。
    18. **法人** フィールドで、法人を選択します。 法人のリストは、ユーザーが前に追加した法人に限定されます。
    19. **販売元** フィールドで、このプロファイルに関連付ける販売元を選択します。 1 つの販売元を複数のアクティブなプロファイルに関連付けることはできません。
    20. 必要な販売元がすべてプロファイルに関連付けられるまで、前の 2 つのステップを繰り返します。
    21. **販売元** ページを閉じます。
    22. **プロファイルを有効化する** オプションを **はい** に設定します。 設定にエラーがある場合は、警告メッセージが表示されます。

## <a name="dom-processing"></a>DOM の処理

DOM は、バッチ ジョブでのみ実行されます。 DOM の実行用にバッチ ジョブを構成するには、次の手順を実行します。

1. **Retail と Commerce \> 配分済み注文の管理 \> バッチ処理 \> DOM プロセッサ ジョブの設定** の順にクリックします。
1. **パラメーター** クイック タブの **フルフィルメント プロファイル** フィールドで、DOM を実行する必要があるプロファイルを選択します。
1. **バックグラウンドで実行** クイック タブの **バッチ グループ** フィールドで、構成済みのバッチ グループを選択します。
1. **タスクの説明** フィールドにバッチ ジョブの名前を入力します。
1. **反復** を選択して、バッチ ジョブの繰り返しを定義します。
1. **OK** を選択します。

処理の際、DOM では、次に示す注文および注文明細行を処理の対象とします。

- DOM プロファイルで定義されている販売注文元、配送モード、および法人の条件を満たし、次のいずれかの条件も満たす注文明細行:

    - コマース チャネルから作成されている。
    - DOM によって仲介されていない。
    - 以前に DOM によって仲介をされているが、例外のマークが付けられ、試行回数の上限のしきい値に達していない。
    - 配送モードが、集荷または電子的方法による納品ではない。
    - 出荷のマークがついていない。
    - 手動で除外されていない。

- 保留中になっていない注文

ルール、在庫の制約、最適化の適用後、DOM は、顧客の配送先住所に最も近い場所を選択します。

![販売注文の基準](./media/ordercriteria.png "販売注文の基準")

## <a name="results-of-dom-runs"></a>DOM 実行の結果

フルフィルメント プロファイルが **結果を自動適用する** に設定されている場合、実行結果は販売注文明細行に自動的に適用され、フルフィルメント計画は別々に確認できます。 ただし、フルフィルメント プロファイルが **結果を自動適用する** に設定されていない場合、実行結果はフルフィルメント計画ビューからのみ確認できます。 

生成されたフルフィルメント計画をすべて表示するには、次の手順を実行します。

1. **Retail と Commerce \> 配分済み注文の管理 \> 配分済み注文の管理** の順にクリックします。
2. **配分済み注文の管理** ワークスペースで、**フルフィルメント計画** タイルを選択します。
3. フルフィルメント計画を表示するには、関連する注文フルフィルメント計画の ID を選択します。

    フルフィルメント計画の注文の詳細セクションには、実行に含まれていた元販売注文明細行が表示されます。 注文の詳細セクションには、標準の販売注文明細行フィールドに加え、次の 3 つの DOM 関連のフィールドも含まれます。

    - **フルフィルメント タイプ** – このフィールドは、販売注文明細行が完全に仲介されたか、部分的に仲介されたか、まったく場所に仲介されなかったかを示します。
    - **分割** – このフィールドは、1 つの販売注文明細行が分割され、複数の場所に仲介されたかどうかを示します。
    - **フルフィルメント場所数** – このフィールドは、1 つの販売注文明細行に対していくつのフルフィルメント明細行が作成されたかを示します (元販売注文明細行が仲介された場所の数に基づきます)。

    注文フルフィルメント詳細情報セクションには、元販売注文明細行の他の場所への割り当てと、その数量が表示されます。

## <a name="order-line-actions-and-statuses"></a>注文明細行のアクションとステータス

注文明細行の設定は、次の通りです。 注文明細行を開くには、**Retail と Commerce \> 顧客 \> すべての販売注文** の順にクリックします。
- 販売注文明細行の **一般** タブの **DOM 処理から除外する** オプションを **はい** に設定した場合、注文または注文明細行は DOM の処理から除外されます。
- 販売注文明細行の **一般** タブの **DOM 状態** フィールドに設定される値は、次のとおりです。

    - **なし** – 注文明細行は一度も仲介されていません。
    - **完了** – 注文明細行は正常に仲介され、場所が割り当てられています。
    - **例外** – 注文明細行は仲介されましたが、場所が割り当てられていません。 例外にはいくつかのサブタイプがあり、DOM ワークスペースから参照できます。

        - **利用可能数量なし** – 注文を割り当てられる利用可能在庫が場所にありません。
        - **最大拒否回数** – 注文明細行が、拒否回数の上限のしきい値に達しています。
        - **データの変更による競合** – 注文が仲介されてから、販売注文明細行が変更されています。 そのため、フルフィルメント計画を注文に適用できません。
        - **注文明細行固有の例外** – 注文明細行に複数の例外があります。

- 販売注文入力の際、DOM を対話モードで実行できます。 注文明細行を入力する際、製品と数量を指定した後、**明細行の更新** を選択してから、**DOM** の下の **フルフィルメント場所を提案する** を選択できます。 DOM ルールに基づき、注文明細行の数量のフルフィルメントができる場所のリストを確認できます。 このリストは、距離に従って並べ替えられます。 場所を選択して、適切なサイトと倉庫を販売注文明細行に設定します。 この機能の実行には、販売明細行の販売元および配送モードに対応する、既存の有効なフルフィルメント プロファイルが存在する必要があります。
- 販売注文明細行に対する DOM の実行ログを表示するには、**販売注文明細行** を選択し、**DOM** の下の **DOM ログを表示する** を選択します。 DOM のログには、DOM の実行で生成されたすべてのイベントとログが表示されます。 このログは、特定の場所が注文明細行に割り当てられた理由や、割り当てにおいてどのルールや制限が適用されたのかを理解するのに役立ちます。 **管理** タブで、販売注文ヘッダーのレベルで DOM ログを表示することもできます。

## <a name="run-a-clean-up-job-for-dom-fulfillment-plans"></a>DOM フルフィルメント計画に対するクリーンアップ ジョブの実行

DOM 処理が実行されると、フルフィルメント計画が作成されます。 時間が経過すると、システムで多数のフルフィルメント計画が保持されることになります。 システムで保持するフルフィルメント計画の数を管理するために、**留保期間 (日)** の値をもとに、古くなったフルフィルメント計画を削除するバッチ ジョブを構成することができます。

1. **Retail と Commerce \> 配分済み注文の管理 \> バッチ処理 \> DOM フルフィルメント データ削除ジョブの設定** の順にクリックします。 
1. **バッチ グループ** フィールドで、構成済みのバッチ グループを選択します。
1. **反復** を選択して、バッチ ジョブの繰り返しを定義します。
1. **OK** を選択します。

## <a name="more-information"></a>詳細情報

DOM 機能を使用する際には、以下の点について考慮する必要があります。

- 現時点では、DOM では、コマース チャネルから作成された注文のみが処理されます。 **コマース販売** オプション が **はい** になっている場合に、販売注文は小売販売注文と見なされます。
- マイクロソフトでは、DOM での高度な倉庫管理機能の使用については、テストを行っていません。 お客様およびパートナー様には、関連のある高度な倉庫管理の機能およびプロセスとの互換性が DOM にあるかどうかを、注意して判断していただく必要があります。
- DOM は、クラウド バージョンの Commerce でのみ利用できます。 オンプレミス配置ではサポートされません。