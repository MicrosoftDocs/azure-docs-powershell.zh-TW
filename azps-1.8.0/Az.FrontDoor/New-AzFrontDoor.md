---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: cea5b69b279b6f7f7a8e783d4ed328237377c18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787830"
---
# <span data-ttu-id="48923-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="48923-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="48923-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48923-102">SYNOPSIS</span></span>
<span data-ttu-id="48923-103">建立新的 Azure 前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="48923-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="48923-104">句法</span><span class="sxs-lookup"><span data-stu-id="48923-104">SYNTAX</span></span>

```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48923-105">說明</span><span class="sxs-lookup"><span data-stu-id="48923-105">DESCRIPTION</span></span>
<span data-ttu-id="48923-106">**新的-AzFrontDoor** Cmdlet 會在指定資源群組中的 [目前訂閱] 下建立新的 Azure 前門負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="48923-106">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="48923-107">示例</span><span class="sxs-lookup"><span data-stu-id="48923-107">EXAMPLES</span></span>

### <span data-ttu-id="48923-108">範例1：根據指定的參數建立前門。</span><span class="sxs-lookup"><span data-stu-id="48923-108">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="48923-109">根據指定的參數建立一個前門。</span><span class="sxs-lookup"><span data-stu-id="48923-109">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="48923-110">參數</span><span class="sxs-lookup"><span data-stu-id="48923-110">PARAMETERS</span></span>

### <span data-ttu-id="48923-111">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="48923-111">-BackendPool</span></span>
<span data-ttu-id="48923-112">Backendpools 可供路由規則使用。</span><span class="sxs-lookup"><span data-stu-id="48923-112">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48923-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48923-113">-DefaultProfile</span></span>
<span data-ttu-id="48923-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="48923-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48923-115">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="48923-115">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="48923-116">是否要針對所有後端池停用 HTTPS 要求的憑證名稱檢查。</span><span class="sxs-lookup"><span data-stu-id="48923-116">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="48923-117">對非 HTTPS 式要求沒有作用。</span><span class="sxs-lookup"><span data-stu-id="48923-117">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="48923-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="48923-118">-EnabledState</span></span>
<span data-ttu-id="48923-119">前蓋負載平衡器的 EnabledState。</span><span class="sxs-lookup"><span data-stu-id="48923-119">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="48923-120">已啟用預設值</span><span class="sxs-lookup"><span data-stu-id="48923-120">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48923-121">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="48923-121">-FrontendEndpoint</span></span>
<span data-ttu-id="48923-122">可供路由規則使用的前端端點。</span><span class="sxs-lookup"><span data-stu-id="48923-122">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48923-123">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="48923-123">-HealthProbeSetting</span></span>
<span data-ttu-id="48923-124">與此前門實例相關聯的健康情況探測器設定。</span><span class="sxs-lookup"><span data-stu-id="48923-124">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48923-125">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="48923-125">-LoadBalancingSetting</span></span>
<span data-ttu-id="48923-126">與此前門實例相關聯的負載平衡設定。</span><span class="sxs-lookup"><span data-stu-id="48923-126">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48923-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="48923-127">-Name</span></span>
<span data-ttu-id="48923-128">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="48923-128">Front Door name.</span></span>

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

### <span data-ttu-id="48923-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48923-129">-ResourceGroupName</span></span>
<span data-ttu-id="48923-130">在其中建立前蓋的資源群組名稱。</span><span class="sxs-lookup"><span data-stu-id="48923-130">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="48923-131">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="48923-131">-RoutingRule</span></span>
<span data-ttu-id="48923-132">與此 FrontDoor 相關聯的路由規則</span><span class="sxs-lookup"><span data-stu-id="48923-132">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48923-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="48923-133">-Tag</span></span>
<span data-ttu-id="48923-134">標記與 FrontDoor 相關聯。</span><span class="sxs-lookup"><span data-stu-id="48923-134">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="48923-135">-確認</span><span class="sxs-lookup"><span data-stu-id="48923-135">-Confirm</span></span>
<span data-ttu-id="48923-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="48923-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48923-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48923-137">-WhatIf</span></span>
<span data-ttu-id="48923-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48923-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48923-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48923-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48923-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48923-140">CommonParameters</span></span>
<span data-ttu-id="48923-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48923-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48923-142">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="48923-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48923-143">輸入</span><span class="sxs-lookup"><span data-stu-id="48923-143">INPUTS</span></span>

### <span data-ttu-id="48923-144">所有</span><span class="sxs-lookup"><span data-stu-id="48923-144">None</span></span>

## <span data-ttu-id="48923-145">輸出</span><span class="sxs-lookup"><span data-stu-id="48923-145">OUTPUTS</span></span>

### <span data-ttu-id="48923-146">PSFrontDoor 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="48923-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="48923-147">筆記</span><span class="sxs-lookup"><span data-stu-id="48923-147">NOTES</span></span>

## <span data-ttu-id="48923-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="48923-148">RELATED LINKS</span></span>

<span data-ttu-id="48923-149">[AzFrontDoor](./Get-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md) 
[移除-AzFrontDoor](./Remove-AzFrontDoor.md) 
[新-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
[新-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
[新-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
[新-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
[新-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="48923-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>