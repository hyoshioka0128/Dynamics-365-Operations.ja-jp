---
title: 電子署名の概要
description: この記事では、電子署名の概要と使用方法を説明します。
author: maertenm
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d1d8952324bb16bcfa6a8b42fc4f157edb75cf1
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811321"
---
# <a name="electronic-signatures-overview"></a>電子署名の概要

[!include [banner](../includes/banner.md)]

この記事では、電子署名の概要と使用方法を説明します。

## <a name="what-is-an-electronic-signature"></a>電子署名とは

電子署名は、コンピューティング プロセスの開始者または承認者を確認するための ID です。 一部の業界では、電子署名は手書きの署名と同じだけの法的拘束力があります。

製薬、飲食料品、航空防衛などの規制対象業界では、規制準拠要件として電子署名が義務付けられています。 また、米国の食品医薬品局 (FDA) の規制である CFR 第 21 章第 11 部に準拠するためにも必要です。

> [!NOTE]
> 電子署名自体は、デジタル署名と同一ではありません。 電子署名は単純に手書きの署名の代わりであり、一方、デジタル署名には追加のセキュリティ対策が用意されています。 デジタル署名は、他のユーザーまたはプロセスによってデータが改ざんされていないことを確認するのに役立ちます。 また、デジタル署名は検証することができ、データに署名するために使用された証明書の所有者が、この検証に異議を唱えることはできません。 以下に説明するように、電子署名には組み込みのデジタル署名機能があります。

## <a name="electronic-signatures"></a>電子署名

重要なビジネス プロセスに電子署名を使用できます。 組み込みの電子署名機能を持つプロセスもあります。 任意のデータベース テーブルおよびフィールド用にカスタム署名要求を作成することもできます。

電子署名には組み込みのデジタル署名機能があります。 ドキュメントに署名する各ユーザーは、有効な暗号証明書を取得する必要があります。 ドキュメントに署名するときに、その証明書に関連付けられたプライベート キーが検証されます。 電子署名の情報は、監査証跡を提供するためにログに記録されます。 電子署名を設定するには、「[電子署名の設定](tasks/set-up-electronic-signatures.md)」を参照してください。

## <a name="users-who-require-access-to-electronic-signatures"></a>電子署名へのアクセスを必要とするユーザー

通常、3 種類のユーザーが、電子署名に対するセキュリティ アクセス権を必要としています。こららのユーザーとは、電子署名の管理者、署名者、電子署名の監査担当者です。

### <a name="electronic-signature-administrator"></a>電子署名の管理者

電子署名の管理者は、署名要求、一般パラメータ、および承認者を設定し、署名を検証できないときに警告を受け取ります。 既定では、**情報技術マネージャー** セキュリティ ロールに属するユーザーが、電子署名を管理するためのアクセス許可を所有しています。

### <a name="signer"></a>署名者

署名者は、署名が要求されているドキュメントおよびプロセスに電子署名を行います。 既定では、**システム ユーザー** セキュリティ ロールに属するユーザーは、ドキュメントに電子署名を行うためのアクセス許可を所有しています。

> [!NOTE]
> 署名者は、署名対象のドキュメントまたはプロセスの関連データにアクセスするために、追加のアクセス許可を必要とする場合があります。 データに変更を加え、変更に署名する必要があるユーザーは、データ変更のためのアクセス許可が必要です。 別のユーザーの代わりに署名するユーザーは、データへのアクセスが必要ない場合があります。 このタイプのユーザーの例は、従業員の変更に署名する監修者です。

### <a name="electronic-signature-auditor"></a>電子署名の監査担当者

電子署名の監査担当者は、データベース ログおよびデータベース ログから表示できる署名の確認ログを確認します。 既定では、**情報技術マネージャー** セキュリティ ロールに属するユーザーが、電子署名を監査するためのアクセス許可を所有しています。

**情報技術マネージャー**以外のロールを使用する場合は、そのロールが次の権限に割り当てられていることを確認します:

- 電子署名の失敗を表示
- データベース ログの表示

## <a name="signing-documents-electronically"></a>ドキュメントに電子的に署名する

### <a name="get-a-certificate"></a>証明書の取得

ドキュメントに電子署名を行うには、各署名者が証明書を事前に要求しておく必要があります。

> [!NOTE]
> Microsoft SQL Server の機能を使用して証明書を作成し、電子署名を有効にします。 追加の証明書または公開キー インフラストラクチャ (PKI) は必要ありません。

証明書を要求すると、公開キーとプライベート キーが作成されます。 プライベート キーは、ユーザーだけが知っているパスワードを使用して暗号化されます。 ドキュメントに電子署名を行う場合、パスワードを入力したときに ID が検証されます。

証明書を要求するには、**オプション**ページの**アカウント**タブで**証明書の取得**をクリックしてください。

署名に使用するパスワードを入力して確認する必要があります。 パスワードは、プライベート キーを保護し、証明書の使用を承認するために使用されます。 このパスワードはデータベースに保存されず、管理者を含めて他のだれも使用できません。

証明書に関連付けられたパスワードを忘れた場合は、その証明書をリセットする必要があります。 証明書をリセットしても、リセット前の証明書を使用して署名したドキュメントに影響はありません。 証明書をリセットするには、**オプション**ページで**証明書のリセット**をクリックします。

### <a name="sign-a-document-electronically"></a>ドキュメントへの電子的な署名

電子署名が要求される変更を行うと、**ドキュメントに署名**ページが表示されます。

1. **ドキュメントに署名**ページで**ドキュメント**タブをクリックし、ドキュメントに対する変更を確認します。
2. **署名**タブで理由コードを選択します。
3. コメントが必要な場合は、コメントを入力します。
4. **署名者**フィールドにユーザー ID が表示されない場合は、一覧から選択します。
5. 自分の場所が必要な場合は、その情報を入力します。
6. **OK** をクリックします

### <a name="sign-for-another-users-changes"></a>別のユーザーによる変更への署名

場合によっては、あるユーザーが行った変更に別のユーザーが署名するような場合があります。 たとえば、従業員が部品表 (BOM) に対して行った変更に監修者が署名することが求められる場合があります。 ユーザーを別のユーザーに対して署名者として指定するには、この手順を使用します。

> [!NOTE]
> 別のユーザーの変更に署名する場合、変更を行ったユーザーのワークステーションで署名を行う必要があります。 署名が行われるまで、変更を行ったユーザーは変更を保存できません。

承認者を指定するには、以下の手順を実行します。

1. **オプション**ページの**アカウント**タブで**指定の承認者**をクリックします。
2. **承認ユーザー ID** フィールドで、別のユーザーの変更に署名する必要があるユーザーの ID を選択します。
3. **ユーザー ID に対する署名**フィールドで、変更に署名してもらう必要があるユーザーの ID を選択します。