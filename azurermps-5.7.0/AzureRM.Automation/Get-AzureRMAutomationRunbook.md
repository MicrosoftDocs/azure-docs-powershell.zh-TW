---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
ms.openlocfilehash: d9ffd6ae2f7695a02f8c29fbe745202642039af6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456259"
---
# Get-AzureRmAutomationRunbook

## 摘要
取得 runbook。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByAll (預設) 
```
Get-AzureRmAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmAutomationRunbook** Cmdlet 會取得 Azure 自動化 runbook。
若要取得特定的 runbook，請指定其名稱。

## 示例

### 範例1：取得所有 runbook
```
PS C:\>Get-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

這個命令會取得 Azure 自動化帳戶（名為 Contoso17）中的所有 runbook。

## 參數

### -AutomationAccountName
指定此 Cmdlet 在其中取得 runbook 的自動化帳戶名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 取得的 runbook 名稱。

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定此 Cmdlet 取得 runbook 之資源群組的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### [-Azure. 命令介面]。

## 筆記

## 相關連結

[Export-AzureRmAutomationRunbook](./Export-AzureRMAutomationRunbook.md)

[匯入-AzureRmAutomationRunbook](./Import-AzureRMAutomationRunbook.md)

[新-AzureRmAutomationRunbook](./New-AzureRMAutomationRunbook.md)

[新-AzureRmAutomationRunbook](./New-AzureRMAutomationRunbook.md)

[發佈-AzureRmAutomationRunbook](./Publish-AzureRMAutomationRunbook.md)

[移除-AzureRmAutomationRunbook](./Remove-AzureRMAutomationRunbook.md)

[Set-AzureRmAutomationRunbook](./Set-AzureRMAutomationRunbook.md)

[開始-AzureRmAutomationRunbook](./Start-AzureRMAutomationRunbook.md)


