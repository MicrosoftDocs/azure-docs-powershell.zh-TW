---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798034"
---
# New-AzStorageContext

## 摘要
建立 Azure 儲存區內容。

## 句法

### OAuthAccount (預設) 
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKey
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### OAuthAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### ConnectionString
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## 說明
**新的-AzStorageCoNtext** Cmdlet 會建立 Azure 儲存區內容。
儲存內容的預設驗證是 OAuth (Azure AD) ，如果只輸入儲存空間帳戶名稱。
請參閱中的儲存服務驗證詳細資料 https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services 。

## 示例

### 範例1：透過指定儲存空間帳戶名稱和金鑰來建立內容
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

這個命令會為使用指定金鑰的帳戶（名為 ContosoGeneral）建立內容。

### 範例2：透過指定連接字串來建立內容
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

這個命令會根據帳戶 ContosoGeneral 的指定連接字串來建立內容。

### 範例3：建立匿名儲存空間帳戶的內容
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

這個命令會建立名為 ContosoGeneral 的帳戶匿名使用的內容。
該命令會將 HTTP 指定為連線通訊協定。

### 範例4：使用本機開發儲存空間帳戶建立內容
```
PS C:\>New-AzStorageContext -Local
```

這個命令會使用本機開發儲存空間帳戶來建立內容。
命令會指定 *本機* 參數。

### 範例5：取得本機開發人員儲存空間帳戶的容器
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

這個命令會使用本機開發儲存空間帳戶建立內容，然後使用管線運算子將新的內容傳送到 **AzStorageContainer** Cmdlet。
此命令會取得本機開發人員儲存空間帳戶的 Azure 儲存體容器。

### 範例6：取得多個容器
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

第一個命令會使用本機開發儲存空間帳戶建立內容，然後將該內容儲存在 $CoNtext 01 變數中。
第二個命令會針對使用指定金鑰的帳戶（名為 ContosoGeneral）建立內容，然後將該內容儲存在 $CoNtext 02 變數中。
最後一個命令會使用 **AzStorageContainer** ，透過 $CoNtext 01 和 $CoNtext 02 中的內容來取得所儲存之上下文的容器。

### 範例7：使用端點建立內容
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

這個命令會建立具有指定儲存端點的 Azure 儲存區內容。
此命令會為使用指定金鑰的帳戶建立名為 ContosoGeneral 的內容。

### 範例8：建立具有指定環境的內容
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

這個命令會建立具有指定 Azure 環境的 Azure 儲存區內容。
此命令會為使用指定金鑰的帳戶建立名為 ContosoGeneral 的內容。

### 範例9：使用 SAS 權杖建立內容
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

第一個命令會使用名為 ContosoMain 之容器的 **新 AzStorageContainerSASToken** Cmdlet 來產生 SAS 權杖，然後將該權杖儲存在 $SasToken 變數中。
該權杖用於讀取、新增、更新和刪除許可權。
第二個命令會建立名為 ContosoGeneral 的帳戶的內容，該帳戶會使用儲存在 $SasToken 中的 SAS 權杖，然後將該內容儲存在 $CoNtext 變數中。
最終命令會使用 $CoNtext 中儲存的內容，列出與名為 ContosoMain 的容器相關的所有 blob。

### 範例10：使用 OAuth 驗證建立內容
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

這個命令會使用 OAuth (Azure AD) 驗證來建立內容。

## 參數

### -匿名
表示此 Cmdlet 會為匿名登入建立 Azure 儲存區內容。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### ConnectionString
指定 Azure 儲存區內容的連線字串。

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -端點
指定 Azure 儲存區內容的端點。

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -環境
指定 Azure 環境。
此參數可接受的值為： AzureCloud 和 AzureChinaCloud。
如需詳細資訊，請輸入 `Get-Help Get-AzEnvironment` 。

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -本機
指示這個 Cmdlet 使用本機開發儲存空間帳戶來建立內容。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -通訊協定
 (HTTPs/HTTP) 傳輸通訊協定。

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasToken
指定內容的共用存取簽名 (SAS) 標記。

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
指定 Azure 儲存空間帳戶金鑰。
這個 Cmdlet 會建立此參數指定之金鑰的內容。

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
指定 Azure 儲存空間帳戶名稱。
這個 Cmdlet 會建立此參數指定之帳戶的內容。

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseConnectedAccount
表示此 Cmdlet 會使用 OAuth (Azure AD) 驗證來建立 Azure 儲存區內容。
預設情況下，如果未指定其他驗證，則 Cmdlet 會使用 OAuth 驗證。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### AzureStorageCoNtext 中的 WindowsAzure

## 筆記

## 相關連結

[AzStorageBlob](./Get-AzStorageBlob.md)

[新-AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)


