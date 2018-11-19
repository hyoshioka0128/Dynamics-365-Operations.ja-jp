---
title: "1 つのバージョンのサービス更新に関するよく寄せられる質問"
description: "このトピックは、一貫性があり、予測可能でシームレスな方法で最新の状態に保つために使用できるサービスの更新、プロセス、ツールを明確にすることを目的としています。"
author: meeramahabala
manager: AnnBe
ms.date: 10/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: 3fe8e665849ba06e6146ca37c609303e97f40697
ms.contentlocale: ja-jp
ms.lasthandoff: 11/01/2018

---

# <a name="one-version-service-updates-faq"></a>1 つのバージョンのサービス更新に関するよく寄せられる質問
[!include[banner](../includes/banner.md)]

2018 年 7 月、一貫性があり、予測可能でシームレスな方法で最新の状態に保つのに役立つ [Dynamics 365 の更新の提供方法の変更](https://cloudblogs.microsoft.com/dynamics365/2018/07/06/modernizing-the-way-we-update-dynamics-365/)を発表しました。 このよく寄せられる質問は、準備のために使用できる Finance and Operations サービスの更新プログラム、プロセス、ツールを明確にすることを目的としています。 必要に応じて、このトピックに追加情報を追加し続けします。

## <a name="service-updates"></a>サービスの更新

### <a name="what-product-versions-are-impacted-by-service-updates"></a>どの製品バージョンがサービスの更新プログラムの影響を受けますか?
| バージョン | 説明 |
|---------|-------|
| 8.1 以降 | 8.1 以降のすべてのユーザーは、2018 年 11 月以降アプリケーションとプラットフォーム更新が結合された毎月の更新プログラムがスケジュールされています。  3 か月以内に更新する必要があります。                   |
| 8.0           | 8.0 のユーザーは、毎月のプラットフォームおよび財務報告の更新を受け取ります。 3 か月以内に更新する必要があります。 2019 年 4 月で 8.0 ライフサイクルが終了します。 8.0 のユーザーは、2018 年 12 月 1 日までに 8.1 に更新することをお勧めします。 このプロセスは、通常のパッケージの更新に似ています。 詳細なドキュメントについては、[バージョン 8.0 から 8.1 への環境の更新](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/appupdate-80-81)トピックを参照してください。  | 
| 7.x           | 7.x のユーザーは、毎月のプラットフォームおよび財務報告の更新を受け取ります。 3 か月以内に更新する必要があります。  2019 年 4 月より前に 8.1 にアップグレードする必要があります (拡張機能が入手可能でない限り、市場で唯一のオーバーレイ バージョンはバージョン 7.3 になります)。 2019 年 4 月から、サービスはバージョン 10.0 に更新されます。 |

### <a name="what-does-the-update-contain"></a>更新プログラムには何が含まれていますか?
8.1 以降では、サービスの更新には、規制の更新を含むサービスの重要な改良であるアプリケーション (財務、レポート、小売を含む) とプラットフォームの変更が含められます。 新しいエクスペリエンスはオプトインになります。 サービス更新プログラムには、下位互換性があります。 この更新プログラムを代表する 1 つのバージョンがあります。

### <a name="what-is-a-regulatory-update"></a>規制の更新とは何ですか?
規制の更新は、法律 (通常は特定の国/地域) によって義務付けられている新機能または既存の機能の変更です。 規制の更新は、特定の法律実施日 (LED) に常に要求され、この日付以前に有効にする必要があります。

### <a name="whats-the-upcoming-schedule-of-updates"></a>更新の将来のスケジュールとは何ですか?
サービスの更新は、2018 年 11 月から毎月提供されます。 Microsoft は、選択された保守時間帯に基づいて更新プログラムを毎月適用します。 3 か月以内に更新する必要があります。

### <a name="are-there-any-major-updates-post-81"></a>8.1 以降のメジャー アップデートはありますか?
4 月と 10 月に、新しいエクスペリエンスを有効にする 2 つのメジャー アップデートがあります。 メジャー アップデートは、コードやデータのアップグレードは必要ありません。 重大な変更は、お客様が計画できるように、12 か月前にお知らせします。 このような変更は、メジャー アップグレード時にのみ導入されます。 2019 年 4 月に利用可能になる 10.0 リリースも、アップグレードではなく更新プログラムになります。

### <a name="what-does-it-mean-when-an-update-is-backward-compatible"></a>更新プログラムに下位互換性がある場合、これは何を意味しますか?
下位互換性では、バイナリと機能の互換性がカバーされます。 バイナリ互換性は、カスタマイズを再コンパイル、再設定、または再展開しなくても、あらゆるランタイム環境に更新プログラムを適用できることを意味します。 つまり、デザイン時の開発環境で、X++ パブリックおよび保護された API とメタデータが変更または削除されません。 Microsoft が古い形式の API を削除することによって互換性をなくす必要がある場合、廃止スケジュールが 12 か月前に発表されます。 デザイン時の互換性には、非 X++/メタデータ API は含まれていません。 機能互換性は、ユーザー エクスペリエンスについてです。 新しいエクスペリエンスはすべてオプトインになります。

### <a name="do-these-updates-apply-to-on-premises"></a>これらの更新プログラムはオンプレミスで適用されますか?
使用しているバージョンの具体的な有効期限については、[ソフトウェアのライフサイクル ポリシーおよびオンプレミス リリース](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/on-prem-version-update-policy?toc=/fin-and-ops/toc.json)を参照してください。 このトピックで説明されている更新のプロセスは、クラウド サービスにのみ適用されます。 

## <a name="process"></a>プロセス

### <a name="can-i-select-the-day-and-time-to-update"></a>更新する日時は選択できますか?
ユーザーは、Lifecycle Services (LCS) に日と保守の時間枠を構成できます。 更新方法に含まれる手順をが記載された LCS 通知を受信するように選択したユーザーには、メールが送信されます。 ユーザーは、更新プログラムの指定された階層 2/UAT サンドボックスを選択できるようになります。 ユーザーは、テストと検証に 5 営業日かけることができます。 ユーザーは、Lifecycle Services を通じてより早い時期に (または早期アクセス プログラムを通じてさらに早く) すべての環境に更新プログラムを適用することをオプションで選択できます。 ユーザーには、更新を追加サンドボックスまたは開発者/ビルド (階層 1) 環境に展開する責任があります。

### <a name="how-do-i-update-to-the-latest-version"></a>最新バージョンに更新する方法を教えてください。
ユーザーは、LCS の環境の詳細ページでタイルを使用して最新バージョンに更新できます。 Microsoft により更新プログラムがリリースされたら、タイルに最新の更新プログラムが表示されます。 ユーザーは、サンドボックスと製造環境で更新エクスペリエンスを経由して独自に更新プログラムを適用することができます。 ドキュメントは docs.microsoft.com でも入手可能になります。

### <a name="what-is-the-expected-downtime"></a>予想されるダウンタイムはどのくらいですか ?
更新が正常に完了するために予想されるダウンタイムは 1 時間 30 分です。 ただし、 更新プログラムの適用時に問題が発生する場合、3 時間のダウンタイムを要求します。 マイクロソフトは、必要とするダウンタイムを減らすために積極的に取り組んでいます。改善は数か月以内に反映されます。

### <a name="whats-the-process-for-deprecation"></a>廃止のプロセスを教えてください。
廃止は、廃止の 12 か月前に通知により発表されます。 機能は、メジャー アップグレード時にのみ非推奨になります。

### <a name="can-i-delay-an-update"></a>更新プログラムを延期することはできますか?
LCS コンフィギュレーションを介して最大 3 か月更新を延期できます。 この期間後は、更新プログラムがスケジュールされ、月単位の更新が再開されます。 遅延更新用の更新エクスペリエンスにより、さらなるダウンタイムが発生します。

### <a name="what-if-i-find-an-issue-during-the-sandbox-update"></a>サンドボックスの更新中に問題が発生した場合はどうなりますか?
サンドボックス環境で検証を行うときに問題が見つかった場合は、有効なサポート チケット番号と業務の妥当性を提供することで直接 LCS を通じて更新をスキップするように要求できます。 要求は、Microsoft により校閲され、承認された場合、その月の更新から除外されます。

### <a name="how-much-time-do-i-get-for-validation"></a>検証にかけることができる時間はどのぐらいですか?
更新がサンドボックス環境に適用されてから、5 日間検証できます。 より多くの時間を必要とする場合は、いずれかのサンドボックス環境に早期アクセス自動更新を登録することができます。 これで、生産ロールアウトよりも前に更新をテストする追加の時間が提供されます。このプログラムの詳細については、まもなく公開されます。

### <a name="will-rollback-be-supported-after-an-update-is-applied"></a>更新プログラムが適用された後、ロールバックはサポートされますか?
数か月後にロールバックがサポートされます。

### <a name="how-will-my-isvs-stay-current"></a>私の ISV は常に最新ですか?
お客様の環境のサービスの更新には下位互換性があるため、独立系ソフトウェア ベンダー (ISV) によるアクションは必要ありません。 ISV は、そのコードが依存する最低限必要なプラットフォーム リリースを開発します。 重大な変更については、ISVが追加して検証するための 12 か月のリード タイムがあります。 ISV は、プラットフォーム ビットへの早期アクセスを獲得して、一般的に使用できるようになる前に更新プログラムに対するソリューションを検証できるようにするために、[パートナー早期アクセス プログラム](https://experience.dynamics.com/insider/)の一部とすることをお勧めします。

### <a name="what-about-new-features"></a>新機能はどうなりますか?
すべての新機能は 12 か月間オプトインとなり、機能の有効化を選択するまで変更管理は必要ありません。

### <a name="are-batch-jobs-suspended-during-a-service-update"></a>バッチ ジョブは、サービスの更新中に中断されますか?
バッチ ジョブはメンテナンス ウィンドウ中に中断され、メンテナンスの完了時に再開します。

## <a name="tools"></a>ツール

### <a name="how-can-i-get-early-access-to-non-released-platform-updates"></a>非リリースのプラットフォーム更新プログラムへの早期アクセスをどのように取得できますか。
[初回リリース プログラム](https://experience.dynamics.com/insider/)に参加できます。Microsoft は、常に最新の更新プログラムによってシステムを最新の状態に保ちます。

### <a name="is-there-tooling-available-to-support-testing-the-latest-release"></a>最新のリリースのテストをサポートするために使用可能なツールはありますか?
Finance and Operations 用の [Regression Suite Automation Tool](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests) は、[現在入手可能](https://www.microsoft.com/en-us/download/details.aspx?id=57357)です。 このツールは、ユーザー受け入れテストの費用と時間を大幅に減少します。 通常、ユーザー受け入れテストは Microsoft アプリケーションの更新プログラムを取得するか、カスタム コードとコンフィギュレーションを Dynamics 365 for Finance and Operations 実稼働環境に適用する前に必要です。 機能パワー ユーザーが Finance and Operations タスク レコーダーを使用してビジネス タスクを記録し、ソース コードを作成しなくても自動テストのスイートに変換できるようにします。 テスト ライブラリは、ビジネス プロセス モデラー (BPM) ライブラリを使用して Lifecycle Services に保存および配分され、テストの実行、報告、調査のために Azure DevOps と完全に統合されます。 テスト データ パラメーターは、テスト ステップから切り離され、Excel データ ファイルに保存されます。

### <a name="how-can-i-test-and-validate-that-the-integrations-continue-to-work"></a>統合が機能し続けていることはどのようにテストおよび検証できますか?
データ タスクの自動化により、さまざまな種類のデータ タスクを簡単に繰り返し、各タスクの結果を検証することができます。 また、タスクの結果の検証を使用して、データ エンティティの自動テストを使用することもできます。 詳細については、[データ タスクの自動化](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-task-automation)トピックの差し込みデータの概要を参照してください。

### <a name="how-can-i-determine-whats-changed-in-a-service-update"></a>サービス更新プログラムの変更内容はどのようにわかりますか?
[リリース ノート](https://docs.microsoft.com/en-us/business-applications-release-notes/)は、リリースのすべての新機能と変更の情報の主要ソースです。 必要に応じて、機能には docs.microsoft.com のヘルプ トピックも含められます。 影響分析ツールは、使用する機能への影響を理解するために LCS で利用可能になります。

## <a name="preparing-for-one-version"></a>1 つのバージョンの準備

### <a name="how-can-i-log-an-extensibility-request"></a>拡張機能の要求を記録するにはどうすればよいですか?
拡張機能の要求は、LCS に記録することができます。 詳細は、[機能拡張要求](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/extensibility/extensibility-requests)トピックにあります。 使用可能な拡張機能をログに記録して使用するには、以下のタイムライムに注目してください。

| 日 | 拡張性の要求 |
|----------|---------------------------------------------------------------------------------------------------------|
| 2019 月 1 日 | 拡張機能のすべての要求は、2019 年 1 月 1 日までにログインする必要があります。 ISV とユーザーは、この時点までにコードを分析し、これらの要求を行うことが要求されます。 要求が 2019 年 1 月 1 日までに提出されない場合、2020 年 4 月より後に 7.3 を維持するための例外は提供されません。 |
| 2019 年 12 月 | 2019 年 1 月 1 日によって記録された要求については、拡張機能は 2019 年 12 月 31 日以前に入手可能になります。 これらの拡張機能を使用しているユーザーは、2020 年 4 月までに現在のバージョンに移行する必要があります。    |

### <a name="what-does-end-of-service-mean"></a>サービスの終了にはどのような意味がありますか?
問題を処理するには、その時点で最新の更新プログラムを実行する必要があります。 個々の修正プログラムは提供しません。 Microsoft は、以前の更新プログラムのパフォーマンスの問題のトラブルシューティングを行うことはできません。

8.1 以降は、リリース日から 3 か月以内にサポートされている最新バージョンを使用する必要があります (8.1.1 など)。 詳細については、[ライフサイクル ポリシー](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/versions-update-policy) を参照してください。

### <a name="will-individual-hotfixes-be-supported"></a>個別の修正プログラムをサポートしますか?
8.1 以降、個別の修正プログラムはサポートされません。 ユーザーは、最新の累積的な更新プログラムに更新して修正プログラム (8.1.1 など) を適用する必要があります。 さらに、重要な修正プログラムは累積的であり、LCS サービス エクスペリエンスを通じて使用可能になります。

### <a name="how-can-i-upgrade-to-8x"></a>8.x にアップグレードする方法を教えてください。
最新のアプリケーションにアップグレードする方法については、[Finance and Operations の最新の更新プログラムに移行するためのプロセス](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/upgrade-latest-update#scenario-3-upgrade-to-the-latest-application-release-1)を参照してください。 [8.0 から 8.1 への](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/appupdate-80-81)更新では、データのアップグレードは不要です。ダウンタイムが大幅に削減されるセルフ サービスの更新になります。

## <a name="retail-service-updates"></a>小売サービスの更新プログラム

### <a name="what-components-of-my-solution-will-be-impacted-by-one-version-service-updates"></a>1 つのバージョンのサービス更新プログラムの影響を受けるソリューションのコンポーネントはどれですか?

Retail サーバーおよびクラウド POS などのすべてのクラウド コンポーネントは、Dynamics 365 バックオフィスと同じ進捗で更新されます。

### <a name="what-options-are-available-to-minimize-impact-to-my-retail-cloud-components"></a>Retail クラウド コンポーネントへの影響を最小限に抑えるためにどのオプションを使用できますか?

Retail クラウド コンポーネントには、Dynamics 365 バックオフィスと同じダウンタイムが必要です。 今後のリリースでは、展開への更新を減らしてさらにスケジュールするために Retail クラウド スケール単位 (RCSU) が使用可能になります。 RCSU の詳細については、[ドキュメント](https://docs.microsoft.com/en-us/business-applications-release-notes/October18/dynamics365-retail/planned-features)および[リリース ノート](https://docs.microsoft.com/en-us/business-applications-release-notes/#pivot=products&panel=products1) サイトにある発行済みのリリース情報を参照してください。

### <a name="will-there-be-options-to-take-individual-hotfixes-for-my-retail-solution-components"></a>Retail ソリューション コンポーネントの個別の修正プログラムを取得するオプションはありますか?

Retail コンポーネントのすべての修正プログラムは累積的です。

### <a name="what-are-the-maintenance-downtime-requirements-that-may-impact-channel-operations"></a>チャンネル工程に影響を与える可能性のある保守ダウンタイム要件は何ですか?

冗長性の業務ニーズがある小売業者のため、Modern POS オフライン機能では、インターネットから切断中またはクラウド環境の更新中にコア Retail POS 処理を使用できます。 Retail Store Scale Unit を運用している店舗では、サポート クラウド メンテナンス期間中もコア POS 処理のサポートを伴う処理を継続します。 詳細については、[オンラインおよびオフライン販売時点管理 (POS) 処理](../../retail/pos-operations.md)を参照してください。

### <a name="when-will-i-need-to-update-my-in-store-components"></a>店舗内コンポーネントを更新する必要があるのはいつですか?

店舗内のすべてのコンポーネントは、サポートを維持するために、1 年以内にリリースされたソフトウェアを実行している必要があります。 ユーザーには、自己ホスト コンポーネントを更新し (店舗かプライベートで管理するデータ センターにインストールされているコンポーネントなど)、これらのコンポーネントのインストールされているバージョンが積極的にサポートされていることを確認する責任があります。

### <a name="will-there-continue-to-be-backward-compatibility-for-the-in-store-retail-components"></a>店舗内小売コンポーネントの下位互換性は続行されますか?

クラウドにホストされているコンポーネントの更新では、そのバージョンのリリース日から 12 か月間、小売業者によって自己ホストされるコンポーネント バージョンとの下位互換性が保持され続けます (店舗またはプライベート データ センターにインストールされているコンポーネントなど - Modern Point of Sale、Retail Store Scale Unit、Hardware Station)。 自己ホストされているコンポーネントは、クラウドでホストされているコンポーネントと同時に更新する必要はなく、独立したリズムで更新できるため、店舗に更新を展開する時間があります。

### <a name="what-options-are-available-for-updating-in-store-components-across-my-organization"></a>組織全体で店舗内コンポーネントを更新するためにどのようなオプションを使用できますか?

ユーザーは、店舗ごとに手動で自己ホストされているコンポーネントを更新するか、Microsoft System Center Configuration Manager、Microsoft Intune などの一括更新ツールを使用するかを選択できます。

### <a name="what-options-do-i-have-to-slowly-enable-new-functionality-across-my-retail-channels"></a>Retail チャネル全体で新しい機能を徐々に有効にするどのようなオプションがありますか?

Microsoft では、店舗、デバイス、およびユーザー全体で機能拡張を徐々に展開して有効にするいくつかのメカニズムを提供しています。

  -  **画面レイアウト デザイナー**: POS のほとんどのビジュアル要素は、顧客組織の管理ユーザーによって構成され、集中管理されます。 つまり、対応する画面レイアウトに含まれるように明示的に設定されていない限り、新しい POS の操作は POS に自動的に表示されません。 画面レイアウトは、画面レイアウト デザイナーを使用して構成され、店舗または POS デバイスに固有の場合があります。 詳細については、[販売時点管理 (POS) の画面レイアウト](../../retail/pos-screen-layouts.md)を参照してください。

  - **機能プロファイル、POS のアクセス許可、Retail パラメーター**: POS の機能の重要な要素は通常、ユーザーがコンフィギュレーション可能です。 これは、機能プロファイル、POS のアクセス許可、小売パラメーター、または該当するシナリオにおけるデバイス、レジスター、店舗、またはユーザー レベルの機能の管理を可能にするその他のコントロールを通じて設定できます。

  - **Modern POS および Retail Store Scale Unit**: Modern POS および Retail Store Scale Unit は小売業者によって自己ホストされるため、いずれかのコンポーネントを含むトポロジによっては、個別 (および低速) のリズムかつクラウド専用トポロジより細かい方法での更新の展開が可能になります。


