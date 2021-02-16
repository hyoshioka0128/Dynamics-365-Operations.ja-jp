---
title: カスタム ヘルプ ツールキット - ConvertHtmlToJson ツール
description: このトピックでは、Finance and Operations アプリ用のカスタム ヘルプ ツールキットに含まれている ConvertHtmlToJson ツールについて説明し ます。
author: edupont04
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.service: dynamics-ax-platform
audience: IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Operations
ms.openlocfilehash: f65545c6650ba7cc4e5e4676836bb48ece5a05e0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685088"
---
# <a name="custom-help-toolkit-the-converthtmltojson-tool"></a>カスタム ヘルプ ツールキット: ConvertHtmlToJson ツール

[!include [banner](../includes/banner.md)]

[カスタム ヘルプ ツールキット](custom-help-toolkit.md) には、HTML ファイルを JavaScript Object Notation (JSON) ファイルに変換する **ConvertHtmlToJson** ツールが含まれています。 検索サービスは、JSON ファイルを使用してヘルプ コンテンツのインデックスを作成します。

## <a name="use-the-converthtmltojson-tool-to-generate-json-files"></a><a name="json"></a>ConvertHtmlToJson ツールを使用して JSON ファイルを生成する

**ConvertHtmlToJson** ツールは、HTML ファイルを JSON ファイルに変換します。 次に、JSON ファイルを Microsoft Azure検索サービスに追加すると、ヘルプ コンテンツへの状況依存リンクが生成されます。

JSON ファイルには、ターゲットのヘルプ ページが対象とするフォームと言語を識別するためにインデクサーが使用するメタデータが含まれています。

ConvertHtmlToJson.exe を実行するための構文は次のとおりです。

```
ConvertHtmlToJson.exe --h <path> -j <path> --v <true|false>
```

パラメータの説明を以下に示します。

| パラメーター | 説明 |
|-----------|-------------|
| h | 処理する HTML ファイルのパスを指定します。 |
| j | JSON ファイルを保存するフォルダを指定します。 指定したフォルダは既に存在している必要があります。 |
| v | このパラメーターを **true** に設定し、詳細ログを有効にします。 それ以外の場合、**false** に設定します。 |

## <a name="example"></a>例

次の例では、詳細ログなしで JSON ファイルを生成します。

```
ConvertHtmlToJson.exe --h D:\D365-Operations\d365F-O\supply-chain\de -j D:\D365-Operations\json\supply-chain\de
```

## <a name="see-also"></a>参照

[カスタム ヘルプの概要](custom-help-overview.md)  
[Azure にカスタム ヘルプを展開](walkthrough-help-azure.md)  
[製品およびヘルプの言語およびロケール記述子](language-locale.md)  
[Dynamics AX カスタム ヘルプを Dynamics 365 で使用するために変換](migrate-dynamicsax2012.md)