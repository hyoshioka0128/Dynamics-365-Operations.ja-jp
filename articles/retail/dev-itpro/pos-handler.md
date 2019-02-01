---
title: "POS 要求ハンドラーのオーバーライド"
description: "このトピックでは、RetailTransactionServiceEx クラスに拡張メソッドを追加して、Commerce Data Exchange - リアルタイム サービスを拡張する方法について説明します。 リアルタイム サービスは、Retail クライアントがリアルタイムで小売機能を操作できるようします。"
author: mugunthanm
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 68673
ms.assetid: 72a63836-2908-45fa-b1a6-3b1c499a19a2
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 209/07/2018
ms.dyn365.ops.version: AX 7.3.5
ms.translationtype: HT
ms.sourcegitcommit: 48e2eea2cc986edc49d5192945c3d913c3bb9756
ms.openlocfilehash: c7f173f7d30809d12c528fd7b68cd9175954a845
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---

# <a name="override-pos-request-handler"></a><span data-ttu-id="19a00-104">POS 要求ハンドラーのオーバーライド</span><span class="sxs-lookup"><span data-stu-id="19a00-104">Override POS request handler</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19a00-105">このトピックでは、POS 要求ハンドラーをオーバーライドする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="19a00-105">This topic explains how to override POS request handler.</span></span> <span data-ttu-id="19a00-106">POS ビジネス ロジックをオーバーライドするための拡張パターンを導入しました。</span><span class="sxs-lookup"><span data-stu-id="19a00-106">We've introduced an extension pattern for overriding the POS business logic.</span></span> <span data-ttu-id="19a00-107">コア POS ビジネス フローにビジネス ロジックを変更/追加するシナリオがある場合、このパターンに従うことができます。</span><span class="sxs-lookup"><span data-stu-id="19a00-107">If you have a scenario where you want to modify/add some business logic to the core POS business flow, then you can follow this pattern.</span></span>

<span data-ttu-id="19a00-108">たとえば、シリアル品目を販売する場合、スキャン後、POS にはその品目のシリアル番号を入力するダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-108">For example, when you sell a serial item, POS will display a dialog box where you can enter the serial number for that item after the scan.</span></span> <span data-ttu-id="19a00-109">コードを使用してシリアル番号を入力することでシリアル番号プロセスを自動化する場合、このシリアル番号要求ハンドラーをオーバーライドしてカスタム ビジネス ロジックを使用できます。</span><span class="sxs-lookup"><span data-stu-id="19a00-109">If you want to automate the serial number process by entering the serial number through code, then you can override this serial number request handler and use custom business logic.</span></span> <span data-ttu-id="19a00-110">POS のビジネス ロジックのほとんどは、要求ハンドラーで実装されます。ただし、関連する要求ハンドラーをオーバーライドして、ビジネス フローに従って応答を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="19a00-110">Most of the business logic in POS is implemented in request handler, however, you can override the relevant request handler and return the response according to your business flow.</span></span>

> [!NOTE]
> <span data-ttu-id="19a00-111">すべての要求ハンドラー ロジックがカスタマイズ用に公開されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="19a00-111">Not all request handler logic is exposed for customization.</span></span> <span data-ttu-id="19a00-112">ビジネス ロジックをカスタマイズする場合で、その要求ハンドラーがオーバーライド可能でない場合、サポート チケットを作成するか、LCS 機能拡張ツールでリクエストを登録します。</span><span class="sxs-lookup"><span data-stu-id="19a00-112">If you want to customize any business logic and if that request handler is not overridable, then create a support ticket or log a request in the LCS extensibility tool.</span></span>

<span data-ttu-id="19a00-113">**オーバーライドするために公開される POS 要求ハンドラー ロジック**</span><span class="sxs-lookup"><span data-stu-id="19a00-113">\*\* POS request handler logic exposed for overriding \*\*</span></span>

<span data-ttu-id="19a00-114">これは、[Microsoft Dynamics 365 for Finance and Operations - バージョン 7.3.5](https://fix.lcs.dynamics.com/Issue/Details?kb=4456209&bugId=235124&qc=9fef9e411bd4f715508205b6c65b16afdc4096cea0f15e1535c3d8e3f13716c1) をベースとしています。</span><span class="sxs-lookup"><span data-stu-id="19a00-114">This is list is based on [Microsoft Dynamics 365 for Finance and Operations - Version 7.3.5.](https://fix.lcs.dynamics.com/Issue/Details?kb=4456209&bugId=235124&qc=9fef9e411bd4f715508205b6c65b16afdc4096cea0f15e1535c3d8e3f13716c1)</span></span> <span data-ttu-id="19a00-115">毎月の更新プログラムのたびに、拡張ポイントが追加されるため、完全な一覧については Retail SDK で Pos.api.d.ts ファイルをチェックしてください。</span><span class="sxs-lookup"><span data-stu-id="19a00-115">In each monthly update we will be adding additional extension points, so check the Pos.api.d.ts file in the Retail SDK for the full list.</span></span> 

<span data-ttu-id="19a00-116">**買い物カゴ拡張ハンドラー**</span><span class="sxs-lookup"><span data-stu-id="19a00-116">**Cart extension handlers**</span></span>

| <span data-ttu-id="19a00-117">**要求名**</span><span class="sxs-lookup"><span data-stu-id="19a00-117">**Request name**</span></span>                           | <span data-ttu-id="19a00-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="19a00-118">**Description**</span></span>                                                                              |
|--------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="19a00-119">AddTenderLineToCartClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-119">AddTenderLineToCartClientRequestHandler</span></span>    | <span data-ttu-id="19a00-120">このハンドラーは、カートに支払/入金方法 (支払) 明細行を追加するときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-120">This handler is executed when you add tender (payment) line to cart.</span></span>                          |
| <span data-ttu-id="19a00-121">GetKeyedInPriceClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-121">GetKeyedInPriceClientRequestHandler</span></span>        | <span data-ttu-id="19a00-122">このハンドラーは、販売時に、価格内にコンフィギュレーション キーを持つ品目を追加するときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-122">This handler is executed when you add an item that has a configuration key in price during sale.</span></span> |
| <span data-ttu-id="19a00-123">GetPickupDateClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-123">GetPickupDateClientRequestHandler</span></span>          | <span data-ttu-id="19a00-124">顧客注文時に集荷日を選択するときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-124">Executed when you select a pickup date during a customer order.</span></span>                                  |
| <span data-ttu-id="19a00-125">GetShippingDateClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-125">GetShippingDateClientRequestHandler</span></span>        | <span data-ttu-id="19a00-126">顧客注文時に出荷日を選択するときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-126">Executed when you select a shipping date during a customer order.</span></span>                                |
| <span data-ttu-id="19a00-127">ShowChangeDueClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-127">ShowChangeDueClientRequestHandler</span></span>          | <span data-ttu-id="19a00-128">トランザクションの終了時に期日の変更ダイアログ ボックスが表示されるときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-128">Executed when the change due dialog box is shown at the end of transaction.</span></span>                             |
| <span data-ttu-id="19a00-129">GetReceiptEmailAddressClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-129">GetReceiptEmailAddressClientRequestHandler</span></span> | <span data-ttu-id="19a00-130">受信者のメール アドレスを取得するときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-130">Executed when you get a receipt email address.</span></span>                                                 |
| <span data-ttu-id="19a00-131">DepositOverrideOperationRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-131">DepositOverrideOperationRequestHandler</span></span>     | <span data-ttu-id="19a00-132">預金をオーバーライドするときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-132">Executed when you override a deposit.</span></span>                                                          |
| <span data-ttu-id="19a00-133">GetShippingChargeClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-133">GetShippingChargeClientRequestHandler</span></span>      | <span data-ttu-id="19a00-134">顧客注文フロー中に開始された出荷費用ワークフローを取得するときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-134">Executed when get shipping charge workflow initiated during customer order flow.</span></span>                                                             |

<span data-ttu-id="19a00-135">**支払拡張機能ハンドラー**</span><span class="sxs-lookup"><span data-stu-id="19a00-135">**Payment extension handler:**</span></span>

| <span data-ttu-id="19a00-136">**要求名**</span><span class="sxs-lookup"><span data-stu-id="19a00-136">**Request name**</span></span>                                 | <span data-ttu-id="19a00-137">**説明**</span><span class="sxs-lookup"><span data-stu-id="19a00-137">**Description**</span></span>                                                                                                                                   |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19a00-138">GetGiftCardByIdServiceRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-138">GetGiftCardByIdServiceRequestHandler</span></span>             | <span data-ttu-id="19a00-139">このハンドラーは、ギフト カード ID を受け取ると実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-139">This handler is executed when you receive the gift card ID.</span></span>                                                                                           |
| <span data-ttu-id="19a00-140">GetPaymentCardTypeByBinRangeClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-140">GetPaymentCardTypeByBinRangeClientRequestHandler</span></span> | <span data-ttu-id="19a00-141">このハンドラーは、Visa や Master Card などのカード タイプを POS が取得するときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-141">This handler is executed when POS gets the card type, such as Visa or Master Card.</span></span> <span data-ttu-id="19a00-142">これは、カード支払/入金の明細行の処理中の HQ コンフィギュレーションに基づきます。</span><span class="sxs-lookup"><span data-stu-id="19a00-142">This is based on the HQ configuration during the card tender line processing.</span></span> |

<span data-ttu-id="19a00-143">**周辺機器要求ハンドラー**</span><span class="sxs-lookup"><span data-stu-id="19a00-143">**Peripherals request handler**</span></span>

| <span data-ttu-id="19a00-144">要求名</span><span class="sxs-lookup"><span data-stu-id="19a00-144">Request name</span></span>                                                  | <span data-ttu-id="19a00-145">説明</span><span class="sxs-lookup"><span data-stu-id="19a00-145">Description</span></span>                                                                                                                                                     |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19a00-146">CardPaymentAuthorizePaymentRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-146">CardPaymentAuthorizePaymentRequestHandler</span></span>                     | <span data-ttu-id="19a00-147">カード支払が承認されたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-147">Executed when a card payment is authorized.</span></span>                                                                                                                       |
| <span data-ttu-id="19a00-148">CardPaymentCapturePaymentRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-148">CardPaymentCapturePaymentRequestHandler</span></span>                       | <span data-ttu-id="19a00-149">カード支払が取得されたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-149">Executed when a card payment is captured.</span></span>                                                                                                                         |
| <span data-ttu-id="19a00-150">CardPaymentExecuteTaskRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-150">CardPaymentExecuteTaskRequestHandler</span></span>                          | <span data-ttu-id="19a00-151">カスタム タスクを実行するために使用します。</span><span class="sxs-lookup"><span data-stu-id="19a00-151">Used to execute any custom task.</span></span> <span data-ttu-id="19a00-152">このハンドラーは、主に、サポートされていない支払コネクタを使用するカスタム機能の拡張機能用です。</span><span class="sxs-lookup"><span data-stu-id="19a00-152">This handler is mainly for extensions for custom functionality with payment connector, which is not supported.</span></span>       |
| <span data-ttu-id="19a00-153">CardPaymentRefundPaymentRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-153">CardPaymentRefundPaymentRequestHandler</span></span>                        | <span data-ttu-id="19a00-154">カード支払が払戻しされたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-154">Executed when a card payment is refunded.</span></span>                                                                                                                         |
| <span data-ttu-id="19a00-155">CardPaymentVoidPaymentRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-155">CardPaymentVoidPaymentRequestHandler</span></span>                          | <span data-ttu-id="19a00-156">カード支払が無効化されたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-156">Executed when a card payment is voided.</span></span>                                                                                                                           |
| <span data-ttu-id="19a00-157">CardPaymentBeginTransactionRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-157">CardPaymentBeginTransactionRequestHandler</span></span>                     | <span data-ttu-id="19a00-158">カード支払が開始されたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-158">Executed when a card payment is initiated.</span></span>                                                                                                                        |
| <span data-ttu-id="19a00-159">CardPaymentEndTransactionRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-159">CardPaymentEndTransactionRequestHandler</span></span>                       | <span data-ttu-id="19a00-160">カード支払が終了したときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-160">Executed when a card payment is ended.</span></span>                                                                                                                            |
| <span data-ttu-id="19a00-161">CardPaymentEnquireGiftCardBalancePeripheralRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-161">CardPaymentEnquireGiftCardBalancePeripheralRequestHandler</span></span>     | <span data-ttu-id="19a00-162">ギフト カードの残高照会が行われるときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-162">Executed when a gift card balance inquiry is made.</span></span>                                                                                                                |
| <span data-ttu-id="19a00-163">PaymentTerminalAuthorizePaymentActivityRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-163">PaymentTerminalAuthorizePaymentActivityRequestHandler</span></span>         | <span data-ttu-id="19a00-164">支払ターミナル/デバイスを使用してカード支払が承認されたときに実行</span><span class="sxs-lookup"><span data-stu-id="19a00-164">Executed when a card payment is authorized using a payment.</span></span> <span data-ttu-id="19a00-165">されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-165">terminal/device.</span></span>                                                                                         |
| <span data-ttu-id="19a00-166">PaymentTerminalAuthorizePaymentRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-166">PaymentTerminalAuthorizePaymentRequestHandler</span></span>                 | <span data-ttu-id="19a00-167">支払ターミナル/デバイスを使用してカード支払が承認されたときに実行</span><span class="sxs-lookup"><span data-stu-id="19a00-167">Executed when a card payment is authorized using a payment.</span></span> <span data-ttu-id="19a00-168">されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-168">terminal/device.</span></span>                                                                                         |
| <span data-ttu-id="19a00-169">PaymentTerminalEnquireGiftCardBalancePeripheralRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-169">PaymentTerminalEnquireGiftCardBalancePeripheralRequestHandler</span></span> | <span data-ttu-id="19a00-170">支払ターミナル/デバイスを使用してギフト カードの残高照会が行われるときに実行</span><span class="sxs-lookup"><span data-stu-id="19a00-170">Executed when a gift card balance inquiry is made using a payment.</span></span> <span data-ttu-id="19a00-171">されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-171">terminal/device.</span></span>                                                                                  |
| <span data-ttu-id="19a00-172">PaymentTerminalExecuteTaskRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-172">PaymentTerminalExecuteTaskRequestHandler</span></span>                      | <span data-ttu-id="19a00-173">カスタム タスクを実行するために使用します。</span><span class="sxs-lookup"><span data-stu-id="19a00-173">Used to execute any custom task.</span></span> <span data-ttu-id="19a00-174">このハンドラーは、主に、サポートされていない支払ターミナル/デバイスを使用するカスタム機能の拡張機能用です。</span><span class="sxs-lookup"><span data-stu-id="19a00-174">This handler is mainly for extensions for custom functionality with payment terminal/device, which is not supported.</span></span> |
| <span data-ttu-id="19a00-175">PaymentTerminalRefundPaymentRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-175">PaymentTerminalRefundPaymentRequestHandler</span></span>                    | <span data-ttu-id="19a00-176">支払ターミナル/デバイスを使用してカード支払が払戻しされたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-176">Executed when a card payment is refunded using a payment terminal/device.</span></span>                                                                                           |
| <span data-ttu-id="19a00-177">PaymentTerminalUpdateLinesRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-177">PaymentTerminalUpdateLinesRequestHandler</span></span>                      | <span data-ttu-id="19a00-178">POS が表示目的で明細行品目の詳細を支払デバイスに送信するときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-178">Executed when POS sends line item details to a payment device for display purposes.</span></span>                                                                                 |
| <span data-ttu-id="19a00-179">PaymentTerminalVoidPaymentRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-179">PaymentTerminalVoidPaymentRequestHandler</span></span>                      | <span data-ttu-id="19a00-180">支払ターミナル/デバイスを使用してカード支払が無効化されたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-180">Executed when a card payment is voided using a payment terminal/device.</span></span>                                                                                             |
| <span data-ttu-id="19a00-181">PaymentTerminalBeginTransactionRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-181">PaymentTerminalBeginTransactionRequestHandler</span></span>                 | <span data-ttu-id="19a00-182">支払ターミナル/デバイスを使用してカード支払が開始されたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-182">Executed when a card payment is initiated using a payment terminal/device.</span></span>                                                                                          |
| <span data-ttu-id="19a00-183">PaymentTerminalCancelOperationRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-183">PaymentTerminalCancelOperationRequestHandler</span></span>                  | <span data-ttu-id="19a00-184">支払ターミナル/デバイスを使用してカード支払がキャンセルされたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-184">Executed when a card payment is cancelled using a payment terminal/device.</span></span>                                                                                          |
| <span data-ttu-id="19a00-185">PaymentTerminalEndTransactionRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-185">PaymentTerminalEndTransactionRequestHandler</span></span>                   | <span data-ttu-id="19a00-186">支払ターミナル/デバイスを使用してカード支払が終了したときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-186">Executed when a card payment is ended using a payment terminal/device.</span></span>                                                                                              |
| <span data-ttu-id="19a00-187">CashDrawerOpenRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-187">CashDrawerOpenRequestHandler</span></span>                                  | <span data-ttu-id="19a00-188">キャッシュ ドロワー オープン要求が POS によって開始されるときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-188">Executed when a cash drawer open request is initiated by POS.</span></span>                                                                                                     |
| <span data-ttu-id="19a00-189">PaymentTerminalActivateGiftCardPeripheralRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-189">PaymentTerminalActivateGiftCardPeripheralRequestHandler</span></span>       | <span data-ttu-id="19a00-190">POS により開始されたギフト カード要求をアクティブにしたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-190">Executed when activate gift card request is initiated by POS.</span></span>                                                                                                     |
| <span data-ttu-id="19a00-191">PaymentTerminalAddBalanceToGiftCardPeripheralRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-191">PaymentTerminalAddBalanceToGiftCardPeripheralRequestHandler</span></span>   | <span data-ttu-id="19a00-192">POS により開始されたギフト カード要求に残高を追加したときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-192">Executed when add balance to gift card request is initiated by POS.</span></span>                                                                                                     |
 
 

<span data-ttu-id="19a00-193">**スキャン要求ハンドラー**</span><span class="sxs-lookup"><span data-stu-id="19a00-193">**Scan request handler**</span></span>

| <span data-ttu-id="19a00-194">要求名</span><span class="sxs-lookup"><span data-stu-id="19a00-194">Request name</span></span>                      | <span data-ttu-id="19a00-195">説明</span><span class="sxs-lookup"><span data-stu-id="19a00-195">Description</span></span>                                                    |
|-----------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="19a00-196">GetScanResultClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-196">GetScanResultClientRequestHandler</span></span> | <span data-ttu-id="19a00-197">スキャンするか、POS トランザクション画面テンキーで入力するときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-197">Executed when you scan or key in a POS transaction screen Numpad.</span></span> |

<span data-ttu-id="19a00-198">**店舗フルフィルメント要求ハンドラー**</span><span class="sxs-lookup"><span data-stu-id="19a00-198">**Store fulfillment request handler**</span></span>

| <span data-ttu-id="19a00-199">要求名</span><span class="sxs-lookup"><span data-stu-id="19a00-199">Request name</span></span>                         | <span data-ttu-id="19a00-200">説明</span><span class="sxs-lookup"><span data-stu-id="19a00-200">Description</span></span>                                                          |
|--------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="19a00-201">PrintPackingSlipClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-201">PrintPackingSlipClientRequestHandler</span></span> | <span data-ttu-id="19a00-202">店舗フルフィルメント ビューから梱包明細を印刷するときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-202">Executed when you print a packing slip from the store fulfillment view.</span></span> |
| <span data-ttu-id="19a00-203">MarkAsPickedServiceRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-203">MarkAsPickedServiceRequestHandler</span></span>    | <span data-ttu-id="19a00-204">店舗フルフィルメント ビューからピッキングされた販売注文明細行をマークするときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-204">Executed when you mark a sales line as picked from the store fulfillment view.</span></span> |


<span data-ttu-id="19a00-205">**店舗運営要求ハンドラー**</span><span class="sxs-lookup"><span data-stu-id="19a00-205">**Store operations request handler**</span></span>

| <span data-ttu-id="19a00-206">要求名</span><span class="sxs-lookup"><span data-stu-id="19a00-206">Request name</span></span>                                       | <span data-ttu-id="19a00-207">説明</span><span class="sxs-lookup"><span data-stu-id="19a00-207">Description</span></span>                                                        |
|----------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="19a00-208">CreateTenderRemovalTransactionClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-208">CreateTenderRemovalTransactionClientRequestHandler</span></span> | <span data-ttu-id="19a00-209">POS で支払/入金の削除操作を行うときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-209">Executed when you do a tender removal operation in POS.</span></span>              |
| <span data-ttu-id="19a00-210">CreateFloatEntryTransactionClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-210">CreateFloatEntryTransactionClientRequestHandler</span></span>    | <span data-ttu-id="19a00-211">POS で釣銭入力操作を行うときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-211">Executed when you do a float entry operation in POS.</span></span>                 |
| <span data-ttu-id="19a00-212">SelectZipCodeInfoClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-212">SelectZipCodeInfoClientRequestHandler</span></span>              | <span data-ttu-id="19a00-213">POS で住所の追加/編集ビューで郵便番号を入力するときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-213">Executed when you key in zip code in address add/edit view in POS.</span></span> |
| <span data-ttu-id="19a00-214">CreateStartingAmountTransactionClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-214">CreateStartingAmountTransactionClientRequestHandler</span></span> | <span data-ttu-id="19a00-215">POS で開始金額申告を行うときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-215">Executed when you do a start amount declaration in POS.</span></span> |
| <span data-ttu-id="19a00-216">LoyaltyCardPointsBalanceOperationRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-216">LoyaltyCardPointsBalanceOperationRequestHandler</span></span>     | <span data-ttu-id="19a00-217">POS でロイヤルティ カード残高操作を行うときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-217">Executed when you do a loyalty card balance operation in POS.</span></span> | 


<span data-ttu-id="19a00-218">**支払/入金計算要求ハンドラー**</span><span class="sxs-lookup"><span data-stu-id="19a00-218">**Tender counting request handler**</span></span>

| <span data-ttu-id="19a00-219">要求名</span><span class="sxs-lookup"><span data-stu-id="19a00-219">Request name</span></span>                                           | <span data-ttu-id="19a00-220">説明</span><span class="sxs-lookup"><span data-stu-id="19a00-220">Description</span></span>                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="19a00-221">CreateSafeDropTransactionClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-221">CreateSafeDropTransactionClientRequestHandler</span></span>          | <span data-ttu-id="19a00-222">POS で金庫保管操作を行うときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-222">Executed when you do a safe drop operation in POS.</span></span>          |
| <span data-ttu-id="19a00-223">GetTenderDetailsClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-223">GetTenderDetailsClientRequestHandler</span></span>                   | <span data-ttu-id="19a00-224">POS で支払/入金申告の詳細を取得するときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-224">Executed when you get tender declaration details in POS.</span></span>  |
| <span data-ttu-id="19a00-225">CreateBankDropTransactionClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-225">CreateBankDropTransactionClientRequestHandler</span></span>          | <span data-ttu-id="19a00-226">POS で銀行入金操作を行うときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-226">Executed when you do a bank drop operation in POS.</span></span>          |
| <span data-ttu-id="19a00-227">CreateTenderDeclarationTransactionClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-227">CreateTenderDeclarationTransactionClientRequestHandler</span></span> | <span data-ttu-id="19a00-228">POS で支払/入金申告操作を行うときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-228">Executed when you do a tender declaration operation in POS.</span></span> |


<span data-ttu-id="19a00-229">**販売注文の要求ハンドラー**</span><span class="sxs-lookup"><span data-stu-id="19a00-229">**Sales orders request handlers**</span></span>

| <span data-ttu-id="19a00-230">要求名</span><span class="sxs-lookup"><span data-stu-id="19a00-230">Request name</span></span>                                           | <span data-ttu-id="19a00-231">説明</span><span class="sxs-lookup"><span data-stu-id="19a00-231">Description</span></span>                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="19a00-232">GetGiftReceiptsClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-232">GetGiftReceiptsClientRequestHandler</span></span>                | <span data-ttu-id="19a00-233">POS でギフト レシートを印刷するときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-233">Executed when you print a gift receipt in POS.</span></span>          |
| <span data-ttu-id="19a00-234">SelectCustomerOrderTypeClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="19a00-234">SelectCustomerOrderTypeClientRequestHandler</span></span>        | <span data-ttu-id="19a00-235">顧客注文または見積のどちらかを選択するためのオプションがあるダイアログ ボックスを取得するときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-235">Executed when you get a dialog box with options to choose between Customer order or quote.</span></span>          |



<span data-ttu-id="19a00-236">**POS でハンドラーをオーバーライドする方法**</span><span class="sxs-lookup"><span data-stu-id="19a00-236">**How to override a handler in POS**</span></span>

<span data-ttu-id="19a00-237">上記の POS 要求ハンドラー ロジックのいずれかをオーバーライドすると、次の手順を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="19a00-237">If you want to override any of the above POS request handler logic, you to need to use the following steps:</span></span>

1.  <span data-ttu-id="19a00-238">新しいクラスを作成し、対応するハンドラー クラスから拡張します。</span><span class="sxs-lookup"><span data-stu-id="19a00-238">Create a new class and extend it from the corresponding handler class.</span></span> <span data-ttu-id="19a00-239">たとえば、GetSerialNumberClientRequestHandler をオーバーライドする場合、クラスを GetSerialNumberClientRequestHandler から拡張します。</span><span class="sxs-lookup"><span data-stu-id="19a00-239">For example, if you are overriding GetSerialNumberClientRequestHandler, then extend your class from GetSerialNumberClientRequestHandler.</span></span>

2.  <span data-ttu-id="19a00-240">executeAsync メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="19a00-240">Implement the executeAsync method.</span></span>

3.  <span data-ttu-id="19a00-241">既定のハンドラーを呼び出すか、executeAsync メソッド内でカスタム ロジックを実行して、応答を返します。</span><span class="sxs-lookup"><span data-stu-id="19a00-241">Either call the default handler or do your custom logic inside the executeAsync method and return the response.</span></span>

<span data-ttu-id="19a00-242">**ステップ バイ ステップの手順**</span><span class="sxs-lookup"><span data-stu-id="19a00-242">**Step by step instructions**</span></span>

<span data-ttu-id="19a00-243">次の例では、GetSerialNumberClientRequestHandler をオーバーライドして POS でシリアル番号の入力を自動化する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="19a00-243">The following example shows how to override the GetSerialNumberClientRequestHandler to automate the serial number entry in POS.</span></span> <span data-ttu-id="19a00-244">既定では、POS には、シリアル番号を要求するよう品目がコンフィギュレーションされている場合は、シリアル番号を入力するダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="19a00-244">By default, POS will display a dialog box to enter the serial number if the item is configured to ask for serial number.</span></span> <span data-ttu-id="19a00-245">このダイアログ ボックスが表示されないようにし、コードを使用してシリアル番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="19a00-245">We want to avoid showing this dialog box and enter serial number through code.</span></span>

1.  <span data-ttu-id="19a00-246">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="19a00-246">Open Visual Studio 2015 in administrator mode.</span></span>

2.  <span data-ttu-id="19a00-247">ModernPOS ソリューションを …\\RetailSDK\\POS から開きます。</span><span class="sxs-lookup"><span data-stu-id="19a00-247">Open ModernPOS solution from …\\RetailSDK\\POS.</span></span>

3.  <span data-ttu-id="19a00-248">POS.Extensions プロジェクトで、POSRequestHandlerExtension という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="19a00-248">Under the POS.Extensions project, create a new folder called POSRequestHandlerExtension.</span></span>

4.  <span data-ttu-id="19a00-249">POSRequestHandlerExtension フォルダーに、Handlers という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="19a00-249">Under the POSRequestHandlerExtension folder, create new folder called Handlers.</span></span>

5.  <span data-ttu-id="19a00-250">Handlers フォルダーに、新しい .ts (typescript) ファイルを追加し、GetSerialNumberClientRequestHandlerExt.ts と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="19a00-250">In the Handlers folder, add a new .ts (typescript) file and name it GetSerialNumberClientRequestHandlerExt.ts.</span></span>

6.  <span data-ttu-id="19a00-251">次の import ステートメントを追加して、GetSerialNumberClientRequestHandlerExt.ts ファイルに関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="19a00-251">Add the following import statement to import the relevant entities and context in the GetSerialNumberClientRequestHandlerExt.ts file.</span></span>

 ```Typescrip 
 import { GetSerialNumberClientRequestHandler } from "PosApi/Extend/RequestHandlers/ProductsRequestHandlers";
 import { GetSerialNumberClientRequest, GetSerialNumberClientResponse } from "PosApi/Consume/Products";
 import { ClientEntities } from "PosApi/Entities";
```
7.  <span data-ttu-id="19a00-252">GetSerialNumberClientRequestHandlerExt.ts ファイルで、GetSerialNumberClientRequestHandlerExtend という新しいクラスを作成し、GetSerialNumberClientRequestHandler から拡張します。</span><span class="sxs-lookup"><span data-stu-id="19a00-252">In the GetSerialNumberClientRequestHandlerExt.ts file, create a new class called GetSerialNumberClientRequestHandlerExtend and extend it from GetSerialNumberClientRequestHandler.</span></span>

    <span data-ttu-id="19a00-253">export default class GetSerialNumberClientRequestHandlerExt extends GetSerialNumberClientRequestHandler { }</span><span class="sxs-lookup"><span data-stu-id="19a00-253">export default class GetSerialNumberClientRequestHandlerExt extends GetSerialNumberClientRequestHandler { }</span></span>

8.  <span data-ttu-id="19a00-254">GetSerialNumberClientRequestHandlerExt クラス内に executeAsync メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="19a00-254">Implement the executeAsync method inside the GetSerialNumberClientRequestHandlerExt class.</span></span> <span data-ttu-id="19a00-255">executeAsync メソッドでは、カスタム ロジックを書き込んで、応答を返すか、既定のハンドラーを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="19a00-255">In the executeAsync method, you can write your custom logic and return the response or call the default handler.</span></span> <span data-ttu-id="19a00-256">POS は、シリアル品目を販売するとき、シリアル番号のロジックを実行する executeAsync を探しますが、オーバーライドされるため、POS は標準メソッドの代わりにこのオーバーライドされた executeAsync メソッドを実行します。</span><span class="sxs-lookup"><span data-stu-id="19a00-256">When POS sells the serial item, it will look for executeAsync to execute the logic for the serial number, however because we are overriding it, POS will now execute this overridden executeAsync method instead of the standard method.</span></span>

 <span data-ttu-id="19a00-257">**executeAsync メソッドをオーバーライドする方法のサンプル実装**</span><span class="sxs-lookup"><span data-stu-id="19a00-257">**Sample implementation of how to override the executeAsync method**</span></span>

 ```Typescrip
 public executeAsync(request: GetSerialNumberClientRequest<GetSerialNumberClientResponse>):
     Promise<ClientEntities.ICancelableDataResult<GetSerialNumberClientResponse>> {

 // User could implement new business logic here to process the serial number.
 // The following example sets serial number "112233" for product 82001.

 if (request.product.ItemId === "82001") {
 let response: GetSerialNumberClientResponse = new GetSerialNumberClientResponse("112233");
 return Promise.resolve(<ClientEntities.ICancelableDataResult<GetSerialNumberClientResponse>>{

 canceled: false,
 data: response

 });

 }

 // If you don’t want to execute custom logic on some conditions, and you just want to call the standard logic, you can call the default request, as shown below.

 return this.defaultExecuteAsync(request);

 }
```
<span data-ttu-id="19a00-258">完全なサンプル コード:</span><span class="sxs-lookup"><span data-stu-id="19a00-258">Full sample code:</span></span>

 ```Typescrip
 /**
 * SAMPLE CODE NOTICE
 *
 * THIS SAMPLE CODE IS MADE AVAILABLE AS IS. MICROSOFT MAKES NO WARRANTIES, WHETHER EXPRESS OR IMPLIED,
 * OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY OR COMPLETENESS OF RESPONSES, OF RESULTS, OR CONDITIONS OF MERCHANTABILITY.
 * THE ENTIRE RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS SAMPLE CODE REMAINS WITH THE USER.
 * NO TECHNICAL SUPPORT IS PROVIDED. YOU MAY NOT DISTRIBUTE THIS CODE UNLESS YOU HAVE A LICENSE AGREEMENT WITH MICROSOFT THAT ALLOWS YOU TO DO SO.
 */

 import { GetSerialNumberClientRequestHandler } from "PosApi/Extend/RequestHandlers/ProductsRequestHandlers";
 import { GetSerialNumberClientRequest, GetSerialNumberClientResponse } from "PosApi/Consume/Products";
 import { ClientEntities } from "PosApi/Entities";

 /**
 * Override request handler class for getting serial number request.
 */

 export default class GetSerialNumberClientRequestHandlerExt extends GetSerialNumberClientRequestHandler {

 /**
 * Executes the request handler asynchronously.
 * @param {GetSerialNumberClientRequest<GetSerialNumberClientResponse>} request The request containing the response.
 * @return {Promise<ICancelableDataResult<GetSerialNumberClientResponse>>} The cancelable promise containing the response.
 */

 public executeAsync(request: GetSerialNumberClientRequest<GetSerialNumberClientResponse>):
    Promise<ClientEntities.ICancelableDataResult<GetSerialNumberClientResponse>> {

 // User could implement new business logic here to process the serial number.
 // The following example sets serial number "112233" for product 82001.

 if (request.product.ItemId === "82001") {
 let response: GetSerialNumberClientResponse = new GetSerialNumberClientResponse("112233");
 return Promise.resolve(<ClientEntities.ICancelableDataResult<GetSerialNumberClientResponse>>{
 canceled: false,
 data: response
 });

 }
 return this.defaultExecuteAsync(request);
 }
 }

```
9.  <span data-ttu-id="19a00-259">POSRequestHandlerExtension フォルダーの下に新しい json ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="19a00-259">Create a new json file under the POSRequestHandlerExtension folder.</span></span> <span data-ttu-id="19a00-260">manifest.json という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="19a00-260">Name it manifest.json.</span></span>

10.  <span data-ttu-id="19a00-261">manifest.json ファイルに、次のコードをコピーして貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="19a00-261">In the manifest.json file, copy and paste the following code.</span></span> <span data-ttu-id="19a00-262">このコードをコピーする前に、既定で生成されたコードを削除してください。</span><span class="sxs-lookup"><span data-stu-id="19a00-262">Be sure to delete the default generated code before copying this code.</span></span>

 ```Typescrip
 {
 "$schema": "../manifestSchema.json",
 "name": "Pos_Extensibility_Samples",
 "publisher": "Microsoft",
 "version": "7.3.5.0",
 "minimumPosVersion": "7.3.5.0",
 "components": {
 "extend": {
 "requestHandlers": [
 {
 "modulePath": "Handlers/GetSerialNumberClientRequestHandlerExt"
 }
 ]
 }
 }
}
```
11.  <span data-ttu-id="19a00-263">POS.Extensions プロジェクトにある extensions.json ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="19a00-263">Open the extensions.json file under the POS.Extensions project.</span></span> <span data-ttu-id="19a00-264">実行時の POS にこの拡張が含まれるように、POSRequestHandlerExtension サンプルで更新します。</span><span class="sxs-lookup"><span data-stu-id="19a00-264">Update it with POSRequestHandlerExtension samples, so that POS during runtime will include this extension.</span></span>
 
```Typescrip
 {
 "extensionPackages": [
    { 
       "baseUrl": "SampleExtensions2" 
     }, 
     { 
       "baseUrl": " SampleExtensions" 
     }, 
     {
      "baseUrl": "POSRequestHandlerExtension"
 }
 ]
}
```
> [!NOTE]
> <span data-ttu-id="19a00-265">extension.json ファイルには、常に 2 つの拡張フォルダー名が含まれている必要があるため、必ず SampleExtensions フォルダー名またはカスタム拡張フォルダー名を保持してください。</span><span class="sxs-lookup"><span data-stu-id="19a00-265">The extension.json file should always contain two extensions folder names, so be sure to keep the SampleExtensions folder name or your custom extension folder name.</span></span> <span data-ttu-id="19a00-266">生産には、サンプル拡張を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="19a00-266">For production, don’t use the sample extensions.</span></span> <span data-ttu-id="19a00-267">独自の拡張フォルダーを追加し、すべてのサンプルを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="19a00-267">You should add your own extension folders and remove all the samples.</span></span>

12.  <span data-ttu-id="19a00-268">tsconfig.json ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="19a00-268">Open the tsconfig.json file to comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="19a00-269">POS では、このファイルを使用して、コンパイル用に拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="19a00-269">POS will use this file to include or exclude the extension for compilation.</span></span> <span data-ttu-id="19a00-270">既定では、リストに除外されたすべての拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="19a00-270">By default, the list contains all the excluded extensions list.</span></span> <span data-ttu-id="19a00-271">POS の拡張部分をコンパイルする場合は、拡張フォルダー名を追加し、以下のように拡張リストから拡張をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="19a00-271">If you want to compile any extension part of the POS, then you need to add the extension folder name and comment the extension from the extension list, as shown below.</span></span>

 ```Typescrip
 "exclude": [

 // "SampleExtensions",
 //"SampleExtensions2",
 //"POSRequestHandlerExtension"

],
```
13.  <span data-ttu-id="19a00-272">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="19a00-272">Compile and rebuild the project.</span></span>

<span data-ttu-id="19a00-273">**拡張機能をテストする方法**</span><span class="sxs-lookup"><span data-stu-id="19a00-273">**How to test your extension**</span></span>

1.  <span data-ttu-id="19a00-274">F5 キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="19a00-274">Press F5 and deploy the POS to test your customization.</span></span>

2.  <span data-ttu-id="19a00-275">POS が開始されたら、POS にサインインし、トランザクションへシリアル品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="19a00-275">After POS launches, sign in to POS and add a serial item to a transaction.</span></span>

3.  <span data-ttu-id="19a00-276">拡張コードにブレークポイントを配置します。</span><span class="sxs-lookup"><span data-stu-id="19a00-276">Place a break point in the extension code.</span></span> <span data-ttu-id="19a00-277">シリアル品目を追加するとき、拡張コードをデバッグできるはずです。</span><span class="sxs-lookup"><span data-stu-id="19a00-277">When you add the serial item you should be able to debug the extension code.</span></span>
