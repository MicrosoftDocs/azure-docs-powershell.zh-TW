---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: d72c7e1ebfdd7543740ea8fafeb62861f4394093
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287215"
---
# <span data-ttu-id="f5564-101">Remove-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f5564-101">Remove-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="f5564-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5564-102">SYNOPSIS</span></span>
<span data-ttu-id="f5564-103">移除命名空間 NetworkRuleSet 的單一指定 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f5564-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="f5564-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5564-104">SYNTAX</span></span>

### <span data-ttu-id="f5564-105">VirtualNetworkRulePropertiesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f5564-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5564-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5564-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5564-107">說明</span><span class="sxs-lookup"><span data-stu-id="f5564-107">DESCRIPTION</span></span>
<span data-ttu-id="f5564-108">移除命名空間 NetworkRuleSet 的單一指定 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f5564-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="f5564-109">示例</span><span class="sxs-lookup"><span data-stu-id="f5564-109">EXAMPLES</span></span>

### <span data-ttu-id="f5564-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f5564-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="f5564-111">移除命名空間 NetworkRuleSet 的單一指定 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f5564-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="f5564-112">範例2</span><span class="sxs-lookup"><span data-stu-id="f5564-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="f5564-113">移除指定命名空間的 $virtualruleset NetworkRuleSet 1</span><span class="sxs-lookup"><span data-stu-id="f5564-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="f5564-114">參數</span><span class="sxs-lookup"><span data-stu-id="f5564-114">PARAMETERS</span></span>

### <span data-ttu-id="f5564-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5564-115">-AsJob</span></span>
<span data-ttu-id="f5564-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5564-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5564-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5564-117">-DefaultProfile</span></span>
<span data-ttu-id="f5564-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5564-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5564-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5564-119">-Name</span></span>
<span data-ttu-id="f5564-120">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="f5564-120">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5564-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5564-121">-PassThru</span></span>
<span data-ttu-id="f5564-122">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="f5564-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f5564-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5564-123">-ResourceGroupName</span></span>
<span data-ttu-id="f5564-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f5564-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5564-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f5564-125">-SubnetId</span></span>
<span data-ttu-id="f5564-126">子網資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f5564-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5564-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="f5564-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="f5564-128">IPRule Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="f5564-128">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5564-129">-確認</span><span class="sxs-lookup"><span data-stu-id="f5564-129">-Confirm</span></span>
<span data-ttu-id="f5564-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f5564-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5564-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5564-131">-WhatIf</span></span>
<span data-ttu-id="f5564-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5564-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5564-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5564-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5564-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5564-134">CommonParameters</span></span>
<span data-ttu-id="f5564-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5564-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f5564-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5564-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5564-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f5564-137">INPUTS</span></span>

### <span data-ttu-id="f5564-138">System.object</span><span class="sxs-lookup"><span data-stu-id="f5564-138">System.String</span></span>

### <span data-ttu-id="f5564-139">PSNWRuleSetVirtualNetworkRulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f5564-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="f5564-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f5564-140">OUTPUTS</span></span>

### <span data-ttu-id="f5564-141">PSNetworkRuleSetAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f5564-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="f5564-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f5564-142">NOTES</span></span>

## <span data-ttu-id="f5564-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5564-143">RELATED LINKS</span></span>