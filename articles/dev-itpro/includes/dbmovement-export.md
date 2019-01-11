## <a name="self-service-database-export"></a><span data-ttu-id="cf994-101">データベースのセルフ サービスエクスポート</span><span class="sxs-lookup"><span data-stu-id="cf994-101">Self-service database export</span></span>

<span data-ttu-id="cf994-102">サンド ボックス環境詳細ページで、**管理** メニューをクリックし、**データベースの移動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf994-102">From your sandbox environment details page, click the **Maintain** menu and then select **Move database**.</span></span>  
<img src="../database/media/DBMovement_Menu.png" width="400px" alt="Move database menu" />

<span data-ttu-id="cf994-103">**エクスポート データベース**アクションが使用できるページでスライダー ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="cf994-103">A slider pane will open on the page where you can use the **Export database** action.</span></span>
<br/>
<img src="../database/media/Export_Menu.png" width="400px" alt="Export database menu"/>

<span data-ttu-id="cf994-104">サンド ボックスの更新やパッケージの展開などの他のサービス操作はこの間実行できません。</span><span class="sxs-lookup"><span data-stu-id="cf994-104">The environment will be unavailable for other servicing operations such as Sandbox Refresh or Package Deployment during this time.</span></span> <span data-ttu-id="cf994-105">ソース環境は Dynamics ユーザーの観点から使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="cf994-105">The source environment will be usable from a Dynamics user perspective.</span></span>  

<span data-ttu-id="cf994-106">エクスポートが正常に完了すると、**環境の詳細** ページで実行している操作からサインオフされます。</span><span class="sxs-lookup"><span data-stu-id="cf994-106">After the export operation completes successfully, sign off on the servicing operation on your **Environment details** page.</span></span> <span data-ttu-id="cf994-107">**データベースのバックアップ** セクションの **資産ライブラリ** で資産を確認できます。</span><span class="sxs-lookup"><span data-stu-id="cf994-107">You can then see the asset in your **Asset Library** in the **Database backups** section.</span></span>
<img src="../database/media/AssetLibrary_Backups.png" width="800px" alt="Asset library backup files"/>

<span data-ttu-id="cf994-108">.bacpac ファイルではここに保存され、レベル 1 開発者環境に手動でダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="cf994-108">The .bacpac files are stored here and can be manually downloaded to your Tier 1 developer environments for import.</span></span> <span data-ttu-id="cf994-109">今後、Microsoft は、エクスポート アクションをトリガーし、資産ライブラリで使用可能なバックアップ ファイルを一覧表示するための API を提供します。</span><span class="sxs-lookup"><span data-stu-id="cf994-109">In the future, Microsoft will provide APIs to trigger the export action, as well as list the available backup files in your asset library.</span></span> <span data-ttu-id="cf994-110">これには、バックアップ資産ファイルを自動でダウンロードするための、または Microsoft Azure Storage SDK を使用して、独自のセキュリティで保護された BLOB ストレージに直接コピーするための、セキュリティで保護された URL が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cf994-110">This includes the secured URL for automatically downloading a backup asset file or copying it directly to your own secure blob storage using Microsoft Azure Storage SDKs.</span></span>