---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: cf120e8e9ca9e0dad8f4d430c7f207d40fcfab3b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286984"
---
# <span data-ttu-id="5627e-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5627e-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="5627e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5627e-102">SYNOPSIS</span></span>
<span data-ttu-id="5627e-103">從 VM 取得下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="5627e-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="5627e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5627e-104">SYNTAX</span></span>

### <span data-ttu-id="5627e-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="5627e-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5627e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5627e-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5627e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5627e-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5627e-108">說明</span><span class="sxs-lookup"><span data-stu-id="5627e-108">DESCRIPTION</span></span>
<span data-ttu-id="5627e-109">Get-AzNetworkWatcherNextHop Cmdlet 會從 VM 取得下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="5627e-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="5627e-110">下一個躍點可讓您查看 Azure 資源類型、該資源的關聯 IP 位址，以及負責路由的路由表規則。</span><span class="sxs-lookup"><span data-stu-id="5627e-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="5627e-111">示例</span><span class="sxs-lookup"><span data-stu-id="5627e-111">EXAMPLES</span></span>

### <span data-ttu-id="5627e-112">範例1：在與網際網路 IP 通訊時取得下一個躍點</span><span class="sxs-lookup"><span data-stu-id="5627e-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="5627e-113">取得從指定虛擬機器上的主要網路介面傳出通訊的下一個躍點，以 204.79.197.200 (www.bing.com) </span><span class="sxs-lookup"><span data-stu-id="5627e-113">Gets the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Machine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="5627e-114">參數</span><span class="sxs-lookup"><span data-stu-id="5627e-114">PARAMETERS</span></span>

### <span data-ttu-id="5627e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5627e-115">-AsJob</span></span>
<span data-ttu-id="5627e-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5627e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5627e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5627e-117">-DefaultProfile</span></span>
<span data-ttu-id="5627e-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5627e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5627e-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="5627e-119">-DestinationIPAddress</span></span>
<span data-ttu-id="5627e-120">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="5627e-120">Destination IP address.</span></span>

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

### <span data-ttu-id="5627e-121">-位置</span><span class="sxs-lookup"><span data-stu-id="5627e-121">-Location</span></span>
<span data-ttu-id="5627e-122">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="5627e-122">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5627e-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5627e-123">-NetworkWatcher</span></span>
<span data-ttu-id="5627e-124">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="5627e-124">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5627e-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5627e-125">-NetworkWatcherName</span></span>
<span data-ttu-id="5627e-126">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="5627e-126">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5627e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5627e-127">-ResourceGroupName</span></span>
<span data-ttu-id="5627e-128">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5627e-128">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5627e-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="5627e-129">-SourceIPAddress</span></span>
<span data-ttu-id="5627e-130">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="5627e-130">Source IP address.</span></span>

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

### <span data-ttu-id="5627e-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="5627e-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="5627e-132">目標網路介面 Id。</span><span class="sxs-lookup"><span data-stu-id="5627e-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="5627e-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="5627e-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="5627e-134">目標虛擬機器 ID。</span><span class="sxs-lookup"><span data-stu-id="5627e-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="5627e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5627e-135">CommonParameters</span></span>
<span data-ttu-id="5627e-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5627e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5627e-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5627e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5627e-138">輸入</span><span class="sxs-lookup"><span data-stu-id="5627e-138">INPUTS</span></span>

### <span data-ttu-id="5627e-139">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5627e-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="5627e-140">System.object</span><span class="sxs-lookup"><span data-stu-id="5627e-140">System.String</span></span>

## <span data-ttu-id="5627e-141">輸出</span><span class="sxs-lookup"><span data-stu-id="5627e-141">OUTPUTS</span></span>

### <span data-ttu-id="5627e-142">PSNextHopResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5627e-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="5627e-143">筆記</span><span class="sxs-lookup"><span data-stu-id="5627e-143">NOTES</span></span>
<span data-ttu-id="5627e-144">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，下一步，hop</span><span class="sxs-lookup"><span data-stu-id="5627e-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="5627e-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="5627e-145">RELATED LINKS</span></span>

[<span data-ttu-id="5627e-146">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5627e-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="5627e-147">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5627e-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5627e-148">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5627e-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5627e-149">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5627e-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5627e-150">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5627e-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5627e-151">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5627e-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="5627e-152">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5627e-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5627e-153">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5627e-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5627e-154">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5627e-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5627e-155">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5627e-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5627e-156">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5627e-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5627e-157">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5627e-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5627e-158">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5627e-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5627e-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5627e-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5627e-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5627e-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="5627e-161">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5627e-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5627e-162">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5627e-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5627e-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5627e-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5627e-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5627e-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5627e-165">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5627e-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5627e-166">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5627e-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5627e-167">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5627e-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5627e-168">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5627e-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5627e-169">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5627e-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5627e-170">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5627e-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="5627e-171">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5627e-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="5627e-172">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5627e-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)