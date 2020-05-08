---
title: 休暇タイプのコンフィギュレーション
description: Dynamics 365 Human Resources で、従業員が使用できる休暇のタイプを設定します。
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198053"
---
# <a name="configure-leave-and-absence-types"></a>休暇タイプのコンフィギュレーション

Dynamics 365 Human Resources で休暇タイプは、従業員がレポートできる休暇のタイプを定義します。 休暇タイプは、組織のニーズに応じてカスタマイズできます。 たとえば次のような休暇タイプを入力します。

- 有給休暇 (PTO)
- 無給休暇
- 有給休暇
- 病気休暇
- 病気休暇
- 家族休暇
- 短期障害者
- 忌引き休暇

## <a name="add-a-leave-type"></a>休暇タイプの追加

1. **休暇および欠勤**のページで、**リンク** タブを選択します。

2. **設定**で、**休暇および欠勤タイプ**を選択します。

3. **新規** を選択します。

4. **タイプ**に休暇のタイプを入力し、**ワークフロー ID** からワークフローを選択して、**説明**に説明を入力します。

5. **全般**で、**カテゴリ** ドロップダウンから、**なし**、**スケジュール済**、**未スケジュール**を選択します。

6. **所得コード** ドロップダウンから、所得コードを選択します。

7. **理由コードの要否**で、理由コードの要否を選択します。 理由コードを必要とする場合は、それらを追加する必要があります。 **理由コード**で、**追加**を選択し、その横にある**有効**チェックボックスをオンにします。

8. **選択したロールにアクセスを制限**で、アクセスを制限するかどうかを選択します。 次に、**この休暇タイプに対するセキュリティ ロール**でセキュリティ ロールを選択します。 セキュリティ ロールは、この手順のはじめで説明した**ワークフロー ID** で選択したワークフローで定義されています。

9. **保存** を選択します。

## <a name="configure-leave-type-rules"></a>休暇タイプ ルールの構成

1. 休暇タイプの丸めオプションを設定します。 オプションには、**なし**、**上**、**下**、**四捨五入**があります。 休暇タイプの丸めの精度を設定することもできます。

2. 休暇タイプに**休日の修正**を設定します。 このオプションを選択すると、Human Resources は作業日に含まれる休日の数を使用して、休暇タイプに対する休暇の見越計上の方法を決定します。 たとえば、クリスマスの日が月曜に当たる場合、Human Resources は、見越計上を処理するときに休暇タイプから 1 日を減算します。

   休日は作業時間カレンダーで設定します。 詳細については、[作業時間カレンダーを作成する](hr-leave-and-absence-working-time-calendar.md)を参照してください
   
## <a name="configure-preview-features"></a>プレビューの機能の構成

休暇および欠勤のプレビュー機能を有効にしている場合は、それらの設定も構成する必要があります。

[!include [banner](includes/preview-feature-leave-absence.md)]

1. 振り替えるために繰越残日数に対して休暇タイプを選択します。 繰越に新しい休暇タイプを作成することもできます。 

## <a name="see-also"></a>参照

- [休暇の概要](hr-leave-and-absence-overview.md)
- [休暇および欠勤計画の作成](hr-leave-and-absence-plans.md)
- [作業時間カレンダーの作成](hr-leave-and-absence-working-time-calendar.md)