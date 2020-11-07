---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: a6635afc19f95f32d7c50ff7a92ba5868a5945e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787398"
---
# <span data-ttu-id="f6893-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f6893-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f6893-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6893-102">SYNOPSIS</span></span>
<span data-ttu-id="f6893-103">在金鑰保存庫中取得憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="f6893-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="f6893-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6893-104">SYNTAX</span></span>

### <span data-ttu-id="f6893-105">VaultAndCertName (預設) </span><span class="sxs-lookup"><span data-stu-id="f6893-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6893-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f6893-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6893-107">說明</span><span class="sxs-lookup"><span data-stu-id="f6893-107">DESCRIPTION</span></span>
<span data-ttu-id="f6893-108">**AzKeyVaultCertificatePolicy** Cmdlet 會取得 Azure 金鑰保存庫中金鑰保存庫中憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="f6893-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="f6893-109">示例</span><span class="sxs-lookup"><span data-stu-id="f6893-109">EXAMPLES</span></span>

### <span data-ttu-id="f6893-110">範例1：取得證書原則</span><span class="sxs-lookup"><span data-stu-id="f6893-110">Example 1: Get a certificate policy</span></span>
```powershell
PS C:\ >Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"

SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Exportable                      : True
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        : 
Ekus                            : {1.3.6.1.5.5.7.3.1, 1.3.6.1.5.5.7.3.2}
ValidityInMonths                : 6
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="f6893-111">這個命令會在 ContosoKV01 金鑰保存庫中取得 TestCert01 憑證的憑證原則。</span><span class="sxs-lookup"><span data-stu-id="f6893-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="f6893-112">參數</span><span class="sxs-lookup"><span data-stu-id="f6893-112">PARAMETERS</span></span>

### <span data-ttu-id="f6893-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6893-113">-DefaultProfile</span></span>
<span data-ttu-id="f6893-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f6893-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6893-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6893-115">-InputObject</span></span>
<span data-ttu-id="f6893-116">[憑證] 物件。</span><span class="sxs-lookup"><span data-stu-id="f6893-116">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6893-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6893-117">-Name</span></span>
<span data-ttu-id="f6893-118">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6893-118">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6893-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f6893-119">-VaultName</span></span>
<span data-ttu-id="f6893-120">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6893-120">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6893-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6893-121">CommonParameters</span></span>
<span data-ttu-id="f6893-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6893-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6893-123">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f6893-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6893-124">輸入</span><span class="sxs-lookup"><span data-stu-id="f6893-124">INPUTS</span></span>

### <span data-ttu-id="f6893-125">PSKeyVaultCertificateIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="f6893-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="f6893-126">輸出</span><span class="sxs-lookup"><span data-stu-id="f6893-126">OUTPUTS</span></span>

### <span data-ttu-id="f6893-127">PSKeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="f6893-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f6893-128">筆記</span><span class="sxs-lookup"><span data-stu-id="f6893-128">NOTES</span></span>

## <span data-ttu-id="f6893-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6893-129">RELATED LINKS</span></span>

[<span data-ttu-id="f6893-130">新-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f6893-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="f6893-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f6893-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)
