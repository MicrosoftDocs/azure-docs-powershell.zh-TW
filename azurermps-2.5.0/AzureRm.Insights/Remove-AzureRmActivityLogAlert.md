---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: 1dfd435d2797ee7430349546a5d2ba6fa2fe0023
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800973"
---
# <span data-ttu-id="11ab6-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="11ab6-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="11ab6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11ab6-102">SYNOPSIS</span></span>
<span data-ttu-id="11ab6-103">移除活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="11ab6-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11ab6-104">句法</span><span class="sxs-lookup"><span data-stu-id="11ab6-104">SYNTAX</span></span>

### <span data-ttu-id="11ab6-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="11ab6-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11ab6-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="11ab6-106">RemoveByInputObject</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11ab6-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="11ab6-107">RemoveByResourceId</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11ab6-108">說明</span><span class="sxs-lookup"><span data-stu-id="11ab6-108">DESCRIPTION</span></span>
<span data-ttu-id="11ab6-109">**AzureRmActivityLogAlert** Cmdlet 會移除活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="11ab6-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="11ab6-110">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際修補資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="11ab6-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="11ab6-111">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="11ab6-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="11ab6-112">示例</span><span class="sxs-lookup"><span data-stu-id="11ab6-112">EXAMPLES</span></span>

### <span data-ttu-id="11ab6-113">範例1：移除活動記錄通知</span><span class="sxs-lookup"><span data-stu-id="11ab6-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="11ab6-114">使用名稱和資源群組名稱作為輸入，移除活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="11ab6-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="11ab6-115">範例2：使用 PSActivityLogAlertResource 做為輸入來移除活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="11ab6-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="11ab6-116">使用 PSActivityLogAlertResource 作為輸入來移除活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="11ab6-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="11ab6-117">範例3：使用 ResourceId 參數移除 ActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="11ab6-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="11ab6-118">這個命令會從管道使用 ResourceId 參數移除 ActivityLogAlert。</span><span class="sxs-lookup"><span data-stu-id="11ab6-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="11ab6-119">參數</span><span class="sxs-lookup"><span data-stu-id="11ab6-119">PARAMETERS</span></span>

### <span data-ttu-id="11ab6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ab6-120">-DefaultProfile</span></span>
<span data-ttu-id="11ab6-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="11ab6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11ab6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11ab6-122">-InputObject</span></span>
<span data-ttu-id="11ab6-123">設定呼叫的 InputObject tags 屬性來解壓縮所需的名稱，以及資源組名屬性。</span><span class="sxs-lookup"><span data-stu-id="11ab6-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11ab6-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="11ab6-124">-Name</span></span>
<span data-ttu-id="11ab6-125">活動記錄通知的名稱。</span><span class="sxs-lookup"><span data-stu-id="11ab6-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ab6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11ab6-126">-ResourceGroupName</span></span>
<span data-ttu-id="11ab6-127">警示資源所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="11ab6-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ab6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11ab6-128">-ResourceId</span></span>
<span data-ttu-id="11ab6-129">設定呼叫的 ResourceId 標籤屬性來解壓縮所需的名稱、資源組名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="11ab6-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ab6-130">-確認</span><span class="sxs-lookup"><span data-stu-id="11ab6-130">-Confirm</span></span>
<span data-ttu-id="11ab6-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="11ab6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11ab6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11ab6-132">-WhatIf</span></span>
<span data-ttu-id="11ab6-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11ab6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11ab6-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11ab6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11ab6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ab6-135">CommonParameters</span></span>
<span data-ttu-id="11ab6-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11ab6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ab6-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11ab6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ab6-138">輸入</span><span class="sxs-lookup"><span data-stu-id="11ab6-138">INPUTS</span></span>

### <span data-ttu-id="11ab6-139">System.object</span><span class="sxs-lookup"><span data-stu-id="11ab6-139">System.String</span></span>

### <span data-ttu-id="11ab6-140">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="11ab6-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="11ab6-141">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="11ab6-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="11ab6-142">輸出</span><span class="sxs-lookup"><span data-stu-id="11ab6-142">OUTPUTS</span></span>

### <span data-ttu-id="11ab6-143">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="11ab6-143">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="11ab6-144">筆記</span><span class="sxs-lookup"><span data-stu-id="11ab6-144">NOTES</span></span>

## <span data-ttu-id="11ab6-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="11ab6-145">RELATED LINKS</span></span>

[<span data-ttu-id="11ab6-146">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="11ab6-146">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="11ab6-147">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="11ab6-147">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="11ab6-148">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="11ab6-148">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="11ab6-149">AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="11ab6-149">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="11ab6-150">新-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="11ab6-150">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="11ab6-151">新-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="11ab6-151">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
