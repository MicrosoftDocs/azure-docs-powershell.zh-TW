---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: f8e51258a56051edf99aa1ec0cfa5e252e0ac0d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789293"
---
# <span data-ttu-id="d80ab-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d80ab-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="d80ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d80ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d80ab-103">建立新的 [資料包捕獲篩選] 物件。</span><span class="sxs-lookup"><span data-stu-id="d80ab-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="d80ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="d80ab-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d80ab-105">說明</span><span class="sxs-lookup"><span data-stu-id="d80ab-105">DESCRIPTION</span></span>
<span data-ttu-id="d80ab-106">New-AzPacketCaptureFilterConfig Cmdlet 會建立新的 [資料包捕獲] 篩選物件。</span><span class="sxs-lookup"><span data-stu-id="d80ab-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="d80ab-107">這個物件是用來限制在資料包捕獲會話期間使用指定準則捕獲的資料包類型。</span><span class="sxs-lookup"><span data-stu-id="d80ab-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="d80ab-108">New-AzNetworkWatcherPacketCapture Cmdlet 可以接受多個篩選物件，以啟用可撰寫的捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="d80ab-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="d80ab-109">示例</span><span class="sxs-lookup"><span data-stu-id="d80ab-109">EXAMPLES</span></span>

### <span data-ttu-id="d80ab-110">範例1：使用多個篩選建立資料包捕獲</span><span class="sxs-lookup"><span data-stu-id="d80ab-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="d80ab-111">在這個範例中，我們會建立名為 "PacketCaptureTest" 的資料包捕獲，並提供多個篩選和時間限制。</span><span class="sxs-lookup"><span data-stu-id="d80ab-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="d80ab-112">會話完成後，就會將它儲存到指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="d80ab-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="d80ab-113">注意：必須在目標虛擬機器上安裝 Azure 網路觀察程式延伸，才能建立資料包捕獲。</span><span class="sxs-lookup"><span data-stu-id="d80ab-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="d80ab-114">參數</span><span class="sxs-lookup"><span data-stu-id="d80ab-114">PARAMETERS</span></span>

### <span data-ttu-id="d80ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d80ab-115">-DefaultProfile</span></span>
<span data-ttu-id="d80ab-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d80ab-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d80ab-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="d80ab-117">-LocalIPAddress</span></span>
<span data-ttu-id="d80ab-118">指定要篩選的本機 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d80ab-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="d80ab-119">[範例] 輸入： [127.0.0.1 "代表單一位址專案。</span><span class="sxs-lookup"><span data-stu-id="d80ab-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="d80ab-120">範圍的 "127.0.0.1-127.0.0.255"。</span><span class="sxs-lookup"><span data-stu-id="d80ab-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="d80ab-121">"127.0.0.1; 127.0.0.5;" 代表多個專案。</span><span class="sxs-lookup"><span data-stu-id="d80ab-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="d80ab-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="d80ab-122">-LocalPort</span></span>
<span data-ttu-id="d80ab-123">指定要篩選的本機 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d80ab-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="d80ab-124">[範例] 輸入： [127.0.0.1 "代表單一位址專案。</span><span class="sxs-lookup"><span data-stu-id="d80ab-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="d80ab-125">範圍的 "127.0.0.1-127.0.0.255"。</span><span class="sxs-lookup"><span data-stu-id="d80ab-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="d80ab-126">"127.0.0.1; 127.0.0.5;" 代表多個專案。</span><span class="sxs-lookup"><span data-stu-id="d80ab-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="d80ab-127">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="d80ab-127">-Protocol</span></span>
<span data-ttu-id="d80ab-128">指定要篩選的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d80ab-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="d80ab-129">可接受的值 "TCP"，"UDP"，"Any"</span><span class="sxs-lookup"><span data-stu-id="d80ab-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d80ab-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="d80ab-130">-RemoteIPAddress</span></span>
<span data-ttu-id="d80ab-131">指定要篩選的遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d80ab-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="d80ab-132">[範例] 輸入： [127.0.0.1 "代表單一位址專案。</span><span class="sxs-lookup"><span data-stu-id="d80ab-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="d80ab-133">範圍的 "127.0.0.1-127.0.0.255"。</span><span class="sxs-lookup"><span data-stu-id="d80ab-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="d80ab-134">"127.0.0.1; 127.0.0.5;" 代表多個專案。</span><span class="sxs-lookup"><span data-stu-id="d80ab-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="d80ab-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="d80ab-135">-RemotePort</span></span>
<span data-ttu-id="d80ab-136">指定要篩選的遠端埠。</span><span class="sxs-lookup"><span data-stu-id="d80ab-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="d80ab-137">遠端埠範例輸入：「80」（適用于單一端口專案）。</span><span class="sxs-lookup"><span data-stu-id="d80ab-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="d80ab-138">範圍的 "80-85"。</span><span class="sxs-lookup"><span data-stu-id="d80ab-138">"80-85" for range.</span></span>
<span data-ttu-id="d80ab-139">"80; 443;" （針對多個專案）。</span><span class="sxs-lookup"><span data-stu-id="d80ab-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="d80ab-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d80ab-140">CommonParameters</span></span>
<span data-ttu-id="d80ab-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d80ab-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d80ab-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d80ab-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d80ab-143">輸入</span><span class="sxs-lookup"><span data-stu-id="d80ab-143">INPUTS</span></span>

### <span data-ttu-id="d80ab-144">System.object</span><span class="sxs-lookup"><span data-stu-id="d80ab-144">System.String</span></span>

## <span data-ttu-id="d80ab-145">輸出</span><span class="sxs-lookup"><span data-stu-id="d80ab-145">OUTPUTS</span></span>

### <span data-ttu-id="d80ab-146">PSPacketCaptureFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d80ab-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="d80ab-147">筆記</span><span class="sxs-lookup"><span data-stu-id="d80ab-147">NOTES</span></span>
<span data-ttu-id="d80ab-148">關鍵字： azure、azurerm、arm、資源、管理、管理員、網路、網路、觀察者、資料包、捕獲、流量、篩選器</span><span class="sxs-lookup"><span data-stu-id="d80ab-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="d80ab-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="d80ab-149">RELATED LINKS</span></span>

[<span data-ttu-id="d80ab-150">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d80ab-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d80ab-151">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d80ab-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d80ab-152">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d80ab-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d80ab-153">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d80ab-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d80ab-154">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d80ab-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d80ab-155">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d80ab-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d80ab-156">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d80ab-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d80ab-157">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d80ab-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d80ab-158">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d80ab-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d80ab-159">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d80ab-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d80ab-160">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d80ab-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d80ab-161">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d80ab-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d80ab-162">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d80ab-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d80ab-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d80ab-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d80ab-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d80ab-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d80ab-165">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d80ab-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d80ab-166">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d80ab-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d80ab-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d80ab-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d80ab-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d80ab-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d80ab-169">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d80ab-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d80ab-170">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d80ab-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d80ab-171">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d80ab-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d80ab-172">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d80ab-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d80ab-173">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d80ab-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d80ab-174">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d80ab-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d80ab-175">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d80ab-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="d80ab-176">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d80ab-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)