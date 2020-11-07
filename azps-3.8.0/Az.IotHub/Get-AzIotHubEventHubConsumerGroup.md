---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958931"
---
# <span data-ttu-id="5621a-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5621a-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="5621a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5621a-102">SYNOPSIS</span></span>
<span data-ttu-id="5621a-103">取得所有 eventhub consumergroups。</span><span class="sxs-lookup"><span data-stu-id="5621a-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="5621a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5621a-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5621a-105">說明</span><span class="sxs-lookup"><span data-stu-id="5621a-105">DESCRIPTION</span></span>
<span data-ttu-id="5621a-106">針對 IotHub 使用的不同 EventHubs，取得所有的 eventhub consumergroups。</span><span class="sxs-lookup"><span data-stu-id="5621a-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="5621a-107">示例</span><span class="sxs-lookup"><span data-stu-id="5621a-107">EXAMPLES</span></span>

### <span data-ttu-id="5621a-108">範例1取得遙測 eventhub 的所有 eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="5621a-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="5621a-109">針對名為 myiothub 的 iothub，取得遙測 eventhub 的所有 eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="5621a-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="5621a-110">參數</span><span class="sxs-lookup"><span data-stu-id="5621a-110">PARAMETERS</span></span>

### <span data-ttu-id="5621a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5621a-111">-DefaultProfile</span></span>
<span data-ttu-id="5621a-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5621a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5621a-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="5621a-113">-Name</span></span>
<span data-ttu-id="5621a-114">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="5621a-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="5621a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5621a-115">-ResourceGroupName</span></span>
<span data-ttu-id="5621a-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="5621a-116">Resource Group Name</span></span>

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

### <span data-ttu-id="5621a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5621a-117">CommonParameters</span></span>
<span data-ttu-id="5621a-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5621a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5621a-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5621a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5621a-120">輸入</span><span class="sxs-lookup"><span data-stu-id="5621a-120">INPUTS</span></span>

### <span data-ttu-id="5621a-121">System.object</span><span class="sxs-lookup"><span data-stu-id="5621a-121">System.String</span></span>

## <span data-ttu-id="5621a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="5621a-122">OUTPUTS</span></span>

### <span data-ttu-id="5621a-123">PSEventHubConsumerGroupInfo （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="5621a-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="5621a-124">筆記</span><span class="sxs-lookup"><span data-stu-id="5621a-124">NOTES</span></span>

## <span data-ttu-id="5621a-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="5621a-125">RELATED LINKS</span></span>