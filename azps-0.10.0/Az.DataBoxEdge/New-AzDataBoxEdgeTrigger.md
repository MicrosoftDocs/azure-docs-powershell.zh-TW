---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: a24b5e5d4cce1e33536b7977590add11a6d7cb39
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795725"
---
# <span data-ttu-id="e1614-101">New-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="e1614-101">New-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="e1614-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1614-102">SYNOPSIS</span></span>
<span data-ttu-id="e1614-103">在裝置上設定觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e1614-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="e1614-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1614-104">SYNTAX</span></span>

### <span data-ttu-id="e1614-105">FileEventTriggerParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e1614-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1614-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1614-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1614-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1614-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1614-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1614-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1614-109">說明</span><span class="sxs-lookup"><span data-stu-id="e1614-109">DESCRIPTION</span></span>
<span data-ttu-id="e1614-110">**新的-AzDataBoxEdgeTrigger** Cmdlet 會在資料編輯方塊邊緣裝置上設定觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e1614-110">The **New-AzDataBoxEdgeTrigger** cmdlet configures a trigger on the Data Box Edge device.</span></span> 

## <span data-ttu-id="e1614-111">示例</span><span class="sxs-lookup"><span data-stu-id="e1614-111">EXAMPLES</span></span>

### <span data-ttu-id="e1614-112">範例1</span><span class="sxs-lookup"><span data-stu-id="e1614-112">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="e1614-113">參數</span><span class="sxs-lookup"><span data-stu-id="e1614-113">PARAMETERS</span></span>

### <span data-ttu-id="e1614-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1614-114">-AsJob</span></span>
<span data-ttu-id="e1614-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e1614-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1614-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1614-116">-DefaultProfile</span></span>
<span data-ttu-id="e1614-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1614-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1614-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e1614-118">-DeviceName</span></span>
<span data-ttu-id="e1614-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="e1614-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1614-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="e1614-120">-FileEvent</span></span>
<span data-ttu-id="e1614-121">傳送這個切換參數來設定 FileEvent 觸發程式</span><span class="sxs-lookup"><span data-stu-id="e1614-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileEventTriggerParameterSet, FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1614-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="e1614-122">-Name</span></span>
<span data-ttu-id="e1614-123">資源名稱</span><span class="sxs-lookup"><span data-stu-id="e1614-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1614-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="e1614-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="e1614-125">傳送這個切換參數來設定 PeriodicTimerEvent 觸發程式</span><span class="sxs-lookup"><span data-stu-id="e1614-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1614-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1614-126">-ResourceGroupName</span></span>
<span data-ttu-id="e1614-127">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e1614-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1614-128">-擁有方</span><span class="sxs-lookup"><span data-stu-id="e1614-128">-RoleName</span></span>
<span data-ttu-id="e1614-129">針對將引發事件的計算角色。</span><span class="sxs-lookup"><span data-stu-id="e1614-129">Compute role against which events will be raised.</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1614-130">-排程</span><span class="sxs-lookup"><span data-stu-id="e1614-130">-Schedule</span></span>
<span data-ttu-id="e1614-131">週期性頻率，需要引發計時器事件。</span><span class="sxs-lookup"><span data-stu-id="e1614-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="e1614-132">指定排程的天數 (介於1與 365) 之間，小時 (介於1到 23) ，或分鐘 (介於1和 59) 之間。</span><span class="sxs-lookup"><span data-stu-id="e1614-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1614-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="e1614-133">-ShareId</span></span>
<span data-ttu-id="e1614-134">要在 FileEvent 觸發程式中傳遞的檔案共用識別碼</span><span class="sxs-lookup"><span data-stu-id="e1614-134">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1614-135">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="e1614-135">-ShareName</span></span>
<span data-ttu-id="e1614-136">要在 FileEvent 觸發程式中傳遞的檔案共用識別碼</span><span class="sxs-lookup"><span data-stu-id="e1614-136">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1614-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e1614-137">-StartTime</span></span>
<span data-ttu-id="e1614-138">一天中產生有效觸發程式的時間。</span><span class="sxs-lookup"><span data-stu-id="e1614-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="e1614-139">[排程] 是以參照至最長秒的時間來計算。</span><span class="sxs-lookup"><span data-stu-id="e1614-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="e1614-140">如果未指定時區，時間會視為裝置時區。</span><span class="sxs-lookup"><span data-stu-id="e1614-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="e1614-141">此值永遠會以 UTC 時間傳回。</span><span class="sxs-lookup"><span data-stu-id="e1614-141">The value will always be returned as UTC time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1614-142">-主題</span><span class="sxs-lookup"><span data-stu-id="e1614-142">-Topic</span></span>
<span data-ttu-id="e1614-143">定期事件發佈至 IoT 裝置的主題。</span><span class="sxs-lookup"><span data-stu-id="e1614-143">Topic where periodic events are published to IoT device.</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1614-144">-確認</span><span class="sxs-lookup"><span data-stu-id="e1614-144">-Confirm</span></span>
<span data-ttu-id="e1614-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1614-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1614-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1614-146">-WhatIf</span></span>
<span data-ttu-id="e1614-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1614-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1614-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1614-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1614-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1614-149">CommonParameters</span></span>
<span data-ttu-id="e1614-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1614-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1614-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e1614-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1614-152">輸入</span><span class="sxs-lookup"><span data-stu-id="e1614-152">INPUTS</span></span>

### <span data-ttu-id="e1614-153">所有</span><span class="sxs-lookup"><span data-stu-id="e1614-153">None</span></span>

## <span data-ttu-id="e1614-154">輸出</span><span class="sxs-lookup"><span data-stu-id="e1614-154">OUTPUTS</span></span>

### <span data-ttu-id="e1614-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="e1614-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="e1614-156">筆記</span><span class="sxs-lookup"><span data-stu-id="e1614-156">NOTES</span></span>

## <span data-ttu-id="e1614-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1614-157">RELATED LINKS</span></span>