---
title: 現金管理の改善
description: このトピックでは、Dynamics 365 Commerce の POS で現金管理の改善について説明します。
author: anpurush
manager: AnnBe
ms.date: 05/21/2019
ms.topic: article
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
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0c561c39dfcbfa739c5a22394c05191e7f9bc107
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127701"
---
# <a name="cash-management-improvements"></a>現金管理の改善

[!include [banner](includes/banner.md)]


現金管理は、現物店舗の小売業者にとって重要な機能です。 小売業者は、店舗内のレジスターとレジ担当者間にて、現金の完全なトレーサビリティと責任、および動きが分かるシステムを店舗に必要としています。 すべての相違点を調整し、説明責任を決定を可能にする必要があります。


Microsoft Dynamics 365 Commerce は、販売時点管理 (POS) アプリケーションでの現金管理機能を備えています。 ただし、バージョン 10.0.3 よりも前のバージョンの小売では、現金管理機能は店舗での現金移動を完全に追跡できないほど堅牢ではありません。 小売業者は店舗の現金を調整できますが、現金不一致が発生した場合には、説明責任を正確に判断することはできません。


Retail バージョン 10.0.3 以降、小売業者は現金の処理に関するトレーサビリティを取得します。 このトレーサビリティの一部として、小売業者は安全を定義し、両面の現金トランザクションを作成し、現金管理トランザクションを調整することができます。

## <a name="set-up-traceability-and-define-safes"></a>トレーサビリティの設定と安全の定義

新しい現金管理機能を設定するには、次の手順に従って店舗の機能プロファイルをコンフィギュレーションします。

1. **Retail と Commerce\> チャネル設定 \> POS の設定 \> POS プロファイル \> 機能プロファイル** の順に移動し、現金管理利用を改善したい店舗にリンクされた機能プロファイルを選択します。
2. 機能プロファイル**機能** FastTab で、**詳細な現金管理**の下にある、**現金トレーサビリティを有効化**オプションを**はい**に設定します。
3. 安全を設定するには、**Retail と Commerce \> チャネル \> 店舗 \> すべての店舗**の順に移動し、店舗を選択します。
4. **店舗**ページの、アクション ペインで、**設定**タブの**設定**グループで、**安全**を選択します。 このオプションを使用すると、店舗の複数の安全を定義および管理できます。
4. 機能を使用する前に、**1070 チャネル構成**ディストリビューション スケジュール ジョブを実行して、構成をチャネル データベースに同期する必要があります。

## <a name="additional-cash-management-changes"></a>追加の現金管理の変更

Retail 10.0.3 以降では、現金トランザクションに関連する次の機能も提供されます。

- 「開始金額の申告」を要求されるユーザーは、現金のソースを入力する必要があります。 ユーザーは、店舗で定義されている使用可能な安全を検索し、レジスターに入れることができるように現金が取り出されている安全を選択できます。
- 「支払/入金の削除」操作を行うユーザーは、未処理の「釣銭入力」トランザクションの一覧で、操作が行われているトランザクションを選択するように求められます。 対応する釣銭入力がシステムに存在しない場合、ユーザーはリンクされていない支払/入金削除トランザクションを作成できます。
- 「釣銭入力」操作を行うユーザーは、未処理の「支払/入金の削除」トランザクションの一覧で、釣銭入力操作が行われているトランザクションを選択するように求められます。 対応する支払/入金削除がシステムに存在しない場合、ユーザーはリンクされていない釣銭入力トランザクションを作成できます。
- 「安全保管」を作成したユーザーが、現金が落とされている安全な場所を選択するように求められます。
- 店舗で定義されている安全については、ユーザーは開始金額の申告、釣銭入力の実行、支払/入金削除の実行、および銀行入金の作成などの操作を管理できます。
- 適切なユーザー特権を持つユーザーに対して、「シフト管理」操作では、有効、中断、およびブラインド クローズ済みシフトの現金残高が表示されます。
- シフト内またはシフト間の現金トランザクションを調整するには、調整するシフトを選択し、**調整**を選択します。 開いているビューには、調整済および未調整のトランザクションの一覧が個別のタブに表示されます。 このビューから、ユーザーは未調整トランザクションを選択して調整するか、以前に調整したトランザクションを選択して未調整にすることができます。
- 調整中に、選択したトランザクションのバランスが取れない場合、ユーザーは不均衡調整の理由説明を入力する必要があります。 ユーザーは、単一のトランザクションを選択し、必要に応じて、関連する理由の説明に従って調整することができます。
- シフトが終了するまで、ユーザーはトランザクションを調整したり、未調整にすることができます。 シフトを終了した後は、トランザクションを調整することはできません。
- シフトの終了を選択した場合、Commerce はシフトに未調整の現金管理トランザクションが含まれていないことを検証します。 未調整トランザクションがある場合、ユーザーはシフトを終了させることはできません。