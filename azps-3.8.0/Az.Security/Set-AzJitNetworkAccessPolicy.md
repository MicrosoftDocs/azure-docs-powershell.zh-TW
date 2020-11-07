---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: a40fba16bd7d361544ca10867d2c575965447c12
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957524"
---
# <span data-ttu-id="63f5b-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="63f5b-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="63f5b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="63f5b-102">SYNOPSIS</span></span>
<span data-ttu-id="63f5b-103">更新 JIT 網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="63f5b-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="63f5b-104">句法</span><span class="sxs-lookup"><span data-stu-id="63f5b-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63f5b-105">說明</span><span class="sxs-lookup"><span data-stu-id="63f5b-105">DESCRIPTION</span></span>
<span data-ttu-id="63f5b-106">更新 JIT 網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="63f5b-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="63f5b-107">示例</span><span class="sxs-lookup"><span data-stu-id="63f5b-107">EXAMPLES</span></span>

### <span data-ttu-id="63f5b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="63f5b-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="63f5b-109">使用新的 VM 規則更新 JIT 網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="63f5b-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="63f5b-110">參數</span><span class="sxs-lookup"><span data-stu-id="63f5b-110">PARAMETERS</span></span>

### <span data-ttu-id="63f5b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f5b-111">-DefaultProfile</span></span>
<span data-ttu-id="63f5b-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="63f5b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63f5b-113">類型</span><span class="sxs-lookup"><span data-stu-id="63f5b-113">-Kind</span></span>
<span data-ttu-id="63f5b-114">明示.</span><span class="sxs-lookup"><span data-stu-id="63f5b-114">Kind.</span></span>

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

### <span data-ttu-id="63f5b-115">-位置</span><span class="sxs-lookup"><span data-stu-id="63f5b-115">-Location</span></span>
<span data-ttu-id="63f5b-116">位於.</span><span class="sxs-lookup"><span data-stu-id="63f5b-116">Location.</span></span>

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

### <span data-ttu-id="63f5b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="63f5b-117">-Name</span></span>
<span data-ttu-id="63f5b-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="63f5b-118">Resource name.</span></span>

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

### <span data-ttu-id="63f5b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63f5b-119">-ResourceGroupName</span></span>
<span data-ttu-id="63f5b-120">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="63f5b-120">Resource group name.</span></span>

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

### <span data-ttu-id="63f5b-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="63f5b-121">-VirtualMachine</span></span>
<span data-ttu-id="63f5b-122">虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="63f5b-122">Virtual Machines.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f5b-123">-確認</span><span class="sxs-lookup"><span data-stu-id="63f5b-123">-Confirm</span></span>
<span data-ttu-id="63f5b-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="63f5b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63f5b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63f5b-125">-WhatIf</span></span>
<span data-ttu-id="63f5b-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="63f5b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63f5b-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="63f5b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63f5b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f5b-128">CommonParameters</span></span>
<span data-ttu-id="63f5b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="63f5b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f5b-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="63f5b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f5b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="63f5b-131">INPUTS</span></span>

### <span data-ttu-id="63f5b-132">所有</span><span class="sxs-lookup"><span data-stu-id="63f5b-132">None</span></span>

## <span data-ttu-id="63f5b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="63f5b-133">OUTPUTS</span></span>

### <span data-ttu-id="63f5b-134">PSSecurityJitNetworkAccessPolicy 中的 JitNetworkAccessPolicies （Security..。</span><span class="sxs-lookup"><span data-stu-id="63f5b-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="63f5b-135">筆記</span><span class="sxs-lookup"><span data-stu-id="63f5b-135">NOTES</span></span>

## <span data-ttu-id="63f5b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="63f5b-136">RELATED LINKS</span></span>