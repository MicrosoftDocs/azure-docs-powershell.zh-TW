---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/remove-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
ms.openlocfilehash: 68631f106b795f42fa8ead1a6379ff9dbaa0f4ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909866"
---
# Remove-AzADDomainService

## 簡介
刪除網域服務作業會刪除現有的網域服務。

## 語法

### 刪除 (預設) 
```
Remove-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### DeleteViaIdentity
```
Remove-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 描述
刪除網域服務作業會刪除現有的網域服務。

## 例子

### 範例 1：刪除 ResourceGroupName 和 Name 的 AzADDomain
```powershell
PS C:\> Remove-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName

```

刪除 ResourceGroupName 和 Name 的 AzADDomain

### 範例 2：刪除 InputObject 的 AzADDomain
```powershell
PS C:\> $GetADDomainExample = Get-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName
Remove-AzADDomainService -InputObject $GetADDomainExample

```

刪除 InputObject 的 AzADDomain

## 參數

### -AsJob
以工作執行命令

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

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
網域服務的名稱。

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
非同步執行命令

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

### -PassThru
命令成功時，會返回 True

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

### -ResourceGroupName
使用者訂閱中資源組的名稱。
名稱不區分大小寫。

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。
訂閱識別碼會構成每個服務通話 URI 的一部分。

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -確認
執行 Cmdlet 之前，提示您確認。

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
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.models.IAdDomainServicesIdentity

## 輸出

### System.Boolean

## 筆記

別名

複雜的參數屬性

若要建立下列描述的參數，請建構包含適當屬性的雜湊表。 有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。


INPUTOBJECT： <IAdDomainServicesIdentity> 身分識別參數
  - `[DomainServiceName <String>]`：網域服務的名稱。
  - `[Id <String>]`：資源識別路徑
  - `[ResourceGroupName <String>]`：使用者訂閱中的資源組名。 名稱不區分大小寫。
  - `[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。 訂閱識別碼會構成每個服務通話 URI 的一部分。

## 相關連結

