---
title: ロールベース セキュリティ
description: このトピックでは、ロールベースのセキュリティの要素の概要を提供します。
author: ChrisGarty
manager: AnnBe
ms.date: 07/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecConfiguration, SysUserGroupInfo, SysSecRoleExcludeUsers
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15211
ms.assetid: 48cfdd5a-7d04-4969-93ac-6cd6d10d5a09
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a5ff11e56d7ce739236171bd386a3690652c0b7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772319"
---
# <a name="role-based-security"></a>ロールベース セキュリティ

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations のロールベースのセキュリティの要素の概要を説明します。 

ロールベース セキュリティでは、個々のユーザーではなく、セキュリティ ロールに対してのみアクセスを許可します。 ユーザーはロールに割り当てられます。 セキュリティ ロールに割り当てられているユーザーは、そのロールに関連付けられている一連の権限にアクセスできます。 任意のロールに割り当てられていないユーザーには権限がありません。 

Finance and Operations アプリでは、ロール ベース セキュリティが業務の構造で調整されます。 ユーザーは、組織内の担当と業務プロセスへの参加に基づいて、セキュリティ ロールに割り当てられます。 管理者は、ユーザーが使用する必要があるプログラム要素へのアクセスではなく、ロールのユーザーが実行する職務権限へのアクセスを許可します。 

自動ロール割り当てのルールを設定できるため、ユーザーの責任が変更されるたびに管理者が関与する必要はありません。 セキュリティ ロールとルールが設定された後、業務管理者は、業務データに基づく日常的なユーザーのアクセスを制御できます。

<a name="overview-of-role-based-security"></a>ロール ベースのセキュリティの概要
-------------------------------

このセクションでは、ロールベースのセキュリティの要素の概要を提供します。 セキュリティ モデルは階層型であり、階層内の各要素は異なるレベルの詳細を表します。 アクセス許可は、メニュー項目やテーブルなどの個々のセキュリティ保護可能なオブジェクトへのアクセスを表します。 権限は、アクセス許可で構成されており、支払のキャンセルや預金残高の処理などのタスクへのアクセスを表します。 職務は特権で構成され、銀行取引の維持などビジネス プロセスの一部を表します。 職務と権限の両方をロールに割り当てて、Finance and Operations へのアクセスを許可することができます。 

次の図は、ロールベースのセキュリティとそれらの関係の要素を示しています。 

[![ロールベースのセキュリティ フレームワークの例](./media/rbs.png)](./media/rbs.png)

<a name="security-roles"></a>セキュリティ ロール
--------------

すべてのユーザーは Finance and Operations にアクセスするため少なくとも 1 つのセキュリティ ロールに割り当てられている必要があります。 ユーザーに割り当てられたセキュリティ ロールにより、ユーザーが実行できる職務と、ユーザーが表示できるユーザー インターフェイスの部分が決まります。 

管理者は、データ セキュリティ ポリシーを適用して、ロールのユーザーがアクセス権を持つデータを制限します。 たとえば、ロールのユーザーは、単一の組織からのみ、データへアクセスできる場合があります。 管理者は、ロールのユーザーが持つ、過去、現在、および将来のレコードに対するアクセスのレベルも指定できます。 たとえば、ロールでのユーザーは、すべての期間のレコードを表示できるよう特権を割り当てられますが、現在の期間のみのレコードを変更できます。 

セキュリティ ロールによるアクセスを管理することで、ユーザーごとに個別にアクセスを管理する必要がないため管理者は時間を節約できます。 セキュリティ ロールは、すべての組織で 1 回定義されます。 さらに、ユーザーを業務データに基づくロールに自動的に割り当てることができます。 たとえば、管理者は、セキュリティ ロールで人事管理の職位に関連付けるルールを設定できます。 ユーザーがその位置に割り当てられるたびに、それらのユーザーは適切なセキュリティ ロールに自動的に追加されます。 

セキュリティ ロールは、階層構造に編成することができます。 ロール階層を使用すると、管理者は別のロールに基づいてロールを定義できます。 たとえば、販売マネージャー ロールは、マネージャー ロールおよび営業担当者ロールの親ロールとして定義されます。 親ロールは、職務、権限、およびその子ロールに割り当てられている条件を自動的に継承します。 したがって、親ロールに割り当てられているユーザーは、子ロールのユーザーが実行できるすべてのタスクを実行できます。 ロールは、1 つ以上の子ロールまたは 1 つ以上の親ロールを持つことができます。 

既定では、サンプルのセキュリティ ロールが提供されています。 すべての機能は少なくとも 1 つのサンプル セキュリティ ロールに関連付けられています。 管理者は、サンプル セキュリティ ロールにユーザーを割り当てるか、企業のニーズに合わせてサンプル セキュリティ ロールを変更するか、または新しいセキュリティ ロールを作成することができます。 既定では、サンプル ロールは階層内に配置されません。

## <a name="duties"></a>職務権限
職務は、ビジネス プロセスの一部に対応します。 管理者は、職務をセキュリティ ロールに割り当てます。 1 つの職務権限に、複数のロールを割り当てることができます。 

セキュリティ モデルでは、職務に権限が含まれます。 たとえば、**銀行トランザクションの管理**職務は、**入金伝票の生成**および**支払のキャンセル**権限を含みます。 職務および権限の両方をセキュリティ ロールに割り当てられますが、職務を使用して Finance and Operations へのアクセスを許可することをお勧めします。 

関連する職務を別々のロールに割り当てることができます。 これらの職務は分離されていると言われています。 職務を分離することにより、企業改革 (SOX)、国際財務報告基準 (IFRS)、米国食品医薬品局 (FDA) などの規制要件をよりよく遵守することができます。 さらに、職務分掌により、不正のリスクを減らし、エラーや反則を検出できます。 

既定の職務が用意されています。 管理者は、職務権限に関連付けられている権限を変更するか、新しい職務権限を作成することができます。

## <a name="privileges"></a>権限
セキュリティ モデルでは、ジョブを実行したり、問題を解決したり、割り当てを完了したりするために必要なアクセス許可のレベルが権限によって指定されます。 権限はロールに直接割り当てることができますが、職務をロールのみに割り当てることをお勧めします。 これにより、権限をまずグループ化して職務にまとめられ、メンテナンスが容易になります。 

権限には、ユーザー インターフェイス要素やテーブルなどの個別のアプリケーション オブジェクトへのアクセス許可が含まれています。 たとえば、**支払のキャンセル**権限には、支払のキャンセルに必要なメニュー項目、フィールド、およびテーブルへのアクセス許可が含まれています。 

既定では、Finance and Operations のすべての機能に対して権限が提供されます。 管理者は、権限に関連付けられているアクセス許可を変更するか、新しい権限を作成することができます。

## <a name="permissions"></a>アクセス許可
フォームまたはサービスなどの各機能は、エントリ ポイントを使ってアクセスします。 メニュー項目、Web コンテンツ項目、およびサービス工程は、総称してエントリ ポイントと呼ばれます。 

セキュリティ モデルでは、セキュリティ保護可能なオブジェクトと機能を実行するために必要なアクセス レベルは権限によってグループ化されます。 これには、エントリ ポイントからアクセスされるテーブル、フィールド、フォーム、またはサーバー側のメソッドが含まれます。