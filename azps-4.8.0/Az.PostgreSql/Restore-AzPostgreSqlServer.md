---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restore-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
ms.openlocfilehash: c9e4134b6787f78442a18836c15ce190c3e685d8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126285"
---
# Restore-AzPostgreSqlServer

## 摘要
從現有的備份還原伺服器

## 句法

### GeoRestore (預設) 
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### PointInTimeRestore
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## 說明
從現有的備份還原伺服器

## 示例

### 範例1：使用 GeoReplica Restore 還原 PostgreSql 伺服器
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName postgresqltestserverreplica | Restore-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -UseGeoRestore

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

這個 Cmdlet 會使用 GeoReplica 還原來還原 PostgreSql 伺服器。

### 範例2：使用 PointInTime Restore 還原 PostgreSql 伺服器
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Restore-AzPostgreSqlServer -Name PostgreSqlTestServerGEO -ResourceGroupName PostgreSqlTestRG -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name                    Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                    -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestservergeo eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

這些 Cmdlet 會使用 PointInTime 還原來還原 PostgreSql 伺服器。

## 參數

### -AsJob
執行命令做為作業。

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

### -InputObject
要從中還原的源伺服器物件。
若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -位置
資源所在的位置。

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

### -名稱
伺服器的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
以非同步方式執行命令。

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
包含資源之資源群組的名稱，您可以從 Azure 資源管理員 API 或入口網站取得此值。

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

### -RestorePointInTime
資源所在的位置。

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sku
Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。

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

### -SubscriptionId
識別 Azure 訂閱的訂閱 ID。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
以鍵值對形式的特定應用程式中繼資料。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseGeoRestore
使用 Geo 模式進行還原

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsePointInTimeRestore
使用 PointInTime 模式來還原

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### IServer （PostgreSql）。 Api20171201。

## 輸出

### IServer （PostgreSql）。 Api20171201。

## 筆記

別名

複雜的參數屬性

若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。 如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。


INPUTOBJECT <IServer> ：要從中還原的源伺服器物件。
  - `Location <String>`：資源所在的位置。
  - `[Tag <ITrackedResourceTags>]`：以鍵值對形式的特定應用程式中繼資料。
    - `[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。
  - `[AdministratorLogin <String>]`：管理員的伺服器登入名稱。 只能在 (建立伺服器時指定，且在建立) 時需要。
  - `[EarliestRestoreDate <DateTime?>]`： (ISO8601 格式的最早還原點建立時間) 
  - `[FullyQualifiedDomainName <String>]`：伺服器的完整功能變數名稱。
  - `[IdentityType <IdentityType?>]`：身分識別類型。 將此值設定為 ' SystemAssigned」，即可自動為資源建立並指派 Azure Active Directory 主體。
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`：顯示伺服器是否已啟用基礎結構加密的狀態。
  - `[MasterServerId <String>]`：複本伺服器的主伺服器 id。
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`：為伺服器強制執行最低的 Tls 版本。
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`：此伺服器是否允許公用網路存取。 Value 是 optional，但如果傳入，就必須是「Enabled」或「Disabled」
  - `[ReplicaCapacity <Int32?>]`：主伺服器可擁有的複本數目上限。
  - `[ReplicationRole <String>]`：伺服器的複製角色。
  - `[SkuCapacity <Int32?>]`： [擴大/縮小] 容量，代表伺服器的計算單位。
  - `[SkuFamily <String>]`：硬體系列。
  - `[SkuName <String>]`： Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 B_Gen4_1、GP_Gen5_8。
  - `[SkuSize <String>]`：根據需要由資源來轉譯的大小代碼。
  - `[SkuTier <SkuTier?>]`：特定 SKU 的層級，例如基本。
  - `[SslEnforcement <SslEnforcementEnum?>]`[：在連線至伺服器時，啟用 ssl 強制執行。
  - `[StorageProfileBackupRetentionDay <Int32?>]`：伺服器的備份保留天數。
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`：啟用地域冗余，或不用於伺服器備份。
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`：啟用儲存空間自動增長。
  - `[StorageProfileStorageMb <Int32?>]`：伺服器允許的最大儲存空間。
  - `[UserVisibleState <ServerState?>]`：使用者可看見的伺服器狀態。
  - `[Version <ServerVersion?>]`：伺服器版本。

## 相關連結

