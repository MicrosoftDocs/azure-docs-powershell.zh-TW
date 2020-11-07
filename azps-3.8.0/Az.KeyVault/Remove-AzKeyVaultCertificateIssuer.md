---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 061b16758386cf2e279250a1ab72cdcf4180a1f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958492"
---
# <span data-ttu-id="d4074-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d4074-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="d4074-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4074-102">SYNOPSIS</span></span>
<span data-ttu-id="d4074-103">從金鑰保存庫刪除憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="d4074-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="d4074-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4074-104">SYNTAX</span></span>

### <span data-ttu-id="d4074-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="d4074-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4074-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d4074-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4074-107">說明</span><span class="sxs-lookup"><span data-stu-id="d4074-107">DESCRIPTION</span></span>
<span data-ttu-id="d4074-108">**AzKeyVaultCertificateIssuer** Cmdlet 會從金鑰保存庫刪除憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="d4074-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="d4074-109">示例</span><span class="sxs-lookup"><span data-stu-id="d4074-109">EXAMPLES</span></span>

### <span data-ttu-id="d4074-110">範例1：移除憑證頒發者</span><span class="sxs-lookup"><span data-stu-id="d4074-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="d4074-111">這個命令會從 [ContosoKV01] 金鑰保存庫中移除名為 TestIssuer01 的憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="d4074-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="d4074-112">參數</span><span class="sxs-lookup"><span data-stu-id="d4074-112">PARAMETERS</span></span>

### <span data-ttu-id="d4074-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4074-113">-DefaultProfile</span></span>
<span data-ttu-id="d4074-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d4074-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4074-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d4074-115">-Force</span></span>
<span data-ttu-id="d4074-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d4074-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d4074-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4074-117">-InputObject</span></span>
<span data-ttu-id="d4074-118">憑證簽發者物件</span><span class="sxs-lookup"><span data-stu-id="d4074-118">Certificate Issuer Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4074-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4074-119">-Name</span></span>
<span data-ttu-id="d4074-120">指定要移除之頒發者的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4074-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4074-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4074-121">-PassThru</span></span>
<span data-ttu-id="d4074-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="d4074-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d4074-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="d4074-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d4074-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d4074-124">-VaultName</span></span>
<span data-ttu-id="d4074-125">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4074-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4074-126">-確認</span><span class="sxs-lookup"><span data-stu-id="d4074-126">-Confirm</span></span>
<span data-ttu-id="d4074-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4074-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4074-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4074-128">-WhatIf</span></span>
<span data-ttu-id="d4074-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4074-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4074-130">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4074-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4074-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4074-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4074-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4074-132">CommonParameters</span></span>
<span data-ttu-id="d4074-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4074-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4074-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d4074-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4074-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d4074-135">INPUTS</span></span>

### <span data-ttu-id="d4074-136">PSKeyVaultCertificateIssuerIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="d4074-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="d4074-137">輸出</span><span class="sxs-lookup"><span data-stu-id="d4074-137">OUTPUTS</span></span>

### <span data-ttu-id="d4074-138">PSKeyVaultCertificateIssuer 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="d4074-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="d4074-139">筆記</span><span class="sxs-lookup"><span data-stu-id="d4074-139">NOTES</span></span>

## <span data-ttu-id="d4074-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4074-140">RELATED LINKS</span></span>

[<span data-ttu-id="d4074-141">AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d4074-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="d4074-142">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d4074-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)

