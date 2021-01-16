---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: fdd461ea2908e59ba824b09a49bed3b6b8f4d38f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274660"
---
# <span data-ttu-id="29bd8-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="29bd8-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="29bd8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="29bd8-103">從現有的應用程式閘道移除重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="29bd8-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="29bd8-104">句法</span><span class="sxs-lookup"><span data-stu-id="29bd8-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29bd8-105">說明</span><span class="sxs-lookup"><span data-stu-id="29bd8-105">DESCRIPTION</span></span>
<span data-ttu-id="29bd8-106">**AzApplicationGatewayRedirectConfiguration** Cmdlet 會從現有的應用程式閘道中移除重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="29bd8-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="29bd8-107">示例</span><span class="sxs-lookup"><span data-stu-id="29bd8-107">EXAMPLES</span></span>

### <span data-ttu-id="29bd8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="29bd8-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="29bd8-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="29bd8-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="29bd8-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 Redirect01 的重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="29bd8-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="29bd8-111">參數</span><span class="sxs-lookup"><span data-stu-id="29bd8-111">PARAMETERS</span></span>

### <span data-ttu-id="29bd8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="29bd8-112">-ApplicationGateway</span></span>
<span data-ttu-id="29bd8-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="29bd8-113">The applicationGateway</span></span>

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

### <span data-ttu-id="29bd8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29bd8-114">-DefaultProfile</span></span>
<span data-ttu-id="29bd8-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29bd8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29bd8-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="29bd8-116">-Name</span></span>
<span data-ttu-id="29bd8-117">重新導向配置的名稱</span><span class="sxs-lookup"><span data-stu-id="29bd8-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="29bd8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29bd8-118">CommonParameters</span></span>
<span data-ttu-id="29bd8-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29bd8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29bd8-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29bd8-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29bd8-121">輸入</span><span class="sxs-lookup"><span data-stu-id="29bd8-121">INPUTS</span></span>

### <span data-ttu-id="29bd8-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="29bd8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="29bd8-123">輸出</span><span class="sxs-lookup"><span data-stu-id="29bd8-123">OUTPUTS</span></span>

### <span data-ttu-id="29bd8-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="29bd8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="29bd8-125">筆記</span><span class="sxs-lookup"><span data-stu-id="29bd8-125">NOTES</span></span>

## <span data-ttu-id="29bd8-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="29bd8-126">RELATED LINKS</span></span>

[<span data-ttu-id="29bd8-127">附加 AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="29bd8-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="29bd8-128">AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="29bd8-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="29bd8-129">新-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="29bd8-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="29bd8-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="29bd8-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)