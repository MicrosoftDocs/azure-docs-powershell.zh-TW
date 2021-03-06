---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: cbe1160c691fe128f5f2950d728501b815294c05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134687"
---
# Restore-AzRecoveryServicesBackupItem

## 摘要

將備份專案的資料和設定還原至指定的復原點。 所需的參數會依備份專案類型而有所不同。
您也可以使用相同的命令來還原 Azure 虛擬機器、在 Azure 虛擬機器和 Azure 檔案共用中執行的資料庫。

## 句法

### AzureVMParameterSet (預設) 
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AzureVMManagedDiskParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureVMRestoreManagedAsUnmanaged
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureVMUnManagedDiskParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureFileShareParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureWorkloadParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase> [-RestoreToSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明

**Restore-AzRecoveryServicesBackupItem** Cmdlet 會將 Azure 備份專案的資料和配置還原至指定的復原點。

**針對 Azure VM 備份**

您可以使用此命令來備份 Azure 虛擬機器和復原磁碟 (受管理和未管理) 。 還原操作不會還原完整的虛擬機器。
如果這是受管理的磁片 VM，則應該在保留復原磁碟的位置指定目標資源群組。 指定目標資源群組時，如果快照存在於備份原則中指定的資源群組中，還原作業就會立即開始，而且磁片是從本機快照建立，並保留在目標資源群組中。 您也可以選擇將它們還原為未受管理的磁片，但這會利用 Azure 復原服務保存庫中的資料，因此會變得更慢。 VM 與部署範本的設定，可用於從已還原的磁片建立 VM，將會下載到指定的儲存空間帳戶。
如果這是未受管理的磁片 VM，則快照會存在於磁片的原始儲存空間帳戶和/或 [恢復服務] 保存庫中。 如果使用者提供使用原始儲存空間帳戶進行還原的選項，則可以提供立即還原。 否則，系統會從 Azure 復原服務電子倉庫取得資料，並在指定的儲存空間帳戶以及 VM 與部署範本的設定中建立磁片。

> [!IMPORTANT]
> 根據預設，Azure VM 備份會備份所有磁片。 您可以在啟用-備份期間，使用 exclusionList 或 InclusionList 參數選擇性地備份相關磁片。 只有有選擇性地備份磁片時，才能使用選擇性復原磁碟的選項。

如需詳細資訊，請參閱不同可能的參數集與參數文字。

> [!NOTE]
> 如果使用-VaultId 參數，則也應該使用-VaultLocation 參數。

**針對 Azure 檔案共用備份**

您可以在共用上還原整個檔案共用或特定/多個檔案/資料夾。 您可以還原至原始位置或移至備用位置。

**針對 Azure 工作負載**

您可以在 Azure Vm 中還原 SQL 存儲


## 示例

### 範例1：從指定的復原點還原已備份之受管理磁片 Azure VM 的磁片

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

第一個命令會取得 [恢復服務] 電子倉庫，並將它儲存在 $vault 變數中。
第二個命令會取得類型為 "V2VM" 的備份專案，並將它儲存在 $BackupItem 變數中。
第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。
第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。
第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。
最後一個命令會將所有磁片還原至 [目標資源] 群組 Target_RG，然後在 [DestRG 資源] 群組的 [儲存帳戶] DestAccount 中提供 VM 配置資訊和部署範本。

### 範例2：從指定的復原點還原已備份之受管理磁片 Azure VM 的指定磁片

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

第一個命令會取得 [恢復服務] 電子倉庫，並將它儲存在 $vault 變數中。
第二個命令會取得類型為 "V2VM" 的備份專案，並將它儲存在 $BackupItem 變數中。
第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。
第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。
第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。
第六個命令會儲存要在 restoreDiskLUN 變數中還原的磁片清單。
最後一個命令會將指定 Lun 的指定磁片還原至 [目標資源] 群組 Target_RG，然後在 [DestRG] 資源群組的 [儲存空間帳戶] DestAccount 中提供 VM 配置資訊和部署範本。

### 範例3：將受管理的 VM 磁片還原為非託管磁片

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

第一個命令會取得 RecoveryServices vault，並將它儲存在 $vault 變數中。
第二個命令會取得備份專案，然後將它儲存在 $BackupItem 變數中。
第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。
第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。
第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。
第六個命令會將磁片還原為非託管磁片。

### 範例4：使用原始儲存空間帳戶將未受管理的 VM 還原為非託管磁片

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -Name "UnManagedVM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

第一個命令會取得 RecoveryServices vault，並將它儲存在 $vault 變數中。
第二個命令會取得備份專案，然後將它儲存在 $BackupItem 變數中。
第三個命令會從前面七天開始取得日期，然後將它儲存在 $StartDate 變數中。
第四個命令會取得目前日期，然後將它儲存在 $EndDate 變數中。
第五個命令會針對 $StartDate 和 $EndDate 篩選的特定備份專案，取得其復原點數的清單。
第六個命令會將磁片還原為非託管磁片至其原始儲存空間帳戶

### 範例5：還原 AzureFileShare 專案的多個檔案

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem   Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

第一個命令會取得 [恢復服務] 電子倉庫，並將它儲存在 $vault 變數中。
第二個命令會取得名為 fileshareitem 的備份專案，然後將它儲存在 $BackupItem 變數中。
第三個命令會針對特定備份專案取得復原點數的清單。
第四個命令會指定要還原哪些檔案，並將其儲存在 $files 變數中。
最後一個命令會將指定的檔案還原至其原始位置。

### 範例6：針對不同的完整復原點，將 Azure VM 中的 SQL 資料庫還原至另一個目標 VM

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $FullRP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithFullConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -RecoveryPoint $FullRP -TargetItem $TargetInstance -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName       Operation        Status            StartTime                 EndTime          JobID
    ------------       ---------        ------            ---------                 -------          -----
    MSSQLSERVER/m...   Restore          InProgress        3/17/2019 10:02:45 AM                      3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

### 範例7：將 Azure VM 中的 SQL 資料庫還原至另一個目標 VM 以取得記錄復原點

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $PointInTime = Get-Date -Date "2019-03-20 01:00:00Z"
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithLogConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -PointInTime $PointInTime -Item $BackupItem -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName     Operation      Status           StartTime                 EndTime           JobID
    ------------     ---------      ------           ---------                 -------           -----
    MSSQLSERVER/m... Restore        InProgress       3/17/2019 10:02:45 AM                       3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

## 參數

### -DefaultProfile

用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -MultipleSourceFilePath
用於多個檔案從檔案共用中還原。 檔案共用中要還原之專案的路徑。

```yaml
Type: System.String[]
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPoint

指定要還原備份專案的復原點。
若要取得 **AzureRmRecoveryServicesBackupRecoveryPoint** 物件，請使用 **AzRecoveryServicesBackupRecoveryPoint** Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResolveConflict

如果還原的專案也存在於目的地中，請使用此選項來指出是否要覆寫。
此參數可接受的值為：

- 原有
- 跳

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConflictOption
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: Overwrite, Skip

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreAsUnmanagedDisks
使用此開關指定要還原為非託管磁片

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMRestoreAsUnmanaged
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreDiskList
指定要復原備份的 VM 的磁片

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreOnlyOSDisk
使用此開關只還原已備份 VM 的 OS 磁片

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFilePath

用於從檔案共用還原特定專案。 要在檔案共用中還原之專案的路徑。

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFileType

用於從檔案共用還原特定專案。 要在檔案共用中還原的專案類型。
此參數可接受的值為：

- 檔案
- 空目錄

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType]
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: File, Directory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName

指定訂閱中目標儲存空間帳戶的名稱。
在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountResourceGroupName

指定包含您訂閱中目標儲存空間帳戶的資源群組的名稱。
在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFileShareName

檔案共用要還原到的檔案共用。

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFolder

要在 TargetFileShareName 中還原檔案共用的資料夾。 如果備份的內容要還原到根資料夾，請將目的檔案夾的值指定為空字串。

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceGroupName

要還原受管理磁片的資源群組。 適用于使用受管理磁片的 VM 備份

```yaml
Type: System.String
Parameter Sets: AzureVMTargetRGParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetStorageAccountName

檔案共用要還原到的儲存空間帳戶。

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseOriginalStorageAccount

如果要將復原點的磁片還原到其原始儲存空間帳戶，請使用此參數。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionSetId 

用來加密已復原磁碟的 DES ID。

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMManagedDiskParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreToSecondaryRegion

使用此開關觸發 [交叉區域] 還原至 [次要區域]。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIaasVM
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId

[恢復服務] 保存庫的 ARM ID。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VaultLocation

[恢復服務] 保存庫的位置。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WLRecoveryConfig

復原配置

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase
Parameter Sets: AzureWorkloadParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -確認

在執行 Cmdlet 之前提示您進行確認。

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

### -WhatIf

顯示在執行 Cmdlet 時會發生什麼情況。 

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### RecoveryPointBase 中的 RecoveryServices，然後再

## 輸出

### JobBase 中的 RecoveryServices，然後再

## 筆記

## 相關連結

[備份-AzRecoveryServicesBackupItem](./Backup-AzRecoveryServicesBackupItem.md)

[AzRecoveryServicesBackupItem](./Get-AzRecoveryServicesBackupItem.md)

[AzRecoveryServicesBackupRecoveryPoint](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
