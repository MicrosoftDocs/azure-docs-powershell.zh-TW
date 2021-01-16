---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 956abaa6dc42f5ba1cab0127e4adb37f3990f1d1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274344"
---
# <span data-ttu-id="74f16-101">Set-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="74f16-101">Set-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="74f16-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74f16-102">SYNOPSIS</span></span>
<span data-ttu-id="74f16-103">儲存已修改的 azure 防火牆策略規則集合群組</span><span class="sxs-lookup"><span data-stu-id="74f16-103">saves a modified azure firewall policy rule collection group</span></span>

## <span data-ttu-id="74f16-104">句法</span><span class="sxs-lookup"><span data-stu-id="74f16-104">SYNTAX</span></span>

### <span data-ttu-id="74f16-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="74f16-105">SetByNameParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String> -FirewallPolicyName <String>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f16-106">SetByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74f16-106">SetByParentInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f16-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74f16-107">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Priority <UInt32>] [-RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f16-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74f16-108">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74f16-109">說明</span><span class="sxs-lookup"><span data-stu-id="74f16-109">DESCRIPTION</span></span>
<span data-ttu-id="74f16-110">**AzFirewallPolicyRuleCollectionGroup** Cmdlet 會更新 Azure 防火牆原則中的規則集合群組。</span><span class="sxs-lookup"><span data-stu-id="74f16-110">The **Set-AzFirewallPolicyRuleCollectionGroup** cmdlet updates a rule collection groups in an Azure Firewall Policy.</span></span>

## <span data-ttu-id="74f16-111">示例</span><span class="sxs-lookup"><span data-stu-id="74f16-111">EXAMPLES</span></span>

### <span data-ttu-id="74f16-112">範例1</span><span class="sxs-lookup"><span data-stu-id="74f16-112">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="74f16-113">這個範例會在防火牆原則中更新規則集合群組 $fp</span><span class="sxs-lookup"><span data-stu-id="74f16-113">This example updates a rule collection group in the firewall policy $fp</span></span>

### <span data-ttu-id="74f16-114">範例2</span><span class="sxs-lookup"><span data-stu-id="74f16-114">Example 2</span></span>

<span data-ttu-id="74f16-115">儲存已修改的 azure 防火牆策略規則集合群組。</span><span class="sxs-lookup"><span data-stu-id="74f16-115">saves a modified azure firewall policy rule collection group.</span></span> <span data-ttu-id="74f16-116"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="74f16-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzFirewallPolicyRuleCollectionGroup -FirewallPolicyName <String> -Name rg1 -Priority 200 -ResourceGroupName TestRg -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
```

## <span data-ttu-id="74f16-117">參數</span><span class="sxs-lookup"><span data-stu-id="74f16-117">PARAMETERS</span></span>

### <span data-ttu-id="74f16-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f16-118">-DefaultProfile</span></span>
<span data-ttu-id="74f16-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74f16-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74f16-120">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="74f16-120">-FirewallPolicyName</span></span>
<span data-ttu-id="74f16-121">防火牆原則的名稱</span><span class="sxs-lookup"><span data-stu-id="74f16-121">The name of the firewall policy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f16-122">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="74f16-122">-FirewallPolicyObject</span></span>
<span data-ttu-id="74f16-123">防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="74f16-123">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f16-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74f16-124">-InputObject</span></span>
<span data-ttu-id="74f16-125">規則清單</span><span class="sxs-lookup"><span data-stu-id="74f16-125">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f16-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="74f16-126">-Name</span></span>
<span data-ttu-id="74f16-127">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="74f16-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f16-128">-優先順序</span><span class="sxs-lookup"><span data-stu-id="74f16-128">-Priority</span></span>
<span data-ttu-id="74f16-129">規則群組的優先順序</span><span class="sxs-lookup"><span data-stu-id="74f16-129">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f16-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74f16-130">-ResourceGroupName</span></span>
<span data-ttu-id="74f16-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="74f16-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f16-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74f16-132">-ResourceId</span></span>
<span data-ttu-id="74f16-133">規則集合 groupy 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="74f16-133">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f16-134">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="74f16-134">-RuleCollection</span></span>
<span data-ttu-id="74f16-135">規則集合清單</span><span class="sxs-lookup"><span data-stu-id="74f16-135">The list of rule collections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f16-136">-確認</span><span class="sxs-lookup"><span data-stu-id="74f16-136">-Confirm</span></span>
<span data-ttu-id="74f16-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="74f16-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f16-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74f16-138">-WhatIf</span></span>
<span data-ttu-id="74f16-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74f16-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74f16-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74f16-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f16-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f16-141">CommonParameters</span></span>
<span data-ttu-id="74f16-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74f16-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f16-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="74f16-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f16-144">輸入</span><span class="sxs-lookup"><span data-stu-id="74f16-144">INPUTS</span></span>

### <span data-ttu-id="74f16-145">System.object</span><span class="sxs-lookup"><span data-stu-id="74f16-145">System.String</span></span>

### <span data-ttu-id="74f16-146">PSAzureFirewallPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="74f16-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="74f16-147">輸出</span><span class="sxs-lookup"><span data-stu-id="74f16-147">OUTPUTS</span></span>

### <span data-ttu-id="74f16-148">PSAzureFirewallPolicyRuleCollectionGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="74f16-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="74f16-149">筆記</span><span class="sxs-lookup"><span data-stu-id="74f16-149">NOTES</span></span>

## <span data-ttu-id="74f16-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="74f16-150">RELATED LINKS</span></span>