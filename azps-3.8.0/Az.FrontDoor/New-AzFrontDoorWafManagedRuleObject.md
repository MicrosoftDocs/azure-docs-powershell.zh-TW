---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 6e56ff9b174ec13d0844a1ac860d34043f8b73cf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959778"
---
# <span data-ttu-id="21c16-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="21c16-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="21c16-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21c16-102">SYNOPSIS</span></span>
<span data-ttu-id="21c16-103">建立 WAF 原則建立的 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="21c16-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="21c16-104">句法</span><span class="sxs-lookup"><span data-stu-id="21c16-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21c16-105">說明</span><span class="sxs-lookup"><span data-stu-id="21c16-105">DESCRIPTION</span></span>
<span data-ttu-id="21c16-106">建立 WAF 原則建立的 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="21c16-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="21c16-107">示例</span><span class="sxs-lookup"><span data-stu-id="21c16-107">EXAMPLES</span></span>

### <span data-ttu-id="21c16-108">範例1</span><span class="sxs-lookup"><span data-stu-id="21c16-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="21c16-109">建立 ManagedRule 物件</span><span class="sxs-lookup"><span data-stu-id="21c16-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="21c16-110">參數</span><span class="sxs-lookup"><span data-stu-id="21c16-110">PARAMETERS</span></span>

### <span data-ttu-id="21c16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c16-111">-DefaultProfile</span></span>
<span data-ttu-id="21c16-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21c16-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21c16-113">-排除</span><span class="sxs-lookup"><span data-stu-id="21c16-113">-Exclusion</span></span>
<span data-ttu-id="21c16-114">他</span><span class="sxs-lookup"><span data-stu-id="21c16-114">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c16-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="21c16-115">-RuleGroupOverride</span></span>
<span data-ttu-id="21c16-116">Azure managed 提供者覆蓋設定的清單</span><span class="sxs-lookup"><span data-stu-id="21c16-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c16-117">-類型</span><span class="sxs-lookup"><span data-stu-id="21c16-117">-Type</span></span>
<span data-ttu-id="21c16-118">規則集的類型</span><span class="sxs-lookup"><span data-stu-id="21c16-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="21c16-119">-版本</span><span class="sxs-lookup"><span data-stu-id="21c16-119">-Version</span></span>
<span data-ttu-id="21c16-120">版本的規則集</span><span class="sxs-lookup"><span data-stu-id="21c16-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="21c16-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c16-121">CommonParameters</span></span>
<span data-ttu-id="21c16-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21c16-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c16-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="21c16-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c16-124">輸入</span><span class="sxs-lookup"><span data-stu-id="21c16-124">INPUTS</span></span>

### <span data-ttu-id="21c16-125">所有</span><span class="sxs-lookup"><span data-stu-id="21c16-125">None</span></span>

## <span data-ttu-id="21c16-126">輸出</span><span class="sxs-lookup"><span data-stu-id="21c16-126">OUTPUTS</span></span>

### <span data-ttu-id="21c16-127">PSAzureManagedRule 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="21c16-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="21c16-128">筆記</span><span class="sxs-lookup"><span data-stu-id="21c16-128">NOTES</span></span>

## <span data-ttu-id="21c16-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="21c16-129">RELATED LINKS</span></span>

<span data-ttu-id="21c16-130">[新-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
[新-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="21c16-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>