---
title: モバイル ワークスペースのセキュリティを強化する
description: このトピックでは、ワークスペースへのユーザー アクセスを制限する方法について説明します。
author: makhabaz
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: makhabaz
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: a388b6aa954f1588c63bf7be83a249270bcf2407
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851453"
---
# <a name="help-secure-mobile-workspaces"></a>モバイル ワークスペースのセキュリティを強化する

[!include [banner](../../../includes/banner.md)]

このトピックでは、ワークスペースへのユーザー アクセスを制限する方法について説明します。

## <a name="assign-a-menu-item-to-workspace"></a>メニュー項目をワークスペースに割り当てる
ワークスペースはメニュー項目に関係させることができます。 ワークスペースはメニュー項目への権限を持つユーザーにのみ表示されるため、メニュー項目へのアクセス権がないユーザーは、ワークスペースを使用できません。

メニュー項目がワークスペースに割り当てられていない場合、ワークスペースは常にユーザーに表示されます。

メニュー項目を割り当てることによってワークスペースのセキュリティを確保するには、これらの手順に従います。

1. **SysAppWorkspaceSecurityAttribute** 属性をワークスペース クラスに追加して、ワークスペースに割り当てるメニュー項目を指定します。

    ![メニュー項目をワークスペースに割り当てます](media/workspace-api/SecureWorkspaceOption1.png)

2. メニュー項目とワークスペースを構築します。 変更をテストするには、メニュー項目にアクセスできないユーザー アカウントを使用してモバイル アプリにサインインします。

## <a name="override-the-workspacehidden-method"></a>WorkspaceHidden メソッドのオーバーライド
パラメーターに基づき、ワークスペースを非表示または表示するか指定することもできます。 **workspaceHidden** メソッドを上書きすることにより、次のコード例に示すように、コードでワークスペースの可視性を制御できます。

![WorkspaceHidden メソッドのオーバーライド](media/workspace-api/SecureWorkspaceOption2.png)

## <a name="add-a-menu-item-and-override-the-workspacehidden-method"></a>メニュー項目を追加して、workspaceHidden メソッドを上書きする
アプリで両方の先行メソッドを使用することができます。 メニュー項目はセキュリティ チェックを提供し、**workspaceHidden** メソッドには、ワークスペースの可視性に関連する追加ロジックが含まれています。
