---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9ff6532cb43d7ece7460651eb4493201de4734b1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793620"
---
# <span data-ttu-id="a8e23-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="a8e23-101">Set-AzsPlan</span></span>

## <span data-ttu-id="a8e23-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8e23-102">SYNOPSIS</span></span>
<span data-ttu-id="a8e23-103">更新指定的方案</span><span class="sxs-lookup"><span data-stu-id="a8e23-103">Updates the specified plan</span></span>

## <span data-ttu-id="a8e23-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8e23-104">SYNTAX</span></span>

### <span data-ttu-id="a8e23-105">更新 (預設) </span><span class="sxs-lookup"><span data-stu-id="a8e23-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8e23-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a8e23-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8e23-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8e23-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8e23-108">說明</span><span class="sxs-lookup"><span data-stu-id="a8e23-108">DESCRIPTION</span></span>
<span data-ttu-id="a8e23-109">更新指定的方案</span><span class="sxs-lookup"><span data-stu-id="a8e23-109">Updates the specified plan</span></span>

## <span data-ttu-id="a8e23-110">示例</span><span class="sxs-lookup"><span data-stu-id="a8e23-110">EXAMPLES</span></span>

### <span data-ttu-id="a8e23-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a8e23-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="a8e23-112">更新指定的方案</span><span class="sxs-lookup"><span data-stu-id="a8e23-112">Updates the specified plan</span></span>

## <span data-ttu-id="a8e23-113">參數</span><span class="sxs-lookup"><span data-stu-id="a8e23-113">PARAMETERS</span></span>

### <span data-ttu-id="a8e23-114">-描述</span><span class="sxs-lookup"><span data-stu-id="a8e23-114">-Description</span></span>
<span data-ttu-id="a8e23-115">方案的描述。</span><span class="sxs-lookup"><span data-stu-id="a8e23-115">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e23-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a8e23-116">-DisplayName</span></span>
<span data-ttu-id="a8e23-117">顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a8e23-117">Display name.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e23-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="a8e23-118">-ExternalReferenceId</span></span>
<span data-ttu-id="a8e23-119">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8e23-119">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e23-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8e23-120">-InputObject</span></span>
<span data-ttu-id="a8e23-121">AzureStack 類型的輸入物件，其為 [系統管理]。</span><span class="sxs-lookup"><span data-stu-id="a8e23-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

```yaml
Type: Plan
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e23-122">-位置</span><span class="sxs-lookup"><span data-stu-id="a8e23-122">-Location</span></span>
<span data-ttu-id="a8e23-123">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="a8e23-123">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e23-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="a8e23-124">-Name</span></span>
<span data-ttu-id="a8e23-125">方案名稱。</span><span class="sxs-lookup"><span data-stu-id="a8e23-125">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e23-126">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="a8e23-126">-QuotaIds</span></span>
<span data-ttu-id="a8e23-127">方案中的配額識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8e23-127">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e23-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8e23-128">-ResourceGroupName</span></span>
<span data-ttu-id="a8e23-129">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a8e23-129">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e23-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8e23-130">-ResourceId</span></span>
<span data-ttu-id="a8e23-131">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="a8e23-131">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e23-132">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="a8e23-132">-SkuIds</span></span>
<span data-ttu-id="a8e23-133">SKU 識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8e23-133">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e23-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="a8e23-134">-SubscriptionCount</span></span>
<span data-ttu-id="a8e23-135">[訂閱計數]。</span><span class="sxs-lookup"><span data-stu-id="a8e23-135">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e23-136">-確認</span><span class="sxs-lookup"><span data-stu-id="a8e23-136">-Confirm</span></span>
<span data-ttu-id="a8e23-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a8e23-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e23-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8e23-138">-WhatIf</span></span>
<span data-ttu-id="a8e23-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a8e23-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8e23-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8e23-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e23-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8e23-141">CommonParameters</span></span>
<span data-ttu-id="a8e23-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8e23-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8e23-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a8e23-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8e23-144">輸入</span><span class="sxs-lookup"><span data-stu-id="a8e23-144">INPUTS</span></span>

## <span data-ttu-id="a8e23-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a8e23-145">OUTPUTS</span></span>

### <span data-ttu-id="a8e23-146">AzureStack. 管理模型. 規劃</span><span class="sxs-lookup"><span data-stu-id="a8e23-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="a8e23-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a8e23-147">NOTES</span></span>

## <span data-ttu-id="a8e23-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8e23-148">RELATED LINKS</span></span>
