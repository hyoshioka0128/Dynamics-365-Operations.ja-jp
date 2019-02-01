---
title: "Dynamics 365 for Operations プラットフォーム更新プログラム 4 (2017 年 2 月) の新機能および変更された機能"
description: "このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 4 における新機能または変更された機能について説明します。 このバージョンは 2017 年 2 月にリリースされ、ビルド番号は 7.0.4425.16161 です。"
author: sericks007
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 271823
ms.assetid: a98f6291-347c-4616-ad80-84d3eb648cba
ms.search.region: global
ms.author: sericks
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: be12cebe8fa536f2bd8a4ddddeb3a52dbf124714
ms.contentlocale: ja-jp
ms.lasthandoff: 12/18/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-operations-platform-update-4-february-2017"></a><span data-ttu-id="fdfb3-104">Dynamics 365 for Operations プラットフォーム更新プログラム 4 (2017 年 2 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="fdfb3-104">What's new or changed in Dynamics 365 for Operations platform update 4 (February 2017)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fdfb3-105">このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 4 における新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-105">This topic describes features that are either new or changed in Dynamics 365 for Operations platform update 4.</span></span> <span data-ttu-id="fdfb3-106">このバージョンは 2017 年 2 月にリリースされ、ビルド番号は 7.0.4425.16161 です。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-106">This version was released in February 2017 and has a build number of 7.0.4425.16161.</span></span>

## <a name="overview"></a><span data-ttu-id="fdfb3-107">概要</span><span class="sxs-lookup"><span data-stu-id="fdfb3-107">Overview</span></span>

<span data-ttu-id="fdfb3-108">Microsoft Dynamics クラウド プラットフォームの継続的な更新サイクルに移行したことをお知らせします。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-108">We are happy to announce that we have moved to a continuous update cycle for the Microsoft Dynamics cloud platform.</span></span> <span data-ttu-id="fdfb3-109">今月、いくつかのエキサイティングなアップデートが提供されています:</span><span class="sxs-lookup"><span data-stu-id="fdfb3-109">This month, some exciting updates are being delivered:</span></span>

- <span data-ttu-id="fdfb3-110">**毎月の更新プログラム**: 頻度を毎月へと移行し、新しいシステムや既存のシステムを最新の状態に保つのに役立つより簡単な更新プロセスを提供しています。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-110">**Monthly updates**: We are moving to a monthly cadence and providing a simpler update process to help keep new and existing systems up to date.</span></span>
- <span data-ttu-id="fdfb3-111">**埋め込み Power BI レポートは、すべてのユーザーに許可されている**: 埋め込み Microsoft Power BI レポートはすべてのユーザーに許可されています。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-111">**Embedded Power BI reports are licensed for all users**: Embedded Microsoft Power BI reports are licensed for all users.</span></span> <span data-ttu-id="fdfb3-112">追加機能は、Power BI Pro ライセンスを持つユーザーが使用できます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-112">Additional functionality is available for users who have Power BI Pro licenses.</span></span>
- <span data-ttu-id="fdfb3-113">**Power BI レポートが埋め込まれているワークスペースのビルドおよびリリース**: Power BI レポートが埋め込まれているワークスペースをビルドおよびリリースして、ユーザーにインタラクティブで視覚的に魅力的なエクスペリエンスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-113">**Build and release workspaces that have embedded Power BI reports**: You can build and release workspaces that have embedded Power BI reports, to provide interactive and visually engaging experiences for users.</span></span>
- <span data-ttu-id="fdfb3-114">**モビリティ**: モバイル フレームワークを更新して、iOS と Android デバイスをサポートする独自のオンラインとオフラインのエクスペリエンスを構築できます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-114">**Mobility**: We updated the mobile framework so that you can build unique online and offline experiences that now also support iOS and Android devices.</span></span>
- <span data-ttu-id="fdfb3-115">**視覚的スケジューリング**: ガント チャートの統合を更新し、新しい視覚アイコン、ローカライズされた形式、ユーザーの効率性の更新、および改善されたリソース管理機能を追加しました。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-115">**Visual scheduling**: We updated Gantt chart integration, added new visual icons, localized formats, updated user efficiencies, and improved resource management features.</span></span>
- <span data-ttu-id="fdfb3-116">**フィードバック**: Microsoft Dynamics 365 for Operations の改善のためにフィードバックをお寄せください。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-116">**Feedback**: You can provide your feedback to help us improve Microsoft Dynamics 365 for Operations.</span></span>

## <a name="monthly-updates"></a><span data-ttu-id="fdfb3-117">毎月の更新プログラム</span><span class="sxs-lookup"><span data-stu-id="fdfb3-117">Monthly updates</span></span>

<span data-ttu-id="fdfb3-118">ご承知の通り、クラウド プラットフォームは更新プログラム 3 の時点で [ロック](whats-new-platform-update-3.md) されています。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-118">As you know, the cloud platform is [locked](whats-new-platform-update-3.md) as of update 3.</span></span> <span data-ttu-id="fdfb3-119">ロックされているプラットフォームでは、拡張機能を使用して豊富なカスタマイズを実行できるだけでなく、コストのかかるコードのアップグレードなしで更新ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-119">A locked platform not only enables rich customizations that use extensions but also lets you to make updates without doing costly code upgrades.</span></span> <span data-ttu-id="fdfb3-120">update 4 以降、クラウド プラットフォームのが毎月の更新プログラムをリリースします。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-120">Starting with update 4, the cloud platform will release monthly updates.</span></span> <span data-ttu-id="fdfb3-121">したがって、ボタンをクリックするだけで、最新のイノベーションを使って新しい環境や既存の環境を最新の状態に保つことができます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-121">Therefore, you can keep new and existing environments up to date with the latest innovations at the click of a button.</span></span>

<span data-ttu-id="fdfb3-122">[http://lcs.dynamics.com](http://lcs.dynamics.com/) の既存の環境に最新の月次プラットフォーム更新プログラムをインストールするには、共用資産ライブラリを開き、**ソフトウェア展開可能なパッケージ** タブを選択します。ここでは、次の図に示すように、プラットフォーム更新プログラム 4 パッケージの展開の準備ができいることがわかります。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-122">To install the latest monthly platform updates in an existing environment, on [http://lcs.dynamics.com](http://lcs.dynamics.com/), go to the Shared asset library, and select the **Software deployable package** tab. There, you will see that the platform update 4 package is ready for deployment, as shown in the following illustration.</span></span> <span data-ttu-id="fdfb3-123">このパッケージをプロジェクトのアセット ライブラリにインポートしてから、更新フローを介して特定の環境に適用することができます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-123">You can import this package into the project's asset library and then apply it to a specific environment through the update flows.</span></span> <span data-ttu-id="fdfb3-124">詳細については、[アップグレード トピック](../../dev-itpro/migration-upgrade/update-platform-each-release.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-124">For more details, see the [upgrade topic](../../dev-itpro/migration-upgrade/update-platform-each-release.md).</span></span>

<span data-ttu-id="fdfb3-125">[![プラットフォーム更新 4 パッケージ](./media/1111111-1024x171.png)](./media/1111111.png)</span><span class="sxs-lookup"><span data-stu-id="fdfb3-125">[![Platform update 4 package](./media/1111111-1024x171.png)](./media/1111111.png)</span></span>

<span data-ttu-id="fdfb3-126">新しい環境では、トポロジには更新プログラム 4 が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-126">For new environments, the topology will include update 4.</span></span>

<span data-ttu-id="fdfb3-127">[![更新 4 を含むトポロジ](./media/2222222222.png)](./media/2222222222.png)</span><span class="sxs-lookup"><span data-stu-id="fdfb3-127">[![Topology that includes update 4](./media/2222222222.png)](./media/2222222222.png)</span></span>

<span data-ttu-id="fdfb3-128">[Dynamics 365 for Operations バージョン 1611](whats-new-platform-update-3.md) では、プラットフォーム モデルをオーバーレイできません。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-128">In [Dynamics 365 for Operations version 1611](whats-new-platform-update-3.md), the platform models can't be overlayered.</span></span> <span data-ttu-id="fdfb3-129">したがって、このリリースからすべての更新がバイナリであるため、**プラットフォーム X++ 更新プログラム** タイルは不要になりました。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-129">Therefore, because all the updates are binary from this release forward, the **Platform X++ Updates** tile is no longer required.</span></span> <span data-ttu-id="fdfb3-130">Dynamics 365 for Operations バージョン 1611 より前のバージョンを使用しているお客様は、引き続きプラットフォーム モデルに対するカスタマイズのために**プラットフォーム X++ 更新プログラム** タイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-130">Customers who are on versions that are earlier than Dynamics 365 for Operations version 1611 will continue to see the **Platform X++ Updates** tile for any customizations to the platform models.</span></span> <span data-ttu-id="fdfb3-131">バイナリ更新プログラムは累積的であるため、常に最新の更新プログラムを適用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-131">Because binary updates are cumulative, we recommended that you always apply the latest update.</span></span> <span data-ttu-id="fdfb3-132">詳細については、[LCS ブログ](https://blogs.msdn.microsoft.com/lcs/2017/01/26/january-2017-release-notes/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-132">For more details, see the [LCS blog](https://blogs.msdn.microsoft.com/lcs/2017/01/26/january-2017-release-notes/).</span></span> <span data-ttu-id="fdfb3-133">Microsoft Dynamics 365 for Operations プラットフォーム更新プログラム 4 でのその他の機能の概要を次に示します。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-133">Here's an overview of some of the other features in Microsoft Dynamics 365 for Operations platform update 4.</span></span>

## <a name="embedded-power-bi-reports-are-licensed-for-all-users"></a><span data-ttu-id="fdfb3-134">埋め込み Power BI レポートは、すべてのユーザーに許可されています</span><span class="sxs-lookup"><span data-stu-id="fdfb3-134">Embedded Power BI reports are licensed for all users</span></span>

<span data-ttu-id="fdfb3-135">[Power BI Embedded](../../dev-itpro/analytics/embed-power-bi-workspaces.md) は、すべてのユーザーが Dynamics 365 for Operations アプリケーションにバンドルされている分析データの豊富なグラフィカル ビューにアクセスできるようにします。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-135">[Power BI Embedded](../../dev-itpro/analytics/embed-power-bi-workspaces.md) lets all users access rich graphical views of analytical data that is bundled with Dynamics 365 for Operations applications.</span></span> <span data-ttu-id="fdfb3-136">レポートは、Dynamics 365 for Operations アプリケーションに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-136">The reports are embedded in the Dynamics 365 for Operations application.</span></span> <span data-ttu-id="fdfb3-137">それらにアクセスするために必要な追加のライセンスはありません。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-137">No additional licenses are required in order to access them.</span></span>

<span data-ttu-id="fdfb3-138">PowerBI.com サービス統合を通じて提供される既存の[タイルピン留めエクスペリエンス](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)のサポートは継続されます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-138">Support for the existing [tile pinning experience](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/) that is provided through PowerBI.com service integration will continue.</span></span> <span data-ttu-id="fdfb3-139">このエンベデッド エクスペリエンス以外の PowerBI.com の機能にアクセスするには、Pro ライセンスを別途取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-139">To access some PowerBI.com functionality outside this embedded experience, you must obtain a Pro license separately.</span></span>

## <a name="build-and-release-workspaces-that-have-embedded-power-bi-reports"></a><span data-ttu-id="fdfb3-140">Power BI レポートが埋め込まれているワークスペースのビルドおよびリリース</span><span class="sxs-lookup"><span data-stu-id="fdfb3-140">Build and release workspaces that have embedded Power BI reports</span></span>

<span data-ttu-id="fdfb3-141">フル ページの、Power BI 駆動による対話型レポートをワークスペースに埋め込むことができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-141">You can now embed full-page, Power BI driven interactive reports in workspaces.</span></span> <span data-ttu-id="fdfb3-142">Power BI がサポートする強力なインフォグラフィックやビジュアル (サード パーティによって提供される多くのコントロールを含む) を使用することで、ワークスペースは非常に視覚的でありながらインタラクティブな体験をユーザーに提供することができます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-142">By using the rich infographics and visuals that Power BI supports (even the many controls that are provided by third parties), workspaces can provide a highly visual but interactive experience for the user.</span></span>

<span data-ttu-id="fdfb3-143">[![Power BI レポートが埋め込まれているワークスペース](./media/3333333333-1024x551.png)](./media/3333333333.png)</span><span class="sxs-lookup"><span data-stu-id="fdfb3-143">[![Workspaces that has embedded Power BI reports](./media/3333333333-1024x551.png)](./media/3333333333.png)</span></span>

<span data-ttu-id="fdfb3-144">ユーザーが power user またはビジネス アナリストである場合は、Power BI ツールを使用して、既製のレポートを調整したり、新しいレポートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-144">If you're a power user or business analyst, you can use Power BI tools to tweak the ready-made reports or create new reports.</span></span> <span data-ttu-id="fdfb3-145">ユーザーが開発者であり、製品の豊富なナビゲーション エクスペリエンスを提供するためにユーザーがワークスペースとして作成したレポートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-145">If you're a developer, you can use the reports that your users develop as workspaces to create rich navigation experiences within the product.</span></span> <span data-ttu-id="fdfb3-146">パートナーおよび独立系ソフトウェア ベンダー (ISV) コミュニティーの一員である場合は、Power BI エクスペリエンスを含む豊富なワークスペースを構築し、それらのワークスペースをソリューションの一部としてリリースすることができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-146">If you're in the partner and independent software vendor (ISV) community, you can now build rich workspaces that include Power BI experiences, and you can release these workspaces as part of your solution.</span></span>

<span data-ttu-id="fdfb3-147">ユーザーが ISV またはシステム インテグレーターである場合は、Microsoft Dynamics Lifecycle Services (LCS) ソリューションの一部として、[Power BI の有効化されたワークスペースをパッケージ化](../../dev-itpro/analytics/power-bi-embedded-integration.md)(ナビゲーション エクスペリエンスと共に) できます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-147">If you're an ISV or a systems integrator, you can [package Power BI enabled workspaces](../../dev-itpro/analytics/power-bi-embedded-integration.md) (together with navigational experiences) as part of a Microsoft Dynamics Lifecycle Services (LCS) solution.</span></span> <span data-ttu-id="fdfb3-148">顧客は同じ体験をしますが、PowerBI.com サブスクリプションは必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-148">Your customers get the same experience but don't have to have a PowerBI.com subscription.</span></span> <span data-ttu-id="fdfb3-149">このソリューションは Dynamics 365 for Operations でのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-149">The solution works with just Dynamics 365 for Operations.</span></span>

<span data-ttu-id="fdfb3-150">これらの機能およびその他の Power BI 機能に関する詳細については、[BI ブログ](https://blogs.msdn.microsoft.com/dynamicsaxbi/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-150">For more details about these features and other Power BI features, see the [BI blog](https://blogs.msdn.microsoft.com/dynamicsaxbi/).</span></span>

## <a name="mobility"></a><span data-ttu-id="fdfb3-151">モビリティ</span><span class="sxs-lookup"><span data-stu-id="fdfb3-151">Mobility</span></span>

<span data-ttu-id="fdfb3-152">Dynamics 365 for Operations のモバイル フレームワークを大幅に向上させました。これにより、パートナーは、固有で完全に機能的なモバイル エクスペリエンスとなるワークスペースを構築できます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-152">We have made major progress on the mobile framework for Dynamics 365 for Operations that lets partners build workspaces that are unique and fully functional mobile experiences.</span></span> <span data-ttu-id="fdfb3-153">これらの新機能により、ユーザーはオンラインとオフラインの両方で Dynamics 365 for Operations とより簡単に対話できます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-153">These new capabilities make it easier for users to interact with Dynamics 365 for Operations both online and offline.</span></span> <span data-ttu-id="fdfb3-154">モバイルフ レームワークは、iOS と Android デバイスをサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-154">The mobile framework now supports iOS and Android devices.</span></span> <span data-ttu-id="fdfb3-155">詳細については、次回の [Mobility ブログ](https://blogs.msdn.microsoft.com/Dynamics365forOperationsMobile/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-155">For more details, see the upcoming [mobility blog](https://blogs.msdn.microsoft.com/Dynamics365forOperationsMobile/).</span></span>

<span data-ttu-id="fdfb3-156">[![モバイル フレームワークを使用して構築されたワークスペース](./media/444444444444-1024x533.png)](./media/444444444444.png)</span><span class="sxs-lookup"><span data-stu-id="fdfb3-156">[![Workspace that was built by using the mobile framework](./media/444444444444-1024x533.png)](./media/444444444444.png)</span></span>

## <a name="visual-scheduling"></a><span data-ttu-id="fdfb3-157">視覚的スケジューリング</span><span class="sxs-lookup"><span data-stu-id="fdfb3-157">Visual scheduling</span></span>

<span data-ttu-id="fdfb3-158">今回のリリースで、[ビジュアル スケジューリング](../../dev-itpro/user-interface/gantt-development-guide.md)を更新しました。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-158">We have made updates to [visual scheduling](../../dev-itpro/user-interface/gantt-development-guide.md) in this release:</span></span>

- <span data-ttu-id="fdfb3-159">ガント チャートで明示的に活動を整理することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-159">You can now explicitly order activities in the Gantt chart.</span></span> <span data-ttu-id="fdfb3-160">ガント チャート内の活動および同じプロジェクト内の移動タスクの順序を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-160">You can set the order of activities in the Gantt chart and move tasks within the same project.</span></span>
- <span data-ttu-id="fdfb3-161">ビジュアル アイコンをタスクに対して使用できます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-161">Visual icons are available for tasks.</span></span> <span data-ttu-id="fdfb3-162">たとえば、警告およびエラーのアイコンがあります。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-162">For example, there are icons for warning and errors.</span></span>
- <span data-ttu-id="fdfb3-163">日付と時刻の書式がローカライズされました。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-163">Date and time formats are now localized.</span></span>
- <span data-ttu-id="fdfb3-164">選択した複数のタスク上でドラッグ アンド ドロップ操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-164">You can perform drag-and-drop operations on multiple selected tasks.</span></span>
- <span data-ttu-id="fdfb3-165">リソース能力バーは、予約超過がある時間間隔を明確に示します。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-165">A resource capacity bar clearly flags time intervals where there is overbooking.</span></span>

<span data-ttu-id="fdfb3-166">[![視覚的スケジューリング](./media/55555555555-1024x539.png)](./media/55555555555.png)</span><span class="sxs-lookup"><span data-stu-id="fdfb3-166">[![Visual scheduling](./media/55555555555-1024x539.png)](./media/55555555555.png)</span></span>

## <a name="feedback"></a><span data-ttu-id="fdfb3-167">フィードバック</span><span class="sxs-lookup"><span data-stu-id="fdfb3-167">Feedback</span></span>

<span data-ttu-id="fdfb3-168">フィードバックを常に大切に扱います。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-168">We always value your feedback.</span></span> <span data-ttu-id="fdfb3-169">この更新処理の一環として、定期的に製品の推奨を評価するように要求されます。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-169">As part of this update, we periodically prompt you to rate your recommendation of the product.</span></span> <span data-ttu-id="fdfb3-170">お客様の経験の継続な向上に役立たせるために、このフィードバックのご提供をお願いいたします。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-170">We encourage you to provide this feedback to help us continually improve your experience.</span></span> <span data-ttu-id="fdfb3-171">改善可能な領域の詳細情報を提供することも推奨します。</span><span class="sxs-lookup"><span data-stu-id="fdfb3-171">We also encourage you to provide details about areas where we can improve.</span></span>

<span data-ttu-id="fdfb3-172">[![フィードバックの確認](./media/6666666666-1024x453.png)](./media/6666666666.png)</span><span class="sxs-lookup"><span data-stu-id="fdfb3-172">[![Prompt for feedback](./media/6666666666-1024x453.png)](./media/6666666666.png)</span></span>
