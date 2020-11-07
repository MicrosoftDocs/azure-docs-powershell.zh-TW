---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959524"
---
# <span data-ttu-id="91367-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="91367-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="91367-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91367-102">SYNOPSIS</span></span>
<span data-ttu-id="91367-103">取得所有可用的 web 應用程式防火牆規則集。</span><span class="sxs-lookup"><span data-stu-id="91367-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="91367-104">句法</span><span class="sxs-lookup"><span data-stu-id="91367-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91367-105">說明</span><span class="sxs-lookup"><span data-stu-id="91367-105">DESCRIPTION</span></span>
<span data-ttu-id="91367-106">**AzApplicationGatewayAvailableWafRuleSet** Cmdlet 會取得所有可用的 web 應用程式防火牆規則集。</span><span class="sxs-lookup"><span data-stu-id="91367-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="91367-107">示例</span><span class="sxs-lookup"><span data-stu-id="91367-107">EXAMPLES</span></span>

### <span data-ttu-id="91367-108">範例1</span><span class="sxs-lookup"><span data-stu-id="91367-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="91367-109">這個命令會傳回所有可用的 web 應用程式防火牆規則集。</span><span class="sxs-lookup"><span data-stu-id="91367-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="91367-110">參數</span><span class="sxs-lookup"><span data-stu-id="91367-110">PARAMETERS</span></span>

### <span data-ttu-id="91367-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91367-111">-DefaultProfile</span></span>
<span data-ttu-id="91367-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91367-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91367-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91367-113">CommonParameters</span></span>
<span data-ttu-id="91367-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91367-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91367-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="91367-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91367-116">輸入</span><span class="sxs-lookup"><span data-stu-id="91367-116">INPUTS</span></span>

### <span data-ttu-id="91367-117">所有</span><span class="sxs-lookup"><span data-stu-id="91367-117">None</span></span>

## <span data-ttu-id="91367-118">輸出</span><span class="sxs-lookup"><span data-stu-id="91367-118">OUTPUTS</span></span>

### <span data-ttu-id="91367-119">PSApplicationGatewayAvailableWafRuleSetsResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="91367-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="91367-120">筆記</span><span class="sxs-lookup"><span data-stu-id="91367-120">NOTES</span></span>
<span data-ttu-id="91367-121">**清單-AzApplicationGatewayAvailableWafRuleSets** 是 **AzApplicationGatewayAvailableWafRuleSet** Cmdlet 的別名。</span><span class="sxs-lookup"><span data-stu-id="91367-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="91367-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="91367-122">RELATED LINKS</span></span>