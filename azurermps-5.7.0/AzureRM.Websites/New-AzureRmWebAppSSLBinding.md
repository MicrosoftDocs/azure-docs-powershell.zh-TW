---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: d3971c2838b3fed04e1aa38d96e2cd27b2e8276e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452939"
---
# New-AzureRmWebAppSSLBinding

## 摘要
針對 Azure Web App 建立 SSL 憑證系結。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### S1
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S3
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### 喚醒
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**新的-AzureRmWebAppSSLBinding** Cmdlet 會針對 Azure Web APP (SSL) 憑證系結建立安全通訊端層。
這個 Cmdlet 以兩種方式建立 SSL 系結： 

- 您可以將 Web 應用程式系結到現有的憑證。
- 您可以上傳新的憑證，然後將 Web App 系結到這個新的憑證。

無論您使用何種方法，證書和 Web 應用程式必須與相同的 Azure 資源群組相關聯。
如果您在 [資源群組 A] 中有 Web 應用程式，而您想要將該 Web App 系結至資源群組 B 中的憑證，唯一的方法就是將憑證複本上傳至資源群組 A。

如果您上傳新的憑證，請記住 Azure SSL 憑證的下列需求： 

- 憑證必須包含私用金鑰。 
- 憑證必須使用個人資訊交換 (PFX) 格式。 
- 憑證的受領人名稱必須與用來存取 Web 應用程式的網域相符。 
- 憑證必須使用最低的2048位加密。

## 示例

### 範例1：將憑證系結到 Web App
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

這個命令會將現有的 Azure 憑證 (與指紋 E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) 的憑證系結到名為 ContosoWebApp 的 web app。

## 參數

### -CertificateFilePath
指定要上傳之憑證的檔案路徑。

只有證書尚未上傳到 Azure 時，才需要 *CertificateFilePath* 參數。

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
指定憑證的解密密碼。

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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
指定 Web 應用程式的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定指派憑證的資源群組的名稱。

您無法在同一命令中使用 *ResourceGroupName* 參數和 *WebApp* 參數。

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -槽
指定 Web 應用程式部署槽的名稱。
您可以使用 Get-AzureRMWebAppSlot Cmdlet 來取得槽。

部署槽提供一種方法，讓您可以暫存並驗證 web 應用程式，而不需要透過網際網路存取這些 app。
通常您會將所做的變更部署到分段網站、驗證這些變更，然後部署到生產 (可透過網際網路存取的) 網站。

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslState
指定是否已啟用證書。
將 *SSLState* 參數設定為1以啟用憑證，或將 *SSLState* 設定為0以停用憑證。

```yaml
Type: SslState
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -指紋
指定憑證的唯一識別碼。

```yaml
Type: String
Parameter Sets: S2, S4
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
指定 Web 應用程式。
若要取得 Web 應用程式，請使用 Get-AzureRmWebApp Cmdlet。

您無法在與 *ResourceGroupName* 參數和/或 *WebAppName* 相同的命令中使用 *WebApp* 參數。

```yaml
Type: Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
指定要建立新 SSL 系結的 Web App 名稱。

您無法在同一命令中使用 *WebAppName* 參數和 *WebApp* 參數。

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 網站地圖
形參 "WebApp" 接受管線中 "Site" 類型的值

## 輸出

## 筆記

## 相關連結

[AzureRmWebAppSSLBinding](./Get-AzureRmWebAppSSLBinding.md)

[移除-AzureRmWebAppSSLBinding](./Remove-AzureRmWebAppSSLBinding.md)

[AzureRMWebAppSlot](./Get-AzureRMWebAppSlot.md)

[AzureRmWebApp](./Get-AzureRmWebApp.md)


