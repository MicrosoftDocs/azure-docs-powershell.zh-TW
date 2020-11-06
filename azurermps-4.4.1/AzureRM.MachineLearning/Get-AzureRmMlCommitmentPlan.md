---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 9f9789d288773b16b2003e23b00674c12ca08738
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451660"
---
# Get-AzureRmMlCommitmentPlan

## 摘要
檢索一或多個承諾方案的摘要資訊。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
檢索承諾方案資訊。
根據傳遞的 paramenters，Cmdlet 會傳回特定的承約方案，以及目前訂閱中指定資源群組的一組承諾方案集合，或目前訂閱中的承諾方案集合。

## 示例

### --------------------------範例1：取得特定的承約方案--------------------------
@ {段落 = PS C： \\ \> }





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### --------------------------範例2：取得目前訂閱中的所有承諾方案資源--------------------------
@ {段落 = PS C： \\ \> }





```
Get-AzureRmMlCommitmentPlan
```

### --------------------------範例3：取得目前訂閱和指定資源群組中的所有承諾方案--------------------------
@ {段落 = PS C： \\ \> }





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## 參數

### -名稱
承諾方案的名稱。

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

### -ResourceGroupName
Azure ML 承諾方案之資源群組的名稱。

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
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### MachineLearning CommitmentPlans. CommitmentPlan （）
CommitmentPlan []. MachineLearning [CommitmentPlans]

## 筆記
關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml

## 相關連結
