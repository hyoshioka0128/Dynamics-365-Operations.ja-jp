---
title: 日時データとタイム ゾーン
description: この記事では、Microsoft Dynamics 365 for Finance and Operations での日付、日時フィールド、タイム ゾーンに関する情報を提供します。
author: pvillads
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, SystemDate
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 13571
ms.assetid: 3ce95bf2-02d7-44b5-95bc-cae6ae27e78e
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da87cbc27d637fbdabc1fceb5777360198a67ff5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573130"
---
# <a name="datetime-data-and-time-zones"></a>日時データとタイム ゾーン

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 for Finance and Operations での日付、日時フィールド、タイム ゾーンに関する情報を提供します。

## <a name="date-and-time-fields"></a>実行日時フィールド

Microsoft Dynamics 365 for Finance and Operations には 3 種類の日付と時刻のフィールドがあり、データベースの異なるデータ型に対応しています。

- **結合された日時フィールド** – これらのフィールドは Microsoft Dynamics 365 for Finance and Operationsで推奨される日付と時刻データの入力方法です。 **utcdatetime** データ型は、単一フィールドの日付と時刻のデータを協定世界時 (UTC) で格納します。 UTC は、世界時で時計と時間が規定される主要な標準時間です。 約 1 秒以内で、0 度の経度での太陽時を示し、夏時間には従いません。 世界中のタイム ゾーンは、UTC に正または負のオフセットを適用して表されます。 事実上、UTC がグリニッジ標準時 (GMT) と交換可能であると見なされます。 現在の UTC のバージョンは、国際電気通信連合の勧告 (ITU-R TF.460-6) によって定義されています。
- **日付フィールド** - これらのフィールドは、日付の入力にのみ使用されます。 **date** データ型は、年、月、日を格納します。 ただし、これらの値は UTC で格納されず、タイム ゾーンに関連付けることもできません。
- **時刻フィールド** – これらのフィールドは現在の日付の午前 0 時からの経過秒数を表示するために使用します。 **timeofDay** データ型は、整数値を格納します。 時刻の値は UTC で格納されません。

## <a name="time-zones"></a>タイム ゾーン

UTC 時刻を現地時間で 表すには、タイム ゾーンを指定する必要があります。 タイム ゾーンは、ローカル時刻に相当する UTC からの補正時間を制御します。 たとえば、モスクワの補正時間は UTC+3 になります。 優先タイム ゾーンは、コンピュータの Windows ロケールに従って最初に設定されますが、管理者によって変更されている場合もあります。 優先タイム ゾーンは、結合された日付と時刻を表示する場合にのみ使用されます。 ユーザーの優先タイム ゾーンを設定するには、**ユーザー** ページに移動します。 ページにシステムのユーザーのリストが表示されます。 優先タイム ゾーンを設定するユーザーを選択し、**ユーザー オプション** をクリックします。 **言語と地域**タブで、優先タイム ゾーンを選択します。
