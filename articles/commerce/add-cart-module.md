---
title: カート モジュール
description: このトピックでは、カート モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696764"
---
# <a name="cart-module"></a>カート モジュール

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

このトピックでは、カート モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。

## <a name="overview"></a>概要

カート モジュールは、カートにある品目を紹介するのに必要なすべてのモジュールをホストするために使用されるコンテナーです。 たとえば、カート、注文集計、およびプロモーション コードに追加されたすべての品目が含まれます。

カート モジュールは、カート ID に基づくデータを表示します。 カート ID は、サイト全体で使用できるブラウザー Cookie です。

## <a name="cart-module-properties-and-slots"></a>カート モジュール プロパティおよびスロット

コンテナーとして、カート モジュールは、ヘッダーおよび幅などのいくつかの基本的なプロパティを制御します。 ヘッダーは通常、**ショッピング バッグ**、**カート**、または**カート内の品目**などのテキストです。 幅の設定により、コンテナー内のモジュールがそのコンテナー内に収まる必要があるかどうか、または画面を埋めれるかどうかを決定します。

カート ページは複数の領域に分割されています: カート明細行品目、"注文集計とチェックアウト、および "店舗で検索" 機能。 各領域はカート モジュールのスロットにマップされ、各スロットは事前定義された一連のモジュールを受け入れます。

## <a name="modules-that-can-be-used-in-a-cart-module"></a>カート モジュールで使用できるモジュール

- **カート明細行品目** – このモジュールでは、カートに追加された各品目の概要が表示されます。 情報には、製品タイトル、選択した分析コード、価格、数量、および割引が含まれます。 このモジュールは、"カートから削除" や "欲しい物リストに追加" などのアクションもサポートします。 明細行品目ごとに、品目を出荷する、または店舗から受け取るオプションがあります。 このオプションは、"店舗で受取り" モジュールで個別にコンフィギュレーションされる必要があります。
- **注文集計** – このモジュールは、注文集計を表示します。 情報には、小計、出荷、税、および割引が含まれます。 このモジュールに対して、ヘッダーをコンフィギュレーションできます。
- **プロモーション コード** – このモジュールにより、顧客はプロモーション コードの引換ができます。 プロモーション コードを適用または削除できます。
- **チェックアウト** – このモジュールによりチェックアウト アクションを開始し、ユーザーをチェックアウト ページにリダイレクトします。 このモジュールに対して 3 つのリンクをコンフィギュレーションする必要があります。

    - **チェックアウト** – このリンクでは、まだサインインしていない顧客にサインインさせます。
    - **ゲスト チェックアウト** – このリンクを使用すると、匿名顧客が注文できます。 顧客がサインインしていない場合にのみ表示されます。
    - **ショッピングに戻る** – このリンクを使用すると、顧客はホーム ページまたはその他のページに移動して買い物を継続できます。

- **コンテンツ リッチ ブロック** – このモジュールは、カート モジュールのカスタム メッセージングをサポートします。 メッセージは、コンテンツ管理システム (CMS) よって発生します。 "注文に関する問題については、1-800-Fabrikam にお問い合わせください" などのメッセージを追加できます。
- **店舗で受け取り** – このモジュールでは、品目の受け取り可能な近隣店舗の一覧を表示します。 既定では、このモジュールは顧客の場所から半径 50 マイル以内の店舗を表示します。 ただし、モジュールで検索する半径をカスタマイズできます。 各店舗で、在庫確認機能がオンになっている場合は、在庫確認が行われ、適切な在庫または在庫切れのメッセージが表示されます。
- **Bing Maps による店舗検索** – このモジュールは、店舗で受け取りモジュール内で使用されます。 顧客は、場所を入力することによって店舗を検索できます。 Bing Maps 位置情報アプリケーション プログラミング インターフェイス (API) は顧客が入力した場所を緯度と経度に変換するために使用します。 このモジュールを使用しない場合、顧客の現在の場所に近い店舗だけが表示され、顧客は別の場所を検索することはできません。

## <a name="cart-module-settings"></a>カート モジュール設定

カート モジュールには、コンフィギュレーション可能な 3 つの設定があります。

- **最大数量** – カートに追加できる各品目の最大数量。 たとえば、小売業者が、単一のトランザクションで販売できるのは各製品 10 個のみと決定する場合があります。
- **在庫確認** – 値が **True** に設定されている場合、購入ボックス モジュールが品目が在庫にあることを確認した後にのみ、品目がカートに追加されます。 この在庫確認は、品目が出荷されるシナリオと、品目を店舗で受け取るシナリオの両方に対して実行されます。 値が **False** に設定されている場合、品目がカートに追加されて注文が行われる前に、在庫確認は実行されません。
- **在庫バッファー** – 在庫はリアルタイムで管理されるため、多くの顧客が注文する場合、正確な在庫数を管理するのが困難な場合があります。 したがって、バッファーは在庫に対して定義できます。 在庫確認が実行されると、在庫がバッファー額を下回る場合、その製品は在庫切れとして処理されます。 したがって、在庫数が完全に同期されないよう、販売が複数のチャンネルを通じて迅速に行われる場合、在庫切れの品目が販売されるリスクは少なくなります。

## <a name="retail-server-interaction"></a>小売サーバー インタラクション

カート モジュールでは、Retail Server API を使用して製品情報を取得します。 ブラウザー Cookie からのカート ID は、小売サーバーからすべての製品情報を取得するために使用されます。

## <a name="add-a-cart-module-to-a-page"></a>カート モジュールをページに追加する

新しいページにカート モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。

1. **カート フラグメント**という名前のフラグメントを作成し、それにカート モジュールを追加します。
1. カート モジュールの**カート明細行品目**で、カート明細行品目モジュールを追加します。
1. **注文集計**スロットで、注文集計モジュールを追加します。
1. **プロモーション コード** スロットで、プロモーション コード モジュールを追加します。
1. **チェックアウト** スロットで、チェックアウト モジュールを追加します。
1. **店舗で検索**スロットで、店舗で受け取りモジュールを追加します。
1. 店舗で受け取りモジュールで、**店舗検索**スロットを選択し、Bing Maps による店舗検索モジュールを追加します。
1. フラグメントをチェックインし、公開します。
1. **カート テンプレート**という名前のテンプレートを作成し、作成したカート フラグメントをそこに追加します。
1. テンプレートを保存し、チェック イン後に発行します。
1. 新しいテンプレートを使用するページを作成します。
1. ページを保存してプレビューします。
1. ページをチェックインしてから公開します。

## <a name="additional-resources"></a>追加リソース

[スタート キットの概要](starter-kit-overview.md)

[コンテナー モジュール](add-container-module.md)

[購入ボックス モジュール](add-buy-box.md)

[チェックアウト モジュール](add-checkout-module.md)

[注文確認モジュール](order-confirmation-module.md)

[ヘッダー モジュール](author-header-module.md)

[フッター モジュール](author-footer-module.md)