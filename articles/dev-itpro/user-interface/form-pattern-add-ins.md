---
title: フォーム パターンをサポートしている Visual Studio アドイン
description: Visual Studio のツールには、パターンの使用をサポートするいくつかのアドインが含まれています。
author: jasongre
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 28891
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ffa9e3c8f91c417634bfcdbece7a6b33799b1e77
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851159"
---
# <a name="visual-studio-add-ins-that-support-form-patterns"></a>フォーム パターンをサポートしている Visual Studio アドイン

[!include [banner](../includes/banner.md)]

Visual Studio のツールには、パターンの使用をサポートするいくつかのアドインが含まれています。 

## <a name="form-statistics-add-in"></a>フォーム統計アドイン
**フォーム統計情報** アドインは、フォームのパターン使用状況の概要を提供します。 **Dynamics 365** メニューから **フォームの統計情報** アドインにアクセスすると、すべてのフォームの統計情報を表示します。 フォーム デザイナーで開いているフォームのショートカット メニューからアドインにアクセスしたとき、アドインにそのフォームのみの統計情報が表示されます。 

![フォーム統計レポート](media/form-statistics.png) 

## <a name="forms-pattern-report"></a>フォームのパターン レポート
**フォーム パターン**レポートは、フォームがトップレベル フォーム パターンを使用するかどうか、ユーザー定義のフォームかどうか、フォーム パターンを指定しないかどうかなど、すべてのフォームについてのパターン情報を示します。 **フォーム パターン** レポートを生成するには、Microsoft Visual Studio を起動し、**DYNAMICS 365**  メニューをクリックし、**アドイン** を展開してから **フォーム パターン レポートを実行** をクリックします。 このプロセスは数秒かかります。 レポートが生成されると、ダイアログ ボックスにレポートの場所を提供します。指定された場所を参照し、Microsoft Excel でファイルを開きます。興味のあるモデルまでレポートをフィルター処理することができます。

Visual Studio アドインの詳細については、[Visual Studio 用のツールおよびアドイン](../dev-tools/developer-tools-add-ins.md)を参照してください。
