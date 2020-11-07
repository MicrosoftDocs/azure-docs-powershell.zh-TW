---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: b06540e1f03058fd36302616d22375270b521b8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790629"
---
# <span data-ttu-id="3c735-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3c735-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="3c735-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c735-102">SYNOPSIS</span></span>
<span data-ttu-id="3c735-103">移除網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="3c735-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="3c735-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c735-104">SYNTAX</span></span>

### <span data-ttu-id="3c735-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3c735-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c735-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3c735-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c735-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3c735-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c735-108">說明</span><span class="sxs-lookup"><span data-stu-id="3c735-108">DESCRIPTION</span></span>
<span data-ttu-id="3c735-109">Remove-AzNetworkWatcher Cmdlet 會移除網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="3c735-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="3c735-110">示例</span><span class="sxs-lookup"><span data-stu-id="3c735-110">EXAMPLES</span></span>

### <span data-ttu-id="3c735-111">範例1：建立及刪除網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="3c735-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="3c735-112">這個範例會在資源群組中建立網路觀察程式，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="3c735-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="3c735-113">請注意，每個訂閱只能建立一個網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="3c735-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="3c735-114">若要在刪除虛擬網路時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="3c735-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="3c735-115">參數</span><span class="sxs-lookup"><span data-stu-id="3c735-115">PARAMETERS</span></span>

### <span data-ttu-id="3c735-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c735-116">-AsJob</span></span>
<span data-ttu-id="3c735-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3c735-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c735-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c735-118">-DefaultProfile</span></span>
<span data-ttu-id="3c735-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c735-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c735-120">-位置</span><span class="sxs-lookup"><span data-stu-id="3c735-120">-Location</span></span>
<span data-ttu-id="3c735-121">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="3c735-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3c735-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c735-122">-Name</span></span>
<span data-ttu-id="3c735-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="3c735-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c735-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3c735-124">-NetworkWatcher</span></span>
<span data-ttu-id="3c735-125">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="3c735-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="3c735-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c735-126">-PassThru</span></span>
<span data-ttu-id="3c735-127">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="3c735-127">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c735-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c735-128">-ResourceGroupName</span></span>
<span data-ttu-id="3c735-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c735-129">The resource group name.</span></span>

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

### <span data-ttu-id="3c735-130">-確認</span><span class="sxs-lookup"><span data-stu-id="3c735-130">-Confirm</span></span>
<span data-ttu-id="3c735-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3c735-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c735-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c735-132">-WhatIf</span></span>
<span data-ttu-id="3c735-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3c735-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c735-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c735-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c735-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c735-135">CommonParameters</span></span>
<span data-ttu-id="3c735-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c735-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c735-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3c735-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c735-138">輸入</span><span class="sxs-lookup"><span data-stu-id="3c735-138">INPUTS</span></span>

### <span data-ttu-id="3c735-139">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3c735-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3c735-140">System.object</span><span class="sxs-lookup"><span data-stu-id="3c735-140">System.String</span></span>

## <span data-ttu-id="3c735-141">輸出</span><span class="sxs-lookup"><span data-stu-id="3c735-141">OUTPUTS</span></span>

### <span data-ttu-id="3c735-142">System.object</span><span class="sxs-lookup"><span data-stu-id="3c735-142">System.Boolean</span></span>

## <span data-ttu-id="3c735-143">筆記</span><span class="sxs-lookup"><span data-stu-id="3c735-143">NOTES</span></span>
<span data-ttu-id="3c735-144">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="3c735-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="3c735-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c735-145">RELATED LINKS</span></span>

[<span data-ttu-id="3c735-146">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3c735-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3c735-147">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3c735-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3c735-148">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3c735-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3c735-149">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3c735-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3c735-150">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3c735-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3c735-151">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3c735-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3c735-152">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3c735-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3c735-153">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3c735-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3c735-154">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3c735-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3c735-155">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3c735-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3c735-156">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3c735-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3c735-157">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3c735-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3c735-158">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c735-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3c735-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3c735-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3c735-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3c735-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3c735-161">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3c735-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3c735-162">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3c735-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3c735-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3c735-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3c735-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3c735-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3c735-165">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3c735-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3c735-166">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3c735-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3c735-167">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3c735-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3c735-168">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3c735-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3c735-169">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3c735-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3c735-170">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3c735-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3c735-171">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3c735-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="3c735-172">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3c735-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)