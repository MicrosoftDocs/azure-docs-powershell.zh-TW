---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: e28ebc04277e3c9031c9c287aa02f7eea32867a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790109"
---
# <span data-ttu-id="6da0e-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6da0e-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="6da0e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6da0e-102">SYNOPSIS</span></span>
<span data-ttu-id="6da0e-103">取得負載平衡器的入站 NAT 規則配置。</span><span class="sxs-lookup"><span data-stu-id="6da0e-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="6da0e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6da0e-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6da0e-105">說明</span><span class="sxs-lookup"><span data-stu-id="6da0e-105">DESCRIPTION</span></span>
<span data-ttu-id="6da0e-106">**AzLoadBalancerInboundNatRuleConfig** Cmdlet 會在 Azure 負載平衡器中取得一或多個入站網路位址轉譯 (NAT) 規則。</span><span class="sxs-lookup"><span data-stu-id="6da0e-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="6da0e-107">示例</span><span class="sxs-lookup"><span data-stu-id="6da0e-107">EXAMPLES</span></span>

### <span data-ttu-id="6da0e-108">範例1：取得入站 NAT 規則設定</span><span class="sxs-lookup"><span data-stu-id="6da0e-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="6da0e-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，並將它儲存在 $slb 的變數中。</span><span class="sxs-lookup"><span data-stu-id="6da0e-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="6da0e-110">第二個命令會從 $slb 中的負載平衡器取得關聯的 NAT 規則（名為 MyInboundNatRule1）。</span><span class="sxs-lookup"><span data-stu-id="6da0e-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="6da0e-111">參數</span><span class="sxs-lookup"><span data-stu-id="6da0e-111">PARAMETERS</span></span>

### <span data-ttu-id="6da0e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6da0e-112">-DefaultProfile</span></span>
<span data-ttu-id="6da0e-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6da0e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6da0e-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6da0e-114">-LoadBalancer</span></span>
<span data-ttu-id="6da0e-115">指定與要取得的輸入 NAT 規則配置相關聯的負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="6da0e-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="6da0e-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="6da0e-116">-Name</span></span>
<span data-ttu-id="6da0e-117">指定要取得的輸入 NAT 規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="6da0e-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="6da0e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da0e-118">CommonParameters</span></span>
<span data-ttu-id="6da0e-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6da0e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da0e-120">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6da0e-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da0e-121">輸入</span><span class="sxs-lookup"><span data-stu-id="6da0e-121">INPUTS</span></span>

### <span data-ttu-id="6da0e-122">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6da0e-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6da0e-123">輸出</span><span class="sxs-lookup"><span data-stu-id="6da0e-123">OUTPUTS</span></span>

### <span data-ttu-id="6da0e-124">PSInboundNatRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6da0e-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="6da0e-125">筆記</span><span class="sxs-lookup"><span data-stu-id="6da0e-125">NOTES</span></span>

## <span data-ttu-id="6da0e-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="6da0e-126">RELATED LINKS</span></span>

[<span data-ttu-id="6da0e-127">AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6da0e-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="6da0e-128">新-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6da0e-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="6da0e-129">移除-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6da0e-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="6da0e-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6da0e-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)

