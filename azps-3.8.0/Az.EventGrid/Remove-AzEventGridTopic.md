---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: 550668a6ae5b1a7f870410961d32f9b53d4947a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956878"
---
# <span data-ttu-id="8c1f1-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="8c1f1-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="8c1f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c1f1-102">SYNOPSIS</span></span>
<span data-ttu-id="8c1f1-103">移除 Azure 事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="8c1f1-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="8c1f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c1f1-104">SYNTAX</span></span>

### <span data-ttu-id="8c1f1-105">TopicNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8c1f1-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c1f1-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c1f1-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c1f1-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c1f1-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c1f1-108">說明</span><span class="sxs-lookup"><span data-stu-id="8c1f1-108">DESCRIPTION</span></span>
<span data-ttu-id="8c1f1-109">移除 Azure 事件格線主題。</span><span class="sxs-lookup"><span data-stu-id="8c1f1-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="8c1f1-110">示例</span><span class="sxs-lookup"><span data-stu-id="8c1f1-110">EXAMPLES</span></span>

### <span data-ttu-id="8c1f1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8c1f1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="8c1f1-112">移除 [ \` \` 資源] 群組 MyResourceGroupName 中的事件格線主題 Topic1 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="8c1f1-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8c1f1-113">範例2</span><span class="sxs-lookup"><span data-stu-id="8c1f1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="8c1f1-114">移除 [ \` \` 資源] 群組 MyResourceGroupName 中的事件格線主題 Topic1 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="8c1f1-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="8c1f1-115">參數</span><span class="sxs-lookup"><span data-stu-id="8c1f1-115">PARAMETERS</span></span>

### <span data-ttu-id="8c1f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c1f1-116">-DefaultProfile</span></span>
<span data-ttu-id="8c1f1-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8c1f1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c1f1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c1f1-118">-InputObject</span></span>
<span data-ttu-id="8c1f1-119">EventGrid 主題物件。</span><span class="sxs-lookup"><span data-stu-id="8c1f1-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f1-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c1f1-120">-Name</span></span>
<span data-ttu-id="8c1f1-121">EventGrid 主題名稱。</span><span class="sxs-lookup"><span data-stu-id="8c1f1-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c1f1-122">-PassThru</span></span>
<span data-ttu-id="8c1f1-123">傳回移除操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="8c1f1-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="8c1f1-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8c1f1-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8c1f1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c1f1-125">-ResourceGroupName</span></span>
<span data-ttu-id="8c1f1-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8c1f1-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c1f1-127">-ResourceId</span></span>
<span data-ttu-id="8c1f1-128">EventGrid 主題 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="8c1f1-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="8c1f1-129">-確認</span><span class="sxs-lookup"><span data-stu-id="8c1f1-129">-Confirm</span></span>
<span data-ttu-id="8c1f1-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c1f1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c1f1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c1f1-131">-WhatIf</span></span>
<span data-ttu-id="8c1f1-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c1f1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c1f1-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c1f1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c1f1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c1f1-134">CommonParameters</span></span>
<span data-ttu-id="8c1f1-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c1f1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c1f1-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c1f1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c1f1-137">輸入</span><span class="sxs-lookup"><span data-stu-id="8c1f1-137">INPUTS</span></span>

### <span data-ttu-id="8c1f1-138">System.object</span><span class="sxs-lookup"><span data-stu-id="8c1f1-138">System.String</span></span>

### <span data-ttu-id="8c1f1-139">PSTopic 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="8c1f1-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="8c1f1-140">輸出</span><span class="sxs-lookup"><span data-stu-id="8c1f1-140">OUTPUTS</span></span>

### <span data-ttu-id="8c1f1-141">System.object</span><span class="sxs-lookup"><span data-stu-id="8c1f1-141">System.Boolean</span></span>

## <span data-ttu-id="8c1f1-142">筆記</span><span class="sxs-lookup"><span data-stu-id="8c1f1-142">NOTES</span></span>

## <span data-ttu-id="8c1f1-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c1f1-143">RELATED LINKS</span></span>