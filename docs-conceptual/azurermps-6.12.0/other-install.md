---
title: Azure PowerShell 的其他安裝方式
description: 如何使用 MSI，但不使用 PowerShellGet 來安裝 Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 9fa5790e0a2aca4f933b40256634f772c258b189
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/07/2018
ms.locfileid: "51212619"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="a2369-103">使用 MSI 在 Windows 上安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a2369-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="a2369-104">本文說明如何使用 MSI 安裝程式在 Windows 上安裝 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="a2369-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span>  
<span data-ttu-id="a2369-105">只有在您的系統需要時才使用這些安裝方法。</span><span class="sxs-lookup"><span data-stu-id="a2369-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="a2369-106">在 Windows 上安裝 Azure PowerShell 的建議方法是使用 PowerShellGet。</span><span class="sxs-lookup"><span data-stu-id="a2369-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="a2369-107">如需使用 PowerShellGet 安裝 Azure PowerShell 的指示，請參閱[使用 PowerShellGet 安裝 Azure PowerShell](install-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="a2369-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a2369-108">Azure PowerShell 6.x 版和更高版本無法再使用 Web Platform Installer 的安裝方法。</span><span class="sxs-lookup"><span data-stu-id="a2369-108">The Web Platform Installer method of installation is no longer available for versions of Azure PowerShell 6.x and higher.</span></span> <span data-ttu-id="a2369-109">如果您需要使用 Web Platform Installer，請考慮改用 MSI，或可安裝舊版的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="a2369-109">If you require use of the Web Platform Installer please consider using the MSI instead, or you can install an earlier version of Azure PowerShell.</span></span>

<span data-ttu-id="a2369-110">若要在 Linux 或 macOS 環境上安裝，請參閱[在 macOS 或 Linux 上安裝 Azure PowerShell](install-azurermps-maclinux.md)。</span><span class="sxs-lookup"><span data-stu-id="a2369-110">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="a2369-111">使用 MSI 套件在 Windows 上安裝或更新</span><span class="sxs-lookup"><span data-stu-id="a2369-111">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="a2369-112">您可以使用 MSI 檔案 (可從 [GitHub](https://github.com/Azure/azure-powershell/releases/latest) 取得) 來安裝 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="a2369-112">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="a2369-113">如果您已利用 MSI 身分安裝舊版的 Azure 模組，安裝程式會自動移除這些模組。</span><span class="sxs-lookup"><span data-stu-id="a2369-113">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="a2369-114">MSI 套件會在 `${env:ProgramFiles}\WindowsPowerShell\Modules` 中安裝模組。</span><span class="sxs-lookup"><span data-stu-id="a2369-114">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="a2369-115">`AzureRM` 和 `Azure` 模組都已安裝。</span><span class="sxs-lookup"><span data-stu-id="a2369-115">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="a2369-116">僅在您使用 Azure 傳統部署模型時，才使用 `Azure` 模組。</span><span class="sxs-lookup"><span data-stu-id="a2369-116">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="a2369-117">若要開始使用 Azure PowerShell，您必須使用 [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) Cmdlet 將 `AzureRM` 載入您目前的 PowerShell 工作階段，然後使用您的 Azure 認證登入。</span><span class="sxs-lookup"><span data-stu-id="a2369-117">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="a2369-118">您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。</span><span class="sxs-lookup"><span data-stu-id="a2369-118">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="a2369-119">自動匯入 `AzureRM` 模組需要設定 PowerShell 設定檔，您可以在[關於設定檔](/powershell/module/microsoft.powershell.core/about/about_profiles)中加以了解。</span><span class="sxs-lookup"><span data-stu-id="a2369-119">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="a2369-120">若要了解如何在工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="a2369-120">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>