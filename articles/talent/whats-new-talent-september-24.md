---
title: "Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 9 月 24 日)"
description: "このトピックでは、Microsoft Dynamics 365 for Talent Core HR の新機能または変更された機能について説明します。"
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 94950fbe5c1aad3dfbd3de59d1bcb47337ff68ea
ms.openlocfilehash: aeb75fe4c775b9003c6429de536498f495224098
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-24-2018"></a>Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 9 月 24 日)

[!include [banner](includes/banner.md)]

**ビルド 8.1.1015.0**

このトピックでは、Core HR の新機能または変更された機能について説明します。

## <a name="currency-added-to-benefits"></a>給付金に追加された通貨

給付金の通貨を含めるため、福利厚生計画が更新されました。 この新しいフィールドも作業者が登録されている給付金に使用できます。 この新しいフィールドは、給付金の管理および給付金のセキュリティ権限の一覧表示の一部です。

## <a name="update-proration-process--leave-and-absence"></a>比例配分処理の更新 – 休暇と欠勤

組織は、従業員の入社日および退社日に基づいて、休暇を別々に付与します。 組織を退職する従業員については、退職日に報奨を終了する必要がある場合もあれば、見越計上処理を停止する勤務最終日に依存する場合もあります。 これらの変更は、退職処理中のどの時期に登録を終了するかを選択する機能を組織に提供します。 これらの新しいオプションは、作業者の退職およびマネージャー セルフ サービスの作業者の退職の特権の一部です。 

## <a name="other-changes"></a>その他の変更

このリリースには、いくつかの追加のバグ修正が含まれています。

## <a name="known-issue"></a>既知の問題

-   **問題:** 作業者に新しい添付ファイルを追加する場合、**新規**および**編集**ボタンは灰色表示です。**回避策:** 添付ファイル ページを開く前に、**作業者**ページの情報ボックスが閉じていることを確認します。 **作業者**ページが読み込まれるとき情報ボックスが閉じている場合、添付ファイルボタンが有効になります。 (この問題は次のプラットフォーム更新プログラムで修正されます。)
