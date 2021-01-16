---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 84c80ba4469d8003344d99b7dfbb89ff7d6660b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274163"
---
# <span data-ttu-id="62278-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="62278-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="62278-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62278-102">SYNOPSIS</span></span>
<span data-ttu-id="62278-103">從應用程式閘道 (s) 取得自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="62278-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="62278-104">句法</span><span class="sxs-lookup"><span data-stu-id="62278-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62278-105">說明</span><span class="sxs-lookup"><span data-stu-id="62278-105">DESCRIPTION</span></span>
<span data-ttu-id="62278-106">**AzApplicationGatewayCustomError** Cmdlet 會從應用程式閘道)  (s 中取得自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="62278-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="62278-107">示例</span><span class="sxs-lookup"><span data-stu-id="62278-107">EXAMPLES</span></span>

### <span data-ttu-id="62278-108">範例1：在應用程式閘道中取得自訂錯誤</span><span class="sxs-lookup"><span data-stu-id="62278-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="62278-109">這個命令會從應用程式閘道 $appgw 取得並傳回 HTTP 狀態碼502的自訂錯誤。</span><span class="sxs-lookup"><span data-stu-id="62278-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="62278-110">範例2：取得應用程式閘道中所有自訂錯誤的清單</span><span class="sxs-lookup"><span data-stu-id="62278-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="62278-111">這個命令會從應用程式閘道 $appgw 取得並傳回所有自訂錯誤的清單。</span><span class="sxs-lookup"><span data-stu-id="62278-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="62278-112">參數</span><span class="sxs-lookup"><span data-stu-id="62278-112">PARAMETERS</span></span>

### <span data-ttu-id="62278-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62278-113">-ApplicationGateway</span></span>
<span data-ttu-id="62278-114">應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="62278-114">The Application Gateway</span></span>

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

### <span data-ttu-id="62278-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62278-115">-DefaultProfile</span></span>
<span data-ttu-id="62278-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62278-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62278-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="62278-117">-StatusCode</span></span>
<span data-ttu-id="62278-118">應用程式閘道客戶錯誤的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="62278-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="62278-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62278-119">CommonParameters</span></span>
<span data-ttu-id="62278-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62278-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62278-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="62278-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62278-122">輸入</span><span class="sxs-lookup"><span data-stu-id="62278-122">INPUTS</span></span>

### <span data-ttu-id="62278-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="62278-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="62278-124">輸出</span><span class="sxs-lookup"><span data-stu-id="62278-124">OUTPUTS</span></span>

### <span data-ttu-id="62278-125">PSApplicationGatewayCustomError 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="62278-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="62278-126">筆記</span><span class="sxs-lookup"><span data-stu-id="62278-126">NOTES</span></span>

## <span data-ttu-id="62278-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="62278-127">RELATED LINKS</span></span>

[<span data-ttu-id="62278-128">附加 AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="62278-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="62278-129">新-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="62278-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="62278-130">移除-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="62278-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="62278-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="62278-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)