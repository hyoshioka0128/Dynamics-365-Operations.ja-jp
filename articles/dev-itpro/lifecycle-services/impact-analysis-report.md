---
title: Lifecycle Services (LCS) の影響分析レポート
description: このトピックでは、 Microsoft Dynamics Lifecycle Services (LCS) の影響分析レポートについて説明します。
author: dfroslieMSFT
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: dfroslie
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: fc665aed80d908b641857ab94af5103ecb7f0c5e
ms.sourcegitcommit: f5c2cfac0411c880994376ead6691ab52f2fd12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "1720230"
---
# <a name="impact-analysis-report-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) の影響分析レポート

[!include [banner](../includes/banner.md)]
[!include [private preview banner](../includes/private-preview-banner.md)]

**影響分析** レポートは、新しいリリースのテスト作業を重点的に行う際に役立ちます。 リリースにて変更されたMicrosoftコードの詳細と、Lifecycle Services (LCS) 内 Microsoft Dynamics のプロジェクトに関連付けられている運用環境の使用状況に関する情報を提供します。 このコンテンツでは、機能の概要と、いくつかの重要な注意事項について説明します。 ただし、このレポートには包括的な情報は含まれていません。 したがって、リリースのテストを予定している場合は、他のツールと組み合わせて使用する必要があります。

## <a name="code-churn"></a>コード チャーン

レポートにおける1つの重要なポイントは、最新のリリースで選択したモデルに対してMicrosoftが行ったコード変更 (またはチャーン) の量です。 コードの変更とは、コードの行数が変更、追加、削除された数を意味します。 レポートには、リリースに寄与した各ファイルにて行われたコード変更の記録が含まれています。

Microsoftエンジニアリングシステムの一部である標準命名規則を使用して、コードの変更を特定のモジュールのレベルに集約することができます。 このようにして、複数のリリースについて、製品のさまざまな部分に対する変更の相対的な量を決定することができます。

リリースおよびモジュールによるコード変更のフィルタ処理に加えて、エンジニアリング サイクルのフェーズによってコード変更をフィルタすることができます。 エンジニアリングの分岐では、リリースがプレビューとして使用可能になる前に変更が行われます。 この分岐には変更の大部分が含まれています。 安定化の分岐には、リリースのプレビューと一般公開の間で行われた変更が含まれています。 安定化の段階にて行われた変更をフィルタリングする機能は、リリースがプレビューとして使用可能になったときにリリースレビューとテストを行う場合に役立ちます。

## <a name="usage"></a>用途

レポートにおける2番目に重要なポイントは、有効なLCSプロジェクトに関連付けられた実稼働環境での製品のフォーム に基づいた使い方です。 この使用方法は、各フォームのユーザー操作をまとめることによって分析を行います。 ユーザーとの対話的操作とは、webクライアントとサービスの間でやりとりが発生したときに記録されるイベントです。 ユーザーとの間で最も頻繁に行われるやり取りは、マウスまたはキーボードでの入力処理です。 ただし、システムが生成した処理も同様にカウントされてしまいます。

コードチャーンと同じ名前付け規則を使用することにより、モジュールレベルで使用情報をまとめることが可能となります。 **カスタム** モジュールは、Microsoftが提供したものではないフォームを表します。

利用状況に関する情報は、リリースフィルタとは連係していません。 その代わりに、これは時間ベースで管理されており、2つ階層からなる詳細情報を保持しています。 モジュールベースのビジュアリゼーションの場合、使用されるデータはアクティブなLCSプロジェクトに関連付けられている実稼動環境での過去95日間に使用されたデータです。 フォームベースのビジュアリゼーションの場合、使用されるデータはアクティブなLCSプロジェクトに関連付けられている実稼動環境での過去35日間に使用されたデータです。 このタイムフレームが選ばれた理由としては、データのボリュームと十分な履歴との間に妥協点があり、月ごとまたは四半期ごとにしか行われない業務活動を保証することに役立つためです。

## <a name="important-considerations"></a>重要な考慮事項

レポートを使用する場合は、次のような重要な注意事項があります。

- このツールでは、変更されたコード(追加、更新、削除)の行数を、リリースに対する変更がおよぼす影響の概算値として使用します。 変更されたコード行数とそれがおよぼす影響との間には妥当な相関関係がありますが、コードの1行の変更によっても影響が生じる可能性があることに注意してください。
- Microsoft モデルによってはコード変更の分析に含まれていない場合があります。 プラットフォームの変更は対象となりません。 さらに、台帳、CaseManagement、ApplicationCommonなど、他の下位レベルのモデルの変更は対象となりません。 対象となるモデルは、レポートのコード変更の詳細に記載されています。
- このレポートをリリースのドキュメントとともに使用して、変更された機能を把握することができます。
- レポートには、関連する機能が有効となっているかどうかにかかわらず、コードに対するすべての変更が表示されます。 機能制御機能によって機能が無効になっている場合は、コードの変更がおよぼす影響は限定されます。
- 本番環境の使用は、ユーザーとWebクライアントとのやりとりに基づいて決定されます。 バッチ処理や統合シナリオなど、システムをその他の用途で使用した場合は除外されます。
- 独立系ソフトウェアベンダー(ISV)のソリューションが行ったコード変更、特定の実装を目的とした拡張のコード変更は除外されます。

要約すると、レポートはコードの変更と使用状況の概算値を表示します。 その他のアクテビティやツールと組み合わせることで、リリースに対するリスク評価を行う場合に役立てることができます。
