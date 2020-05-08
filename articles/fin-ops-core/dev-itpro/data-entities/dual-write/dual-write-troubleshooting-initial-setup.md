---
title: 初期設定中に発生した問題に関するトラブルシューティング
description: このトピックでは、Finance and Operations アプリと Common Data Service においてデュアル書き込み統合の初期設定を行う際に、発生する可能性がある問題を修正するトラブルシューティング情報を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 76e104c9ebd7db7ebcbaf214e84be6c4353e8a73
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275444"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>初期設定中に発生した問題に関するトラブルシューティング

[!include [banner](../../includes/banner.md)]



このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。 このトピックでは、 デュアル書き込み統合の初期設定を行う際に、発生する可能性がある問題を修正するトラブルシューティングに特化した情報を提供します。

> [!IMPORTANT]
> このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。 各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。

## <a name="you-cant-link-a-finance-and-operations-app-to-common-data-service"></a>Finance and Operations アプリを Common Data Service にリンクさせることはできません。

**デュアル書き込みの設定に必要なロール:** Finance and Operations アプリと Common Data Service 両方のシステム管理者権限。

一般的には、 **Common Data Serviceへのリンク設定** ページで発生するエラーは、設定が不完全な場合やアクセス権限の問題が原因で発生するします。 次の図に示すように、**Common Data Serviceへのリンク設定** ページで正常性チェック全体が合格になっていることを確認してください。 正常性チェック全体で合格しない限りは、デュアル書き込みをリンクすることはできません。

![正常性チェックの成功](media/health_check.png)

Azure AD 環境と Finance and Operations 環境えおリンクするには、Common Data Service テナント管理者の資格情報が必要です。 環境をリンクした後は、ユーザーはアカウントの資格情報を使用してログインし、既存のエンティティ マッピングを更新できます。

## <a name="error-when-you-open-the-link-to-common-data-service-page"></a>Common Data Service ページへのリンクを開いた際のエラー

**問題の解決に必要な資格情報：** Azure ADテナント管理者

Finance and Operations アプリで **Common Data Serviceへのリンク** を開いた際に、次のエラー メッセージが表示される場合があります。

*応答状態コードが成功とならない: 404 (Not Found)。*

このエラーは、同意の手順が完了していない場合に発生します。 同意の手順が完了しているかどうかを検証するには、Azure AD テナント管理者のアカウントを使用して portal.Azure.com にログインし、ID **33976c19-1db5-4c02-810e-c243db79efde** を持つサードパーティ製のアプリが Azure AD**エンタープライズ アプリケーション** のリストに表示されるかどうかを確認します。 これが存在しない場合は、アプリの同意をする必要があります。

アプリへの同意をするには、次の手順を実行します。

1. 管理者の資格情報を使用して、次のURLを開きます。 同意を求めるメッセージが表示されます。

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. ご利用のテナントで ID **33976c19-1db5-4c02-810e-c243db79efde** が含まれているアプリのインストールに同意していることを示す場合は、**同意する** を選択します。

    > [!TIP]
    > このアプリは、Common Data Service および Finance and Operations アプリをリンクするために必要となります。 この手順に問題がある場合は、ブラウザーを incognito モード（Google Chrome の場合）または InPrivate モード（Microsoft Edge の場合）で開きます。

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a>会社のデータとデュアル書き込みのチームがリンク設定中に正しく設定されていることを確認する

デュアル書き込みが正常に機能するように、設定時に選択した会社は Common Data Service 環境で作成されます。 既定では、これらの会社は読み取り専用となっており、**IsDualWriteEnable** プロパティは **True** に設定されています。 さらに、既定の所有権を持つ業務部門の所有者とチームが作成され、会社名が含まれます。 マッピングを有効にする前に、既定のチームの所有者が指定されていることを確認してください。 **会社 (CDM \_Company)** エンティティを検索するには、次の手順に従います。

1. Dynamics 365 のモデル駆動型のアプリで、右上隅のフィルターを選択します。
2. ドロップダウン リストにて、**会社** を選択します。
3. 結果を表示するには、**実行** を選択します。
4. デュアル書き込みの構成時にリンクしていた会社を選択します。
5. **既定の所有チーム** フィールドに値が設定されていることを確認します。 次の図では、**既定の所有チーム** フィールドが **USMF デュアル書き込み**に設定されています。

    ![既定の所有チームを確認する](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-entities-or-companies-that-can-be-linked-for-dual-write"></a>デュアル書き込み対してにリンク可能な、法人または会社数の制限を確認する

マッピングを有効化した際に、次のエラー メッセージが表示される場合があります。

*デュアル書き込みエラー: プラグインの登録に失敗しました：\[（プロジェクト DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea のパーティション マッピングを取得できません。エラー DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea で許容されるマッピングの最大パーティション数を超過超しました）\]、1 つまたは複数のエラーが発生しました。*

現在のところ、環境をリンク可能な法人の制限は、約 40 件です。 このエラーは、マッピングを有効化する際に発生し、環境間で 40 以上の法人がリンクされている場合に発生します。