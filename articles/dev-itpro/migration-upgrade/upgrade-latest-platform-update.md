---
title: "Dynamics 365 Finance and Operations 環境に最新のプラットフォーム更新プログラムを適用"
description: "ここでは、Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 環境に最新のプラットフォーム リリースを適用する方法について説明します。"
author: tariqbell
manager: AnnBe
ms.date: 03/06/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 253274
ms.assetid: a70a4f28-9269-4b35-bc29-1edba0b92d83
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fdb2f3dace42f735b5f2bed5c2a60a63a7690962
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="apply-the-latest-platform-update-to-your-microsoft-dynamics-365-finance-and-operations-environment"></a><span data-ttu-id="15222-103">Microsoft Dynamics 365 Finance and Operations 環境への最新のプラットフォーム更新プログラムの適用</span><span class="sxs-lookup"><span data-stu-id="15222-103">Apply the latest platform update to your Microsoft Dynamics 365 Finance and Operations environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15222-104">ここでは、Microsoft Dynamics 365 for Finance and Operations 環境に最新のプラットフォーム リリースを適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="15222-104">This topic explains how to apply the latest platform release to your Microsoft Dynamics 365 for Finance and Operations environment.</span></span>

## <a name="overview"></a><span data-ttu-id="15222-105">概要</span><span class="sxs-lookup"><span data-stu-id="15222-105">Overview</span></span>

<span data-ttu-id="15222-106">Microsoft Dynamics 365 for Finance and Operations プラットフォームは、次のコンポーネントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="15222-106">The Microsoft Dynamics 365 for Finance and Operations platform consists of the following components:</span></span>

-   <span data-ttu-id="15222-107">Application Object Server (AOS)、データ管理フレームワーク、レポートおよびビジネス インテリジェンス (BI) フレームワーク、開発ツール、および分析サービスなどの Finance and Operations プラットフォーム バイナリ。</span><span class="sxs-lookup"><span data-stu-id="15222-107">Finance and Operations platform binaries such as Application Object Server (AOS), the data management framework, the reporting and business intelligence (BI) framework, development tools, and analytics services.</span></span>
-   <span data-ttu-id="15222-108">次のアプリケーション オブジェクト ツリー (AOT) パッケージ。</span><span class="sxs-lookup"><span data-stu-id="15222-108">The following Application Object Tree (AOT) packages:</span></span>
    -   <span data-ttu-id="15222-109">アプリケーション プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="15222-109">Application Platform</span></span>
    -   <span data-ttu-id="15222-110">アプリケーション基準</span><span class="sxs-lookup"><span data-stu-id="15222-110">Application Foundation</span></span>
    -   <span data-ttu-id="15222-111">Test Essentials</span><span class="sxs-lookup"><span data-stu-id="15222-111">Test Essentials</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15222-112">最新の Finance and Operations プラットフォームに移行するためには、Finance and Operations の実装で、プラットフォームに属する AOT パッケージのカスタマイズ (オーバーレイヤー) を行うことは**できません**。</span><span class="sxs-lookup"><span data-stu-id="15222-112">To move to the latest Finance and Operations platform, your Finance and Operations implementation **cannot** have any customizations (overlayering) of any of the AOT packages that belong to the platform.</span></span> <span data-ttu-id="15222-113">この制限は、プラットフォーム更新 3 で導入されたため、プラットフォームにシームレスに継続的な更新を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="15222-113">This restriction was introduced in Platform update 3, so that seamless continuous updates can be made to the platform.</span></span> <span data-ttu-id="15222-114">プラットフォーム 更新プログラム 3 よりも古いプラットフォームで実行している場合、「[以前のビルドからプラットフォーム更新プログラム 3 にアップグレードする](#Upgrading-to-platform-update-3-from-an-earlier-build)」というセクションを参照します。</span><span class="sxs-lookup"><span data-stu-id="15222-114">If you are running on a platform that is older than Platform update 3, see the section [Upgrading to Platform update 3 from an earlier build](#Upgrading-to-platform-update-3-from-an-earlier-build) section at the end of this topic.</span></span>

## <a name="overall-flow"></a><span data-ttu-id="15222-115">全体的な流れ</span><span class="sxs-lookup"><span data-stu-id="15222-115">Overall flow</span></span>
<span data-ttu-id="15222-116">次の図は、Finance and Operations プラットフォームを最新の更新プログラムにアップグレードするための全体的なプロセスを示しています。</span><span class="sxs-lookup"><span data-stu-id="15222-116">The following illustration shows the overall process for upgrading the Finance and Operations platform to the latest update.</span></span>

<span data-ttu-id="15222-117">[![プラットフォームのカスタマイズがない実装のアップグレード プロセス](./media/flownocustomisations.jpg)](./media/flownocustomisations.jpg)</span><span class="sxs-lookup"><span data-stu-id="15222-117">[![Upgrade process for implementations that have no customization of the platform](./media/flownocustomisations.jpg)](./media/flownocustomisations.jpg)</span></span>

<span data-ttu-id="15222-118">既にプラットフォーム更新プログラム 4 以降で実行している場合は、Finance and Operations プラットフォームを最新のリリースに更新することが単純なサービス工程となります。</span><span class="sxs-lookup"><span data-stu-id="15222-118">If you are already running on platform update 4 or later, updating the Finance and Operations platform to the latest release is a simple servicing operation.</span></span> <span data-ttu-id="15222-119">プラットフォーム更新プログラムのパッケージが LCS アセット ライブラリに入ったら、LCS 環境ページから更新を適用するためにフローに従います。メンテナンスで更新プログラムの適用を選択し、プラットフォーム更新プログラム パッケージを選択します。</span><span class="sxs-lookup"><span data-stu-id="15222-119">Once the platform update package is in your LCS asset library, follow the flow to apply an update from the LCS environment page: Select Apply updates under Maintain then select the platform update package.</span></span>

<span data-ttu-id="15222-120">[![更新プログラムの適用](./media/applyupdates.jpg)](./media/applyupdates.jpg)</span><span class="sxs-lookup"><span data-stu-id="15222-120">[![Apply updates](./media/applyupdates.jpg)](./media/applyupdates.jpg)</span></span>

<span data-ttu-id="15222-121">次のセクションでは**最新のプラットフォーム パッケージを取得して、LCS を通じて配置された環境に適用する**方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="15222-121">Learn how to **get the latest platform package and apply it to an environment deployed through LCS** in the next section.</span></span>

## <a name="apply-the-latest-platform-update-package"></a><span data-ttu-id="15222-122">最新のプラットフォーム更新プログラム パッケージを適用</span><span class="sxs-lookup"><span data-stu-id="15222-122">Apply the latest platform update package</span></span>
<span data-ttu-id="15222-123">LCS で、環境ページから最新のプラットフォーム更新パッケージを入手するには、2つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="15222-123">There are two ways to get the latest platform update package in LCS from your environment page.</span></span>
- <span data-ttu-id="15222-124">**プラットフォーム バイナリ更新プログラム** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="15222-124">Click the **Platform binary updates** tile</span></span> 
- <span data-ttu-id="15222-125">**すべてのバイナリ更新プログラム** タイルをクリックすると、アプリケーションとプラットフォームのバイナリ アップデートのパッケージの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="15222-125">Click the **All Binary Updates** tile to see a list of combined package of application and platform binary updates.</span></span> <span data-ttu-id="15222-126">(現在のプラットフォーム更新プログラム 4 では、LCS のバイナリ更新プログラムに、最新のプラットフォームへのアップグレードが含まれています)。</span><span class="sxs-lookup"><span data-stu-id="15222-126">(As of Platform update 4, binary updates from LCS include an upgrade to the latest platform).</span></span>

> [!NOTE]
> <span data-ttu-id="15222-127">LCS の環境ページのタイルは、現在のバージョンと環境の状態に基づいて、環境に適用される更新のみを表示します。</span><span class="sxs-lookup"><span data-stu-id="15222-127">Tiles on an environment's page in LCS show only the updates that are applicable to your environment based on the current version and state of the environment.</span></span>

<span data-ttu-id="15222-128">上記に示されたように、2 つのタイルのいずれかをクリックして、最新のプラットフォーム更新プログラム パッケージを取得します。</span><span class="sxs-lookup"><span data-stu-id="15222-128">Get the latest platform update package by clicking on one of the two tiles as mentioned above.</span></span> <span data-ttu-id="15222-129">プラットフォームに含まれる修正を確認した後に、**パッケージの保存**をクリックして、プロジェクト アセット ライブラリにパッケージを保存します。</span><span class="sxs-lookup"><span data-stu-id="15222-129">After reviewing the fixes included in the platform, click **Save Package** to save the package to the project asset library.</span></span>

<span data-ttu-id="15222-130">プロセスの観点では、プラットフォーム更新プログラム パッケージの展開は、バイナリ修正プログラムの展開可能なパッケージに似ています。</span><span class="sxs-lookup"><span data-stu-id="15222-130">From a process perspective, deploying a platform upgrade package resembles a binary hotfix deployable package.</span></span>

-   <span data-ttu-id="15222-131">クラウド開発、ビルド、デモ、第 2 層サンド ボックス、または実稼働環境にプラットフォーム更新パッケージを適用するには、LCS から直接更新します。</span><span class="sxs-lookup"><span data-stu-id="15222-131">To apply a platform update package to your cloud development, build, demo, tier-2 sandbox, or production environment, update directly from LCS.</span></span>
<span data-ttu-id="15222-132">[![更新プログラムの適用](./media/applyupdates.jpg)](./media/applyupdates.jpg)</span><span class="sxs-lookup"><span data-stu-id="15222-132">[![Apply updates](./media/applyupdates.jpg)](./media/applyupdates.jpg)</span></span>

<span data-ttu-id="15222-133">詳細については、[配置可能パッケージの適用](../deployment/apply-deployable-package-system.md) で、バイナリ修正プログラムを適用するための指示に従って下さい。</span><span class="sxs-lookup"><span data-stu-id="15222-133">For more details, follow the instructions for applying a binary hotfix in [Apply a deployable package](../deployment/apply-deployable-package-system.md).</span></span>

> [!NOTE]
> <span data-ttu-id="15222-134">**ドキュメント管理用のファイルの移行**: プラットフォーム更新プログラム 6 以降にアップグレードした後、管理者は**ドキュメント管理パラメーター**ページの**ファイルの移行**ボタンをクリックして、アップグレード プロセスを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15222-134">**Migrate files for Document management**: After upgrading to Platform update 6 or later, an administrator needs to click the **Migrate Files** button on the **Document management parameters** page to finish the upgrade process.</span></span> <span data-ttu-id="15222-135">これにより、データベースに格納されている添付ファイルが BLOB ストレージに移行されます。</span><span class="sxs-lookup"><span data-stu-id="15222-135">This will migrate any attachments stored in the database to blob storage.</span></span> <span data-ttu-id="15222-136">移行はバッチ プロセスとして実行され、データベースから Azure Blob Storage に移動されるファイルの数とサイズに応じて、時間がかかる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="15222-136">The migration will run as a batch process and could take a long time, depending on the number and size of the files being moved from the database into Azure blob storage.</span></span> <span data-ttu-id="15222-137">移行プロセスの実行中に、ユーザーは引き続き添付ファイルを使用できるため、移行には、ユーザーが気づくほどの影響はありません。</span><span class="sxs-lookup"><span data-stu-id="15222-137">The attachments will continue to be available to users while the migration process is running, so there should be no noticeable effects from the migration.</span></span> <span data-ttu-id="15222-138">バッチ処理がまだ実行されているかどうかを確認するには、**バッチ ジョブ** ページで **データベースに格納されたファイルをブロブ ストレージに移行する** プロセスを探します。</span><span class="sxs-lookup"><span data-stu-id="15222-138">To check if the batch process is still running, look for the **Migrate files stored in the database to blob storage** process on the **Batch jobs** page.</span></span>

## <a name="apply-a-platform-update-to-environments-that-are-not-connected-to-lcs"></a><span data-ttu-id="15222-139">LCS に接続されていない環境にプラットフォーム更新プログラムを適用します</span><span class="sxs-lookup"><span data-stu-id="15222-139">Apply a platform update to environments that are not connected to LCS</span></span>
<span data-ttu-id="15222-140">このセクションでは、プラットフォーム更新パッケージを*ローカル開発環境* (LCS に接続されていないもの) に適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="15222-140">This section describes how to apply a platform update package to a *local development environment* (one that that is not connected to LCS).</span></span>

### <a name="how-to-get-the-platform-update-package"></a><span data-ttu-id="15222-141">プラットフォーム更新プログラム パッケージを取得する方法</span><span class="sxs-lookup"><span data-stu-id="15222-141">How to get the platform update package</span></span>
<span data-ttu-id="15222-142">プラットフォーム更新プログラム パッケージは、Microsoft によってリリースされ、Microsoft Dynamics Lifecycle Services (LCS) の共有資産ライブラリからインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="15222-142">Platform update packages are released by Microsoft and can be imported from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="15222-143">パッケージ名の先頭に **Dynamics 365 Unified Operations Platform Update** が付きます。</span><span class="sxs-lookup"><span data-stu-id="15222-143">The package name is prefixed with **Dynamics 365 Unified Operations Platform Update**.</span></span> <span data-ttu-id="15222-144">プラットフォーム更新プログラムのパッケージをインポートするには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="15222-144">Use these steps to import the platform update package:</span></span>

1.  <span data-ttu-id="15222-145">LCS プロジェクトの資産ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="15222-145">Go to your LCS project's Asset library.</span></span>
2.  <span data-ttu-id="15222-146">**ソフトウェア配置可能パッケージ**タブで、**インポート**をクリックし、プラットフォーム更新プログラム パッケージへの参照を作成します。</span><span class="sxs-lookup"><span data-stu-id="15222-146">On the **Software deployable package** tab, click **Import** to create a reference to the platform update package.</span></span> <span data-ttu-id="15222-147">[![ボタンのインポート](./media/importupgradepackage.png)](./media/importupgradepackage.png)</span><span class="sxs-lookup"><span data-stu-id="15222-147">[![Import button](./media/importupgradepackage.png)](./media/importupgradepackage.png)</span></span>
3.  <span data-ttu-id="15222-148">目的のプラットフォーム更新プログラム パッケージを選択します。</span><span class="sxs-lookup"><span data-stu-id="15222-148">Select the desired platform update package.</span></span>

> [!NOTE]
> <span data-ttu-id="15222-149">共有アセット ライブラリのパッケージは、目的のプラットフォーム リリースの最新ビルド (ホットフィックス付き) に対応していない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="15222-149">The package in the Shared Asset library may not correspond to the latest build (with hotfixes) of the desired platform release.</span></span> <span data-ttu-id="15222-150">最新のビルドを保証するには、この記事の前半で説明した LCS 環境ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="15222-150">To guarrantee the latest build, use the LCS environment page as described earlier in this article.</span></span>

### <a name="apply-the-platform-update-package-to-your-development-environment"></a><span data-ttu-id="15222-151">開発環境にプラットフォーム更新プログラム パッケージを適用</span><span class="sxs-lookup"><span data-stu-id="15222-151">Apply the platform update package to your development environment</span></span>
> [!NOTE]
> <span data-ttu-id="15222-152">これらの手順は、LCS から直接更新できない環境にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="15222-152">These instructions apply only to environments that cannot be updated directly from LCS.</span></span>

### <a name="install-the-deployable-package"></a><span data-ttu-id="15222-153">配置可能パッケージのインストール</span><span class="sxs-lookup"><span data-stu-id="15222-153">Install the deployable package</span></span>

1.  <span data-ttu-id="15222-154">プラットフォーム更新パッケージ (AXPlatformUpdate.zip) を使用中の仮想マシン (VM) にダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="15222-154">Download the platform update package (AXPlatformUpdate.zip) to your virtual machine (VM).</span></span>
2.  <span data-ttu-id="15222-155">コンテンツをローカル ディレクトリに解凍します。</span><span class="sxs-lookup"><span data-stu-id="15222-155">Unzip the contents to a local directory.</span></span>
3.  <span data-ttu-id="15222-156">アップグレードする環境のタイプに応じて、\\AOSService\\ スクリプトの下の PlatformUpdatePackages.Config ファイルを開き、**MetaPackage** 値を変更します。</span><span class="sxs-lookup"><span data-stu-id="15222-156">Depending on the type of environment that you're upgrading, open the PlatformUpdatePackages.Config file under \\AOSService\\Scripts, and change the **MetaPackage** value.</span></span>
    -   <span data-ttu-id="15222-157">開発をアップグレードする場合、またはソース コードが含まれているデモ環境をアップグレードする場合は、**MetaPackage** 値を **dynamicsax-meta-platform-development** に変更します。</span><span class="sxs-lookup"><span data-stu-id="15222-157">If you're upgrading a development or demo environment that contains source code, change the **MetaPackage** value to **dynamicsax-meta-platform-development**.</span></span>
    -   <span data-ttu-id="15222-158">レベル 2 のサンド ボックスやソース コードが含まれていない別の環境を含むランタイム環境をアップグレードする場合は、既定値の **dynamicsax-meta-platform-runtime** は正しい値になります。</span><span class="sxs-lookup"><span data-stu-id="15222-158">If you're upgrading a runtime environment, such as a tier-2 sandbox environment or another environment that doesn't contain source code, the default value, **dynamicsax-meta-platform-runtime**, is correct.</span></span>

> [!NOTE]
> <span data-ttu-id="15222-159">Platform Update 4 以降にアップグレードするときは、手順 3 は適用されません。</span><span class="sxs-lookup"><span data-stu-id="15222-159">Step 3 is not applicable when upgrading to platform update 4 or later.</span></span>

4.  <span data-ttu-id="15222-160">配置可能パッケージをインストールする指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="15222-160">Follow the instructions for installing a deployable package.</span></span> <span data-ttu-id="15222-161">[配置可能パッケージのインストール](../deployment/install-deployable-package.md)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="15222-161">See [Install a deployable package](../deployment/install-deployable-package.md).</span></span>
5.  <span data-ttu-id="15222-162">開発環境で作業している場合、アプリケーションのコードをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="15222-162">If you're working in a development environment, rebuild your application’s code.</span></span>

#### <a name="example"></a><span data-ttu-id="15222-163">例</span><span class="sxs-lookup"><span data-stu-id="15222-163">Example</span></span>

<span data-ttu-id="15222-164">\`\`\`AXUpdateInstaller.exe generate -runbookid="OneBoxDev" -topologyfile="DefaultTopologyData.xml" -servicemodelfile="DefaultServiceModelData.xml" -runbookfile="OneBoxDev-runbook.xml"</span><span class="sxs-lookup"><span data-stu-id="15222-164">\`\`\`AXUpdateInstaller.exe generate -runbookid="OneBoxDev" -topologyfile="DefaultTopologyData.xml" -servicemodelfile="DefaultServiceModelData.xml" -runbookfile="OneBoxDev-runbook.xml"</span></span>

    AXUpdateInstaller.exe import -runbookfile=OneBoxDev-runbook.xml

    AXUpdateInstaller.exe execute -runbookid=OneBoxDev
```

### Install the Visual Studio development tools (Platform update 3 or earlier)

> [!NOTE]
> Skip this section if you are updating to platform update 4 or later, development tools are automatically installed as part of installing the deployable package.

Update the Visual Studio development tools as described in [Updating the Visual Studio development tools](../dev-tools/update-development-tools.md).

### Regenerate form adaptor models

Form adaptor models are required for test automation. Regenerate the platform form adaptor models, based on the newly updated platform models. Use the xppfagen.exe tool to generate the form adaptor models. This tool is located in the package's bin folder (typically, j:\\AosService\\PackagesLocalDirectory\\bin). Here is a list of the platform form adaptor models:

-   ApplicationPlatformFormAdaptor
-   ApplicationFoundationFormAdaptor
-   DirectoryFormAdaptor

The following examples show how to generate the form adaptor models.
```
<span data-ttu-id="15222-165">xppfagen.exe -metadata=j:\AosService\PackagesLocalDirectory -model="ApplicationPlatformFormAdaptor" -xmllog="c:\temp\log1.xml"</span><span class="sxs-lookup"><span data-stu-id="15222-165">xppfagen.exe -metadata=j:\AosService\PackagesLocalDirectory -model="ApplicationPlatformFormAdaptor" -xmllog="c:\temp\log1.xml"</span></span>

<span data-ttu-id="15222-166">xppfagen.exe -metadata=j:\AosService\PackagesLocalDirectory -model="ApplicationFoundationFormAdaptor" -xmllog="c:\temp\log2.xml"</span><span class="sxs-lookup"><span data-stu-id="15222-166">xppfagen.exe -metadata=j:\AosService\PackagesLocalDirectory -model="ApplicationFoundationFormAdaptor" -xmllog="c:\temp\log2.xml"</span></span>

<span data-ttu-id="15222-167">xppfagen.exe -metadata=j:\AosService\PackagesLocalDirectory -model="DirectoryFormAdaptor" -xmllog="c:\temp\log3.xml"</span><span class="sxs-lookup"><span data-stu-id="15222-167">xppfagen.exe -metadata=j:\AosService\PackagesLocalDirectory -model="DirectoryFormAdaptor" -xmllog="c:\temp\log3.xml"</span></span>
```

### Install the Data Management service (Platform update 3 or earlier)

> [!NOTE]
> Skip this section if you are updating to platform update 4 or newer, the data management service is automatically installed as part of installing the deployable package.

After the deployable package is installed, follow these instructions to install the new Data Management service. Open a **Command Prompt** window as an administrator, and run the following commands from the .\\DIXFService\\Scripts folder.

    msiExec.exe /uninstall {5C74B12A-8583-4B4F-B5F5-8E526507A3E0} /passive /qn /quiet

If you're connected to Microsoft SQL Server Integration Services 2016 (13.0), run the following command.

    msiexec /i "DIXF_Service_x64.msi" ISSQLSERVERVERSION="Bin\2012" SERVICEACCOUNT="NT AUTHORITY\NetworkService" /qb /lv DIXF_log.txt

If you're connected to an earlier release of Microsoft SQL Server Integration Services, run the following command.

    msiexec /i "DIXF_Service_x64.msi" ISSQLSERVERVERSION="Bin" SERVICEACCOUNT="NT AUTHORITY\NetworkService" /qb /lv DIXF_log.txt

## Apply the platform update package on a build environment (Platform update 6 or earlier)

> [!NOTE]
> Skip this section if you are updating to platform update 7 or newer. This was a pre-requesite step for build environments.

If the build machine has been used for one or more builds, you should restore the metadata packages folder from the metadata backup folder before you upgrade the VM to a newer Dynamics 365 for Finance and Operations platform. You should then delete the metadata backup. These steps help ensure that the platform update will be applied on a clean environment. The next build process will then detect that no metadata backup exists and will automatically create a new one. This new metadata backup will include the updated platform. To determine whether a complete metadata backup exists, look for a BackupComplete.txt file in I:\\DynamicsBackup\\Packages (or C:\\DynamicsBackup\\Packages on a downloadable virtual hard disk \[VHD\]). If this file is present, a metadata backup exists, and the file will contain a timestamp that indicates when it was created. To restore the deployment's metadata packages folder from the metadata backup, open an elevated Windows PowerShell **Command Prompt** window, and run the following command. This command will run the same script that is used in the first step of the build process.

    if (Test-Path -Path "I:\DynamicsBackup\Packages\BackupComplete.txt") { C:\DynamicsSDK\PrepareForBuild.ps1 }

If a complete metadata backup doesn't exist, the command will create a new backup. This command will also stop the Finance and Operations deployment services and Internet Information Services (IIS) before it restores the files from the metadata backup to the deployment's metadata packages folder. 
You should see output that resembles the following example. 
```
<span data-ttu-id="15222-168">午後 6 時 17 分 52 秒: ビルド定義環境を準備しています...\* <em>午後 6 時 17 分 53 秒: 指定された値で Dynamics SDK のレジストリ キーを更新しています...</em> <em>午後 6 時 17 分 53 秒: AOS の web config からの値で Dynamics SDK レジストリ キーを更新しています...</em> <em>午後 6 時 17 分 53 秒: Finance and Operations の配置を停止しています...</em> <em>午後 6 時 18 分 06 秒: \*\*バックアップが次の場所に既に存在します: I:\\DynamicsBackup\\Packages。新しいバックアップは作成されません</em><em>。</em></span><span class="sxs-lookup"><span data-stu-id="15222-168">6:17:52 PM: Preparing build environment...\* <em>6:17:53 PM: Updating Dynamics SDK registry key with specified values...</em> <em>6:17:53 PM: Updating Dynamics SDK registry key with values from AOS web config...</em> <em>6:17:53 PM: Stopping Finance and Operations deployment...</em> <em>6:18:06 PM: \*\*A backup already exists at: I:\\DynamicsBackup\\Packages. No new backup will be created</em><em>.</em></span></span> <span data-ttu-id="15222-169"><em>午後 6 時 18 分 6 秒: **メタデータ パッケージをバックアップから復元する</em>** <em>午後 6 時 22 分 56 秒: **メタデータ パッケージを正常にバックアップから復元しました</em><em>。</em></span><span class="sxs-lookup"><span data-stu-id="15222-169"><em>6:18:06 PM: **Restoring metadata packages from backup...</em>** <em>6:22:56 PM: **Metadata packages successfully restored from backup</em><em>.</em></span></span> <span data-ttu-id="15222-170"><em>午後 6 時 22 分 57: ビルド環境の準備が完了しました。</em></span><span class="sxs-lookup"><span data-stu-id="15222-170"><em>6:22:57 PM: Preparing build environment complete.</em></span></span> <span data-ttu-id="15222-171"><em>午後 6 時 22 分 57 秒: 終了コード 0 でスクリプトが完了</em></span><span class="sxs-lookup"><span data-stu-id="15222-171"><em>6:22:57 PM: Script completed with exit code: 0</em></span></span> 
```

After the metadata backup has been restored, delete (or rename) the metadata backup folder (DynamicsBackup\\Packages), so that it will no longer be found by the build process.

### Apply the platform update package

After you've prepared your build environment for this update, apply the platform update package by using the same method that you use on other environments.

## Upgrading to platform update 3 from an earlier build
When upgrading to platform update 3 from an earlier build, there are some very important considerations because of two key changes in update 3:

- It is no longer possible to overlayer platform models (Application Platform, Application Foundation, Test Essentials).
- You need to delete all X++ hotfixes to the platform that are in you version control (see the section below)
- The Directory model is no longer in platform, it has moved to the application in Finance and Operations release 1611.

This means two things:

1.  If taking only platform update 3 and not taking the application update (Finance and Operations version 1611), then you cannot have overlayering on any of the following models. All overlayering on these models must be removed before attempting to install update 3:
    -   Application Platform
    -   Application Foundation
    -   Test Essentials
    -   Directory

2.  If you cannot remove over-layering from the Directory model, and you still want to upgrade, you will have to do a complete upgrade of the platform and the application (Finance and Operations version 1611) as described in [Overview of moving to the latest update of Finance and Operations](upgrade-latest-update.md).

### Delete platform metadata hotfixes from your VSTS project (Platform update 2 or earlier)

> [!NOTE]
> This section is not relevant if you are already on Platform update 3 and updating to a newer platform.

Before you install the new platform update, you must clean up your Microsoft Visual Studio Team Services (VSTS) source control project.
Remove any X++ or metadata hotfixes that you've installed on your existing platform. If you have any X++ or metadata hotfixes that are checked in to your VSTS project for any of the following Microsoft models, delete them from your project by using the Microsoft Visual Studio Source Control Explorer.

-   Application Platform
-   Application Foundation
-   TestEssentials
-   Directory

You can find these hotfixes by browsing the check-in history of these Microsoft models. For example, use Source Control Explorer to browse the check-in history of the Trunk\\Main\\Metadata\\ApplicationFoundation\\ApplicationFoundation folder, and delete all XML files that have been checked in to it.
![View History](./media/checkinhistory.png)

Additional resources
--------

[Overview of moving to the latest update of Microsoft Dynamics 365 for Finance and Operations](upgrade-latest-update.md)



