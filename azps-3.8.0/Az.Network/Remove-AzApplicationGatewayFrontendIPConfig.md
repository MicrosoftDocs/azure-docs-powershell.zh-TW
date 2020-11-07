---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 8abfca99729dcbf99592a8efcb191e6a7883e3b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956301"
---
# <span data-ttu-id="3cd65-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3cd65-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="3cd65-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3cd65-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd65-103">從應用程式閘道移除前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="3cd65-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="3cd65-104">句法</span><span class="sxs-lookup"><span data-stu-id="3cd65-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cd65-105">說明</span><span class="sxs-lookup"><span data-stu-id="3cd65-105">DESCRIPTION</span></span>
<span data-ttu-id="3cd65-106">**AzApplicationGatewayFrontendIPConfig** Cmdlet 會將前端 IP 從 Azure 應用程式閘道中移除。</span><span class="sxs-lookup"><span data-stu-id="3cd65-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="3cd65-107">示例</span><span class="sxs-lookup"><span data-stu-id="3cd65-107">EXAMPLES</span></span>

### <span data-ttu-id="3cd65-108">範例1：移除前端 IP 設定</span><span class="sxs-lookup"><span data-stu-id="3cd65-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="3cd65-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="3cd65-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3cd65-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 FrontEndIP02 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="3cd65-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="3cd65-111">參數</span><span class="sxs-lookup"><span data-stu-id="3cd65-111">PARAMETERS</span></span>

### <span data-ttu-id="3cd65-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3cd65-112">-ApplicationGateway</span></span>
<span data-ttu-id="3cd65-113">指定要移除前端 IP 設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="3cd65-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="3cd65-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd65-114">-DefaultProfile</span></span>
<span data-ttu-id="3cd65-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3cd65-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cd65-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="3cd65-116">-Name</span></span>
<span data-ttu-id="3cd65-117">指定要移除的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="3cd65-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="3cd65-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd65-118">CommonParameters</span></span>
<span data-ttu-id="3cd65-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3cd65-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd65-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3cd65-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd65-121">輸入</span><span class="sxs-lookup"><span data-stu-id="3cd65-121">INPUTS</span></span>

### <span data-ttu-id="3cd65-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3cd65-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3cd65-123">輸出</span><span class="sxs-lookup"><span data-stu-id="3cd65-123">OUTPUTS</span></span>

### <span data-ttu-id="3cd65-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3cd65-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3cd65-125">筆記</span><span class="sxs-lookup"><span data-stu-id="3cd65-125">NOTES</span></span>

## <span data-ttu-id="3cd65-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="3cd65-126">RELATED LINKS</span></span>

[<span data-ttu-id="3cd65-127">附加 AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3cd65-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3cd65-128">AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3cd65-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3cd65-129">新-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3cd65-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3cd65-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3cd65-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)

