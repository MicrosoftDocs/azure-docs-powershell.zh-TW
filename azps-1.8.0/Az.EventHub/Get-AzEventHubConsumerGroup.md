---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: 7f10df478851679afeb73157252d954f756f0c4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622295"
---
# <span data-ttu-id="163fc-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="163fc-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="163fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="163fc-102">SYNOPSIS</span></span>
<span data-ttu-id="163fc-103">取得指定事件中樞消費者群組的詳細資料，或取得事件中樞中的消費者群組清單。</span><span class="sxs-lookup"><span data-stu-id="163fc-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="163fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="163fc-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="163fc-105">說明</span><span class="sxs-lookup"><span data-stu-id="163fc-105">DESCRIPTION</span></span>
<span data-ttu-id="163fc-106">Get-AzEventHubConsumerGroup Cmdlet 會取得指定事件中樞消費者群組的詳細資料，或指定事件中樞中的消費者群組清單。</span><span class="sxs-lookup"><span data-stu-id="163fc-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="163fc-107">如果提供消費者群組的名稱，則會傳回單一消費者群組詳細資料的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="163fc-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="163fc-108">如果未提供消費者群組的名稱，則會傳回指定事件中樞中的消費者群組清單。</span><span class="sxs-lookup"><span data-stu-id="163fc-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="163fc-109">示例</span><span class="sxs-lookup"><span data-stu-id="163fc-109">EXAMPLES</span></span>

### <span data-ttu-id="163fc-110">範例1</span><span class="sxs-lookup"><span data-stu-id="163fc-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="163fc-111">\` \` 在事件中心 MyEventHubName 中取得消費者群組 MyConsumerGroupName，該活動中心已 \` \` 存在於 \` \` 包含資源群組 MyResourceGroupName 的命名空間 MyNamespaceName 中 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="163fc-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="163fc-112">範例2</span><span class="sxs-lookup"><span data-stu-id="163fc-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="163fc-113">在事件中心 MyEventHubName 中取得消費者群組的清單，該使用者群組 \` \` 存在於 \` \` 包含資源群組 MyResourceGroupName 的命名空間 MyNamespaceName 中 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="163fc-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="163fc-114">參數</span><span class="sxs-lookup"><span data-stu-id="163fc-114">PARAMETERS</span></span>

### <span data-ttu-id="163fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="163fc-115">-DefaultProfile</span></span>
<span data-ttu-id="163fc-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="163fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="163fc-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="163fc-117">-EventHub</span></span>
<span data-ttu-id="163fc-118">EventHub 名稱</span><span class="sxs-lookup"><span data-stu-id="163fc-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="163fc-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="163fc-119">-MaxCount</span></span>
<span data-ttu-id="163fc-120">決定要傳回的 ConsumerGroups 數目上限。</span><span class="sxs-lookup"><span data-stu-id="163fc-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163fc-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="163fc-121">-Name</span></span>
<span data-ttu-id="163fc-122">ConsumerGroup 名稱</span><span class="sxs-lookup"><span data-stu-id="163fc-122">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="163fc-123">-命名空間</span><span class="sxs-lookup"><span data-stu-id="163fc-123">-Namespace</span></span>
<span data-ttu-id="163fc-124">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="163fc-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="163fc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="163fc-125">-ResourceGroupName</span></span>
<span data-ttu-id="163fc-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="163fc-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="163fc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="163fc-127">CommonParameters</span></span>
<span data-ttu-id="163fc-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="163fc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="163fc-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="163fc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="163fc-130">輸入</span><span class="sxs-lookup"><span data-stu-id="163fc-130">INPUTS</span></span>

### <span data-ttu-id="163fc-131">System.object</span><span class="sxs-lookup"><span data-stu-id="163fc-131">System.String</span></span>

## <span data-ttu-id="163fc-132">輸出</span><span class="sxs-lookup"><span data-stu-id="163fc-132">OUTPUTS</span></span>

### <span data-ttu-id="163fc-133">PSConsumerGroupAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="163fc-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="163fc-134">筆記</span><span class="sxs-lookup"><span data-stu-id="163fc-134">NOTES</span></span>

## <span data-ttu-id="163fc-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="163fc-135">RELATED LINKS</span></span>