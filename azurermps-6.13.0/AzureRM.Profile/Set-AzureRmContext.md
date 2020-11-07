---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
ms.openlocfilehash: 42c7e2b632b175ef12f34e04ff682020d634ef74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624583"
---
# <span data-ttu-id="98242-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="98242-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="98242-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98242-102">SYNOPSIS</span></span>
<span data-ttu-id="98242-103">設定要在目前會話中使用之 Cmdlet 的租使用者、訂閱及環境。</span><span class="sxs-lookup"><span data-stu-id="98242-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98242-104">句法</span><span class="sxs-lookup"><span data-stu-id="98242-104">SYNTAX</span></span>

### <span data-ttu-id="98242-105">預設) 的內容 (</span><span class="sxs-lookup"><span data-stu-id="98242-105">Context (Default)</span></span>
```
Set-AzureRmContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98242-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="98242-106">TenantObject</span></span>
```
Set-AzureRmContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98242-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="98242-107">SubscriptionObject</span></span>
```
Set-AzureRmContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98242-108">訂閱</span><span class="sxs-lookup"><span data-stu-id="98242-108">Subscription</span></span>
```
Set-AzureRmContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98242-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="98242-109">TenantNameOnly</span></span>
```
Set-AzureRmContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98242-110">說明</span><span class="sxs-lookup"><span data-stu-id="98242-110">DESCRIPTION</span></span>
<span data-ttu-id="98242-111">Set-AzureRmContext Cmdlet 會針對您在目前會話中執行的 Cmdlet 設定驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="98242-111">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="98242-112">內容包括租使用者、訂閱及環境資訊。</span><span class="sxs-lookup"><span data-stu-id="98242-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="98242-113">示例</span><span class="sxs-lookup"><span data-stu-id="98242-113">EXAMPLES</span></span>

### <span data-ttu-id="98242-114">範例1：設定訂閱內容</span><span class="sxs-lookup"><span data-stu-id="98242-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="98242-115">這個命令會將內容設定為使用指定的訂閱。</span><span class="sxs-lookup"><span data-stu-id="98242-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="98242-116">參數</span><span class="sxs-lookup"><span data-stu-id="98242-116">PARAMETERS</span></span>

### <span data-ttu-id="98242-117">-內容</span><span class="sxs-lookup"><span data-stu-id="98242-117">-Context</span></span>
<span data-ttu-id="98242-118">指定目前會話的內容。</span><span class="sxs-lookup"><span data-stu-id="98242-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Context
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98242-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98242-119">-DefaultProfile</span></span>
<span data-ttu-id="98242-120">用於與 azure 進行通訊的認證、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="98242-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98242-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="98242-121">-ExtendedProperty</span></span>
<span data-ttu-id="98242-122">其他內容屬性</span><span class="sxs-lookup"><span data-stu-id="98242-122">Additional context properties</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98242-123">-Force</span><span class="sxs-lookup"><span data-stu-id="98242-123">-Force</span></span>
<span data-ttu-id="98242-124">使用相同的名稱覆寫現有的內容（如果有）。</span><span class="sxs-lookup"><span data-stu-id="98242-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="98242-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="98242-125">-Name</span></span>
<span data-ttu-id="98242-126">內容的名稱</span><span class="sxs-lookup"><span data-stu-id="98242-126">Name of the context</span></span>

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

### <span data-ttu-id="98242-127">-範圍</span><span class="sxs-lookup"><span data-stu-id="98242-127">-Scope</span></span>
<span data-ttu-id="98242-128">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="98242-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98242-129">-訂閱</span><span class="sxs-lookup"><span data-stu-id="98242-129">-Subscription</span></span>
<span data-ttu-id="98242-130">應將內容設定為之訂閱的名稱或識別碼。</span><span class="sxs-lookup"><span data-stu-id="98242-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="98242-131">這個參數具有-SubscriptionName 和-SubscriptionId 的別名，所以為了清楚起見，您可以在分別指定名稱和識別碼時，使用其中一種方式，而不是訂閱。</span><span class="sxs-lookup"><span data-stu-id="98242-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98242-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="98242-132">-SubscriptionObject</span></span>
<span data-ttu-id="98242-133">訂閱物件</span><span class="sxs-lookup"><span data-stu-id="98242-133">A subscription object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98242-134">-租使用者</span><span class="sxs-lookup"><span data-stu-id="98242-134">-Tenant</span></span>
<span data-ttu-id="98242-135">租使用者名稱或識別碼</span><span class="sxs-lookup"><span data-stu-id="98242-135">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98242-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="98242-136">-TenantObject</span></span>
<span data-ttu-id="98242-137">租使用者物件</span><span class="sxs-lookup"><span data-stu-id="98242-137">A Tenant Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureTenant
Parameter Sets: TenantObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98242-138">-確認</span><span class="sxs-lookup"><span data-stu-id="98242-138">-Confirm</span></span>
<span data-ttu-id="98242-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="98242-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98242-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98242-140">-WhatIf</span></span>
<span data-ttu-id="98242-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98242-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98242-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98242-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98242-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98242-143">CommonParameters</span></span>
<span data-ttu-id="98242-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98242-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98242-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="98242-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98242-146">輸入</span><span class="sxs-lookup"><span data-stu-id="98242-146">INPUTS</span></span>

### <span data-ttu-id="98242-147">PSAzureCoNtext 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="98242-147">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="98242-148">參數：內容 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="98242-148">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="98242-149">PSAzureTenant 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="98242-149">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>
<span data-ttu-id="98242-150">參數： TenantObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="98242-150">Parameters: TenantObject (ByValue)</span></span>

### <span data-ttu-id="98242-151">PSAzureSubscription 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="98242-151">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>
<span data-ttu-id="98242-152">參數： SubscriptionObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="98242-152">Parameters: SubscriptionObject (ByValue)</span></span>

## <span data-ttu-id="98242-153">輸出</span><span class="sxs-lookup"><span data-stu-id="98242-153">OUTPUTS</span></span>

### <span data-ttu-id="98242-154">PSAzureCoNtext 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="98242-154">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="98242-155">筆記</span><span class="sxs-lookup"><span data-stu-id="98242-155">NOTES</span></span>

## <span data-ttu-id="98242-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="98242-156">RELATED LINKS</span></span>

[<span data-ttu-id="98242-157">AzureRMCoNtext</span><span class="sxs-lookup"><span data-stu-id="98242-157">Get-AzureRMContext</span></span>](./Get-AzureRMContext.md)
