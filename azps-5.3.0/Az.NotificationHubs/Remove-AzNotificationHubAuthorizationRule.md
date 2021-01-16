---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: d908d9d12e917efca6901c08bc69d4888072b6ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288615"
---
# <span data-ttu-id="59150-101">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="59150-101">Remove-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="59150-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59150-102">SYNOPSIS</span></span>
<span data-ttu-id="59150-103">從通知中樞移除授權規則。</span><span class="sxs-lookup"><span data-stu-id="59150-103">Removes an authorization rule from a notification hub.</span></span>

## <span data-ttu-id="59150-104">句法</span><span class="sxs-lookup"><span data-stu-id="59150-104">SYNTAX</span></span>

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59150-105">說明</span><span class="sxs-lookup"><span data-stu-id="59150-105">DESCRIPTION</span></span>
<span data-ttu-id="59150-106">**AzNotificationHubAuthorizationRule** Cmdlet 會從通知中樞中移除 (SAS) 授權規則的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="59150-106">The **Remove-AzNotificationHubAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="59150-107">授權規則會根據不同的許可權等級，透過建立連結（例如 Uri）來管理通知中樞的存取權。</span><span class="sxs-lookup"><span data-stu-id="59150-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="59150-108">許可權等級可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="59150-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="59150-109">聆聽</span><span class="sxs-lookup"><span data-stu-id="59150-109">Listen</span></span>
- <span data-ttu-id="59150-110">發送</span><span class="sxs-lookup"><span data-stu-id="59150-110">Send</span></span>
- <span data-ttu-id="59150-111">系統會根據適當的許可權等級，將管理用戶端導向到其中一個 Uri。</span><span class="sxs-lookup"><span data-stu-id="59150-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="59150-112">例如，擁有偵聽許可權的用戶端將會導向該許可權的 URI。</span><span class="sxs-lookup"><span data-stu-id="59150-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="59150-113">移除授權規則也會移除對應的使用者許可權。</span><span class="sxs-lookup"><span data-stu-id="59150-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="59150-114">示例</span><span class="sxs-lookup"><span data-stu-id="59150-114">EXAMPLES</span></span>

### <span data-ttu-id="59150-115">範例1：從通知中樞移除授權規則</span><span class="sxs-lookup"><span data-stu-id="59150-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="59150-116">這個命令會從名為 [ContosoExternalHub] 的通知中心中移除名為 ListenRule 的授權規則。</span><span class="sxs-lookup"><span data-stu-id="59150-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="59150-117">當您執行此命令時，您必須指定該中樞所指派的命名空間和資源群組。</span><span class="sxs-lookup"><span data-stu-id="59150-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="59150-118">參數</span><span class="sxs-lookup"><span data-stu-id="59150-118">PARAMETERS</span></span>

### <span data-ttu-id="59150-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="59150-119">-AuthorizationRule</span></span>
<span data-ttu-id="59150-120">指定此 Cmdlet 移除之 SAS 驗證規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="59150-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59150-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59150-121">-DefaultProfile</span></span>
<span data-ttu-id="59150-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="59150-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59150-123">-Force</span><span class="sxs-lookup"><span data-stu-id="59150-123">-Force</span></span>
<span data-ttu-id="59150-124">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="59150-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="59150-125">-命名空間</span><span class="sxs-lookup"><span data-stu-id="59150-125">-Namespace</span></span>
<span data-ttu-id="59150-126">指定通知中心指派給哪個命名空間。</span><span class="sxs-lookup"><span data-stu-id="59150-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="59150-127">命名空間提供一種群組和分類通知中樞的方式。</span><span class="sxs-lookup"><span data-stu-id="59150-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59150-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="59150-128">-NotificationHub</span></span>
<span data-ttu-id="59150-129">指定授權規則指派給哪個通知中樞。</span><span class="sxs-lookup"><span data-stu-id="59150-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="59150-130">通知中樞可用來傳送推播通知給多個用戶端，而不論平臺為何。</span><span class="sxs-lookup"><span data-stu-id="59150-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59150-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="59150-131">-ResourceGroup</span></span>
<span data-ttu-id="59150-132">指定通知中心指派給哪個資源群組。</span><span class="sxs-lookup"><span data-stu-id="59150-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="59150-133">資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。</span><span class="sxs-lookup"><span data-stu-id="59150-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59150-134">-確認</span><span class="sxs-lookup"><span data-stu-id="59150-134">-Confirm</span></span>
<span data-ttu-id="59150-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="59150-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59150-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59150-136">-WhatIf</span></span>
<span data-ttu-id="59150-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="59150-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59150-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="59150-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59150-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59150-139">CommonParameters</span></span>
<span data-ttu-id="59150-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59150-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59150-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="59150-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59150-142">輸入</span><span class="sxs-lookup"><span data-stu-id="59150-142">INPUTS</span></span>

### <span data-ttu-id="59150-143">System.object</span><span class="sxs-lookup"><span data-stu-id="59150-143">System.String</span></span>

## <span data-ttu-id="59150-144">輸出</span><span class="sxs-lookup"><span data-stu-id="59150-144">OUTPUTS</span></span>

### <span data-ttu-id="59150-145">System.void</span><span class="sxs-lookup"><span data-stu-id="59150-145">System.Void</span></span>

## <span data-ttu-id="59150-146">筆記</span><span class="sxs-lookup"><span data-stu-id="59150-146">NOTES</span></span>

## <span data-ttu-id="59150-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="59150-147">RELATED LINKS</span></span>

[<span data-ttu-id="59150-148">AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="59150-148">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="59150-149">新-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="59150-149">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="59150-150">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="59150-150">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)

