---
title: バッチジョブ履歴のクリーンアップ
description: ここではMicrosoft Dynamics 365 for Finance and Operationsにおいて、バッチ ジョブ履歴をクリーンアップする方法について情報を提供します。
author: hasaid
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: Platform update 25
ms.openlocfilehash: f59e58383075a3a4a5d7ea970e11d57d473ffb57
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851437"
---
# <a name="clean-up-the-job-batch-history"></a>バッチジョブ履歴のクリーンアップ

[!include [banner](../includes/banner.md)]

バッチ ジョブを実行すると、実行履歴が記録されます。 この履歴によって、ジョブが正しく実行されているか管理することができます。 複数のバッチ ジョブが作成されている場合で、特に実行頻度が高いバッチ ジョブには大量のジョブ実行履歴が生成されます。 履歴テーブルにエントリが多すぎる場合は、将来的にジョブのパフォーマンス低下につながる可能性があります。

**システム管理**モジュールには2つのページが追加されており、バッチ ジョブ履歴のクリーンアップが容易になっています。

- バッチ ジョブ履歴のクリーンアップ
- バッチ ジョブ履歴クリーンアップをカスタマイズする

![システム管理の定期処理タスク](./media/Menu-Cleanup.png)

> [!NOTE]
> 定期的にバッチ ジョブ履歴をクリーンアップすることと、この作業を業務時間外に行うことを推奨します。

## <a name="batch-job-history-clean-up"></a>バッチ ジョブ履歴のクリーンアップ

この手順では、指定した日数よりも古い履歴の全エントリを手早くクリーンアップします。

1. **システム管理の定期処理タスク** モジュールで、 **バッチ ジョブ履歴クリーンアップ** を選択します。
2. **履歴の範囲 (日数)** フィールドで、バッチ ジョブの履歴を保存する日数を指定します。
3. **OK** を選択します。

![定期的なジョブ](./media/batch-cleanup-regular.png)

## <a name="batch-job-history-clean-up-custom"></a>バッチ ジョブ履歴のクリーンアップ (カスタマイズ)。

カスタムのバッチ ジョブでは追加フィルターが適用され、ステータス、ジョブの概要、会社、またはユーザー名などのキーワードに基づいて抽出できます。 フィルター条件を追加するには、**フィルタ**ボタンを選択します。

1. **システム管理の定期処理タスク** モジュールで、 **バッチ ジョブ履歴クリーンアップ**  (カスマイズ) を選択します。
2. **履歴の範囲 (日数)** フィールドで、バッチ ジョブの履歴を保存する日数を指定します。
3. **レポートに含めるレコード** クイック タブで、必要なフィルタ条件を指定し **OK** を選択します。
4. **OK** を選択します。

![カスタマイズ ジョブ](./media/batch-cleanup-custom.png)
