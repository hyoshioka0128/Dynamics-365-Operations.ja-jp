---
title: Dynamics 365 for Finance and Operations バージョン 8.1.1 (2018 年 11 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations version 8.1.1 の新機能または変更された機能について説明します。 このバージョンは 2018 年 11 月にリリースされました。
author: tonyafehr
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: ''
ms.assetid: b364a31c-52d3-45c5-b698-64c5242c592a
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Release 8.1.1
ms.openlocfilehash: cad33f36d157b724a0f8704994e3409261b0e4b6
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863509"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-version-811-november-2018"></a>Dynamics 365 for Finance and Operations バージョン 8.1.1 (2018 年 11 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations version 8.1.1 (2018 年 11 月) の新機能または変更された機能について説明します。 このバージョンは 2018 年 11 月にリリースされ、ビルド番号は 8.1.170 です。

Microsoft Dynamics 365 for Retail の新機能と変更についての最新のリリースでについては、[Dynamics 365 for Retail の新機能と変更](https://docs.microsoft.com/dynamics365/unified-operations/retail/get-started/whats-new) を参照してください。

### <a name="announcing-the-dynamics-365-october-18-release-notes"></a>Dynamics 365 2018 年 10 月リリース ノートの発表

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2018 年 10 月リリース ノートを確認](https://go.microsoft.com/fwlink/?linkid=870424). あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

## <a name="bug-fixes"></a>バグ修正

Finance and Operations 8.1.1 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://go.microsoft.com/fwlink/?linkid=2038101)を参照してください。

## <a name="platform-update-21"></a>プラットフォーム update 21

Microsoft Dynamics 365 for Finance and Operations バージョン8.1.1には、プラットフォーム更新プログラム 21 が含まれています。 プラットフォーム更新プロフラム 21 については、[Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 21 (2018 年 10 月) の新機能と変更](whats-new-platform-update-21.md) をご覧ください。

## <a name="ledger-settlements"></a>元帳決済

元帳決済では、一般会計の借方および貸方トランザクションを照合し、決済済としてマークすることができます。 この方法で、関連するトランザクションがクリアされていることを確認することができます。 誤って行われた決済を取り消すこともできます。 詳細については、[元帳決済](../../financials/general-ledger/ledger-settlements.md)を参照してください。

## <a name="prevent-generating-offset-tax-transactions-during-tax-settlement"></a>税決済時の相殺税トランザクションの生成を防止

税決済プロセス中、システムは相殺税トランザクションを生成しますが、一定期間内に大量の税トランザクションを処理する必要がある場合、パフォーマンスの問題を引き起こす可能性があります。 これが発生しないように、**相殺税トランザクションを生成しないようにする** チェック ボックスが **売上税決済期間** ページに追加されました。 詳細については、「[消費税清算期間の設定](../../financials/general-ledger/tasks/set-up-sales-tax-settlement-periods.md)」を参照してください。

## <a name="extensibility-enhancements"></a>拡張性の強化

Finance and Operations の今回のリリースでは、列挙、メタデータ、メソッドの強化など、拡張性をサポートするために、さまざまな拡張機能の強化が加えられています。 詳細については、[Dynamics 365 for Finance and Operations バージョン 8.1.1 で変更された拡張機能](../../dev-itpro/extensibility/extensibility-changes-811.md) を参照してください。

## <a name="vat-declaration-for-russia"></a>ロシアの VAT申告

今回のリリースでは、電子的な形式でロシアの VAT 申告を生成する ER コンフィギュレーションを確認できます。 詳細については、[電子形式の RUS/ロシア VAT 申告](https://support.microsoft.com/help/4477332/rusrussiavatdeclarationinelectronicformat)を参照してください。
