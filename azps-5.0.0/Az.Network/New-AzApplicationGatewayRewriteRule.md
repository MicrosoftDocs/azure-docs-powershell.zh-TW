---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 5eaa5cdc8b00fa13d9fc0c06821b664f1afc2a65
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287508"
---
# <span data-ttu-id="bff4d-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="bff4d-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="bff4d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bff4d-102">SYNOPSIS</span></span>
<span data-ttu-id="bff4d-103">建立應用程式閘道的重寫規則。</span><span class="sxs-lookup"><span data-stu-id="bff4d-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="bff4d-104">句法</span><span class="sxs-lookup"><span data-stu-id="bff4d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bff4d-105">說明</span><span class="sxs-lookup"><span data-stu-id="bff4d-105">DESCRIPTION</span></span>
<span data-ttu-id="bff4d-106">**新的-AzApplicationGatewayRewriteRule** Cmdlet 會建立 Azure 應用程式閘道的重寫規則。</span><span class="sxs-lookup"><span data-stu-id="bff4d-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="bff4d-107">示例</span><span class="sxs-lookup"><span data-stu-id="bff4d-107">EXAMPLES</span></span>

### <span data-ttu-id="bff4d-108">範例1：建立應用程式閘道的重寫規則</span><span class="sxs-lookup"><span data-stu-id="bff4d-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="bff4d-109">這個命令會建立名為 rule1 的重新寫入規則，並將結果儲存在名為 $rule 的變數中。</span><span class="sxs-lookup"><span data-stu-id="bff4d-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="bff4d-110">參數</span><span class="sxs-lookup"><span data-stu-id="bff4d-110">PARAMETERS</span></span>

### <span data-ttu-id="bff4d-111">-ActionSet</span><span class="sxs-lookup"><span data-stu-id="bff4d-111">-ActionSet</span></span>
<span data-ttu-id="bff4d-112">重寫規則的 ActionSet</span><span class="sxs-lookup"><span data-stu-id="bff4d-112">ActionSet of the rewrite rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff4d-113">-條件</span><span class="sxs-lookup"><span data-stu-id="bff4d-113">-Condition</span></span>
<span data-ttu-id="bff4d-114">要執行重寫規則的條件</span><span class="sxs-lookup"><span data-stu-id="bff4d-114">Condition for the rewrite rule to execute</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff4d-115">-DefaultProfile</span></span>
<span data-ttu-id="bff4d-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bff4d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bff4d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="bff4d-117">-Name</span></span>
<span data-ttu-id="bff4d-118">RewriteRule 的名稱</span><span class="sxs-lookup"><span data-stu-id="bff4d-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="bff4d-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="bff4d-119">-RuleSequence</span></span>
<span data-ttu-id="bff4d-120">此重新寫入規則集中此重寫規則的規則排序</span><span class="sxs-lookup"><span data-stu-id="bff4d-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff4d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff4d-121">CommonParameters</span></span>
<span data-ttu-id="bff4d-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bff4d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff4d-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bff4d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff4d-124">輸入</span><span class="sxs-lookup"><span data-stu-id="bff4d-124">INPUTS</span></span>

### <span data-ttu-id="bff4d-125">所有</span><span class="sxs-lookup"><span data-stu-id="bff4d-125">None</span></span>

## <span data-ttu-id="bff4d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="bff4d-126">OUTPUTS</span></span>

### <span data-ttu-id="bff4d-127">PSApplicationGatewayRewriteRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bff4d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="bff4d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="bff4d-128">NOTES</span></span>

## <span data-ttu-id="bff4d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="bff4d-129">RELATED LINKS</span></span>

[<span data-ttu-id="bff4d-130">附加 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bff4d-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bff4d-131">AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bff4d-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bff4d-132">新-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bff4d-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bff4d-133">移除-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bff4d-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bff4d-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bff4d-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bff4d-135">新-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="bff4d-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="bff4d-136">新-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="bff4d-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)