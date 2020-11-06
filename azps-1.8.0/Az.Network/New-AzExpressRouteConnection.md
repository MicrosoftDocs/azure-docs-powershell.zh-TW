---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 72aa8af012addf4fa309adc7c63467ecaf667fff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621799"
---
# <span data-ttu-id="26436-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="26436-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="26436-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26436-102">SYNOPSIS</span></span>
<span data-ttu-id="26436-103">建立一個 ExpressRoute 連線，將 ExpressRoute 閘道連線到內部部署 ExpressRoute 電路</span><span class="sxs-lookup"><span data-stu-id="26436-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="26436-104">句法</span><span class="sxs-lookup"><span data-stu-id="26436-104">SYNTAX</span></span>

### <span data-ttu-id="26436-105">ByExpressRouteGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="26436-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26436-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="26436-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26436-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="26436-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26436-108">說明</span><span class="sxs-lookup"><span data-stu-id="26436-108">DESCRIPTION</span></span>
<span data-ttu-id="26436-109">在虛擬中樞內的 ExpressRoute 閘道內部部署 ExpressRoute 電路 BGP 對等之間建立 ExpressRoute 連線。</span><span class="sxs-lookup"><span data-stu-id="26436-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="26436-110">示例</span><span class="sxs-lookup"><span data-stu-id="26436-110">EXAMPLES</span></span>

### <span data-ttu-id="26436-111">範例1</span><span class="sxs-lookup"><span data-stu-id="26436-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
```

<span data-ttu-id="26436-112">上述將會建立一個資源群組、虛擬 WAN、虛擬網路、虛擬中樞、快速路由閘道，以及在 Microsoft 中的 [testRG] 資源群組中使用私人對等的 ExpressRoute 回路。</span><span class="sxs-lookup"><span data-stu-id="26436-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="26436-113">建立閘道之後，就會使用 [New-AzExpressRouteConnection] 命令將其連線至 ExpressRoute 電路對等。</span><span class="sxs-lookup"><span data-stu-id="26436-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="26436-114">參數</span><span class="sxs-lookup"><span data-stu-id="26436-114">PARAMETERS</span></span>

### <span data-ttu-id="26436-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26436-115">-AsJob</span></span>
<span data-ttu-id="26436-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26436-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26436-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="26436-117">-AuthorizationKey</span></span>
<span data-ttu-id="26436-118">從 ExpressRoute 回路擁有者取得的金鑰，可以建立與不同訂閱中的閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="26436-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

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

### <span data-ttu-id="26436-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26436-119">-DefaultProfile</span></span>
<span data-ttu-id="26436-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26436-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26436-121">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="26436-121">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="26436-122">要建立此快速路由閘道連接之快速路由線路對等的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="26436-122">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

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

### <span data-ttu-id="26436-123">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="26436-123">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="26436-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="26436-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26436-125">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="26436-125">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="26436-126">此連接的父 ExpressRouteGateway。</span><span class="sxs-lookup"><span data-stu-id="26436-126">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26436-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="26436-127">-Name</span></span>
<span data-ttu-id="26436-128">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="26436-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26436-129">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="26436-129">-ParentResourceId</span></span>
<span data-ttu-id="26436-130">此連線之父 ExpressRouteGateway 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="26436-130">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26436-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26436-131">-ResourceGroupName</span></span>
<span data-ttu-id="26436-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="26436-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26436-133">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="26436-133">-RoutingWeight</span></span>
<span data-ttu-id="26436-134">需要指派給這個連線之資料包路由的權重。</span><span class="sxs-lookup"><span data-stu-id="26436-134">The weight for packet routing that needs to be assigned to this connection.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26436-135">-確認</span><span class="sxs-lookup"><span data-stu-id="26436-135">-Confirm</span></span>
<span data-ttu-id="26436-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26436-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26436-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26436-137">-WhatIf</span></span>
<span data-ttu-id="26436-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26436-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26436-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26436-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26436-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26436-140">CommonParameters</span></span>
<span data-ttu-id="26436-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26436-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26436-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26436-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26436-143">輸入</span><span class="sxs-lookup"><span data-stu-id="26436-143">INPUTS</span></span>

### <span data-ttu-id="26436-144">PSExpressRouteGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="26436-144">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="26436-145">System.object</span><span class="sxs-lookup"><span data-stu-id="26436-145">System.String</span></span>

## <span data-ttu-id="26436-146">輸出</span><span class="sxs-lookup"><span data-stu-id="26436-146">OUTPUTS</span></span>

### <span data-ttu-id="26436-147">PSExpressRouteConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="26436-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="26436-148">筆記</span><span class="sxs-lookup"><span data-stu-id="26436-148">NOTES</span></span>

## <span data-ttu-id="26436-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="26436-149">RELATED LINKS</span></span>