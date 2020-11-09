---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 963a7005e95941a644b35a57f80b558f02e2d6a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284687"
---
# <span data-ttu-id="42ea8-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="42ea8-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="42ea8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="42ea8-103">在金鑰保存庫中建立或更新憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="42ea8-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="42ea8-104">句法</span><span class="sxs-lookup"><span data-stu-id="42ea8-104">SYNTAX</span></span>

### <span data-ttu-id="42ea8-105">ExpandedRenewPercentage (預設) </span><span class="sxs-lookup"><span data-stu-id="42ea8-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42ea8-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="42ea8-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42ea8-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="42ea8-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42ea8-108">說明</span><span class="sxs-lookup"><span data-stu-id="42ea8-108">DESCRIPTION</span></span>
<span data-ttu-id="42ea8-109">**AzKeyVaultCertificatePolicy** Cmdlet 會建立或更新金鑰保存庫中的憑證原則。</span><span class="sxs-lookup"><span data-stu-id="42ea8-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="42ea8-110">示例</span><span class="sxs-lookup"><span data-stu-id="42ea8-110">EXAMPLES</span></span>

### <span data-ttu-id="42ea8-111">範例1：設定憑證原則</span><span class="sxs-lookup"><span data-stu-id="42ea8-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        :
KeyUsage                        :
Ekus                            :
ValidityInMonths                : 6
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry :
RenewAtPercentageLifetime       :
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
CertificateTransparency         :
Enabled                         : True
Created                         :
Updated                         :
```

<span data-ttu-id="42ea8-112">這個命令會在 ContosoKV01 金鑰保存庫中設定 TestCert01 憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="42ea8-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="42ea8-113">參數</span><span class="sxs-lookup"><span data-stu-id="42ea8-113">PARAMETERS</span></span>

### <span data-ttu-id="42ea8-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="42ea8-114">-CertificateTransparency</span></span>
<span data-ttu-id="42ea8-115">指出是否已針對此憑證/頒發者啟用憑證透明;如果沒有指定，則預設值為 "true"。</span><span class="sxs-lookup"><span data-stu-id="42ea8-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'.</span></span>
<span data-ttu-id="42ea8-116">`-IssuerName` 需要在設定此屬性時指定。</span><span class="sxs-lookup"><span data-stu-id="42ea8-116">`-IssuerName` needs to be specified when setting this property.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-117">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="42ea8-117">-CertificateType</span></span>
<span data-ttu-id="42ea8-118">指定發行人的憑證類型。</span><span class="sxs-lookup"><span data-stu-id="42ea8-118">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-119">-曲線</span><span class="sxs-lookup"><span data-stu-id="42ea8-119">-Curve</span></span>
<span data-ttu-id="42ea8-120">指定憑證金鑰的橢圓曲線名稱。</span><span class="sxs-lookup"><span data-stu-id="42ea8-120">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="42ea8-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="42ea8-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42ea8-122">P-256</span><span class="sxs-lookup"><span data-stu-id="42ea8-122">P-256</span></span>
- <span data-ttu-id="42ea8-123">P-384</span><span class="sxs-lookup"><span data-stu-id="42ea8-123">P-384</span></span>
- <span data-ttu-id="42ea8-124">P-521</span><span class="sxs-lookup"><span data-stu-id="42ea8-124">P-521</span></span>
- <span data-ttu-id="42ea8-125">P-256K</span><span class="sxs-lookup"><span data-stu-id="42ea8-125">P-256K</span></span>
- <span data-ttu-id="42ea8-126">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="42ea8-126">SECP256K1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: P-256, P-384, P-521, P-256K, SECP256K1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ea8-127">-DefaultProfile</span></span>
<span data-ttu-id="42ea8-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="42ea8-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42ea8-129">-已停用</span><span class="sxs-lookup"><span data-stu-id="42ea8-129">-Disabled</span></span>
<span data-ttu-id="42ea8-130">表示憑證原則已停用。</span><span class="sxs-lookup"><span data-stu-id="42ea8-130">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-131">-DnsName</span><span class="sxs-lookup"><span data-stu-id="42ea8-131">-DnsName</span></span>
<span data-ttu-id="42ea8-132">指定憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="42ea8-132">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-133">-Eku</span><span class="sxs-lookup"><span data-stu-id="42ea8-133">-Ekus</span></span>
<span data-ttu-id="42ea8-134">指定憑證中 (Eku) 的增強型金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="42ea8-134">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-135">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="42ea8-135">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="42ea8-136">指定自動續約開始時到期前的天數。</span><span class="sxs-lookup"><span data-stu-id="42ea8-136">Specifies the number of days before expiration when automatic renewal should start.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-137">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="42ea8-137">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="42ea8-138">指定啟動通知自動程式開始的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="42ea8-138">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42ea8-139">-InputObject</span></span>
<span data-ttu-id="42ea8-140">指定憑證原則。</span><span class="sxs-lookup"><span data-stu-id="42ea8-140">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-141">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="42ea8-141">-IssuerName</span></span>
<span data-ttu-id="42ea8-142">指定此憑證的頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="42ea8-142">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-143">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="42ea8-143">-KeyNotExportable</span></span>
<span data-ttu-id="42ea8-144">表示金鑰無法匯出。</span><span class="sxs-lookup"><span data-stu-id="42ea8-144">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-145">KeySize</span><span class="sxs-lookup"><span data-stu-id="42ea8-145">-KeySize</span></span>
<span data-ttu-id="42ea8-146">指定憑證的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="42ea8-146">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="42ea8-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="42ea8-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42ea8-148">2048</span><span class="sxs-lookup"><span data-stu-id="42ea8-148">2048</span></span>
- <span data-ttu-id="42ea8-149">3072</span><span class="sxs-lookup"><span data-stu-id="42ea8-149">3072</span></span>
- <span data-ttu-id="42ea8-150">4096</span><span class="sxs-lookup"><span data-stu-id="42ea8-150">4096</span></span>
- <span data-ttu-id="42ea8-151">256</span><span class="sxs-lookup"><span data-stu-id="42ea8-151">256</span></span>
- <span data-ttu-id="42ea8-152">384</span><span class="sxs-lookup"><span data-stu-id="42ea8-152">384</span></span>
- <span data-ttu-id="42ea8-153">521</span><span class="sxs-lookup"><span data-stu-id="42ea8-153">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: 2048
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-154">-KeyType</span><span class="sxs-lookup"><span data-stu-id="42ea8-154">-KeyType</span></span>
<span data-ttu-id="42ea8-155">指定支援憑證之金鑰的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="42ea8-155">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="42ea8-156">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="42ea8-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42ea8-157">與眾不同</span><span class="sxs-lookup"><span data-stu-id="42ea8-157">RSA</span></span>
- <span data-ttu-id="42ea8-158">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="42ea8-158">RSA-HSM</span></span>
- <span data-ttu-id="42ea8-159">成員國</span><span class="sxs-lookup"><span data-stu-id="42ea8-159">EC</span></span>
- <span data-ttu-id="42ea8-160">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="42ea8-160">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-161">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="42ea8-161">-KeyUsage</span></span>
<span data-ttu-id="42ea8-162">指定憑證中的金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="42ea8-162">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-163">-名稱</span><span class="sxs-lookup"><span data-stu-id="42ea8-163">-Name</span></span>
<span data-ttu-id="42ea8-164">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="42ea8-164">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-165">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42ea8-165">-PassThru</span></span>
<span data-ttu-id="42ea8-166">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="42ea8-166">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="42ea8-167">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="42ea8-167">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="42ea8-168">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="42ea8-168">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="42ea8-169">指定到期前的天數，在此之後，就會開始更新自動程式。</span><span class="sxs-lookup"><span data-stu-id="42ea8-169">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-170">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="42ea8-170">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="42ea8-171">指定啟動證書自動程式開始前的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="42ea8-171">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-172">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="42ea8-172">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="42ea8-173">表示憑證在續約時重複使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="42ea8-173">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-174">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="42ea8-174">-SecretContentType</span></span>
<span data-ttu-id="42ea8-175">指定新的主要電子倉庫密碼的內容類型。</span><span class="sxs-lookup"><span data-stu-id="42ea8-175">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="42ea8-176">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="42ea8-176">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42ea8-177">應用程式/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="42ea8-177">application/x-pkcs12</span></span>
- <span data-ttu-id="42ea8-178">應用程式/x pem-檔案</span><span class="sxs-lookup"><span data-stu-id="42ea8-178">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-179">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="42ea8-179">-SubjectName</span></span>
<span data-ttu-id="42ea8-180">指定憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="42ea8-180">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="42ea8-181">-ValidityInMonths</span></span>
<span data-ttu-id="42ea8-182">指定憑證有效的月份數。</span><span class="sxs-lookup"><span data-stu-id="42ea8-182">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-183">-VaultName</span><span class="sxs-lookup"><span data-stu-id="42ea8-183">-VaultName</span></span>
<span data-ttu-id="42ea8-184">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="42ea8-184">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea8-185">-確認</span><span class="sxs-lookup"><span data-stu-id="42ea8-185">-Confirm</span></span>
<span data-ttu-id="42ea8-186">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="42ea8-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42ea8-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42ea8-187">-WhatIf</span></span>
<span data-ttu-id="42ea8-188">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="42ea8-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42ea8-189">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42ea8-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42ea8-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ea8-190">CommonParameters</span></span>
<span data-ttu-id="42ea8-191">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42ea8-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ea8-192">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="42ea8-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ea8-193">輸入</span><span class="sxs-lookup"><span data-stu-id="42ea8-193">INPUTS</span></span>

### <span data-ttu-id="42ea8-194">PSKeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="42ea8-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="42ea8-195">輸出</span><span class="sxs-lookup"><span data-stu-id="42ea8-195">OUTPUTS</span></span>

### <span data-ttu-id="42ea8-196">PSKeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="42ea8-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="42ea8-197">筆記</span><span class="sxs-lookup"><span data-stu-id="42ea8-197">NOTES</span></span>

## <span data-ttu-id="42ea8-198">相關連結</span><span class="sxs-lookup"><span data-stu-id="42ea8-198">RELATED LINKS</span></span>

[<span data-ttu-id="42ea8-199">AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="42ea8-199">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="42ea8-200">新-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="42ea8-200">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)
