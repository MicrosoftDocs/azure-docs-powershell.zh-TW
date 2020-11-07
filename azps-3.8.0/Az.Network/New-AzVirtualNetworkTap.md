---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 0ac64d9b1aee363a1681b8d62da2ecf73574f7cd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959170"
---
# <span data-ttu-id="02655-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="02655-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="02655-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02655-102">SYNOPSIS</span></span>
<span data-ttu-id="02655-103">建立 VirtualNetworkTap 資源。</span><span class="sxs-lookup"><span data-stu-id="02655-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="02655-104">句法</span><span class="sxs-lookup"><span data-stu-id="02655-104">SYNTAX</span></span>

### <span data-ttu-id="02655-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="02655-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02655-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="02655-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02655-107">說明</span><span class="sxs-lookup"><span data-stu-id="02655-107">DESCRIPTION</span></span>
<span data-ttu-id="02655-108">**新的-AzVirtualNetworkTap** Cmdlet 會建立 Azure 虛擬網路攻絲資源。</span><span class="sxs-lookup"><span data-stu-id="02655-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="02655-109">示例</span><span class="sxs-lookup"><span data-stu-id="02655-109">EXAMPLES</span></span>

### <span data-ttu-id="02655-110">範例1：建立 Azure 虛擬網路分流</span><span class="sxs-lookup"><span data-stu-id="02655-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="02655-111">這個命令會建立一個名為「VirtualNetworkTap1」的虛擬網路，其中包含目的地 VM 設定詳細資料 (DestinationIpConfiguration、DestinationPort) 。</span><span class="sxs-lookup"><span data-stu-id="02655-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="02655-112">所有來源攻絲設定的 VM 流量都會路由到這個目的地 IP + 埠。</span><span class="sxs-lookup"><span data-stu-id="02655-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="02655-113">範例2：使用 LoadBalancer IP 建立 Azure 虛擬網路</span><span class="sxs-lookup"><span data-stu-id="02655-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="02655-114">這個命令會建立一個名為「VirtualNetworkTap1」的虛擬網路，其具有目的地 VM 配置詳細資料 (FrontEndIpConfiguration) 。</span><span class="sxs-lookup"><span data-stu-id="02655-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="02655-115">所有來源攻絲設定的 VM 流量都會路由到此 LoadBalancer IpConfiguration。</span><span class="sxs-lookup"><span data-stu-id="02655-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="02655-116">預設的目的地埠是4789。</span><span class="sxs-lookup"><span data-stu-id="02655-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="02655-117">參數</span><span class="sxs-lookup"><span data-stu-id="02655-117">PARAMETERS</span></span>

### <span data-ttu-id="02655-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02655-118">-AsJob</span></span>
<span data-ttu-id="02655-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="02655-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02655-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02655-120">-DefaultProfile</span></span>
<span data-ttu-id="02655-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="02655-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02655-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="02655-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="02655-123">目的地負載平衡器前端 IP 設定資源的參照。</span><span class="sxs-lookup"><span data-stu-id="02655-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02655-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="02655-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="02655-125">目的地負載平衡器前端 IP 設定資源的參照。</span><span class="sxs-lookup"><span data-stu-id="02655-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02655-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="02655-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="02655-127">目的地 network 介面 IP 設定資源的參照。</span><span class="sxs-lookup"><span data-stu-id="02655-127">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02655-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="02655-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="02655-129">目的地 network 介面 IP 設定資源的參照。</span><span class="sxs-lookup"><span data-stu-id="02655-129">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02655-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="02655-130">-DestinationPort</span></span>
<span data-ttu-id="02655-131">[資料包收集器] 的目的地埠</span><span class="sxs-lookup"><span data-stu-id="02655-131">The Destination Port of the packet collector</span></span>

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

### <span data-ttu-id="02655-132">-Force</span><span class="sxs-lookup"><span data-stu-id="02655-132">-Force</span></span>
<span data-ttu-id="02655-133">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="02655-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="02655-134">-位置</span><span class="sxs-lookup"><span data-stu-id="02655-134">-Location</span></span>
<span data-ttu-id="02655-135">位置。</span><span class="sxs-lookup"><span data-stu-id="02655-135">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02655-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="02655-136">-Name</span></span>
<span data-ttu-id="02655-137">攻絲的名稱。</span><span class="sxs-lookup"><span data-stu-id="02655-137">The name of the tap.</span></span>

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

### <span data-ttu-id="02655-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02655-138">-ResourceGroupName</span></span>
<span data-ttu-id="02655-139">虛擬網路的 [資源] 群組名稱。</span><span class="sxs-lookup"><span data-stu-id="02655-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="02655-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="02655-140">-Tag</span></span>
<span data-ttu-id="02655-141">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="02655-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02655-142">-確認</span><span class="sxs-lookup"><span data-stu-id="02655-142">-Confirm</span></span>
<span data-ttu-id="02655-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="02655-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02655-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02655-144">-WhatIf</span></span>
<span data-ttu-id="02655-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="02655-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02655-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02655-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02655-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02655-147">CommonParameters</span></span>
<span data-ttu-id="02655-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02655-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02655-149">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="02655-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02655-150">輸入</span><span class="sxs-lookup"><span data-stu-id="02655-150">INPUTS</span></span>

### <span data-ttu-id="02655-151">System.object</span><span class="sxs-lookup"><span data-stu-id="02655-151">System.String</span></span>

### <span data-ttu-id="02655-152">System.object</span><span class="sxs-lookup"><span data-stu-id="02655-152">System.Int32</span></span>

### <span data-ttu-id="02655-153">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="02655-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="02655-154">PSNetworkInterfaceIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="02655-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="02655-155">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="02655-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="02655-156">輸出</span><span class="sxs-lookup"><span data-stu-id="02655-156">OUTPUTS</span></span>

### <span data-ttu-id="02655-157">PSVirtualNetworkTap 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="02655-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="02655-158">筆記</span><span class="sxs-lookup"><span data-stu-id="02655-158">NOTES</span></span>

## <span data-ttu-id="02655-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="02655-159">RELATED LINKS</span></span>

[<span data-ttu-id="02655-160">AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="02655-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="02655-161">移除-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="02655-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="02655-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="02655-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)