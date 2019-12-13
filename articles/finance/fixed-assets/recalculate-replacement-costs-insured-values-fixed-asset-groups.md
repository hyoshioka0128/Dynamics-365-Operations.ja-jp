---
title: 固定資産グループの交換費用と保証金額の再計算
description: この記事は、固定資産の交換費用と保証金額を更新するプロセスを説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9dd04072b4845fe5df2a918b64ba1835ea584dd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187110"
---
# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a>固定資産グループの交換費用と保証金額の再計算

[!include [banner](../includes/banner.md)]

この記事は、固定資産の交換費用と保証金額を更新するプロセスを説明します。

定期的に、特定の固定資産を交換または保証する費用が変化したことが通知される場合があります。 たとえば、前年が 3 パーセントのインフレであったため、すべての固定資産の交換費用を 3 パーセントだけ増やす必要があるという連絡を、マネージャから受け取る場合などです。 

**固定資産** ページで固定資産の交換費用と保証金額を個別に編集することもできますが、**交換費用と保証金額の更新** ページを使用すると、資産のグループ全体でのこれらの値を一度に更新できます。 ここでは、固定資産グループの値またはグループ内の特定資産の値を更新する方法を説明します。

## <a name="how-values-are-updated"></a>値の更新方法
固定資産グループの交換費用および保証金額を再計算するには、最初に既存の交換費用および保証金額を変更する率を指定した後、定期更新を実行して、実際に値を再計算する必要があります。 変更率は、**固定資産グループ** ページの **交換費用係数** および **保証金額係数** フィールドで指定します。 これらの係数は固定資産グループに対して指定しますが、**交換費用と保証金額の更新** ページを使用すると、グループ内の特定の固定資産についてのみ、交換費用と保証金額の再計算を行うことができます。 

**交換費用と保証金額の更新** ページを使用して資産の交換費用および保証金額を再計算する場合は、次の式が使用されます。

-   \[(資産グループの交換費用係数 / 100) + 1\] \* 資産の既存の交換費用
-   \[(資産グループの保証金額係数 / 100) + 1\] \* 資産の既存の保証金額

> [!NOTE] 
> **交換費用と保証金額の更新** ページを使用するときは、交換費用と保証金額の両方が、選択した資産について更新されます。どちらか一方の値のみを更新するようには指定できません。 一方の値を同じままにして他方の値を更新するには、**固定資産グループ** ページで係数として 0 (ゼロ) を入力します。 係数にゼロを指定するか空白のままにすると、更新で計算が省略されます。 固定資産の簿価額および正味簿価額は、定期更新では更新されません。 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a>日付を使用して、更新する品目を選択する方法
既定では、選択された資産のうち、当日に更新されていないものが更新プロセスで更新されますが、その資産が前日までに更新されている可能性があります。 たとえば、&lt; 現在の日付は「今日の日付より前」になります。 **選択** ボタンをクリックすると、**交換費用と保証金額の更新** ページで日付を変更することができます。 指定した日付条件は、その資産が最後に定期更新された日付と比較されます (**固定資産** ページの **値/原価の最後の定期更新** フィールド)。 固定資産の交換費用または保証金額が正常に更新されるたびに、**値/原価の最後の定期更新** フィールドが当日の日付で自動的に更新されます。 

例 

昨日、車両、オフィス家具、および建物の各グループの交換費用を 5% 更新しており、これらの資産については正しく更新されているものと考えられます。 今日、他のすべての固定資産を更新するときにこれらの資産を除外するには、**値/原価の最後の定期更新** フィールドに、昨日より前の日付 (&lt; 昨日の日付) を入力します。このようにすると、**車両**、**オフィス家具**、**建物** のグループの最後の更新は、入力した日付条件の範囲外で行われたことになります。

## <a name="cumulative-effect-of-each-update"></a>各更新の累積効果
各更新には累積効果があります。 したがって、更新は慎重に計画する必要があります。 たとえば、火曜日にすべての資産を 3% 上げ、金曜日にオフィス家具を 4% 上げた場合は、オフィス家具は合計 7.12% 上昇することになります。

## <a name="scenario"></a>シナリオ
マネージャから、固定資産に対する次のような変更を指示されました。
-   コンピュータを除くすべての固定資産の交換費用を、3.25% 高くする。
-   すべてのオフィス家具の交換費用を、さらに 1% 高くする。
-   すべてのコンピュータの交換費用および保証金額を、10% 低くする。

次の変更を行います。
1.  **オフィス家具** グループと **コンピューター** グループを除くすべての固定資産グループについて、**固定資産グループ** ページで、**交換費用係数** フィールドに 3.25、そして **保証金額係数** フィールドに 0 と入力します。
2.  **オフィス家具** グループについては、**交換費用係数** フィールドに 4.25、そして **保証金額係数** フィールドに 0 と入力します。
3.  **コンピューター** グループについては、**交換費用係数** フィールドに -10、**保証金額係数** フィールドに -10 と入力します。
4.  **交換費用と保証金額の更新** ページで、**OK** をクリックし、すべての固定資産の再計算を実行します。

翌日、マネージャーから、コンピュータは 10% ではなく、8% 下げるように指示されたため、交換費用と保証金額を修正する必要があります。 誤りを修正するには、2 つの方法があります。
-   **コンピューター** 固定資産グループの各固定資産ごとに、**固定資産** ページの **保証金額** フィールドと **交換費用** フィールドを手作業で変更します。 元の金額を 8% だけ減らしたかのように計算して、値を手作業で入力します。 この方法を使用することで、**交換費用と保証金額の更新** ページは使用しません。
-   **固定資産グループ** ページの **交換費用係数** フィールドと **保証金額係数** フィールドに、**コンピューター** グループの交換費用と保証金額の係数を入力します。 これは、資産を元の値 (10% 下げる前) にリセットしてから、元の値を 8% 下げる方法です。 その後、**交換費用と保証金額の更新** ページを使用し、入力した係数に応じて値を再計算します。

> [!NOTE]  
> 正の係数 10 (または –10 と –8 の差の係数 2) を入力して、-10 という係数を元に戻すことはできません。これでは、正しい金額は算出されません。 




