---
title: 販売時点管理 (POS) アプリケーションおよびユーザー言語の設定
description: このトピックでは、Retail Modern POS (MPOS) とクラウド POS の言語設定を変更する方法を説明します。
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: faf8cdcee70b55842072298b51789f6cd7a577af
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545103"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a>販売時点管理 (POS) アプリケーションおよびユーザー言語の設定

[!include [banner](includes/banner.md)]

このトピックでは、Retail Modern POS (MPOS) とクラウド POS の言語設定を変更する方法を説明します。

## <a name="overview"></a>概要

Retail Modern POS (MPOS) とクラウド POS は、言語設定と翻訳が店舗とユーザーの設定によって異なる場合があります。 たとえば、店舗は顧客にとって英語が最も一般的な地域に位置することができますが、一部の作業者はフランス語の翻訳でアプリケーションを使用することを好みます。

## <a name="data-language"></a>データ言語

ユーザーの設定にかかわらず、MPOS と Cloud POS は常にストアの言語設定を使用してデータに使用される翻訳を決定します。 これにより、すべてのユーザーと顧客が一貫性のあるエクスペリエンスを確保できるようになります。 データの例は次のとおりです:

- 製品
- 属性と値
- カテゴリ名
- 印刷または電子メール送信されたトランザクション受領書
- 支払方法名
- ライン ディスプレイ メッセージ

ログインする前にユーザーがわからないため、店舗の言語はメインの POS ログイン画面にも使用されます。 店舗の言語で翻訳が利用できない場合、POS は会社の言語に戻ります。

### <a name="configuring-the-stores-language-setting"></a>店舗の言語設定のコンフィギュレーション

店舗の言語設定は、**一般 &gt; 地域の設定 &gt; 言語**の**小売店舗**ページにある**すべての小売店舗**から設定します。 ドロップ ダウンを使用して、各店舗の言語を選択します。

## <a name="user-interface-language"></a>ユーザー インターフェイス言語

POS ユーザーの言語設定によって、アプリケーション ユーザー インターフェースで使用される翻訳が決まります。 これには、データと見なされないすべてのラベル、メニュー、およびリストが含まれます。 1 つの例外は POS ボタン グリッドに表示されるテキストです。 ボタン グリッドは翻訳をサポートしていないため、ボタンに定義されているテキストが常に表示されます。 翻訳されたボタンをサポートするには、別々のボタン グリッドをコピーして管理し、必要に応じてそれらをユーザーに割り当てる必要があります。

### <a name="configuring-the-users-language-setting"></a>ユーザーの言語設定のコンフィギュレーション

POS ユーザーの言語設定は、**小売 &gt; 言語**の下の**作業者**ページの**すべての作業者**から設定します。 メインのプロフィール タブでは設定しません。この設定は POS では使用されません。 ユーザーの言語が設定されていないか、翻訳が使用できない言語に設定されている場合、POS は店舗の言語に戻ります。

|             | [UI l言語]                  | [データ言語 (製品、受領書フォーマット、ライン ディスプレイなど)] |
|-------------|----------------------------|---------------------------------------------------------------|
| **会社** | 既定                    | 既定                                                       |
| **店舗**   | 会社を上書き          | 会社を上書き                                             |
| **ユーザー**    | 店舗又は会社を上書き | なし                                                         |
