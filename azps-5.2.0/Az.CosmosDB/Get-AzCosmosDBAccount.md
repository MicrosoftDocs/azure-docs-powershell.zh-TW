---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 5c6dffe65022fa0282ab53bb04efe651ec123c2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275771"
---
# <span data-ttu-id="71cab-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="71cab-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="71cab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71cab-102">SYNOPSIS</span></span>
<span data-ttu-id="71cab-103">取得 CosmosDB 帳戶。</span><span class="sxs-lookup"><span data-stu-id="71cab-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="71cab-104">句法</span><span class="sxs-lookup"><span data-stu-id="71cab-104">SYNTAX</span></span>

### <span data-ttu-id="71cab-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="71cab-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71cab-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71cab-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71cab-107">說明</span><span class="sxs-lookup"><span data-stu-id="71cab-107">DESCRIPTION</span></span>
<span data-ttu-id="71cab-108">**AzCosmosDBAccount** Cmdlet 會取得指定 ResourceGroupName 之所有現有 CosmosDB 帳戶的清單，並取得指定 ResourceGroupName 和 AccountName 的單一 CosmosDB 帳戶。</span><span class="sxs-lookup"><span data-stu-id="71cab-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="71cab-109">示例</span><span class="sxs-lookup"><span data-stu-id="71cab-109">EXAMPLES</span></span>

### <span data-ttu-id="71cab-110">範例1</span><span class="sxs-lookup"><span data-stu-id="71cab-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBAccount -ResourceGroupName {resourceGroupName} -Name {databaseAccountName}


Id                            : /subscriptions/{subscriptionid}/resourceGroups/{resourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{databaseAccountName}
Name                          : {databaseAccountName}
FailoverPolicies              : {databaseAccountName-region1}
ReadLocations                 : {databaseAccountName-region1}
WriteLocations                : {databaseAccountName-region1}
Capabilities                  : {}
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
EnableAutomaticFailover       : False
IsVirtualNetworkFilterEnabled : False
IpRangeFilter                 :
DatabaseAccountOfferType      : Standard
DocumentEndpoint              : https://databaseAccountName.documents.azure.com:443/
ProvisioningState             : Succeeded
Kind                          : GlobalDocumentDB
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
```

<span data-ttu-id="71cab-111">在 ResourceGroup resourceGroupName 中取得 name databaseAccountName 的 CosmosDB 資料庫帳戶。</span><span class="sxs-lookup"><span data-stu-id="71cab-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="71cab-112">參數</span><span class="sxs-lookup"><span data-stu-id="71cab-112">PARAMETERS</span></span>

### <span data-ttu-id="71cab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71cab-113">-DefaultProfile</span></span>
<span data-ttu-id="71cab-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71cab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71cab-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="71cab-115">-Name</span></span>
<span data-ttu-id="71cab-116">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="71cab-116">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71cab-117">-ResourceGroupName</span></span>
<span data-ttu-id="71cab-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="71cab-118">Name of resource group.</span></span>

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

### <span data-ttu-id="71cab-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71cab-119">-ResourceId</span></span>
<span data-ttu-id="71cab-120">資源的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="71cab-120">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71cab-121">CommonParameters</span></span>
<span data-ttu-id="71cab-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71cab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71cab-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="71cab-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71cab-124">輸入</span><span class="sxs-lookup"><span data-stu-id="71cab-124">INPUTS</span></span>

### <span data-ttu-id="71cab-125">所有</span><span class="sxs-lookup"><span data-stu-id="71cab-125">None</span></span>

## <span data-ttu-id="71cab-126">輸出</span><span class="sxs-lookup"><span data-stu-id="71cab-126">OUTPUTS</span></span>

### <span data-ttu-id="71cab-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="71cab-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="71cab-128">筆記</span><span class="sxs-lookup"><span data-stu-id="71cab-128">NOTES</span></span>

## <span data-ttu-id="71cab-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="71cab-129">RELATED LINKS</span></span>