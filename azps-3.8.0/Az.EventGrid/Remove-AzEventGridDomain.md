---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 2eb9fc2575af16f6f0bc2d6e239f63d95a0c27d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957371"
---
# <span data-ttu-id="9c4c0-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="9c4c0-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="9c4c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c4c0-102">SYNOPSIS</span></span>
<span data-ttu-id="9c4c0-103">移除 Azure 事件格線網域。</span><span class="sxs-lookup"><span data-stu-id="9c4c0-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="9c4c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c4c0-104">SYNTAX</span></span>

### <span data-ttu-id="9c4c0-105">DomainNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9c4c0-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c4c0-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c4c0-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c4c0-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c4c0-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c4c0-108">說明</span><span class="sxs-lookup"><span data-stu-id="9c4c0-108">DESCRIPTION</span></span>
<span data-ttu-id="9c4c0-109">移除 Azure 事件格線網域。</span><span class="sxs-lookup"><span data-stu-id="9c4c0-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="9c4c0-110">示例</span><span class="sxs-lookup"><span data-stu-id="9c4c0-110">EXAMPLES</span></span>

### <span data-ttu-id="9c4c0-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9c4c0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="9c4c0-112">移除 [ \` \` 資源群組 MyResourceGroupName] 中的事件網格網域 Domain1 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="9c4c0-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="9c4c0-113">範例2</span><span class="sxs-lookup"><span data-stu-id="9c4c0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="9c4c0-114">移除 [ \` \` 資源群組 MyResourceGroupName] 中的事件網格網域 Domain1 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="9c4c0-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="9c4c0-115">參數</span><span class="sxs-lookup"><span data-stu-id="9c4c0-115">PARAMETERS</span></span>

### <span data-ttu-id="9c4c0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c4c0-116">-DefaultProfile</span></span>
<span data-ttu-id="9c4c0-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c4c0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c4c0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c4c0-118">-InputObject</span></span>
<span data-ttu-id="9c4c0-119">EventGrid Domain 物件。</span><span class="sxs-lookup"><span data-stu-id="9c4c0-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4c0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="9c4c0-120">-Name</span></span>
<span data-ttu-id="9c4c0-121">EventGrid [功能變數名稱]。</span><span class="sxs-lookup"><span data-stu-id="9c4c0-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4c0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c4c0-122">-PassThru</span></span>
<span data-ttu-id="9c4c0-123">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="9c4c0-123">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4c0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c4c0-124">-ResourceGroupName</span></span>
<span data-ttu-id="9c4c0-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c4c0-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4c0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c4c0-126">-ResourceId</span></span>
<span data-ttu-id="9c4c0-127">代表事件網格網域的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c4c0-127">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4c0-128">-確認</span><span class="sxs-lookup"><span data-stu-id="9c4c0-128">-Confirm</span></span>
<span data-ttu-id="9c4c0-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9c4c0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c4c0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c4c0-130">-WhatIf</span></span>
<span data-ttu-id="9c4c0-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9c4c0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c4c0-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c4c0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c4c0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c4c0-133">CommonParameters</span></span>
<span data-ttu-id="9c4c0-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c4c0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c4c0-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9c4c0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c4c0-136">輸入</span><span class="sxs-lookup"><span data-stu-id="9c4c0-136">INPUTS</span></span>

### <span data-ttu-id="9c4c0-137">System.object</span><span class="sxs-lookup"><span data-stu-id="9c4c0-137">System.String</span></span>

### <span data-ttu-id="9c4c0-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="9c4c0-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="9c4c0-139">輸出</span><span class="sxs-lookup"><span data-stu-id="9c4c0-139">OUTPUTS</span></span>

### <span data-ttu-id="9c4c0-140">System.object</span><span class="sxs-lookup"><span data-stu-id="9c4c0-140">System.Boolean</span></span>

## <span data-ttu-id="9c4c0-141">筆記</span><span class="sxs-lookup"><span data-stu-id="9c4c0-141">NOTES</span></span>

## <span data-ttu-id="9c4c0-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c4c0-142">RELATED LINKS</span></span>