---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288707"
---
# <span data-ttu-id="48a2a-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="48a2a-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="48a2a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="48a2a-103">建立連接監視器端點。</span><span class="sxs-lookup"><span data-stu-id="48a2a-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="48a2a-104">句法</span><span class="sxs-lookup"><span data-stu-id="48a2a-104">SYNTAX</span></span>

### <span data-ttu-id="48a2a-105">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="48a2a-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48a2a-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="48a2a-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48a2a-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="48a2a-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48a2a-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="48a2a-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48a2a-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="48a2a-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48a2a-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="48a2a-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48a2a-111">說明</span><span class="sxs-lookup"><span data-stu-id="48a2a-111">DESCRIPTION</span></span>
<span data-ttu-id="48a2a-112">New-AzNetworkWatcherConnectionMonitorEndpointObject Cmdlet 會建立連接監視器端點。</span><span class="sxs-lookup"><span data-stu-id="48a2a-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="48a2a-113">示例</span><span class="sxs-lookup"><span data-stu-id="48a2a-113">EXAMPLES</span></span>

### <span data-ttu-id="48a2a-114">範例1</span><span class="sxs-lookup"><span data-stu-id="48a2a-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="48a2a-115">名稱： workspaceEndpoint 類型： MMAWorkspaceMachine ResourceId：/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace 位址： Scope： {"Include"： [{"Address"： "WIN-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="48a2a-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="48a2a-116">參數</span><span class="sxs-lookup"><span data-stu-id="48a2a-116">PARAMETERS</span></span>

### <span data-ttu-id="48a2a-117">-位址</span><span class="sxs-lookup"><span data-stu-id="48a2a-117">-Address</span></span>
<span data-ttu-id="48a2a-118">連線監視端點的位址 (IP 或功能變數名稱) 。</span><span class="sxs-lookup"><span data-stu-id="48a2a-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExternalAddress, MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48a2a-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="48a2a-119">-AzureSubnet</span></span>
<span data-ttu-id="48a2a-120">Azure 子網端點交換器。</span><span class="sxs-lookup"><span data-stu-id="48a2a-120">Azure Subnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48a2a-121">-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="48a2a-121">-AzureVM</span></span>
<span data-ttu-id="48a2a-122">Azure VM 端點交換器。</span><span class="sxs-lookup"><span data-stu-id="48a2a-122">Azure VM endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48a2a-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="48a2a-123">-AzureVNet</span></span>
<span data-ttu-id="48a2a-124">Azure Vnet 端點交換器。</span><span class="sxs-lookup"><span data-stu-id="48a2a-124">Azure Vnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVNet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48a2a-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="48a2a-125">-CoverageLevel</span></span>
<span data-ttu-id="48a2a-126">端點的測試覆蓋率。</span><span class="sxs-lookup"><span data-stu-id="48a2a-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="48a2a-127">支援的值為 Default、Low、BelowAverage、Average、AboveAvergae、Full。</span><span class="sxs-lookup"><span data-stu-id="48a2a-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48a2a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48a2a-128">-DefaultProfile</span></span>
<span data-ttu-id="48a2a-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="48a2a-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48a2a-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="48a2a-130">-ExcludeItem</span></span>
<span data-ttu-id="48a2a-131">需要從端點範圍中排除的專案清單。</span><span class="sxs-lookup"><span data-stu-id="48a2a-131">List of items which need to be excluded from endpoint scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48a2a-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="48a2a-132">-ExternalAddress</span></span>
<span data-ttu-id="48a2a-133">[外部地址] 端點開關。</span><span class="sxs-lookup"><span data-stu-id="48a2a-133">External Address endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExternalAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48a2a-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="48a2a-134">-IncludeItem</span></span>
<span data-ttu-id="48a2a-135">需要納入 endpont 範圍的專案清單。</span><span class="sxs-lookup"><span data-stu-id="48a2a-135">List of items which need to be included into endpont scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, MMAWorkspaceMachine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48a2a-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="48a2a-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="48a2a-137">MMA 工作區電腦端點開關。</span><span class="sxs-lookup"><span data-stu-id="48a2a-137">MMA Workspace Machine endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48a2a-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="48a2a-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="48a2a-139">MMA 工作區網路端點交換器。</span><span class="sxs-lookup"><span data-stu-id="48a2a-139">MMA Workspace Network endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48a2a-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="48a2a-140">-Name</span></span>
<span data-ttu-id="48a2a-141">[連線監視者] 端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="48a2a-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="48a2a-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48a2a-142">-ResourceId</span></span>
<span data-ttu-id="48a2a-143">[連線監視者] 端點的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="48a2a-143">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM, AzureVNet, AzureSubnet, MMAWorkspaceMachine, MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48a2a-144">-確認</span><span class="sxs-lookup"><span data-stu-id="48a2a-144">-Confirm</span></span>
<span data-ttu-id="48a2a-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="48a2a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48a2a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48a2a-146">-WhatIf</span></span>
<span data-ttu-id="48a2a-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48a2a-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48a2a-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48a2a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48a2a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48a2a-149">CommonParameters</span></span>
<span data-ttu-id="48a2a-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48a2a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48a2a-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="48a2a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48a2a-152">輸入</span><span class="sxs-lookup"><span data-stu-id="48a2a-152">INPUTS</span></span>

### <span data-ttu-id="48a2a-153">所有</span><span class="sxs-lookup"><span data-stu-id="48a2a-153">None</span></span>

## <span data-ttu-id="48a2a-154">輸出</span><span class="sxs-lookup"><span data-stu-id="48a2a-154">OUTPUTS</span></span>

### <span data-ttu-id="48a2a-155">PSNetworkWatcherConnectionMonitorEndpointObject 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="48a2a-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="48a2a-156">筆記</span><span class="sxs-lookup"><span data-stu-id="48a2a-156">NOTES</span></span>

## <span data-ttu-id="48a2a-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="48a2a-157">RELATED LINKS</span></span>