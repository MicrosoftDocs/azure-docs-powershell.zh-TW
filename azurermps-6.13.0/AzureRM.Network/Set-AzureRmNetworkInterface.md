---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterface.md
ms.openlocfilehash: 771681739e8afd95215c8789a6ac849835bb2c8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623406"
---
# <span data-ttu-id="5a80a-101">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5a80a-101">Set-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="5a80a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a80a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a80a-103">設定網路介面的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="5a80a-103">Sets the goal state for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a80a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a80a-104">SYNTAX</span></span>

```
Set-AzureRmNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a80a-105">說明</span><span class="sxs-lookup"><span data-stu-id="5a80a-105">DESCRIPTION</span></span>
<span data-ttu-id="5a80a-106">**AzureRmNetworkInterface 設定** 的是 Azure network 介面的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="5a80a-106">The **Set-AzureRmNetworkInterface** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="5a80a-107">示例</span><span class="sxs-lookup"><span data-stu-id="5a80a-107">EXAMPLES</span></span>

### <span data-ttu-id="5a80a-108">範例1：設定網路介面</span><span class="sxs-lookup"><span data-stu-id="5a80a-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzureRmNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="5a80a-109">這個範例會設定網路介面。</span><span class="sxs-lookup"><span data-stu-id="5a80a-109">This example configures a network interface.</span></span>
<span data-ttu-id="5a80a-110">第一個命令會在資源群組 ResourceGroup1 中取得名為 NetworkInterface1 的網路介面。</span><span class="sxs-lookup"><span data-stu-id="5a80a-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="5a80a-111">第二個命令會設定 IP 配置的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="5a80a-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="5a80a-112">第三個命令會將專用 IP 配置方法設定為 Static。</span><span class="sxs-lookup"><span data-stu-id="5a80a-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="5a80a-113">第四個命令會在網路介面上設定標記。</span><span class="sxs-lookup"><span data-stu-id="5a80a-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="5a80a-114">第五個命令使用儲存在 $Nic 變數中的資訊來設定網路介面。</span><span class="sxs-lookup"><span data-stu-id="5a80a-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="5a80a-115">範例2：變更網路介面上的 DNS 設定</span><span class="sxs-lookup"><span data-stu-id="5a80a-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="5a80a-116">第一個命令會取得名為 NetworkInterface1 的網路介面，該網路介面存在於資源群組 ResourceGroup1 中。</span><span class="sxs-lookup"><span data-stu-id="5a80a-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="5a80a-117">第二個命令會將 DNS 伺服器192.168.1.100 新增到這個介面。</span><span class="sxs-lookup"><span data-stu-id="5a80a-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="5a80a-118">第三個命令會將這些變更套用至網路介面。</span><span class="sxs-lookup"><span data-stu-id="5a80a-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="5a80a-119">若要移除 DNS 伺服器，請遵循上面所列的命令，但要取代 "。新增 "with"。第二個命令中的 [移除]。</span><span class="sxs-lookup"><span data-stu-id="5a80a-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="5a80a-120">範例3：在網路介面上啟用 IP forwading</span><span class="sxs-lookup"><span data-stu-id="5a80a-120">Example 3: Enable IP forwading on a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="5a80a-121">第一個命令會取得名為 NetworkInterface1 的現有網路介面，並將它儲存在 $nic 變數中。</span><span class="sxs-lookup"><span data-stu-id="5a80a-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="5a80a-122">第二個命令會將 IP 轉寄值變更為 true。</span><span class="sxs-lookup"><span data-stu-id="5a80a-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="5a80a-123">最後，第三個命令會將變更套用至網路介面。</span><span class="sxs-lookup"><span data-stu-id="5a80a-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="5a80a-124">若要在網路介面上停用 IP 轉寄功能，請遵循範例範例，但務必將第二個命令改為「$nic。EnableIPForwarding = 0 "。</span><span class="sxs-lookup"><span data-stu-id="5a80a-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="5a80a-125">範例4：變更網路介面的子網</span><span class="sxs-lookup"><span data-stu-id="5a80a-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzureRmVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzureRmVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="5a80a-126">第一個命令會取得網路介面 NetworkInterface1，並將它儲存在 $nic 變數中。</span><span class="sxs-lookup"><span data-stu-id="5a80a-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="5a80a-127">第二個命令會取得與網路介面將要關聯之子網相關聯的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="5a80a-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="5a80a-128">第二個命令會取得子網，並將它儲存在 $subnet 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="5a80a-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="5a80a-129">第三個命令會將網路介面的主要私人 IP 位址與新的子網相關聯。</span><span class="sxs-lookup"><span data-stu-id="5a80a-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="5a80a-130">最後，最後一個命令會在網路介面上套用這些變更。</span><span class="sxs-lookup"><span data-stu-id="5a80a-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="5a80a-131">您必須先動態使用 IP 設定，才能變更子網。</span><span class="sxs-lookup"><span data-stu-id="5a80a-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="5a80a-132">如果您有靜態 IP 設定，請先將它變更為 [動態]，然後再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="5a80a-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="5a80a-133">如果網路介面有多個 IP 設定，則在執行最後一個 Set-AzureRmNetworkInterface 命令之前，必須完成所有這些 IP 設定的第四個命令。</span><span class="sxs-lookup"><span data-stu-id="5a80a-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzureRmNetworkInterface command is executed.</span></span> <span data-ttu-id="5a80a-134">您可以在第四個命令中完成，但將 "0" 取代為適當的數位。</span><span class="sxs-lookup"><span data-stu-id="5a80a-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="5a80a-135">如果網路介面具有 N 個 IP 配置，則必須存在這些命令的 N-1。</span><span class="sxs-lookup"><span data-stu-id="5a80a-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="5a80a-136">範例5：將網路安全群組關聯/取消關聯至網路介面</span><span class="sxs-lookup"><span data-stu-id="5a80a-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="5a80a-137">第一個命令會取得名為 NetworkInterface1 的現有網路介面，並將它儲存在 $nic 變數中。</span><span class="sxs-lookup"><span data-stu-id="5a80a-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="5a80a-138">第二個命令會取得一個名為 MyNSG 的現有網路安全性群組，並將它儲存在 $nsg 變數中。</span><span class="sxs-lookup"><span data-stu-id="5a80a-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="5a80a-139">第四個命令會將 $nsg 指派給 $nic。</span><span class="sxs-lookup"><span data-stu-id="5a80a-139">The forth command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="5a80a-140">最後，第五個命令會將變更套用至網路介面。</span><span class="sxs-lookup"><span data-stu-id="5a80a-140">Finally, the fifth command applies the changes to the Network interface.</span></span> <span data-ttu-id="5a80a-141">若要將網路安全群組與網路介面取消關聯，請在第四個命令中簡單地取代 $nsg $null。</span><span class="sxs-lookup"><span data-stu-id="5a80a-141">To dissociate network security groups from a network interface, simple replace $nsg in the forth command with $null.</span></span>

## <span data-ttu-id="5a80a-142">參數</span><span class="sxs-lookup"><span data-stu-id="5a80a-142">PARAMETERS</span></span>

### <span data-ttu-id="5a80a-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a80a-143">-AsJob</span></span>
<span data-ttu-id="5a80a-144">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5a80a-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a80a-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a80a-145">-DefaultProfile</span></span>
<span data-ttu-id="5a80a-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a80a-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a80a-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5a80a-147">-NetworkInterface</span></span>
<span data-ttu-id="5a80a-148">指定代表網路介面目標狀態的 **NetworkInterface** 物件。</span><span class="sxs-lookup"><span data-stu-id="5a80a-148">Specifies a **NetworkInterface** object that represents the goal state for a network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a80a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a80a-149">CommonParameters</span></span>
<span data-ttu-id="5a80a-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a80a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a80a-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5a80a-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a80a-152">輸入</span><span class="sxs-lookup"><span data-stu-id="5a80a-152">INPUTS</span></span>

### <span data-ttu-id="5a80a-153">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5a80a-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>
<span data-ttu-id="5a80a-154">參數： NetworkInterface (ByValue) </span><span class="sxs-lookup"><span data-stu-id="5a80a-154">Parameters: NetworkInterface (ByValue)</span></span>

## <span data-ttu-id="5a80a-155">輸出</span><span class="sxs-lookup"><span data-stu-id="5a80a-155">OUTPUTS</span></span>

### <span data-ttu-id="5a80a-156">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5a80a-156">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="5a80a-157">筆記</span><span class="sxs-lookup"><span data-stu-id="5a80a-157">NOTES</span></span>

## <span data-ttu-id="5a80a-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a80a-158">RELATED LINKS</span></span>

[<span data-ttu-id="5a80a-159">AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5a80a-159">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="5a80a-160">AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5a80a-160">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="5a80a-161">新-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5a80a-161">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="5a80a-162">移除-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5a80a-162">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)