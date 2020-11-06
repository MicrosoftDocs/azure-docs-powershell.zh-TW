---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 7d7403fff78d04153f1c088cbdf41f61677e2e7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621646"
---
# <span data-ttu-id="0183d-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0183d-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="0183d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0183d-102">SYNOPSIS</span></span>
<span data-ttu-id="0183d-103">從應用程式閘道移除重寫規則集。</span><span class="sxs-lookup"><span data-stu-id="0183d-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="0183d-104">句法</span><span class="sxs-lookup"><span data-stu-id="0183d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0183d-105">說明</span><span class="sxs-lookup"><span data-stu-id="0183d-105">DESCRIPTION</span></span>
<span data-ttu-id="0183d-106">**AzApplicationGatewayRewriteRuleSet** Cmdlet 會從 Azure 應用程式閘道移除重新寫入規則集。</span><span class="sxs-lookup"><span data-stu-id="0183d-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="0183d-107">示例</span><span class="sxs-lookup"><span data-stu-id="0183d-107">EXAMPLES</span></span>

### <span data-ttu-id="0183d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0183d-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="0183d-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="0183d-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0183d-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 RuleSet02 的重新寫入規則集。</span><span class="sxs-lookup"><span data-stu-id="0183d-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="0183d-111">參數</span><span class="sxs-lookup"><span data-stu-id="0183d-111">PARAMETERS</span></span>

### <span data-ttu-id="0183d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0183d-112">-ApplicationGateway</span></span>
<span data-ttu-id="0183d-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0183d-113">The applicationGateway</span></span>

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

### <span data-ttu-id="0183d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0183d-114">-DefaultProfile</span></span>
<span data-ttu-id="0183d-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0183d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0183d-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="0183d-116">-Name</span></span>
<span data-ttu-id="0183d-117">應用程式閘道 RewriteRuleSet 的名稱</span><span class="sxs-lookup"><span data-stu-id="0183d-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="0183d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0183d-118">CommonParameters</span></span>
<span data-ttu-id="0183d-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0183d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0183d-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0183d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0183d-121">輸入</span><span class="sxs-lookup"><span data-stu-id="0183d-121">INPUTS</span></span>

### <span data-ttu-id="0183d-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0183d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0183d-123">輸出</span><span class="sxs-lookup"><span data-stu-id="0183d-123">OUTPUTS</span></span>

### <span data-ttu-id="0183d-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0183d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0183d-125">筆記</span><span class="sxs-lookup"><span data-stu-id="0183d-125">NOTES</span></span>

## <span data-ttu-id="0183d-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="0183d-126">RELATED LINKS</span></span>

[<span data-ttu-id="0183d-127">附加 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0183d-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0183d-128">AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0183d-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0183d-129">新-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0183d-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0183d-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0183d-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0183d-131">新-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0183d-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="0183d-132">新-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0183d-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="0183d-133">新-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0183d-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)