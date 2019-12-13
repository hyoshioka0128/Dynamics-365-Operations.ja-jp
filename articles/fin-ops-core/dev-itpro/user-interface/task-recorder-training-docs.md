---
title: タスク レコーダーによるドキュメントやトレーニングの作成
description: このトピックでは、タスク レコーダーとタスク ガイド、タスク記録の作成方法、また Microsoft タスク ガイドのカスタマイズ方法とそれをヘルプに含める方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4bb523c2817a220623d8a1b6cc1ac04d7b96283
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812652"
---
# <a name="create-documentation-or-training-with-task-recorder"></a>タスク レコーダーによるドキュメントやトレーニングの作成

[!include [banner](../includes/banner.md)]

このトピックでは、タスク レコーダーとタスク ガイド、タスク記録の作成方法、また Microsoft タスク ガイドのカスタマイズ方法とそれをヘルプに含める方法について説明します。

> [!IMPORTANT]
> Dynamics 365 Talent 用のタスク ガイドを記録できますが、それをビジネス プロセス モデラー (BPM) ライブラリに保存したり、またはこの時点でヘルプ ウィンドウから開くことはできません。 ローカルまたはネットワーク上の場所に保存することはでき、タスク レコーダーを使用して開き再生します。 

<a name="learn-about-task-recorder"></a>タスク レコーダーについて学ぶ
-------------------------

タスク レコーダーは、製品のユーザー インターフェイス (UI) で実行するアクションを記録するのに使用するツールです。 タスク レコーダーを使用している場合は、UI で実行する、サーバーに対して実行されるイベント —値の追加、設定の変更、データの削除— はすべて取得されます。 記録する手順は、*タスク記録* と呼ばれます。 タスク記録はさまざまな方法で使用できます。

-   **タスク記録はタスク ガイドとして再生できます。** タスク ガイドは、ヘルプ エクスペリエンスの不可欠な部分です。タスク ガイドは、業務プロセスのステップを通じて管理、ガイドされたインタラクティブなエクスペリエンスです。 ユーザーは、UI 上でアニメーションされ、ユーザーが操作する必要がある UI 要素を指定するポップアップ プロンプト (または「バブル」) で各ステップを完了するよう指示されます。 「バブル」は、「ここをクリックします」または「このフィールドで値を入力します」などの、要素を操作する方法に関する情報も提供します。タスク ガイドはユーザーの現在のデータ セットに対して実行され、入力されるデータはユーザーの環境に保存されます。
-   **タスク記録をヘルプ ウィンドウの手順に関するステップとして表示できます。** タスク記録の検索と表示にヘルプ ウィンドウを使用できます。 ヘルプ ウィンドウにアクセスするには、ナビゲーション バー上の **?** をクリックするか、 ショートカット キーの組み合わせ  **Ctrl+Shift+?** を使用します。 ヘルプ ウィンドウでタスク記録の手順を読むか、記録をタスク ガイドとして再生して UI を実行できます。
-   **タスク記録を BPM に保存できます。** Lifecycle Services (LCS) の BPM ライブラリの階層の明細行にタスク記録を保存できます。 手順の一覧および業務プロセスのフローチャートが記録に基づいて生成されます。 BPM ライブラリに保存されたタスク記録は、ヘルプとして表示できます。
-   **タスク記録を Word 文書として保存できます。** これにより、印刷可能なトレーニング ガイドを簡単に作成することができます。

自分のタスク記録を作成、または Microsoft が提供するタスク記録を再生、または自分のコンフィギュレーションを反映するように変更できます。タスク レコーダーの詳細については、「[タスク レコーダー](task-recorder.md)」を参照してください。

## <a name="plan-your-task-recording"></a>タスク記録を計画する
新しいタスク記録を作成、または Microsoft のタスク記録を基に記録する場合も、次の情報に注意してください。

-   記録を、ビデオを計画するかのように計画します。 決定はすべて事前に行います。
-   ステップを理解するために、業務プロセスを記録せずに何度か確認します。
-   記録する前にプロセスを確認するとき、実際の記録中にショートカット キーまたは **Enter** キーを使用することを避けられるようできるように、それらが使用される場所を確認してください。
-   次を識別します。
    -   ステップをサブタスクにグループ化しますか。 サブタスクは、プロセスのセクションを視覚的に分離します。 たとえば、「製品の作成とリリース」のための記録を作成する場合、製品を作成するために必要な手順をグループ化し、製品をリリースするために必要な手順をグループ化したい場合があります。 サブタスクは、長いプロセスを読みやすくします。
    -   注釈を追加しますか、またどこに追加しますか。 詳細については、「注釈のさまざまなタイプを理解する」を参照してください。
    -   業務プロセスのステップを完了するときにさまざまなフィールドにどのような値を追加しますか。 記録しながら後戻りしたり間違いを修正する必要がないよう、記録時に何を選択または入力するのかを把握しておくことをお勧めします。

**説明、および注釈を事前に記述**

-   各タスク記録の先頭には、記録の概要を入力できる説明フィールドがあります。 記録するときにタスク記録にコピーおよび貼り付けできるよう、説明を事前に別のドキュメントに作成して保存することをお勧めします。 これにより、記録していないときはテキストの調整に時間を使うことができます。 テキストを切り取りおよび貼り付けすると、記録のプロセスをより迅速かつスムーズに行えます。
-   タスク記録のステップごとに注釈を作成できます。 タスク ガイドの再生中、注釈はステップのテキストの上または下に注記として「バブル」で表示されます。 ヘルプ ウィンドウにテキストとして表示される際、注釈はステップのテキスト インラインとして表示されます。 説明と同様、別のドキュメントに注釈を作成して保存することをお勧めします。 タスク記録を記録するときには、そのドキュメントから注釈を切り取りおよび貼り付けします。

**注釈のさまざまなタイプを理解する** すべての注釈はオプションです。 ユーザーに役立つ情報を提供する場合にのみ追加します。

-   **タイトル**: タイトル注釈はタスク レコーダに自動的に生成するステップ テキストの前に表示されます。タスク ガイドでは、タイトル注記は自動的に生成されたテキストの上に表示されます。 このタイプの注釈は、ユーザーがこの手順を行う理由またはコンテキストを追加するのに使用します。

これは、記録の作成時に注釈を追加する際に表示される編集ウィンドウです。 **タイトル** ボックスに、タイトルの注釈を入力します。 

[![タイトルの注釈のある編集ウィンドウ](./media/screen1.png)](./media/screen1.png) 

タスク ガイドの「バブル」に表示される注記の注釈は次のような外観です。 

[![タスク ガイドでのタイトル注釈の表示](./media/screen2.png)](./media/screen2.png)

-   **メモ:** 注記の注釈は、タスク レコーダに自動的に生成するステップ テキストの後に表示されます。 タスク ガイドでは、ユーザーがタスク ガイドの「バブル」の**詳細表示**リンクをクリックした場合にのみ表示されます。 ユーザーがステップを完了するために知る必要があることを説明するには、このタイプの注釈を使用します。

これは、記録の作成時に注釈を追加する際に表示される編集ウィンドウです。 **注記** ボックスに、タイトルの注記を入力します。 

[![注記ボックスにおける編集ウィンドウおよびタイトルの注釈](./media/screen3.png)](./media/screen3.png) 

タスク ガイドの「バブル」に表示される注記の注釈は次のような外観です。

[![タスク ガイドでの注記の注釈の表示](./media/screen4.png)](./media/screen4.png)

-   **参考ステップ**: これらの注釈は、コントロールまたはフォーム &lt; **タスク レコーダー** &lt; **参考ステップの追加**の任意の場所を右クリックすることで作成されます。 参考ステップは、アクションが UI で記録されていない場合でも、どこに挿入しても番号付きの手順として表示されます。 フォーム レベル参考ステップまたはコントロールと関連付けられた参考ステップを追加できます。 参考ステップがフォームに関連付けられている場合にタスク ガイドを再生すると、タスク ガイドの「バブル」がポインタがない状態でフォームのどこかに表示されます。 参考ステップがコントロールに関連付けられている場合にタスク ガイドを再生すると、タスク ガイドの「バブル」がコントロールをポイントします。ヘルプ ウィンドウで、参考ステップの注釈が入力した任意のテキストとともに番号付きの手順として表示されます。 参考ステップは、次の手順のためのユーザーの準備、アプリケーションの外部で行う必要があるステップの説明、または他の記録の参照 (注釈にハイパーリンクを作成することはできませんが) に使用します。

**記録の長さを決定**

-   ユーザーは通常、記録を開始から終了まで再生するため、別に実行した方が良いステップまたはタスクは結合しないでください。
-   複数のサブプロセスに及ぶ長いシナリオを記録しないようにしてください。 たとえば、「店舗の顧客サービス デスクの運用」は漠然としすぎているので、「返品の承認」や「ギフト カードに追加」など、短いタスクに分割します。
-   タスクが複数のさまざまな業務プロセスの一部として実行できる場合、個別の記録を作成して他の記録で参照できます。
-   ユーザーが一度に実行する可能性がある複数のタスクがプロセスに含まれる場合、たとえば、「機能プロファイルの設定および割り当て」などの 1 つの記録に含めることができます。
-   ユーザーが一度行うもので (コンフィギュレーションなど) 別のタスクをすぐ後に、繰り返し、単独で実行する場合、2 つの記録に分割します。

**UI のどこで記録を開始するか決定** タスク記録を開始したときのページは、タスク ガイドをどのページに対して再生するかに影響します。たとえば、タスク記録をユーザーが総勘定元帳パラメーター ページでヘルプをクリックしたときにヘルプ ウィンドウに表示させるには、総勘定元帳パラメーター ページで記録を開始する必要があります。 **.axtr ファイルとして記録を保存** タスク記録の作成または編集を完了すると、記録のダウンロードまたは保存方法の複数の選択が表示されます。 ファイルを、タスク記録パッケージ (.axtr)、未加工の記録ファイル (.xml)、Word 文書としてダウンロードまたは LCS ライブラリに保存できます。 タスク記録は、常にタスク記録パッケージ ファイル (.axtr) として保存しておくことをお勧めします。 これは、手順や注釈を後で変更する必要がある場合など、ファイルの保守を容易にすることができます。 ファイルを Word 文書としてダウンロードする場合も、タスク記録パッケージ ファイルとして保存します。

## <a name="create-your-task-recording"></a>タスク記録を作成
手順の詳細については、[タスク レコーダーのリソース](task-recorder.md) を参照してください。

## <a name="copy-and-customize-microsofts-task-recordings"></a>Microsoft のタスク記録をコピーしてカスタマイズ
Microsoft のタスク記録をダウンロードおよび編集し、自分のヘルプ ドキュメントまたはトレーニング資料に使用できます。 Microsoft のタスク記録をダウンロードするには、次の手順に従います。

1.  タスク レコーダーを開きます。 タスク レコーダーは **設定** メニューにあります。
2.  [タスク レコーダー] ウィンドウで、**記録の管理** をクリックします。
3.  **記録はどこにありますか** で **LCS ライブラリ内にあります**をクリックします。
4.  **LCS ライブラリの選択** をクリックします。
5.  Microsoft グローバル ライブラリを選択します。
6.  ツリーで、タスク記録が関連付けられる業務プロセス ライブラリのノードを選択します。
7.  **OK** をクリックします
8.  **開始** をクリックします。
9.  この時点で記録を進めてみて、再記録のときに任意のステップを変更します。 **メモ**: 記録のテキストのみを変更する必要がある場合は、**記録の注釈の編集**モードで記録を開いて保存します。
10. 記録が最後まで再生された後、画面の上部にあるタスク レコーダ バーの **停止** をクリックします。
11. タスク記録を保存する方法を選択してください。

## <a name="include-your-task-recordings-in-the-help-pane"></a>ヘルプ ウィンドウにタスク記録を盛り込む
独自のカスタマイズされたタスク記録をタスクガイドとして再生またはテキストとして表示するためにヘルプ ウィンドウに表示するには、タスク記録を BPM ライブラリに保存して、ヘルプ システム パラメーターを BPM ライブラリにポイントするように更新します。 詳細については、[ヘルプ システムの接続](../../fin-ops/get-started/help-connect.md) を参照してください。

<a name="additional-resources"></a>追加リソース
--------

[ヘルプ システム](../../fin-ops/get-started/help-overview.md)

[ヘルプ システムに接続する](../../fin-ops/get-started/help-connect.md)

[タスク レコーダー](task-recorder.md)

[タスク レコーダー (外部リンク) でリッチ ヘルプ トピックを作成](https://mbspartner.microsoft.com/AX/Videos/970)