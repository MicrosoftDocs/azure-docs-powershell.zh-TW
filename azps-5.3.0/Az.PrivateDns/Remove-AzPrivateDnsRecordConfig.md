---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 1e3362850880f02c648fb3318db226515fc95eef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435674"
---
# <span data-ttu-id="9d93f-101">Remove-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9d93f-101">Remove-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="9d93f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d93f-102">SYNOPSIS</span></span>
<span data-ttu-id="9d93f-103">從本機記錄集物件中移除私人 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="9d93f-103">Removes a Private DNS record from a local record set object.</span></span>

## <span data-ttu-id="9d93f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d93f-104">SYNTAX</span></span>

### <span data-ttu-id="9d93f-105"> (預設) </span><span class="sxs-lookup"><span data-stu-id="9d93f-105">A (Default)</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d93f-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="9d93f-106">AAAA</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d93f-107">MX</span><span class="sxs-lookup"><span data-stu-id="9d93f-107">MX</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d93f-108">PTR</span><span class="sxs-lookup"><span data-stu-id="9d93f-108">PTR</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d93f-109">文字檔</span><span class="sxs-lookup"><span data-stu-id="9d93f-109">TXT</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d93f-110">DNS-SRV</span><span class="sxs-lookup"><span data-stu-id="9d93f-110">SRV</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d93f-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="9d93f-111">CNAME</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d93f-112">說明</span><span class="sxs-lookup"><span data-stu-id="9d93f-112">DESCRIPTION</span></span>
<span data-ttu-id="9d93f-113">Remove-AzPrivateDnsRecordConfig Cmdlet 會從記錄集中移除 (DNS) 記錄的私人網功能變數名稱稱系統。</span><span class="sxs-lookup"><span data-stu-id="9d93f-113">The Remove-AzPrivateDnsRecordConfig cmdlet removes a Private Domain Name System (DNS) record from a record set.</span></span> <span data-ttu-id="9d93f-114">RecordSet 物件是離線物件，而對它所做的變更不會變更私人 DNS 回應，除非您執行 Set-AzPrivateDnsRecordSet Cmdlet，才能保留 Microsoft Azure 私人 DNS 服務的變更。</span><span class="sxs-lookup"><span data-stu-id="9d93f-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="9d93f-115">若要移除記錄，該記錄類型的所有欄位都必須完全相符。</span><span class="sxs-lookup"><span data-stu-id="9d93f-115">To remove a record, all the fields for that record type must match exactly.</span></span> <span data-ttu-id="9d93f-116">您無法新增或移除 SOA 記錄。</span><span class="sxs-lookup"><span data-stu-id="9d93f-116">You cannot add or remove SOA records.</span></span> <span data-ttu-id="9d93f-117">當您在 [私人 dns 區域] 被刪除時，系統會自動建立 SOA 記錄，並自動刪除。</span><span class="sxs-lookup"><span data-stu-id="9d93f-117">SOA records are automatically created when a Private DNS zone is created and automatically deleted when the Private DNS zone is deleted.</span></span> <span data-ttu-id="9d93f-118">您可以將 RecordSet 物件作為參數傳遞給這個 Cmdlet，或使用管線運算子。</span><span class="sxs-lookup"><span data-stu-id="9d93f-118">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="9d93f-119">示例</span><span class="sxs-lookup"><span data-stu-id="9d93f-119">EXAMPLES</span></span>

### <span data-ttu-id="9d93f-120">範例1：從記錄集中移除 A 記錄</span><span class="sxs-lookup"><span data-stu-id="9d93f-120">Example 1: Remove an A record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="9d93f-121">這個範例會從現有的記錄集中移除 A 記錄。</span><span class="sxs-lookup"><span data-stu-id="9d93f-121">This example removes an A record from an existing record set.</span></span> <span data-ttu-id="9d93f-122">如果這是記錄集中的唯一記錄，結果就會是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="9d93f-122">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="9d93f-123">若要完全移除記錄集，請參閱移除-AzPrivateDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="9d93f-123">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="9d93f-124">範例2：從記錄集中移除 AAAA 記錄</span><span class="sxs-lookup"><span data-stu-id="9d93f-124">Example 2: Remove an AAAA record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="9d93f-125">這個範例會從現有的記錄集中移除 AAAA 記錄。</span><span class="sxs-lookup"><span data-stu-id="9d93f-125">This example removes an AAAA record from an existing record set.</span></span> <span data-ttu-id="9d93f-126">如果這是記錄集中的唯一記錄，結果就會是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="9d93f-126">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="9d93f-127">若要完全移除記錄集，請參閱移除-AzPrivateDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="9d93f-127">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="9d93f-128">範例3：從記錄集中移除 CNAME 記錄</span><span class="sxs-lookup"><span data-stu-id="9d93f-128">Example 3: Remove a CNAME record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="9d93f-129">這個範例會從現有的記錄集中移除 CNAME 記錄。</span><span class="sxs-lookup"><span data-stu-id="9d93f-129">This example removes a CNAME record from an existing record set.</span></span> <span data-ttu-id="9d93f-130">因為 CNAME 記錄集最多可以包含一筆記錄，所以結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="9d93f-130">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="9d93f-131">範例4：從記錄集中移除 MX 記錄</span><span class="sxs-lookup"><span data-stu-id="9d93f-131">Example 4: Remove a MX record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="9d93f-132">這個範例會從現有的記錄集中移除 MX 記錄。</span><span class="sxs-lookup"><span data-stu-id="9d93f-132">This example removes an MX record from an existing record set.</span></span> <span data-ttu-id="9d93f-133">記錄名稱 "@" 代表在區域 apex 上設定的記錄。</span><span class="sxs-lookup"><span data-stu-id="9d93f-133">The record name "@" indicates a record set at the zone apex.</span></span> <span data-ttu-id="9d93f-134">如果這是記錄集中的唯一記錄，則結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="9d93f-134">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="9d93f-135">若要完全移除記錄集，請參閱移除-AzPrivateDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="9d93f-135">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="9d93f-136">範例5：從記錄集中移除 PTR 記錄</span><span class="sxs-lookup"><span data-stu-id="9d93f-136">Example 5: Remove a PTR record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="9d93f-137">這個範例會從現有的記錄集中移除 PTR 記錄。</span><span class="sxs-lookup"><span data-stu-id="9d93f-137">This example removes a PTR record from an existing record set.</span></span> <span data-ttu-id="9d93f-138">如果這是記錄集中的唯一記錄，則結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="9d93f-138">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="9d93f-139">若要完全移除記錄集，請參閱移除-AzPrivateDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="9d93f-139">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="9d93f-140">範例6：從記錄集中移除 SRV 記錄</span><span class="sxs-lookup"><span data-stu-id="9d93f-140">Example 6: Remove a SRV record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="9d93f-141">這個範例會從現有的記錄集中移除 SRV 記錄。</span><span class="sxs-lookup"><span data-stu-id="9d93f-141">This example removes an SRV record from an existing record set.</span></span> <span data-ttu-id="9d93f-142">如果這是記錄集中的唯一記錄，則結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="9d93f-142">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="9d93f-143">若要完全移除記錄集，請參閱移除-AzPrivateDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="9d93f-143">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="9d93f-144">範例7：從記錄集中移除 TXT 記錄</span><span class="sxs-lookup"><span data-stu-id="9d93f-144">Example 7: Remove a TXT record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Value "This is a TXT Record"  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="9d93f-145">這個範例會從現有的記錄集中移除 TXT 記錄。</span><span class="sxs-lookup"><span data-stu-id="9d93f-145">This example removes a TXT record from an existing record set.</span></span> <span data-ttu-id="9d93f-146">如果這是記錄集中的唯一記錄，則結果是一個空的記錄集。</span><span class="sxs-lookup"><span data-stu-id="9d93f-146">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="9d93f-147">若要完全移除記錄集，請參閱移除-AzPrivateDnsRecordSet。</span><span class="sxs-lookup"><span data-stu-id="9d93f-147">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

## <span data-ttu-id="9d93f-148">參數</span><span class="sxs-lookup"><span data-stu-id="9d93f-148">PARAMETERS</span></span>

### <span data-ttu-id="9d93f-149">-Cname</span><span class="sxs-lookup"><span data-stu-id="9d93f-149">-Cname</span></span>
<span data-ttu-id="9d93f-150">要移除之 CNAME 記錄的正式名稱。</span><span class="sxs-lookup"><span data-stu-id="9d93f-150">The canonical name of the CNAME record to remove.</span></span>
<span data-ttu-id="9d93f-151">不得與區功能變數名稱稱相關。</span><span class="sxs-lookup"><span data-stu-id="9d93f-151">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="9d93f-152">不能有終止點</span><span class="sxs-lookup"><span data-stu-id="9d93f-152">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d93f-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d93f-153">-DefaultProfile</span></span>
<span data-ttu-id="9d93f-154">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d93f-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d93f-155">-Exchange</span><span class="sxs-lookup"><span data-stu-id="9d93f-155">-Exchange</span></span>
<span data-ttu-id="9d93f-156">要移除之 MX 記錄的郵件交換主機。</span><span class="sxs-lookup"><span data-stu-id="9d93f-156">The mail exchange host of the MX record to remove.</span></span>
<span data-ttu-id="9d93f-157">不得與區功能變數名稱稱相關。</span><span class="sxs-lookup"><span data-stu-id="9d93f-157">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="9d93f-158">不能有終止點</span><span class="sxs-lookup"><span data-stu-id="9d93f-158">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d93f-159">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="9d93f-159">-Ipv4Address</span></span>
<span data-ttu-id="9d93f-160">要移除之 A 記錄的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="9d93f-160">The IPv4 address of the A record to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d93f-161">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="9d93f-161">-Ipv6Address</span></span>
<span data-ttu-id="9d93f-162">要移除之 AAAA 記錄的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="9d93f-162">The IPv6 address of the AAAA record to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d93f-163">-埠</span><span class="sxs-lookup"><span data-stu-id="9d93f-163">-Port</span></span>
<span data-ttu-id="9d93f-164">要移除之 SRV 記錄的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="9d93f-164">The port number of the SRV record to remove.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d93f-165">-喜好設定</span><span class="sxs-lookup"><span data-stu-id="9d93f-165">-Preference</span></span>
<span data-ttu-id="9d93f-166">要移除之 MX 記錄的喜好設定值。</span><span class="sxs-lookup"><span data-stu-id="9d93f-166">The preference value of the MX record to remove.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d93f-167">-優先順序</span><span class="sxs-lookup"><span data-stu-id="9d93f-167">-Priority</span></span>
<span data-ttu-id="9d93f-168">要移除之 SRV 記錄的優先順序值。</span><span class="sxs-lookup"><span data-stu-id="9d93f-168">The priority value of the SRV record to remove.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d93f-169">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="9d93f-169">-Ptrdname</span></span>
<span data-ttu-id="9d93f-170">要移除之 PTR 記錄的目標主機。</span><span class="sxs-lookup"><span data-stu-id="9d93f-170">The target host of the PTR record to remove.</span></span>
<span data-ttu-id="9d93f-171">不得與區功能變數名稱稱相關。</span><span class="sxs-lookup"><span data-stu-id="9d93f-171">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="9d93f-172">不能有終止點</span><span class="sxs-lookup"><span data-stu-id="9d93f-172">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d93f-173">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="9d93f-173">-RecordSet</span></span>
<span data-ttu-id="9d93f-174">要從中移除記錄的記錄集。</span><span class="sxs-lookup"><span data-stu-id="9d93f-174">The record set from which to remove the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d93f-175">-目標</span><span class="sxs-lookup"><span data-stu-id="9d93f-175">-Target</span></span>
<span data-ttu-id="9d93f-176">要移除之 SRV 記錄的目標主機。</span><span class="sxs-lookup"><span data-stu-id="9d93f-176">The target host of the SRV record to remove.</span></span>
<span data-ttu-id="9d93f-177">不得與區功能變數名稱稱相關。</span><span class="sxs-lookup"><span data-stu-id="9d93f-177">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="9d93f-178">不能有終止點</span><span class="sxs-lookup"><span data-stu-id="9d93f-178">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d93f-179">-值</span><span class="sxs-lookup"><span data-stu-id="9d93f-179">-Value</span></span>
<span data-ttu-id="9d93f-180">要移除之 TXT 記錄的文字值。</span><span class="sxs-lookup"><span data-stu-id="9d93f-180">The text value of the TXT record to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d93f-181">寬度</span><span class="sxs-lookup"><span data-stu-id="9d93f-181">-Weight</span></span>
<span data-ttu-id="9d93f-182">要移除之 SRV 記錄的 [體重] 值。</span><span class="sxs-lookup"><span data-stu-id="9d93f-182">The weight value of the SRV record to remove.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d93f-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d93f-183">CommonParameters</span></span>
<span data-ttu-id="9d93f-184">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d93f-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d93f-185">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9d93f-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d93f-186">輸入</span><span class="sxs-lookup"><span data-stu-id="9d93f-186">INPUTS</span></span>

### <span data-ttu-id="9d93f-187">PSPrivateDnsRecordSet 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="9d93f-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="9d93f-188">輸出</span><span class="sxs-lookup"><span data-stu-id="9d93f-188">OUTPUTS</span></span>

### <span data-ttu-id="9d93f-189">PSPrivateDnsRecordSet 中的 PrivateDns。</span><span class="sxs-lookup"><span data-stu-id="9d93f-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="9d93f-190">筆記</span><span class="sxs-lookup"><span data-stu-id="9d93f-190">NOTES</span></span>

## <span data-ttu-id="9d93f-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d93f-191">RELATED LINKS</span></span>