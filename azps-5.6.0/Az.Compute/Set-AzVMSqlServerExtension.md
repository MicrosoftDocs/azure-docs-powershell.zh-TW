---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 9aa895245f491e7b7ee077d083f052cd7e4e46e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910254"
---
# Set-AzVMSqlServerExtension

## 簡介
設定虛擬機器上的 Azure SQL Server 擴充功能。

## 語法

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Set-AzCMSqlServerExtension** Cmdlet 會設定虛擬機器上的 AzureSQL Server 擴充功能。

## 例子

### 範例 1：在虛擬機器上設定自動修補設定
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

第一個命令會使用 **New-AzCMSqlServerAutoPatchingConfig** Cmdlet 來建立組組物件。
該命令將組$AutoPatchingConfig變數。
第二個命令會使用 Get-AzVM Cmdlet，在名為 Service02 的服務上，獲得名為 VirtualMachine11 的虛擬機器。
該命令會使用管線運算子，將該物件傳遞至目前的 Cmdlet。
目前的 Cmdlet 會針對虛擬機器$AutoPatchingConfig自動修補設定。
該命令會將虛擬機器傳遞至 Update-AzVM Cmdlet。

### 範例 2：在虛擬機器上設定自動備份設定
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

第一個命令會使用 **New-AzCMSqlServerAutoBackupConfig Cmdlet 建立** 組組物件。
該命令將組$AutoBackupConfig變數。
第二個命令會獲得名為 Service02 的服務上名為 VirtualMachine11 的虛擬機器，然後將它傳遞至目前的 Cmdlet。
目前的 Cmdlet 會設定$AutoBackupConfig的自動備份設定。
該命令會將虛擬機器傳遞至 Update-AzVM Cmdlet。

### 範例 3：停用虛擬機器上的 SQL Server 擴充功能
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

此命令在 Service03 上會獲得一個名為 VirtualMachine08 的虛擬機器，然後將它傳遞至目前的 Cmdlet。
該命令會停用該虛擬機器上的 SQL Server 虛擬機器擴充功能。

### 範例 4：卸載特定虛擬機器上的 SQL Server 擴充功能
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

此命令在 Service03 上會獲得一個名為 VirtualMachine08 的虛擬機器，然後將它傳遞至目前的 Cmdlet。
該命令會卸載該虛擬機器上的 SQL Server 虛擬機器擴充功能。

## 參數

### -自動BackupSettings
指定 SQL Server 自動備份設定。
若要建立 **AutoBackupSettings 物件** ，請使用 New-AzVMSqlServerAutoBackupConfig Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -自動修補設定
指定自動 SQL Server 修補設定。
若要建立 **AutoPatchingSettings 物件** ，請使用 New-AzVMSqlServerAutoPatchingConfig Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

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

### -KeyVaultCredentialSettings
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -位置
指定虛擬機器的位置。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定擴充功能 SQL Server 的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定虛擬機器的資源組名。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -版本
指定 SQL Server 擴充功能的版本。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
指定此 Cmdlet 設定 SQL Server 副檔名的虛擬機器名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

### Microsoft.Azure.Commands.Compute.AutoPatchingSettings

### Microsoft.Azure.Commands.Compute.AutoBackupSettings

### Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings

## 輸出

### Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse

## 筆記

## 相關連結

[Get-AzMS](./Get-AzVM.md)

[Get-AzMSqlServerExtension](./Get-AzVMSqlServerExtension.md)

[New-AzMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[New-AzMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Remove-AzMSqlServerExtension](./Remove-AzVMSqlServerExtension.md)

[Update-AzMS](./Update-AzVM.md)


