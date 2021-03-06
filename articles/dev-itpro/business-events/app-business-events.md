---
title: アプリケーション ビジネス イベント
description: このトピックでは、アプリケーション ビジネス イベントを一覧します。
author: Sunil-Garg
manager: AnnBe
ms.date: 01/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: Platform update 24
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: 5bfa0d8313c06211aa999b5904c4e50bc6575e23
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1505430"
---
# <a name="application-business-events"></a>アプリケーション ビジネス イベント

[!include[banner](../includes/banner.md)]

このトピックでは、アプリケーション ビジネス イベントを一覧します。

<a name="procure-to-pay"></a>仕入れから支払
--------------

| ビジネス イベント                  | 説明                                                                                                                                | モジュール           |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| 仕入先請求書が一致しました          | これは、仕入れから支払プロセスの一部として仕入先請求書のために請求書照合検証が完了するときに発生します。 | 買掛金管理 |
| 仕入先請求書が転記されました           | 調達から支払いまでのプロセスの一環として、ユーザーが仕入先請求書を転記する場合、このビジネス イベントがトリガーされます。 | 買掛金管理 |
| 仕入先支払が転記されました           | これはユーザーが仕入れから支払プロセスの一部として仕入先支払を転記するときに発生します。                                 | 買掛金管理 |
| 仕入帳仕訳帳が転記されました | これはユーザーが仕入れから支払プロセスの一部として仕入帳仕訳を転記するときに発生します。                      | 買掛金管理 |
| 請求仕訳帳が転記されました          | これはユーザーが仕入れから支払プロセスの一部として請求仕訳帳を転記するときに発生します。                               | 買掛金管理 |
| 請求書承認仕訳帳が転帰されました | これはユーザーが仕入れから支払プロセスの一部として請求書承認仕訳帳を転記するときに発生します。                      | 買掛金管理 | 
|発注書が確認されました |これは発注書が仕入先によって確認されたときに発生します。 次のいずれかのアクションがイベントを発生させます: ユーザーが発注書のユーザー インターフェイスで手動で発注書を確認する、発注書の確認がバッチで実行されるとき、または確認が会社間シナリオでプログラムで実行されるとき。 仕入先コラボレーションが使用されるシナリオ、および仕入先コラボレーションのポリシーが発注書の自動確認にセットされるシナリオでは、 **仕入先コラボレーション** ポータルの **発注書の確認** ページで **承認** ボタンがクリックされるときにトリガーが発生します。|調達|
|発注書が受領されました |これは、商品やサービスが 1 つまたは複数の発注書に対して入庫済として登録されるときに発生します。 次のいずれかのアクションがイベントを発生させます: 製品受領書が 1 または複数の発注書に対して発注書および製品受領書のユーザー インターフェイスで手動で生成される、製品受領書がバッチで生成されるとき、または製品受領書が会社間シナリオでプログラムで生成されるとき。|調達||

<a name="quote-to-cash"></a>現金に対する見積
-------------

| ビジネス イベント                             | 説明                                                                                                                       | モジュール                 |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|------------------------|
| 販売注文から請求書が作成されます      | これはユーザーが見積から入金プロセスの一部として販売注文請求書を転記するときに発生します。                    | 売掛金管理    |
| 自由書式の請求書が転記されました                   | これはユーザーが見積から入金プロセスの一部として自由書式の請求書を転記するときに発生します。                      | 売掛金管理    |
| 支払が転記されました                             | これはユーザーが見積から入金プロセスの一部として支払を転記するときに発生します。                                | 売掛金管理    |
| トランザクションが損金処理されました                 | これはユーザーが見積から入金プロセスの一部として顧客取引を記述するときに発生します。              | 売掛金管理    |
| トランザクションの回収状態が変更されました | これはユーザーが見積から入金プロセスの一部として回収状態を更新するときに発生します。 | 売掛金管理    |
| 利子計算書が転記されました                       | これはユーザーが見積から入金プロセスの一部として利子計算書を転記するときに発生します。                         | 売掛金管理    |
| 督促状が作成されました                  | これはユーザーが見積から入金プロセスの一部として督促状を作成するときに発生します。     | 貸方転記および取立 |

