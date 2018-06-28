---
title: "ハードウェア ステーションの概要および拡張機能"
description: "このトピックでは、新規デバイスと既存デバイスの新規デバイス タイプのサポートを追加するために、Hardware Station を拡張する方法について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 17971
ms.assetid: 256f7f2b-c419-442f-b195-0c6a299a056e
ms.search.region: Global
ms.author: sijoshi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2799af6d6d2e7afbbfbcbd639bd62c0818645805
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="hardware-station-overview-and-extensibility"></a><span data-ttu-id="b1444-103">ハードウェア ステーションの概要および拡張機能</span><span class="sxs-lookup"><span data-stu-id="b1444-103">Hardware Station overview and extensibility</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1444-104">このトピックでは、新規デバイスと既存デバイスの新規デバイス タイプのサポートを追加するために、Hardware Station を拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b1444-104">This topic explains how to extend Hardware Station to add support for new devices and new device types for existing devices.</span></span>

<a name="retail-hardware-station-overview"></a><span data-ttu-id="b1444-105">Retail Hardware Station の概要</span><span class="sxs-lookup"><span data-stu-id="b1444-105">Retail Hardware Station overview</span></span>
--------------------------------

<span data-ttu-id="b1444-106">Retail Hardware Station は、プリンター、キャッシュ ドロワー、スキャナー、および支払ターミナルなどの小売ハードウェア周辺機器に接続するために Retai Modern POS および Cloud POS で使用されます。</span><span class="sxs-lookup"><span data-stu-id="b1444-106">Retail Hardware Station is used by Retail Modern POS and Cloud POS to connect to retail hardware peripherals such as printers, cash drawers, scanners, and payment terminals.</span></span> 

<span data-ttu-id="b1444-107">[![HWS-Local-Traditional](./media/hws-local-300x236.png)](./media/hws-local.png)</span><span class="sxs-lookup"><span data-stu-id="b1444-107">[![HWS-Local-Traditional](./media/hws-local-300x236.png)](./media/hws-local.png)</span></span>

<span data-ttu-id="b1444-108">[![HWS-Shared](./media/hws-shared-300x224.png)](./media/hws-shared.png)</span><span class="sxs-lookup"><span data-stu-id="b1444-108">[![HWS-Shared](./media/hws-shared-300x224.png)](./media/hws-shared.png)</span></span>

## <a name="retail-hardware-station-setup"></a><span data-ttu-id="b1444-109">Retail Hardware Station の設定</span><span class="sxs-lookup"><span data-stu-id="b1444-109">Retail Hardware Station setup</span></span>
<span data-ttu-id="b1444-110">開始する前に、[Retail ハードウェア ステーションのコンフィギュレーションとインストール](../retail-hardware-station-configuration-installation.md)の情報を使用してハードウェア ステーションをインストールし、ハードウェアがどのようなものでインストールがどのようにされているかを知ることができます。</span><span class="sxs-lookup"><span data-stu-id="b1444-110">Before you start, use the information in [Retail hardware station configuration and installation](../retail-hardware-station-configuration-installation.md) to install Hardware Station, and to get a feel of what hardware is and how it's installed.</span></span>

## <a name="retail-hardware-station-architecture"></a><span data-ttu-id="b1444-111">Retail Hardware Station アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="b1444-111">Retail Hardware Station architecture</span></span>
<span data-ttu-id="b1444-112">ハードウェア ステーションは、ハードウェア ステーション アプリケーション プログラミング インターフェイス (API) 用の Web API を公開します。</span><span class="sxs-lookup"><span data-stu-id="b1444-112">Hardware Station exposes Web API for Hardware Station application programming interfaces (APIs).</span></span> <span data-ttu-id="b1444-113">新しいデバイス (たとえば、現金自動支払機) の新しいコントローラーを実装するか、または既存のデバイス タイプ (たとえば、新しいオーディオ ジャック磁気ストライプ リーダー (MSR) の実装) の既存のコント ローラーを上書きするかのいずれかによって、ハードウェア ステーションを拡張できます。</span><span class="sxs-lookup"><span data-stu-id="b1444-113">Hardware Station can be extended either by implementing a new controller for a new device (for example, a cash dispenser) or by overriding an existing controller for an existing device type (for example, a new Audio Jack magnetic stripe reader (MSR) implementation).</span></span>

<span data-ttu-id="b1444-114">[![ハードウェア ステーション アーキテクチャ](./media/hardware-station-architecture-1024x764.png)](./media/hardware-station-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="b1444-114">[![Hardware Station Architecture](./media/hardware-station-architecture-1024x764.png)](./media/hardware-station-architecture.png)</span></span>

## <a name="retail-hardware-station-extensibility-scenarios"></a><span data-ttu-id="b1444-115">Retail Hardware Station 拡張性シナリオ</span><span class="sxs-lookup"><span data-stu-id="b1444-115">Retail Hardware Station extensibility scenarios</span></span>
<span data-ttu-id="b1444-116">.NTE にサポートされている [Managed Extensibility Framework (MEF)](https://msdn.microsoft.com/en-us/library/dd460648(v=vs.110).aspx) を使用して、ハードウェア ステーションの拡張性が獲得されます。</span><span class="sxs-lookup"><span data-stu-id="b1444-116">Extensibility in Hardware Station is achieved by using [Managed Extensibility Framework (MEF)](https://msdn.microsoft.com/en-us/library/dd460648(v=vs.110).aspx), which is supported by .NET.</span></span> <span data-ttu-id="b1444-117">**拡張性の規定:** 拡張機能アセンブリで、常に、拡張機能の書き込みをします。</span><span class="sxs-lookup"><span data-stu-id="b1444-117">**Extensibility guideline:** Always write your extension in your own extension assembly.</span></span> <span data-ttu-id="b1444-118">そのようにして、実際の拡張機能を記述し、アップグレードがかなり簡単になります。</span><span class="sxs-lookup"><span data-stu-id="b1444-118">That way, you're writing a true extension, and upgrades will be much easier.</span></span> <span data-ttu-id="b1444-119">拡張のための 2 つの基本的なシナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="b1444-119">There are two basic scenarios for extension:</span></span>

-   <span data-ttu-id="b1444-120">**新しいデバイスを追加する** - 最初から用意されているハードウェア ステーションはデバイス (現金自動支払機など) をまだサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="b1444-120">**Adding a new device** – The out-of-box Hardware Station doesn't already support the device (for example, a cash dispenser).</span></span> <span data-ttu-id="b1444-121">したがって、ハードウェア ステーションで新しいデバイスのサポートを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1444-121">Therefore, you must add support for the new device in Hardware Station.</span></span>
-   <span data-ttu-id="b1444-122">**既存のデバイスに対する新しいデバイス タイプを追加する** - 最初から用意されているハードウェア ステーションの実装ではすでにデバイス (MSR など) がサポートされていますが、特定のデバイス タイプ (オーディオ ジャック MSR 実装) のサポートを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1444-122">**Adding a new device type for an existing device** – The out-of-box Hardware Station implementation already supports the device (for example, an MSR), but you must add support for a specific device type (for example, an Audio Jack MSR implementation).</span></span>

### <a name="scenario-1-adding-a-new-device"></a><span data-ttu-id="b1444-123">シナリオ 1: 新しいデバイスを追加する</span><span class="sxs-lookup"><span data-stu-id="b1444-123">Scenario 1: Adding a new device</span></span>

<span data-ttu-id="b1444-124">このシナリオでは、ハードウェア ステーションで、現金自動支払機装置のサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="b1444-124">For this scenario, we will add support for a cash dispenser device in Hardware Station.</span></span> <span data-ttu-id="b1444-125">ここでは、メモ帳ファイルで現金を分配する疑似現金自動支払機を作成します。</span><span class="sxs-lookup"><span data-stu-id="b1444-125">In our example, we will create a fake cash dispenser that dispenses cash in the Notepad file.</span></span> <span data-ttu-id="b1444-126">ただし、この例はハードウェア ステーションのエンド ツー エンドの拡張機能を理解するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b1444-126">However, this example will help you understand the end-to-end extensibility of Hardware Station.</span></span>

-   <span data-ttu-id="b1444-127">Retail ソフトウェア開発キット (SDK) には、現金自動支払機のサンプルがあります。</span><span class="sxs-lookup"><span data-stu-id="b1444-127">The Retail software development kit (SDK) has a cash dispenser sample.</span></span> <span data-ttu-id="b1444-128">RetailSdk\\SampleExtensions\\HardwareStation を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b1444-128">See RetailSdk\\SampleExtensions\\HardwareStation.</span></span>
-   <span data-ttu-id="b1444-129">この場合、新しい Web API コントローラーおよびヘルパー プロパティ/メソッドを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1444-129">In this case, we must add a new Web API controller and helper properties/methods.</span></span>
-   <span data-ttu-id="b1444-130">新しい **CashDispenser** コントローラーは、**ApiController** と **IHardwareStationController** を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1444-130">The new **CashDispenser** controller must extend **ApiController** and **IHardwareStationController**.</span></span>
-   <span data-ttu-id="b1444-131">ここの **エクスポート** 属性文字列は、このコントローラーが使用されるデバイスを指定します: \[Export("CASHDISPENSER", typeof(IHardwareStationController))\]</span><span class="sxs-lookup"><span data-stu-id="b1444-131">The **Export** attribute string here specifies the device that this controller is used for: \[Export("CASHDISPENSER", typeof(IHardwareStationController))\]</span></span>

<!-- -->

    namespace Contoso
    {
        namespace Commerce.HardwareStation.CashDispenserSample
        {
            using System;
            using System.Composition;
            using System.Web.Http;
            using Microsoft.Dynamics.Commerce.HardwareStation;
            using Microsoft.Dynamics.Retail.Diagnostics;
            /// <summary>
            /// Cash dispenser web API controller class.
            /// </summary>
            [Export("CASHDISPENSER", typeof(IHardwareStationController))]
            public class CashDispenserController : ApiController, IHardwareStationController
            { 
                // Add your controller code here
            }

### <a name="scenario-2-adding-a-new-device-type-for-an-existing-device"></a><span data-ttu-id="b1444-132">シナリオ 2: 既存のデバイスの新しいデバイス タイプを追加する</span><span class="sxs-lookup"><span data-stu-id="b1444-132">Scenario 2: Adding a new device type for an existing device</span></span>

<span data-ttu-id="b1444-133">このシナリオでは、既存のデバイス (オーディオ ジャック MSR 実装) に対する新しいデバイス タイプのサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="b1444-133">For this scenario, we will add support for a new device type for an existing device (an Audio Jack MSR implementation).</span></span>

-   <span data-ttu-id="b1444-134">**エクスポート** 属性文字列は、このコントローラーが使用されるデバイスを指定します: \[Export("MSR", typeof(IHardwareStationController))\]</span><span class="sxs-lookup"><span data-stu-id="b1444-134">The **Export** attribute string specifies the device that this controller is used for: \[Export("MSR", typeof(IHardwareStationController))\]</span></span>
-   <span data-ttu-id="b1444-135">MSR に対して複数のコントローラーが存在するため、ハードウェア ステーションは構成ファイルを使用して実行時にどの実装を使用するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b1444-135">Because there will be multiple controllers for MSRs, Hardware Station uses the configuration file to determine which implementation to use at run time.</span></span> <span data-ttu-id="b1444-136">詳細については、この記事の後半の「Retail ハードウェア ステーションの拡張機能コンフィギュレーション」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b1444-136">For more information, see the "Retail Hardware Station extensibility configuration" section later in this article.</span></span>

<!-- -->

    namespace Contoso
    {
        namespace Commerce.HardwareStation.RamblerService
        {
            using System;
            using System.Composition;
            using System.Threading.Tasks;
            using System.Web.Http;
            using System.Web.Http.Controllers;
            using Microsoft.Dynamics.Commerce.HardwareStation;
            using Microsoft.Dynamics.Commerce.HardwareStation.DataEntity;
            using Microsoft.Dynamics.Commerce.HardwareStation.Models;
            using Microsoft.Dynamics.Retail.Diagnostics;
            /// <summary>
            /// MSR device web API controller class.
            /// </summary>
            [Export("MSR", typeof(IHardwareStationController))]
            [Authorize]
            public class AudioJackMSRController : ApiController, IHardwareStationController
            {
                // Add controller implementation here
            }

## <a name="retail-hardware-station-extensibility-configuration"></a><span data-ttu-id="b1444-137">Retail Hardware Station 拡張性コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b1444-137">Retail Hardware Station extensibility configuration</span></span>
### <a name="configuration-for-iis-hosted-hardware-station"></a><span data-ttu-id="b1444-138">IIS でホストされているハードウェア ステーションのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b1444-138">Configuration for IIS-hosted Hardware Station</span></span>

<span data-ttu-id="b1444-139">ハードウェア ステーションが拡張機能を使用する前に、拡張機能のエントリが含まれるようにハードウェア ステーション Web.config ファイルの**合成**セクションを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1444-139">Before Hardware Station can consume your extension, the **composition** section in the Hardware Station Web.config file must be updated so that it includes an entry for your extension.</span></span> <span data-ttu-id="b1444-140">コンフィギュレーション ファイルの構成ターゲットの順序によって優先順位が決まります。</span><span class="sxs-lookup"><span data-stu-id="b1444-140">The order of the composition targets in the configuration file determines precedence.</span></span> 

<span data-ttu-id="b1444-141">[![ハードウェア ステーション Web コンフィギュレーション](./media/hws-webconfig.png)](./media/hws-webconfig.png)</span><span class="sxs-lookup"><span data-stu-id="b1444-141">[![Hardware Station Web Config](./media/hws-webconfig.png)](./media/hws-webconfig.png)</span></span>

### <a name="configuration-for-local-ipc-based-hardware-station"></a><span data-ttu-id="b1444-142">ローカル IPC ベースのハードウェア ステーションのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b1444-142">Configuration for local IPC-based Hardware Station</span></span>

<span data-ttu-id="b1444-143">ローカルのハードウェア ステーションが拡張機能を使用する前に、拡張機能用のエントリが含まれるように Modern POS DllHost.exe.config ファイル (C:\\Program Files (x86)\\Microsoft Dynamics AX\\70\\Retail Modern POS\\ClientBroker) の**合成**セクションを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1444-143">Before local Hardware Station can consume your extension, the **composition** section in the Modern POS DLLHost.exe.config file (C:\\Program Files (x86)\\Microsoft Dynamics AX\\70\\Retail Modern POS\\ClientBroker) must be updated so that it includes an entry for your extension.</span></span> <span data-ttu-id="b1444-144">コンフィギュレーション ファイルの構成ターゲットの順序によって優先順位が決まります。</span><span class="sxs-lookup"><span data-stu-id="b1444-144">The order of the composition targets in the configuration file determines precedence.</span></span>

<span data-ttu-id="b1444-145">[</span><span class="sxs-lookup"><span data-stu-id="b1444-145">[</span></span>![ローカル ハードウェア ステーションのコンフィギュレーション](./media/hws-dll-host-local-config.png)




