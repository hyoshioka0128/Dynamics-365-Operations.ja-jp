---
title: Talent のプロビジョニング
description: このトピックでは、Microsoft Dynamics 365 for Talent の新しい環境のプロビジョニングについて説明します。
author: andreabichsel
manager: AnnBe
ms.date: 05/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: c249df697553cd42eccd59d3f2c3f5f083ead1cb
ms.sourcegitcommit: 15154b0aa86110ce5fad6f63e6763103a676a1d2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/10/2019
ms.locfileid: "1624610"
---
# <a name="provision-talent"></a>Talent のプロビジョニング

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Talent の新しい実稼動環境のプロビジョニングについて説明します。 このトピックでは、Talent をクラウド ソリューション プロバイダー、またはエンタープライズ アーキテクチャ (EA) 契約を通して購入したことを前提にしています。 Talent サービス プランがすでに含まれている Microsoft Dynamics 365 ライセンスがあり、このトピックの手順を完了できない場合は、サポートに問い合わせてください。

始めに、グローバル管理者は [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) にサインインし、新しい Talent プロジェクトを作成します。 ライセンスの問題で Talent プロビジョニングが妨げられない限り、サポートまたは Dynamics サービス エンジニアリング チーム (DSE) の担当者に問い合わせる必要はありません

## <a name="create-an-lcs-project"></a>LCS プロジェクトの作成
Talent 環境を管理するために LCS を使用するには、最初に LCS プロジェクトを作成する必要があります。

1. Talent をサブスクライブするために使用したアカウントを使用して [LCS](https://lcs.dynamics.com/Logon/Index) にサインインします。
2. プラス記号 (**+**) を選択してプロジェクトを作成します。
3. 製品名、製品バージョンとして **Microsoft Dynamics 365 for Talent** を選択します。
4. **Dynamics 365 for Talent** 方法を選択します。
5. **作成** を選択します。

Talent を使い始める方法については、新しいプロジェクトで作成した **Talent** の方法を参照してくだい。 プロジェクトの作成が終了したら、Talent 環境を設定するために次の手順を完了してください。

## <a name="provision-a-talent-project"></a>Talent プロジェクトのプロビジョニング
LCS プロジェクトを作成した後は、環境に Talent をプロビジョニングすることができます。

1. LCS プロジェクトでは、**Talent アプリの管理** タイルを選択します。
2. これが人材のサンドボックスまたは実稼働インスタンスであるかどうかを示します。 初期のプレビュー機能をサンドボックス インスタンスで使用することにより、早期のフィードバックおよびテストを行うことができます。 
    > [!NOTE]
    > Talent のインスタンス タイプは、PowerApps 管理センターで設定された PowerApps 環境のインスタンス タイプとは異なります。
3. Talent テスト ドライブ エクスペリエンスで使用される同じデモ データのセットを環境に含める場合は、**デモ データを含む**オプションをオンにします。 これは長期的なデモまたはトレーニング環境に便利であり、稼動環境で使用されることはありません。  初期展開時にこのオプションを選択する必要があることに注意してください。 後で、既存の配置を更新することはできません。
4. Talent は、Microsoft PowerApps の環境に常にプロビジョニングされていて、これにより PowerApps の統合および拡張機能が有効になります。 続行する前に、このトピックの「PowerApps 環境の選択」を参照してください。 まだ PowerApps 環境を持っていない場合は、LCS で環境の管理を選択するか、または PowerApps 管理センターに移動します。 次に、以下の手順に従います [PowerApps 環境の作成](https://docs.microsoft.com/en-us/powerapps/administrator/create-environment)。

    > [!NOTE]
    > 既存の環境を表示、または新しい環境を作成するために、Talent をプロビジョニングするテナント管理者は PowerApps P2 ライセンスに割り当てられる必要があります。 組織に PowerApps P2 ライセンスがない場合、CSP または [PowerApps 価格ページ](https://powerapps.microsoft.com/en-us/pricing/) から入手することができます。

5. 人材を供給する環境を選択します。
6. 使用条件に同意、および展開を開始するために **はい** を選択します。

    新しい環境は、左のナビゲーション ウィンドウにある環境の一覧に表示されます。 ただし、配置状態が**配置済み**に更新されるまでは、環境の使用を開始できません。 このプロセスには通常、数分間かかります。 プロビジョニング プロセスに失敗する場合は、サポートに連絡する必要があります。

7. 新しい環境を使用するために **Talent にログオンします** を選択します。

    > [!NOTE]
    > 最終要件をまだサインオフしていない場合、プロジェクトに Talent のテスト インスタンスを配置することができます。 サインオフするまで、ソリューションをテストするためにこのインスタンスを使用することができます。 テストのために新しい環境を使用する場合は、実稼動環境を作成するためにこの手順を繰り返す必要があります。

    > Talent 定期売買の一部として 2 つの LCS 環境のみが許可されるため、60 日間無料 [Talent 試用環境](https://dynamics.microsoft.com/en-us/talent/overview/) の活用を考慮するかもしれません。 試用環境は要求したユーザーにより所有されていますが、Core HR のシステム管理経験を通じて他のユーザーも招待できます。 試用環境には、安全にプログラムを活用するために使用する架空のデータが含まれます。 これらは実稼動環境として使用するものではありません。 試用環境が 60 日後に期限が切れると、その中にあるすべてのデータが削除され復元できないことに注意してください。 既存の環境の期限が切れた後、新しい試用環境に登録することができます。

## <a name="select-a-powerapps-environment"></a>PowerApps 環境の選択

Talent と PowerApps 環境との統合では、PowerApps ツールを使用して Talent データの使用を統合および拡張することができます。 PowerApps 環境の目的を理解することで、Talent を拡張するためのアプリを構築するために役立つだけでなく、Talent プロビジョニングするときに正しい環境を選択するのにも役立ちます。 環境スコープ、環境アクセス、および環境の作成および選択を含む、PowerApps 環境の詳細については、[ PowerApps 環境の発表](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/) をご覧ください。 

Talent を配置する PowerApps 環境を決定する際には、次のガイダンスを参考にしてください。 

1. LCS で**管理の環境**を選択するか、または PowerApps 管理者センターに直接移動して、既存の環境を表示および新しい環境を作成できます。
2. 1 つの Talent 環境は、1 つの PowerApps 環境にマップされます。
3. PowerApps 環境には、対応する PowerApps、フロー、および Common Data Service アプリケーションと共に、Talent アプリケーションが「含まれて」います。 PowerApps 環境を削除すると、その中のアプリも削除されます。 Talent 環境をプロビジョニングする場合、「試用版」または「製品版」のいずれかをプロビジョニングできます。 環境の使用方法に基づいて環境のタイプを選択します。 
4. サンドボックス、UAT、または生産などのデータの統合およびテスト戦略を考慮する必要があります。 PowerApps 環境にマッピングされる Talent 環境を後に変更することは容易ではないため、配置へのさまざまな影響について考慮することをお勧めします。
5. 次の PowerApps 環境は Talent に対しては使用できず、LCS 内の選択リストからもフィルター処理されます。
 
    - **既定の PowerApps 環境** - 各テナントは、既定の PowerApps 環境で自動的にプロビジョニングされますが、すべてのテナント ユーザーは PowerApps 環境にアクセスすることができ、PowerApps または Flow 統合を使用してテストや調査を行う際に意図せずに生産データが壊れる可能性があるため、Talent でそれらを使用することはお勧めしません。
   
    - **試用環境** - これらの環境は有効期限付きで作成され、その期間が経過すると有効期限切れになり、環境およびその中に含まれるすべての Talent インスタンスは自動的に削除されます。
   
    - **サポートされていない地域** - 現在の Talent は、次の地域でのみサポートされます: 米国、ヨーロッパ、英国またはオーストラリア。
  
6. 使用する正しい環境を決定した後、プロビジョニング プロセスを続行できます。 
 
## <a name="grant-access-to-the-environment"></a>環境へのアクセスを付与
既定では、環境を作成したグローバル管理者がそこにアクセスできます。 ただし、追加のアプリケーション ユーザーは、明示的にアクセスを許可する必要があります。 アクセスを許可するには、Core HR 環境でユーザーを追加し適切なロールを割り当てる必要があります。 Talent を展開するグローバル管理者は、初期化を完了して、他のテナント ユーザーのアクセスを有効にするため、Attract および Onboard アプリケーションの両方も起動する必要があります。  これが発生するまで、他のユーザーは Attract および Onboard アプリケーションにアクセスすることはできませんし、アクセス違反エラーが発生します。 詳細については、[新規ユーザーの作成](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) および [ユーザーのセキュリティ ロールへの割り当て](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles) を参照してください。 
