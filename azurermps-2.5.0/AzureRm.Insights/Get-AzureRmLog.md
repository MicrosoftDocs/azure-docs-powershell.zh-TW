---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlog
schema: 2.0.0
ms.openlocfilehash: 2c63efe0d22f1582b0828f595ba8a72cd389b435
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799954"
---
# <span data-ttu-id="43a29-101">Get-AzureRmLog</span><span class="sxs-lookup"><span data-stu-id="43a29-101">Get-AzureRmLog</span></span>

## <span data-ttu-id="43a29-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43a29-102">SYNOPSIS</span></span>
<span data-ttu-id="43a29-103">取得事件的記錄。</span><span class="sxs-lookup"><span data-stu-id="43a29-103">Gets a log of events.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43a29-104">句法</span><span class="sxs-lookup"><span data-stu-id="43a29-104">SYNTAX</span></span>

### <span data-ttu-id="43a29-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="43a29-105">GetByCorrelationId</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43a29-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="43a29-106">GetByResourceId</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43a29-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="43a29-107">GetByResourceGroup</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43a29-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="43a29-108">GetByResourceProvider</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43a29-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="43a29-109">GetBySubscription</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43a29-110">說明</span><span class="sxs-lookup"><span data-stu-id="43a29-110">DESCRIPTION</span></span>
<span data-ttu-id="43a29-111">**AzureRmLog** Cmdlet 會取得事件的記錄。</span><span class="sxs-lookup"><span data-stu-id="43a29-111">The **Get-AzureRmLog** cmdlet gets a log of events.</span></span>
<span data-ttu-id="43a29-112">事件可以與目前的訂閱識別碼、相關識別碼、資源群組、資源識別碼或資源提供者相關聯。</span><span class="sxs-lookup"><span data-stu-id="43a29-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="43a29-113">示例</span><span class="sxs-lookup"><span data-stu-id="43a29-113">EXAMPLES</span></span>

### <span data-ttu-id="43a29-114">範例1：依訂閱識別碼取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="43a29-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzureRmLog
```

<span data-ttu-id="43a29-115">這個命令會列出與使用者訂閱識別碼相關聯的1000事件，這些事件是在目前日期/時間之前的7天內發生。</span><span class="sxs-lookup"><span data-stu-id="43a29-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="43a29-116">範例2：依訂閱識別碼（含最大事件數）來取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="43a29-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -MaxEvents 100
```

<span data-ttu-id="43a29-117">這個命令會列出與使用者訂閱識別碼相關聯的100事件，這些事件是在目前日期/時間之前的7天內發生。</span><span class="sxs-lookup"><span data-stu-id="43a29-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="43a29-118">範例3：依訂閱識別碼（含開始時間）取得事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="43a29-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzureRmLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="43a29-119">這個命令會列出與在2017年或2017之後所發生的使用者訂閱識別碼相關聯的1000事件（最大01T10：30個當地時間），如果該日期/時間不是從目前日期/時間的90天之前。</span><span class="sxs-lookup"><span data-stu-id="43a29-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="43a29-120">範例4：按照訂閱識別碼，以開始時間和結束時間來取得事件記錄。</span><span class="sxs-lookup"><span data-stu-id="43a29-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzureRmLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="43a29-121">這個命令最多可列出與在2017年或2017年之後所發生的使用者訂閱 ID 相關的事件 1000 01T10：30個當地時間，以及2017年-14T11：30（當地時間）如果整個日期/時間範圍不超過從目前日期/時間的90天，亦即： [保留期間]。</span><span class="sxs-lookup"><span data-stu-id="43a29-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="43a29-122">範例5：依相關識別碼取得事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="43a29-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="43a29-123">這個命令會列出與指定的相關識別碼相關聯的1000事件，這些事件會從目前的日期/時間開始，發生7天。</span><span class="sxs-lookup"><span data-stu-id="43a29-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="43a29-124">**注意** ：這通常只是一個事件。</span><span class="sxs-lookup"><span data-stu-id="43a29-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="43a29-125">範例6：使用最大事件數的相關識別碼來取得事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="43a29-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxEvents 100
```

<span data-ttu-id="43a29-126">這個命令會列出與指定的相關識別碼相關聯的100事件，這些事件會從目前的日期/時間開始，發生7天。</span><span class="sxs-lookup"><span data-stu-id="43a29-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="43a29-127">**注意** ：這通常只是一個事件。</span><span class="sxs-lookup"><span data-stu-id="43a29-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="43a29-128">範例7：依相關識別碼和開始時間取得事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="43a29-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="43a29-129">這個命令最多可列出與2017年或2017之後所發生的指定相關識別碼相關聯的1000事件，22T04：30：00當地時間（如果開始時間不是從目前日期/時間的90天之前）。</span><span class="sxs-lookup"><span data-stu-id="43a29-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="43a29-130">**注意** ：這通常只是一個事件。</span><span class="sxs-lookup"><span data-stu-id="43a29-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="43a29-131">範例8：依 [開始時間] 和 [結束時間] 的相關識別碼來取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="43a29-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="43a29-132">這個命令會列出與在2017年或2017年15T04：30個當地時間，但在2017年到 04-25T12：30個當地時間為止，如果整個日期/時間範圍不是從目前日期/時間開始的90天內，就會列出與此設定相關聯的1000事件（例如： [保留期間]）。</span><span class="sxs-lookup"><span data-stu-id="43a29-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="43a29-133">範例9：取得資源群組的事件記錄</span><span class="sxs-lookup"><span data-stu-id="43a29-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="43a29-134">這個命令1000最多可列出與指定資源群組相關聯的事件，這些事件是從目前的日期/時間開始7天。</span><span class="sxs-lookup"><span data-stu-id="43a29-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="43a29-135">範例10：取得含有最大事件數之資源群組的事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="43a29-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -MaxEvents 100
```

<span data-ttu-id="43a29-136">這個命令會列出與特定資源群組相關聯的100事件，這些事件是從目前的日期/時間開始7天。</span><span class="sxs-lookup"><span data-stu-id="43a29-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="43a29-137">範例11：依開始時間取得資源群組的事件記錄</span><span class="sxs-lookup"><span data-stu-id="43a29-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="43a29-138">這個命令最多可列出與2017年或之後所發生的指定資源群組相關聯的 1000 evetns，22T04：30：00當地時間（如果開始時間不早于目前日期/時間的90天）。</span><span class="sxs-lookup"><span data-stu-id="43a29-138">This command lists at most 1000 evetns associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="43a29-139">範例12：取得具有開始時間和結束時間之資源群組的事件記錄</span><span class="sxs-lookup"><span data-stu-id="43a29-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="43a29-140">這個命令會列出與在2017年或2017之後所發生的特定資源群組相關聯的1000事件，但在2017年到 04-25T12：30個15T04 之前，如果整個日期/時間範圍不超過從目前日期/時間的90天，亦即： [保留期間]。</span><span class="sxs-lookup"><span data-stu-id="43a29-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="43a29-141">範例13：透過資源識別碼取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="43a29-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="43a29-142">這個命令會列出與指定的資源識別碼相關聯的1000事件，這些事件是從目前的日期/時間開始所發生的7天。</span><span class="sxs-lookup"><span data-stu-id="43a29-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="43a29-143">範例14：以資源識別碼（含最大事件數）來取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="43a29-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxEvents 100
```

<span data-ttu-id="43a29-144">這個命令會列出與指定的資源識別碼相關聯的100事件，這些事件是從目前的日期/時間開始所發生的7天。</span><span class="sxs-lookup"><span data-stu-id="43a29-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="43a29-145">範例15：透過資源識別碼取得開始時間的事件記錄</span><span class="sxs-lookup"><span data-stu-id="43a29-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="43a29-146">這個命令最多可列出與2017年或2017之後所發生的指定資源識別碼相關聯的1000事件（22T04：30：00當地時間），如果開始時間不是從目前日期/時間的90天之前。</span><span class="sxs-lookup"><span data-stu-id="43a29-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="43a29-147">範例16：以資源識別碼（含開始時間和結束時間）來取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="43a29-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="43a29-148">這個命令會列出與在2017年或2017年之後所發生的指定資源識別碼相關聯的1000事件，但在2017年到 04-25T12：30個15T04 之前，如果整個日期/時間範圍不是從目前日期/時間的90天之前，即為 [保留期間]。</span><span class="sxs-lookup"><span data-stu-id="43a29-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="43a29-149">範例17：透過資源提供者取得事件記錄</span><span class="sxs-lookup"><span data-stu-id="43a29-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="43a29-150">這個命令會列出與指定資源提供者相關的1000事件，這些事件是從目前的日期/時間開始所發生的7天。</span><span class="sxs-lookup"><span data-stu-id="43a29-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="43a29-151">範例18：以資源提供者取得最大事件數的事件記錄</span><span class="sxs-lookup"><span data-stu-id="43a29-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -MaxEvents 100
```

<span data-ttu-id="43a29-152">這個命令會列出與指定資源提供者相關的100事件，這些事件是從目前的日期/時間開始所發生的7天。</span><span class="sxs-lookup"><span data-stu-id="43a29-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="43a29-153">範例19：由資源提供者使用啟動時間來取得事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="43a29-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="43a29-154">這個命令會列出與在2017年或之後所發生的指定資源提供者相關聯的1000事件（最多個），22T04：30：00當地時間（如果開始時間不是從目前日期/時間的90天之前）。</span><span class="sxs-lookup"><span data-stu-id="43a29-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="43a29-155">範例20：透過資源提供者取得開始時間和結束時間的事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="43a29-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="43a29-156">這個命令會列出與在2017年或2017之後所發生的指定資源提供者所產生的1000事件（15T04：30個當地時間），但在2017年之前的25T12：30個當地時間（如果整個日期/時間範圍不是從目前日期/時間起的90天以內），亦即： [保留期間]。</span><span class="sxs-lookup"><span data-stu-id="43a29-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="43a29-157">參數</span><span class="sxs-lookup"><span data-stu-id="43a29-157">PARAMETERS</span></span>

### <span data-ttu-id="43a29-158">-來電者</span><span class="sxs-lookup"><span data-stu-id="43a29-158">-Caller</span></span>
<span data-ttu-id="43a29-159">指定來電者。</span><span class="sxs-lookup"><span data-stu-id="43a29-159">Specifies a caller.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a29-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="43a29-160">-CorrelationId</span></span>
<span data-ttu-id="43a29-161">指定相關識別碼。</span><span class="sxs-lookup"><span data-stu-id="43a29-161">Specifies the correlation ID.</span></span>
<span data-ttu-id="43a29-162">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="43a29-162">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a29-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a29-163">-DefaultProfile</span></span>
<span data-ttu-id="43a29-164">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="43a29-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43a29-165">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="43a29-165">-DetailedOutput</span></span>
<span data-ttu-id="43a29-166">表示此 Cmdlet 會顯示詳細的輸出。</span><span class="sxs-lookup"><span data-stu-id="43a29-166">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="43a29-167">根據預設，輸出是匯總的。</span><span class="sxs-lookup"><span data-stu-id="43a29-167">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a29-168">-EndTime</span><span class="sxs-lookup"><span data-stu-id="43a29-168">-EndTime</span></span>
<span data-ttu-id="43a29-169">指定當地時間的查詢結束時間。</span><span class="sxs-lookup"><span data-stu-id="43a29-169">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="43a29-170">預設值是目前的時間。</span><span class="sxs-lookup"><span data-stu-id="43a29-170">The default value is the current time.</span></span>
<span data-ttu-id="43a29-171">此值必須晚于 *StartTime* 。</span><span class="sxs-lookup"><span data-stu-id="43a29-171">The value must be later than *StartTime*.</span></span>
<span data-ttu-id="43a29-172">您可以使用 Get-Date Cmdlet 來取得 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="43a29-172">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a29-173">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="43a29-173">-MaxRecord</span></span>
<span data-ttu-id="43a29-174">指定要取得指定篩選的記錄總數。</span><span class="sxs-lookup"><span data-stu-id="43a29-174">Specifies the total number of records to fetch for the specified filter.</span></span>
<span data-ttu-id="43a29-175">預設值為1000，且已接受的最大值為100000。</span><span class="sxs-lookup"><span data-stu-id="43a29-175">The default value is 1000 and the maximum value accepted is 100000.</span></span> <span data-ttu-id="43a29-176">負值和0會被忽略，且會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="43a29-176">Negative values and 0 are ignored and the default value will be used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a29-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43a29-177">-ResourceGroupName</span></span>
<span data-ttu-id="43a29-178">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="43a29-178">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a29-179">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43a29-179">-ResourceId</span></span>
<span data-ttu-id="43a29-180">指定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="43a29-180">Specifies the resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a29-181">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="43a29-181">-ResourceProvider</span></span>
<span data-ttu-id="43a29-182">指定依據資源提供者的篩選。</span><span class="sxs-lookup"><span data-stu-id="43a29-182">Specifies a filter by resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a29-183">-StartTime</span><span class="sxs-lookup"><span data-stu-id="43a29-183">-StartTime</span></span>
<span data-ttu-id="43a29-184">指定當地時間查詢的開始時間。</span><span class="sxs-lookup"><span data-stu-id="43a29-184">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="43a29-185">預設值為 [ *EndTime* 減去七天]。</span><span class="sxs-lookup"><span data-stu-id="43a29-185">The default value is *EndTime* minus seven days.</span></span>
<span data-ttu-id="43a29-186">您可以使用 Get-Date Cmdlet 來取得 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="43a29-186">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a29-187">-狀態</span><span class="sxs-lookup"><span data-stu-id="43a29-187">-Status</span></span>
<span data-ttu-id="43a29-188">指定狀態。</span><span class="sxs-lookup"><span data-stu-id="43a29-188">Specifies the status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43a29-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a29-189">CommonParameters</span></span>
<span data-ttu-id="43a29-190">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43a29-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a29-191">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43a29-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a29-192">輸入</span><span class="sxs-lookup"><span data-stu-id="43a29-192">INPUTS</span></span>

### <span data-ttu-id="43a29-193">系統. Nullable "1 [[System. DateTime，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="43a29-193">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="43a29-194">System.object</span><span class="sxs-lookup"><span data-stu-id="43a29-194">System.String</span></span>

### <span data-ttu-id="43a29-195">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="43a29-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="43a29-196">System.object</span><span class="sxs-lookup"><span data-stu-id="43a29-196">System.Int32</span></span>

## <span data-ttu-id="43a29-197">輸出</span><span class="sxs-lookup"><span data-stu-id="43a29-197">OUTPUTS</span></span>

### <span data-ttu-id="43a29-198">PSEventData 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="43a29-198">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="43a29-199">筆記</span><span class="sxs-lookup"><span data-stu-id="43a29-199">NOTES</span></span>

## <span data-ttu-id="43a29-200">相關連結</span><span class="sxs-lookup"><span data-stu-id="43a29-200">RELATED LINKS</span></span>