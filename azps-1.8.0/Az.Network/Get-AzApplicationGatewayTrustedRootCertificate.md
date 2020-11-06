---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 1e617ef1283937116bd97c24a968f247fa7552de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622070"
---
# <span data-ttu-id="f2bb3-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f2bb3-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="f2bb3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="f2bb3-103">從應用程式閘道取得具有特定名稱的受根信任證書。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="f2bb3-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2bb3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2bb3-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2bb3-105">DESCRIPTION</span></span>
<span data-ttu-id="f2bb3-106">**AzApplicationGatewayTrustedRootCertificate** Cmdlet 會從應用程式閘道取得具有特定名稱的根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="f2bb3-107">示例</span><span class="sxs-lookup"><span data-stu-id="f2bb3-107">EXAMPLES</span></span>

### <span data-ttu-id="f2bb3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f2bb3-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="f2bb3-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="f2bb3-110">第二個命令會從應用程式閘道取得具有指定名稱的受根信任證書。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="f2bb3-111">參數</span><span class="sxs-lookup"><span data-stu-id="f2bb3-111">PARAMETERS</span></span>

### <span data-ttu-id="f2bb3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2bb3-112">-ApplicationGateway</span></span>
<span data-ttu-id="f2bb3-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2bb3-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2bb3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2bb3-114">-DefaultProfile</span></span>
<span data-ttu-id="f2bb3-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2bb3-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2bb3-116">-Name</span></span>
<span data-ttu-id="f2bb3-117">TrustedRoot 憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="f2bb3-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="f2bb3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2bb3-118">CommonParameters</span></span>
<span data-ttu-id="f2bb3-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2bb3-120">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2bb3-121">輸入</span><span class="sxs-lookup"><span data-stu-id="f2bb3-121">INPUTS</span></span>

### <span data-ttu-id="f2bb3-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f2bb3-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f2bb3-123">輸出</span><span class="sxs-lookup"><span data-stu-id="f2bb3-123">OUTPUTS</span></span>

### <span data-ttu-id="f2bb3-124">PSApplicationGatewayTrustedRootCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f2bb3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="f2bb3-125">筆記</span><span class="sxs-lookup"><span data-stu-id="f2bb3-125">NOTES</span></span>

## <span data-ttu-id="f2bb3-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2bb3-126">RELATED LINKS</span></span>

[<span data-ttu-id="f2bb3-127">附加 AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f2bb3-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f2bb3-128">新-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f2bb3-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f2bb3-129">移除-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f2bb3-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f2bb3-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f2bb3-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)