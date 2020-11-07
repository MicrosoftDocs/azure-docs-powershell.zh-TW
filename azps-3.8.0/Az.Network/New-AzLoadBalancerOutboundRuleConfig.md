---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: a089f5b9e27a6fd7458dc02937a8bb75d1cbbb02
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796894"
---
# <span data-ttu-id="a1bdf-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1bdf-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="a1bdf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="a1bdf-103">建立負載平衡器的輸出規則配置。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="a1bdf-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1bdf-104">SYNTAX</span></span>

### <span data-ttu-id="a1bdf-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a1bdf-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1bdf-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1bdf-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1bdf-107">說明</span><span class="sxs-lookup"><span data-stu-id="a1bdf-107">DESCRIPTION</span></span>
<span data-ttu-id="a1bdf-108">**新的-AzLoadBalancerOutboundRuleConfig** Cmdlet 會建立 Azure 負載平衡器的輸出規則配置。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a1bdf-109">示例</span><span class="sxs-lookup"><span data-stu-id="a1bdf-109">EXAMPLES</span></span>

### <span data-ttu-id="a1bdf-110">範例1：為負載平衡器建立輸出規則配置</span><span class="sxs-lookup"><span data-stu-id="a1bdf-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="a1bdf-111">第一個命令會在名為 MyResourceGroup 的資源群組中建立名為 MyPublicIP 的公用 IP 位址，然後將它儲存在 $publicip 變數中。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="a1bdf-112">第二個命令會使用 $publicip 中的公用 IP 位址來建立名為 FrontendIpConfig01 的前端 IP 設定，然後將其儲存在 $frontend 變數中。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="a1bdf-113">第三個命令會建立名為 BackendAddressPool01 的後端位址集區配置，然後將它儲存在 $backend 變數中。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="a1bdf-114">第四個命令會使用 $frontend 和 $backend 中的前端和後端物件來建立名為 MyOutboundRule 的輸出規則配置。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="a1bdf-115">必須有 *Protocol* 、 *FrontendIPConfiguration* 和 *BackendAddressPool* 參數，才能建立輸出規則設定。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-115">The *Protocol* , *FrontendIPConfiguration* , and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

## <span data-ttu-id="a1bdf-116">參數</span><span class="sxs-lookup"><span data-stu-id="a1bdf-116">PARAMETERS</span></span>

### <span data-ttu-id="a1bdf-117">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="a1bdf-117">-AllocatedOutboundPort</span></span>
<span data-ttu-id="a1bdf-118">要用於 NAT 的輸出埠數目。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-118">The number of outbound ports to be used for NAT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1bdf-119">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a1bdf-119">-BackendAddressPool</span></span>
<span data-ttu-id="a1bdf-120">對 Dip 池的參照。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="a1bdf-121">輸出流量會在後端 Ip 中的 IPs 之間隨機地進行負載平衡。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1bdf-122">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a1bdf-122">-BackendAddressPoolId</span></span>
<span data-ttu-id="a1bdf-123">對 Dip 池的參照。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="a1bdf-124">輸出流量會在後端 Ip 中的 IPs 之間隨機地進行負載平衡。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1bdf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1bdf-125">-DefaultProfile</span></span>
<span data-ttu-id="a1bdf-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1bdf-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="a1bdf-127">-EnableTcpReset</span></span>
<span data-ttu-id="a1bdf-128">在 TCP 資料流程閒置超時或意外的連線終止中接收雙向 TCP 重設。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="a1bdf-129">這個元素只會在通訊協定設定為 TCP 時使用。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="a1bdf-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1bdf-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a1bdf-131">負載平衡器的前端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-131">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1bdf-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a1bdf-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a1bdf-133">TCP 空閒連線的超時時間</span><span class="sxs-lookup"><span data-stu-id="a1bdf-133">The timeout for the TCP idle connection</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1bdf-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1bdf-134">-Name</span></span>
<span data-ttu-id="a1bdf-135">輸出規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="a1bdf-136">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="a1bdf-136">-Protocol</span></span>
<span data-ttu-id="a1bdf-137">通訊協定-TCP、UDP 或 All</span><span class="sxs-lookup"><span data-stu-id="a1bdf-137">Protocol - TCP, UDP or All</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1bdf-138">-確認</span><span class="sxs-lookup"><span data-stu-id="a1bdf-138">-Confirm</span></span>
<span data-ttu-id="a1bdf-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1bdf-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1bdf-140">-WhatIf</span></span>
<span data-ttu-id="a1bdf-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1bdf-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1bdf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1bdf-143">CommonParameters</span></span>
<span data-ttu-id="a1bdf-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1bdf-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a1bdf-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1bdf-146">輸入</span><span class="sxs-lookup"><span data-stu-id="a1bdf-146">INPUTS</span></span>

### <span data-ttu-id="a1bdf-147">System.object</span><span class="sxs-lookup"><span data-stu-id="a1bdf-147">System.Int32</span></span>

### <span data-ttu-id="a1bdf-148">System.object</span><span class="sxs-lookup"><span data-stu-id="a1bdf-148">System.String</span></span>

### <span data-ttu-id="a1bdf-149">PSResourceId [] （[]）</span><span class="sxs-lookup"><span data-stu-id="a1bdf-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="a1bdf-150">PSBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a1bdf-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="a1bdf-151">輸出</span><span class="sxs-lookup"><span data-stu-id="a1bdf-151">OUTPUTS</span></span>

### <span data-ttu-id="a1bdf-152">PSOutboundRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a1bdf-152">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="a1bdf-153">筆記</span><span class="sxs-lookup"><span data-stu-id="a1bdf-153">NOTES</span></span>

## <span data-ttu-id="a1bdf-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1bdf-154">RELATED LINKS</span></span>

[<span data-ttu-id="a1bdf-155">附加 AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1bdf-155">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="a1bdf-156">AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1bdf-156">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="a1bdf-157">移除-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1bdf-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="a1bdf-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1bdf-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)