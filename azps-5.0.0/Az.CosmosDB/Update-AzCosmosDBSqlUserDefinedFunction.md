---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285398"
---
# <span data-ttu-id="0dc9e-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="0dc9e-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="0dc9e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0dc9e-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc9e-103">更新 CosmosDB Sql UserDefinedFunction。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="0dc9e-104">讀取現有的 UserDefinedFunction，以執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="0dc9e-105">句法</span><span class="sxs-lookup"><span data-stu-id="0dc9e-105">SYNTAX</span></span>

### <span data-ttu-id="0dc9e-106">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0dc9e-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dc9e-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc9e-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0dc9e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc9e-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dc9e-109">說明</span><span class="sxs-lookup"><span data-stu-id="0dc9e-109">DESCRIPTION</span></span>
<span data-ttu-id="0dc9e-110">更新 CosmosDB Sql UserDefinedFunction。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="0dc9e-111">讀取現有的 UserDefinedFunction，以執行用戶端的修補程式操作。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="0dc9e-112">示例</span><span class="sxs-lookup"><span data-stu-id="0dc9e-112">EXAMPLES</span></span>

### <span data-ttu-id="0dc9e-113">範例1</span><span class="sxs-lookup"><span data-stu-id="0dc9e-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="0dc9e-114">參數</span><span class="sxs-lookup"><span data-stu-id="0dc9e-114">PARAMETERS</span></span>

### <span data-ttu-id="0dc9e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0dc9e-115">-AccountName</span></span>
<span data-ttu-id="0dc9e-116">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0dc9e-117">-Body</span><span class="sxs-lookup"><span data-stu-id="0dc9e-117">-Body</span></span>
<span data-ttu-id="0dc9e-118">使用者定義函數的主體。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="0dc9e-119">-確認</span><span class="sxs-lookup"><span data-stu-id="0dc9e-119">-Confirm</span></span>
<span data-ttu-id="0dc9e-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dc9e-121">-容器</span><span class="sxs-lookup"><span data-stu-id="0dc9e-121">-ContainerName</span></span>
<span data-ttu-id="0dc9e-122">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-122">Container name.</span></span>

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

### <span data-ttu-id="0dc9e-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0dc9e-123">-DatabaseName</span></span>
<span data-ttu-id="0dc9e-124">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-124">Database name.</span></span>

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

### <span data-ttu-id="0dc9e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc9e-125">-DefaultProfile</span></span>
<span data-ttu-id="0dc9e-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dc9e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0dc9e-127">-InputObject</span></span>
<span data-ttu-id="0dc9e-128">Sql 使用者定義函數物件</span><span class="sxs-lookup"><span data-stu-id="0dc9e-128">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc9e-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="0dc9e-129">-Name</span></span>
<span data-ttu-id="0dc9e-130">使用者定義的函數名稱。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="0dc9e-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0dc9e-131">-ParentObject</span></span>
<span data-ttu-id="0dc9e-132">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-132">Sql Container object.</span></span>

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

### <span data-ttu-id="0dc9e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc9e-133">-ResourceGroupName</span></span>
<span data-ttu-id="0dc9e-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-134">Name of resource group.</span></span>

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

### <span data-ttu-id="0dc9e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dc9e-135">-WhatIf</span></span>
<span data-ttu-id="0dc9e-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dc9e-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dc9e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc9e-138">CommonParameters</span></span>
<span data-ttu-id="0dc9e-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc9e-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc9e-141">輸入</span><span class="sxs-lookup"><span data-stu-id="0dc9e-141">INPUTS</span></span>

### <span data-ttu-id="0dc9e-142">PSSqlContainerGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="0dc9e-143">PSSqlUserDefinedFunctionGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="0dc9e-144">輸出</span><span class="sxs-lookup"><span data-stu-id="0dc9e-144">OUTPUTS</span></span>

### <span data-ttu-id="0dc9e-145">PSSqlUserDefinedFunctionGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="0dc9e-146">ResourceNotFoundException 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="0dc9e-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="0dc9e-147">筆記</span><span class="sxs-lookup"><span data-stu-id="0dc9e-147">NOTES</span></span>

## <span data-ttu-id="0dc9e-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="0dc9e-148">RELATED LINKS</span></span>