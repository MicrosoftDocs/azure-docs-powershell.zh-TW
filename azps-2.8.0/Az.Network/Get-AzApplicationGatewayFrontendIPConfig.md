---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 88393e7c40ba9888602f144410263e7210a3db9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790209"
---
# <span data-ttu-id="4532b-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4532b-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="4532b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4532b-102">SYNOPSIS</span></span>
<span data-ttu-id="4532b-103">取得應用程式閘道的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="4532b-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="4532b-104">句法</span><span class="sxs-lookup"><span data-stu-id="4532b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4532b-105">說明</span><span class="sxs-lookup"><span data-stu-id="4532b-105">DESCRIPTION</span></span>
<span data-ttu-id="4532b-106">**AzApplicationGatewayFrontendIPConfig** Cmdlet 會取得應用程式閘道的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="4532b-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="4532b-107">示例</span><span class="sxs-lookup"><span data-stu-id="4532b-107">EXAMPLES</span></span>

### <span data-ttu-id="4532b-108">範例1：取得指定的前端 IP 設定</span><span class="sxs-lookup"><span data-stu-id="4532b-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="4532b-109">第一個命令會從名為 ResourceGroup01 的資源群組中取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會從 $AppGw 取得名為 FrontEndIP01 的前端 IP 設定，並將它儲存在 $FrontEndIP 變數中。</span><span class="sxs-lookup"><span data-stu-id="4532b-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="4532b-110">範例2：取得前端 IP 配置清單</span><span class="sxs-lookup"><span data-stu-id="4532b-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="4532b-111">第一個命令會從名為 ResourceGroup01 的資源群組中取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會從 $AppGw 取得前端 IP 配置的清單，並將其儲存在 $FrontEndIPs 變數中。</span><span class="sxs-lookup"><span data-stu-id="4532b-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="4532b-112">參數</span><span class="sxs-lookup"><span data-stu-id="4532b-112">PARAMETERS</span></span>

### <span data-ttu-id="4532b-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4532b-113">-ApplicationGateway</span></span>
<span data-ttu-id="4532b-114">指定包含前端 IP 設定的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="4532b-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="4532b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4532b-115">-DefaultProfile</span></span>
<span data-ttu-id="4532b-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4532b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4532b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4532b-117">-Name</span></span>
<span data-ttu-id="4532b-118">指定此 Cmdlet 所取得之前端 IP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="4532b-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4532b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4532b-119">CommonParameters</span></span>
<span data-ttu-id="4532b-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4532b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4532b-121">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4532b-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4532b-122">輸入</span><span class="sxs-lookup"><span data-stu-id="4532b-122">INPUTS</span></span>

### <span data-ttu-id="4532b-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4532b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4532b-124">輸出</span><span class="sxs-lookup"><span data-stu-id="4532b-124">OUTPUTS</span></span>

### <span data-ttu-id="4532b-125">PSApplicationGatewayFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4532b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="4532b-126">筆記</span><span class="sxs-lookup"><span data-stu-id="4532b-126">NOTES</span></span>

## <span data-ttu-id="4532b-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="4532b-127">RELATED LINKS</span></span>

[<span data-ttu-id="4532b-128">附加 AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4532b-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4532b-129">新-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4532b-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4532b-130">移除-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4532b-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4532b-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4532b-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)

