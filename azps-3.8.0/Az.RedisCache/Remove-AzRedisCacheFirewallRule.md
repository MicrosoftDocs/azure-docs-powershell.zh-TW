---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: c19be1f524519a55a5a95a575e97cfd250952570
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798581"
---
# <span data-ttu-id="d6f18-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d6f18-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="d6f18-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d6f18-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f18-103">從 Redis 快取中移除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="d6f18-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="d6f18-104">句法</span><span class="sxs-lookup"><span data-stu-id="d6f18-104">SYNTAX</span></span>

### <span data-ttu-id="d6f18-105">NormalParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d6f18-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6f18-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="d6f18-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6f18-107">說明</span><span class="sxs-lookup"><span data-stu-id="d6f18-107">DESCRIPTION</span></span>
<span data-ttu-id="d6f18-108">從 Redis 快取中移除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="d6f18-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="d6f18-109">示例</span><span class="sxs-lookup"><span data-stu-id="d6f18-109">EXAMPLES</span></span>

### <span data-ttu-id="d6f18-110">範例1：移除單一防火牆規則</span><span class="sxs-lookup"><span data-stu-id="d6f18-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="d6f18-111">這個命令會從名為 mycache 的 Redis Cache 中移除名為 ruleone 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="d6f18-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="d6f18-112">參數</span><span class="sxs-lookup"><span data-stu-id="d6f18-112">PARAMETERS</span></span>

### <span data-ttu-id="d6f18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f18-113">-DefaultProfile</span></span>
<span data-ttu-id="d6f18-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6f18-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6f18-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6f18-115">-InputObject</span></span>
<span data-ttu-id="d6f18-116">類型 PSRedisFirewallRule 的物件</span><span class="sxs-lookup"><span data-stu-id="d6f18-116">object of type PSRedisFirewallRule</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f18-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6f18-117">-Name</span></span>
<span data-ttu-id="d6f18-118">Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6f18-118">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f18-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6f18-119">-PassThru</span></span>
<span data-ttu-id="d6f18-120">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="d6f18-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d6f18-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f18-121">-ResourceGroupName</span></span>
<span data-ttu-id="d6f18-122">快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6f18-122">Name of resource group in which cache exists.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f18-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="d6f18-123">-RuleName</span></span>
<span data-ttu-id="d6f18-124">防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6f18-124">Name of firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f18-125">-確認</span><span class="sxs-lookup"><span data-stu-id="d6f18-125">-Confirm</span></span>
<span data-ttu-id="d6f18-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d6f18-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6f18-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f18-127">-WhatIf</span></span>
<span data-ttu-id="d6f18-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6f18-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6f18-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6f18-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6f18-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f18-130">CommonParameters</span></span>
<span data-ttu-id="d6f18-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d6f18-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f18-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d6f18-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f18-133">輸入</span><span class="sxs-lookup"><span data-stu-id="d6f18-133">INPUTS</span></span>

### <span data-ttu-id="d6f18-134">System.object</span><span class="sxs-lookup"><span data-stu-id="d6f18-134">System.String</span></span>

### <span data-ttu-id="d6f18-135">PSRedisFirewallRule 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="d6f18-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="d6f18-136">輸出</span><span class="sxs-lookup"><span data-stu-id="d6f18-136">OUTPUTS</span></span>

### <span data-ttu-id="d6f18-137">System.object</span><span class="sxs-lookup"><span data-stu-id="d6f18-137">System.Boolean</span></span>

## <span data-ttu-id="d6f18-138">筆記</span><span class="sxs-lookup"><span data-stu-id="d6f18-138">NOTES</span></span>

## <span data-ttu-id="d6f18-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6f18-139">RELATED LINKS</span></span>

[<span data-ttu-id="d6f18-140">新-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d6f18-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="d6f18-141">AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d6f18-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="d6f18-142">AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d6f18-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="d6f18-143">新-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d6f18-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="d6f18-144">移除-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d6f18-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="d6f18-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d6f18-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)