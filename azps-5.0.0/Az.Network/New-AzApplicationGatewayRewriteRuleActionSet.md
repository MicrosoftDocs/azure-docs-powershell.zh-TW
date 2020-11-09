---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f20647613a6e484d46a8785cfebea304b6a7ff23
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287504"
---
# <span data-ttu-id="d0dd2-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d0dd2-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="d0dd2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="d0dd2-103">建立應用程式閘道的重寫規則動作集。</span><span class="sxs-lookup"><span data-stu-id="d0dd2-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="d0dd2-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0dd2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0dd2-105">說明</span><span class="sxs-lookup"><span data-stu-id="d0dd2-105">DESCRIPTION</span></span>
<span data-ttu-id="d0dd2-106">**新的-AzApplicationGatewayRewriteRuleActionSet** Cmdlet 會建立 Azure 應用程式閘道的重寫規則動作集。</span><span class="sxs-lookup"><span data-stu-id="d0dd2-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="d0dd2-107">示例</span><span class="sxs-lookup"><span data-stu-id="d0dd2-107">EXAMPLES</span></span>

### <span data-ttu-id="d0dd2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d0dd2-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="d0dd2-109">這個命令會建立重寫規則動作集，並將結果儲存在名為 $action 的變數中。</span><span class="sxs-lookup"><span data-stu-id="d0dd2-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="d0dd2-110">參數</span><span class="sxs-lookup"><span data-stu-id="d0dd2-110">PARAMETERS</span></span>

### <span data-ttu-id="d0dd2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0dd2-111">-DefaultProfile</span></span>
<span data-ttu-id="d0dd2-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0dd2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0dd2-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0dd2-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="d0dd2-114">要求標頭設定清單</span><span class="sxs-lookup"><span data-stu-id="d0dd2-114">List of request header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0dd2-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0dd2-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="d0dd2-116">回應標頭設定清單</span><span class="sxs-lookup"><span data-stu-id="d0dd2-116">List of response header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0dd2-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0dd2-117">-UrlConfiguration</span></span>
<span data-ttu-id="d0dd2-118">動作集的 Url 設定</span><span class="sxs-lookup"><span data-stu-id="d0dd2-118">Url Configuration for action set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0dd2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0dd2-119">CommonParameters</span></span>
<span data-ttu-id="d0dd2-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0dd2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0dd2-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d0dd2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0dd2-122">輸入</span><span class="sxs-lookup"><span data-stu-id="d0dd2-122">INPUTS</span></span>

### <span data-ttu-id="d0dd2-123">所有</span><span class="sxs-lookup"><span data-stu-id="d0dd2-123">None</span></span>

## <span data-ttu-id="d0dd2-124">輸出</span><span class="sxs-lookup"><span data-stu-id="d0dd2-124">OUTPUTS</span></span>

### <span data-ttu-id="d0dd2-125">PSApplicationGatewayRewriteRuleActionSet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d0dd2-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="d0dd2-126">筆記</span><span class="sxs-lookup"><span data-stu-id="d0dd2-126">NOTES</span></span>

## <span data-ttu-id="d0dd2-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0dd2-127">RELATED LINKS</span></span>

[<span data-ttu-id="d0dd2-128">附加 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0dd2-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d0dd2-129">AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0dd2-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d0dd2-130">新-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0dd2-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d0dd2-131">移除-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0dd2-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d0dd2-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0dd2-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d0dd2-133">新-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d0dd2-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="d0dd2-134">新-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0dd2-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="d0dd2-135">新-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0dd2-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)