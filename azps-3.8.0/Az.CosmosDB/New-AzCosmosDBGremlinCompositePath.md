---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlincompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
ms.openlocfilehash: 612f4623c7944c3c3d930ece44d4c2ae938e1a68
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956854"
---
# <span data-ttu-id="b50f7-101">New-AzCosmosDBGremlinCompositePath</span><span class="sxs-lookup"><span data-stu-id="b50f7-101">New-AzCosmosDBGremlinCompositePath</span></span>

## <span data-ttu-id="b50f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b50f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b50f7-103">建立 PSCompositePath 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="b50f7-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="b50f7-104">您可以將它作為 AzCosmosDBGremlinGraph 的參數值來傳遞。</span><span class="sxs-lookup"><span data-stu-id="b50f7-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="b50f7-105">句法</span><span class="sxs-lookup"><span data-stu-id="b50f7-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinCompositePath [-Path <String>] [-Order <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b50f7-106">說明</span><span class="sxs-lookup"><span data-stu-id="b50f7-106">DESCRIPTION</span></span>
<span data-ttu-id="b50f7-107">對應至 Gremlin API CompositePath 的物件。</span><span class="sxs-lookup"><span data-stu-id="b50f7-107">Object corresponding to Gremlin API's CompositePath.</span></span>

## <span data-ttu-id="b50f7-108">示例</span><span class="sxs-lookup"><span data-stu-id="b50f7-108">EXAMPLES</span></span>

### <span data-ttu-id="b50f7-109">範例1</span><span class="sxs-lookup"><span data-stu-id="b50f7-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="b50f7-110">參數</span><span class="sxs-lookup"><span data-stu-id="b50f7-110">PARAMETERS</span></span>

### <span data-ttu-id="b50f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b50f7-111">-DefaultProfile</span></span>
<span data-ttu-id="b50f7-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b50f7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b50f7-113">-訂單</span><span class="sxs-lookup"><span data-stu-id="b50f7-113">-Order</span></span>
<span data-ttu-id="b50f7-114">取得或設定複合路徑的排序次序。</span><span class="sxs-lookup"><span data-stu-id="b50f7-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="b50f7-115">可能的值包括： [昇冪]、"遞減"</span><span class="sxs-lookup"><span data-stu-id="b50f7-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="b50f7-116">-Path</span><span class="sxs-lookup"><span data-stu-id="b50f7-116">-Path</span></span>
<span data-ttu-id="b50f7-117">要套用索引行為的路徑。</span><span class="sxs-lookup"><span data-stu-id="b50f7-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="b50f7-118">索引路徑通常是從 root 開始，並以萬用字元 (/path/\* ) </span><span class="sxs-lookup"><span data-stu-id="b50f7-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="b50f7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b50f7-119">CommonParameters</span></span>
<span data-ttu-id="b50f7-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b50f7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b50f7-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b50f7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b50f7-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b50f7-122">INPUTS</span></span>

### <span data-ttu-id="b50f7-123">所有</span><span class="sxs-lookup"><span data-stu-id="b50f7-123">None</span></span>

## <span data-ttu-id="b50f7-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b50f7-124">OUTPUTS</span></span>

### <span data-ttu-id="b50f7-125">PSCompositePath 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="b50f7-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="b50f7-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b50f7-126">NOTES</span></span>

## <span data-ttu-id="b50f7-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="b50f7-127">RELATED LINKS</span></span>