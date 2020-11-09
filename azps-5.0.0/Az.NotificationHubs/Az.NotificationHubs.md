---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: dd39a8f87120ea7aaddb4570276e1e3060873e2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287783"
---
# <span data-ttu-id="7f056-101">Az NotificationHubs 模組</span><span class="sxs-lookup"><span data-stu-id="7f056-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="7f056-102">說明</span><span class="sxs-lookup"><span data-stu-id="7f056-102">Description</span></span>
<span data-ttu-id="7f056-103">本主題顯示 Azure 通知中樞 Cmdlet 的說明主題。</span><span class="sxs-lookup"><span data-stu-id="7f056-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="7f056-104">通知中樞是用來傳送推播通知給多個用戶端，而不考慮平臺 (iOS、Android、Windows Phone 8、Windows 市集中等等。 ) 由這些用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="7f056-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="7f056-105">這些中樞大致相當於個別 app：您的每個應用程式通常都有自己的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="7f056-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="7f056-106">通知中心是組織在稱為命名空間的邏輯容器中，而共用存取簽章 (SAS) 授權規則是用來管理中樞和命名空間的存取權。</span><span class="sxs-lookup"><span data-stu-id="7f056-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="7f056-107">所有這些元素都可以使用通知中心 Cmdlet 來管理。</span><span class="sxs-lookup"><span data-stu-id="7f056-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="7f056-108">Az NotificationHubs Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7f056-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="7f056-109">AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7f056-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="7f056-110">取得通知中樞的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f056-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="7f056-111">AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7f056-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="7f056-112">取得與通知中樞相關聯之授權規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f056-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="7f056-113">AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="7f056-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="7f056-114">取得與通知中樞授權規則相關聯的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="7f056-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="7f056-115">AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="7f056-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="7f056-116">取得通知中樞的 PNS 認證。</span><span class="sxs-lookup"><span data-stu-id="7f056-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="7f056-117">AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7f056-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="7f056-118">取得通知中心命名空間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f056-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="7f056-119">AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7f056-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="7f056-120">取得與通知中心命名空間相關聯之授權規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f056-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="7f056-121">AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="7f056-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="7f056-122">取得與通知中心命名空間授權規則相關聯的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="7f056-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="7f056-123">新-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7f056-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="7f056-124">建立通知中樞。</span><span class="sxs-lookup"><span data-stu-id="7f056-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="7f056-125">新-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7f056-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="7f056-126">建立授權規則，並將規則指派給通知中樞。</span><span class="sxs-lookup"><span data-stu-id="7f056-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="7f056-127">新-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="7f056-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="7f056-128">重新產生 NotificationHub 的授權規則金鑰。</span><span class="sxs-lookup"><span data-stu-id="7f056-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="7f056-129">新-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7f056-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="7f056-130">建立通知中心命名空間。</span><span class="sxs-lookup"><span data-stu-id="7f056-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="7f056-131">新-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7f056-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="7f056-132">建立授權規則，並將該規則指派給通知中心命名空間。</span><span class="sxs-lookup"><span data-stu-id="7f056-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="7f056-133">新-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="7f056-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="7f056-134">重新產生命名空間的授權規則金鑰。</span><span class="sxs-lookup"><span data-stu-id="7f056-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="7f056-135">移除-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7f056-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="7f056-136">移除現有的通知中樞。</span><span class="sxs-lookup"><span data-stu-id="7f056-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="7f056-137">移除-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7f056-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="7f056-138">從通知中樞移除授權規則。</span><span class="sxs-lookup"><span data-stu-id="7f056-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="7f056-139">移除-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7f056-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="7f056-140">移除 [通知中心] 命名空間。</span><span class="sxs-lookup"><span data-stu-id="7f056-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="7f056-141">移除-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7f056-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="7f056-142">從通知中心命名空間移除授權規則。</span><span class="sxs-lookup"><span data-stu-id="7f056-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="7f056-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7f056-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="7f056-144">設定通知中樞的屬性值。</span><span class="sxs-lookup"><span data-stu-id="7f056-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="7f056-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7f056-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="7f056-146">設定通知中樞的授權規則。</span><span class="sxs-lookup"><span data-stu-id="7f056-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="7f056-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7f056-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="7f056-148">設定通知中心命名空間的屬性值。</span><span class="sxs-lookup"><span data-stu-id="7f056-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="7f056-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7f056-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="7f056-150">設定通知中心命名空間的授權規則。</span><span class="sxs-lookup"><span data-stu-id="7f056-150">Sets authorization rules for a notification hub namespace.</span></span>
