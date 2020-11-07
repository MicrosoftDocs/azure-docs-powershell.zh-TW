---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 2617ca54050f6a37fcc5714fe80e2f2d50e33e40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626344"
---
# <span data-ttu-id="d88eb-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="d88eb-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="d88eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d88eb-102">SYNOPSIS</span></span>
<span data-ttu-id="d88eb-103">建立 SQL Server 自動備份的設定物件。</span><span class="sxs-lookup"><span data-stu-id="d88eb-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d88eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="d88eb-104">SYNTAX</span></span>

### <span data-ttu-id="d88eb-105">StorageUriSqlServerAutoBackup (預設) </span><span class="sxs-lookup"><span data-stu-id="d88eb-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d88eb-106">StorageCoNtextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="d88eb-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d88eb-107">說明</span><span class="sxs-lookup"><span data-stu-id="d88eb-107">DESCRIPTION</span></span>
<span data-ttu-id="d88eb-108">**新的-AzureVMSqlServerAutoBackupConfig** Cmdlet 會建立 SQL Server 自動備份的設定物件。</span><span class="sxs-lookup"><span data-stu-id="d88eb-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="d88eb-109">示例</span><span class="sxs-lookup"><span data-stu-id="d88eb-109">EXAMPLES</span></span>

### <span data-ttu-id="d88eb-110">範例1：使用儲存空間 URI 和帳戶金鑰建立自動備份配置</span><span class="sxs-lookup"><span data-stu-id="d88eb-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="d88eb-111">這個命令會透過指定儲存 URI 和帳戶金鑰來建立自動備份設定物件。</span><span class="sxs-lookup"><span data-stu-id="d88eb-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="d88eb-112">自動備份已啟用，自動備份會保留10天。</span><span class="sxs-lookup"><span data-stu-id="d88eb-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="d88eb-113">該命令會將結果儲存在 $AutoBackupConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="d88eb-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="d88eb-114">您可以為其他 Cmdlet 指定此設定專案，例如 Set-AzureRmVMSqlServerExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d88eb-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="d88eb-115">範例2：使用儲存內容建立自動備份配置</span><span class="sxs-lookup"><span data-stu-id="d88eb-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="d88eb-116">第一個命令會建立儲存內容，然後將它儲存在 $StorageCoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="d88eb-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="d88eb-117">如需詳細資訊，請參閱新 AzureStorageCoNtext。</span><span class="sxs-lookup"><span data-stu-id="d88eb-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="d88eb-118">第二個命令會透過指定 $StorageCoNtext 中的儲存內容來建立自動備份設定物件。</span><span class="sxs-lookup"><span data-stu-id="d88eb-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="d88eb-119">自動備份已啟用，自動備份會保留10天。</span><span class="sxs-lookup"><span data-stu-id="d88eb-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="d88eb-120">範例3：使用含加密及密碼的儲存空間內容建立自動備份配置</span><span class="sxs-lookup"><span data-stu-id="d88eb-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="d88eb-121">這個命令會建立並儲存自動備份設定物件。</span><span class="sxs-lookup"><span data-stu-id="d88eb-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="d88eb-122">此命令會指定在前一個範例中建立的儲存內容。</span><span class="sxs-lookup"><span data-stu-id="d88eb-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="d88eb-123">使用密碼加密的命令。</span><span class="sxs-lookup"><span data-stu-id="d88eb-123">The command enables encryption with password.</span></span>
<span data-ttu-id="d88eb-124">密碼先前已以安全字串形式儲存在 $CertificatePassword 變數中。</span><span class="sxs-lookup"><span data-stu-id="d88eb-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="d88eb-125">若要建立安全的字串，請使用 ConvertTo-SecureString Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d88eb-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="d88eb-126">參數</span><span class="sxs-lookup"><span data-stu-id="d88eb-126">PARAMETERS</span></span>

### <span data-ttu-id="d88eb-127">-啟用</span><span class="sxs-lookup"><span data-stu-id="d88eb-127">-Enable</span></span>
<span data-ttu-id="d88eb-128">表示已啟用 SQL Server 虛擬機器的自動備份。</span><span class="sxs-lookup"><span data-stu-id="d88eb-128">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="d88eb-129">如果您指定此參數，[自動備份] 會為所有目前的資料庫和新資料庫設定備份排程。</span><span class="sxs-lookup"><span data-stu-id="d88eb-129">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="d88eb-130">這會更新您受管理的備份設定，以遵循此排程。</span><span class="sxs-lookup"><span data-stu-id="d88eb-130">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d88eb-131">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="d88eb-131">-RetentionPeriodInDays</span></span>
<span data-ttu-id="d88eb-132">指定保留備份的天數。</span><span class="sxs-lookup"><span data-stu-id="d88eb-132">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d88eb-133">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="d88eb-133">-EnableEncryption</span></span>
<span data-ttu-id="d88eb-134">表示此 Cmdlet 啟用加密。</span><span class="sxs-lookup"><span data-stu-id="d88eb-134">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d88eb-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="d88eb-135">-CertificatePassword</span></span>
<span data-ttu-id="d88eb-136">指定密碼來加密用來執行 SQL Server 加密備份的憑證。</span><span class="sxs-lookup"><span data-stu-id="d88eb-136">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88eb-137">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="d88eb-137">-StorageUri</span></span>
<span data-ttu-id="d88eb-138">指定 blob 儲存空間帳戶 (URI) 的統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="d88eb-138">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d88eb-139">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="d88eb-139">-StorageKey</span></span>
<span data-ttu-id="d88eb-140">指定 [blob 儲存空間] 帳戶的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="d88eb-140">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d88eb-141">-設定檔</span><span class="sxs-lookup"><span data-stu-id="d88eb-141">-Profile</span></span>
<span data-ttu-id="d88eb-142">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d88eb-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d88eb-143">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="d88eb-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Utilities.Common.AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88eb-144">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d88eb-144">-InformationAction</span></span>
<span data-ttu-id="d88eb-145">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="d88eb-145">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88eb-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d88eb-146">-InformationVariable</span></span>
<span data-ttu-id="d88eb-147">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="d88eb-147">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88eb-148">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="d88eb-148">-StorageContext</span></span>
<span data-ttu-id="d88eb-149">指定將用來儲存備份的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="d88eb-149">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="d88eb-150">若要取得 **AzureStorageCoNtext** 物件，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d88eb-150">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="d88eb-151">預設值是與 SQL Server 虛擬機器相關聯的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="d88eb-151">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d88eb-152">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="d88eb-152">-BackupScheduleType</span></span>
<span data-ttu-id="d88eb-153">備份排程類型、手動或自動</span><span class="sxs-lookup"><span data-stu-id="d88eb-153">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="d88eb-154">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="d88eb-154">-BackupSystemDbs</span></span>
<span data-ttu-id="d88eb-155">備份系統資料庫</span><span class="sxs-lookup"><span data-stu-id="d88eb-155">Backup system databases</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d88eb-156">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="d88eb-156">-FullBackupFrequency</span></span>
<span data-ttu-id="d88eb-157">Sql Server 完整備份頻率、每天或每週</span><span class="sxs-lookup"><span data-stu-id="d88eb-157">Sql Server Full Backup frequency, daily or week</span></span>

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

### <span data-ttu-id="d88eb-158">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="d88eb-158">-FullBackupStartHour</span></span>
<span data-ttu-id="d88eb-159">當 Sql Server 完整備份啟動時， (0-23) 一天的小時</span><span class="sxs-lookup"><span data-stu-id="d88eb-159">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d88eb-160">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="d88eb-160">-FullBackupWindowInHours</span></span>
<span data-ttu-id="d88eb-161">Sql Server 完整備份視窗的時間（小時）</span><span class="sxs-lookup"><span data-stu-id="d88eb-161">Sql Server Full Backup window in hours</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d88eb-162">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="d88eb-162">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="d88eb-163">Sql Server 記錄備份頻率，每隔1-60 分鐘一次</span><span class="sxs-lookup"><span data-stu-id="d88eb-163">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d88eb-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d88eb-164">CommonParameters</span></span>
<span data-ttu-id="d88eb-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d88eb-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d88eb-166">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d88eb-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d88eb-167">輸入</span><span class="sxs-lookup"><span data-stu-id="d88eb-167">INPUTS</span></span>

## <span data-ttu-id="d88eb-168">輸出</span><span class="sxs-lookup"><span data-stu-id="d88eb-168">OUTPUTS</span></span>

## <span data-ttu-id="d88eb-169">筆記</span><span class="sxs-lookup"><span data-stu-id="d88eb-169">NOTES</span></span>

## <span data-ttu-id="d88eb-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="d88eb-170">RELATED LINKS</span></span>

[<span data-ttu-id="d88eb-171">新-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="d88eb-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="d88eb-172">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d88eb-172">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)

