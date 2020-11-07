---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: fe9449eedaedfa08880548ceda769835d6eb3f7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790745"
---
# <span data-ttu-id="5eef1-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="5eef1-101">New-AzVpnSite</span></span>

## <span data-ttu-id="5eef1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5eef1-102">SYNOPSIS</span></span>
<span data-ttu-id="5eef1-103">建立新的 Azure VpnSite 資源。</span><span class="sxs-lookup"><span data-stu-id="5eef1-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="5eef1-104">這是使用 Cortex 虛擬中樞上傳至 Azure 以進行 S2S 連線的客戶分支的 RM 表示。</span><span class="sxs-lookup"><span data-stu-id="5eef1-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="5eef1-105">句法</span><span class="sxs-lookup"><span data-stu-id="5eef1-105">SYNTAX</span></span>

### <span data-ttu-id="5eef1-106">ByVirtualWanNameByVpnSiteIpAddress (預設) </span><span class="sxs-lookup"><span data-stu-id="5eef1-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5eef1-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="5eef1-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5eef1-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="5eef1-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5eef1-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="5eef1-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5eef1-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="5eef1-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5eef1-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="5eef1-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5eef1-112">說明</span><span class="sxs-lookup"><span data-stu-id="5eef1-112">DESCRIPTION</span></span>
<span data-ttu-id="5eef1-113">建立新的 Azure VpnSite 資源。</span><span class="sxs-lookup"><span data-stu-id="5eef1-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="5eef1-114">這是使用 Cortex 虛擬中樞上傳至 Azure 以進行 S2S 連線的客戶分支的 RM 表示。</span><span class="sxs-lookup"><span data-stu-id="5eef1-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="5eef1-115">示例</span><span class="sxs-lookup"><span data-stu-id="5eef1-115">EXAMPLES</span></span>

### <span data-ttu-id="5eef1-116">範例1</span><span class="sxs-lookup"><span data-stu-id="5eef1-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "nonlinkSite"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "nonlinkSite" -Name myVirtualWAN -Location "East US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "nonlinkSite" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : nonlinkSite
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="5eef1-117">上述將會在 Azure 中的 [nonlinkSite] 資源群組中，建立一個 [美國] 資源群組、[東部] 的虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="5eef1-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="5eef1-118">接著，它會建立代表客戶分支的 VpnSite，並將它連結至虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="5eef1-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="5eef1-119">接著，就可以使用 [New-AzVpnConnection] 命令設定 IPSec 連線與此分支與 VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="5eef1-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="5eef1-120">範例2</span><span class="sxs-lookup"><span data-stu-id="5eef1-120">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "multilink"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName multilink -Name myVirtualWAN -Location "East US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "multilink" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)
```

<span data-ttu-id="5eef1-121">上述將會在 Azure 中的 [多重連結] 資源群組中，建立一個資源群組、虛擬 WAN 及 VpnSite，並在美國使用 1 VpnSiteLinks。</span><span class="sxs-lookup"><span data-stu-id="5eef1-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

## <span data-ttu-id="5eef1-122">參數</span><span class="sxs-lookup"><span data-stu-id="5eef1-122">PARAMETERS</span></span>

### <span data-ttu-id="5eef1-123">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="5eef1-123">-AddressSpace</span></span>
<span data-ttu-id="5eef1-124">虛擬網路的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="5eef1-124">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="5eef1-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5eef1-125">-AsJob</span></span>
<span data-ttu-id="5eef1-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5eef1-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5eef1-127">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="5eef1-127">-BgpAsn</span></span>
<span data-ttu-id="5eef1-128">此 VpnSite 的 BGP ASN。</span><span class="sxs-lookup"><span data-stu-id="5eef1-128">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-129">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="5eef1-129">-BgpPeeringAddress</span></span>
<span data-ttu-id="5eef1-130">此 VpnSite 的 BGP 對等位址。</span><span class="sxs-lookup"><span data-stu-id="5eef1-130">The BGP Peering Address for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-131">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="5eef1-131">-BgpPeeringWeight</span></span>
<span data-ttu-id="5eef1-132">此 VpnSite 的 BGP 對等權重。</span><span class="sxs-lookup"><span data-stu-id="5eef1-132">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eef1-133">-DefaultProfile</span></span>
<span data-ttu-id="5eef1-134">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5eef1-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eef1-135">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="5eef1-135">-DeviceModel</span></span>
<span data-ttu-id="5eef1-136">遠端 vpn 裝置的裝置模型。</span><span class="sxs-lookup"><span data-stu-id="5eef1-136">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="5eef1-137">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="5eef1-137">-DeviceVendor</span></span>
<span data-ttu-id="5eef1-138">遠端 vpn 裝置的裝置廠商。</span><span class="sxs-lookup"><span data-stu-id="5eef1-138">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="5eef1-139">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="5eef1-139">-IpAddress</span></span>
<span data-ttu-id="5eef1-140">此 VpnSite 的 IPAddress。</span><span class="sxs-lookup"><span data-stu-id="5eef1-140">The IPAddress for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-141">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="5eef1-141">-LinkSpeedInMbps</span></span>
<span data-ttu-id="5eef1-142">遠端 vpn 裝置的裝置模型。</span><span class="sxs-lookup"><span data-stu-id="5eef1-142">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-143">-位置</span><span class="sxs-lookup"><span data-stu-id="5eef1-143">-Location</span></span>
<span data-ttu-id="5eef1-144">資源位置。</span><span class="sxs-lookup"><span data-stu-id="5eef1-144">The resource location.</span></span>

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

### <span data-ttu-id="5eef1-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="5eef1-145">-Name</span></span>
<span data-ttu-id="5eef1-146">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5eef1-146">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eef1-147">-ResourceGroupName</span></span>
<span data-ttu-id="5eef1-148">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5eef1-148">The resource name.</span></span>

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

### <span data-ttu-id="5eef1-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="5eef1-149">-Tag</span></span>
<span data-ttu-id="5eef1-150">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="5eef1-150">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-151">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="5eef1-151">-VirtualWan</span></span>
<span data-ttu-id="5eef1-152">此 VpnSite 需要連線至的 VirtualWan。</span><span class="sxs-lookup"><span data-stu-id="5eef1-152">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-153">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="5eef1-153">-VirtualWanId</span></span>
<span data-ttu-id="5eef1-154">此 VpnSite 的 ResourceId VirtualWan 需要連線至。</span><span class="sxs-lookup"><span data-stu-id="5eef1-154">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-155">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="5eef1-155">-VirtualWanName</span></span>
<span data-ttu-id="5eef1-156">此 VpnSite 需要連線至的 VirtualWan 名稱。</span><span class="sxs-lookup"><span data-stu-id="5eef1-156">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-157">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eef1-157">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="5eef1-158">此 VpnSite 需要連線至之 VirtualWan 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="5eef1-158">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-159">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="5eef1-159">-VpnSiteLink</span></span>
<span data-ttu-id="5eef1-160">此 VpnSite 的 VpnSiteLinks 清單。</span><span class="sxs-lookup"><span data-stu-id="5eef1-160">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: ByVirtualWanNameByVpnSiteLinkObject, ByVirtualWanObjectByVpnSiteLinkObject, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-161">-確認</span><span class="sxs-lookup"><span data-stu-id="5eef1-161">-Confirm</span></span>
<span data-ttu-id="5eef1-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5eef1-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eef1-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eef1-163">-WhatIf</span></span>
<span data-ttu-id="5eef1-164">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5eef1-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eef1-165">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5eef1-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eef1-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eef1-166">CommonParameters</span></span>
<span data-ttu-id="5eef1-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5eef1-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eef1-168">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5eef1-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eef1-169">輸入</span><span class="sxs-lookup"><span data-stu-id="5eef1-169">INPUTS</span></span>

### <span data-ttu-id="5eef1-170">所有</span><span class="sxs-lookup"><span data-stu-id="5eef1-170">None</span></span>

## <span data-ttu-id="5eef1-171">輸出</span><span class="sxs-lookup"><span data-stu-id="5eef1-171">OUTPUTS</span></span>

### <span data-ttu-id="5eef1-172">PSVpnSite 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5eef1-172">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="5eef1-173">筆記</span><span class="sxs-lookup"><span data-stu-id="5eef1-173">NOTES</span></span>

## <span data-ttu-id="5eef1-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="5eef1-174">RELATED LINKS</span></span>

[<span data-ttu-id="5eef1-175">AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="5eef1-175">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="5eef1-176">移除-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="5eef1-176">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="5eef1-177">更新-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="5eef1-177">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)