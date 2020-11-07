---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 622fb5278f7e0a78fb6163954829b1a2aaa6bba7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799734"
---
# <span data-ttu-id="18f00-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18f00-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="18f00-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18f00-102">SYNOPSIS</span></span>
<span data-ttu-id="18f00-103">更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="18f00-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18f00-104">句法</span><span class="sxs-lookup"><span data-stu-id="18f00-104">SYNTAX</span></span>

### <span data-ttu-id="18f00-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="18f00-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18f00-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="18f00-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18f00-107">說明</span><span class="sxs-lookup"><span data-stu-id="18f00-107">DESCRIPTION</span></span>
<span data-ttu-id="18f00-108">**AzureRmVirtualNetworkGateway** Cmdlet 會更新虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="18f00-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="18f00-109">示例</span><span class="sxs-lookup"><span data-stu-id="18f00-109">EXAMPLES</span></span>

### <span data-ttu-id="18f00-110">範例1：設定虛擬網路閘道的目標狀態</span><span class="sxs-lookup"><span data-stu-id="18f00-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="18f00-111">第一個命令會取得屬於資源群組 ResourceGroup001 的名為 Gateway01 的虛擬網路閘道，並將其儲存到名為 $Gateway 的變數</span><span class="sxs-lookup"><span data-stu-id="18f00-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="18f00-112">第二個命令會針對儲存在 variable $Gateway 中的虛擬網路閘道設定目標狀態。</span><span class="sxs-lookup"><span data-stu-id="18f00-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="18f00-113">此命令也會將 ASN 設定為1337。</span><span class="sxs-lookup"><span data-stu-id="18f00-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="18f00-114">參數</span><span class="sxs-lookup"><span data-stu-id="18f00-114">PARAMETERS</span></span>

### <span data-ttu-id="18f00-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18f00-115">-AsJob</span></span>
<span data-ttu-id="18f00-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="18f00-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-117">-Asn</span><span class="sxs-lookup"><span data-stu-id="18f00-117">-Asn</span></span>
<span data-ttu-id="18f00-118">指定虛擬網路閘道自治系統號碼 (ASN) ，用來設定在 IPsec 隧道內 (BGP) 會話的邊界閘道通訊協定。</span><span class="sxs-lookup"><span data-stu-id="18f00-118">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18f00-119">-DefaultProfile</span></span>
<span data-ttu-id="18f00-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="18f00-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-121">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="18f00-121">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="18f00-122">停用作用中的功能。</span><span class="sxs-lookup"><span data-stu-id="18f00-122">Disables the active-active feature.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-123">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="18f00-123">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="18f00-124">啟用 [作用中-作用中] 功能。</span><span class="sxs-lookup"><span data-stu-id="18f00-124">Enables the active-active feature.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-125">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="18f00-125">-GatewayDefaultSite</span></span>
<span data-ttu-id="18f00-126">指定要用於強制隧道的預設網站。</span><span class="sxs-lookup"><span data-stu-id="18f00-126">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="18f00-127">如果指定了預設網站，閘道的虛擬私人網路 (VPN) 的所有網際網路流量都會路由到該網站。</span><span class="sxs-lookup"><span data-stu-id="18f00-127">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-128">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="18f00-128">-GatewaySku</span></span>
<span data-ttu-id="18f00-129">指定虛擬網路閘道 (SKU) 的庫存單位。</span><span class="sxs-lookup"><span data-stu-id="18f00-129">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="18f00-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="18f00-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="18f00-131">空白</span><span class="sxs-lookup"><span data-stu-id="18f00-131">Basic</span></span>
- <span data-ttu-id="18f00-132">標準</span><span class="sxs-lookup"><span data-stu-id="18f00-132">Standard</span></span>
- <span data-ttu-id="18f00-133">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="18f00-133">HighPerformance</span></span>
- <span data-ttu-id="18f00-134">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="18f00-134">VpnGw1</span></span>
- <span data-ttu-id="18f00-135">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="18f00-135">VpnGw2</span></span>
- <span data-ttu-id="18f00-136">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="18f00-136">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-137">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="18f00-137">-PeerWeight</span></span>
<span data-ttu-id="18f00-138">指定透過此虛擬網路閘道通過 BGP 瞭解的路線所新增的體重</span><span class="sxs-lookup"><span data-stu-id="18f00-138">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-139">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="18f00-139">-RadiusServerAddress</span></span>
<span data-ttu-id="18f00-140">P2S 外部 Radius 伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="18f00-140">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-141">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="18f00-141">-RadiusServerSecret</span></span>
<span data-ttu-id="18f00-142">P2S [外部 Radius 伺服器] 密碼。</span><span class="sxs-lookup"><span data-stu-id="18f00-142">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-143">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18f00-143">-VirtualNetworkGateway</span></span>
<span data-ttu-id="18f00-144">指定要作為修改基礎的虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="18f00-144">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="18f00-145">您可以使用 Get-AzureRmVirtualNetworkGateway Cmdlet 來取得虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="18f00-145">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="18f00-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="18f00-147">指定此 Cmdlet 用來從哪個位址空間來指派 VPN 用戶端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="18f00-147">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="18f00-148">這不應與虛擬網路或內部部署範圍重迭。</span><span class="sxs-lookup"><span data-stu-id="18f00-148">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-149">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="18f00-149">-VpnClientProtocol</span></span>
<span data-ttu-id="18f00-150">P2S VPN 用戶端隧道通訊協定清單</span><span class="sxs-lookup"><span data-stu-id="18f00-150">A list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-151">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="18f00-151">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="18f00-152">指定已吊銷之 VPN 用戶端憑證的清單。</span><span class="sxs-lookup"><span data-stu-id="18f00-152">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="18f00-153">VPN 用戶端會移除與其中一個相符的憑證。</span><span class="sxs-lookup"><span data-stu-id="18f00-153">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-154">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="18f00-154">-VpnClientRootCertificates</span></span>
<span data-ttu-id="18f00-155">指定要用於 VPN 用戶端驗證的 VPN 用戶端根憑證清單。</span><span class="sxs-lookup"><span data-stu-id="18f00-155">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="18f00-156">[連線 VPN 用戶端] 必須出示從這些根憑證的其中一個證書產生的憑證。</span><span class="sxs-lookup"><span data-stu-id="18f00-156">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-157">-確認</span><span class="sxs-lookup"><span data-stu-id="18f00-157">-Confirm</span></span>
<span data-ttu-id="18f00-158">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="18f00-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18f00-159">-WhatIf</span></span>
<span data-ttu-id="18f00-160">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="18f00-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18f00-161">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="18f00-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18f00-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f00-162">CommonParameters</span></span>
<span data-ttu-id="18f00-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18f00-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f00-164">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="18f00-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f00-165">輸入</span><span class="sxs-lookup"><span data-stu-id="18f00-165">INPUTS</span></span>

### <span data-ttu-id="18f00-166">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18f00-166">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="18f00-167">形參 "VirtualNetworkGateway" 接受管線中 "PSVirtualNetworkGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="18f00-167">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="18f00-168">輸出</span><span class="sxs-lookup"><span data-stu-id="18f00-168">OUTPUTS</span></span>

### <span data-ttu-id="18f00-169">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="18f00-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="18f00-170">筆記</span><span class="sxs-lookup"><span data-stu-id="18f00-170">NOTES</span></span>
* <span data-ttu-id="18f00-171">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="18f00-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="18f00-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="18f00-172">RELATED LINKS</span></span>

[<span data-ttu-id="18f00-173">AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18f00-173">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="18f00-174">新-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18f00-174">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="18f00-175">移除-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18f00-175">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="18f00-176">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18f00-176">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="18f00-177">調整大小-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="18f00-177">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

