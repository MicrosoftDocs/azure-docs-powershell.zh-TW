---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 1bde6608f5dd87c2c102f3f2957832a2eb41e50a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789993"
---
# <span data-ttu-id="85e5c-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85e5c-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="85e5c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85e5c-102">SYNOPSIS</span></span>
<span data-ttu-id="85e5c-103">建立應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="85e5c-103">Creates an application gateway.</span></span>

## <span data-ttu-id="85e5c-104">句法</span><span class="sxs-lookup"><span data-stu-id="85e5c-104">SYNTAX</span></span>

### <span data-ttu-id="85e5c-105">IdentityByUserAssignedIdentityId (預設) </span><span class="sxs-lookup"><span data-stu-id="85e5c-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85e5c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="85e5c-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicyId <String>] [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>]
 [-EnableHttp2] [-EnableFIPS] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85e5c-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="85e5c-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85e5c-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="85e5c-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity> [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85e5c-109">說明</span><span class="sxs-lookup"><span data-stu-id="85e5c-109">DESCRIPTION</span></span>
<span data-ttu-id="85e5c-110">**新的-AzApplicationGateway** Cmdlet 會建立 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="85e5c-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="85e5c-111">應用程式閘道需要下列各項：</span><span class="sxs-lookup"><span data-stu-id="85e5c-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="85e5c-112">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="85e5c-112">A resource group.</span></span>
- <span data-ttu-id="85e5c-113">虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="85e5c-113">A virtual network.</span></span>
- <span data-ttu-id="85e5c-114">後端伺服器池，包含後端伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="85e5c-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="85e5c-115">後端伺服器池設定。</span><span class="sxs-lookup"><span data-stu-id="85e5c-115">Back-end server pool settings.</span></span> <span data-ttu-id="85e5c-116">每個池都有套用至池中所有伺服器的埠、通訊協定及 cookie 關聯性等設定。</span><span class="sxs-lookup"><span data-stu-id="85e5c-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="85e5c-117">前端 IP 位址，也就是在應用程式閘道開啟的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="85e5c-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="85e5c-118">前端 IP 位址可以是公用 IP 位址或內部 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="85e5c-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="85e5c-119">前端埠，即是在應用程式閘道開啟的公用埠。</span><span class="sxs-lookup"><span data-stu-id="85e5c-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="85e5c-120">擊中這些埠的流量會重新導向到後端伺服器。</span><span class="sxs-lookup"><span data-stu-id="85e5c-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="85e5c-121">系結監聽器與後端伺服器池的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="85e5c-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="85e5c-122">規則會定義當通信量擊中特定的監聽程式時，應該會將它導向到哪個後端伺服器池。</span><span class="sxs-lookup"><span data-stu-id="85e5c-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="85e5c-123">偵聽程式有前端埠、前端 IP 位址、通訊協定 (HTTP 或 HTTPS) 以及安全通訊端層 (SSL) 憑證名 (如果設定 SSL 卸載) 。</span><span class="sxs-lookup"><span data-stu-id="85e5c-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="85e5c-124">示例</span><span class="sxs-lookup"><span data-stu-id="85e5c-124">EXAMPLES</span></span>

### <span data-ttu-id="85e5c-125">範例1：建立應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="85e5c-125">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="85e5c-126">下列範例會先建立資源群組和虛擬網路，以及下列專案來建立應用程式閘道：</span><span class="sxs-lookup"><span data-stu-id="85e5c-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="85e5c-127">後端伺服器池</span><span class="sxs-lookup"><span data-stu-id="85e5c-127">A back-end server pool</span></span>
- <span data-ttu-id="85e5c-128">後端伺服器池設定</span><span class="sxs-lookup"><span data-stu-id="85e5c-128">Back-end server pool settings</span></span>
- <span data-ttu-id="85e5c-129">前端埠</span><span class="sxs-lookup"><span data-stu-id="85e5c-129">Front-end ports</span></span>
- <span data-ttu-id="85e5c-130">前端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="85e5c-130">Front-end IP addresses</span></span>
- <span data-ttu-id="85e5c-131">要求路由規則這四個命令會建立一個虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="85e5c-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="85e5c-132">第一個命令會建立子網配置。</span><span class="sxs-lookup"><span data-stu-id="85e5c-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="85e5c-133">第二個命令會建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="85e5c-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="85e5c-134">第三個命令會驗證子網設定，而第四個命令會驗證虛擬網路已順利建立。</span><span class="sxs-lookup"><span data-stu-id="85e5c-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="85e5c-135">下列命令會建立應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="85e5c-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="85e5c-136">第一個命令會為先前建立的子網建立名為 GatewayIp01 的 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="85e5c-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="85e5c-137">第二個命令會使用後端 IP 位址清單來建立名為 Pool01 的後端伺服器池，並將該池儲存在 $Pool 變數中。</span><span class="sxs-lookup"><span data-stu-id="85e5c-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="85e5c-138">第三個命令會建立後端伺服器池的設定，並將設定儲存在 $PoolSetting 變數中。</span><span class="sxs-lookup"><span data-stu-id="85e5c-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="85e5c-139">第四個命令會在埠80建立前端埠，將它命名為 FrontEndPort01，並將埠儲存在 $FrontEndPort 變數中。</span><span class="sxs-lookup"><span data-stu-id="85e5c-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="85e5c-140">第五個命令會使用新的 AzPublicIpAddress 建立公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="85e5c-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="85e5c-141">第六個命令會使用 $PublicIp 建立前端 IP 設定，並將其命名為 FrontEndPortConfig01，並將它儲存在 $FrontEndIpConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="85e5c-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="85e5c-142">第七個命令會使用先前建立的 $FrontEndIpConfig $FrontEndPort 來建立偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="85e5c-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="85e5c-143">第八個命令會建立監聽程式的規則。</span><span class="sxs-lookup"><span data-stu-id="85e5c-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="85e5c-144">第九個命令會設定 SKU。</span><span class="sxs-lookup"><span data-stu-id="85e5c-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="85e5c-145">第10個命令會使用先前命令所設定的物件來建立閘道。</span><span class="sxs-lookup"><span data-stu-id="85e5c-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="85e5c-146">範例2：使用 UserAssigned 身分識別來建立應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="85e5c-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Identity = New-AzUserAssignedIdentity -Name "Identity01" -ResourceGroupName "ResourceGroup01" -Location "West US"
PS C:\> $AppgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $Identity.Id
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $AppgwIdentity -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

## <span data-ttu-id="85e5c-147">參數</span><span class="sxs-lookup"><span data-stu-id="85e5c-147">PARAMETERS</span></span>

### <span data-ttu-id="85e5c-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85e5c-148">-AsJob</span></span>
<span data-ttu-id="85e5c-149">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="85e5c-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85e5c-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="85e5c-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="85e5c-151">指定應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="85e5c-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="85e5c-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="85e5c-153">自動縮放設定</span><span class="sxs-lookup"><span data-stu-id="85e5c-153">Autoscale Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="85e5c-154">-BackendAddressPools</span></span>
<span data-ttu-id="85e5c-155">指定應用程式閘道的後端位址集區清單。</span><span class="sxs-lookup"><span data-stu-id="85e5c-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="85e5c-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="85e5c-157">指定應用程式閘道的後端 HTTP 設定清單。</span><span class="sxs-lookup"><span data-stu-id="85e5c-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="85e5c-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="85e5c-159">應用程式閘道的客戶錯誤</span><span class="sxs-lookup"><span data-stu-id="85e5c-159">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85e5c-160">-DefaultProfile</span></span>
<span data-ttu-id="85e5c-161">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="85e5c-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85e5c-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="85e5c-162">-EnableFIPS</span></span>
<span data-ttu-id="85e5c-163">是否已啟用 FIPS。</span><span class="sxs-lookup"><span data-stu-id="85e5c-163">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="85e5c-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="85e5c-164">-EnableHttp2</span></span>
<span data-ttu-id="85e5c-165">是否已啟用 HTTP2。</span><span class="sxs-lookup"><span data-stu-id="85e5c-165">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="85e5c-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="85e5c-166">-FirewallPolicy</span></span>
<span data-ttu-id="85e5c-167">防火牆設定</span><span class="sxs-lookup"><span data-stu-id="85e5c-167">Firewall configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="85e5c-168">-FirewallPolicyId</span></span>
<span data-ttu-id="85e5c-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="85e5c-169">FirewallPolicyId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-170">-Force</span><span class="sxs-lookup"><span data-stu-id="85e5c-170">-Force</span></span>
<span data-ttu-id="85e5c-171">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="85e5c-171">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="85e5c-172">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="85e5c-172">-FrontendIPConfigurations</span></span>
<span data-ttu-id="85e5c-173">指定應用程式閘道的前端 IP 配置清單。</span><span class="sxs-lookup"><span data-stu-id="85e5c-173">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-174">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="85e5c-174">-FrontendPorts</span></span>
<span data-ttu-id="85e5c-175">指定應用程式閘道的前端埠清單。</span><span class="sxs-lookup"><span data-stu-id="85e5c-175">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-176">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="85e5c-176">-GatewayIPConfigurations</span></span>
<span data-ttu-id="85e5c-177">指定應用程式閘道的 IP 配置清單。</span><span class="sxs-lookup"><span data-stu-id="85e5c-177">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-178">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="85e5c-178">-HttpListeners</span></span>
<span data-ttu-id="85e5c-179">指定應用程式閘道的 HTTP 攔截器清單。</span><span class="sxs-lookup"><span data-stu-id="85e5c-179">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-180">身分識別</span><span class="sxs-lookup"><span data-stu-id="85e5c-180">-Identity</span></span>
<span data-ttu-id="85e5c-181">要指派給應用程式閘道的應用程式閘道身分識別。</span><span class="sxs-lookup"><span data-stu-id="85e5c-181">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-182">-位置</span><span class="sxs-lookup"><span data-stu-id="85e5c-182">-Location</span></span>
<span data-ttu-id="85e5c-183">指定要在其中建立應用程式閘道的區域。</span><span class="sxs-lookup"><span data-stu-id="85e5c-183">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="85e5c-184">-名稱</span><span class="sxs-lookup"><span data-stu-id="85e5c-184">-Name</span></span>
<span data-ttu-id="85e5c-185">指定應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="85e5c-185">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="85e5c-186">-探針</span><span class="sxs-lookup"><span data-stu-id="85e5c-186">-Probes</span></span>
<span data-ttu-id="85e5c-187">指定應用程式閘道的探測器。</span><span class="sxs-lookup"><span data-stu-id="85e5c-187">Specifies probes for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-188">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="85e5c-188">-RedirectConfigurations</span></span>
<span data-ttu-id="85e5c-189">重新導向配置清單</span><span class="sxs-lookup"><span data-stu-id="85e5c-189">The list of redirect configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-190">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="85e5c-190">-RequestRoutingRules</span></span>
<span data-ttu-id="85e5c-191">指定應用程式閘道的要求路由規則清單。</span><span class="sxs-lookup"><span data-stu-id="85e5c-191">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85e5c-192">-ResourceGroupName</span></span>
<span data-ttu-id="85e5c-193">指定要在其中建立應用程式閘道的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="85e5c-193">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="85e5c-194">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="85e5c-194">-RewriteRuleSet</span></span>
<span data-ttu-id="85e5c-195">RewriteRuleSet 清單</span><span class="sxs-lookup"><span data-stu-id="85e5c-195">The list of RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-196">-Sku</span><span class="sxs-lookup"><span data-stu-id="85e5c-196">-Sku</span></span>
<span data-ttu-id="85e5c-197">指定應用程式閘道 (SKU) 的庫存單位。</span><span class="sxs-lookup"><span data-stu-id="85e5c-197">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-198">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="85e5c-198">-SslCertificates</span></span>
<span data-ttu-id="85e5c-199">指定 (SSL) 應用程式閘道憑證的安全通訊端層的清單。</span><span class="sxs-lookup"><span data-stu-id="85e5c-199">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-200">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="85e5c-200">-SslPolicy</span></span>
<span data-ttu-id="85e5c-201">指定應用程式閘道的 SSL 原則。</span><span class="sxs-lookup"><span data-stu-id="85e5c-201">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-202">-Tag</span><span class="sxs-lookup"><span data-stu-id="85e5c-202">-Tag</span></span>
<span data-ttu-id="85e5c-203">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="85e5c-203">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="85e5c-204">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="85e5c-204">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="85e5c-205">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="85e5c-205">-TrustedRootCertificate</span></span>
<span data-ttu-id="85e5c-206">受信任的根憑證清單</span><span class="sxs-lookup"><span data-stu-id="85e5c-206">The list of trusted root certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-207">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="85e5c-207">-UrlPathMaps</span></span>
<span data-ttu-id="85e5c-208">指定應用程式閘道的 URL 路徑對應。</span><span class="sxs-lookup"><span data-stu-id="85e5c-208">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-209">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="85e5c-209">-UserAssignedIdentityId</span></span>
<span data-ttu-id="85e5c-210">指派給應用程式閘道的使用者指派身分識別的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="85e5c-210">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-211">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="85e5c-211">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="85e5c-212">指定 (WAF) 設定的 web 應用程式防火牆。</span><span class="sxs-lookup"><span data-stu-id="85e5c-212">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="85e5c-213">您可以使用 Get-AzApplicationGatewayWebApplicationFirewallConfiguration Cmdlet 來取得 WAF。</span><span class="sxs-lookup"><span data-stu-id="85e5c-213">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-214">-Zone</span><span class="sxs-lookup"><span data-stu-id="85e5c-214">-Zone</span></span>
<span data-ttu-id="85e5c-215">顯示應用程式閘道需要來源之位置的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="85e5c-215">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e5c-216">-確認</span><span class="sxs-lookup"><span data-stu-id="85e5c-216">-Confirm</span></span>
<span data-ttu-id="85e5c-217">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="85e5c-217">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85e5c-218">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85e5c-218">-WhatIf</span></span>
<span data-ttu-id="85e5c-219">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="85e5c-219">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85e5c-220">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85e5c-220">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85e5c-221">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e5c-221">CommonParameters</span></span>
<span data-ttu-id="85e5c-222">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85e5c-222">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e5c-223">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85e5c-223">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e5c-224">輸入</span><span class="sxs-lookup"><span data-stu-id="85e5c-224">INPUTS</span></span>

### <span data-ttu-id="85e5c-225">System.object</span><span class="sxs-lookup"><span data-stu-id="85e5c-225">System.String</span></span>

### <span data-ttu-id="85e5c-226">PSApplicationGatewaySku 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="85e5c-226">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="85e5c-227">PSApplicationGatewaySslPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="85e5c-227">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="85e5c-228">PSApplicationGatewayIPConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="85e5c-228">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="85e5c-229">PSApplicationGatewaySslCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="85e5c-229">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="85e5c-230">PSApplicationGatewayAuthenticationCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="85e5c-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="85e5c-231">PSApplicationGatewayTrustedRootCertificate [] （[]）</span><span class="sxs-lookup"><span data-stu-id="85e5c-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="85e5c-232">PSApplicationGatewayFrontendIPConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="85e5c-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="85e5c-233">PSApplicationGatewayFrontendPort [] （[]）</span><span class="sxs-lookup"><span data-stu-id="85e5c-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="85e5c-234">PSApplicationGatewayProbe [] （[]）</span><span class="sxs-lookup"><span data-stu-id="85e5c-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="85e5c-235">PSApplicationGatewayBackendAddressPool [] （[]）</span><span class="sxs-lookup"><span data-stu-id="85e5c-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="85e5c-236">PSApplicationGatewayBackendHttpSettings [] （[]）</span><span class="sxs-lookup"><span data-stu-id="85e5c-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="85e5c-237">PSApplicationGatewayHttpListener [] （[]）</span><span class="sxs-lookup"><span data-stu-id="85e5c-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="85e5c-238">PSApplicationGatewayUrlPathMap [] （[]）</span><span class="sxs-lookup"><span data-stu-id="85e5c-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="85e5c-239">PSApplicationGatewayRequestRoutingRule [] （[]）</span><span class="sxs-lookup"><span data-stu-id="85e5c-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="85e5c-240">PSApplicationGatewayRewriteRuleSet [] （[]）</span><span class="sxs-lookup"><span data-stu-id="85e5c-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="85e5c-241">PSApplicationGatewayRedirectConfiguration [] （[]）</span><span class="sxs-lookup"><span data-stu-id="85e5c-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="85e5c-242">PSApplicationGatewayWebApplicationFirewallConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="85e5c-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="85e5c-243">PSApplicationGatewayAutoscaleConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="85e5c-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="85e5c-244">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="85e5c-244">System.Collections.Hashtable</span></span>

## <span data-ttu-id="85e5c-245">輸出</span><span class="sxs-lookup"><span data-stu-id="85e5c-245">OUTPUTS</span></span>

### <span data-ttu-id="85e5c-246">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="85e5c-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="85e5c-247">筆記</span><span class="sxs-lookup"><span data-stu-id="85e5c-247">NOTES</span></span>

## <span data-ttu-id="85e5c-248">相關連結</span><span class="sxs-lookup"><span data-stu-id="85e5c-248">RELATED LINKS</span></span>

[<span data-ttu-id="85e5c-249">新-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="85e5c-249">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="85e5c-250">新-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="85e5c-250">New-AzApplicationGatewayBackendHttpSettings</span></span>](./New-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="85e5c-251">新-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="85e5c-251">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="85e5c-252">新-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="85e5c-252">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="85e5c-253">新-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="85e5c-253">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="85e5c-254">新-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="85e5c-254">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="85e5c-255">新-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="85e5c-255">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="85e5c-256">新-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="85e5c-256">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="85e5c-257">新-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="85e5c-257">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="85e5c-258">新-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="85e5c-258">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)