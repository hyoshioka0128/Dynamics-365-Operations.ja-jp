---
title: 機能的な場所を作成する
description: このトピックでは、資産管理で機能的な場所を作成する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01bd399e6104ec216d5c8aa80f32700df76bc514
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571832"
---
# <a name="create-functional-locations"></a>機能的な場所を作成する

[!include [banner](../../includes/banner.md)]

 

このトピックでは、資産管理で機能的な場所を作成する方法について説明します。

機能的な場所の構造を作成する場合、一度機能的な場所を作成すると、元の場所から移動できないことに注意してください。 つまり、資産管理で機能的な場所の作成を開始する前に、機能的な場所の構造を慎重に検討する必要があります。 機能的な場所を後悔している場合、まだ使用されていない場合は削除できます。

機能的な場所を操作できるようにするには、まず機能的な場所の 2 つの "カテゴリ" を作成します。

- サブ場所ではない *1 つ*の既定の機能的な場所を作成します。 この機能的な場所は、新しい資産を作成するときに資産に対する標準の場所としてのみ使用されます。  
- 会社のメンテナンス ジョブの管理に必要な機能的な場所の構造を作成します。

## <a name="create-a-default-functional-location"></a>既定の機能的な場所を作成する

機能する的な場所を使用する場合は、まず新しい資産の作成時に使用する既定の場所を 1 つ作成します。 この機能的な場所は、**資産管理** > **設定** > **資産管理パラメーター** > **資産** リンク > **既定の機能的な場所**フィールドで選択したものです。 既定の機能的な場所は、新しい資産を作成するときに使用できますが、それらの資産に対する機能的な場所の構造がまだ設定されていません。

1. **資産管理** > **共通** > **機能的な場所** > **すべての機能的な場所**を選択します。  
2. **すべての機能的な場所**で、**新規**を選択します。
3. **機能的な場所**フィールドに "0000" や "既定" などの ID を挿入し、これが特別な機能的な場所であることを示します。
4. **名前**フィールドに、既定の機能的な場所の名前を挿入します。
5. **親**フィールドで親を選択*しない*でください – フィールドは空白のままにします。
6. **機能的な場所タイプ** フィールドで、既定の機能的な場所に使用する機能的な場所タイプを選択します。 機能的な場所タイプの設定方法の詳細については、[機能的な場所タイプ](../setup-for-functional-locations/functional-location-types.md) を参照してください。
7. **OK** を選択します。 この機能的な場所は、会社が使用する機能的な場所に資産をインストールするまで新しい資産の一時的な場所としてのみ使用されるため、ここにデータを追加しないでください。

## <a name="create-functional-locations"></a>機能的な場所を作成する

次の手順では、会社のメンテナンス管理に必要な機能的な場所を作成する方法について説明します。

1. **資産管理** > **共通** > **機能的な場所** > **すべての機能的な場所**を選択します。 グリッド ビューまたは詳細ビューから機能的な場所を作成できます。
2. **新規**ボタンを選択します。
3. **機能的な場所**フィールドに ID を挿入します。
4. **名前**フィールドに、機能的な場所の名前を挿入します。
5. 機能的な場所が構造内のサブ場所である場合は、**親**フィールドの親場所を選択します。
6. **機能的な場所タイプ** フィールドでタイプを選択します。
7. **OK** を選択します。
8. 機能的な場所を選択し、**編集**ボタンをクリックして詳細情報を追加します。

>[!NOTE]
>機能的な場所のライフサイクル状態の設定によっては、機能的な場所に対するすべてのサブ場所を作成し、資産のインストールを開始する前に機能的な場所のライフサイクル状態を変更することが必要な場合があります。 資産インストールの詳細については、[機能の場所への資産のインストール](../functional-locations/install-objects-on-functional-locations.md) を参照してください。 機能的な場所のライフサイクル状態の設定の詳細については、[機能的な場所のライフサイクル状態](../setup-for-functional-locations/functional-location-stages.md) を参照してください。

詳細ビューには、機能的な場所に関する情報を追加および編集できるクイック タブが表示されます。

## <a name="general-information"></a>一般情報

このセクションでは、機能的な場所の構造での親情報および子情報の概要を説明します。 **詳細**セクションでは、機能的な場所に関連する資産属性、メンテナンス計画、および資産の数を確認できます。 **在庫**セクションでは、機能的な場所に関連するサイトおよび倉庫を選択できます。 サイトおよび倉庫は、ワーク オーダー品目予測に関連して使用されます。 品目予測を作成すると、資産の機能的な場所からサイトおよび倉庫情報が自動的に使用されます。 **ライフサイクル状態**セクションでは、機能的な場所のライフサイクル状態に関する情報が表示されます。

## <a name="installed-assets"></a>インストール済資産

資産インストールの詳細については、[機能の場所への資産のインストール](../functional-locations/install-objects-on-functional-locations.md) を参照してください。 このクイック タブの**表示**ボタンを使用して、クイック タブにより多くのフィールドを表示できます。 **発効日**および**サブ資産**フィールドをグリッドに表示できます。

## <a name="asset-attribute-requirements"></a>資産属性の要件

このクイック タブでは、機能的な場所にインストールする資産の特定の属性要件を追加できます。 これらの要件は、情報提供のみを目的としています。 他の属性要件を持つ資産をインストールするのを妨げるものではありません。 **明細行の追加**を選択して、属性タイプを選択します。 次に、該当する**値**を挿入し、**しきい値基準**フィールドでしきい値を選択し、レコードを保存します。

## <a name="maintenance-plans-and-maintenance-rounds"></a>メンテナンス計画およびメンテナンス ラウンド

ここでは、開始日を含むメンテナンス計画とメンテナンス ラウンドを機能的な場所に追加できます。 機能的な場所にインストールされている資産には、他のメンテナンス計画が設定されている場合があります。 すべてのメンテナンス計画およびメンテナンス ラウンドは、機能的な場所および現在インストールされている資産の資産カレンダー エントリのスケジューリングに使用できます。

>[!NOTE]
>**すべての機能的な場所**詳細ビュー > **メンテナンス計画**クイック タブで、メンテナンス計画の資産タイプ、資産ブランド、資産モデルの設定の更新をする場合、メンテナンス計画をスケジューリングした後、機能的な場所に関連する既存のメンテナンス スケジュール エントリは自動的に削除されます。 機能的な場所の更新されたメンテナンス計画設定に対応する新しいスケジュール エントリを作成するには、その機能的な場所に対する新しいメンテナンス計画スケジュールを実行する必要があります。 

## <a name="address"></a>住所

**アドレス** クイック タブに、機能的な場所アドレスを挿入します。 機能的な場所のアドレスは継承されます。つまりサブ場所にアドレスが定義されていない場合は、親場所のアドレスが使用されます。

## <a name="workers"></a>作業者

このクイック タブでは、機能的な場所に所属する作業者を追加し、作業者の基本として機能的な場所を選択できます。 

## <a name="attributes"></a>属性

このクイック タブでは、機能的な場所属性の値を設定できます。 これらの属性を使用して、構造プロパティ、建物タイプ、エリアの説明、地上または地下の場所など、機能的な場所に関連するプロパティまたは特性を記述できます。

**明細行の追加**を選択して、属性タイプを選択します。 次に、属性タイプに関連付けられている**値**を挿入し、レコードを保存します。

## <a name="financial-dimensions"></a>財務分析コード

機能的な場所の財務分析コードを選択できます。 [機能的な場所タイプ](../setup-for-functional-locations/functional-location-types.md) は、機能的な場所からの財務分析コードを自動的に更新できるように設定できます。 つまり、財務分析コードにインストールされた資産は、機能的な場所の財務分析コードを自動的に取得します。 これは、場所に応じて異なるコスト センターが必要な場合に便利です。

**サイト**、**倉庫**、**アドレス**、および**財務分析コード**に関するデータが親機能的な場所で更新されると、更新中に行われるその選択に応じて、サブ機能的な場所が更新されます。 ダイアログが開き、更新オプションが提供されます。

## <a name="copy-a-functional-location-structure"></a>機能的な場所の構造をコピーする

会社に類似した場所構造を持つ複数の機能的な場所がある場合、資産管理のコピー機能を使用して、類似した複数の場所階層をすばやく作成できます。 特定の機能的な場所または構造全体をコピーすると、新しい場所または構造はコピーした名前と同じ名前になります。 コピー手順の完了後、新しい機能的な場所に対して選択した機能的な場所のライフサイクル状態で許可されている場合、新しい機能的な場所の名前または他の設定を簡単に変更できます。

1. **すべての機能的な場所**で、コピーする機能的な場所を選択します。 たとえば、サブ場所を含む機能的な場所の構造全体をコピーする場合は、一番上の場所 (親) を選択します。
2. **機能的な場所の構造をコピーする**ボタンを選択します。 リスト ページで選択した場所が、**コピー元**フィールドに表示されます。
3. **新しい機能的な場所**フィールドに新しい場所の名前を挿入します。
4. **親で貼り付け**フィールドでは、作成する場所が既存の機能的な場所構造の一部である必要がある場合にのみ、親 ID を挿入する必要があります。
5. **OK**をクリックします。 新しい機能的な場所構造は、**すべての機能的な場所**に表示されます。

>[!NOTE]
>機能的な場所構造をコピーすると、新しい構造での機能的な場所のライフサイクル状態は、機能的な場所用に作成した "最初の状態" に設定されます。 **すべての機能的な場所**で**名前変更**および**削除**ボタンを使用して、機能的な場所の名前変更または削除ができるかどうかは、機能的な場所の現在のライフサイクル状態によって異なります。

## <a name="delete-a-functional-location"></a>機能的な場所の削除

削除しようとしている機能的な場所のいずれかに資産がインストールされていない場合、および現在の機能的な場所のライフサイクル状態が許可している場合は、関連するサブ場所を持つ機能的な場所を削除できます。

1. **すべての機能的な場所**で、削除する機能的な場所を選択します。
2. 必要に応じて、機能的な場所を、機能的な場所の削除を許可する機能的な場所のライフサイクル状態に更新します。
3. **削除**を選択します。

>[!NOTE]
>機能的な場所を削除できない場合は、代わりに、この目的用に機能的な場所のライフサイクル状態を設定して削除を処理できます。 たとえば、**機能的な場所のライフサイクル状態**フォームで、有効な状態であってはならない "仕損済" または "削除済" 状態を設定できます。