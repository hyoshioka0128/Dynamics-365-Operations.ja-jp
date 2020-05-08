---
title: 与信管理パラメーターの設定
description: このトピックでは、業務要件を満たすよう与信管理をコンフィギュレーションするために使用できるオプションについて説明します。
author: mikefalkner
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6d4ced14e51dd28d51d2081d8e92891e31eea49d
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154531"
---
# <a name="credit-management-parameters-setup"></a>与信管理パラメーターの設定

[!include [banner](../includes/banner.md)]

このトピックでは、業務要件を満たすよう与信管理をコンフィギュレーションするために使用できるオプションについて説明します。 与信管理機能の使用を開始するには、**与信および取立パラメーター** ページ (**与信および回収 \> 設定 \> 与信および取立パラメーター**) でパラメーターを設定します。

## <a name="credit-parameters"></a>与信パラメーター

**クレジット** セクションには 4 つのクイック タブがあり、与信管理を制御するパラメーターを変更できます: **与信保留**、**与信管理チェックポイント**、**与信管理統計**、**与信限度額**。 次のセクションでは、各クイック タブで使用できる設定について説明します。

### <a name="credit-holds"></a>与信保留

- 販売注文が保留中の一覧からリリースされた後に販売注文の値 (拡張価格) が変更された場合に転記ルールを再度チェックするように要求するには、**注文保留の後、販売注文の値を編集できるようにする**のオプションを**はい**に設定します。 .
- **キャンセルされた注文の理由**フィールドで、与信管理の保留時に販売注文がキャンセルされたときに既定で使用されるリリースの理由を選択します。
- **顧客与信グループの与信限度額を確認**のオプションを**はい**に設定して、販売注文の顧客が顧客与信グループに属している場合に、顧客与信グループの与信限度額を確認します。 グループの与信限度額がチェックされ、その値が十分であれば、顧客の与信限度額が確認されます。
- **支払条件が増加した場合に与信限度額を確認**のオプションを**はい**に設定して、顧客向け既定値の支払条件が販売注文の支払条件と異なるかどうかを判断するために、支払条件のランキングを確認します。 新しい支払条件のランクが元の支払条件よりも高い場合は、注文は与信管理保留になります。
- **決済割引が増加した場合に与信限度額を確認**のオプションを**はい**に設定して、顧客向け既定値の現金割引が販売注文の現金割引と異なるかどうかを判断するために、決済割引のランキングを確認します。 新しい現金割引のランクが元の現金割引よりも高い場合は、注文は与信管理保留になります。
- **変更された注文をリリースする理由**のフィールドで、変更された注文が与信管理保留から自動的にリリースされる場合に既定で使用されるリリースの理由を選択します。
- **与信限度額の期限切れ**ルールの動作をコントロールするには、**有効期限が空白の場合に与信限度額の期限切れブロック ルールを無視する**を**はい**に設定します。 有効期限が空白の場合に注文をブロックするには、このオプションを**いいえ**に設定します。
- 倉庫管理では、販売注文入力時に積荷を作成できます。 販売注文が与信保留中の場合に、販売注文明細行を積荷に残すには、**ブロックされた積荷明細行の削除**のオプションを**いいえ**に設定します。 販売注文が保留の間は、積荷を処理できません。 販売注文が与信保留中の場合に、積荷から販売注文明細行を削除するには、オプションを**はい**に設定します。 その後、積荷を処理できます。
- 販売注文は、与信管理レビューから自動的にリリースできます。 **自動的にリリースする理由**のフィールドで、販売注文が自動的にリリースされるときに既定で使用されるリリースの理由を選択します。
- 販売注文は、与信管理レビューから自動的にリリースできます。 **自動的にリリースする**のフィールドで**転記なし**を選択して、注文の保留をリリースします。 注文を保留にするプロセスは手動で実行する必要があります。 販売注文が保留中に実行された場合と同じ転記プロセスを使用して注文を転記するには、**転記付き**を選択します。

### <a name="credit-management-checkpoint"></a>与信管理のチェックポイント

与信問題の販売注文を確認するために使用するタイミングを設定できます。 **与信管理チェックポイント** クイック タブは、与信管理ルールの処理を含むドキュメントの転記プロセスを識別します。 また、見積転記または販売注文の完全な転記を行うときに、与信ルールを確認することもできます。 与信管理のブロック ルールが処理された後に懸案事項が見つかった場合に、その注文を保留にする転記プロセスを定義するには、このチェック ボックスをオンにします。

また、与信ルールが再確認されるまでの支払猶予日数を定義することもできます。 与信管理ルールを転記時に確認するように指定することもできますが、指定した支払猶予日数に対してはルールはチェックされません。 たとえば、1 日目に販売注文を確認し、確認手順に 2 日の支払猶予日数を指定したとします。 この場合、与信ルールは次の転記手順 (梱包明細の作成や注文請求の作成など) では 4 日目までは確認されません。 4 日目以降は、転記が発生するとルールが再度チェックされ、支払猶予日数は、次の転記チェックポイントに対して指定された値に変更されます。

支払猶予日数を指定しない場合は、与信管理ルールを実行するように設定されているすべての転記手順で、与信ルールがチェックされます。 販売注文を転記せずにリリースした後で、同じ注文処理手順を再度実行すると、与信ルールが再度確認されます。 たとえば、注文は確認後に保留中になり、転記があるかどうかにかかわらずリリースされます。 この場合、注文は、再度確認すると保留になります。 注文が再び保留されずに次の処理ステップに進む必要がある場合は、支払猶予日数を使用します。

一部の転記チェックポイントに対して支払猶予日数を指定できませんが、他のチェックポイントには指定できます。 すべての転記チェックポイントを設定して猶予日数を設定するか、猶予日数がないようにすべての転記チェックポイントを設定する必要があります。

- 明細行に表示される転記チェックポイントが実行されるときに与信管理ルールを実行するには、**転記**チェック ボックスをオンにします。 このチェック ボックスをオフにすると、転記プロセス全体でルールが 1 回だけチェックされます。
- **転記**チェック ボックスをオンにした場合は、ブロック ルールが再度オンになるまでに経過する支払猶予日数を指定します。 **転記**のチェック ボックスをオフにした場合は、支払猶予日数を追加することはできません。
- 明細行に表示される見積転記チェックポイントが実行されるときに与信管理ルールを実行するには、**見積**チェック ボックスをオンにします。 ほとんどの場合、**転記**フィールドは、販売注文が転記されたときに表示されるダイアログ ボックスで**いいえ**に設定されます。
- **転記**チェック ボックスをオンにした場合は、ブロック ルールが再度オンになるまでに経過する支払猶予日数を指定します。 **転記**のチェック ボックスをオフにした場合は、支払猶予日数を追加することはできません。

### <a name="credit-management-statistics"></a>与信管理統計

いくつかの与信管理統計は、**顧客**ページの**顧客の与信管理統計**情報ボックスに含まれています。 これらの統計を計算するために必要な値をいくつか指定する必要があります。 **顧客の与信管理統計**情報ボックスで次の値を計算するために使用される月数を入力します。

1. 売掛債権回転日数 1
2. 売掛債権回転日数 2
3. 平均残高 1
4. 平均残高 2
5. 平均与信限度額 %
6. 平均エクスポージャ %

### <a name="credit-limits"></a>与信限度額

- 与信管理では、顧客の与信限度額は顧客の通貨で表示されます。 与信限度額の為替レート タイプを顧客の通貨で定義する必要があります。 **与信限度額の為替レート タイプ** フィールドで、基本与信限度額を顧客の与信限度額に換算するために使用される為替レートのタイプを選択します。
- **与信限度額の手動編集を許可する**オプションを**いいえ**に設定すると、ユーザーは**顧客**ページで与信限度額を編集できなくなります。 このオプションを**いいえ**に設定した場合は、与信限度額調整トランザクションを転記することによってのみ、顧客の与信限度額を変更できます。

### <a name="number-sequences-and-shared-number-sequence-parameters"></a>番号順序と共有番号順序パラメーター

与信限度額調整を処理するには、仕訳帳 ID が必要です。 仕訳帳 ID の生成に使用する与信限度額調整番号を追加する必要があります。