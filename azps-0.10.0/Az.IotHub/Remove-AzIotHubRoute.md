---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: 1066c922e24f8a521ac7a52bab437812a7733021
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794700"
---
# <span data-ttu-id="ccd83-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="ccd83-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="ccd83-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ccd83-102">SYNOPSIS</span></span>
<span data-ttu-id="ccd83-103">刪除 IoT 中樞中的路線</span><span class="sxs-lookup"><span data-stu-id="ccd83-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="ccd83-104">句法</span><span class="sxs-lookup"><span data-stu-id="ccd83-104">SYNTAX</span></span>

### <span data-ttu-id="ccd83-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ccd83-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccd83-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ccd83-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccd83-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ccd83-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccd83-108">說明</span><span class="sxs-lookup"><span data-stu-id="ccd83-108">DESCRIPTION</span></span>
<span data-ttu-id="ccd83-109">刪除端點的路線</span><span class="sxs-lookup"><span data-stu-id="ccd83-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="ccd83-110">示例</span><span class="sxs-lookup"><span data-stu-id="ccd83-110">EXAMPLES</span></span>

### <span data-ttu-id="ccd83-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ccd83-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="ccd83-112">從「myiothub」 IoT 中樞刪除路由 "R1"。</span><span class="sxs-lookup"><span data-stu-id="ccd83-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="ccd83-113">參數</span><span class="sxs-lookup"><span data-stu-id="ccd83-113">PARAMETERS</span></span>

### <span data-ttu-id="ccd83-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccd83-114">-DefaultProfile</span></span>
<span data-ttu-id="ccd83-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ccd83-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccd83-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccd83-116">-InputObject</span></span>
<span data-ttu-id="ccd83-117">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="ccd83-117">IotHub Object</span></span>

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

### <span data-ttu-id="ccd83-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ccd83-118">-Name</span></span>
<span data-ttu-id="ccd83-119">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="ccd83-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ccd83-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccd83-120">-PassThru</span></span>
<span data-ttu-id="ccd83-121">允許傳回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="ccd83-121">Allows to return the boolean object.</span></span> <span data-ttu-id="ccd83-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ccd83-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ccd83-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccd83-123">-ResourceGroupName</span></span>
<span data-ttu-id="ccd83-124">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="ccd83-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ccd83-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccd83-125">-ResourceId</span></span>
<span data-ttu-id="ccd83-126">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ccd83-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ccd83-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="ccd83-127">-RouteName</span></span>
<span data-ttu-id="ccd83-128">路線的名稱</span><span class="sxs-lookup"><span data-stu-id="ccd83-128">Name of the Route</span></span>

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

### <span data-ttu-id="ccd83-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ccd83-129">-Confirm</span></span>
<span data-ttu-id="ccd83-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ccd83-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccd83-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccd83-131">-WhatIf</span></span>
<span data-ttu-id="ccd83-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ccd83-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccd83-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ccd83-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccd83-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccd83-134">CommonParameters</span></span>
<span data-ttu-id="ccd83-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ccd83-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccd83-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ccd83-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccd83-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ccd83-137">INPUTS</span></span>

### <span data-ttu-id="ccd83-138">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="ccd83-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ccd83-139">System.object</span><span class="sxs-lookup"><span data-stu-id="ccd83-139">System.String</span></span>

## <span data-ttu-id="ccd83-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ccd83-140">OUTPUTS</span></span>

### <span data-ttu-id="ccd83-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ccd83-141">System.Boolean</span></span>

## <span data-ttu-id="ccd83-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ccd83-142">NOTES</span></span>

## <span data-ttu-id="ccd83-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ccd83-143">RELATED LINKS</span></span>