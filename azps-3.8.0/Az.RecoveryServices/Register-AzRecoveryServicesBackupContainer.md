---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: a6c47561b8fdb9e748940c917d85548d25be1ccf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958624"
---
# Register-AzRecoveryServicesBackupContainer

## 摘要
這個命令可讓 Azure Backup 將資源轉換成備份容器，然後再將登錄到指定的 [恢復服務] 保存庫。 然後，Azure 備份服務就可以在此容器中發現指定工作負荷類型的工作負荷，以備日後受到保護。

## 句法

### 註冊 (預設) 
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 于
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
這個 Cmdlet 會使用特定 workloadType 註冊 AzureWorkloads 的 Azure VM。

## 示例

### 範例1
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

這個 Cmdlet 會針對工作負荷 MSSQL 註冊 azure VM。

## 參數

### -BackupManagementType
Azure 備份容器的備份管理類型

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -容器
專案所在的容器

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: ReRegister
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -Force
強制註冊容器 (會防止確認對話方塊) 。 這個參數是選用的。

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

### -ResourceId
需要檢查其代表代表的 Azure 資源（如果訂閱中的某些 RecoveryServices 保存庫已受到保護）的 ID。

```yaml
Type: System.String
Parameter Sets: Register
Aliases:

Required: True
Position: 0
Default value: None
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

### -WorkloadType
資源的工作量類型 (例如： Add-azurevm、WindowsServer、AzureFiles、MSSQL) 。

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
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
未執行 Cmdlet。

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

## 輸出

### ContainerBase 中的 RecoveryServices，然後再

## 筆記

## 相關連結
