---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 46d86b6a910abcd00257277f61bb44dd426ab945
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286524"
---
# <span data-ttu-id="eda6b-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eda6b-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="eda6b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eda6b-102">SYNOPSIS</span></span>
<span data-ttu-id="eda6b-103">更新服務端點原則定義。</span><span class="sxs-lookup"><span data-stu-id="eda6b-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="eda6b-104">句法</span><span class="sxs-lookup"><span data-stu-id="eda6b-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eda6b-105">說明</span><span class="sxs-lookup"><span data-stu-id="eda6b-105">DESCRIPTION</span></span>
<span data-ttu-id="eda6b-106">**AzServiceEndpointPolicyDefinition** Cmdlet 會建立服務端點原則定義。</span><span class="sxs-lookup"><span data-stu-id="eda6b-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="eda6b-107">示例</span><span class="sxs-lookup"><span data-stu-id="eda6b-107">EXAMPLES</span></span>

### <span data-ttu-id="eda6b-108">範例1：更新服務端點原則中的服務端點原則定義</span><span class="sxs-lookup"><span data-stu-id="eda6b-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="eda6b-109">這個命令會更新 $ServiceEndpointPolicy 物件定義之服務端點原則中名為 Policydef1 的服務端點原則定義。</span><span class="sxs-lookup"><span data-stu-id="eda6b-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="eda6b-110">參數</span><span class="sxs-lookup"><span data-stu-id="eda6b-110">PARAMETERS</span></span>

### <span data-ttu-id="eda6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eda6b-111">-DefaultProfile</span></span>
<span data-ttu-id="eda6b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eda6b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eda6b-113">-描述</span><span class="sxs-lookup"><span data-stu-id="eda6b-113">-Description</span></span>
<span data-ttu-id="eda6b-114">定義的描述</span><span class="sxs-lookup"><span data-stu-id="eda6b-114">The description of the definition</span></span>

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

### <span data-ttu-id="eda6b-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="eda6b-115">-Name</span></span>
<span data-ttu-id="eda6b-116">規則名稱</span><span class="sxs-lookup"><span data-stu-id="eda6b-116">The name of the rule</span></span>

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

### <span data-ttu-id="eda6b-117">-服務</span><span class="sxs-lookup"><span data-stu-id="eda6b-117">-Service</span></span>
<span data-ttu-id="eda6b-118">服務名稱</span><span class="sxs-lookup"><span data-stu-id="eda6b-118">Name of the service</span></span>

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

### <span data-ttu-id="eda6b-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="eda6b-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="eda6b-120">NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="eda6b-120">The NetworkSecurityGroup</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eda6b-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="eda6b-121">-ServiceResource</span></span>
<span data-ttu-id="eda6b-122">服務資源清單</span><span class="sxs-lookup"><span data-stu-id="eda6b-122">List of service resources</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eda6b-123">-確認</span><span class="sxs-lookup"><span data-stu-id="eda6b-123">-Confirm</span></span>
<span data-ttu-id="eda6b-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eda6b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eda6b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eda6b-125">-WhatIf</span></span>
<span data-ttu-id="eda6b-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eda6b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eda6b-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eda6b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eda6b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eda6b-128">CommonParameters</span></span>
<span data-ttu-id="eda6b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eda6b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eda6b-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eda6b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eda6b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="eda6b-131">INPUTS</span></span>

### <span data-ttu-id="eda6b-132">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="eda6b-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="eda6b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="eda6b-133">OUTPUTS</span></span>

### <span data-ttu-id="eda6b-134">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="eda6b-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="eda6b-135">筆記</span><span class="sxs-lookup"><span data-stu-id="eda6b-135">NOTES</span></span>

## <span data-ttu-id="eda6b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="eda6b-136">RELATED LINKS</span></span>

[<span data-ttu-id="eda6b-137">附加 AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eda6b-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="eda6b-138">AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eda6b-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="eda6b-139">新-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eda6b-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="eda6b-140">移除-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eda6b-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)