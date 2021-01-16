---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285132"
---
# <span data-ttu-id="6860f-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="6860f-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="6860f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6860f-102">SYNOPSIS</span></span>
<span data-ttu-id="6860f-103">更新 CosmosDB Sql StoredProcedure。</span><span class="sxs-lookup"><span data-stu-id="6860f-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="6860f-104">讀取現有的 StoredProcedure，以執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="6860f-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="6860f-105">句法</span><span class="sxs-lookup"><span data-stu-id="6860f-105">SYNTAX</span></span>

### <span data-ttu-id="6860f-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6860f-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6860f-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6860f-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6860f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6860f-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6860f-109">說明</span><span class="sxs-lookup"><span data-stu-id="6860f-109">DESCRIPTION</span></span>
<span data-ttu-id="6860f-110">更新 CosmosDB Sql StoredProcedure。</span><span class="sxs-lookup"><span data-stu-id="6860f-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="6860f-111">讀取現有的 StoredProcedure，以執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="6860f-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="6860f-112">示例</span><span class="sxs-lookup"><span data-stu-id="6860f-112">EXAMPLES</span></span>

### <span data-ttu-id="6860f-113">範例1</span><span class="sxs-lookup"><span data-stu-id="6860f-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="6860f-114">參數</span><span class="sxs-lookup"><span data-stu-id="6860f-114">PARAMETERS</span></span>

### <span data-ttu-id="6860f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6860f-115">-AccountName</span></span>
<span data-ttu-id="6860f-116">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="6860f-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6860f-117">-Body</span><span class="sxs-lookup"><span data-stu-id="6860f-117">-Body</span></span>
<span data-ttu-id="6860f-118">已儲存程式的內文。</span><span class="sxs-lookup"><span data-stu-id="6860f-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="6860f-119">-確認</span><span class="sxs-lookup"><span data-stu-id="6860f-119">-Confirm</span></span>
<span data-ttu-id="6860f-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6860f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6860f-121">-容器</span><span class="sxs-lookup"><span data-stu-id="6860f-121">-ContainerName</span></span>
<span data-ttu-id="6860f-122">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="6860f-122">Container name.</span></span>

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

### <span data-ttu-id="6860f-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6860f-123">-DatabaseName</span></span>
<span data-ttu-id="6860f-124">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="6860f-124">Database name.</span></span>

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

### <span data-ttu-id="6860f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6860f-125">-DefaultProfile</span></span>
<span data-ttu-id="6860f-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6860f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6860f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6860f-127">-InputObject</span></span>
<span data-ttu-id="6860f-128">Sql 儲存過程物件</span><span class="sxs-lookup"><span data-stu-id="6860f-128">Sql Stored Procedure Object</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6860f-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="6860f-129">-Name</span></span>
<span data-ttu-id="6860f-130">儲存的 Prcodecure 名稱。</span><span class="sxs-lookup"><span data-stu-id="6860f-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="6860f-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6860f-131">-ParentObject</span></span>
<span data-ttu-id="6860f-132">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="6860f-132">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6860f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6860f-133">-ResourceGroupName</span></span>
<span data-ttu-id="6860f-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6860f-134">Name of resource group.</span></span>

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

### <span data-ttu-id="6860f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6860f-135">-WhatIf</span></span>
<span data-ttu-id="6860f-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6860f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6860f-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6860f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6860f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6860f-138">CommonParameters</span></span>
<span data-ttu-id="6860f-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6860f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6860f-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6860f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6860f-141">輸入</span><span class="sxs-lookup"><span data-stu-id="6860f-141">INPUTS</span></span>

### <span data-ttu-id="6860f-142">PSSqlContainerGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="6860f-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="6860f-143">PSSqlStoredProcedureGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="6860f-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="6860f-144">輸出</span><span class="sxs-lookup"><span data-stu-id="6860f-144">OUTPUTS</span></span>

### <span data-ttu-id="6860f-145">PSSqlStoredProcedureGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="6860f-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="6860f-146">ResourceNotFoundException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="6860f-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="6860f-147">筆記</span><span class="sxs-lookup"><span data-stu-id="6860f-147">NOTES</span></span>

## <span data-ttu-id="6860f-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="6860f-148">RELATED LINKS</span></span>