---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: aff2fccde6fc43b9153d8da421f34a6038688fd7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621602"
---
# <span data-ttu-id="affcf-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="affcf-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="affcf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="affcf-102">SYNOPSIS</span></span>
<span data-ttu-id="affcf-103">從負載平衡器移除輸出規則配置。</span><span class="sxs-lookup"><span data-stu-id="affcf-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="affcf-104">句法</span><span class="sxs-lookup"><span data-stu-id="affcf-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="affcf-105">說明</span><span class="sxs-lookup"><span data-stu-id="affcf-105">DESCRIPTION</span></span>
<span data-ttu-id="affcf-106">**AzLoadBalancerOutboundRuleConfig** Cmdlet 會從 Azure 負載平衡器移除輸出規則配置。</span><span class="sxs-lookup"><span data-stu-id="affcf-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="affcf-107">示例</span><span class="sxs-lookup"><span data-stu-id="affcf-107">EXAMPLES</span></span>

### <span data-ttu-id="affcf-108">範例1：從 Azure 負載平衡器刪除輸出規則</span><span class="sxs-lookup"><span data-stu-id="affcf-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="affcf-109">第一個命令會取得與您想要移除的輸出規則配置相關聯的負載平衡器，然後將它儲存在 $slb 變數中。</span><span class="sxs-lookup"><span data-stu-id="affcf-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="affcf-110">第二個命令會從負載平衡器移除關聯的輸出規則配置。</span><span class="sxs-lookup"><span data-stu-id="affcf-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="affcf-111">第三個命令會更新負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="affcf-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="affcf-112">參數</span><span class="sxs-lookup"><span data-stu-id="affcf-112">PARAMETERS</span></span>

### <span data-ttu-id="affcf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="affcf-113">-DefaultProfile</span></span>
<span data-ttu-id="affcf-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="affcf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="affcf-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="affcf-115">-LoadBalancer</span></span>
<span data-ttu-id="affcf-116">負載平衡器資源的參照。</span><span class="sxs-lookup"><span data-stu-id="affcf-116">The reference of the load balancer resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="affcf-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="affcf-117">-Name</span></span>
<span data-ttu-id="affcf-118">輸出規則的名稱</span><span class="sxs-lookup"><span data-stu-id="affcf-118">The Name of outbound rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affcf-119">-確認</span><span class="sxs-lookup"><span data-stu-id="affcf-119">-Confirm</span></span>
<span data-ttu-id="affcf-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="affcf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="affcf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="affcf-121">-WhatIf</span></span>
<span data-ttu-id="affcf-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="affcf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="affcf-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="affcf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="affcf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="affcf-124">CommonParameters</span></span>
<span data-ttu-id="affcf-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="affcf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="affcf-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="affcf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="affcf-127">輸入</span><span class="sxs-lookup"><span data-stu-id="affcf-127">INPUTS</span></span>

### <span data-ttu-id="affcf-128">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="affcf-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="affcf-129">輸出</span><span class="sxs-lookup"><span data-stu-id="affcf-129">OUTPUTS</span></span>

### <span data-ttu-id="affcf-130">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="affcf-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="affcf-131">筆記</span><span class="sxs-lookup"><span data-stu-id="affcf-131">NOTES</span></span>

## <span data-ttu-id="affcf-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="affcf-132">RELATED LINKS</span></span>

[<span data-ttu-id="affcf-133">附加 AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="affcf-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="affcf-134">AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="affcf-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="affcf-135">新-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="affcf-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="affcf-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="affcf-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)