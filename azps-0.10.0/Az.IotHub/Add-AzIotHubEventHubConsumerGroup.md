---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 2592284be483793ea246d30e95a4c9065fdd6e3c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795645"
---
# <span data-ttu-id="f9a01-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="f9a01-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="f9a01-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9a01-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a01-103">建立 eventhub 消費者群組。</span><span class="sxs-lookup"><span data-stu-id="f9a01-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="f9a01-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9a01-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9a01-105">說明</span><span class="sxs-lookup"><span data-stu-id="f9a01-105">DESCRIPTION</span></span>
<span data-ttu-id="f9a01-106">在與指定 IotHub 相關聯的 Eventhub 中建立消費者群組。</span><span class="sxs-lookup"><span data-stu-id="f9a01-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="f9a01-107">示例</span><span class="sxs-lookup"><span data-stu-id="f9a01-107">EXAMPLES</span></span>

### <span data-ttu-id="f9a01-108">範例1：將消費者群組新增至遙測 eventhub</span><span class="sxs-lookup"><span data-stu-id="f9a01-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="f9a01-109">將名為 "myconsumergroup" 的新 consumergroup，新增到名為 "myiothub" 的 iothub 中的 [] 的 eventhub 事件</span><span class="sxs-lookup"><span data-stu-id="f9a01-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="f9a01-110">參數</span><span class="sxs-lookup"><span data-stu-id="f9a01-110">PARAMETERS</span></span>

### <span data-ttu-id="f9a01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a01-111">-DefaultProfile</span></span>
<span data-ttu-id="f9a01-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f9a01-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9a01-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="f9a01-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="f9a01-114">您想要新增的 EventHub ConsumerGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9a01-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9a01-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9a01-115">-Name</span></span>
<span data-ttu-id="f9a01-116">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="f9a01-116">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a01-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9a01-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9a01-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9a01-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="f9a01-119">-確認</span><span class="sxs-lookup"><span data-stu-id="f9a01-119">-Confirm</span></span>
<span data-ttu-id="f9a01-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f9a01-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9a01-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9a01-121">-WhatIf</span></span>
<span data-ttu-id="f9a01-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9a01-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9a01-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9a01-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9a01-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a01-124">CommonParameters</span></span>
<span data-ttu-id="f9a01-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9a01-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a01-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f9a01-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a01-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f9a01-127">INPUTS</span></span>

### <span data-ttu-id="f9a01-128">System.object</span><span class="sxs-lookup"><span data-stu-id="f9a01-128">System.String</span></span>

## <span data-ttu-id="f9a01-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f9a01-129">OUTPUTS</span></span>

### <span data-ttu-id="f9a01-130">System.object</span><span class="sxs-lookup"><span data-stu-id="f9a01-130">System.String</span></span>

## <span data-ttu-id="f9a01-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f9a01-131">NOTES</span></span>

## <span data-ttu-id="f9a01-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9a01-132">RELATED LINKS</span></span>