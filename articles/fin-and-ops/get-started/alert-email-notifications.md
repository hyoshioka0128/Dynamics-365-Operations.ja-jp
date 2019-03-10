---
title: 電子メールによるクライアント警告通知
description: このトピックでは、定義済のイベントが発生する電子メール通知を送信するルールを設定する方法について説明します。
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 314f04eec04a75aed058c9c38066738e8758f653
ms.sourcegitcommit: 440ebe14ad26574ba227d23ee8370f6b6110645b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2019
ms.locfileid: "373793"
---
# <a name="client-alert-notifications-by-email"></a>電子メールによるクライアント警告通知

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 for Finance and Operations で、データのフィルター処理されたビューを監視し、定義済のイベントが発生した場合に、電子メール通知を自動的に送信するカスタム警告ルールを定義できます。 電子メール通知を送信するオプションは、サポートされているすべての警告タイプで使用可能であり、既存の警告ルールでも有効にできます。

組み込みのコントロールを使用して、システム バッチ ジョブのフィルタ処理されたビューを監視する警告ルールを作成できます。 **ステータス**フィールドの値を監視することで、バッチ ジョブが失敗したときに電子メールを送信する警告ルールも設定できます。 これらの警告ルールを作成した後は、ビジネス データへの変更についてレポートを確認する必要はなくなりました。 代わりに、Finance and Operations のインテリジェントな変更検出サービスに監視させることができます。

クライアントの警告は、Microsoft Office との統合を通じて提供される電子メール サブシステムによって異なります。 電子メールの配信がローカル メール クライアントに依存する必要がないように、Simple Mail Transfer Protocol (SMTP) プロバイダーを使用することをお勧めします。

電子メールで通知を送信するには、顧客が統合電子メール サービスをコンフィギュレーションする必要があります。 電子メール通知は、警告の所有者に代わって受信者に送信されます。

Finance and Operations で電子メールをコンフィギュレーションする方法の詳細については、[電子メールのコンフィギュレーションと送信](../organization-administration/configure-email.md)をご覧ください。

次の図は、**電子メールの送信**オプションを含む**警告ルールの作成**ダイアログ ボックスを示しています。

[![ 電子メールの送信オプションがはいに設定されている警告ルールの作成ダイアログ ボックス](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> **電子メールの送信**オプションが**はい**に設定されている場合、警告通知はアクション センターから配信され続けます。

## <a name="alert-notification-email-templates"></a>警告通知用電子メール テンプレート

このサービスは、警告通知の基本詳細情報を配信する定義済の電子メール テンプレートを使用して、電子メール通知を送信します。 これらの詳細には、警告ルールが定義されたページへの直接リンクが含まれます。

次の図は、電子メールで受信された時の警告通知の構造を表示します。

[![レコードの作成、フィールドの変更、およびテンプレート削除のためのテンプレートに基づく警告通知](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)