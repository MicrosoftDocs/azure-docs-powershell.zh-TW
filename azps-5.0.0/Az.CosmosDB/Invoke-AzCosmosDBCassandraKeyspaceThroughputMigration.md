---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: a5e636f37b032411069b3e6c9a85226eb751705e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285555"
---
# <span data-ttu-id="dab7c-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="dab7c-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="dab7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dab7c-102">SYNOPSIS</span></span>
<span data-ttu-id="dab7c-103">使用此操作可將自動縮放輸送量遷移成手動輸送量，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="dab7c-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="dab7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="dab7c-104">SYNTAX</span></span>

### <span data-ttu-id="dab7c-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dab7c-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dab7c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dab7c-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dab7c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dab7c-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dab7c-108">說明</span><span class="sxs-lookup"><span data-stu-id="dab7c-108">DESCRIPTION</span></span>
<span data-ttu-id="dab7c-109">ThroughpyteType 參數定義您想要將哪些輸送量遷移至。</span><span class="sxs-lookup"><span data-stu-id="dab7c-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="dab7c-110">示例</span><span class="sxs-lookup"><span data-stu-id="dab7c-110">EXAMPLES</span></span>

### <span data-ttu-id="dab7c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="dab7c-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="dab7c-112">參數</span><span class="sxs-lookup"><span data-stu-id="dab7c-112">PARAMETERS</span></span>

### <span data-ttu-id="dab7c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dab7c-113">-AccountName</span></span>
<span data-ttu-id="dab7c-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="dab7c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dab7c-115">-確認</span><span class="sxs-lookup"><span data-stu-id="dab7c-115">-Confirm</span></span>
<span data-ttu-id="dab7c-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dab7c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dab7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dab7c-117">-DefaultProfile</span></span>
<span data-ttu-id="dab7c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dab7c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dab7c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dab7c-119">-InputObject</span></span>
<span data-ttu-id="dab7c-120">Cassandra Keyspace 物件。</span><span class="sxs-lookup"><span data-stu-id="dab7c-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dab7c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="dab7c-121">-Name</span></span>
<span data-ttu-id="dab7c-122">Cassandra Keyspace Name。</span><span class="sxs-lookup"><span data-stu-id="dab7c-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="dab7c-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dab7c-123">-ParentObject</span></span>
<span data-ttu-id="dab7c-124">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="dab7c-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="dab7c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dab7c-125">-ResourceGroupName</span></span>
<span data-ttu-id="dab7c-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dab7c-126">Name of resource group.</span></span>

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

### <span data-ttu-id="dab7c-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="dab7c-127">-ThroughputType</span></span>
<span data-ttu-id="dab7c-128">要遷移到的輸送量類型。</span><span class="sxs-lookup"><span data-stu-id="dab7c-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="dab7c-129">可能的值為：自動縮放、手動。</span><span class="sxs-lookup"><span data-stu-id="dab7c-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="dab7c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dab7c-130">-WhatIf</span></span>
<span data-ttu-id="dab7c-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dab7c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dab7c-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dab7c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dab7c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dab7c-133">CommonParameters</span></span>
<span data-ttu-id="dab7c-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dab7c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dab7c-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dab7c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dab7c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="dab7c-136">INPUTS</span></span>

### <span data-ttu-id="dab7c-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="dab7c-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="dab7c-138">PSCassandraKeyspaceGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="dab7c-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="dab7c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="dab7c-139">OUTPUTS</span></span>

### <span data-ttu-id="dab7c-140">PSThroughputSettingsGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="dab7c-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="dab7c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="dab7c-141">NOTES</span></span>

## <span data-ttu-id="dab7c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="dab7c-142">RELATED LINKS</span></span>