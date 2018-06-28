---
title: "構成マネージャーの設定"
description: "このトピックでは、構成マネージャーの設定方法について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012, Operations
ms.custom: 62673
ms.assetid: 0845ab95-9597-4813-9967-e4f3815849ba
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: bb8279b09aa1c75536b275e60c8add254a570513
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-configuration-manager"></a><span data-ttu-id="df532-103">構成マネージャーの設定</span><span class="sxs-lookup"><span data-stu-id="df532-103">Set up Configuration manager</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="df532-104">この機能は、運用上の用途ではサポートされて**いません**。 </span><span class="sxs-lookup"><span data-stu-id="df532-104">This feature is **not** supported for production use.</span></span> <span data-ttu-id="df532-105">構成マネージャー (ベータ) は、環境内のデータのインポート/エクスポート フレームワークからのエンティティに依存します。</span><span class="sxs-lookup"><span data-stu-id="df532-105">Configuration manager (beta) relies on entities from the Data Import/Export Framework in your environment.</span></span> <span data-ttu-id="df532-106">これらのエンティティには現在 AX 2012 R3 のすべての機能が含まれていないため、一部の構成データは環境間でコピーされません。</span><span class="sxs-lookup"><span data-stu-id="df532-106">Because these entities do not currently include all the functionality in AX 2012 R3, some configuration data is not copied between environments.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="df532-107">準備</span><span class="sxs-lookup"><span data-stu-id="df532-107">Before you begin</span></span>
<span data-ttu-id="df532-108">開始する前に、環境には次のコンポーネントが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="df532-108">Before you begin, your environment must include the following components:</span></span>

- <span data-ttu-id="df532-109">業務に合わせてコンフィギュレーションされた実行中の AX 2012 R3 のバージョン。</span><span class="sxs-lookup"><span data-stu-id="df532-109">A running version of AX 2012 R3 that has been configured for your business.</span></span> <span data-ttu-id="df532-110">AX 2012 R3 をインストールする方法の詳細については、[Microsoft Dynamics AX 2012 のインストール](http://technet.microsoft.com/library/fbe52b68-1294-4398-b233-f8ec37c6d531(AX.60).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df532-110">For more information about how to install AX 2012 R3, see [Install Microsoft Dynamics AX 2012](http://technet.microsoft.com/library/fbe52b68-1294-4398-b233-f8ec37c6d531(AX.60).aspx).</span></span>
- <span data-ttu-id="df532-111">実行中のデータのインポート/エクスポート フレームワークのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="df532-111">A running instance of the Data Import/Export Framework.</span></span> <span data-ttu-id="df532-112">データのインポート/エクスポート フレームワークをインストールする方法の詳細については、[データのインポート/エクスポート フレームワークをインストール (AX 2012)](./ax-2012/install-dixf.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df532-112">For more information about how to install the Data Import/Export Framework, see [Install the Data import/export framework (AX 2012)](./ax-2012/install-dixf.md).</span></span> 
  > [!IMPORTANT]
  > <span data-ttu-id="df532-113">データのインポート/エクスポート フレームワークへ接続するためには、構成マネージャー (ベータ) を有効にする DMFEntityExecutionStatusService および DMFService サービス グループを配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df532-113">You must deploy the DMFEntityExecutionStatusService and DMFService service groups to enable to Configuration manager (beta) to connect to Data Import/Export Framework.</span></span>
- <span data-ttu-id="df532-114">Lifecycle Services の AX 2012 R3 プロジェクトです。</span><span class="sxs-lookup"><span data-stu-id="df532-114">An AX 2012 R3 project in Lifecycle Services.</span></span> 
  > [!WARNING]
  > <span data-ttu-id="df532-115">環境間でコンフィギュレーションをコピーすることは破壊的な操作になります。</span><span class="sxs-lookup"><span data-stu-id="df532-115">Copying configurations between environments can be a destructive operation.</span></span> <span data-ttu-id="df532-116">すべてのプロジェクト所有者は構成およびこれらの操作を実行する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="df532-116">All project owners have the right to configure and perform these operations.</span></span> <span data-ttu-id="df532-117">信頼されたユーザーのみがプロジェクト所有者として設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="df532-117">Make sure that only trusted individuals are set as project owners.</span></span>

## <a name="create-data-importexport-framework-source-data-formats-in-ax-2012-r3"></a><span data-ttu-id="df532-118">AX 2012 R3 でのデータのインポート/エクスポート フレームワーク ソース データ形式の作成</span><span class="sxs-lookup"><span data-stu-id="df532-118">Create Data Import/Export Framework source data formats in AX 2012 R3</span></span>
<span data-ttu-id="df532-119">構成をエクスポートおよびインポートするすべての環境で構成を管理するには、Dynamics AX と CSV ソース データ形式の両方を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df532-119">You must create both a Dynamics AX and a CSV source data format to manage configurations in all environments where you intend to export and import configurations.</span></span>

### <a name="create-an-ax-source-data-format"></a><span data-ttu-id="df532-120">AX ソース データ フォーマットを作成する</span><span class="sxs-lookup"><span data-stu-id="df532-120">Create an AX source data format</span></span>

<span data-ttu-id="df532-121">構成をエクスポートする環境で、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="df532-121">Complete the following procedure in the environment that you intend to export a configuration from.</span></span>

1.  <span data-ttu-id="df532-122">**データのインポート/エクスポート フレームワーク** &gt; **設定** &gt; **ソース データ形式**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="df532-122">Click **Data import export framework** &gt; **Setup** &gt; **Source data formats**.</span></span>
2.  <span data-ttu-id="df532-123">**新規**をクリックし、ソース AX の名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="df532-123">Click **New**, and name the source AX.</span></span>
3.  <span data-ttu-id="df532-124">タイプが **AX** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="df532-124">Verify that the type is **AX.**</span></span>
4.  <span data-ttu-id="df532-125">構成のインポート先の環境で、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="df532-125">Repeat this procedure in the environment that you intend to import the configuration to.</span></span>

### <a name="create-a-csv-source-data-format"></a><span data-ttu-id="df532-126">CSV ソース データ フォーマットを作成する</span><span class="sxs-lookup"><span data-stu-id="df532-126">Create a CSV source data format</span></span>

<span data-ttu-id="df532-127">構成をエクスポートする環境で、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="df532-127">Complete the following procedure in the environment that you intend to export a configuration from.</span></span>

1. <span data-ttu-id="df532-128">**データのインポート/エクスポート フレームワーク** &gt; **設定** &gt; **ソース データ形式**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="df532-128">Click **Data import export framework** &gt; **Setup** &gt; **Source data formats**.</span></span>
2. <span data-ttu-id="df532-129">**新規**をクリックし、ソース CSV の名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="df532-129">Click **New**, and name the source CSV.</span></span>
3. <span data-ttu-id="df532-130">タイプが **ファイル** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="df532-130">Verify that the type is **File**.</span></span>
4. <span data-ttu-id="df532-131">**一般**タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="df532-131">On the **General** tab, set the following values.</span></span>

   |                  <span data-ttu-id="df532-132">設定</span><span class="sxs-lookup"><span data-stu-id="df532-132">Setting</span></span>                  |     <span data-ttu-id="df532-133">先頭値</span><span class="sxs-lookup"><span data-stu-id="df532-133">Value</span></span>      |
   |-------------------------------------------|----------------|
   |       <span data-ttu-id="df532-134"><strong>ファイル形式</strong></span><span class="sxs-lookup"><span data-stu-id="df532-134"><strong>File format</strong></span></span>        |   <span data-ttu-id="df532-135">区切り</span><span class="sxs-lookup"><span data-stu-id="df532-135">Delimited</span></span>    |
   |     <span data-ttu-id="df532-136"><strong>先頭行のヘッダー</strong></span><span class="sxs-lookup"><span data-stu-id="df532-136"><strong>First row header</strong></span></span>     |    <span data-ttu-id="df532-137">選択済</span><span class="sxs-lookup"><span data-stu-id="df532-137">Selected</span></span>    |
   |      <span data-ttu-id="df532-138"><strong>行区切り</strong></span><span class="sxs-lookup"><span data-stu-id="df532-138"><strong>Row delimiter</strong></span></span>       |    <span data-ttu-id="df532-139">{CR}{LF}</span><span class="sxs-lookup"><span data-stu-id="df532-139">{CR}{LF}</span></span>    |
   |     <span data-ttu-id="df532-140"><strong>列区切り</strong></span><span class="sxs-lookup"><span data-stu-id="df532-140"><strong>Column delimiter</strong></span></span>     | <span data-ttu-id="df532-141">縦棒 {</span><span class="sxs-lookup"><span data-stu-id="df532-141">Vertical bar {</span></span> |
   |      <span data-ttu-id="df532-142"><strong>テキスト修飾子</strong></span><span class="sxs-lookup"><span data-stu-id="df532-142"><strong>Text qualifier</strong></span></span>      |       @@       |
   |         <span data-ttu-id="df532-143"><strong>行をスキップ</strong></span><span class="sxs-lookup"><span data-stu-id="df532-143"><strong>Skip row</strong></span></span>         |       <span data-ttu-id="df532-144">0</span><span class="sxs-lookup"><span data-stu-id="df532-144">0</span></span>        |
   |        <span data-ttu-id="df532-145"><strong>コード ページ</strong></span><span class="sxs-lookup"><span data-stu-id="df532-145"><strong>Code page</strong></span></span>         |      <span data-ttu-id="df532-146">1252</span><span class="sxs-lookup"><span data-stu-id="df532-146">1252</span></span>      |
   |     <span data-ttu-id="df532-147"><strong>言語ロケール</strong></span><span class="sxs-lookup"><span data-stu-id="df532-147"><strong>Language locale</strong></span></span>      |     <span data-ttu-id="df532-148">EN-US</span><span class="sxs-lookup"><span data-stu-id="df532-148">EN-US</span></span>      |
   | <span data-ttu-id="df532-149"><strong>複数値の区切り</strong></span><span class="sxs-lookup"><span data-stu-id="df532-149"><strong>Multiple value separator</strong></span></span> |       <span data-ttu-id="df532-150">;</span><span class="sxs-lookup"><span data-stu-id="df532-150">;</span></span>        |

   ![構成マネージャーの DIXF 設定](./media/dixfconfigurationmanager.png)
5. <span data-ttu-id="df532-152">構成のインポート先の環境で、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="df532-152">Repeat this procedure in the environment that you intend to import the configuration to.</span></span>

## <a name="install-and-configure-the-local-component-of-the-system-diagnostics-lifecycle-services"></a><span data-ttu-id="df532-153">システム診断 (Lifecycle Services) のローカル コンポーネントのインストールと構成</span><span class="sxs-lookup"><span data-stu-id="df532-153">Install and configure the local component of the System diagnostics (Lifecycle Services)</span></span>
<span data-ttu-id="df532-154">構成をエクスポートする環境で、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="df532-154">Complete the following procedure in the environment that you intend to export a configuration from.</span></span> 
> [!IMPORTANT]
> <span data-ttu-id="df532-155">プロジェクトおよび環境のシステム診断のローカル コンポーネントを既にインストールしている場合、**プログラムの追加と削除**を使用し、アンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="df532-155">If you have already installed the local component of the System diagnostics for your project and environment, you must uninstall it by using **Add/Remove programs**.</span></span> <span data-ttu-id="df532-156">検出されたインスタンスの数にかかわらず、環境ごとに 1 つのMicrosoft Dynamics AX Application Object Server (AOS) だけが、コンフィギュレーションの管理と共に使用されます。</span><span class="sxs-lookup"><span data-stu-id="df532-156">Only one instance of Microsoft Dynamics AX Application Object Server (AOS) per environment can be used with Configuration management, regardless of the number of instances that are discovered.</span></span>

1.  <span data-ttu-id="df532-157">システム診断のローカル コンポーネントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="df532-157">Install the local component of the System diagnostics.</span></span> <span data-ttu-id="df532-158">詳細については、[システム診断のインストールと実行 (Lifecycle Services)](./ax-2012/install-run-system-diagnostics-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df532-158">For details, see [Install and run System diagnostics (Lifecycle Services)](./ax-2012/install-run-system-diagnostics-lcs.md).</span></span> <span data-ttu-id="df532-159">重要: この beta リリースでは、システム診断のサービス アカウントを AX 2012 R3 の sysadmin ロールに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df532-159">Important: For this beta release, we require that you add the service account for the System diagnostics to the sysadmin role in AX 2012 R3.</span></span>
2.  <span data-ttu-id="df532-160">**開始** &gt; **Microsoft Dynamics AX Lifecycle Services 診断サービス検索**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="df532-160">Click **Start** &gt; **Microsoft Dynamics AX Lifecycle Services Diagnostic Service Discovery**.</span></span>
3.  <span data-ttu-id="df532-161">**環境の検出**ウィンドウに、環境の名前と Microsoft SQL Server のインスタンスとデータベースの完全修飾名を入力します。</span><span class="sxs-lookup"><span data-stu-id="df532-161">In the **Environment Discovery** window, enter a name for the environment, and the fully-qualified name of the Microsoft SQL Server instance and database.</span></span> <span data-ttu-id="df532-162">その後、[環境を検出] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="df532-162">Then click Discover environment.</span></span>
4.  <span data-ttu-id="df532-163">探索を完了した後、**コンフィギュレーション管理 (ベータ)** セクションに値を入力し、**保存**をクリックして、**アップロード環境**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="df532-163">After discovery is completed, enter the values in the **Configuration management (Beta)** section, click **Save**, and then click **Upload environment**.</span></span>
    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="df532-164">オプション</span><span class="sxs-lookup"><span data-stu-id="df532-164">Option</span></span></th>
    <th><span data-ttu-id="df532-165">先頭値</span><span class="sxs-lookup"><span data-stu-id="df532-165">Value</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="df532-166"><span class="ui">コンフィギュレーションの上書きを有効にする</span></span><span class="sxs-lookup"><span data-stu-id="df532-166"><span class="ui">Enable configuration overwrites</span></span></span></td>
    <td><span data-ttu-id="df532-167">指定した AOS インスタンスのコンフィギュレーションをコピーし、上書きできるようにするには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="df532-167">Select this option to enable configurations to be copied and overwritten for the specified AOS instance.</span></span>
    <div class="alert">
    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="df532-168"><strong>注意 </strong></span><span class="sxs-lookup"><span data-stu-id="df532-168"><strong>Caution</strong></span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="df532-169">環境を完全に構成したときは、構成の上書きを無効にすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="df532-169">We strongly recommend that you disable configuration overwrites when you have fully configured an environment.</span></span></td>
    </tr>
    </tbody>
    </table>
    </div></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="df532-170"><span class="ui">AOS インスタンス</span></span><span class="sxs-lookup"><span data-stu-id="df532-170"><span class="ui">AOS instance</span></span></span></td>
    <td><span data-ttu-id="df532-171">コピーまたは上書きが可能な AOS インスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="df532-171">Specify the AOS instance that can be copied from or overwritten.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="df532-172"><span class="ui">保存場所</span></span><span class="sxs-lookup"><span data-stu-id="df532-172"><span class="ui">Storage location</span></span></span></td>
    <td><span data-ttu-id="df532-173">構成のローカルの格納場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="df532-173">Specify the location where configurations are stored locally.</span></span> <span data-ttu-id="df532-174">AOS サービス アカウントとデータのインポート/エクスポート フレームワーク サービス アカウントには、この場所への書き込みアクセス権が必要です。</span><span class="sxs-lookup"><span data-stu-id="df532-174">The AOS service account and the Data Import/Export Framework service account must have read and write access to this location.</span></span>
    <div class="alert">
    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="df532-175"><strong>重要</strong></span><span class="sxs-lookup"><span data-stu-id="df532-175"><strong>Important</strong></span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="df532-176">データ インポート/エクスポート フレームワークに使用されている同じディレクトリを使用することを強くお勧めします。共有ディレクトリには、インポートおよびエクスポートする内容によっては、機密データが含まれていることがあるので注意してください。</span><span class="sxs-lookup"><span data-stu-id="df532-176">We strongly recommend that you use the same directory that is used for the Data Import/Export Framework.Be aware that the shared directory might contain sensitive data, depending on what you are importing and exporting.</span></span> <span data-ttu-id="df532-177">出来る限りの少数のユーザーが、AOS サービス アカウントおよびデータのインポート / エクスポート フレームワーク サービス アカウントに加えて、その場所にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="df532-177">Make sure that as few users as possible, in addition to the AOS service account and the Data Import/Export Framework service account, have access to the location.</span></span></td>
    </tr>
    </tbody>
    </table>
    </div></td>
    </tr>
    </tbody>
    </table>

    ![構成マネージャーのシステム診断の検出](./media/systemdiagnosticconfigurationmanagerdiscoverysettings.png)
5.  <span data-ttu-id="df532-179">構成のインポート先の環境で、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="df532-179">Repeat this procedure in the environment that you intend to import a configuration to.</span></span>

## <a name="next-steps"></a><span data-ttu-id="df532-180">次のステップ</span><span class="sxs-lookup"><span data-stu-id="df532-180">Next steps</span></span>
<span data-ttu-id="df532-181">この環境は、設定をコピーして管理するための準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="df532-181">The environment is now ready for you to copy and manage configurations.</span></span> <span data-ttu-id="df532-182">詳細については、[コンフィギュレーションのコピー (Lifecycle Services、LCS)](copy-configuration-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df532-182">For more information, see [Copy a configuration (Lifecycle Services, LCS)](copy-configuration-lcs.md).</span></span>



