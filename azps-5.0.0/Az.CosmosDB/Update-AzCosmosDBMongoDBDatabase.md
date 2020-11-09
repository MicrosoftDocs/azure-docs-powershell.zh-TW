---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: ed97687a03a40df8bbc965a21d7beb268cb67432
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285415"
---
# <span data-ttu-id="d8e3d-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="d8e3d-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="d8e3d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e3d-103">更新 CosmosDB MongoDB 資料庫。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="d8e3d-104">透過讀取現有的資料庫來執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="d8e3d-105">句法</span><span class="sxs-lookup"><span data-stu-id="d8e3d-105">SYNTAX</span></span>

### <span data-ttu-id="d8e3d-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d8e3d-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8e3d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8e3d-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8e3d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8e3d-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8e3d-109">說明</span><span class="sxs-lookup"><span data-stu-id="d8e3d-109">DESCRIPTION</span></span>
<span data-ttu-id="d8e3d-110">更新 CosmosDB MongoDB 資料庫。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="d8e3d-111">透過讀取現有的資料庫來執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="d8e3d-112">示例</span><span class="sxs-lookup"><span data-stu-id="d8e3d-112">EXAMPLES</span></span>

### <span data-ttu-id="d8e3d-113">範例1</span><span class="sxs-lookup"><span data-stu-id="d8e3d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="d8e3d-114">參數</span><span class="sxs-lookup"><span data-stu-id="d8e3d-114">PARAMETERS</span></span>

### <span data-ttu-id="d8e3d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d8e3d-115">-AccountName</span></span>
<span data-ttu-id="d8e3d-116">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d8e3d-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d8e3d-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d8e3d-118">啟用自動縮放時的最大輸送量值。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d8e3d-119">-確認</span><span class="sxs-lookup"><span data-stu-id="d8e3d-119">-Confirm</span></span>
<span data-ttu-id="d8e3d-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8e3d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e3d-121">-DefaultProfile</span></span>
<span data-ttu-id="d8e3d-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8e3d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8e3d-123">-InputObject</span></span>
<span data-ttu-id="d8e3d-124">Mongo 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-124">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e3d-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8e3d-125">-Name</span></span>
<span data-ttu-id="d8e3d-126">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-126">Database name.</span></span>

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

### <span data-ttu-id="d8e3d-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d8e3d-127">-ParentObject</span></span>
<span data-ttu-id="d8e3d-128">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="d8e3d-128">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e3d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e3d-129">-ResourceGroupName</span></span>
<span data-ttu-id="d8e3d-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-130">Name of resource group.</span></span>

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

### <span data-ttu-id="d8e3d-131">-輸送量</span><span class="sxs-lookup"><span data-stu-id="d8e3d-131">-Throughput</span></span>
<span data-ttu-id="d8e3d-132">Mongo 資料庫的輸送量 (RU/秒) 。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="d8e3d-133">預設值為400。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-133">Default value is 400.</span></span>

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

### <span data-ttu-id="d8e3d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8e3d-134">-WhatIf</span></span>
<span data-ttu-id="d8e3d-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8e3d-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8e3d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e3d-137">CommonParameters</span></span>
<span data-ttu-id="d8e3d-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e3d-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e3d-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d8e3d-140">INPUTS</span></span>

### <span data-ttu-id="d8e3d-141">所有</span><span class="sxs-lookup"><span data-stu-id="d8e3d-141">None</span></span>

## <span data-ttu-id="d8e3d-142">輸出</span><span class="sxs-lookup"><span data-stu-id="d8e3d-142">OUTPUTS</span></span>

### <span data-ttu-id="d8e3d-143">PSMongoDBDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="d8e3d-144">ResourceNotFoundException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="d8e3d-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="d8e3d-145">筆記</span><span class="sxs-lookup"><span data-stu-id="d8e3d-145">NOTES</span></span>

## <span data-ttu-id="d8e3d-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8e3d-146">RELATED LINKS</span></span>