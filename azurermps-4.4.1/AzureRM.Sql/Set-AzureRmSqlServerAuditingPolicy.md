---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4FCC7D8B-A46E-4E5B-8BE2-F62B3D3E715D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: daec1290dfa70166e532265da98bdb507b1318e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450768"
---
# Set-AzureRmSqlServerAuditingPolicy

## 摘要
變更 SQL 資料庫伺服器的審核原則。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmSqlServerAuditingPolicy [-AuditType <AuditType>] [-AuditActionGroup <AuditActionGroups[]>]
 [-PassThru] [-EventType <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-TableIdentifier <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmSqlServerAuditingPolicy** Cmdlet 會變更 Azure SQL 資料庫伺服器的審核原則。
指定 *ResourceGroupName* 和 *ServerName* 參數來識別伺服器、 *StorageAccountName* 參數以指定審核記錄的儲存空間帳戶，以及用來定義要使用之儲存空間的 *StorageKeyType* 參數。

您也可以設定 *RetentionInDays* 和 *TableIdentifier* 參數的值來定義 [審核記錄] 資料表的保留，以定義審核記錄資料表名稱的期間和種子。
指定事件 *類型參數，* 以定義要審核的事件種類。
在您執行此 Cmdlet 之後，就會啟用使用此伺服器原則的資料庫審核。
如果 Cmdlet 成功且您指定 *PassThru* 參數，則 Cmdlet 會傳回描述目前審核原則和伺服器識別碼的物件。
伺服器識別碼包括 **ResourceGroupName** 和 **ServerName** 。

## 示例

### 範例1：設定 Azure SQL server 的審核原則使用資料表審核
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Table -StorageAccountName "Storage22"
```

這個命令會將名為 Server01 的伺服器的審核原則設定為使用名為 Storage22 的儲存空間帳戶。

### 範例2：設定 Azure SQL server 現有審核原則的儲存空間帳戶金鑰
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountKey Secondary
```

這個命令會將名為 Server01 的伺服器的審核原則設定為使用次要金鑰。
此命令不會修改儲存空間帳戶名稱。

### 範例3：將 Azure SQL server 的審核原則設定為使用特定的事件種類
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventType Login_Failure
```

### 範例4：將資料庫的審核原則設定為使用 Blob 審核
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -RetentionInDays 8
```

這個命令會將名為 Server01 的伺服器的審核原則設定為使用 Login_Failure 事件種類。
這個命令不會修改任何其他設定。

## 參數

### -AuditActionGroup
指定一個或多個審核動作群組。 這個參數只適用于 Blob 審核。

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases: 
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuditType
指定審核類型。 審核記錄可以寫入資料表儲存空間或 Blob 儲存空間。 Blob 審核可提供較高的效能並支持對象層級的審核。

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType
Parameter Sets: (All)
Aliases: 
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -事件
指定要審核的事件種類。
這個參數只適用于資料表審核。

您可以指定數種事件種類。
您可以指定 All 來審核所有事件種類，或指定 None，以指定不會審核任何事件。
如果您同時指定 All 或 None，命令就會失敗。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

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

### -ResourceGroupName
指定包含資料庫之資源群組的名稱。

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

### -RetentionInDays
指定 [審核記錄] 資料表的保留天數。
零的值 (0) 表示該表格未保留。
這是預設值。
如果您指定的值大於零，您也必須指定 *TableIdentifer* 參數的值。

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

### -ServerName
指定包含資料庫的伺服器名稱。

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

### -StorageAccountName
指定要審核資料庫的儲存空間帳戶名稱。
不允許通配字元。
如果您沒有指定此參數，則此 Cmdlet 會使用先前在資料庫的審核原則中定義的儲存空間帳戶。
如果這是已定義資料庫審核原則的第一次，且您不指定此參數，命令就會失敗。

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

### -StorageKeyType
指定要使用的儲存空間便捷鍵。
此參數可接受的值為：

- 首選
- 備用

預設值為 [主要]。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TableIdentifier
指定 [審核記錄] 資料表的名稱。
如果您為 *RetentionInDays* 參數指定的值大於零，請指定此值。

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

## 輸出

### ServerAuditingPolicyModel 中的 [.Sql.]

## 筆記

## 相關連結

[AzureRmSqlServerAuditingPolicy](./Get-AzureRmSqlServerAuditingPolicy.md)

[使用-AzureRmSqlServerAuditingPolicy](./Use-AzureRmSqlServerAuditingPolicy.md)

[SQL 資料庫檔](https://docs.microsoft.com/azure/sql-database/)


