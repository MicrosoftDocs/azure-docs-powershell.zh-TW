---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: d6aa49cce1a97d0177c66dd735180df2fa46c97d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794696"
---
# <span data-ttu-id="fb119-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="fb119-101">Set-AzIotHub</span></span>

## <span data-ttu-id="fb119-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb119-102">SYNOPSIS</span></span>
<span data-ttu-id="fb119-103">更新 IotHub 的屬性。</span><span class="sxs-lookup"><span data-stu-id="fb119-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="fb119-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb119-104">SYNTAX</span></span>

### <span data-ttu-id="fb119-105">UpdateSku (預設) </span><span class="sxs-lookup"><span data-stu-id="fb119-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb119-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="fb119-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb119-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="fb119-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb119-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="fb119-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb119-109">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="fb119-109">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb119-110">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="fb119-110">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb119-111">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="fb119-111">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb119-112">說明</span><span class="sxs-lookup"><span data-stu-id="fb119-112">DESCRIPTION</span></span>
<span data-ttu-id="fb119-113">更新 IotHub 的屬性。</span><span class="sxs-lookup"><span data-stu-id="fb119-113">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="fb119-114">示例</span><span class="sxs-lookup"><span data-stu-id="fb119-114">EXAMPLES</span></span>

### <span data-ttu-id="fb119-115">範例1更新 sku</span><span class="sxs-lookup"><span data-stu-id="fb119-115">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="fb119-116">針對名稱為 "myiothub" 的 IotHub，將 sku 更新為 S1，並將單位更新為5</span><span class="sxs-lookup"><span data-stu-id="fb119-116">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="fb119-117">範例2更新 eventhub 屬性</span><span class="sxs-lookup"><span data-stu-id="fb119-117">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="fb119-118">針對名為 "myiothub" 的 IotHub，將遙測的保留時間更新為4天</span><span class="sxs-lookup"><span data-stu-id="fb119-118">Update the retention time of telemetry in days to 4 for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="fb119-119">參數</span><span class="sxs-lookup"><span data-stu-id="fb119-119">PARAMETERS</span></span>

### <span data-ttu-id="fb119-120">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="fb119-120">-CloudToDevice</span></span>
<span data-ttu-id="fb119-121">雲端 to device 命令佇列的屬性。</span><span class="sxs-lookup"><span data-stu-id="fb119-121">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb119-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb119-122">-DefaultProfile</span></span>
<span data-ttu-id="fb119-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fb119-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb119-124">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="fb119-124">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="fb119-125">此標誌指定是否應針對檔案上傳啟用通知。</span><span class="sxs-lookup"><span data-stu-id="fb119-125">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: System.Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb119-126">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="fb119-126">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="fb119-127">保留時間（天）。</span><span class="sxs-lookup"><span data-stu-id="fb119-127">Retention time in days.</span></span> 

```yaml
Type: System.Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb119-128">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="fb119-128">-FallbackRoute</span></span>
<span data-ttu-id="fb119-129">路由的備用路線</span><span class="sxs-lookup"><span data-stu-id="fb119-129">Fallback Route for Routing</span></span>

```yaml
Type: Microsoft.Azure.Management.IotHub.Models.PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb119-130">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="fb119-130">-FileUploadContainerName</span></span>
<span data-ttu-id="fb119-131">要上傳檔案的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="fb119-131">The name of the container to upload the files to.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb119-132">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="fb119-132">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="fb119-133">檔案上傳通知的最大傳遞數。</span><span class="sxs-lookup"><span data-stu-id="fb119-133">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb119-134">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="fb119-134">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="fb119-135">檔案上傳通知佇列中郵件的存留時間值。</span><span class="sxs-lookup"><span data-stu-id="fb119-135">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb119-136">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="fb119-136">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="fb119-137">針對檔案上傳所產生的 SAS Uri 的存留時間。</span><span class="sxs-lookup"><span data-stu-id="fb119-137">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb119-138">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="fb119-138">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="fb119-139">要上傳檔案的儲存空間連接字串。</span><span class="sxs-lookup"><span data-stu-id="fb119-139">The storage connection string to upload the files to.</span></span> 

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb119-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb119-140">-Name</span></span>
<span data-ttu-id="fb119-141">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="fb119-141">Name of the IotHub</span></span>

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

### <span data-ttu-id="fb119-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb119-142">-ResourceGroupName</span></span>
<span data-ttu-id="fb119-143">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="fb119-143">Resource Group Name</span></span>

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

### <span data-ttu-id="fb119-144">-路線</span><span class="sxs-lookup"><span data-stu-id="fb119-144">-Routes</span></span>
<span data-ttu-id="fb119-145">要新增以進行路由的路由</span><span class="sxs-lookup"><span data-stu-id="fb119-145">Routes to be added for Routing</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]
Parameter Sets: UpdateRouteProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb119-146">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="fb119-146">-RoutingProperties</span></span>
<span data-ttu-id="fb119-147">將訊息路由至外部端點的路由屬性</span><span class="sxs-lookup"><span data-stu-id="fb119-147">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb119-148">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fb119-148">-SkuName</span></span>
<span data-ttu-id="fb119-149">Sku 的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb119-149">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb119-150">單位</span><span class="sxs-lookup"><span data-stu-id="fb119-150">-Units</span></span>
<span data-ttu-id="fb119-151">單位數量</span><span class="sxs-lookup"><span data-stu-id="fb119-151">Number of Units</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateSku
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb119-152">-確認</span><span class="sxs-lookup"><span data-stu-id="fb119-152">-Confirm</span></span>
<span data-ttu-id="fb119-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fb119-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb119-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb119-154">-WhatIf</span></span>
<span data-ttu-id="fb119-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fb119-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb119-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb119-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb119-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb119-157">CommonParameters</span></span>
<span data-ttu-id="fb119-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb119-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb119-159">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fb119-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb119-160">輸入</span><span class="sxs-lookup"><span data-stu-id="fb119-160">INPUTS</span></span>

### <span data-ttu-id="fb119-161">System.object</span><span class="sxs-lookup"><span data-stu-id="fb119-161">System.String</span></span>

## <span data-ttu-id="fb119-162">輸出</span><span class="sxs-lookup"><span data-stu-id="fb119-162">OUTPUTS</span></span>

### <span data-ttu-id="fb119-163">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="fb119-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="fb119-164">筆記</span><span class="sxs-lookup"><span data-stu-id="fb119-164">NOTES</span></span>

## <span data-ttu-id="fb119-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb119-165">RELATED LINKS</span></span>