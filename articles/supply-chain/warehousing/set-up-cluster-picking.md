---
title: クラスター ピッキングの設定
description: このトピックでは、クラスター ピッキングを設定する方法およびクラスター ピッキングに品目の確認を適用する方法について説明します。
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7adec850cfb473b0bfc9536dcb1ef1cfd74129a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559003"
---
[!include[banner](../includes/banner.md)]

# <a name="set-up-cluster-picking"></a>クラスター ピッキングの設定

このトピックでは、作業者がモバイル デバイスを使用してピッキング作業をクラスターにグループ化して、複数のワーク オーダーに対して 1 つの場所から品目を同時にピッキングできるようにする方法について説明します。 これは *クラスター ピッキング*と呼ばれます。

## <a name="about-cluster-picking"></a>クラスター ピッキングについて

ワーク オーダーが倉庫にリリースされると、作業者はモバイル デバイスを使用してクラスターにオーダーを割り当てることができます。 クラスターは、作業者のピッキング作業を整理します。 ワーク オーダーがクラスターに割り当てられると、作業者はクラスター ピッキングを使用して、そのオーダーのピッキング作業を実行する必要があります。 作業者は、他のピッキング方法を使用できません。 ワーク オーダーがクラスターに誤って割り当てられた場合、作業者はクラスターを破棄して、クラスターを再作成する必要があります。

必要に応じて、作業者は別の作業者にクラスターを渡すことができます。 これにより、クラスターの状態が [引渡済み] に変わります。 作業者がモバイル デバイスを使用してピッキングとプット アウェイ作業が完了したことを示したとき、出荷または積荷を Dynamics 365 for Finance and Operations クライアントで確認する必要があります。

## <a name="set-up-cluster-picking"></a>クラスター ピッキングの設定

クラスター ピッキングを有効にするには、次の設定を行う必要があります。

-   **クラスター プロファイル** – クラスター ID、使用するポジションの数、クラスターを破棄する時期、ピッキング作業の順序付けと検証の方法を自動的に生成するかどうかを指定します。

-   **作業テンプレート** – クラスター ピッキングのピッキング作業を作成する方法を定義します。

-   **場所のディレクティブ** – 品目のピッキングの場所とプット アウェイの場所を指定します。

-   **モバイル デバイスのメニュー品目** – クラスター ピッキングによって指示される既存の作業を使用するモバイル デバイス メニュー項目をコンフィギュレーションします。 次に、モバイル デバイスに表示されるように、モバイル デバイスのメニューにメニュー項目を追加する必要があります。

-   **倉庫管理パラメーター** – クラスターの ID を生成するには、使用する番号順序を指定します。

## <a name="set-up-a-cluster-profile"></a>クラスター プロファイルの設定

クラスター プロファイルを設定するには、次の手順に従います。

1.  **倉庫管理** \> **設定** \> **モバイル デバイス** \> **クラスター プロファイル** をクリックします。

2.  **新規** をクリックして、新しいプロファイルを作成します。

3.  **クラスターを作成** をクリックし、**クラスターの並べ替え** の下で、**新規** をクリックして、クラスターの並べ替え基準を設定します。 並べ替え基準は、作業者がピッキング作業を実行する順序を制御します。 必要な数だけ基準を追加できます。

4.  **順序番号** フィールドで、並べ替え基準が処理される順序を定義する番号を入力します。

5.  **フィールド名** フィールドで、並べ替えを決定するフィールドを選択します。 たとえば、**WMSLocationId** フィールドを選択した場合、作業は場所別に並べ替えられます。

6.  **並べ替え** フィールドで、次のいずれかのオプションを選択します。

| **オプション**     | **説明**                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **昇順**  | ピッキング作業は、並べ替え基準に基づいて、昇順で順序付けられます。 たとえば、並べ替え基準として **WMSLocationId** フィールドを使用し、その場所 ID が 1、2、3、および 4 の場合、最初に場所 4 からピッキングします。 |
| **降順** | ピッキング作業は、並べ替え基準に基づいて、降順で順序付けられます。 たとえば、並べ替え基準として **WMSLocationId** フィールドを使用し、その場所 ID が 1、2、3、および 4 の場合、最初に場所 1 からピッキングします。 |

## <a name="item-confirmation"></a>品目確認

クラスタ ピッキングが適用される場合、クラスタに追加される品目を確認するための品目確認書は重要です。 クラスタ ピッキング プロセス中にクラスタ ピッキングの品目を確認することができます。 設定は、製品バー コード設定に基づいています。

### <a name="set-up-item-verification-with-cluster-picking"></a>クラスタ ピッキングの品目の検証の設定

1.  モバイル デバイスのメニュー項目で、作業確認の設定フォームを次のように開きます。**倉庫管理** \> **倉庫管理** \> **設定** \> **モバイル デバイス** \> **モバイル デバイスのメニュー品目**。

2.  モバイル デバイス メニュー品目から、**作業確認の設定**を開きます。 **製品確認** オプションでは、スャンしたときにモバイル デバイスから各在庫を確認できます。
