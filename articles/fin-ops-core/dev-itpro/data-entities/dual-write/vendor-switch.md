---
title: 仕入先デザインの切り替え
description: このトピックでは、Finance and Operations アプリと Common Data Service との間の仕入先データの統合を切り替える方法について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: ffd7a4c01810578b4abb6942aeff76e5147fafa9
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173042"
---
# <a name="switch-between-vendor-designs"></a>仕入先デザインの切り替え

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a>仕入先データ フロー 

**取引先企業** エンティティを使用して **組織** タイプの仕入先を保存し、**連絡先** エンティティを使用して **個人** タイプの仕入先を保存する場合は、次のワークフローをコンフィギュレーションします。 それ以外の場合、このコンフィギュレーションは必須ではありません。

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>組織タイプの仕入先に対して拡張された仕入先設計を使用します

**Dynamics365FinanceExtended** ソリューション パッケージには、次のワークフロー プロセス テンプレートが含まれています。 各テンプレートのワークフローを作成します。

+ アカウント エンティティでの仕入先の作成
+ 仕入先エンティティでの仕入先の作成
+ アカウント エンティティでの仕入先の更新
+ 仕入先エンティティでの仕入先の更新

ワークフロー プロセス テンプレートを使用して新しいワークフロー プロセスを作成するには、次のステップに従います。

1. **仕入先** エンティティのワークフロー プロセスを作成して、**アカウント エンティティで仕入先を作成** ワークフロー テンプレートを選択します。 その後、**OK** を選択します。 このワークフローでは、**アカウント** エンティティの仕入先作成シナリオを処理します。

    ![アカウント エンティティ ワークフロー プロセスでの仕入先の作成](media/create_process.png)

2. **仕入先** エンティティのワークフロー プロセスを作成して、**アカウント エンティティで仕入先を更新** ワークフロー テンプレートを選択します。 その後、**OK** を選択します。 このワークフローでは、**アカウント** エンティティの仕入先更新シナリオを処理します。
3. **アカウント** エンティティのワークフロー プロセスを作成して、**仕入先エンティティで仕入先を作成** ワークフロー テンプレートを選択します。
4. **アカウント** エンティティのワークフロー プロセスを作成して、**仕入先エンティティで仕入先を更新** ワークフロー テンプレートを選択します。
5. ワークフローは、必要に応じてリアルタイムまたはバックグラウンドのワークフローとしてコンフィギュレーションできます。 ワークフローをバックグラウンド ワークフローとしてコンフィギュレーションするには、**バックグラウンド ワークフローに変換** を選択します。

    ![バックグラウンド ワークフロー ボタンへの変換](media/background_workflow.png)

6. **アカウント** エンティティと **仕入先** エンティティで作成したワークフローを有効にして、その **組織** タイプの仕入先情報を保存するために **アカウント**  エンティティの使用を開始します。

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>個人タイプの仕入先に対して拡張された仕入先設計を使用します

**Dynamics365FinanceExtended** ソリューション パッケージには、次のワークフロー プロセス テンプレートが含まれています。 各テンプレートのワークフローを作成します。

+ 仕入先エンティティでの個人タイプの仕入先の作成
+ 連絡先エンティティでタイプが個人の仕入先を作成する
+ 連絡先エンティティでタイプが個人の仕入先を更新する
+ 仕入先エンティティでタイプが個人の仕入先を作成する

ワークフロー プロセス テンプレートを使用して新しいワークフロー プロセスを作成するには、次のステップに従います。

1. **仕入先** エンティティのワークフロー プロセスを作成して、**連絡先エンティティでタイプが個人の仕入先を作成する** ワークフロー テンプレートを選択します。 その後、**OK** を選択します。 このワークフローでは、**連絡先** エンティティの仕入先作成シナリオを処理します。
2. **仕入先** エンティティのワークフロー プロセスを作成して、**連絡先エンティティでタイプが個人の仕入先を更新する** ワークフロー テンプレートを選択します。 その後、**OK** を選択します。 このワークフローでは、**連絡先** エンティティの仕入先更新シナリオを処理します。
3. **連絡先** エンティティのワークフロー プロセスを作成して、**仕入先エンティティでタイプが個人の仕入先を作成する** ワークフロー テンプレートを選択します。
4. **連絡先** エンティティのワークフロー プロセスを作成して、**仕入先エンティティでタイプが個人の仕入先を更新する** ワークフロー テンプレートを選択します。
5. ワークフローは、必要に応じてリアルタイムまたはバックグラウンドのワークフローとしてコンフィギュレーションできます。 ワークフローをバックグラウンド ワークフローとしてコンフィギュレーションするには、**バックグラウンド ワークフローに変換** を選択します。
6. **連絡先** エンティティと **仕入先** エンティティで作成したワークフローを有効にして、その **個人** タイプの仕入先情報を保存するために **連絡先** エンティティの使用を開始します。