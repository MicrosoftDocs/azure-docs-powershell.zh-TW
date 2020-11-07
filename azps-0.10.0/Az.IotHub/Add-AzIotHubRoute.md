---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: 3828b6ef95c629362ce0082d6bb97e2af1ccb687
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795618"
---
# <span data-ttu-id="705b3-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="705b3-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="705b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="705b3-102">SYNOPSIS</span></span>
<span data-ttu-id="705b3-103">在 IoT 中樞中建立路線</span><span class="sxs-lookup"><span data-stu-id="705b3-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="705b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="705b3-104">SYNTAX</span></span>

### <span data-ttu-id="705b3-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="705b3-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="705b3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="705b3-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="705b3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="705b3-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="705b3-108">說明</span><span class="sxs-lookup"><span data-stu-id="705b3-108">DESCRIPTION</span></span>
<span data-ttu-id="705b3-109">建立路由以傳送特定資料來源和條件至所需的端點。</span><span class="sxs-lookup"><span data-stu-id="705b3-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="705b3-110">示例</span><span class="sxs-lookup"><span data-stu-id="705b3-110">EXAMPLES</span></span>

### <span data-ttu-id="705b3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="705b3-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="705b3-112">建立新的路由 "R1"。</span><span class="sxs-lookup"><span data-stu-id="705b3-112">Create a new route "R1".</span></span>

## <span data-ttu-id="705b3-113">參數</span><span class="sxs-lookup"><span data-stu-id="705b3-113">PARAMETERS</span></span>

### <span data-ttu-id="705b3-114">-條件</span><span class="sxs-lookup"><span data-stu-id="705b3-114">-Condition</span></span>
<span data-ttu-id="705b3-115">評估以套用路由規則的條件</span><span class="sxs-lookup"><span data-stu-id="705b3-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="705b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="705b3-116">-DefaultProfile</span></span>
<span data-ttu-id="705b3-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="705b3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="705b3-118">-啟用</span><span class="sxs-lookup"><span data-stu-id="705b3-118">-Enabled</span></span>
<span data-ttu-id="705b3-119">啟用路線</span><span class="sxs-lookup"><span data-stu-id="705b3-119">Enable route</span></span>

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

### <span data-ttu-id="705b3-120">-終結點</span><span class="sxs-lookup"><span data-stu-id="705b3-120">-EndpointName</span></span>
<span data-ttu-id="705b3-121">路由端點的名稱</span><span class="sxs-lookup"><span data-stu-id="705b3-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="705b3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="705b3-122">-InputObject</span></span>
<span data-ttu-id="705b3-123">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="705b3-123">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="705b3-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="705b3-124">-Name</span></span>
<span data-ttu-id="705b3-125">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="705b3-125">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="705b3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="705b3-126">-ResourceGroupName</span></span>
<span data-ttu-id="705b3-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="705b3-127">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="705b3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="705b3-128">-ResourceId</span></span>
<span data-ttu-id="705b3-129">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="705b3-129">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="705b3-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="705b3-130">-RouteName</span></span>
<span data-ttu-id="705b3-131">路線的名稱</span><span class="sxs-lookup"><span data-stu-id="705b3-131">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="705b3-132">-來源</span><span class="sxs-lookup"><span data-stu-id="705b3-132">-Source</span></span>
<span data-ttu-id="705b3-133">路線來源</span><span class="sxs-lookup"><span data-stu-id="705b3-133">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="705b3-134">-確認</span><span class="sxs-lookup"><span data-stu-id="705b3-134">-Confirm</span></span>
<span data-ttu-id="705b3-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="705b3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="705b3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="705b3-136">-WhatIf</span></span>
<span data-ttu-id="705b3-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="705b3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="705b3-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="705b3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="705b3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="705b3-139">CommonParameters</span></span>
<span data-ttu-id="705b3-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="705b3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="705b3-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="705b3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="705b3-142">輸入</span><span class="sxs-lookup"><span data-stu-id="705b3-142">INPUTS</span></span>

### <span data-ttu-id="705b3-143">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="705b3-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="705b3-144">System.object</span><span class="sxs-lookup"><span data-stu-id="705b3-144">System.String</span></span>

## <span data-ttu-id="705b3-145">輸出</span><span class="sxs-lookup"><span data-stu-id="705b3-145">OUTPUTS</span></span>

### <span data-ttu-id="705b3-146">PSRouteMetadata （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="705b3-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="705b3-147">筆記</span><span class="sxs-lookup"><span data-stu-id="705b3-147">NOTES</span></span>

## <span data-ttu-id="705b3-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="705b3-148">RELATED LINKS</span></span>