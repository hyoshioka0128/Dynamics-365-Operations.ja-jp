---
title: 繰延タイプ<T>
description: 繰延タイプ
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: ''
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4e8304ed0427db1862cfc04163b132f6e7f0b322
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851637"
---
# <a name="deferred-typelttgt"></a>延期されたタイプ&lt;T&gt;

[!include [banner](../../../../includes/banner.md)]

### <a name="hierarchy"></a>階層

繰延 <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [promise](defer-ideferred.md#promise)

### <a name="methods"></a>メソッド

* [否認](defer-ideferred.md#reject)
* [解決](defer-ideferred.md#resolve)

## <a name="properties"></a>プロパティ

### <a name="promise"></a>promise

promise: Promise &lt;T&gt;




## <a name="methods"></a>メソッド

### <a name="reject"></a>否認


reject(error?: any): void




#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| エラー?|any||

#### <a name="returns-void"></a>void を返します

### <a name="resolve"></a>解決


resolve (value?: T &#124; PromiseLike &lt;T&gt;) : void




#### <a name="parameters"></a>パラメーター

| 氏名 | 型 | 説明 |
| ---- | ---- | ----------- |
| value?|T &#124; PromiseLike &lt;T&gt;||

#### <a name="returns-void"></a>void を返します

