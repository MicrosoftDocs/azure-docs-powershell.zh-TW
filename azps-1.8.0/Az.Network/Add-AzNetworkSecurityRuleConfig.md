---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 3e11b1ca7b83a4f01ce2d344874f4da02b399221
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622143"
---
# <span data-ttu-id="c58e2-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c58e2-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="c58e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c58e2-102">SYNOPSIS</span></span>
<span data-ttu-id="c58e2-103">新增網路安全規則設定至網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="c58e2-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="c58e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="c58e2-104">SYNTAX</span></span>

### <span data-ttu-id="c58e2-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="c58e2-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c58e2-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c58e2-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c58e2-107">說明</span><span class="sxs-lookup"><span data-stu-id="c58e2-107">DESCRIPTION</span></span>
<span data-ttu-id="c58e2-108">**AzNetworkSecurityRuleConfig** Cmdlet 會將網路安全規則設定新增至 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="c58e2-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="c58e2-109">示例</span><span class="sxs-lookup"><span data-stu-id="c58e2-109">EXAMPLES</span></span>

### <span data-ttu-id="c58e2-110">1：新增網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="c58e2-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="c58e2-111">第一個命令會從資源群組 "rg1" 檢索名為 "nsg1" 的 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="c58e2-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="c58e2-112">第二個命令會將一個名為「rdp-rule」的網路安全規則新增，允許從埠3389上的網際網路通訊到檢索到的網路安全群組物件。</span><span class="sxs-lookup"><span data-stu-id="c58e2-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="c58e2-113">保持已修改的 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="c58e2-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="c58e2-114">2：使用應用程式安全性群組新增新的安全性規則</span><span class="sxs-lookup"><span data-stu-id="c58e2-114">2: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="c58e2-115">首先，我們會建立兩個新的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="c58e2-115">First, we create two new application security groups.</span></span> <span data-ttu-id="c58e2-116">接著，我們會從資源群組「rg1」檢索名為「nsg1」的 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="c58e2-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="c58e2-117">然後將名為 "rdp-rule" 的網路安全性規則新增至它。</span><span class="sxs-lookup"><span data-stu-id="c58e2-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="c58e2-118">此規則允許從應用程式安全性群組 "srcAsg" 中的所有 IP 設定到埠3389上 "destAsg" 的所有 ip 設定的流量。</span><span class="sxs-lookup"><span data-stu-id="c58e2-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="c58e2-119">新增規則之後，我們會保留已修改的 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="c58e2-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="c58e2-120">參數</span><span class="sxs-lookup"><span data-stu-id="c58e2-120">PARAMETERS</span></span>

### <span data-ttu-id="c58e2-121">-Access</span><span class="sxs-lookup"><span data-stu-id="c58e2-121">-Access</span></span>
<span data-ttu-id="c58e2-122">指定是否允許或拒絕網路流量。</span><span class="sxs-lookup"><span data-stu-id="c58e2-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="c58e2-123">此參數可接受的值為： [允許] 和 [拒絕]。</span><span class="sxs-lookup"><span data-stu-id="c58e2-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c58e2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c58e2-124">-DefaultProfile</span></span>
<span data-ttu-id="c58e2-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c58e2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c58e2-126">-描述</span><span class="sxs-lookup"><span data-stu-id="c58e2-126">-Description</span></span>
<span data-ttu-id="c58e2-127">指定網路安全規則配置的描述。</span><span class="sxs-lookup"><span data-stu-id="c58e2-127">Specifies a description of a network security rule configuration.</span></span>

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

### <span data-ttu-id="c58e2-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c58e2-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="c58e2-129">指定目的地位址首碼。</span><span class="sxs-lookup"><span data-stu-id="c58e2-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="c58e2-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c58e2-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c58e2-131">未類別的域間路由 (CIDR) 位址</span><span class="sxs-lookup"><span data-stu-id="c58e2-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="c58e2-132">目的地 IP 位址範圍</span><span class="sxs-lookup"><span data-stu-id="c58e2-132">A destination IP address range</span></span>
- <span data-ttu-id="c58e2-133">萬用字元 ( \* ) 若要與任何 IP 位址相符，您可以使用 VirtualNetwork、AzureLoadBalancer 和 Internet 等標記。</span><span class="sxs-lookup"><span data-stu-id="c58e2-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="c58e2-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c58e2-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="c58e2-135">針對規則設定為目的地的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="c58e2-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="c58e2-136">它不能與 "DestinationAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c58e2-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c58e2-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c58e2-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="c58e2-138">針對規則設定為目的地的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="c58e2-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="c58e2-139">它不能與 "DestinationAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c58e2-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c58e2-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="c58e2-140">-DestinationPortRange</span></span>
<span data-ttu-id="c58e2-141">指定目的地埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="c58e2-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="c58e2-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c58e2-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c58e2-143">整數</span><span class="sxs-lookup"><span data-stu-id="c58e2-143">An integer</span></span>
- <span data-ttu-id="c58e2-144">0到65535之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="c58e2-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="c58e2-145">萬用字元 ( \* ) 與任何埠相符</span><span class="sxs-lookup"><span data-stu-id="c58e2-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="c58e2-146">方向</span><span class="sxs-lookup"><span data-stu-id="c58e2-146">-Direction</span></span>
<span data-ttu-id="c58e2-147">指定是否要針對傳入或傳出流量評估規則。</span><span class="sxs-lookup"><span data-stu-id="c58e2-147">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="c58e2-148">此參數可接受的值為：入站和出站。</span><span class="sxs-lookup"><span data-stu-id="c58e2-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c58e2-149">-名稱</span><span class="sxs-lookup"><span data-stu-id="c58e2-149">-Name</span></span>
<span data-ttu-id="c58e2-150">指定網路安全規則配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="c58e2-150">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="c58e2-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c58e2-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="c58e2-152">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="c58e2-152">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="c58e2-153">這個 Cmdlet 會將網路安全規則設定新增至此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="c58e2-153">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c58e2-154">-優先順序</span><span class="sxs-lookup"><span data-stu-id="c58e2-154">-Priority</span></span>
<span data-ttu-id="c58e2-155">指定規則配置的優先順序。</span><span class="sxs-lookup"><span data-stu-id="c58e2-155">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="c58e2-156">此參數可接受的值為：100和4096之間的整數。</span><span class="sxs-lookup"><span data-stu-id="c58e2-156">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="c58e2-157">對於集合中的每個規則，優先順序編號必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="c58e2-157">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="c58e2-158">優先順序編號越低，規則的優先順序就越高。</span><span class="sxs-lookup"><span data-stu-id="c58e2-158">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c58e2-159">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="c58e2-159">-Protocol</span></span>
<span data-ttu-id="c58e2-160">指定規則配置適用的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c58e2-160">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="c58e2-161">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c58e2-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c58e2-162">Tcp-out</span><span class="sxs-lookup"><span data-stu-id="c58e2-162">Tcp</span></span>
- <span data-ttu-id="c58e2-163">Udp-in</span><span class="sxs-lookup"><span data-stu-id="c58e2-163">Udp</span></span>
- <span data-ttu-id="c58e2-164">萬用字元 ( \* ) 與以上兩個相符</span><span class="sxs-lookup"><span data-stu-id="c58e2-164">Wildcard character (\*) to match both</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c58e2-165">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c58e2-165">-SourceAddressPrefix</span></span>
<span data-ttu-id="c58e2-166">指定來源位址首碼。</span><span class="sxs-lookup"><span data-stu-id="c58e2-166">Specifies a source address prefix.</span></span>
<span data-ttu-id="c58e2-167">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c58e2-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c58e2-168">CIDR</span><span class="sxs-lookup"><span data-stu-id="c58e2-168">A CIDR</span></span>
- <span data-ttu-id="c58e2-169">來源 IP 範圍</span><span class="sxs-lookup"><span data-stu-id="c58e2-169">A source IP range</span></span>
- <span data-ttu-id="c58e2-170">通配字元 ( \* ) ，以符合任何 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c58e2-170">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="c58e2-171">您也可以使用 [VirtualNetwork]、[AzureLoadBalancer] 和 [網際網路] 等標記。</span><span class="sxs-lookup"><span data-stu-id="c58e2-171">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="c58e2-172">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c58e2-172">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="c58e2-173">針對規則設定為 [來源] 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="c58e2-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="c58e2-174">它不能與 "SourceAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c58e2-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c58e2-175">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c58e2-175">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="c58e2-176">針對規則設定為 [來源] 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="c58e2-176">The application security group set as source for the rule.</span></span> <span data-ttu-id="c58e2-177">它不能與 "SourceAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c58e2-177">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c58e2-178">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="c58e2-178">-SourcePortRange</span></span>
<span data-ttu-id="c58e2-179">指定來源埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="c58e2-179">Specifies a source port or range.</span></span>
<span data-ttu-id="c58e2-180">這個值會以整數表示，以0到65535之間的範圍，或以萬用字元字元 ( \* ) 來與任何來源埠相符。</span><span class="sxs-lookup"><span data-stu-id="c58e2-180">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

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

### <span data-ttu-id="c58e2-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c58e2-181">CommonParameters</span></span>
<span data-ttu-id="c58e2-182">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c58e2-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c58e2-183">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c58e2-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c58e2-184">輸入</span><span class="sxs-lookup"><span data-stu-id="c58e2-184">INPUTS</span></span>

### <span data-ttu-id="c58e2-185">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c58e2-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="c58e2-186">輸出</span><span class="sxs-lookup"><span data-stu-id="c58e2-186">OUTPUTS</span></span>

### <span data-ttu-id="c58e2-187">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c58e2-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="c58e2-188">筆記</span><span class="sxs-lookup"><span data-stu-id="c58e2-188">NOTES</span></span>

## <span data-ttu-id="c58e2-189">相關連結</span><span class="sxs-lookup"><span data-stu-id="c58e2-189">RELATED LINKS</span></span>

[<span data-ttu-id="c58e2-190">AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c58e2-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c58e2-191">新-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c58e2-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c58e2-192">移除-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c58e2-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c58e2-193">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c58e2-193">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

