---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 7d6b8ec3e42ce34cc5652893e56fa272ce710c9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621833"
---
# <span data-ttu-id="81d01-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="81d01-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="81d01-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81d01-102">SYNOPSIS</span></span>
<span data-ttu-id="81d01-103">將條件新增至應用程式閘道的 RewriteRule。</span><span class="sxs-lookup"><span data-stu-id="81d01-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="81d01-104">句法</span><span class="sxs-lookup"><span data-stu-id="81d01-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81d01-105">說明</span><span class="sxs-lookup"><span data-stu-id="81d01-105">DESCRIPTION</span></span>
<span data-ttu-id="81d01-106">**AzApplicationGatewayRewriteRuleCondition** Cmdlet 會建立 Azure 應用程式閘道的重寫規則條件。</span><span class="sxs-lookup"><span data-stu-id="81d01-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="81d01-107">示例</span><span class="sxs-lookup"><span data-stu-id="81d01-107">EXAMPLES</span></span>

### <span data-ttu-id="81d01-108">範例1</span><span class="sxs-lookup"><span data-stu-id="81d01-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayRewriteRuleCondition -Variable "var_request_uri" -Pattern "http" -IgnoreCase
PS C:\> $condition

Variable   : var_request_uri
Pattern    : http
IgnoreCase : True
Negate     : False

PS C:\> $condition | Format-Table

Variable        Pattern IgnoreCase Negate
--------        ------- ---------- ------
var_request_uri http          True  False
```
<span data-ttu-id="81d01-109">這個命令會在重寫規則中建立一個條件，並將結果儲存在名為 $condition 的變數中。</span><span class="sxs-lookup"><span data-stu-id="81d01-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="81d01-110">參數</span><span class="sxs-lookup"><span data-stu-id="81d01-110">PARAMETERS</span></span>

### <span data-ttu-id="81d01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d01-111">-DefaultProfile</span></span>
<span data-ttu-id="81d01-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81d01-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d01-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="81d01-113">-IgnoreCase</span></span>
<span data-ttu-id="81d01-114">在模式上將此標誌設定為忽略大小寫</span><span class="sxs-lookup"><span data-stu-id="81d01-114">Set this flag to ignore case on the pattern</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d01-115">-否定</span><span class="sxs-lookup"><span data-stu-id="81d01-115">-Negate</span></span>
<span data-ttu-id="81d01-116">將此標誌設定為否定條件驗證</span><span class="sxs-lookup"><span data-stu-id="81d01-116">Set this flag to negate the condition validation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d01-117">-模式</span><span class="sxs-lookup"><span data-stu-id="81d01-117">-Pattern</span></span>
<span data-ttu-id="81d01-118">要在變數標頭中尋找的模式</span><span class="sxs-lookup"><span data-stu-id="81d01-118">Pattern to look for in the Variable Header</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d01-119">變數</span><span class="sxs-lookup"><span data-stu-id="81d01-119">-Variable</span></span>
<span data-ttu-id="81d01-120">要設定條件的標頭名稱</span><span class="sxs-lookup"><span data-stu-id="81d01-120">Name of the Header to set condition on it</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d01-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d01-121">CommonParameters</span></span>
<span data-ttu-id="81d01-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81d01-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="81d01-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81d01-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d01-124">輸入</span><span class="sxs-lookup"><span data-stu-id="81d01-124">INPUTS</span></span>

### <span data-ttu-id="81d01-125">所有</span><span class="sxs-lookup"><span data-stu-id="81d01-125">None</span></span>

## <span data-ttu-id="81d01-126">輸出</span><span class="sxs-lookup"><span data-stu-id="81d01-126">OUTPUTS</span></span>

### <span data-ttu-id="81d01-127">PSApplicationGatewayRewriteRuleCondition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="81d01-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="81d01-128">筆記</span><span class="sxs-lookup"><span data-stu-id="81d01-128">NOTES</span></span>

## <span data-ttu-id="81d01-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="81d01-129">RELATED LINKS</span></span>
[<span data-ttu-id="81d01-130">附加 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="81d01-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="81d01-131">AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="81d01-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="81d01-132">新-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="81d01-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="81d01-133">移除-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="81d01-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="81d01-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="81d01-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="81d01-135">新-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="81d01-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="81d01-136">新-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="81d01-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)