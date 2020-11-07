---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b6e8139f201a69684d4236a5e84e89f6607c5c
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793435"
---
# <span data-ttu-id="8dc27-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="8dc27-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="8dc27-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8dc27-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc27-103">在指定的位置設定備份配置。</span><span class="sxs-lookup"><span data-stu-id="8dc27-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="8dc27-104">句法</span><span class="sxs-lookup"><span data-stu-id="8dc27-104">SYNTAX</span></span>

### <span data-ttu-id="8dc27-105">更新 (預設) </span><span class="sxs-lookup"><span data-stu-id="8dc27-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionKey <SecureString>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc27-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8dc27-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8dc27-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dc27-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8dc27-108">說明</span><span class="sxs-lookup"><span data-stu-id="8dc27-108">DESCRIPTION</span></span>
<span data-ttu-id="8dc27-109">在指定的位置設定備份配置。</span><span class="sxs-lookup"><span data-stu-id="8dc27-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="8dc27-110">示例</span><span class="sxs-lookup"><span data-stu-id="8dc27-110">EXAMPLES</span></span>

### <span data-ttu-id="8dc27-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8dc27-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionKey $encryptionKey
```

<span data-ttu-id="8dc27-112">設定 Azure 堆疊備份配置。</span><span class="sxs-lookup"><span data-stu-id="8dc27-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="8dc27-113">參數</span><span class="sxs-lookup"><span data-stu-id="8dc27-113">PARAMETERS</span></span>

### <span data-ttu-id="8dc27-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8dc27-114">-AsJob</span></span>
<span data-ttu-id="8dc27-115">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="8dc27-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc27-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="8dc27-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="8dc27-117">排程程式執行備份之頻率的間隔（以小時為單位）。</span><span class="sxs-lookup"><span data-stu-id="8dc27-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc27-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="8dc27-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="8dc27-119">在儲存位置備份的保留期間（天）。</span><span class="sxs-lookup"><span data-stu-id="8dc27-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc27-120">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="8dc27-120">-EncryptionKey</span></span>
<span data-ttu-id="8dc27-121">用來加密備份的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="8dc27-121">Encryption key used to encrypt backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc27-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dc27-122">-InputObject</span></span>
<span data-ttu-id="8dc27-123">AzsBackupConfiguration 所傳回的備份位置設定。</span><span class="sxs-lookup"><span data-stu-id="8dc27-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc27-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="8dc27-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="8dc27-125">是否應該啟用備份排程器。</span><span class="sxs-lookup"><span data-stu-id="8dc27-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc27-126">-位置</span><span class="sxs-lookup"><span data-stu-id="8dc27-126">-Location</span></span>
<span data-ttu-id="8dc27-127">要設定的位置。</span><span class="sxs-lookup"><span data-stu-id="8dc27-127">Location to configure.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc27-128">-Password</span><span class="sxs-lookup"><span data-stu-id="8dc27-128">-Password</span></span>
<span data-ttu-id="8dc27-129">存取備份位置所需的密碼。</span><span class="sxs-lookup"><span data-stu-id="8dc27-129">Password required to access backup location.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc27-130">-Path</span><span class="sxs-lookup"><span data-stu-id="8dc27-130">-Path</span></span>
<span data-ttu-id="8dc27-131">儲存備份的位置。</span><span class="sxs-lookup"><span data-stu-id="8dc27-131">Location where backups will be stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc27-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dc27-132">-ResourceGroupName</span></span>
<span data-ttu-id="8dc27-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8dc27-133">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc27-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dc27-134">-ResourceId</span></span>
<span data-ttu-id="8dc27-135">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8dc27-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc27-136">-Username</span><span class="sxs-lookup"><span data-stu-id="8dc27-136">-Username</span></span>
<span data-ttu-id="8dc27-137">存取備份位置所需的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="8dc27-137">Username required to access backup location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc27-138">-確認</span><span class="sxs-lookup"><span data-stu-id="8dc27-138">-Confirm</span></span>
<span data-ttu-id="8dc27-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8dc27-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc27-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc27-140">-WhatIf</span></span>
<span data-ttu-id="8dc27-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8dc27-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dc27-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8dc27-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc27-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc27-143">CommonParameters</span></span>
<span data-ttu-id="8dc27-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8dc27-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc27-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8dc27-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc27-146">輸入</span><span class="sxs-lookup"><span data-stu-id="8dc27-146">INPUTS</span></span>

## <span data-ttu-id="8dc27-147">輸出</span><span class="sxs-lookup"><span data-stu-id="8dc27-147">OUTPUTS</span></span>

### <span data-ttu-id="8dc27-148">BackupLocation 中的 [AzureStack]</span><span class="sxs-lookup"><span data-stu-id="8dc27-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="8dc27-149">筆記</span><span class="sxs-lookup"><span data-stu-id="8dc27-149">NOTES</span></span>

## <span data-ttu-id="8dc27-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="8dc27-150">RELATED LINKS</span></span>
