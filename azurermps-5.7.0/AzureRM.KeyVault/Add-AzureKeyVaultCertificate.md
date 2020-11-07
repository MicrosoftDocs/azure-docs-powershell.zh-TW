---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 89299823-3382-402D-9458-519466748051
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificate.md
ms.openlocfilehash: ed667c726aab59cde592e99d2742c458050cd7db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624305"
---
# <span data-ttu-id="11efb-101">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="11efb-101">Add-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="11efb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11efb-102">SYNOPSIS</span></span>
<span data-ttu-id="11efb-103">將憑證新增到金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="11efb-103">Adds a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11efb-104">句法</span><span class="sxs-lookup"><span data-stu-id="11efb-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [[-CertificatePolicy] <PSKeyVaultCertificatePolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11efb-105">說明</span><span class="sxs-lookup"><span data-stu-id="11efb-105">DESCRIPTION</span></span>
<span data-ttu-id="11efb-106">**AzureKeyVaultCertificate** Cmdlet 會啟動在 Azure 金鑰保存庫中，在金鑰電子倉庫中註冊憑證的程式。</span><span class="sxs-lookup"><span data-stu-id="11efb-106">The **Add-AzureKeyVaultCertificate** cmdlet starts the process of enrolling for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="11efb-107">示例</span><span class="sxs-lookup"><span data-stu-id="11efb-107">EXAMPLES</span></span>

### <span data-ttu-id="11efb-108">範例1：新增憑證</span><span class="sxs-lookup"><span data-stu-id="11efb-108">Example 1: Add a certificate</span></span>
```
PS C:\>$Policy = New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
PS C:\> Add-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -CertificatePolicy $Policy

Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : PS C:\>Get-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : completed
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        :
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="11efb-109">第一個命令使用 New-AzureKeyVaultCertificatePolicy Cmdlet 來建立證書原則，然後將它儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="11efb-109">The first command uses the New-AzureKeyVaultCertificatePolicy cmdlet to create a certificate policy, and then stores it in the $Policy variable.</span></span>

<span data-ttu-id="11efb-110">第二個命令使用 [ **載入 AzureKeyVaultCertificate** ] 來啟動程式來建立證書。</span><span class="sxs-lookup"><span data-stu-id="11efb-110">The second command uses **Add-AzureKeyVaultCertificate** to start the process to create a certificate.</span></span>

<span data-ttu-id="11efb-111">第三個命令使用 Get-AzureKeyVaultCertificateOperation Cmdlet 來輪詢操作，以確認該作業已完成。</span><span class="sxs-lookup"><span data-stu-id="11efb-111">The third command uses the Get-AzureKeyVaultCertificateOperation cmdlet to poll the operation to verify that it's complete.</span></span>

<span data-ttu-id="11efb-112">最後一個命令會使用 Get-AzureKeyVaultCertificate Cmdlet 來取得憑證。</span><span class="sxs-lookup"><span data-stu-id="11efb-112">The final command uses the Get-AzureKeyVaultCertificate cmdlet to get the certificate.</span></span>

## <span data-ttu-id="11efb-113">參數</span><span class="sxs-lookup"><span data-stu-id="11efb-113">PARAMETERS</span></span>

### <span data-ttu-id="11efb-114">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="11efb-114">-CertificatePolicy</span></span>
<span data-ttu-id="11efb-115">指定 **KeyVaultCertificatePolicy** 物件。</span><span class="sxs-lookup"><span data-stu-id="11efb-115">Specifies a **KeyVaultCertificatePolicy** object.</span></span>

```yaml
Type: PSKeyVaultCertificatePolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11efb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11efb-116">-DefaultProfile</span></span>
<span data-ttu-id="11efb-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="11efb-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11efb-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="11efb-118">-Name</span></span>
<span data-ttu-id="11efb-119">指定要新增的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="11efb-119">Specifies the name of the certificate to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11efb-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="11efb-120">-Tag</span></span>
<span data-ttu-id="11efb-121">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="11efb-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="11efb-122">例如：</span><span class="sxs-lookup"><span data-stu-id="11efb-122">For example:</span></span>

<span data-ttu-id="11efb-123">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="11efb-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11efb-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="11efb-124">-VaultName</span></span>
<span data-ttu-id="11efb-125">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="11efb-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="11efb-126">-確認</span><span class="sxs-lookup"><span data-stu-id="11efb-126">-Confirm</span></span>
<span data-ttu-id="11efb-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="11efb-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11efb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11efb-128">-WhatIf</span></span>
<span data-ttu-id="11efb-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11efb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11efb-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11efb-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11efb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11efb-131">CommonParameters</span></span>
<span data-ttu-id="11efb-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11efb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11efb-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11efb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11efb-134">輸入</span><span class="sxs-lookup"><span data-stu-id="11efb-134">INPUTS</span></span>

### <span data-ttu-id="11efb-135">所有</span><span class="sxs-lookup"><span data-stu-id="11efb-135">None</span></span>
<span data-ttu-id="11efb-136">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="11efb-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="11efb-137">輸出</span><span class="sxs-lookup"><span data-stu-id="11efb-137">OUTPUTS</span></span>

### <span data-ttu-id="11efb-138">PSKeyVaultCertificateOperation 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="11efb-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="11efb-139">筆記</span><span class="sxs-lookup"><span data-stu-id="11efb-139">NOTES</span></span>

## <span data-ttu-id="11efb-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="11efb-140">RELATED LINKS</span></span>

[<span data-ttu-id="11efb-141">AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="11efb-141">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="11efb-142">匯入-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="11efb-142">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="11efb-143">移除-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="11efb-143">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)