---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 8253e43052203d4f5ba844cec02ec3b2af592b1d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957999"
---
# <span data-ttu-id="2ca8c-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ca8c-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="2ca8c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ca8c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca8c-103">建立新的網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="2ca8c-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="2ca8c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ca8c-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ca8c-105">說明</span><span class="sxs-lookup"><span data-stu-id="2ca8c-105">DESCRIPTION</span></span>
<span data-ttu-id="2ca8c-106">New-AzNetworkWatcher Cmdlet 會建立新的網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="2ca8c-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="2ca8c-107">示例</span><span class="sxs-lookup"><span data-stu-id="2ca8c-107">EXAMPLES</span></span>

### <span data-ttu-id="2ca8c-108">範例1：建立網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="2ca8c-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="2ca8c-109">這個範例會在新建立的資源群組內建立新的網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="2ca8c-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="2ca8c-110">請注意，每個訂閱只能建立一個網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="2ca8c-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="2ca8c-111">參數</span><span class="sxs-lookup"><span data-stu-id="2ca8c-111">PARAMETERS</span></span>

### <span data-ttu-id="2ca8c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca8c-112">-DefaultProfile</span></span>
<span data-ttu-id="2ca8c-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ca8c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ca8c-114">-位置</span><span class="sxs-lookup"><span data-stu-id="2ca8c-114">-Location</span></span>
<span data-ttu-id="2ca8c-115">位於.</span><span class="sxs-lookup"><span data-stu-id="2ca8c-115">Location.</span></span>

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

### <span data-ttu-id="2ca8c-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ca8c-116">-Name</span></span>
<span data-ttu-id="2ca8c-117">網路觀察程式名稱。</span><span class="sxs-lookup"><span data-stu-id="2ca8c-117">The network watcher name.</span></span>

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

### <span data-ttu-id="2ca8c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ca8c-118">-ResourceGroupName</span></span>
<span data-ttu-id="2ca8c-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ca8c-119">The resource group name.</span></span>

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

### <span data-ttu-id="2ca8c-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="2ca8c-120">-Tag</span></span>
<span data-ttu-id="2ca8c-121">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="2ca8c-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2ca8c-122">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2ca8c-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2ca8c-123">-確認</span><span class="sxs-lookup"><span data-stu-id="2ca8c-123">-Confirm</span></span>
<span data-ttu-id="2ca8c-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2ca8c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ca8c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ca8c-125">-WhatIf</span></span>
<span data-ttu-id="2ca8c-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2ca8c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ca8c-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ca8c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ca8c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca8c-128">CommonParameters</span></span>
<span data-ttu-id="2ca8c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ca8c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca8c-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2ca8c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca8c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2ca8c-131">INPUTS</span></span>

### <span data-ttu-id="2ca8c-132">System.object</span><span class="sxs-lookup"><span data-stu-id="2ca8c-132">System.String</span></span>

### <span data-ttu-id="2ca8c-133">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2ca8c-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2ca8c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2ca8c-134">OUTPUTS</span></span>

### <span data-ttu-id="2ca8c-135">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2ca8c-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="2ca8c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2ca8c-136">NOTES</span></span>
<span data-ttu-id="2ca8c-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="2ca8c-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="2ca8c-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ca8c-138">RELATED LINKS</span></span>

[<span data-ttu-id="2ca8c-139">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ca8c-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2ca8c-140">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ca8c-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2ca8c-141">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ca8c-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2ca8c-142">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2ca8c-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2ca8c-143">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2ca8c-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2ca8c-144">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2ca8c-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2ca8c-145">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2ca8c-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2ca8c-146">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ca8c-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2ca8c-147">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2ca8c-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2ca8c-148">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ca8c-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2ca8c-149">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ca8c-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2ca8c-150">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ca8c-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2ca8c-151">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ca8c-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2ca8c-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2ca8c-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2ca8c-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2ca8c-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2ca8c-154">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ca8c-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2ca8c-155">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ca8c-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2ca8c-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ca8c-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2ca8c-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2ca8c-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2ca8c-158">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ca8c-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2ca8c-159">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ca8c-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2ca8c-160">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2ca8c-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2ca8c-161">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2ca8c-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2ca8c-162">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2ca8c-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2ca8c-163">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2ca8c-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2ca8c-164">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2ca8c-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="2ca8c-165">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ca8c-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)