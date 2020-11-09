---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: e144e863ec0c9d55b14295486cdc4e94e26e8909
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285568"
---
# <span data-ttu-id="bf87f-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="bf87f-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="bf87f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf87f-102">SYNOPSIS</span></span>
<span data-ttu-id="bf87f-103">取得 CosmosDB Sql StoredProcedure。</span><span class="sxs-lookup"><span data-stu-id="bf87f-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="bf87f-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf87f-104">SYNTAX</span></span>

### <span data-ttu-id="bf87f-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf87f-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf87f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf87f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf87f-107">說明</span><span class="sxs-lookup"><span data-stu-id="bf87f-107">DESCRIPTION</span></span>
<span data-ttu-id="bf87f-108">**AzCosmosDBSqlStoredProcedure** Cmdlet 會取得特定 ResourceGroupName、Accountname、databasename 及的所有現有 CosmosDB sql StoredProcedures 清單，並針對特定的 CosmosDB、Accountname、databasename、和 StoredProcedure 取得單一的 ResourceGroupName sql StoredProcedureName。</span><span class="sxs-lookup"><span data-stu-id="bf87f-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="bf87f-109">示例</span><span class="sxs-lookup"><span data-stu-id="bf87f-109">EXAMPLES</span></span>

### <span data-ttu-id="bf87f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="bf87f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="bf87f-111">參數</span><span class="sxs-lookup"><span data-stu-id="bf87f-111">PARAMETERS</span></span>

### <span data-ttu-id="bf87f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bf87f-112">-AccountName</span></span>
<span data-ttu-id="bf87f-113">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf87f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bf87f-114">-容器</span><span class="sxs-lookup"><span data-stu-id="bf87f-114">-ContainerName</span></span>
<span data-ttu-id="bf87f-115">容器名稱。</span><span class="sxs-lookup"><span data-stu-id="bf87f-115">Container name.</span></span>

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

### <span data-ttu-id="bf87f-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bf87f-116">-DatabaseName</span></span>
<span data-ttu-id="bf87f-117">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="bf87f-117">Database name.</span></span>

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

### <span data-ttu-id="bf87f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf87f-118">-DefaultProfile</span></span>
<span data-ttu-id="bf87f-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf87f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf87f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="bf87f-120">-Name</span></span>
<span data-ttu-id="bf87f-121">儲存的 Prcodecure 名稱。</span><span class="sxs-lookup"><span data-stu-id="bf87f-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="bf87f-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bf87f-122">-ParentObject</span></span>
<span data-ttu-id="bf87f-123">Sql 容器物件。</span><span class="sxs-lookup"><span data-stu-id="bf87f-123">Sql Container object.</span></span>

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

### <span data-ttu-id="bf87f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf87f-124">-ResourceGroupName</span></span>
<span data-ttu-id="bf87f-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf87f-125">Name of resource group.</span></span>

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

### <span data-ttu-id="bf87f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf87f-126">CommonParameters</span></span>
<span data-ttu-id="bf87f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf87f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf87f-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bf87f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf87f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="bf87f-129">INPUTS</span></span>

### <span data-ttu-id="bf87f-130">所有</span><span class="sxs-lookup"><span data-stu-id="bf87f-130">None</span></span>

## <span data-ttu-id="bf87f-131">輸出</span><span class="sxs-lookup"><span data-stu-id="bf87f-131">OUTPUTS</span></span>

### <span data-ttu-id="bf87f-132">PSSqlStoredProcedureGetResults 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="bf87f-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="bf87f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="bf87f-133">NOTES</span></span>

## <span data-ttu-id="bf87f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf87f-134">RELATED LINKS</span></span>