---
title: 透過 Azure PowerShell 使用 Azure 服務主體
description: 了解如何搭配 Azure PowerShell 來建立和使用服務主體。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.openlocfilehash: 4c47d2bac2c63f13ac0ebbccda3e2eed12cd658f
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/05/2020
ms.locfileid: "81445674"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="12e02-103">使用 Azure PowerShell 來建立 Azure 服務主體</span><span class="sxs-lookup"><span data-stu-id="12e02-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="12e02-104">使用 Azure 服務的自動化工具應一律具有權限限制。</span><span class="sxs-lookup"><span data-stu-id="12e02-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="12e02-105">Azure 提供的服務主體，可替代以具有完整權限的使用者身分登入應用程式。</span><span class="sxs-lookup"><span data-stu-id="12e02-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="12e02-106">Azure 服務主體是一種身分識別，建立目的是為了搭配應用程式、託管服務及自動化工具來存取 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="12e02-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="12e02-107">此存取會受限於指派給服務主體的角色，以便您控制可存取的資源，以及在哪個層級上存取。</span><span class="sxs-lookup"><span data-stu-id="12e02-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="12e02-108">基於安全理由，我們建議您一律搭配自動化工具使用服務主體，而不是讓服務主體透過使用者身分識別來登入。</span><span class="sxs-lookup"><span data-stu-id="12e02-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="12e02-109">本文會示範搭配 Azure PowerShell 建立服務主體，以及擷取其資訊和重設服務主體的步驟。</span><span class="sxs-lookup"><span data-stu-id="12e02-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="12e02-110">建立服務主體</span><span class="sxs-lookup"><span data-stu-id="12e02-110">Create a service principal</span></span>

<span data-ttu-id="12e02-111">使用 [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) Cmdlet 建立服務主體。</span><span class="sxs-lookup"><span data-stu-id="12e02-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="12e02-112">建立服務主體時，您可以選擇其所用的登入驗證類型。</span><span class="sxs-lookup"><span data-stu-id="12e02-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
>
> <span data-ttu-id="12e02-113">如果您的帳戶沒有建立服務主體的權限，`New-AzADServicePrincipal` 會傳回「權限不足，無法完成作業」的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="12e02-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="12e02-114">請連絡您的 Azure Active Directory 管理員，以建立服務主體。</span><span class="sxs-lookup"><span data-stu-id="12e02-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="12e02-115">有兩種驗證類型可用於服務主體：密碼式驗證和憑證式驗證。</span><span class="sxs-lookup"><span data-stu-id="12e02-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="12e02-116">密碼式驗證</span><span class="sxs-lookup"><span data-stu-id="12e02-116">Password-based authentication</span></span>

<span data-ttu-id="12e02-117">密碼式驗證沒有任何其他驗證參數，而是搭配使用為您建立的隨機密碼。</span><span class="sxs-lookup"><span data-stu-id="12e02-117">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="12e02-118">如果您想使用密碼式驗證，建議使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="12e02-118">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="12e02-119">傳回的物件包含 `Secret` 成員，其為包含所產生密碼的 `SecureString`。</span><span class="sxs-lookup"><span data-stu-id="12e02-119">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="12e02-120">請確定您將此值儲存在安全的位置，以便驗證服務主體。</span><span class="sxs-lookup"><span data-stu-id="12e02-120">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="12e02-121">該值__不會__顯示在主控台輸出。</span><span class="sxs-lookup"><span data-stu-id="12e02-121">Its value __won't__ be displayed in the console output.</span></span> <span data-ttu-id="12e02-122">如果您遺失密碼，[請重設服務主體認證](#reset-credentials)。</span><span class="sxs-lookup"><span data-stu-id="12e02-122">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="12e02-123">下列程式碼可讓您匯出祕密：</span><span class="sxs-lookup"><span data-stu-id="12e02-123">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="12e02-124">對於使用者提供的密碼，`-PasswordCredential` 引數會採用 `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` 物件。</span><span class="sxs-lookup"><span data-stu-id="12e02-124">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="12e02-125">這些物件必須具有有效的 `StartDate` 和 `EndDate`，並採取純文字 `Password`。</span><span class="sxs-lookup"><span data-stu-id="12e02-125">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="12e02-126">建立密碼時，請務必遵循 [Azure Active Directory 密碼規則和限制](/azure/active-directory/active-directory-passwords-policy)。</span><span class="sxs-lookup"><span data-stu-id="12e02-126">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="12e02-127">請勿使用弱式密碼或重複使用密碼。</span><span class="sxs-lookup"><span data-stu-id="12e02-127">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="12e02-128">從 `New-AzADServicePrincipal` 傳回的物件包含 `Id` 和 `DisplayName` 成員，兩者都可用於使用服務主體登入。</span><span class="sxs-lookup"><span data-stu-id="12e02-128">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="12e02-129">使用服務主體登入需要在其下建立服務主體的租用戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="12e02-129">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="12e02-130">若要在建立服務主體時取得作用中的租用戶，請在建立服務主體__之後立即__執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="12e02-130">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a><span data-ttu-id="12e02-131">憑證式驗證</span><span class="sxs-lookup"><span data-stu-id="12e02-131">Certificate-based authentication</span></span>

<span data-ttu-id="12e02-132">使用憑證式驗證的服務主體會使用 `-CertValue` 參數建立。</span><span class="sxs-lookup"><span data-stu-id="12e02-132">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="12e02-133">這個參數會採用公開憑證的 base64 編碼 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="12e02-133">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="12e02-134">這會以 PEM 檔案，或文字編碼 CRT 或 CER 表示。</span><span class="sxs-lookup"><span data-stu-id="12e02-134">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="12e02-135">不支援公開憑證的二進位編碼。</span><span class="sxs-lookup"><span data-stu-id="12e02-135">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="12e02-136">這些指示會假設您已經有可用的憑證。</span><span class="sxs-lookup"><span data-stu-id="12e02-136">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="12e02-137">您也可以使用 `-KeyCredential` 參數，其採用 `PSADKeyCredential` 物件。</span><span class="sxs-lookup"><span data-stu-id="12e02-137">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="12e02-138">這些物件必須具有有效的 `StartDate`、`EndDate`，而且 `CertValue` 成員設定為公開憑證的 base64 編碼 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="12e02-138">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="12e02-139">從 `New-AzADServicePrincipal` 傳回的物件包含 `Id` 和 `DisplayName` 成員，兩者都可用於使用服務主體登入。</span><span class="sxs-lookup"><span data-stu-id="12e02-139">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="12e02-140">使用服務主體登入的用戶端也需要存取憑證的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="12e02-140">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="12e02-141">使用服務主體登入需要在其下建立服務主體的租用戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="12e02-141">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="12e02-142">若要在建立服務主體時取得作用中的租用戶，請在建立服務主體__之後立即__執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="12e02-142">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="12e02-143">取得現有的服務主體</span><span class="sxs-lookup"><span data-stu-id="12e02-143">Get an existing service principal</span></span>

<span data-ttu-id="12e02-144">您可以使用 [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) 擷取目前作用中租用戶的服務主體清單。</span><span class="sxs-lookup"><span data-stu-id="12e02-144">A list of service principals for the currently active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="12e02-145">依預設，此命令會傳回租用戶中的__所有__服務主體，因此對於大型組織，可能需要長時間來傳回結果。</span><span class="sxs-lookup"><span data-stu-id="12e02-145">By default this command returns __all__ service principals in a tenant, so for large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="12e02-146">建議使用選擇性伺服器端篩選引數的其中一個：</span><span class="sxs-lookup"><span data-stu-id="12e02-146">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

* <span data-ttu-id="12e02-147">`-DisplayNameBeginsWith` 會要求服務主體的_前置詞_符合所提供的值。</span><span class="sxs-lookup"><span data-stu-id="12e02-147">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="12e02-148">服務主體的顯示名稱是建立期間使用 `-DisplayName` 所設定的值。</span><span class="sxs-lookup"><span data-stu-id="12e02-148">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
* <span data-ttu-id="12e02-149">`-DisplayName` 要求服務主體名稱_完全相符_。</span><span class="sxs-lookup"><span data-stu-id="12e02-149">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="12e02-150">管理服務主體角色</span><span class="sxs-lookup"><span data-stu-id="12e02-150">Manage service principal roles</span></span>

<span data-ttu-id="12e02-151">Azure PowerShell 提供下列 Cmdlet 以供您管理角色指派：</span><span class="sxs-lookup"><span data-stu-id="12e02-151">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="12e02-152">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="12e02-152">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="12e02-153">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="12e02-153">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="12e02-154">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="12e02-154">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="12e02-155">服務主體的預設角色是**參與者**。</span><span class="sxs-lookup"><span data-stu-id="12e02-155">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="12e02-156">此角色具有讀取和寫入至 Azure 帳戶的完整權限。</span><span class="sxs-lookup"><span data-stu-id="12e02-156">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="12e02-157">**讀者**角色的權限較為侷限，僅有唯讀存取權。</span><span class="sxs-lookup"><span data-stu-id="12e02-157">The **Reader** role is more restrictive, with read-only access.</span></span>  <span data-ttu-id="12e02-158">如需角色型存取控制 (RBAC) 和角色的詳細資訊，請參閱 [RBAC：內建角色](/azure/active-directory/role-based-access-built-in-roles)。</span><span class="sxs-lookup"><span data-stu-id="12e02-158">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="12e02-159">此範例會新增**讀者**角色，並移除**參與者**角色：</span><span class="sxs-lookup"><span data-stu-id="12e02-159">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> <span data-ttu-id="12e02-160">角色指派 Cmdlet 不需要服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="12e02-160">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="12e02-161">該 Cmdlet 需要在建立時所產生的相關聯應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="12e02-161">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="12e02-162">若要取得服務主體的應用程式識別碼，請使用 `Get-AzADServicePrincipal`。</span><span class="sxs-lookup"><span data-stu-id="12e02-162">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="12e02-163">如果您的帳戶沒有足夠權限可指派角色，您會看到錯誤訊息，這表示您的帳戶「沒有執行 'Microsoft.Authorization/roleAssignments/write' 動作的權限」。請連絡您的 Azure Active Directory 管理員，以管理角色。</span><span class="sxs-lookup"><span data-stu-id="12e02-163">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'." Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="12e02-164">新增角色「不會」  限制之前指派的權限。</span><span class="sxs-lookup"><span data-stu-id="12e02-164">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="12e02-165">限制服務主體的權限時，應移除「參與者」  角色。</span><span class="sxs-lookup"><span data-stu-id="12e02-165">When restricting a service principal's permissions, the __Contributor__ role should be removed.</span></span>

<span data-ttu-id="12e02-166">列出指派的角色可以驗證變更：</span><span class="sxs-lookup"><span data-stu-id="12e02-166">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="12e02-167">使用服務主體來登入</span><span class="sxs-lookup"><span data-stu-id="12e02-167">Sign in using a service principal</span></span>

<span data-ttu-id="12e02-168">藉由登入來測試新服務主體的認證和權限。</span><span class="sxs-lookup"><span data-stu-id="12e02-168">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="12e02-169">若要使用服務主體登入，您需要相關聯的 `applicationId` 值，以及在其下建立的租用戶。</span><span class="sxs-lookup"><span data-stu-id="12e02-169">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="12e02-170">透過服務主體來使用密碼登入：</span><span class="sxs-lookup"><span data-stu-id="12e02-170">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

<span data-ttu-id="12e02-171">憑證式驗證要求 Azure PowerShell 可從以憑證指紋為基礎的本機憑證存放區擷取資訊。</span><span class="sxs-lookup"><span data-stu-id="12e02-171">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="12e02-172">如需將憑證匯入 PowerShell 可存取的認證存放區指示，請參閱[使用 Azure PowerShell 登入](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="12e02-172">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="12e02-173">重設認證</span><span class="sxs-lookup"><span data-stu-id="12e02-173">Reset credentials</span></span>

<span data-ttu-id="12e02-174">如果您忘記服務主體的認證，請使用 [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) 新增認證。</span><span class="sxs-lookup"><span data-stu-id="12e02-174">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential.</span></span> <span data-ttu-id="12e02-175">此 Cmdlet 會採用與 `New-AzADServicePrincipal` 相同的認證引數和類型。</span><span class="sxs-lookup"><span data-stu-id="12e02-175">This cmdlet takes the same credential arguments and types as `New-AzADServicePrincipal`.</span></span> <span data-ttu-id="12e02-176">會建立新的 `PasswordCredential` 搭配隨機密碼，且不具任何認證引數。</span><span class="sxs-lookup"><span data-stu-id="12e02-176">Without any credential arguments, a new `PasswordCredential` with a random password is created.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12e02-177">在指派任何新認證之前，您需要移除現有的認證，以避免使用這些認證登入。</span><span class="sxs-lookup"><span data-stu-id="12e02-177">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="12e02-178">若要這樣做，請使用 [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="12e02-178">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```