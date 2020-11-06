---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: fff1e9190edda9ca5de12da66a2a138aa481ac7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621820"
---
# <span data-ttu-id="eed0f-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="eed0f-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="eed0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eed0f-102">SYNOPSIS</span></span>
<span data-ttu-id="eed0f-103">為應用程式閘道建立信任的根憑證。</span><span class="sxs-lookup"><span data-stu-id="eed0f-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="eed0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="eed0f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eed0f-105">說明</span><span class="sxs-lookup"><span data-stu-id="eed0f-105">DESCRIPTION</span></span>
<span data-ttu-id="eed0f-106">**新的-AzApplicationGatewayTrustedRootCertificate** Cmdlet 會針對 Azure 應用程式閘道建立信任的根憑證。</span><span class="sxs-lookup"><span data-stu-id="eed0f-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="eed0f-107">示例</span><span class="sxs-lookup"><span data-stu-id="eed0f-107">EXAMPLES</span></span>

### <span data-ttu-id="eed0f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="eed0f-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" --CertificateFile $certFilePath
```

<span data-ttu-id="eed0f-109">這個命令會建立名為 List "trc1" 的根信任證書，並將結果儲存在名為 $trc 的變數中。</span><span class="sxs-lookup"><span data-stu-id="eed0f-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="eed0f-110">參數</span><span class="sxs-lookup"><span data-stu-id="eed0f-110">PARAMETERS</span></span>

### <span data-ttu-id="eed0f-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="eed0f-111">-CertificateFile</span></span>
<span data-ttu-id="eed0f-112">憑證 CER 檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="eed0f-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="eed0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed0f-113">-DefaultProfile</span></span>
<span data-ttu-id="eed0f-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eed0f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eed0f-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="eed0f-115">-Name</span></span>
<span data-ttu-id="eed0f-116">TrustedRoot 憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="eed0f-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="eed0f-117">-確認</span><span class="sxs-lookup"><span data-stu-id="eed0f-117">-Confirm</span></span>
<span data-ttu-id="eed0f-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eed0f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eed0f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eed0f-119">-WhatIf</span></span>
<span data-ttu-id="eed0f-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eed0f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eed0f-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eed0f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eed0f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed0f-122">CommonParameters</span></span>
<span data-ttu-id="eed0f-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eed0f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed0f-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eed0f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed0f-125">輸入</span><span class="sxs-lookup"><span data-stu-id="eed0f-125">INPUTS</span></span>

### <span data-ttu-id="eed0f-126">所有</span><span class="sxs-lookup"><span data-stu-id="eed0f-126">None</span></span>

## <span data-ttu-id="eed0f-127">輸出</span><span class="sxs-lookup"><span data-stu-id="eed0f-127">OUTPUTS</span></span>

### <span data-ttu-id="eed0f-128">PSApplicationGatewayTrustedRootCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="eed0f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="eed0f-129">筆記</span><span class="sxs-lookup"><span data-stu-id="eed0f-129">NOTES</span></span>

## <span data-ttu-id="eed0f-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="eed0f-130">RELATED LINKS</span></span>

[<span data-ttu-id="eed0f-131">附加 AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="eed0f-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="eed0f-132">AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="eed0f-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="eed0f-133">移除-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="eed0f-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="eed0f-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="eed0f-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)