---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287620"
---
# <span data-ttu-id="bed50-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="bed50-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="bed50-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bed50-102">SYNOPSIS</span></span>
<span data-ttu-id="bed50-103">取得支援票證。</span><span class="sxs-lookup"><span data-stu-id="bed50-103">Get support tickets.</span></span>

## <span data-ttu-id="bed50-104">句法</span><span class="sxs-lookup"><span data-stu-id="bed50-104">SYNTAX</span></span>

### <span data-ttu-id="bed50-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bed50-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="bed50-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bed50-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="bed50-107">說明</span><span class="sxs-lookup"><span data-stu-id="bed50-107">DESCRIPTION</span></span>
<span data-ttu-id="bed50-108">取得支援票證的清單。</span><span class="sxs-lookup"><span data-stu-id="bed50-108">Gets the list of support tickets.</span></span> <span data-ttu-id="bed50-109">如果您沒有指定任何參數，就會取得所有支援票證。</span><span class="sxs-lookup"><span data-stu-id="bed50-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="bed50-110">您也可以使用 Filter 參數，依狀態或 CreatedDate 篩選支援票證。</span><span class="sxs-lookup"><span data-stu-id="bed50-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="bed50-111">以下是您可以指定之篩選值的一些範例。</span><span class="sxs-lookup"><span data-stu-id="bed50-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="bed50-112">例子</span><span class="sxs-lookup"><span data-stu-id="bed50-112">Scenario</span></span>                                                         | <span data-ttu-id="bed50-113">條件</span><span class="sxs-lookup"><span data-stu-id="bed50-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="bed50-114">取得處於開啟狀態的入場券</span><span class="sxs-lookup"><span data-stu-id="bed50-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="bed50-115">"狀態 eq" 開啟 ""</span><span class="sxs-lookup"><span data-stu-id="bed50-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="bed50-116">取得處於關閉狀態的入場券</span><span class="sxs-lookup"><span data-stu-id="bed50-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="bed50-117">"狀態 eq" 已關閉 ""</span><span class="sxs-lookup"><span data-stu-id="bed50-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="bed50-118">取得在2019年12月20日或之後所建立的票證</span><span class="sxs-lookup"><span data-stu-id="bed50-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="bed50-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="bed50-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="bed50-120">取得2019年12月20日之後所建立的票證</span><span class="sxs-lookup"><span data-stu-id="bed50-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="bed50-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="bed50-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="bed50-122">取得處於開啟狀態的2019年12月20日之後所建立的票證</span><span class="sxs-lookup"><span data-stu-id="bed50-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="bed50-123">"CreatedDate gt 2019-12-20 和狀態 eq" Open ""</span><span class="sxs-lookup"><span data-stu-id="bed50-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="bed50-124">這個 Cmdlet 支援透過第一個和略過參數進行分頁。</span><span class="sxs-lookup"><span data-stu-id="bed50-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="bed50-125">您也可以透過指定票證名稱來取得單一支援票證。</span><span class="sxs-lookup"><span data-stu-id="bed50-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="bed50-126">示例</span><span class="sxs-lookup"><span data-stu-id="bed50-126">EXAMPLES</span></span>

### <span data-ttu-id="bed50-127">範例1：取得前2個入場券</span><span class="sxs-lookup"><span data-stu-id="bed50-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="bed50-128">範例2：略過前2個票證之後取得前2個入場券</span><span class="sxs-lookup"><span data-stu-id="bed50-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="bed50-129">範例3：依名稱取得支援票證</span><span class="sxs-lookup"><span data-stu-id="bed50-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="bed50-130">範例4：取得前2個依狀態篩選的支援票證</span><span class="sxs-lookup"><span data-stu-id="bed50-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="bed50-131">範例5：取得開啟狀態中的所有支援票證，並在2019年12月20日之後建立</span><span class="sxs-lookup"><span data-stu-id="bed50-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="bed50-132">參數</span><span class="sxs-lookup"><span data-stu-id="bed50-132">PARAMETERS</span></span>

### <span data-ttu-id="bed50-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bed50-133">-DefaultProfile</span></span>
<span data-ttu-id="bed50-134">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bed50-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bed50-135">-篩選</span><span class="sxs-lookup"><span data-stu-id="bed50-135">-Filter</span></span>
<span data-ttu-id="bed50-136">要套用至此 Cmdlet 結果的篩選。</span><span class="sxs-lookup"><span data-stu-id="bed50-136">Filter to be applied to the results of this cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed50-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="bed50-137">-Name</span></span>
<span data-ttu-id="bed50-138">此 Cmdlet 取得的支援票證的名稱。</span><span class="sxs-lookup"><span data-stu-id="bed50-138">Name of support ticket that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed50-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="bed50-139">-IncludeTotalCount</span></span>
<span data-ttu-id="bed50-140">報告資料集中的物件總數 (整數) 接著選取的物件。</span><span class="sxs-lookup"><span data-stu-id="bed50-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="bed50-141">如果 Cmdlet 無法判斷總計數，則會顯示「未知總計數」。</span><span class="sxs-lookup"><span data-stu-id="bed50-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="bed50-142">這個整數有一個正確性屬性，指出總計數值的可靠性。</span><span class="sxs-lookup"><span data-stu-id="bed50-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="bed50-143">精確度的值範圍從0.0 到1.0，其中0.0 表示 Cmdlet 無法計算物件，1.0 表示該計數完全正確，而在0.0 與1.0 之間的值則表示日益可靠的估計。</span><span class="sxs-lookup"><span data-stu-id="bed50-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="bed50-144">-略過</span><span class="sxs-lookup"><span data-stu-id="bed50-144">-Skip</span></span>
<span data-ttu-id="bed50-145">忽略指定的物件數目，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="bed50-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="bed50-146">輸入要略過的物件數目。</span><span class="sxs-lookup"><span data-stu-id="bed50-146">Enter the number of objects to skip.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed50-147">-優先</span><span class="sxs-lookup"><span data-stu-id="bed50-147">-First</span></span>
<span data-ttu-id="bed50-148">只取得指定數目的物件。</span><span class="sxs-lookup"><span data-stu-id="bed50-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="bed50-149">輸入要取得的物件數目。</span><span class="sxs-lookup"><span data-stu-id="bed50-149">Enter the number of objects to get.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed50-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bed50-150">CommonParameters</span></span>
<span data-ttu-id="bed50-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bed50-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bed50-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bed50-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bed50-153">輸入</span><span class="sxs-lookup"><span data-stu-id="bed50-153">INPUTS</span></span>

### <span data-ttu-id="bed50-154">所有</span><span class="sxs-lookup"><span data-stu-id="bed50-154">None</span></span>

## <span data-ttu-id="bed50-155">輸出</span><span class="sxs-lookup"><span data-stu-id="bed50-155">OUTPUTS</span></span>

### <span data-ttu-id="bed50-156">PSSupportTicket （支援）。</span><span class="sxs-lookup"><span data-stu-id="bed50-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="bed50-157">筆記</span><span class="sxs-lookup"><span data-stu-id="bed50-157">NOTES</span></span>

## <span data-ttu-id="bed50-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="bed50-158">RELATED LINKS</span></span>