---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: 3ba9706c452c293dea6ad6a0e23a51ccb03ada9c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957832"
---
# <span data-ttu-id="4ac8e-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="4ac8e-101">Update-AzIotHub</span></span>

## <span data-ttu-id="4ac8e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ac8e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac8e-103">更新 Azure IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="4ac8e-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="4ac8e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ac8e-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ac8e-105">說明</span><span class="sxs-lookup"><span data-stu-id="4ac8e-105">DESCRIPTION</span></span>
<span data-ttu-id="4ac8e-106">您可以更新 IotHub 的 [標籤] 屬性。</span><span class="sxs-lookup"><span data-stu-id="4ac8e-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="4ac8e-107">示例</span><span class="sxs-lookup"><span data-stu-id="4ac8e-107">EXAMPLES</span></span>

### <span data-ttu-id="4ac8e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4ac8e-108">Example 1</span></span>
```
PS C:\> Update-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiotdps
Name           : myiotdps
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[k1, v1]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="4ac8e-109">將 " @tags " 新增至 Azure IoT 中樞 "myiotdps" 的標記。</span><span class="sxs-lookup"><span data-stu-id="4ac8e-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="4ac8e-110">參數</span><span class="sxs-lookup"><span data-stu-id="4ac8e-110">PARAMETERS</span></span>

### <span data-ttu-id="4ac8e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac8e-111">-DefaultProfile</span></span>
<span data-ttu-id="4ac8e-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ac8e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ac8e-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ac8e-113">-Name</span></span>
<span data-ttu-id="4ac8e-114">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="4ac8e-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4ac8e-115">-重設</span><span class="sxs-lookup"><span data-stu-id="4ac8e-115">-Reset</span></span>
<span data-ttu-id="4ac8e-116">重設 IoTHub 標記</span><span class="sxs-lookup"><span data-stu-id="4ac8e-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="4ac8e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ac8e-117">-ResourceGroupName</span></span>
<span data-ttu-id="4ac8e-118">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="4ac8e-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4ac8e-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="4ac8e-119">-Tag</span></span>
<span data-ttu-id="4ac8e-120">IoTHub 標記集合</span><span class="sxs-lookup"><span data-stu-id="4ac8e-120">IoTHub Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac8e-121">-確認</span><span class="sxs-lookup"><span data-stu-id="4ac8e-121">-Confirm</span></span>
<span data-ttu-id="4ac8e-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ac8e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ac8e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ac8e-123">-WhatIf</span></span>
<span data-ttu-id="4ac8e-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ac8e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ac8e-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ac8e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ac8e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac8e-126">CommonParameters</span></span>
<span data-ttu-id="4ac8e-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ac8e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac8e-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4ac8e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac8e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="4ac8e-129">INPUTS</span></span>

### <span data-ttu-id="4ac8e-130">System.object</span><span class="sxs-lookup"><span data-stu-id="4ac8e-130">System.String</span></span>

## <span data-ttu-id="4ac8e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="4ac8e-131">OUTPUTS</span></span>

### <span data-ttu-id="4ac8e-132">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="4ac8e-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="4ac8e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="4ac8e-133">NOTES</span></span>

## <span data-ttu-id="4ac8e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ac8e-134">RELATED LINKS</span></span>