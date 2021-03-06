---
title: ユーザー インターフェイス開発ホーム ページ
description: このトピックには、ユーザー インターフェイス要素の開発に関するトピックへのリンクが含まれています。
author: RobinARH
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 191453
ms.assetid: aea345a3-2302-4b72-9887-f23f72b911f1
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ee58e0da586194212a5e9530fddd507b42b77bd
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851039"
---
# <a name="user-interface-development-home-page"></a>ユーザー インターフェイス開発ホーム ページ

[!include [banner](../includes/banner.md)]

このトピックには、ユーザー インターフェイス要素の開発に関するトピックへのリンクが含まれています。

Microsoft Dynamics 365 for Finance and Operations のユーザー インターフェイスは、Microsoft Dynamics AX 2012 のユーザー インターフェイスと大きく異なります。 Dynamics AX 2012 のクライアントは、ActiveX、WinForm、または WPF コントロールを使用する拡張機能を備えた Microsoft Win32 アプリケーションです。 X++ アプリケーション ロジックが、フォーム メソッドおよびテーブル メソッドに対してクライアントで実行され、何らかのロジックがサーバー上で発生します。 コントロールについては、X++ ロジック アプリケーション プログラミング インターフェイス (API) および現物 Win32 コントロールの両方が、クライアントで密に接続されます。 クライアントは、すべての主要なブラウザーで動作する HTML Web クライアントです。 これらのブラウザーには、Microsoft Edge、Internet Explorer 11、Chrome、および Safari が含まれます ([システム要件](../../fin-and-ops/get-started/system-requirements.md) を参照)。 Web クライアントへの移行により、クライアントのフォームとコントロールに以下の変更が加えられました。

-   フォームとコントロールの物理的な表現は、現在は、ブラウザー内の HTML、JavaScript、および CSS です。
-   フォーム コントロールは、論理的および物理的な部分に分割されます。 X++ 論理 API および関連する状態は、サーバーで実行されます。
-   論理的部分と物理的部分は、それぞれの側から変更を伝えるサービス コールによって同期されています。 たとえば、クライアントのユーザー アクションは、すぐに送信されるまたは後で送信されるようにキューに入れられるかのいずれかであるサーバーへのサービス コールを作成します。
-   サーバー層は、フォームが開いている間にフォーム状態をメモリーに保持します。

フォーム メタモデルは、コントロールとアプリケーション ロジックを定義するために引き続き使用されます。 この方法は、ほとんどすべての既存の Form、Form DataSource、および Form Control のメタモデルと X++ のオーバーライドメソッドをサポートしています。 ただし、新しいプラットフォームでの互換性またはパフォーマンス上の理由から、一部のコントロール タイプ、プロパティ、およびオーバーライド メソッドは削除されました。 たとえば、ActiveX および ManagedHost コントロールは、HTML プラットフォームと互換性がないため、カスタム コントロールを追加するためには使用できなくなります。 代わりに、新しい拡張可能コントロール フレームワークが追加され、さらにコントロールを追加できます。

## <a name="tutorials"></a>チュートリアル
-   [レンタル料金のタイプ フォームの作成](build-rental-charge-type-form.md)
-   [顧客フォームの作成](build-customer-form.md)

## <a name="forms"></a>フォーム
-   [ナビゲーション概念](page-navigation.md)
<!---   [The new user experience](https://mix.office.com/watch/1ohsrrpsd02e1)-->
-   [レイアウト](page-layout.md)
-   [Symbol フォント](symbol-font.md)
-   [カスタム パターンを使用したテスト フォーム](testing-forms-custom-patterns.md)

## <a name="controls"></a>コントロール
-   [アクション コントロール](action-controls.md)
-   [入力コントロールとグリッド列のサイズ変更](sizing-input-controls-grid-columns.md)
-   [ツリー コントロールでのチェック ボックスのサポート](check-box-tree-controls.md)
-   [フィルター処理](filtering.md)
-   [[新しいウィンドウで開く] アイコンを使用してページを並べて表示する](../../fin-and-ops/get-started/display-pages-side-by-side.md)
-   [コードの移行 - コンテキスト メニュー](../migration-upgrade/code-migration-context-menus.md)
-   [コードの移行 - マウス ダブルクリック](../migration-upgrade/code-migration-double-click.md)
-   [ルックアップのコンテキスト データ入力](contextual-data-entry-lookups.md)
-   [HierarchyViewer コントロール](hierarchy-viewer-control.md)
-   [ルックアップ コントロール](lookups-controls.md)
-   [ファイルのアップロード コントロール](file-upload-control.md)
-   [方法: システム定義ボタン](system-defined-buttons.md)
-   [画像の使用](images-form-grid.md)
-   [入力、テーブル、およびグリッド コントロールのフォントと背景色を指定する](specify-color-font-background-controls.md)
-   [右から左へ読み書きする言語のサポート: 双方向テキストの入門書](bidirectional-support.md)
-   [ワークスペース タイル用のアイコンの作成](create-icons-workspace-tiles.md)
-   [拡張可能なコントロールのキーボード ショートカット](keyboard-shortcuts-controls.md)
-   [拡張可能なコントロール – パブリック JavaScript API](public-javascript-apis.md)

## <a name="messaging"></a>メッセージング
-   [スライダーとメッセージ ボックス](slider-messagebox.md)
-   [メッセージング API: メッセージ センター、メッセージ バー、およびメッセージ詳細](messaging-api-center-bar-details.md)
-   [ユーザーにメッセージを送信する](messaging-user.md)

## <a name="form-pattern-guidelines"></a>フォーム パターンのガイドライン
-   [フォーム パターンの選択](select-form-pattern.md)
-   [フォームのスタイルとパターン](form-styles-patterns.md)
-   [フォーム パターン アドイン](form-pattern-add-ins.md)

| フォーム パターン     | フォーム パターンのサポート       | サブ パターン      |
|---|---|---|
| [詳細マスター](details-master-form-pattern.md)<br>[詳細トランザクション](details-transaction-form-pattern.md)<br>[フォーム パート セクション リスト](section-list-form-pattern.md)<br>[リスト ページ](list-page-form-pattern.md)<br>[簡易詳細](simple-details-form-pattern.md)<br>[簡易リスト](simple-list-form-pattern.md)<br>[簡易リストと詳細](simple-list-details-form-pattern.md)<br>[目次](table-of-contents-form-pattern.md)<br>[タスク シングル](task-single-form-pattern.md)<br>[タスク ダブル](task-double-form-pattern.md)<br>[ウィザード](wizard-form-pattern.md)<br>[ワークスペース](workspace-form-pattern.md)<br>[フォームの全般的なガイドライン](general-form-guidelines.md) | [高度な選択](advanced-selection-form-pattern.md)<br>[ダイアログ](dialog-form-pattern.md)<br>[ドロップ ダイアログ](drop-dialog-form-pattern.md)<br>[ルックアップ](lookup-form-pattern.md)<br>[情報ボックス](factbox-form-patterns.md) | [カスタム フィルター グループ](custom-filter-group-subpattern.md)<br>[分析コード エントリ コントロール](../financial/dimension-entry-control-subpattern.md)<br>[分析コード式ビルダー](../financial/dimension-expression-builder-subpattern.md)<br>[フィールドおよびフィールド グループ](fields-field-groups-subpattern.md)<br>[フィルターおよびツールバー](filters-toolbar-subpattern.md)<br>[テキスト入力](fill-text-subpattern.md)<br>[水平フィールドおよびボタン グループ](horizontal-fields-buttons-group-subpattern.md)<br>[画像のプレビュー](image-preview-subpattern.md)<br>[リスト パネル](list-panel-subpattern.md)<br>[入れ子になった簡易リストおよび詳細](nested-simple-list-details-subpattern.md)<br>[セクション グラフ](section-chart-form-pattern.md)<br>[セクション Power BI](section-powerbi-subpattern.md)<br>[セクション関連リンク](section-related-links-subpattern.md)<br>[セクション積み上げグラフ](section-stacked-chart-subpattern.md)<br>[セクション タブ付きリスト](section-tabbed-list-subpattern.md)<br>[セクション タイル](section-tiles-subpattern.md) [表形式フィールド](tabular-fields-subpattern.md)<br>[ツールバーおよびリスト](toolbar-list-subpattern.md)<br>[ツールバーおよびフィールド](toolbar-fields-subpattern.md)<br>[ワークスペース フィルター グループ](workspace-filter-group-subpattern.md) |

## <a name="control-extensibility"></a>コントロールの拡張機能
-   [拡張可能コントロールの構築](build-extensible-control.md)
-   [拡張可能なコントロールのプログラミング リファレンス](extensible-control-programming-reference.md)
-   [コントロールの拡張機能](control-extensibility.md)
-   [ローカライズ可能なラベルを拡張可能なコントロールに追加する](create-localizable-labels-client.md)
-   [拡張可能なコントロール レイアウトのガイドライン](extensible-controls-layout.md)
-   [コントロールに対してタスク レコーダーが生成するテキストの制御](task-recorder-control-text.md)






