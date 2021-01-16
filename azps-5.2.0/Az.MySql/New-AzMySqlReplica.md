---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
ms.openlocfilehash: 54463e38982a711f98515879f826a3cd2e068384
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285083"
---
# <span data-ttu-id="c00f9-101">New-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="c00f9-101">New-AzMySqlReplica</span></span>

## <span data-ttu-id="c00f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c00f9-102">SYNOPSIS</span></span>
<span data-ttu-id="c00f9-103">從現有資料庫建立新的複本。</span><span class="sxs-lookup"><span data-stu-id="c00f9-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="c00f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="c00f9-104">SYNTAX</span></span>

```
New-AzMySqlReplica -Replica <String> -ResourceGroupName <String> -Master <IServer> [-SubscriptionId <String>]
 [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c00f9-105">說明</span><span class="sxs-lookup"><span data-stu-id="c00f9-105">DESCRIPTION</span></span>
<span data-ttu-id="c00f9-106">從現有資料庫建立新的複本。</span><span class="sxs-lookup"><span data-stu-id="c00f9-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="c00f9-107">示例</span><span class="sxs-lookup"><span data-stu-id="c00f9-107">EXAMPLES</span></span>

### <span data-ttu-id="c00f9-108">範例1：建立新的 MySql 伺服器複本</span><span class="sxs-lookup"><span data-stu-id="c00f9-108">Example 1: Create a new MySql server replica</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | New-AzMySqlReplica -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="c00f9-109">這個 Cmdlet 會建立新的 MySql 伺服器複製。</span><span class="sxs-lookup"><span data-stu-id="c00f9-109">This cmdlet creates a new MySql server replica.</span></span>

### <span data-ttu-id="c00f9-110">範例2：建立新的 MySql 伺服器複本</span><span class="sxs-lookup"><span data-stu-id="c00f9-110">Example 2: Create a new MySql server replica</span></span>
```powershell
PS C:\> $mysql = Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
PS C:\> New-AzMySqlReplica -Master $mysql -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="c00f9-111">此 Cmdlet 與參數主機 (inputobject) 會建立新的 MySql 伺服器複本。</span><span class="sxs-lookup"><span data-stu-id="c00f9-111">This cmdlet with parameter master(inputobject) creates a new MySql server replica.</span></span>

## <span data-ttu-id="c00f9-112">參數</span><span class="sxs-lookup"><span data-stu-id="c00f9-112">PARAMETERS</span></span>

### <span data-ttu-id="c00f9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c00f9-113">-AsJob</span></span>
<span data-ttu-id="c00f9-114">執行命令做為作業。</span><span class="sxs-lookup"><span data-stu-id="c00f9-114">Run the command as a job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c00f9-115">-DefaultProfile</span></span>
<span data-ttu-id="c00f9-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c00f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00f9-117">-位置</span><span class="sxs-lookup"><span data-stu-id="c00f9-117">-Location</span></span>
<span data-ttu-id="c00f9-118">資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="c00f9-118">The location the resource resides in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00f9-119">-主要</span><span class="sxs-lookup"><span data-stu-id="c00f9-119">-Master</span></span>
<span data-ttu-id="c00f9-120">要從中建立複本的來源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="c00f9-120">The source server object to create replica from.</span></span>
<span data-ttu-id="c00f9-121">若要建立，請參閱 MASTER 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c00f9-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c00f9-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c00f9-122">-NoWait</span></span>
<span data-ttu-id="c00f9-123">以非同步方式執行命令。</span><span class="sxs-lookup"><span data-stu-id="c00f9-123">Run the command asynchronously.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00f9-124">-複本</span><span class="sxs-lookup"><span data-stu-id="c00f9-124">-Replica</span></span>
<span data-ttu-id="c00f9-125">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c00f9-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00f9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c00f9-126">-ResourceGroupName</span></span>
<span data-ttu-id="c00f9-127">包含資源之資源群組的名稱，您可以從 Azure 資源管理員 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="c00f9-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00f9-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="c00f9-128">-Sku</span></span>
<span data-ttu-id="c00f9-129">Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="c00f9-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00f9-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c00f9-130">-SubscriptionId</span></span>
<span data-ttu-id="c00f9-131">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="c00f9-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00f9-132">-確認</span><span class="sxs-lookup"><span data-stu-id="c00f9-132">-Confirm</span></span>
<span data-ttu-id="c00f9-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c00f9-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00f9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c00f9-134">-WhatIf</span></span>
<span data-ttu-id="c00f9-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c00f9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c00f9-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c00f9-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00f9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c00f9-137">CommonParameters</span></span>
<span data-ttu-id="c00f9-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c00f9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c00f9-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c00f9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c00f9-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c00f9-140">INPUTS</span></span>

### <span data-ttu-id="c00f9-141">IServer 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="c00f9-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="c00f9-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c00f9-142">OUTPUTS</span></span>

### <span data-ttu-id="c00f9-143">IServer 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="c00f9-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="c00f9-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c00f9-144">NOTES</span></span>

<span data-ttu-id="c00f9-145">別名</span><span class="sxs-lookup"><span data-stu-id="c00f9-145">ALIASES</span></span>

<span data-ttu-id="c00f9-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c00f9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c00f9-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c00f9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c00f9-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c00f9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c00f9-149">MASTER <IServer> （主要）：要從中建立複本的來源伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="c00f9-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="c00f9-150">`Location <String>`：資源所在的地理位置</span><span class="sxs-lookup"><span data-stu-id="c00f9-150">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="c00f9-151">`SkuName <String>`： Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。</span><span class="sxs-lookup"><span data-stu-id="c00f9-151">`SkuName <String>`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="c00f9-152">`[Tag <ITrackedResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="c00f9-152">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="c00f9-153">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="c00f9-153">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c00f9-154">`[AdministratorLogin <String>]`：管理員的伺服器登入名稱。</span><span class="sxs-lookup"><span data-stu-id="c00f9-154">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="c00f9-155">只能在 (建立伺服器時指定，且在建立) 時需要。</span><span class="sxs-lookup"><span data-stu-id="c00f9-155">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="c00f9-156">`[EarliestRestoreDate <DateTime?>]`： (ISO8601 格式的最早還原點建立時間) </span><span class="sxs-lookup"><span data-stu-id="c00f9-156">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="c00f9-157">`[FullyQualifiedDomainName <String>]`：伺服器的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="c00f9-157">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="c00f9-158">`[IdentityType <IdentityType?>]`：身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="c00f9-158">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="c00f9-159">將此值設定為 ' SystemAssigned」，即可自動為資源建立並指派 Azure Active Directory 主體。</span><span class="sxs-lookup"><span data-stu-id="c00f9-159">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="c00f9-160">`[InfrastructureEncryption <InfrastructureEncryption?>]`：顯示伺服器是否已啟用基礎結構加密的狀態。</span><span class="sxs-lookup"><span data-stu-id="c00f9-160">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="c00f9-161">`[MasterServerId <String>]`：複本伺服器的主伺服器 id。</span><span class="sxs-lookup"><span data-stu-id="c00f9-161">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="c00f9-162">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`：為伺服器強制執行最低的 Tls 版本。</span><span class="sxs-lookup"><span data-stu-id="c00f9-162">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="c00f9-163">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`：此伺服器是否允許公用網路存取。</span><span class="sxs-lookup"><span data-stu-id="c00f9-163">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="c00f9-164">Value 是 optional，但如果傳入，就必須是「Enabled」或「Disabled」</span><span class="sxs-lookup"><span data-stu-id="c00f9-164">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="c00f9-165">`[ReplicaCapacity <Int32?>]`：主伺服器可擁有的複本數目上限。</span><span class="sxs-lookup"><span data-stu-id="c00f9-165">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="c00f9-166">`[ReplicationRole <String>]`：伺服器的複製角色。</span><span class="sxs-lookup"><span data-stu-id="c00f9-166">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="c00f9-167">`[SkuCapacity <Int32?>]`： [擴大/縮小] 容量，代表伺服器的計算單位。</span><span class="sxs-lookup"><span data-stu-id="c00f9-167">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="c00f9-168">`[SkuFamily <String>]`：硬體系列。</span><span class="sxs-lookup"><span data-stu-id="c00f9-168">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="c00f9-169">`[SkuSize <String>]`：根據需要由資源來轉譯的大小代碼。</span><span class="sxs-lookup"><span data-stu-id="c00f9-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="c00f9-170">`[SkuTier <SkuTier?>]`：特定 SKU 的層級，例如基本。</span><span class="sxs-lookup"><span data-stu-id="c00f9-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="c00f9-171">`[SslEnforcement <SslEnforcementEnum?>]`[：在連線至伺服器時，啟用 ssl 強制執行。</span><span class="sxs-lookup"><span data-stu-id="c00f9-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="c00f9-172">`[StorageProfileBackupRetentionDay <Int32?>]`：伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="c00f9-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="c00f9-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`：啟用地域冗余，或不用於伺服器備份。</span><span class="sxs-lookup"><span data-stu-id="c00f9-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="c00f9-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`：啟用儲存空間自動增長。</span><span class="sxs-lookup"><span data-stu-id="c00f9-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="c00f9-175">`[StorageProfileStorageMb <Int32?>]`：伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="c00f9-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="c00f9-176">`[UserVisibleState <ServerState?>]`：使用者可看見的伺服器狀態。</span><span class="sxs-lookup"><span data-stu-id="c00f9-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="c00f9-177">`[Version <ServerVersion?>]`：伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="c00f9-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="c00f9-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="c00f9-178">RELATED LINKS</span></span>
