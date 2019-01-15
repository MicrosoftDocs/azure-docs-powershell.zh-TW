---
title: 使用 Azure PowerShell 登入
description: 如何使用 Azure PowerShell 以使用者身分登入、使用服務主體登入，或使用適用於 Azure 資源的受控識別登入。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 8b085720aeabe26c1293ece193e050b31f99a693
ms.sourcegitcommit: ae81b08a45d8729fc8d40156422e3eb2e94de8c7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/27/2018
ms.locfileid: "53786674"
---
# <a name="sign-in-with-azure-powershell"></a>使用 Azure PowerShell 登入

Azure PowerShell 支援數種驗證方法。 最簡單的入門方法是在命令列以互動方式登入。

## <a name="sign-in-interactively"></a>以互動方式登入

若要以互動方式登入，請使用 [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) Cmdlet。

```azurepowershell-interactive
Connect-AzAccount
```

執行時，此 Cmdlet 會出示權杖字串。 若要登入，請複製這個字串並將它貼至瀏覽器中的 https://microsoft.com/devicelogin。 PowerShell 工作階段接著會進行驗證以便連線至 Azure。 此驗證的效用限於目前的 PowerShell 工作階段。

> [!IMPORTANT]
>
> 只要您保持登入，認證就會在多個 PowerShell 工作階段之間共用。
> 如需詳細資訊，請參閱[持續性認證](context-persistence.md)中的文章。

## <a name="sign-in-with-a-service-principal"></a>使用服務主體來登入

服務主體為非互動式 Azure 帳戶。 如同其他使用者帳戶，其權限也受到 Azure Active Directory 的管理。 藉由僅為服務主體授與其所需的權限，您的自動化指令碼得以受到保護。

若要了解如何建立與 Azure PowerShell 搭配使用的服務主體，請參閱[使用 Azure PowerShell 建立 Azure 服務主體](create-azure-service-principal-azureps.md)。

若要使用服務主體來登入，請使用 `-ServicePrincipal` 引數和 `Connect-AzAccount` Cmdlet。 您也需要服務主體的應用程式識別碼、登入認證，以及與服務主體相關聯的租用戶識別碼。 若要取得服務主體的認證作為適當物件，請使用 [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) Cmdlet。 這個 Cmdlet 會顯示請您輸入服務主體使用者識別碼和密碼的提示。

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a>使用 Azure 受控服務識別登入

適用於 Azure 資源的受控識別是 Azure Active Directory 的一項功能。 您可以使用受控識別服務主體進行登入，並取得僅限應用程式的存取權杖來存取其他資源。 受控識別僅適用於在 Azure 雲端中執行的虛擬機器。

若想進一步了解適用於 Azure 資源的受控識別，請參閱[如何在 Azure VM 上使用適用於 Azure 資源的受控識別取得存取權杖](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token)。

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a>以雲端解決方案提供者 (CSP) 身分登入

[雲端解決方案提供者 (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) 登入需要使用 `-TenantId`。 一般來說，此參數可以提供作為租用戶識別碼或網域名稱。 不過，如果是 CSP 登入，則必須提供為**租用戶識別碼**。

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>登入其他雲端

Azure 雲端服務提供符合區域資料處理法規的環境。
針對區域雲端中的帳戶，使用 `-Environment` 引數設定您登入時的環境。
例如，如果您的帳戶位於中國雲端：

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

下列命令可取得可用環境的清單：

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>深入了解如何管理 Azure 角色型存取

如需 Azure 中的驗證與訂用帳戶管理的詳細資訊，請參閱[管理帳戶、訂用帳戶和管理角色](/azure/active-directory/role-based-access-control-configure)。

可用來管理角色的 Azure PowerShell Cmdlet：

* [Get-AzRoleAssignment](/powershell/module/az.Resources/Get-azRoleAssignment)
* [Get-AzRoleDefinition](/powershell/module/az.Resources/Get-azRoleDefinition)
* [New-AzRoleAssignment](/powershell/module/az.Resources/New-azRoleAssignment)
* [New-AzRoleDefinition](/powershell/module/az.Resources/New-azRoleDefinition)
* [Remove-AzRoleAssignment](/powershell/module/az.Resources/Remove-azRoleAssignment)
* [Remove-AzRoleDefinition](/powershell/module/az.Resources/Remove-azRoleDefinition)
* [Set-AzRoleDefinition](/powershell/module/az.Resources/Set-azRoleDefinition)