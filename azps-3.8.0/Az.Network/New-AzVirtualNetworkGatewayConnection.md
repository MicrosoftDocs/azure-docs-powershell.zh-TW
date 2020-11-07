---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: f6dc25bc1000466d853715f62e38237ddfc76aa2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959174"
---
# <span data-ttu-id="31f93-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="31f93-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="31f93-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31f93-102">SYNOPSIS</span></span>
<span data-ttu-id="31f93-103">在虛擬網路閘道與內部部署 VPN 裝置之間建立點對點 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="31f93-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="31f93-104">句法</span><span class="sxs-lookup"><span data-stu-id="31f93-104">SYNTAX</span></span>

### <span data-ttu-id="31f93-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="31f93-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-SharedKey <String>]
 [-Peer <PSPeering>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] 
 [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31f93-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="31f93-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-SharedKey <String>]
 [-PeerId <String>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] [-Force]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31f93-107">說明</span><span class="sxs-lookup"><span data-stu-id="31f93-107">DESCRIPTION</span></span>
<span data-ttu-id="31f93-108">在虛擬網路閘道與內部部署 VPN 裝置之間建立點對點 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="31f93-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="31f93-109">示例</span><span class="sxs-lookup"><span data-stu-id="31f93-109">EXAMPLES</span></span>

### <span data-ttu-id="31f93-110">範例1</span><span class="sxs-lookup"><span data-stu-id="31f93-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="31f93-111">參數</span><span class="sxs-lookup"><span data-stu-id="31f93-111">PARAMETERS</span></span>

### <span data-ttu-id="31f93-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31f93-112">-AsJob</span></span>
<span data-ttu-id="31f93-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="31f93-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31f93-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="31f93-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="31f93-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="31f93-115">-ConnectionProtocol</span></span>
<span data-ttu-id="31f93-116">閘道連線通訊協定： IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="31f93-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f93-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="31f93-117">-ConnectionType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f93-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f93-118">-DefaultProfile</span></span>
<span data-ttu-id="31f93-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="31f93-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31f93-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="31f93-120">-EnableBgp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f93-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="31f93-121">-ExpressRouteGatewayBypass</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f93-122">-Force</span><span class="sxs-lookup"><span data-stu-id="31f93-122">-Force</span></span>

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

### <span data-ttu-id="31f93-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="31f93-123">-IpsecPolicies</span></span>
<span data-ttu-id="31f93-124">IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="31f93-124">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f93-125">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="31f93-125">-LocalNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f93-126">-位置</span><span class="sxs-lookup"><span data-stu-id="31f93-126">-Location</span></span>

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

### <span data-ttu-id="31f93-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="31f93-127">-Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f93-128">對等</span><span class="sxs-lookup"><span data-stu-id="31f93-128">-Peer</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f93-129">-PeerId</span><span class="sxs-lookup"><span data-stu-id="31f93-129">-PeerId</span></span>

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

### <span data-ttu-id="31f93-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f93-130">-ResourceGroupName</span></span>

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

### <span data-ttu-id="31f93-131">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="31f93-131">-RoutingWeight</span></span>

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

### <span data-ttu-id="31f93-132">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="31f93-132">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="31f93-133">連線的死對等檢測超時值（以秒為單位）</span><span class="sxs-lookup"><span data-stu-id="31f93-133">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="31f93-134">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="31f93-134">-SharedKey</span></span>

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

### <span data-ttu-id="31f93-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="31f93-135">-Tag</span></span>
<span data-ttu-id="31f93-136">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="31f93-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="31f93-137">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="31f93-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="31f93-138">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="31f93-138">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="31f93-139">流量選取器原則的清單。</span><span class="sxs-lookup"><span data-stu-id="31f93-139">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f93-140">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="31f93-140">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="31f93-141">是否針對此 S2S VPN 隧道使用 PrivateIP</span><span class="sxs-lookup"><span data-stu-id="31f93-141">Whether to use PrivateIP for this S2S VPN tunnel</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f93-142">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="31f93-142">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="31f93-143">針對 S2S 連線使用原則式流量選擇器</span><span class="sxs-lookup"><span data-stu-id="31f93-143">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f93-144">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="31f93-144">-VirtualNetworkGateway1</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f93-145">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="31f93-145">-VirtualNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f93-146">-確認</span><span class="sxs-lookup"><span data-stu-id="31f93-146">-Confirm</span></span>
<span data-ttu-id="31f93-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="31f93-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f93-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31f93-148">-WhatIf</span></span>
<span data-ttu-id="31f93-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="31f93-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31f93-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31f93-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f93-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f93-151">CommonParameters</span></span>
<span data-ttu-id="31f93-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31f93-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f93-153">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="31f93-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f93-154">輸入</span><span class="sxs-lookup"><span data-stu-id="31f93-154">INPUTS</span></span>

### <span data-ttu-id="31f93-155">System.object</span><span class="sxs-lookup"><span data-stu-id="31f93-155">System.String</span></span>

### <span data-ttu-id="31f93-156">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="31f93-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="31f93-157">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="31f93-157">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="31f93-158">System.object</span><span class="sxs-lookup"><span data-stu-id="31f93-158">System.Int32</span></span>

### <span data-ttu-id="31f93-159">PSPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="31f93-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="31f93-160">System.object</span><span class="sxs-lookup"><span data-stu-id="31f93-160">System.Boolean</span></span>

### <span data-ttu-id="31f93-161">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="31f93-161">System.Collections.Hashtable</span></span>

### <span data-ttu-id="31f93-162">PSIpsecPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="31f93-162">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="31f93-163">PSTrafficSelectorPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="31f93-163">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="31f93-164">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="31f93-164">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="31f93-165">輸出</span><span class="sxs-lookup"><span data-stu-id="31f93-165">OUTPUTS</span></span>

### <span data-ttu-id="31f93-166">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="31f93-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="31f93-167">筆記</span><span class="sxs-lookup"><span data-stu-id="31f93-167">NOTES</span></span>

## <span data-ttu-id="31f93-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="31f93-168">RELATED LINKS</span></span>

[<span data-ttu-id="31f93-169">AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="31f93-169">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="31f93-170">移除-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="31f93-170">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="31f93-171">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="31f93-171">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)