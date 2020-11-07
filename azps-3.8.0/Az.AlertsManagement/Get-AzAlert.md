---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: da462e5a8fd95b32275e37097bef18a2e7928d6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957149"
---
# <span data-ttu-id="0217b-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="0217b-101">Get-AzAlert</span></span>

## <span data-ttu-id="0217b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0217b-102">SYNOPSIS</span></span>
<span data-ttu-id="0217b-103">取得提醒資訊</span><span class="sxs-lookup"><span data-stu-id="0217b-103">Get Alerts Information</span></span>

## <span data-ttu-id="0217b-104">句法</span><span class="sxs-lookup"><span data-stu-id="0217b-104">SYNTAX</span></span>

### <span data-ttu-id="0217b-105">AlertsListByFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="0217b-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0217b-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="0217b-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0217b-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="0217b-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0217b-108">說明</span><span class="sxs-lookup"><span data-stu-id="0217b-108">DESCRIPTION</span></span>
<span data-ttu-id="0217b-109">**AzAlert** Cmdlet 會觸發警報實例。</span><span class="sxs-lookup"><span data-stu-id="0217b-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="0217b-110">示例</span><span class="sxs-lookup"><span data-stu-id="0217b-110">EXAMPLES</span></span>

### <span data-ttu-id="0217b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0217b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="0217b-112">使用 Sev2 嚴重度及激發的監視器條件列出所有警示。</span><span class="sxs-lookup"><span data-stu-id="0217b-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="0217b-113">將 IncludeCoNtext 設定為 true，包括自訂的警示負載。</span><span class="sxs-lookup"><span data-stu-id="0217b-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="0217b-114">使用 Format-List 取得清單中每個警示的完整詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0217b-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="0217b-115">範例2</span><span class="sxs-lookup"><span data-stu-id="0217b-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="0217b-116">透過識別碼 (GUID) 或資源識別碼 (完整 ARM Id 取得警報詳細資料) </span><span class="sxs-lookup"><span data-stu-id="0217b-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="0217b-117">參數</span><span class="sxs-lookup"><span data-stu-id="0217b-117">PARAMETERS</span></span>

### <span data-ttu-id="0217b-118">-AlertId</span><span class="sxs-lookup"><span data-stu-id="0217b-118">-AlertId</span></span>
<span data-ttu-id="0217b-119">警示/警示的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="0217b-119">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="0217b-120">-AlertRuleId</span></span>
<span data-ttu-id="0217b-121">篩選警示規則識別碼</span><span class="sxs-lookup"><span data-stu-id="0217b-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-122">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="0217b-122">-CustomTimeRange</span></span>
<span data-ttu-id="0217b-123">支援的格式- \< \> / \< \> 在時間為 ISO-8601 格式時的開始時間結束時間</span><span class="sxs-lookup"><span data-stu-id="0217b-123">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0217b-124">-DefaultProfile</span></span>
<span data-ttu-id="0217b-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0217b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0217b-126">-IncludeCoNtext</span><span class="sxs-lookup"><span data-stu-id="0217b-126">-IncludeContext</span></span>
<span data-ttu-id="0217b-127">包含內容 (自訂的負載) 警報</span><span class="sxs-lookup"><span data-stu-id="0217b-127">Include context (custom payload) of alert</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-128">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="0217b-128">-IncludeEgressConfig</span></span>
<span data-ttu-id="0217b-129">包括 EgressConfig</span><span class="sxs-lookup"><span data-stu-id="0217b-129">Include EgressConfig</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-130">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="0217b-130">-MonitorCondition</span></span>
<span data-ttu-id="0217b-131">篩選監視器條件</span><span class="sxs-lookup"><span data-stu-id="0217b-131">Filter on Monitor Condition</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-132">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="0217b-132">-MonitorService</span></span>
<span data-ttu-id="0217b-133">篩選 Moniter 服務</span><span class="sxs-lookup"><span data-stu-id="0217b-133">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-134">-PageCount</span><span class="sxs-lookup"><span data-stu-id="0217b-134">-PageCount</span></span>
<span data-ttu-id="0217b-135">要在頁面中回遷的警示數目。</span><span class="sxs-lookup"><span data-stu-id="0217b-135">Number of alerts to be fetched in a page.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-136">-選取</span><span class="sxs-lookup"><span data-stu-id="0217b-136">-Select</span></span>
<span data-ttu-id="0217b-137">從基本版將必要的欄位投影出來。</span><span class="sxs-lookup"><span data-stu-id="0217b-137">Project the required fields out of essentials.</span></span>
<span data-ttu-id="0217b-138">預期的輸入是以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="0217b-138">Expected input is comma-separated.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-139">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="0217b-139">-Severity</span></span>
<span data-ttu-id="0217b-140">在警示嚴重度篩選</span><span class="sxs-lookup"><span data-stu-id="0217b-140">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-141">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="0217b-141">-SmartGroupId</span></span>
<span data-ttu-id="0217b-142">篩選具有智慧群組識別碼的所有警示</span><span class="sxs-lookup"><span data-stu-id="0217b-142">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-143">-SortBy</span><span class="sxs-lookup"><span data-stu-id="0217b-143">-SortBy</span></span>
<span data-ttu-id="0217b-144">排序時要使用的警示屬性</span><span class="sxs-lookup"><span data-stu-id="0217b-144">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-145">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="0217b-145">-SortOrder</span></span>
<span data-ttu-id="0217b-146">排序次序</span><span class="sxs-lookup"><span data-stu-id="0217b-146">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-147">-State</span><span class="sxs-lookup"><span data-stu-id="0217b-147">-State</span></span>
<span data-ttu-id="0217b-148">篩選警示狀態</span><span class="sxs-lookup"><span data-stu-id="0217b-148">Filter on State of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-149">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0217b-149">-TargetResourceGroup</span></span>
<span data-ttu-id="0217b-150">篩選 [警示] 目標資源的 [資源] 群組名稱。</span><span class="sxs-lookup"><span data-stu-id="0217b-150">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-151">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="0217b-151">-TargetResourceId</span></span>
<span data-ttu-id="0217b-152">篩選警報目標資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0217b-152">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-153">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="0217b-153">-TargetResourceType</span></span>
<span data-ttu-id="0217b-154">篩選警報目標資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="0217b-154">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-155">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="0217b-155">-TimeRange</span></span>
<span data-ttu-id="0217b-156">支援的時間範圍值-1h、1d、7d、30d (預設為 1d) </span><span class="sxs-lookup"><span data-stu-id="0217b-156">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0217b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0217b-157">CommonParameters</span></span>
<span data-ttu-id="0217b-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0217b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0217b-159">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0217b-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0217b-160">輸入</span><span class="sxs-lookup"><span data-stu-id="0217b-160">INPUTS</span></span>

### <span data-ttu-id="0217b-161">所有</span><span class="sxs-lookup"><span data-stu-id="0217b-161">None</span></span>

## <span data-ttu-id="0217b-162">輸出</span><span class="sxs-lookup"><span data-stu-id="0217b-162">OUTPUTS</span></span>

### <span data-ttu-id="0217b-163">AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="0217b-163">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="0217b-164">筆記</span><span class="sxs-lookup"><span data-stu-id="0217b-164">NOTES</span></span>

## <span data-ttu-id="0217b-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="0217b-165">RELATED LINKS</span></span>