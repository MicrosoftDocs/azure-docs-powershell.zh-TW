---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959728"
---
# <span data-ttu-id="e0314-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0314-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="e0314-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0314-102">SYNOPSIS</span></span>
<span data-ttu-id="e0314-103">將重寫規則集新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e0314-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="e0314-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0314-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0314-105">說明</span><span class="sxs-lookup"><span data-stu-id="e0314-105">DESCRIPTION</span></span>
<span data-ttu-id="e0314-106">**AzApplicationGatewayRewriteRuleSet** Cmdlet 會將重新寫入規則集新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e0314-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="e0314-107">示例</span><span class="sxs-lookup"><span data-stu-id="e0314-107">EXAMPLES</span></span>

### <span data-ttu-id="e0314-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e0314-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="e0314-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="e0314-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e0314-110">第二個命令會將重寫規則集新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e0314-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="e0314-111">參數</span><span class="sxs-lookup"><span data-stu-id="e0314-111">PARAMETERS</span></span>

### <span data-ttu-id="e0314-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e0314-112">-ApplicationGateway</span></span>
<span data-ttu-id="e0314-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e0314-113">The applicationGateway</span></span>

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

### <span data-ttu-id="e0314-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0314-114">-DefaultProfile</span></span>
<span data-ttu-id="e0314-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0314-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0314-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="e0314-116">-Name</span></span>
<span data-ttu-id="e0314-117">RewriteRuleSet 的名稱</span><span class="sxs-lookup"><span data-stu-id="e0314-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="e0314-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="e0314-118">-RewriteRule</span></span>
<span data-ttu-id="e0314-119">重新寫入規則的清單</span><span class="sxs-lookup"><span data-stu-id="e0314-119">List of rewrite rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0314-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0314-120">CommonParameters</span></span>
<span data-ttu-id="e0314-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0314-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0314-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0314-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0314-123">輸入</span><span class="sxs-lookup"><span data-stu-id="e0314-123">INPUTS</span></span>

### <span data-ttu-id="e0314-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e0314-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e0314-125">輸出</span><span class="sxs-lookup"><span data-stu-id="e0314-125">OUTPUTS</span></span>

### <span data-ttu-id="e0314-126">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e0314-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e0314-127">筆記</span><span class="sxs-lookup"><span data-stu-id="e0314-127">NOTES</span></span>

## <span data-ttu-id="e0314-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0314-128">RELATED LINKS</span></span>

[<span data-ttu-id="e0314-129">AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0314-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e0314-130">新-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0314-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e0314-131">移除-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0314-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e0314-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0314-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e0314-133">新-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e0314-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="e0314-134">新-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e0314-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="e0314-135">新-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0314-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)