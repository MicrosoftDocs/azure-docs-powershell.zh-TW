---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: e4329c0d3ad4499af1174458ea3e0449672774a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959425"
---
# <span data-ttu-id="8603d-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8603d-101">Set-AzSearchService</span></span>

## <span data-ttu-id="8603d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8603d-102">SYNOPSIS</span></span>
<span data-ttu-id="8603d-103">更新 Azure 搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="8603d-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="8603d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8603d-104">SYNTAX</span></span>

### <span data-ttu-id="8603d-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8603d-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8603d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8603d-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8603d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8603d-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8603d-108">說明</span><span class="sxs-lookup"><span data-stu-id="8603d-108">DESCRIPTION</span></span>
<span data-ttu-id="8603d-109">**AzSearchService** Cmdlet 會修改 Azure 搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="8603d-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="8603d-110">示例</span><span class="sxs-lookup"><span data-stu-id="8603d-110">EXAMPLES</span></span>

### <span data-ttu-id="8603d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8603d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="8603d-112">這個範例會將 Azure 搜尋服務的 [分區計數] 和 [複本計數] 變更為 [2]。</span><span class="sxs-lookup"><span data-stu-id="8603d-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="8603d-113">參數</span><span class="sxs-lookup"><span data-stu-id="8603d-113">PARAMETERS</span></span>

### <span data-ttu-id="8603d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8603d-114">-DefaultProfile</span></span>
<span data-ttu-id="8603d-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8603d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8603d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8603d-116">-InputObject</span></span>
<span data-ttu-id="8603d-117">搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="8603d-117">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8603d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="8603d-118">-Name</span></span>
<span data-ttu-id="8603d-119">搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="8603d-119">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8603d-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="8603d-120">-PartitionCount</span></span>
<span data-ttu-id="8603d-121">搜尋服務分區計數。</span><span class="sxs-lookup"><span data-stu-id="8603d-121">Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8603d-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="8603d-122">-ReplicaCount</span></span>
<span data-ttu-id="8603d-123">搜尋服務複本計數。</span><span class="sxs-lookup"><span data-stu-id="8603d-123">Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8603d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8603d-124">-ResourceGroupName</span></span>
<span data-ttu-id="8603d-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8603d-125">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8603d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8603d-126">-ResourceId</span></span>
<span data-ttu-id="8603d-127">搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8603d-127">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8603d-128">-確認</span><span class="sxs-lookup"><span data-stu-id="8603d-128">-Confirm</span></span>
<span data-ttu-id="8603d-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8603d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8603d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8603d-130">-WhatIf</span></span>
<span data-ttu-id="8603d-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8603d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8603d-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8603d-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8603d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8603d-133">CommonParameters</span></span>
<span data-ttu-id="8603d-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8603d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8603d-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8603d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8603d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8603d-136">INPUTS</span></span>

### <span data-ttu-id="8603d-137">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="8603d-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="8603d-138">System.object</span><span class="sxs-lookup"><span data-stu-id="8603d-138">System.String</span></span>

## <span data-ttu-id="8603d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="8603d-139">OUTPUTS</span></span>

### <span data-ttu-id="8603d-140">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="8603d-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="8603d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="8603d-141">NOTES</span></span>

## <span data-ttu-id="8603d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="8603d-142">RELATED LINKS</span></span>

[<span data-ttu-id="8603d-143">新-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8603d-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="8603d-144">AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8603d-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="8603d-145">移除-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8603d-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)