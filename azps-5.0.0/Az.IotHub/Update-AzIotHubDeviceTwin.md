---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 16c3ab31959268aa998d50290180d4d8b3231ccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284707"
---
# <span data-ttu-id="2de9f-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="2de9f-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="2de9f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2de9f-102">SYNOPSIS</span></span>
<span data-ttu-id="2de9f-103">更新裝置的標記與所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="2de9f-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="2de9f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2de9f-104">SYNTAX</span></span>

### <span data-ttu-id="2de9f-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2de9f-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2de9f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2de9f-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2de9f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2de9f-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2de9f-108">說明</span><span class="sxs-lookup"><span data-stu-id="2de9f-108">DESCRIPTION</span></span>
<span data-ttu-id="2de9f-109">更新或取代 device 雙子。</span><span class="sxs-lookup"><span data-stu-id="2de9f-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="2de9f-110">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins 。</span><span class="sxs-lookup"><span data-stu-id="2de9f-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="2de9f-111">示例</span><span class="sxs-lookup"><span data-stu-id="2de9f-111">EXAMPLES</span></span>

### <span data-ttu-id="2de9f-112">範例1</span><span class="sxs-lookup"><span data-stu-id="2de9f-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="2de9f-113">傳回更新的裝置雙子物件物件。</span><span class="sxs-lookup"><span data-stu-id="2de9f-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="2de9f-114">範例2</span><span class="sxs-lookup"><span data-stu-id="2de9f-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="2de9f-115">傳回具有更新之所需屬性的 device 雙子物件物件。</span><span class="sxs-lookup"><span data-stu-id="2de9f-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="2de9f-116">範例3</span><span class="sxs-lookup"><span data-stu-id="2de9f-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="2de9f-117">傳回含更新標記屬性的 device 雙子物件物件。</span><span class="sxs-lookup"><span data-stu-id="2de9f-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="2de9f-118">範例4</span><span class="sxs-lookup"><span data-stu-id="2de9f-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="2de9f-119">傳回取代 device 雙子物件。</span><span class="sxs-lookup"><span data-stu-id="2de9f-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="2de9f-120">參數</span><span class="sxs-lookup"><span data-stu-id="2de9f-120">PARAMETERS</span></span>

### <span data-ttu-id="2de9f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de9f-121">-DefaultProfile</span></span>
<span data-ttu-id="2de9f-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2de9f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2de9f-123">-所需</span><span class="sxs-lookup"><span data-stu-id="2de9f-123">-Desired</span></span>
<span data-ttu-id="2de9f-124">在 device 雙子中新增或更新所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="2de9f-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="2de9f-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2de9f-125">-DeviceId</span></span>
<span data-ttu-id="2de9f-126">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="2de9f-126">Target Device Id.</span></span>

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

### <span data-ttu-id="2de9f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2de9f-127">-InputObject</span></span>
<span data-ttu-id="2de9f-128">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="2de9f-128">IotHub object</span></span>

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

### <span data-ttu-id="2de9f-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2de9f-129">-IotHubName</span></span>
<span data-ttu-id="2de9f-130">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="2de9f-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2de9f-131">-部分</span><span class="sxs-lookup"><span data-stu-id="2de9f-131">-Partial</span></span>
<span data-ttu-id="2de9f-132">僅允許部分更新裝置雙子的標記和所需屬性。</span><span class="sxs-lookup"><span data-stu-id="2de9f-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="2de9f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de9f-133">-ResourceGroupName</span></span>
<span data-ttu-id="2de9f-134">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="2de9f-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2de9f-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2de9f-135">-ResourceId</span></span>
<span data-ttu-id="2de9f-136">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2de9f-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2de9f-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="2de9f-137">-Tag</span></span>
<span data-ttu-id="2de9f-138">新增或更新 device 雙子中的 tags 屬性。</span><span class="sxs-lookup"><span data-stu-id="2de9f-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="2de9f-139">-確認</span><span class="sxs-lookup"><span data-stu-id="2de9f-139">-Confirm</span></span>
<span data-ttu-id="2de9f-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2de9f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2de9f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2de9f-141">-WhatIf</span></span>
<span data-ttu-id="2de9f-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2de9f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2de9f-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2de9f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2de9f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de9f-144">CommonParameters</span></span>
<span data-ttu-id="2de9f-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2de9f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de9f-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2de9f-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de9f-147">輸入</span><span class="sxs-lookup"><span data-stu-id="2de9f-147">INPUTS</span></span>

### <span data-ttu-id="2de9f-148">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="2de9f-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2de9f-149">System.object</span><span class="sxs-lookup"><span data-stu-id="2de9f-149">System.String</span></span>

## <span data-ttu-id="2de9f-150">輸出</span><span class="sxs-lookup"><span data-stu-id="2de9f-150">OUTPUTS</span></span>

### <span data-ttu-id="2de9f-151">System.object</span><span class="sxs-lookup"><span data-stu-id="2de9f-151">System.String</span></span>

## <span data-ttu-id="2de9f-152">筆記</span><span class="sxs-lookup"><span data-stu-id="2de9f-152">NOTES</span></span>

## <span data-ttu-id="2de9f-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="2de9f-153">RELATED LINKS</span></span>