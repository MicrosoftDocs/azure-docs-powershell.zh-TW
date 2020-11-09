---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 6f2490eee06ab9cded7634fec1c938d40b4feb50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285455"
---
# <span data-ttu-id="589eb-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="589eb-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="589eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="589eb-102">SYNOPSIS</span></span>
<span data-ttu-id="589eb-103">刪除 CosmosDB MongoDB 資料庫。</span><span class="sxs-lookup"><span data-stu-id="589eb-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="589eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="589eb-104">SYNTAX</span></span>

### <span data-ttu-id="589eb-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="589eb-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="589eb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="589eb-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="589eb-107">說明</span><span class="sxs-lookup"><span data-stu-id="589eb-107">DESCRIPTION</span></span>
<span data-ttu-id="589eb-108">**AzCosmosDBMongoDBDatabase** Cmdlet 會刪除 CosmosDB MongoDB 資料庫。</span><span class="sxs-lookup"><span data-stu-id="589eb-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="589eb-109">示例</span><span class="sxs-lookup"><span data-stu-id="589eb-109">EXAMPLES</span></span>

### <span data-ttu-id="589eb-110">範例1</span><span class="sxs-lookup"><span data-stu-id="589eb-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="589eb-111">如果刪除成功，則此 Cmdlet 會) 傳回類型為 bool (的物件。</span><span class="sxs-lookup"><span data-stu-id="589eb-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="589eb-112">參數</span><span class="sxs-lookup"><span data-stu-id="589eb-112">PARAMETERS</span></span>

### <span data-ttu-id="589eb-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="589eb-113">-AccountName</span></span>
<span data-ttu-id="589eb-114">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="589eb-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="589eb-115">-確認</span><span class="sxs-lookup"><span data-stu-id="589eb-115">-Confirm</span></span>
<span data-ttu-id="589eb-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="589eb-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="589eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="589eb-117">-DefaultProfile</span></span>
<span data-ttu-id="589eb-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="589eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="589eb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="589eb-119">-InputObject</span></span>
<span data-ttu-id="589eb-120">Mongo 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="589eb-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="589eb-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="589eb-121">-Name</span></span>
<span data-ttu-id="589eb-122">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="589eb-122">Database name.</span></span>

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

### <span data-ttu-id="589eb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="589eb-123">-PassThru</span></span>
<span data-ttu-id="589eb-124">如果使用者想要接收輸出，則設為 true。</span><span class="sxs-lookup"><span data-stu-id="589eb-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="589eb-125">如果操作成功，則輸出為 true，否則會拋回錯誤。</span><span class="sxs-lookup"><span data-stu-id="589eb-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="589eb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="589eb-126">-ResourceGroupName</span></span>
<span data-ttu-id="589eb-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="589eb-127">Name of resource group.</span></span>

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

### <span data-ttu-id="589eb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="589eb-128">-WhatIf</span></span>
<span data-ttu-id="589eb-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="589eb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="589eb-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="589eb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="589eb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="589eb-131">CommonParameters</span></span>
<span data-ttu-id="589eb-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="589eb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="589eb-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="589eb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="589eb-134">輸入</span><span class="sxs-lookup"><span data-stu-id="589eb-134">INPUTS</span></span>

### <span data-ttu-id="589eb-135">PSMongoDBDatabaseGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="589eb-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="589eb-136">輸出</span><span class="sxs-lookup"><span data-stu-id="589eb-136">OUTPUTS</span></span>

### <span data-ttu-id="589eb-137">System.void</span><span class="sxs-lookup"><span data-stu-id="589eb-137">System.Void</span></span>

### <span data-ttu-id="589eb-138">System.object</span><span class="sxs-lookup"><span data-stu-id="589eb-138">System.Boolean</span></span>

## <span data-ttu-id="589eb-139">筆記</span><span class="sxs-lookup"><span data-stu-id="589eb-139">NOTES</span></span>

## <span data-ttu-id="589eb-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="589eb-140">RELATED LINKS</span></span>