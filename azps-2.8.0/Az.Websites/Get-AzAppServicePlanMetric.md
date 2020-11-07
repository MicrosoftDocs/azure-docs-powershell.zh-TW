---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplanmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
ms.openlocfilehash: 04f07e435f8656ef18e452538d97b3728179c969
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793258"
---
# <span data-ttu-id="322df-101">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="322df-101">Get-AzAppServicePlanMetric</span></span>

## <span data-ttu-id="322df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="322df-102">SYNOPSIS</span></span>

## <span data-ttu-id="322df-103">句法</span><span class="sxs-lookup"><span data-stu-id="322df-103">SYNTAX</span></span>

### <span data-ttu-id="322df-104">S1</span><span class="sxs-lookup"><span data-stu-id="322df-104">S1</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="322df-105">S2</span><span class="sxs-lookup"><span data-stu-id="322df-105">S2</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="322df-106">說明</span><span class="sxs-lookup"><span data-stu-id="322df-106">DESCRIPTION</span></span>
<span data-ttu-id="322df-107">**AzAppServicePlanMetric** 會取得 App 服務方案度量單位。</span><span class="sxs-lookup"><span data-stu-id="322df-107">The **Get-AzAppServicePlanMetric** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="322df-108">示例</span><span class="sxs-lookup"><span data-stu-id="322df-108">EXAMPLES</span></span>

### <span data-ttu-id="322df-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="322df-109">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="322df-110">這個命令會在每分鐘 (PT1M 輪詢時間1分鐘內，) StartTime 和 EndTime 之間取得 App 服務方案的 CPU 百分比</span><span class="sxs-lookup"><span data-stu-id="322df-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="322df-111">參數</span><span class="sxs-lookup"><span data-stu-id="322df-111">PARAMETERS</span></span>

### <span data-ttu-id="322df-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="322df-112">-AppServicePlan</span></span>
<span data-ttu-id="322df-113">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="322df-113">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="322df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="322df-114">-DefaultProfile</span></span>
<span data-ttu-id="322df-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="322df-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="322df-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="322df-116">-EndTime</span></span>
<span data-ttu-id="322df-117">UTC 的結束時間</span><span class="sxs-lookup"><span data-stu-id="322df-117">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322df-118">-細微性</span><span class="sxs-lookup"><span data-stu-id="322df-118">-Granularity</span></span>
<span data-ttu-id="322df-119">細微性</span><span class="sxs-lookup"><span data-stu-id="322df-119">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322df-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="322df-120">-InstanceDetails</span></span>
<span data-ttu-id="322df-121">實例詳細資料</span><span class="sxs-lookup"><span data-stu-id="322df-121">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322df-122">-度量單位</span><span class="sxs-lookup"><span data-stu-id="322df-122">-Metrics</span></span>
<span data-ttu-id="322df-123">指標</span><span class="sxs-lookup"><span data-stu-id="322df-123">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322df-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="322df-124">-Name</span></span>
<span data-ttu-id="322df-125">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="322df-125">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322df-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="322df-126">-ResourceGroupName</span></span>
<span data-ttu-id="322df-127">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="322df-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322df-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="322df-128">-StartTime</span></span>
<span data-ttu-id="322df-129">UTC 的開始時間</span><span class="sxs-lookup"><span data-stu-id="322df-129">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322df-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="322df-130">CommonParameters</span></span>
<span data-ttu-id="322df-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="322df-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="322df-132">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="322df-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="322df-133">輸入</span><span class="sxs-lookup"><span data-stu-id="322df-133">INPUTS</span></span>

### <span data-ttu-id="322df-134">WebApps WebApp. PSAppServicePlan （）</span><span class="sxs-lookup"><span data-stu-id="322df-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="322df-135">輸出</span><span class="sxs-lookup"><span data-stu-id="322df-135">OUTPUTS</span></span>

### <span data-ttu-id="322df-136">ResourceMetric 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="322df-136">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="322df-137">筆記</span><span class="sxs-lookup"><span data-stu-id="322df-137">NOTES</span></span>

## <span data-ttu-id="322df-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="322df-138">RELATED LINKS</span></span>