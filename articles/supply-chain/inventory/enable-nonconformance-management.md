---
title: 不適合管理
description: この記事は、不適合を使用するために必要な基本設定について説明します。 品質指示を使用する場合、追加の設定が必要になります。
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc1e1eb9d8ede1d07a873ca98a1c385cf0126c3f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557527"
---
# <a name="nonconformance-management"></a>不適合管理

[!include [banner](../includes/banner.md)]

この記事は、不適合を使用するために必要な基本設定について説明します。 品質指示を使用する場合、追加の設定が必要になります。

不適合管理を有効化するには、次の手順に従います。

1.  不適合に関連した在庫および倉庫管理パラメーターを定義します。
    -   **品質管理を使用する**オプションを**はい**に設定します。
    -   **時間レート** フィールドに、国内通貨で時給レートを入力します。 時給レートは、不適合に関連する工程の原価計算に使用されます。 時間あたりのレートと算出原価は、不適合の参照情報を提供するものです。 これらは、他の機能に作用することはありません。
    -   **レポートの設定**ページの **品質管理**タブを使用して、印刷する文書のタイプを定義します。 不適合レポート、不適合タグ、または修正レポートを印刷できます。 複数のレコードを定義して、1 つのレポートに複数のドキュメント タイプを印刷したり、社内ノートや社外ノートを印刷できます。 通常は、**文書の種類**ページで、不適合用と訂正用にそれぞれ固有の文書タイプを定義することをお勧めします。 たとえば、不適合用の固有の文書タイプを使用すると、不適合に関するメモを入力できます。 この場合、レポート オプションで、一意の文書タイプを識別します。
    -   不適合および訂正参照に使用する番号順序を有効にします。

2.  不適合のユーザー承認を有効にします。 不適合を承認する必要がある各ユーザーに従業員を割り当てるには、**ユーザー** ページの**名前**フィールドを使用します。 システムは、不適合状態を変更する従業員を使用して、不適合履歴を追跡します。 ユーザーは、従業員 ID が割り当てられていない限り不適合を承認できません。
3.  不適合に割り当てられる問題タイプを定義します。 各種の不適合タイプで遭遇する品質上の問題の分類を定義するためには、**問題タイプ** ページを使用します。 次の不適合タイプを設定できます: **内部**、**顧客**、**仕入先**、**サービス要求**、**生産**、**連産品の生産**。 **不適合タイプ** ページを使用して、1 つ以上の不適合タイプで使用する問題タイプを承認します。 たとえば、欠陥コードに関連した問題タイプは、すべての不適合タイプに適用できます。一方、顧客の苦情に関する問題タイプは、**顧客**および**サービス要求**の不適合タイプにしか適用できません。
4.  欠陥材料の処理に関連した指示を提供する検査ゾーンを定義します。 不適合に割り当てることができるゾーンを定義するためには、**検査ゾーン** ページを使用します。 印刷された不適合タグには、割り当てられている検査ゾーンと欠陥材料をどのように扱うべきかの指示として使用する情報が表示されます。 ゾーンは在庫場所または運営リソースに対応する場合があります。
5.  訂正に割り当てられる診断タイプを定義します。 診断アクションの分類を定義するためには、**診断タイプ** ページを使用します。 訂正は、承認された不適合に対して行う必要のある診断アクションのタイプ、担当者などを指定します。 また、要求された完了日、予定完了日を指定します。
6.  不適合に割り当てられる、関連する工程を定義します。 **工程**ページを使用して、承認済の不適合に対して実行される作業の分類を定義します。 関連する工程を不適合に割り当てるときに、関連する材料、労働時間、雑費など、その工程を実行するために必要な条件についての詳細情報を指定することもできます。 この情報は、工程の見積原価を計算するのに使用されます。 詳細情報および見積原価は、参考目的で提供されます。 品質に関連する工程は、生産工順に対して定義できる工程とは異なります。


<a name="additional-resources"></a>その他のリソース
--------

[不適合 (タスク ガイド) を作成して処理する](tasks/create-process-non-conformance.md)

[品質管理プロセス](quality-management-processes.md)

[不適合管理の前提条件の確認 (タスク ガイド)](tasks/set-up-prerequisites-nonconformance-management.md)
