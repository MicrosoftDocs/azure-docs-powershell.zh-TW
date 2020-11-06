---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 17d99840bffb9063ad61dec00d4b7d5983118399
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456815"
---
# New-AzureVMSqlServerAutoPatchingConfig

## 摘要
在虛擬機器上建立自動修補的設定物件。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**新的-AzureVMSqlServerAutoPatchingConfig** Cmdlet 會在虛擬機器上建立自動修補的設定物件。

## 示例

### 範例1：建立設定物件以設定自動修補
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

這個命令會建立用來修補的設定物件。
該命令會指定一周中的一天，並定義 [維護] 視窗。
這項設定會啟用使用這些值的修補程式。
該命令會將結果儲存在 $AutoBackupConfig 變數中。
您可以為其他 Cmdlet 指定此設定專案，例如 Set-AzureRmVMSqlServerExtension Cmdlet。

## 參數

### -啟用
表示已啟用虛擬機器的自動修補程式。
如果您啟用自動修補，則 Cmdlet 會將 Windows 更新放入互動模式。
如果您停用自動修補，Windows Update 設定就不會變更。

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

### -DayOfWeek
指定一周中要安裝更新的日期。

此參數可接受的值為：

- 日
- 從
- 星期二
- 星期三
- 星期四
- 日
- 星期六
- 生活

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowStartingHour
指定 [維護] 視窗啟動當天的小時。
此時間定義更新開始安裝的時機。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowDuration
指定 [維護] 視窗的持續時間（以分鐘為單位）。
自動修補可避免執行可能會影響虛擬機器在該視窗以外的可用性的動作。
指定30分鐘的倍數。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PatchCategory
指定是否應包含重要更新。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
@ {Text =}

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

### -InformationVariable
@ {Text =}

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### AutoPatchingSettings
這個 Cmdlet 會傳回物件，其中包含自動修補程式的設定。

## 筆記

## 相關連結

[新-AzureVMSqlServerAutoBackupConfig](./New-AzureVMSqlServerAutoBackupConfig.md)

[Set-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)

