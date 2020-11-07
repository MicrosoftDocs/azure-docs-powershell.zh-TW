---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 01e132dab83931a48254bb8483cc794d7c619a6e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790642"
---
# <span data-ttu-id="bfff1-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bfff1-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="bfff1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bfff1-102">SYNOPSIS</span></span>
<span data-ttu-id="bfff1-103">移除負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="bfff1-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="bfff1-104">句法</span><span class="sxs-lookup"><span data-stu-id="bfff1-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfff1-105">說明</span><span class="sxs-lookup"><span data-stu-id="bfff1-105">DESCRIPTION</span></span>
<span data-ttu-id="bfff1-106">**AzLoadBalancerRuleConfig** Cmdlet 會移除 Azure 負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="bfff1-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="bfff1-107">示例</span><span class="sxs-lookup"><span data-stu-id="bfff1-107">EXAMPLES</span></span>

### <span data-ttu-id="bfff1-108">範例1：從負載平衡器移除規則配置</span><span class="sxs-lookup"><span data-stu-id="bfff1-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="bfff1-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="bfff1-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="bfff1-110">第二個命令會從 $loadbalancer 中的負載平衡器移除名為 MyLBruleName 的規則配置。</span><span class="sxs-lookup"><span data-stu-id="bfff1-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="bfff1-111">參數</span><span class="sxs-lookup"><span data-stu-id="bfff1-111">PARAMETERS</span></span>

### <span data-ttu-id="bfff1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfff1-112">-DefaultProfile</span></span>
<span data-ttu-id="bfff1-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bfff1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfff1-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bfff1-114">-LoadBalancer</span></span>
<span data-ttu-id="bfff1-115">指定包含此 Cmdlet 移除之規則配置的 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="bfff1-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bfff1-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="bfff1-116">-Name</span></span>
<span data-ttu-id="bfff1-117">指定此 Cmdlet 移除的負載等化器規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="bfff1-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfff1-118">-確認</span><span class="sxs-lookup"><span data-stu-id="bfff1-118">-Confirm</span></span>
<span data-ttu-id="bfff1-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bfff1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfff1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfff1-120">-WhatIf</span></span>
<span data-ttu-id="bfff1-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bfff1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bfff1-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bfff1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfff1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfff1-123">CommonParameters</span></span>
<span data-ttu-id="bfff1-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bfff1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfff1-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bfff1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfff1-126">輸入</span><span class="sxs-lookup"><span data-stu-id="bfff1-126">INPUTS</span></span>

### <span data-ttu-id="bfff1-127">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bfff1-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="bfff1-128">輸出</span><span class="sxs-lookup"><span data-stu-id="bfff1-128">OUTPUTS</span></span>

### <span data-ttu-id="bfff1-129">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bfff1-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="bfff1-130">筆記</span><span class="sxs-lookup"><span data-stu-id="bfff1-130">NOTES</span></span>

## <span data-ttu-id="bfff1-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="bfff1-131">RELATED LINKS</span></span>

[<span data-ttu-id="bfff1-132">附加 AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bfff1-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="bfff1-133">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bfff1-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="bfff1-134">AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bfff1-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="bfff1-135">新-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bfff1-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="bfff1-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bfff1-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)

