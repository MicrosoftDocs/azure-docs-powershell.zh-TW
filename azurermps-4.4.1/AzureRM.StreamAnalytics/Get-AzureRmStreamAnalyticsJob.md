---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 7b1130d222e36d53fbef1dcbb60f6d74615c5b11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449474"
---
# Get-AzureRmStreamAnalyticsJob

## 摘要
取得串流分析作業資訊。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 在指定資源群組中的串流分析物件
```
Get-AzureRmStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 針對指定訂閱中的串流分析物件
```
Get-AzureRmStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmStreamAnalyticsJob** Cmdlet 會列出 Azure 訂閱或指定資源群組中定義的所有串流分析作業，或取得資源群組中特定作業的工作資訊。

## 示例

### 範例1：取得訂閱中所有作業的相關資訊
```
PS C:\>Get-AzureRmStreamAnalyticsJob
```

這個命令會傳回有關 Azure 訂閱中所有串流分析作業的資訊。

### 範例2：取得資源群組中所有工作的相關資訊
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

這個命令會傳回有關 [資源群組 StreamAnalytics] 中所有串流分析作業的資訊-預設值-西部-美國。

### 範例3：取得資源群組中特定作業的相關資訊
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

這個命令會傳回有關 [資源] 群組中 [資料流程分析作業 StreamingJob] 的資訊 StreamAnalytics-預設值-西部-美國。

## 參數

### -名稱
指定要檢索之 Azure 串流分析作業的名稱。

```yaml
Type: System.String
Parameter Sets: For stream analytics objects in the given resource group
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NoExpand
指示 Cmdlet 將會檢索 Azure 資料流程分析作業，但不會傳回其輸入、輸出及轉換的資訊。

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

### -ResourceGroupName
指定 Azure 資料流程分析作業所屬之資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: For stream analytics objects in the given resource group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### [System.object]. 清單 ' 1 [StreamAnalytics. PSJob，StreamAnalytics]]]]]]]]]]]]

## 筆記

## 相關連結

[新-AzureRmStreamAnalyticsJob](./New-AzureRmStreamAnalyticsJob.md)

[移除-AzureRmStreamAnalyticsJob](./Remove-AzureRmStreamAnalyticsJob.md)

[開始-AzureRmStreamAnalyticsJob](./Start-AzureRmStreamAnalyticsJob.md)

[停止 AzureRmStreamAnalyticsJob](./Stop-AzureRmStreamAnalyticsJob.md)


