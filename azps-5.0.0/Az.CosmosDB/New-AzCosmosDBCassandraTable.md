---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 42ec4db0f9c0967e375cc30a582c35aaca65840f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285528"
---
# <span data-ttu-id="3b213-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="3b213-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="3b213-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b213-102">SYNOPSIS</span></span>
<span data-ttu-id="3b213-103">建立新的 CosmosDB Cassandra 表格。</span><span class="sxs-lookup"><span data-stu-id="3b213-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="3b213-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b213-104">SYNTAX</span></span>

### <span data-ttu-id="3b213-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3b213-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b213-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b213-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b213-107">說明</span><span class="sxs-lookup"><span data-stu-id="3b213-107">DESCRIPTION</span></span>
<span data-ttu-id="3b213-108">建立新的 CosmosDB Cassandra 表格。</span><span class="sxs-lookup"><span data-stu-id="3b213-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="3b213-109">示例</span><span class="sxs-lookup"><span data-stu-id="3b213-109">EXAMPLES</span></span>

### <span data-ttu-id="3b213-110">範例1</span><span class="sxs-lookup"><span data-stu-id="3b213-110">Example 1</span></span>
```powershell
PS C:\>       
      $Column1 = New-AzCosmosDBCassandraColumn -Name "ColumnA" -Type "int"
      $Column2 = New-AzCosmosDBCassandraColumn -Name "ColumnB" -Type "ascii"
      $Column3 = New-AzCosmosDBCassandraColumn -Name "ColumnC" -Type "int"
      $Column4 = New-AzCosmosDBCassandraColumn -Name "ColumnD" -Type "ascii"

      $clusterkey1 = New-AzCosmosDBCassandraClusterKey -Name "ColumnB" -OrderBy "Asc"
      $clusterkey2 = New-AzCosmosDBCassandraClusterKey -Name "ColumnA" -OrderBy "Asc"

      $schema = New-AzCosmosDBCassandraSchema -Column $Column1,$Column2 -ClusterKey $clusterkey1 -PartitionKey "ColumnA"

      New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema $schema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

## <span data-ttu-id="3b213-111">參數</span><span class="sxs-lookup"><span data-stu-id="3b213-111">PARAMETERS</span></span>

### <span data-ttu-id="3b213-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3b213-112">-AccountName</span></span>
<span data-ttu-id="3b213-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b213-113">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b213-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="3b213-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="3b213-115">分析儲存 TTL。</span><span class="sxs-lookup"><span data-stu-id="3b213-115">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="3b213-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="3b213-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="3b213-117">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="3b213-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="3b213-118">-確認</span><span class="sxs-lookup"><span data-stu-id="3b213-118">-Confirm</span></span>
<span data-ttu-id="3b213-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3b213-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b213-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b213-120">-DefaultProfile</span></span>
<span data-ttu-id="3b213-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b213-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b213-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="3b213-122">-KeyspaceName</span></span>
<span data-ttu-id="3b213-123">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="3b213-123">Cassandra Keyspace Name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b213-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b213-124">-Name</span></span>
<span data-ttu-id="3b213-125">Cassandra 資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="3b213-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="3b213-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3b213-126">-ParentObject</span></span>
<span data-ttu-id="3b213-127">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="3b213-127">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b213-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b213-128">-ResourceGroupName</span></span>
<span data-ttu-id="3b213-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b213-129">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b213-130">-架構</span><span class="sxs-lookup"><span data-stu-id="3b213-130">-Schema</span></span>
<span data-ttu-id="3b213-131">PSCassandraSchema 物件。</span><span class="sxs-lookup"><span data-stu-id="3b213-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="3b213-132">使用 New-AzCosmosDBCassandraSchema 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="3b213-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b213-133">-輸送量</span><span class="sxs-lookup"><span data-stu-id="3b213-133">-Throughput</span></span>
<span data-ttu-id="3b213-134">Cassandra Keyspace (RU/秒的輸送量) 。</span><span class="sxs-lookup"><span data-stu-id="3b213-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="3b213-135">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="3b213-135">Default value is 400.</span></span>

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

### <span data-ttu-id="3b213-136">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="3b213-136">-TtlInSeconds</span></span>
<span data-ttu-id="3b213-137">預設 Ttl （以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3b213-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="3b213-138">如果值遺失或設定為-1，則專案不會過期。</span><span class="sxs-lookup"><span data-stu-id="3b213-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="3b213-139">如果該值設定為 n，專案將在最後修改時間之後到期 n 秒。</span><span class="sxs-lookup"><span data-stu-id="3b213-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="3b213-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b213-140">-WhatIf</span></span>
<span data-ttu-id="3b213-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3b213-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b213-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b213-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b213-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b213-143">CommonParameters</span></span>
<span data-ttu-id="3b213-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b213-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b213-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3b213-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b213-146">輸入</span><span class="sxs-lookup"><span data-stu-id="3b213-146">INPUTS</span></span>

### <span data-ttu-id="3b213-147">PSCassandraSchema 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="3b213-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="3b213-148">PSCassandraKeyspaceGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="3b213-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="3b213-149">輸出</span><span class="sxs-lookup"><span data-stu-id="3b213-149">OUTPUTS</span></span>

### <span data-ttu-id="3b213-150">PSCassandraTableGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="3b213-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="3b213-151">ConflictingResourceException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="3b213-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="3b213-152">筆記</span><span class="sxs-lookup"><span data-stu-id="3b213-152">NOTES</span></span>

## <span data-ttu-id="3b213-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b213-153">RELATED LINKS</span></span>