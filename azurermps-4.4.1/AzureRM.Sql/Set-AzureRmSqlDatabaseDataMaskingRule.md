---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 1a26cc83bfd42ba63f2ae914ea6c288b862ccaf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446612"
---
# Set-AzureRmSqlDatabaseDataMaskingRule

## 摘要
為資料庫設定資料遮罩規則的屬性。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
**AzureRmSqlDatabaseDataMaskingRule** Cmdlet 會為 Azure SQL 資料庫設定資料遮罩規則。
若要使用 Cmdlet，請提供 *ResourceGroupName* 、 *ServerName* 、 *DatabaseName* 及 *RuleId* 參數來識別規則。
您可以提供 *SchemaName* 、 *TableName* 和 *ColumnName* 的任何參數，以將規則重新置放。
指定 *MaskingFunction* 參數來修改資料的遮罩方式。

如果您指定 *MaskingFunction* 的數位或文字值，您可以為數位遮罩指定 *NumberFrom* 和 *NumberTo* 參數，或針對文字遮罩指定 *PrefixSize* 、 *ReplacementString* 和 *SuffixSize* 參數。
如果命令成功，且您指定 *PassThru* 參數，則 Cmdlet 會傳回描述資料遮罩規則屬性與規則識別碼的物件。
規則識別碼包括但不限於、 **ResourceGroupName** 、 **ServerName** 、 **DatabaseName** 及 **RuleId** 。

Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。

## 示例

### 範例1：變更資料庫中資料遮罩規則的範圍
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

這個命令會修改 ID 為 Rule17 的資料遮罩規則。
該規則會在伺服器 Server01 上名為 Database01 的資料庫中運作。
這個命令會變更作為遮罩值產生亂數字的間隔界限。
新的範圍是23到42。

## 參數

### -ColumnName
指定遮罩規則所針對的欄名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseName
指定資料庫的名稱。

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

### -MaskingFunction
指定規則所使用的遮罩函數。
此參數可接受的值為：

- 設置
- NoMasking
- 字體
- 電話
- SocialSecurityNumber
- CreditCardNumber
- 電子郵件

預設值為 [預設值]。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberFrom
指定從中選取隨機值的間隔下限數位。
只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。
預設值為0。

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberTo
指定從哪個間隔開始選取隨機值的上限。
只有在您為 *MaskingFunction* 參數指定 Number 值時，才能指定此參數。
預設值為0。

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
傳回代表您正在使用之專案的物件。
根據預設，這個 Cmdlet 不會產生任何輸出。

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

### -PrefixSize
指定未遮罩之文字開頭的字元數。
只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。
預設值為0。

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReplacementString
指定未遮罩之文字結尾的字元數。
只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。
預設值為0。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定指派給資料庫之資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SchemaName
指定架構的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
指定託管資料庫的伺服器名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SuffixSize
指定未遮罩之文字結尾的字元數。
只有在您指定 *MaskingFunction* 參數的 Text 值時，才能指定此參數。
預設值為0。

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TableName
指定包含遮罩資料行的資料庫資料表名稱。

```yaml
Type: System.String
Parameter Sets: (All)
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

###  
所有

## 輸出

### DatabaseDataMaskingRuleModel 中的 [.Sql.]

## 筆記

## 相關連結

[AzureRmSqlDatabaseDataMaskingRule](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[新-AzureRmSqlDatabaseDataMaskingRule](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[移除-AzureRmSqlDatabaseDataMaskingRule](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[SQL 資料庫檔](https://docs.microsoft.com/azure/sql-database/)


