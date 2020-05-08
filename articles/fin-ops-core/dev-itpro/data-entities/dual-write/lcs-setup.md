---
title: Lifecycle Services からの二重書き込み設定
description: このトピックでは、新しい Finance and Operations 環境と新しい Common Data Service 環境間での二重書き込み接続を Microsoft Dynamics Lifecycle Services (LCS) から設定する方法について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c78752aa1544b12f61071fa06617af4ac2809233
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172995"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Lifecycle Services からの二重書き込み設定

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

このトピックでは、新しい Finance and Operations 環境と新しい Common Data Service 環境間での二重書き込み接続を Microsoft Dynamics Lifecycle Services (LCS) から設定する方法について説明します。

## <a name="prerequisites"></a>必要条件

二重書き込み接続を設定するには、管理者である必要があります。

+ テナントにアクセスできる必要があります。
+ Finance and Operations 環境および Common Data Service 環境の両方において管理者である必要があります。

## <a name="set-up-a-dual-write-connection"></a>二重書き込み接続の設定

二重書き込み接続を設定するには、次の手順に従います。

1. LCS で、プロジェクトに移動します。
2. **コンフィギュレーション**を選択して、新しい環境を配置します。
3. バージョンを選択します。 
4. トポロジを選択します。 使用可能なトポロジが 1 つだけの場合、自動的に選択されます。
5. **配置設定**ウィザードの最初の手順を完了します。
6. **Common Data Service** タブで、次の手順のいずれかを実行します。

    - テナントに Common Data Service が既にプロビジョニングされている場合、それを選択できます。

        1. **Common Data Service のコンフィギュレーション** オプションを**はい**に設定します。
        2. **使用可能な環境**フィールドで、Finance and Operations データと統合する環境を選択します。 一覧には、管理者特権を持っているすべての環境が含まれます。
        3. **同意**チェック ボックスをオンにして、使用条件に同意することを示します。

        ![テナントに Common Data Service が既にプロビジョニングされている場合の Common Data Service タブ](../dual-write/media/lcs_setup_1.png)

    - テナントに Common Data Service 環境がまだ存在しない場合、新しい環境がプロビジョニングされます。

        1. **Common Data Service のコンフィギュレーション** オプションを**はい**に設定します。
        2. Common Data Service 環境の名前を入力します。
        3. 環境を配置する地域を選択します。
        4. 環境の既定の言語と通貨を選択します。

            > [!NOTE]
            > 言語と通貨を後で変更することはできません。

        5. **同意**チェック ボックスをオンにして、使用条件に同意することを示します。

        ![テナントに Common Data Service 環境がまだ存在しない場合の Common Data Service タブ](../dual-write/media/lcs_setup_2.png)

7. **配置設定**ウィザードの残りの手順を完了します。
8. 環境の状態が**配置**になった後、環境の詳細ページを開きます。 **Common Data Service 環境情報**セクションには、リンクされている Finance and Operations 環境および Common Data Service 環境の名前が表示されます。

    ![Common Data Service 環境情報セクション](../dual-write/media/lcs_setup_3.png)

9. Finance and Operations 環境の管理者がリンクを完了するには、LCS にサインインし、**アプリの CDS にリンク**を選択する必要があります。 環境の詳細ページには、管理者の連絡先情報が表示されます。

    リンクが完了した後、状態が**環境のリンクが正常に完了しました**に更新されます。

10. Finance and Operations 環境で **データ統合**ワークスペースを開いて、使用可能なテンプレートを管理するには、**アプリの CDS にリンク**を選択します。

    ![Common Data Service 環境情報セクションのアプリの CDS ボタンににリンク](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> LCS を使用して環境のリンクを解除することはできません。 環境のリンクを解除するには、Finance and Operations 環境の**データ統合**ワークスペースを開き、**リンク解除**を選択します。