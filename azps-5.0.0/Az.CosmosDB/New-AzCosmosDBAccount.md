---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: f082f9390dd5a00fa5984aa2e0df26e8c3b63636
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285535"
---
# <span data-ttu-id="652fe-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="652fe-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="652fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="652fe-102">SYNOPSIS</span></span>
<span data-ttu-id="652fe-103">建立新的 CosmosDB 帳戶。</span><span class="sxs-lookup"><span data-stu-id="652fe-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="652fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="652fe-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>]
 [-ServerVersion <String>] [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="652fe-105">說明</span><span class="sxs-lookup"><span data-stu-id="652fe-105">DESCRIPTION</span></span>
<span data-ttu-id="652fe-106">在指定的 ResourceGroup 中建立新的 CosmosDB 帳戶。</span><span class="sxs-lookup"><span data-stu-id="652fe-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="652fe-107">示例</span><span class="sxs-lookup"><span data-stu-id="652fe-107">EXAMPLES</span></span>

### <span data-ttu-id="652fe-108">範例1</span><span class="sxs-lookup"><span data-stu-id="652fe-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name databaseAccountName  -Location "East US"

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {databaseAccountName-eastus}
ReadLocations                 : {databaseAccountName-eastus}
FailoverPolicies              : {databaseAccountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/databaseAccountName
Name                          : databaseAccountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="652fe-109">在 ResourceGroup resourceGroupName 中，會建立名稱為 databaseAccountName 的新 CosmosDB 帳戶。</span><span class="sxs-lookup"><span data-stu-id="652fe-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="652fe-110">參數</span><span class="sxs-lookup"><span data-stu-id="652fe-110">PARAMETERS</span></span>

### <span data-ttu-id="652fe-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="652fe-111">-ApiKind</span></span>
<span data-ttu-id="652fe-112">要建立的 Cosmos DB 資料庫帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="652fe-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="652fe-113">已接受的值： GlobalDocumentDB、MongoDB、Gremlin、Table、Cassandra。</span><span class="sxs-lookup"><span data-stu-id="652fe-113">Accepted values: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="652fe-114">預設值： GlobalDocumentDB</span><span class="sxs-lookup"><span data-stu-id="652fe-114">Default value: GlobalDocumentDB</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="652fe-115">-AsJob</span></span>
<span data-ttu-id="652fe-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="652fe-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-117">-確認</span><span class="sxs-lookup"><span data-stu-id="652fe-117">-Confirm</span></span>
<span data-ttu-id="652fe-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="652fe-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="652fe-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="652fe-120">Cosmos DB 資料庫帳戶的預設一致性等級。</span><span class="sxs-lookup"><span data-stu-id="652fe-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="652fe-121">已接受的值： BoundedStaleness、ConsistentPrefix、最終、會話、強</span><span class="sxs-lookup"><span data-stu-id="652fe-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="652fe-122">-DefaultProfile</span></span>
<span data-ttu-id="652fe-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="652fe-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="652fe-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="652fe-125">在中繼資料資源 (資料庫、容器、透過帳戶金鑰) 的輸送量中停用寫入作業</span><span class="sxs-lookup"><span data-stu-id="652fe-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="652fe-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="652fe-127">[Bool]，表示該帳戶是否已啟用 AnalyticalStorage。</span><span class="sxs-lookup"><span data-stu-id="652fe-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="652fe-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="652fe-129">在由於中斷而無法使用區域的極少事件中，啟用寫入區域的自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="652fe-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="652fe-130">自動容錯移轉會針對該帳戶產生新的寫入區域，並根據針對該帳戶所設定的容錯移轉優先順序來選取。</span><span class="sxs-lookup"><span data-stu-id="652fe-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="652fe-131">已接受的值： false、true</span><span class="sxs-lookup"><span data-stu-id="652fe-131">Accepted values: false, true</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-132">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="652fe-132">-EnableFreeTier</span></span>
<span data-ttu-id="652fe-133">[Bool]，表示該帳戶是否已啟用 FreeTier。</span><span class="sxs-lookup"><span data-stu-id="652fe-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="652fe-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="652fe-135">啟用多個寫位置。</span><span class="sxs-lookup"><span data-stu-id="652fe-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="652fe-136">已接受的值： false、true</span><span class="sxs-lookup"><span data-stu-id="652fe-136">Accepted values: false, true</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="652fe-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="652fe-138">在 Cosmos DB 資料庫帳戶上啟用虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="652fe-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="652fe-139">已接受的值： false、true</span><span class="sxs-lookup"><span data-stu-id="652fe-139">Accepted values: false, true</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="652fe-140">-IpRule</span></span>
<span data-ttu-id="652fe-141">防火牆支援。</span><span class="sxs-lookup"><span data-stu-id="652fe-141">Firewall support.</span></span> <span data-ttu-id="652fe-142">指定 CIDR 格式的 IP 位址或 IP 位址範圍的集合，以作為指定資料庫帳戶的允許用戶端 Ip 清單。</span><span class="sxs-lookup"><span data-stu-id="652fe-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="652fe-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="652fe-144">KeyVault 的 URI</span><span class="sxs-lookup"><span data-stu-id="652fe-144">URI of the KeyVault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-145">-位置</span><span class="sxs-lookup"><span data-stu-id="652fe-145">-Location</span></span>
<span data-ttu-id="652fe-146">在 Cosmos DB 資料庫帳戶中新增位置。</span><span class="sxs-lookup"><span data-stu-id="652fe-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="652fe-147">依容錯移轉優先順序排序的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="652fe-147">Array of strings, ordered by failover priority.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-148">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="652fe-148">-LocationObject</span></span>
<span data-ttu-id="652fe-149">在 Cosmos DB 資料庫帳戶中新增位置。</span><span class="sxs-lookup"><span data-stu-id="652fe-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="652fe-150">PSLocation 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="652fe-150">Array of PSLocation objects.</span></span>

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-151">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="652fe-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="652fe-152">在與限制失效的一致性搭配使用時，此值代表 timespan) 容許的過期 (時間量。</span><span class="sxs-lookup"><span data-stu-id="652fe-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="652fe-153">此值的接受範圍是5-86400。</span><span class="sxs-lookup"><span data-stu-id="652fe-153">Accepted range for this value is 5-86400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="652fe-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="652fe-155">在與限制失效的一致性搭配使用時，此值代表容許的過時要求數量。</span><span class="sxs-lookup"><span data-stu-id="652fe-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="652fe-156">此值的接受範圍為 1-2147483647。</span><span class="sxs-lookup"><span data-stu-id="652fe-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-157">-名稱</span><span class="sxs-lookup"><span data-stu-id="652fe-157">-Name</span></span>
<span data-ttu-id="652fe-158">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="652fe-158">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="652fe-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="652fe-160">此伺服器是否允許公用端點存取。</span><span class="sxs-lookup"><span data-stu-id="652fe-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="652fe-161">可能的值包括：「已啟用」、「已停用」</span><span class="sxs-lookup"><span data-stu-id="652fe-161">Possible values include: 'Enabled', 'Disabled'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="652fe-162">-ResourceGroupName</span></span>
<span data-ttu-id="652fe-163">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="652fe-163">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="652fe-164">-ServerVersion</span></span>
<span data-ttu-id="652fe-165">ServerVersion，僅在 MongoDB 帳戶時有效。</span><span class="sxs-lookup"><span data-stu-id="652fe-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="652fe-166">-Tag</span></span>
<span data-ttu-id="652fe-167">以鍵值對的方式將標記 Hashtable 組成。</span><span class="sxs-lookup"><span data-stu-id="652fe-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="652fe-168">使用空字串清除現有標記。</span><span class="sxs-lookup"><span data-stu-id="652fe-168">Use empty string to clear existing tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-169">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="652fe-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="652fe-170">虛擬網路 ACL 的字串值陣列。</span><span class="sxs-lookup"><span data-stu-id="652fe-170">Array of string values of ACL's for virtual network.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-171">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="652fe-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="652fe-172">虛擬網路的 PSVirtualNetworkRuleObjects 陣列。</span><span class="sxs-lookup"><span data-stu-id="652fe-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="652fe-173">-WhatIf</span></span>
<span data-ttu-id="652fe-174">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="652fe-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="652fe-175">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="652fe-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652fe-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="652fe-176">CommonParameters</span></span>
<span data-ttu-id="652fe-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="652fe-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="652fe-178">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="652fe-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="652fe-179">輸入</span><span class="sxs-lookup"><span data-stu-id="652fe-179">INPUTS</span></span>

### <span data-ttu-id="652fe-180">PSCorsRule [] 的 CosmosDB []</span><span class="sxs-lookup"><span data-stu-id="652fe-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="652fe-181">輸出</span><span class="sxs-lookup"><span data-stu-id="652fe-181">OUTPUTS</span></span>

### <span data-ttu-id="652fe-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="652fe-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="652fe-183">筆記</span><span class="sxs-lookup"><span data-stu-id="652fe-183">NOTES</span></span>

## <span data-ttu-id="652fe-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="652fe-184">RELATED LINKS</span></span>