---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: c544ce2ea5f02d5c0b3b7aee41e19992a0dc356d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135071"
---
# New-AzMySqlFlexibleServer

## 摘要
建立新的 MySQL 靈活伺服器。

## 句法

```
New-AzMySqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-HighAvailability <Object>] [-Location <String>] [-PublicAccess <String>] [-Sku <String>]
 [-SkuTier <String>] [-StorageInMb <Int32>] [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>]
 [-Version <ServerVersion>] [-Vnet <String>] [-VnetPrefix <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 說明
建立新的 MySQL 靈活伺服器。

## 示例

### 範例1：使用引數建立新的 MySql 彈性伺服器
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellMySqlTest ...
Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group MySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```



### 範例2：使用預設設定建立新的 MySql 彈性伺服器
```powershell
PS C:\> New-AzMySqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group group00000000...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

這個 Cmdlet 會使用預設參數值來建立 MySql 彈性伺服器，並在新的虛擬網路中提供伺服器，並將子網委派給伺服器。
[地點] 的預設值是 [西部美國 2]、Sku 為 Standard_B1ms、Sku 層是 Burstable，而 [儲存空間大小] 是10GiB。


如果您想要尋找伺服器的自動產生的密碼，請使用 ConvertFrom-SecureString 將 ' SecuredPassword」屬性轉換為純文字。

 (例如 $server。SecuredPassword |ConvertFrom-SecureString AsPlainText) 

### 範例3：使用虛擬網路建立新的 MySql 靈活伺服器
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzMySqlFlexibleServer  -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

Resource group PowershellMySqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellMySqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group PowershellMySqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

這個 Cmdlet 會使用使用者提供的 vnet id 或 vnet 名稱來建立 MySql 彈性伺服器。
如果虛擬網路不存在，則 Cmdlet 會建立一個。

### 範例4：使用虛擬網路和子網名稱建立新的 MySql 彈性伺服器
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Vnet mysql-vnet -Subnet mysql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellMySqlTest exists ? : True
Creating new vnet mysql-vnet in resource group PowershellMySqlTest
Creating new subnet mysql-subnet in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

這個 Cmdlet 會使用 vnet 名稱、子網名稱、vnet 首碼及子網首碼來建立 MySql 彈性伺服器。
如果虛擬網路和子網不存在，則 Cmdlet 會建立一個。

### 範例7：建立新的 MySql 靈活的伺服器，以公開存取所有 Ip
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess All

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

這個 Cmdlet 會建立 MySql 彈性伺服器來開啟所有 IP 位址。

### 範例8：使用防火牆建立新的 MySql 靈活伺服器
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

這個 Cmdlet 會將 MySql 靈活的伺服器建立為指定的 IP 位址。

## 參數

### -AdministratorLoginPassword
系統管理員的密碼。
最少8個字元和最大的128個字元。
密碼必須包含下列其中三種類別的字元：英文大寫字母、英文小寫字母、數位和非數位元字元。

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdministratorUserName
伺服器的系統管理員使用者名稱。
一旦設定，就無法變更。

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

### -BackupRetentionDay
伺服器的備份保留天數。
日算在7到35。

```yaml
Type: System.Int32
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

### -HighAvailability
啟用或停用高可用性功能。
預設值為 Disabled。
預設：已停用。

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

Required: False
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

### -PublicAccess
決定公用存取。
輸入要包含在允許的 ip 地址清單中的一或一系列 IP 位址。
IP 位址範圍必須以破折號分隔，且不能包含任何空格。
指定0.0.0.0 允許從 Azure 中部署的任何資源公開存取，以存取您的伺服器。
指定 [沒有 IP 位址] 會將伺服器設定為 [公用存取] 模式，但不會建立防火牆規則。

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
包含資源之資源群組的名稱，您可以從 Azure 資源管理員 API 或入口網站取得此值。

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

### -Sku
Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 Standard_B1ms、Standard_D2ds_v4。

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

### -SkuTier
計算伺服器的層級。
已接受的值： Burstable、GeneralPurpose、記憶體已優化。
預設值： Burstable。

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

### -StorageInMb
伺服器允許的最大儲存空間。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -子網
要建立之現有子網或新名稱的名稱或識別碼。
請注意，該子網會委派給 DBforMySQL/flexibleServers。
委派之後，此子網無法用於任何其他類型的 Azure 資源。

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

### -SubnetPrefix
以 CIDR 格式建立新的 vnet 時要使用的子網 IP 位址前置詞。
預設值為 10.0.0.0/24。

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

### -版本
伺服器版本。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vnet
要建立之現有虛擬網路或新名稱的名稱或 Id。
名稱必須介於2到64個字元之間。
名稱必須以字母或數位開頭、以字母、數位或底線結尾，且只能包含字母、數位、底線、句號或連字號。

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

### -VnetPrefix
以 CIDR 格式建立新的 vnet 時要使用的 IP 位址前置詞。
預設值為 10.0.0.0/16。

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

## 輸出

### IServerAutoGenerated 中的 Api20200701Preview （）。

## 筆記

別名

## 相關連結

