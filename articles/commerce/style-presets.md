---
title: スタイル プリセットの作業
description: このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーでのサイト スタイル プリセットの作業方法について説明します。
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 250f2386cefee8bef45df66c4eef31b4e7fc2686
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413821"
---
# <a name="work-with-style-presets"></a>スタイル プリセットの作業

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーでのサイト スタイル プリセットの作業方法について説明します。

## <a name="overview"></a>概要

スタイル プリセットは、サイトのテーマ全体のすべてのカスタム スタイル値の保存されたセットです。 これを使用すると、サイト ビルダーからサイトの外観をすぐに変更できます。 スタイルのプリセットにより、Commerce サイト ビルダーの作成者は、カスケード スタイルシート (CSS) を使用したり、テーマを配置することなく、サイト全体のスタイル値をすばやく変更、プレビュー、およびアクティブにできます。 スタイル変数の一般的な例としては、スタイルのプリセットを使用して管理できるフォント スタイル、ボタン スタイル、サイト カラーなどがあります。

サイトで使用できるスタイル変数のセットは、サイトのテナントに配置されているテーマとモジュール ライブラリによって決まります。 Dynamics 365 Commerce オンライン ソフトウェア開発キット (SDK) を使用すると、開発者は、特定のテーマに対して必要な数のカスタム スタイル変数を実装できるようになります。 より多くのスタイル変数を有効にすることによって、テーマ開発者は、サイト ビルダーの作成者にサイト スタイルの最終決定を任せることができます。 したがって、開発者以外はツール セットを使用してサイト スタイルを更新およびプレビューできます。 また、この機能は、テーマや CSS を直接変更したり不要なオーバーヘッドを生じたりするようなシナリオで役に立ちます。

カスタム スタイル変数が有効になっているテーマでは、既定のスタイル プリセットが必要です。 必要に応じて、配置されたテーマ パッケージの一部として追加のプリセット オプションを含めることができます。 たとえば、1 つの既定の "モダン ライト" スタイル プリセットを持つテーマを配置することができます。 また、既定のプリセットに加えて、"モダン ダーク"、"ビンテージ ライト"、または "ビンテージ ダーク" などの追加のスタイル プリセット オプションが含まれている場合もあります。 これらの組み込みテーマの事前設定は、開発者によって作成され、新しいサイト デザインの開始点として使用できます。

サイト ビルダーでは、作成者は、テーマの組み込みプリセットから選択するか、有効なスタイル変数を使用して独自のスタイル プリセットとカスタマイズを作成することができます。 実際のサイトで有効にする前に、スタイル プリセットをサイト ビルダーでプレビューできます。 作成者のスタイルの変更がレビューされた後、スタイルのプリセットを実際のサイトに対して "有効" に設定できます。

## <a name="preview-a-style-preset"></a>スタイル プリセットのプレビュー

サイト ビルダーでサイトのスタイル プリセットをプレビューするには、次の手順を実行します。

1. サイトの左側のナビゲーション ウィンドウで、**サイト設定 \>のデザイン** に移動します。
1. デザイン エディターの上部にある **スタイル プリセット** タブの **使用可能なプリセット** リストでプリセットを選択し、**表示** をクリックしてプリセット エディターに移動します。

    現在、**使用可能なプリセット** の一覧にプリセットが存在しない場合は、[カスタム スタイル プリセットの作成](#create-a-custom-style-preset) を参照してください。

    > [!NOTE]
    > テーマに含まれていたプリセットは、**組み込み** のバッジで示されます。 これらの組み込みのプリセットは、読み取り専用です。 組み込みのプリセットを新しいカスタマイズ可能なプリセットとしてコピーするには、省略記号ボタン (**...**) を選択し、**名前を付けて保存** を選択します。

1. コマンド バーで、**プレビュー** を選択します。
1. スタイル プリセットをプレビューを使用するために自分のサイトからの URL を選択して、**OK** を選択します。
1. バリアントの名前を選択して、プレビューするチャンネル固有でロケール固有の URL バリアントを選択します。 新しいプレビュー ブラウザ ウィンドウが開き、選択したスタイルのプリセットが指定したページに適用されます。

> [!NOTE]
> プレビュー URL は永続的で認証されています。 したがって、実際のサイトで "有効" に設定する前に、認証された他の同僚にコピーして貼り付けて送信し、確認することができます。 また、プレビュー URL は、さまざまなデバイス、さまざまなブラウザー、さまざまな画面でスタイルをチェックする場合にも役立ちます。

> [!TIP]
> スタイル プリセットを編集する間に、別のブラウザ ウィンドウでプレビュー ブラウザ ウィンドウを開いたままにしておくと、変更をすぐに検証できます。 プリセットに変更を保存した後、開いたプレビュー ブラウザ ウィンドウを更新して、ユーザー エクスペリエンスを検証します。

## <a name="create-a-custom-style-preset"></a>カスタム スタイルのプリセットを作成する

サイト ビルダーでカスタム スタイル プリセットを作成するには、次の手順を実行します。

1. サイトの左側のナビゲーション ウィンドウで、**サイト設定 \>のデザイン** に移動します。
1. デザイン エディターの上部にある **スタイル プリセット** タブのコマンド バーで、**新規プリセット** を選択します。
1. 新規プリセットの名前と説明を入力して、**保存** を選択します。 このテーマの既定値を出発点として使用する、新しいカスタマイズ可能なプリセットが作成されます。

> [!NOTE]
> また、既存のプリセットから新しいカスタム スタイルのプリセットを作成するには、そのプリセットの省略符号ボタン (**...**) を選択し、**名前を付けて保存** を選択します。 または、プリセット エディタのコマンドバーで **名前を付けて保存** を選択します。

## <a name="modify-global-and-module-type-style-values"></a>グローバル タイプとモジュール タイプのスタイル値の変更

一部のテーマのスタイル変数は、複数のモジュールタイプの間で共有されます。 これらのスタイル変数は、*グローバル* スタイル変数と呼ばれます。 例としては、プライマリ サイトの色、既定のフォント スタイル、ボタンのスタイルなどがあります。 グローバル変数を設定することにより、さまざまな種類のモジュールに対して外観を変更することができます。

一部のスタイル値は、モジュール タイプに固有の場合もあれば、既定のグローバル値を上書きする必要がある場合もあります。 サイトのテーマによって、モジュール タイプのスタイル変数が実装されている場合、サイト ビルダーの作成者は、グローバル設定とは別にモジュール タイプのスタイルをカスタマイズできます。 モジュール タイプ変数は、テーマのグローバル スタイル変数を補強または上書きすることができます。

> [!NOTE]
> サイトのスタイル値の階層は、次のような方法で動作します。 スタイル値は右方向に表示され、その左にあるスタイル値は上書きされます。
>
> テーマの既定値 \<グローバルスタイル値 \<モジュール タイプ スタイル値 \<CSS上書き

サイト ビルダーでスタイル プリセットのグローバル タイプの値かモジュールタイプの値を変更するには、次の手順に従います。

1. サイトの左側のナビゲーション ウィンドウで、**サイト設定 \>のデザイン** に移動します。
1. デザインエディターの上部にある **スタイル プリセット** タブで、プリセット エディターに移動するスタイル プリセットの **表示** を選択します。
1. **プレビュー** を選択し、URLの選択の手順に従って、プリセットのフルブラウザー ウィンドウ プレビューを開きます。 このプレビュー ブラウザ ウィンドウは開いたままにしておきます。
1. プリセット エディターで、右上にある **編集** を選択します。
1. グローバル スタイルの値を変更するには、エディターのスタイル変数コントロールを使用します。
1. エディターの最上部で、**グローバル** タブの右側にある **モジュール** タブで、スタイルを設定する必要があるモジュールのタイプを選択します。
1. スタイル コントロールを使用して、モジュール タイプの値を変更します。
1. 変更をプレビューする準備ができたら、コマンドバーの **保存** を選択します。
1. 開いているプレビュー ブラウザー ウィンドウに戻り、最新の状態に更新します。 完全ブラウザ ウィンドウのプレビューは、さまざまな表示ブレークポイント、異なるブラウザー、異なるデバイス プラットフォームでスタイルの変更をチェックする場合に役立ちます。
1. すべての変更が完了して検証されたら、エディターの右上にある **編集の完了** を選択します。

> [!NOTE]
> サイトで現在有効なスタイル プリセットを編集している場合、青色の **有効な** バッジがエディターに表示されます。 このバッジは、プリセットが Web サイト上で現在有効であることを示します。 有効なプリセットを変更する場合は、**発行** を選択してその変更を実際のサイトにプッシュします。

## <a name="make-a-new-style-preset-active-on-your-live-site"></a>実際のサイトで新しいスタイルのプリセットを有効にする

サイトの新しい有効なプリセットとしてスタイル プリセットを設定するには、次の手順を実行します。

- 次のいずれかの場所で、**有効なボタンとして設定** を選択します。

    - スタイル プリセット エディターのコマンドバー
    - **サイト設定 \> デザイン** の **スタイル プリセット** のメイン ビューにある利用可能なプリセットの省略記号メニュー (**...**)

プリセットのスタイル値が一般公開 Web サイト全体で有効になります。

## <a name="additional-resources"></a>追加リソース

[ロゴの追加](add-logo.md)

[サイト テーマの選択](select-site-theme.md)

[CSS 上書きファイルの作業](css-override-files.md)

[ファビコンの追加](add-favicon.md)

[ようこそメッセージの追加](add-welcome-message.md)

[著作権に関する注意事項の追加](add-copyright-notice.md)

[サイトに言語を追加する](add-languages-to-site.md)

[サイト ページにスクリプト コードを追加してテレメトリをサポートする](add-telemetry.md)