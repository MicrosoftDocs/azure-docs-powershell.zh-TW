---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 683d03537f410b38260b502bc25ed90c9da9b4d2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284721"
---
# <span data-ttu-id="06e81-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="06e81-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="06e81-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06e81-102">SYNOPSIS</span></span>
<span data-ttu-id="06e81-103">刪除 IoT 中樞中的郵件擴充。</span><span class="sxs-lookup"><span data-stu-id="06e81-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="06e81-104">句法</span><span class="sxs-lookup"><span data-stu-id="06e81-104">SYNTAX</span></span>

### <span data-ttu-id="06e81-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="06e81-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06e81-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="06e81-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06e81-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="06e81-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06e81-108">說明</span><span class="sxs-lookup"><span data-stu-id="06e81-108">DESCRIPTION</span></span>
<span data-ttu-id="06e81-109">如需 Azure IoT 中樞中郵件 enrichments 的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="06e81-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="06e81-110">示例</span><span class="sxs-lookup"><span data-stu-id="06e81-110">EXAMPLES</span></span>

### <span data-ttu-id="06e81-111">範例1</span><span class="sxs-lookup"><span data-stu-id="06e81-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="06e81-112">刪除「newKey」訊息擴充。</span><span class="sxs-lookup"><span data-stu-id="06e81-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="06e81-113">參數</span><span class="sxs-lookup"><span data-stu-id="06e81-113">PARAMETERS</span></span>

### <span data-ttu-id="06e81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e81-114">-DefaultProfile</span></span>
<span data-ttu-id="06e81-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="06e81-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06e81-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06e81-116">-InputObject</span></span>
<span data-ttu-id="06e81-117">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="06e81-117">IotHub object</span></span>

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

### <span data-ttu-id="06e81-118">-鍵</span><span class="sxs-lookup"><span data-stu-id="06e81-118">-Key</span></span>
<span data-ttu-id="06e81-119">擴充的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="06e81-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="06e81-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="06e81-120">-Name</span></span>
<span data-ttu-id="06e81-121">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="06e81-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="06e81-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06e81-122">-PassThru</span></span>
<span data-ttu-id="06e81-123">允許傳回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="06e81-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="06e81-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="06e81-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="06e81-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06e81-125">-ResourceGroupName</span></span>
<span data-ttu-id="06e81-126">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="06e81-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="06e81-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06e81-127">-ResourceId</span></span>
<span data-ttu-id="06e81-128">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="06e81-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="06e81-129">-確認</span><span class="sxs-lookup"><span data-stu-id="06e81-129">-Confirm</span></span>
<span data-ttu-id="06e81-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="06e81-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06e81-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06e81-131">-WhatIf</span></span>
<span data-ttu-id="06e81-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06e81-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06e81-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06e81-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06e81-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e81-134">CommonParameters</span></span>
<span data-ttu-id="06e81-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06e81-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e81-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="06e81-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e81-137">輸入</span><span class="sxs-lookup"><span data-stu-id="06e81-137">INPUTS</span></span>

### <span data-ttu-id="06e81-138">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="06e81-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="06e81-139">System.object</span><span class="sxs-lookup"><span data-stu-id="06e81-139">System.String</span></span>

## <span data-ttu-id="06e81-140">輸出</span><span class="sxs-lookup"><span data-stu-id="06e81-140">OUTPUTS</span></span>

### <span data-ttu-id="06e81-141">System.object</span><span class="sxs-lookup"><span data-stu-id="06e81-141">System.Boolean</span></span>

## <span data-ttu-id="06e81-142">筆記</span><span class="sxs-lookup"><span data-stu-id="06e81-142">NOTES</span></span>

## <span data-ttu-id="06e81-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="06e81-143">RELATED LINKS</span></span>