---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 8998e9e2462e64dab3d2a96c739c93449e2e360c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285531"
---
# <span data-ttu-id="5e9d3-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="5e9d3-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="5e9d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="5e9d3-103">建立新的 CosmosDB Cassandra Keyspace。</span><span class="sxs-lookup"><span data-stu-id="5e9d3-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="5e9d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e9d3-104">SYNTAX</span></span>

### <span data-ttu-id="5e9d3-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5e9d3-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e9d3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e9d3-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e9d3-107">說明</span><span class="sxs-lookup"><span data-stu-id="5e9d3-107">DESCRIPTION</span></span>
<span data-ttu-id="5e9d3-108">建立新的 CosmosDB Cassandra Keyspace。</span><span class="sxs-lookup"><span data-stu-id="5e9d3-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="5e9d3-109">示例</span><span class="sxs-lookup"><span data-stu-id="5e9d3-109">EXAMPLES</span></span>

### <span data-ttu-id="5e9d3-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5e9d3-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="5e9d3-111">參數</span><span class="sxs-lookup"><span data-stu-id="5e9d3-111">PARAMETERS</span></span>

### <span data-ttu-id="5e9d3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5e9d3-112">-AccountName</span></span>
<span data-ttu-id="5e9d3-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e9d3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5e9d3-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5e9d3-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5e9d3-115">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="5e9d3-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5e9d3-116">-確認</span><span class="sxs-lookup"><span data-stu-id="5e9d3-116">-Confirm</span></span>
<span data-ttu-id="5e9d3-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5e9d3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e9d3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e9d3-118">-DefaultProfile</span></span>
<span data-ttu-id="5e9d3-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e9d3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e9d3-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e9d3-120">-Name</span></span>
<span data-ttu-id="5e9d3-121">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="5e9d3-121">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="5e9d3-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5e9d3-122">-ParentObject</span></span>
<span data-ttu-id="5e9d3-123">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="5e9d3-123">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e9d3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e9d3-124">-ResourceGroupName</span></span>
<span data-ttu-id="5e9d3-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e9d3-125">Name of resource group.</span></span>

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

### <span data-ttu-id="5e9d3-126">-輸送量</span><span class="sxs-lookup"><span data-stu-id="5e9d3-126">-Throughput</span></span>
<span data-ttu-id="5e9d3-127">Cassandra Keyspace (RU/秒的輸送量) 。</span><span class="sxs-lookup"><span data-stu-id="5e9d3-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="5e9d3-128">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="5e9d3-128">Default value is 400.</span></span>

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

### <span data-ttu-id="5e9d3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e9d3-129">-WhatIf</span></span>
<span data-ttu-id="5e9d3-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5e9d3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e9d3-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5e9d3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e9d3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e9d3-132">CommonParameters</span></span>
<span data-ttu-id="5e9d3-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e9d3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e9d3-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5e9d3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e9d3-135">輸入</span><span class="sxs-lookup"><span data-stu-id="5e9d3-135">INPUTS</span></span>

### <span data-ttu-id="5e9d3-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="5e9d3-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="5e9d3-137">輸出</span><span class="sxs-lookup"><span data-stu-id="5e9d3-137">OUTPUTS</span></span>

### <span data-ttu-id="5e9d3-138">PSCassandraKeyspaceGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="5e9d3-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="5e9d3-139">ConflictingResourceException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="5e9d3-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="5e9d3-140">筆記</span><span class="sxs-lookup"><span data-stu-id="5e9d3-140">NOTES</span></span>

## <span data-ttu-id="5e9d3-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e9d3-141">RELATED LINKS</span></span>