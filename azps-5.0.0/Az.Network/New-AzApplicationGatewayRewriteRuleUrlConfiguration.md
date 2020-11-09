---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287500"
---
# <span data-ttu-id="daa81-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa81-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="daa81-102">摘要</span><span class="sxs-lookup"><span data-stu-id="daa81-102">SYNOPSIS</span></span>
<span data-ttu-id="daa81-103">建立應用程式閘道的重寫規則 url 配置。</span><span class="sxs-lookup"><span data-stu-id="daa81-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="daa81-104">句法</span><span class="sxs-lookup"><span data-stu-id="daa81-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daa81-105">說明</span><span class="sxs-lookup"><span data-stu-id="daa81-105">DESCRIPTION</span></span>
<span data-ttu-id="daa81-106">**AzApplicationGatewayRewriteRuleUrlConfiguration** Cmdlet 會建立 Azure 應用程式閘道的重寫規則 url 配置。</span><span class="sxs-lookup"><span data-stu-id="daa81-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="daa81-107">示例</span><span class="sxs-lookup"><span data-stu-id="daa81-107">EXAMPLES</span></span>

### <span data-ttu-id="daa81-108">範例1</span><span class="sxs-lookup"><span data-stu-id="daa81-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="daa81-109">這個命令會建立重寫規則 url 設定，並將結果儲存在名為 $urlConfiguration 的變數中。</span><span class="sxs-lookup"><span data-stu-id="daa81-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="daa81-110">如果您想要更新任何現有的 UrlConfiguration，您可以建立新的 UrlConfiguration，並將新 UrlConfiguration 指派給重新寫入規則動作集的 UrlConfiguration 屬性來執行此操作。</span><span class="sxs-lookup"><span data-stu-id="daa81-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="daa81-111">參數</span><span class="sxs-lookup"><span data-stu-id="daa81-111">PARAMETERS</span></span>

### <span data-ttu-id="daa81-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa81-112">-DefaultProfile</span></span>
<span data-ttu-id="daa81-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="daa81-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daa81-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="daa81-114">-ModifiedPath</span></span>
<span data-ttu-id="daa81-115">Url 路徑值。</span><span class="sxs-lookup"><span data-stu-id="daa81-115">Url path value.</span></span>

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

### <span data-ttu-id="daa81-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="daa81-116">-ModifiedQueryString</span></span>
<span data-ttu-id="daa81-117">Url 查詢字串值。</span><span class="sxs-lookup"><span data-stu-id="daa81-117">Url query string value.</span></span>

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

### <span data-ttu-id="daa81-118">-重新路由</span><span class="sxs-lookup"><span data-stu-id="daa81-118">-Reroute</span></span>
<span data-ttu-id="daa81-119">使用 [已修改的路徑] 重新評估以路徑為基礎的要求路由規則中提供的 url 路徑對應的標記。</span><span class="sxs-lookup"><span data-stu-id="daa81-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daa81-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa81-120">CommonParameters</span></span>
<span data-ttu-id="daa81-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="daa81-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa81-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="daa81-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa81-123">輸入</span><span class="sxs-lookup"><span data-stu-id="daa81-123">INPUTS</span></span>

### <span data-ttu-id="daa81-124">所有</span><span class="sxs-lookup"><span data-stu-id="daa81-124">None</span></span>

## <span data-ttu-id="daa81-125">輸出</span><span class="sxs-lookup"><span data-stu-id="daa81-125">OUTPUTS</span></span>

### <span data-ttu-id="daa81-126">PSApplicationGatewayUrlConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="daa81-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="daa81-127">筆記</span><span class="sxs-lookup"><span data-stu-id="daa81-127">NOTES</span></span>

## <span data-ttu-id="daa81-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="daa81-128">RELATED LINKS</span></span>

[<span data-ttu-id="daa81-129">附加 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa81-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="daa81-130">AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa81-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="daa81-131">新-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa81-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="daa81-132">移除-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa81-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="daa81-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa81-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="daa81-134">新-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="daa81-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="daa81-135">新-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="daa81-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)