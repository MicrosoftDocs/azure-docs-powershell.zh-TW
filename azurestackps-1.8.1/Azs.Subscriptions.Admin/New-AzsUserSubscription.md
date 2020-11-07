---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d4b7abdeb085c7cfee6444c4afeeb6a3e79d99e9
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793789"
---
# <span data-ttu-id="f19c7-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="f19c7-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="f19c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f19c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f19c7-103">建立新的訂閱。</span><span class="sxs-lookup"><span data-stu-id="f19c7-103">Create a new subscription.</span></span>

## <span data-ttu-id="f19c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="f19c7-104">SYNTAX</span></span>

```
New-AzsUserSubscription [-Owner] <String> [-OfferId] <String> [[-TenantId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-RoutingResourceManagerType] <String>]
 [[-ExternalReferenceId] <String>] [[-State] <String>] [[-SubscriptionId] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f19c7-105">說明</span><span class="sxs-lookup"><span data-stu-id="f19c7-105">DESCRIPTION</span></span>
<span data-ttu-id="f19c7-106">建立新的訂閱。</span><span class="sxs-lookup"><span data-stu-id="f19c7-106">Create a new subscription.</span></span>

## <span data-ttu-id="f19c7-107">示例</span><span class="sxs-lookup"><span data-stu-id="f19c7-107">EXAMPLES</span></span>

### <span data-ttu-id="f19c7-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f19c7-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsUserSubscription -Owner user@contoso.com -OfferId "/subscriptions/302d0fcd-5263-4f4d-82ba-383ad95a3e53/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/offers/offer1"
```

<span data-ttu-id="f19c7-109">建立新的使用者訂閱</span><span class="sxs-lookup"><span data-stu-id="f19c7-109">Creates a new user subscription</span></span>

## <span data-ttu-id="f19c7-110">參數</span><span class="sxs-lookup"><span data-stu-id="f19c7-110">PARAMETERS</span></span>

### <span data-ttu-id="f19c7-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f19c7-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="f19c7-112">父 DelegatedProvider 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f19c7-112">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19c7-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f19c7-113">-DisplayName</span></span>
<span data-ttu-id="f19c7-114">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="f19c7-114">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19c7-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="f19c7-115">-ExternalReferenceId</span></span>
<span data-ttu-id="f19c7-116">外部參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="f19c7-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19c7-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="f19c7-117">-OfferId</span></span>
<span data-ttu-id="f19c7-118">受委派提供者範圍內提供的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f19c7-118">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19c7-119">-擁有者</span><span class="sxs-lookup"><span data-stu-id="f19c7-119">-Owner</span></span>
<span data-ttu-id="f19c7-120">訂閱擁有者。</span><span class="sxs-lookup"><span data-stu-id="f19c7-120">Subscription owner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19c7-121">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="f19c7-121">-RoutingResourceManagerType</span></span>
<span data-ttu-id="f19c7-122">路由資源管理器類型。</span><span class="sxs-lookup"><span data-stu-id="f19c7-122">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19c7-123">-State</span><span class="sxs-lookup"><span data-stu-id="f19c7-123">-State</span></span>
<span data-ttu-id="f19c7-124">訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="f19c7-124">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19c7-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f19c7-125">-SubscriptionId</span></span>
<span data-ttu-id="f19c7-126">[訂閱識別碼]。</span><span class="sxs-lookup"><span data-stu-id="f19c7-126">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19c7-127">-TenantId</span><span class="sxs-lookup"><span data-stu-id="f19c7-127">-TenantId</span></span>
<span data-ttu-id="f19c7-128">目錄租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="f19c7-128">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19c7-129">-確認</span><span class="sxs-lookup"><span data-stu-id="f19c7-129">-Confirm</span></span>
<span data-ttu-id="f19c7-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f19c7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f19c7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f19c7-131">-WhatIf</span></span>
<span data-ttu-id="f19c7-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f19c7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f19c7-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f19c7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f19c7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f19c7-134">CommonParameters</span></span>
<span data-ttu-id="f19c7-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f19c7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f19c7-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f19c7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f19c7-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f19c7-137">INPUTS</span></span>

## <span data-ttu-id="f19c7-138">輸出</span><span class="sxs-lookup"><span data-stu-id="f19c7-138">OUTPUTS</span></span>

### <span data-ttu-id="f19c7-139">AzureStack. 系統管理. 訂閱</span><span class="sxs-lookup"><span data-stu-id="f19c7-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="f19c7-140">筆記</span><span class="sxs-lookup"><span data-stu-id="f19c7-140">NOTES</span></span>

## <span data-ttu-id="f19c7-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="f19c7-141">RELATED LINKS</span></span>
