---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 734C98C1-0EF7-43E5-AB6F-A1C625FF9CE7
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9713c8b39fa4e2842cdf1cfcbfe962ead86d729
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966981"
---
# Get-AzureVMAccessExtension

## 摘要
取得在虛擬機器上套用的 VMAccess 延伸。

## 句法

```
Get-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**AzureVMAccessExtension** Cmdlet 會取得在虛擬機器上套用的 VMAccess 延伸。

## 示例

### 範例1：取得虛擬機器的 VMAccess 延伸功能
```
PS C:\> Get-AzureVMAccessExtension -VM $VM;
```

這個命令會取得虛擬機器的 VMAccess 延伸。

## 參數

### -InformationAction
指定這個 Cmdlet 回應資訊事件的方式。

此參數可接受的值為：

- 持續
- 理會
- 看
- SilentlyContinue
- 停止
- 封存

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
指定資訊變數。

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
指定持久性虛擬電腦物件。

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[移除-AzureVMAccessExtension](./Remove-AzureVMAccessExtension.md)

[Set-AzureVMAccessExtension](./Set-AzureVMAccessExtension.md)


