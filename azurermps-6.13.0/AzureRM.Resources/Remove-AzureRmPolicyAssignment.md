---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: 63b88096200c5db55f9c40a4ba839ffbf25c681d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448916"
---
# Remove-AzureRmPolicyAssignment

## 摘要
移除原則指派。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### NameParameterSet (預設) 
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### IdParameterSet
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmPolicyAssignment** Cmdlet 會移除指定的原則指派。

## 示例

### 範例1：依名稱與作用域移除原則指派
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

第一個命令會使用 Get-AzureRMResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。
該命令會將該物件儲存在 $ResourceGroup 變數中。
第二個命令會移除在資源群組層級指派的名為 PolicyAssignment07 的原則指派。
$ResourceGroup 的 **ResourceId** 屬性會識別資源群組。

### 範例2：依識別碼移除原則指派
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

第一個命令會取得名為 ResourceGroup11 的資源群組，然後將該物件儲存在 $ResourceGroup 變數中。
第二個命令會在資源群組層級取得原則指派，然後將它儲存在 $PolicyAssignment 變數中。
$ResourceGroup 的 **ResourceId** 屬性會識別資源群組。
最後一個命令會移除 $PolicyAssignment 的 **ResourceId** 屬性所識別的原則指派。

## 參數

### -ApiVersion
指定要使用的資源提供者 API 版本。
如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。

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

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -識別碼
指定此 Cmdlet 移除之原則指派的完整限定資源識別碼。

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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
指定資訊變數。

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

### -名稱
指定此 Cmdlet 移除之原則指派的名稱。

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -預先
表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。

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

### -範圍
指定應用原則的範圍。

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[AzureRmPolicyAssignment](./Get-AzureRmPolicyAssignment.md)

[新-AzureRmPolicyAssignment](./New-AzureRmPolicyAssignment.md)

[Set-AzureRmPolicyAssignment](./Set-AzureRmPolicyAssignment.md)

