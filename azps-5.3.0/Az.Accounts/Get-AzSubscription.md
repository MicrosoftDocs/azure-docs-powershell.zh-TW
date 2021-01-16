---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
ms.openlocfilehash: aecdd4a0b5f0ef4465f08441841fb923a273afdf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447788"
---
# <span data-ttu-id="5f6c1-101">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="5f6c1-101">Get-AzSubscription</span></span>

## <span data-ttu-id="5f6c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f6c1-102">SYNOPSIS</span></span>
<span data-ttu-id="5f6c1-103">取得目前帳戶可以存取的訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f6c1-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="5f6c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f6c1-104">SYNTAX</span></span>

### <span data-ttu-id="5f6c1-105">ListByIdInTenant (預設) </span><span class="sxs-lookup"><span data-stu-id="5f6c1-105">ListByIdInTenant (Default)</span></span>
```
Get-AzSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f6c1-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="5f6c1-106">ListByNameInTenant</span></span>
```
Get-AzSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f6c1-107">說明</span><span class="sxs-lookup"><span data-stu-id="5f6c1-107">DESCRIPTION</span></span>
<span data-ttu-id="5f6c1-108">Get-AzSubscription Cmdlet 會取得目前帳戶可存取之訂閱的訂閱識別碼、訂閱名稱及家用租使用者。</span><span class="sxs-lookup"><span data-stu-id="5f6c1-108">The Get-AzSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="5f6c1-109">示例</span><span class="sxs-lookup"><span data-stu-id="5f6c1-109">EXAMPLES</span></span>

### <span data-ttu-id="5f6c1-110">範例1：取得所有承租人中的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="5f6c1-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="5f6c1-111">這個命令會取得所有針對目前帳戶授權的租使用者的訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f6c1-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="5f6c1-112">範例2：取得特定租使用者的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="5f6c1-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzSubscription -TenantId "aaaa-aaaa-aaaa-aaaa"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="5f6c1-113">列出已針對目前帳戶授權的指定租使用者中的所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f6c1-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="5f6c1-114">範例3：取得目前租使用者中的所有訂閱</span><span class="sxs-lookup"><span data-stu-id="5f6c1-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="5f6c1-115">這個命令會在目前的租使用者中取得目前已授權的所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f6c1-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="5f6c1-116">範例4：變更目前的內容以使用特定的訂閱</span><span class="sxs-lookup"><span data-stu-id="5f6c1-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="5f6c1-117">這個命令會取得指定的訂閱，然後設定目前的內容來使用它。</span><span class="sxs-lookup"><span data-stu-id="5f6c1-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="5f6c1-118">此會話中的所有後續 Cmdlet 都會預設使用 (Contoso 訂閱 1) 的新訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f6c1-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="5f6c1-119">參數</span><span class="sxs-lookup"><span data-stu-id="5f6c1-119">PARAMETERS</span></span>

### <span data-ttu-id="5f6c1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f6c1-120">-AsJob</span></span>
<span data-ttu-id="5f6c1-121">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="5f6c1-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5f6c1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f6c1-122">-DefaultProfile</span></span>
<span data-ttu-id="5f6c1-123">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="5f6c1-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f6c1-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f6c1-124">-SubscriptionId</span></span>
<span data-ttu-id="5f6c1-125">指定要取得的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f6c1-125">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByIdInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6c1-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="5f6c1-126">-SubscriptionName</span></span>
<span data-ttu-id="5f6c1-127">指定要取得的訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="5f6c1-127">Specifies the name of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByNameInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6c1-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="5f6c1-128">-TenantId</span></span>
<span data-ttu-id="5f6c1-129">指定包含要取得之訂閱的租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f6c1-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f6c1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f6c1-130">CommonParameters</span></span>
<span data-ttu-id="5f6c1-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f6c1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f6c1-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5f6c1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f6c1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="5f6c1-133">INPUTS</span></span>

### <span data-ttu-id="5f6c1-134">System.object</span><span class="sxs-lookup"><span data-stu-id="5f6c1-134">System.String</span></span>

## <span data-ttu-id="5f6c1-135">輸出</span><span class="sxs-lookup"><span data-stu-id="5f6c1-135">OUTPUTS</span></span>

### <span data-ttu-id="5f6c1-136">PSAzureSubscription 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="5f6c1-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="5f6c1-137">筆記</span><span class="sxs-lookup"><span data-stu-id="5f6c1-137">NOTES</span></span>

## <span data-ttu-id="5f6c1-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f6c1-138">RELATED LINKS</span></span>