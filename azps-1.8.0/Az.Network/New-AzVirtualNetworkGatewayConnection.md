---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 8f6b095a502c235927a48f2043a9140483cedc3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621706"
---
# <span data-ttu-id="4845f-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4845f-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="4845f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4845f-102">SYNOPSIS</span></span>
<span data-ttu-id="4845f-103">在虛擬網路閘道與內部部署 VPN 裝置之間建立點對點 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="4845f-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="4845f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4845f-104">SYNTAX</span></span>

### <span data-ttu-id="4845f-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="4845f-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-AsJob] [-ExpressRouteGatewayBypass]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4845f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4845f-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-AsJob] [-ExpressRouteGatewayBypass]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4845f-107">說明</span><span class="sxs-lookup"><span data-stu-id="4845f-107">DESCRIPTION</span></span>
<span data-ttu-id="4845f-108">在虛擬網路閘道與內部部署 VPN 裝置之間建立點對點 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="4845f-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="4845f-109">示例</span><span class="sxs-lookup"><span data-stu-id="4845f-109">EXAMPLES</span></span>

### <span data-ttu-id="4845f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="4845f-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="4845f-111">參數</span><span class="sxs-lookup"><span data-stu-id="4845f-111">PARAMETERS</span></span>

### <span data-ttu-id="4845f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4845f-112">-AsJob</span></span>
<span data-ttu-id="4845f-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4845f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4845f-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="4845f-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="4845f-115">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="4845f-115">-ConnectionType</span></span>

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

### <span data-ttu-id="4845f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4845f-116">-DefaultProfile</span></span>
<span data-ttu-id="4845f-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4845f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4845f-118">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="4845f-118">-EnableBgp</span></span>

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

### <span data-ttu-id="4845f-119">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="4845f-119">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="4845f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4845f-120">-Force</span></span>

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

### <span data-ttu-id="4845f-121">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="4845f-121">-IpsecPolicies</span></span>
<span data-ttu-id="4845f-122">IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="4845f-122">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="4845f-123">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="4845f-123">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="4845f-124">-位置</span><span class="sxs-lookup"><span data-stu-id="4845f-124">-Location</span></span>

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

### <span data-ttu-id="4845f-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="4845f-125">-Name</span></span>

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

### <span data-ttu-id="4845f-126">對等</span><span class="sxs-lookup"><span data-stu-id="4845f-126">-Peer</span></span>

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

### <span data-ttu-id="4845f-127">-PeerId</span><span class="sxs-lookup"><span data-stu-id="4845f-127">-PeerId</span></span>

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

### <span data-ttu-id="4845f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4845f-128">-ResourceGroupName</span></span>

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

### <span data-ttu-id="4845f-129">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="4845f-129">-RoutingWeight</span></span>

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

### <span data-ttu-id="4845f-130">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="4845f-130">-SharedKey</span></span>

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

### <span data-ttu-id="4845f-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="4845f-131">-Tag</span></span>
<span data-ttu-id="4845f-132">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="4845f-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4845f-133">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4845f-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4845f-134">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="4845f-134">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="4845f-135">針對 S2S 連線使用原則式流量選擇器</span><span class="sxs-lookup"><span data-stu-id="4845f-135">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="4845f-136">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="4845f-136">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="4845f-137">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="4845f-137">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="4845f-138">-確認</span><span class="sxs-lookup"><span data-stu-id="4845f-138">-Confirm</span></span>
<span data-ttu-id="4845f-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4845f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4845f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4845f-140">-WhatIf</span></span>
<span data-ttu-id="4845f-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4845f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4845f-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4845f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4845f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4845f-143">CommonParameters</span></span>
<span data-ttu-id="4845f-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4845f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4845f-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4845f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4845f-146">輸入</span><span class="sxs-lookup"><span data-stu-id="4845f-146">INPUTS</span></span>

### <span data-ttu-id="4845f-147">System.object</span><span class="sxs-lookup"><span data-stu-id="4845f-147">System.String</span></span>

### <span data-ttu-id="4845f-148">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4845f-148">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="4845f-149">PSLocalNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4845f-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="4845f-150">System.object</span><span class="sxs-lookup"><span data-stu-id="4845f-150">System.Int32</span></span>

### <span data-ttu-id="4845f-151">PSPeering 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4845f-151">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="4845f-152">System.object</span><span class="sxs-lookup"><span data-stu-id="4845f-152">System.Boolean</span></span>

### <span data-ttu-id="4845f-153">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4845f-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4845f-154">PSIpsecPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="4845f-154">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="4845f-155">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="4845f-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4845f-156">輸出</span><span class="sxs-lookup"><span data-stu-id="4845f-156">OUTPUTS</span></span>

### <span data-ttu-id="4845f-157">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4845f-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="4845f-158">筆記</span><span class="sxs-lookup"><span data-stu-id="4845f-158">NOTES</span></span>

## <span data-ttu-id="4845f-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="4845f-159">RELATED LINKS</span></span>

[<span data-ttu-id="4845f-160">AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4845f-160">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="4845f-161">移除-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4845f-161">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="4845f-162">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4845f-162">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)