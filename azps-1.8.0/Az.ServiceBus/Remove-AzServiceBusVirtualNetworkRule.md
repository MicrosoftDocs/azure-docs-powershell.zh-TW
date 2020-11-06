---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: 146c6157163209fabb8472ef7602d223bb344530
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620600"
---
# <span data-ttu-id="13824-101">Remove-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="13824-101">Remove-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="13824-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13824-102">SYNOPSIS</span></span>
<span data-ttu-id="13824-103">移除命名空間 NetworkRuleSet 的單一指定 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="13824-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="13824-104">句法</span><span class="sxs-lookup"><span data-stu-id="13824-104">SYNTAX</span></span>

### <span data-ttu-id="13824-105">VirtualNetworkRulePropertiesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="13824-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13824-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13824-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13824-107">說明</span><span class="sxs-lookup"><span data-stu-id="13824-107">DESCRIPTION</span></span>
<span data-ttu-id="13824-108">移除命名空間 NetworkRuleSet 的單一指定 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="13824-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="13824-109">示例</span><span class="sxs-lookup"><span data-stu-id="13824-109">EXAMPLES</span></span>

### <span data-ttu-id="13824-110">範例1</span><span class="sxs-lookup"><span data-stu-id="13824-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="13824-111">移除命名空間 NetworkRuleSet 的單一指定 VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="13824-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="13824-112">範例2</span><span class="sxs-lookup"><span data-stu-id="13824-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="13824-113">移除指定命名空間的 $virtualruleset NetworkRuleSet 1</span><span class="sxs-lookup"><span data-stu-id="13824-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="13824-114">參數</span><span class="sxs-lookup"><span data-stu-id="13824-114">PARAMETERS</span></span>

### <span data-ttu-id="13824-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13824-115">-AsJob</span></span>
<span data-ttu-id="13824-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="13824-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13824-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13824-117">-DefaultProfile</span></span>
<span data-ttu-id="13824-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="13824-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13824-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="13824-119">-Name</span></span>
<span data-ttu-id="13824-120">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="13824-120">Namespace Name</span></span>

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

### <span data-ttu-id="13824-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13824-121">-PassThru</span></span>
<span data-ttu-id="13824-122">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="13824-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="13824-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13824-123">-ResourceGroupName</span></span>
<span data-ttu-id="13824-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="13824-124">Resource Group Name</span></span>

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

### <span data-ttu-id="13824-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="13824-125">-SubnetId</span></span>
<span data-ttu-id="13824-126">子網資源識別碼</span><span class="sxs-lookup"><span data-stu-id="13824-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="13824-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="13824-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="13824-128">IPRule Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="13824-128">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="13824-129">-確認</span><span class="sxs-lookup"><span data-stu-id="13824-129">-Confirm</span></span>
<span data-ttu-id="13824-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13824-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13824-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13824-131">-WhatIf</span></span>
<span data-ttu-id="13824-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13824-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13824-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13824-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13824-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13824-134">CommonParameters</span></span>
<span data-ttu-id="13824-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13824-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="13824-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13824-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13824-137">輸入</span><span class="sxs-lookup"><span data-stu-id="13824-137">INPUTS</span></span>

### <span data-ttu-id="13824-138">System.object</span><span class="sxs-lookup"><span data-stu-id="13824-138">System.String</span></span>

### <span data-ttu-id="13824-139">PSNWRuleSetVirtualNetworkRulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="13824-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="13824-140">輸出</span><span class="sxs-lookup"><span data-stu-id="13824-140">OUTPUTS</span></span>

### <span data-ttu-id="13824-141">PSNetworkRuleSetAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="13824-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="13824-142">筆記</span><span class="sxs-lookup"><span data-stu-id="13824-142">NOTES</span></span>

## <span data-ttu-id="13824-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="13824-143">RELATED LINKS</span></span>