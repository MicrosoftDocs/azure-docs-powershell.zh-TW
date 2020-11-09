---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 865ab4ab3cca9d921fc8c40e9c6ae5cd03eaf00a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288103"
---
# <span data-ttu-id="d66f9-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d66f9-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="d66f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d66f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d66f9-103">從私人 DNS 區域刪除記錄集。</span><span class="sxs-lookup"><span data-stu-id="d66f9-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="d66f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="d66f9-104">SYNTAX</span></span>

### <span data-ttu-id="d66f9-105">預設)  (的欄位</span><span class="sxs-lookup"><span data-stu-id="d66f9-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d66f9-106">混淆</span><span class="sxs-lookup"><span data-stu-id="d66f9-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d66f9-107">面向</span><span class="sxs-lookup"><span data-stu-id="d66f9-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d66f9-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d66f9-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d66f9-109">說明</span><span class="sxs-lookup"><span data-stu-id="d66f9-109">DESCRIPTION</span></span>
<span data-ttu-id="d66f9-110">Remove-AzPrivateDnsRecordSet Cmdlet 會從指定的區域刪除指定的記錄集。</span><span class="sxs-lookup"><span data-stu-id="d66f9-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="d66f9-111">您無法刪除在私人區域 apex 自動建立的 SOA 記錄。</span><span class="sxs-lookup"><span data-stu-id="d66f9-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="d66f9-112">您可以使用管線運算子或作為參數或 ResourceId，將 RecordSet 物件傳遞到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d66f9-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="d66f9-113">若要透過名稱和類型來找出不使用 RecordSet 物件的記錄，您必須使用管線運算子或參數，將該區域以 PSPrivateDnsZone 物件傳遞給這個 Cmdlet，或者也可以指定 ZoneName 和 ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="d66f9-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="d66f9-114">您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d66f9-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="d66f9-115">使用 RecordSet 物件指定記錄集時，如果在已檢索到本機 RecordSet 物件之後，在 Azure 私人 DNS 中變更了記錄集，就不會刪除。</span><span class="sxs-lookup"><span data-stu-id="d66f9-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="d66f9-116">這可為併發變更提供保護。</span><span class="sxs-lookup"><span data-stu-id="d66f9-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="d66f9-117">您可以使用 Overwrite 參數來取消這項設定，不論併發變更為何，都會刪除記錄集。</span><span class="sxs-lookup"><span data-stu-id="d66f9-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="d66f9-118">示例</span><span class="sxs-lookup"><span data-stu-id="d66f9-118">EXAMPLES</span></span>

### <span data-ttu-id="d66f9-119">範例1：移除記錄集</span><span class="sxs-lookup"><span data-stu-id="d66f9-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="d66f9-120">第一個命令會取得指定的記錄集，然後將它儲存在 $RecordSet 變數中。第二個命令會移除 $RecordSet 中的記錄集。</span><span class="sxs-lookup"><span data-stu-id="d66f9-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="d66f9-121">範例2：移除記錄集並禁止所有確認</span><span class="sxs-lookup"><span data-stu-id="d66f9-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="d66f9-122">第一個命令會取得指定的記錄集。</span><span class="sxs-lookup"><span data-stu-id="d66f9-122">The first command gets the specified record set.</span></span> <span data-ttu-id="d66f9-123">第二個命令會刪除記錄集，即使在其間已變更也一樣。</span><span class="sxs-lookup"><span data-stu-id="d66f9-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="d66f9-124">已取消確認提示。</span><span class="sxs-lookup"><span data-stu-id="d66f9-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="d66f9-125">參數</span><span class="sxs-lookup"><span data-stu-id="d66f9-125">PARAMETERS</span></span>

### <span data-ttu-id="d66f9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d66f9-126">-DefaultProfile</span></span>
<span data-ttu-id="d66f9-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d66f9-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d66f9-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="d66f9-128">-Name</span></span>
<span data-ttu-id="d66f9-129">記錄集中的記錄名稱 (相對於區域的名稱，且不需要終止點) 。</span><span class="sxs-lookup"><span data-stu-id="d66f9-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66f9-130">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="d66f9-130">-Overwrite</span></span>
<span data-ttu-id="d66f9-131">請勿使用 RecordSet 參數的 ETag 欄位來進行開放式併發檢查。</span><span class="sxs-lookup"><span data-stu-id="d66f9-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66f9-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d66f9-132">-PassThru</span></span>
<span data-ttu-id="d66f9-133">用來傳送操作的結果 (布林) ，以從管線中移除私有區域。</span><span class="sxs-lookup"><span data-stu-id="d66f9-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="d66f9-134">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="d66f9-134">-RecordSet</span></span>
<span data-ttu-id="d66f9-135">要在其中新增記錄的記錄集。</span><span class="sxs-lookup"><span data-stu-id="d66f9-135">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d66f9-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="d66f9-136">-RecordType</span></span>
<span data-ttu-id="d66f9-137">記錄集中的私人 DNS 記錄類型。</span><span class="sxs-lookup"><span data-stu-id="d66f9-137">The type of Private DNS records in the record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66f9-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d66f9-138">-ResourceGroupName</span></span>
<span data-ttu-id="d66f9-139">該區域所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="d66f9-139">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66f9-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d66f9-140">-ResourceId</span></span>
<span data-ttu-id="d66f9-141">私人 DNS 記錄集 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="d66f9-141">Private DNS RecordSet ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d66f9-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="d66f9-142">-Zone</span></span>
<span data-ttu-id="d66f9-143">代表要在其中建立記錄集之區域的 PrivateDnsZone 物件。</span><span class="sxs-lookup"><span data-stu-id="d66f9-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d66f9-144">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="d66f9-144">-ZoneName</span></span>
<span data-ttu-id="d66f9-145">已存在記錄集的區域 (沒有終止點) 。</span><span class="sxs-lookup"><span data-stu-id="d66f9-145">The zone in which the record set exists (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66f9-146">-確認</span><span class="sxs-lookup"><span data-stu-id="d66f9-146">-Confirm</span></span>
<span data-ttu-id="d66f9-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d66f9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d66f9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d66f9-148">-WhatIf</span></span>
<span data-ttu-id="d66f9-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d66f9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d66f9-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d66f9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d66f9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d66f9-151">CommonParameters</span></span>
<span data-ttu-id="d66f9-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d66f9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d66f9-153">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d66f9-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d66f9-154">輸入</span><span class="sxs-lookup"><span data-stu-id="d66f9-154">INPUTS</span></span>

### <span data-ttu-id="d66f9-155">PSPrivateDnsZone 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="d66f9-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="d66f9-156">PSPrivateDnsRecordSet 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="d66f9-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="d66f9-157">System.object</span><span class="sxs-lookup"><span data-stu-id="d66f9-157">System.String</span></span>

## <span data-ttu-id="d66f9-158">輸出</span><span class="sxs-lookup"><span data-stu-id="d66f9-158">OUTPUTS</span></span>

### <span data-ttu-id="d66f9-159">System.object</span><span class="sxs-lookup"><span data-stu-id="d66f9-159">System.Boolean</span></span>

## <span data-ttu-id="d66f9-160">筆記</span><span class="sxs-lookup"><span data-stu-id="d66f9-160">NOTES</span></span>

## <span data-ttu-id="d66f9-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="d66f9-161">RELATED LINKS</span></span>