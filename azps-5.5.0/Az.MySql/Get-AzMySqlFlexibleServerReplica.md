---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
ms.openlocfilehash: 77b1dae0db73a9a90a2100edef893edabfe87d0b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135079"
---
# Get-AzMySqlFlexibleServerReplica

## 摘要
列出指定伺服器的所有複本。

## 句法

```
Get-AzMySqlFlexibleServerReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## 說明
列出指定伺服器的所有複本。

## 示例

### 範例1：依資源群組和伺服器名稱取得 MySql 伺服器複本
```powershell
PS C:\> Get-AzMySqlFlexibleServerReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

這個 Cmdlet 透過資源群組和伺服器名稱來取得 MySql 伺服器複製。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -ResourceGroupName
資源群組的名稱。
名稱不區分大小寫。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
伺服器的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
目標訂閱的 ID。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

## 輸出

### IServerAutoGenerated 中的 Api20200701Preview （）。

## 筆記

別名

## 相關連結

