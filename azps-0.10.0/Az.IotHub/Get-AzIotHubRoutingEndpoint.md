---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: ac8fc7e3be69704b69fc2dfbfa30ec8df7bf996b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795614"
---
# <span data-ttu-id="3d241-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="3d241-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="3d241-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d241-102">SYNOPSIS</span></span>
<span data-ttu-id="3d241-103">在您的 IoT 中心中取得所有端點的相關資訊</span><span class="sxs-lookup"><span data-stu-id="3d241-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="3d241-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d241-104">SYNTAX</span></span>

### <span data-ttu-id="3d241-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3d241-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d241-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3d241-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d241-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3d241-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d241-108">說明</span><span class="sxs-lookup"><span data-stu-id="3d241-108">DESCRIPTION</span></span>
<span data-ttu-id="3d241-109">取得端點的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3d241-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="3d241-110">示例</span><span class="sxs-lookup"><span data-stu-id="3d241-110">EXAMPLES</span></span>

### <span data-ttu-id="3d241-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3d241-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="3d241-112">從「myiothub」 IoT 中樞取得所有端點。</span><span class="sxs-lookup"><span data-stu-id="3d241-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="3d241-113">範例2</span><span class="sxs-lookup"><span data-stu-id="3d241-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="3d241-114">從「myiothub」 IoT 中樞取得類型為 EventHub 的所有端點。</span><span class="sxs-lookup"><span data-stu-id="3d241-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="3d241-115">範例3</span><span class="sxs-lookup"><span data-stu-id="3d241-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="3d241-116">從「myiothub」 IoT 中樞取得類型為 EventHub 的所有端點。</span><span class="sxs-lookup"><span data-stu-id="3d241-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="3d241-117">範例4</span><span class="sxs-lookup"><span data-stu-id="3d241-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="3d241-118">從「myiothub」 IoT 中樞取得端點資訊。</span><span class="sxs-lookup"><span data-stu-id="3d241-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="3d241-119">參數</span><span class="sxs-lookup"><span data-stu-id="3d241-119">PARAMETERS</span></span>

### <span data-ttu-id="3d241-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d241-120">-DefaultProfile</span></span>
<span data-ttu-id="3d241-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d241-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d241-122">-終結點</span><span class="sxs-lookup"><span data-stu-id="3d241-122">-EndpointName</span></span>
<span data-ttu-id="3d241-123">路由端點的名稱</span><span class="sxs-lookup"><span data-stu-id="3d241-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="3d241-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="3d241-124">-EndpointType</span></span>
<span data-ttu-id="3d241-125">路由端點的類型</span><span class="sxs-lookup"><span data-stu-id="3d241-125">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d241-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d241-126">-InputObject</span></span>
<span data-ttu-id="3d241-127">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="3d241-127">IotHub Object</span></span>

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

### <span data-ttu-id="3d241-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d241-128">-Name</span></span>
<span data-ttu-id="3d241-129">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="3d241-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3d241-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d241-130">-ResourceGroupName</span></span>
<span data-ttu-id="3d241-131">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="3d241-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3d241-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d241-132">-ResourceId</span></span>
<span data-ttu-id="3d241-133">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3d241-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3d241-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d241-134">CommonParameters</span></span>
<span data-ttu-id="3d241-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d241-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d241-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3d241-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d241-137">輸入</span><span class="sxs-lookup"><span data-stu-id="3d241-137">INPUTS</span></span>

### <span data-ttu-id="3d241-138">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="3d241-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3d241-139">System.object</span><span class="sxs-lookup"><span data-stu-id="3d241-139">System.String</span></span>

## <span data-ttu-id="3d241-140">輸出</span><span class="sxs-lookup"><span data-stu-id="3d241-140">OUTPUTS</span></span>

### <span data-ttu-id="3d241-141">PSRoutingEventHubEndpoint （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="3d241-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="3d241-142">[System.object]. 清單 ' 1 [IotHub. PSRoutingEventHubProperties，IotHub，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））））。）</span><span class="sxs-lookup"><span data-stu-id="3d241-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="3d241-143">PSRoutingServiceBusQueueEndpoint （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="3d241-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="3d241-144">PSRoutingServiceBusQueueEndpointProperties []. IotHub. []</span><span class="sxs-lookup"><span data-stu-id="3d241-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="3d241-145">PSRoutingServiceBusTopicEndpoint （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="3d241-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="3d241-146">PSRoutingServiceBusTopicEndpointProperties []. IotHub. []</span><span class="sxs-lookup"><span data-stu-id="3d241-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="3d241-147">PSRoutingStorageContainerEndpoint （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="3d241-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="3d241-148">PSRoutingStorageContainerProperties []. IotHub. []</span><span class="sxs-lookup"><span data-stu-id="3d241-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="3d241-149">PSRoutingCustomEndpoint []. IotHub. []</span><span class="sxs-lookup"><span data-stu-id="3d241-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="3d241-150">筆記</span><span class="sxs-lookup"><span data-stu-id="3d241-150">NOTES</span></span>

## <span data-ttu-id="3d241-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d241-151">RELATED LINKS</span></span>