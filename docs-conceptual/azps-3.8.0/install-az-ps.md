---
title: 使用 PowerShellGet 安裝 Azure PowerShell
description: 如何使用 PowerShellGet 安裝 Azure PowerShell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/26/2020
ms.openlocfilehash: 7a25270566f5e856ee44c4c191a47a3e7334508b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740247"
---
# <a name="install-azure-powershell"></a><span data-ttu-id="89f8c-103">安裝 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="89f8c-103">Install Azure PowerShell</span></span>

<span data-ttu-id="89f8c-104">本文說明如何使用 PowerShellGet 安裝 Azure PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="89f8c-104">This article explains how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="89f8c-105">這些指示適用於 Windows、macOS 和 Linux 平台。</span><span class="sxs-lookup"><span data-stu-id="89f8c-105">These instructions work on Windows, macOS, and Linux platforms.</span></span>

<span data-ttu-id="89f8c-106">Azure PowerShell 也可在 Azure [Cloud Shell](/azure/cloud-shell/overview) 取得，且現在已預先安裝在 [Docker 映像](azureps-in-docker.md)中。</span><span class="sxs-lookup"><span data-stu-id="89f8c-106">Azure PowerShell is also available in Azure [Cloud Shell](/azure/cloud-shell/overview) and is now preinstalled in [Docker images](azureps-in-docker.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89f8c-107">需求</span><span class="sxs-lookup"><span data-stu-id="89f8c-107">Requirements</span></span>

<span data-ttu-id="89f8c-108">Azure PowerShell 可在 Windows 上與 PowerShell 5.1 或更新版本搭配運作，或在所有平台上與 PowerShell Core 6.x 和更新版本搭配運作。</span><span class="sxs-lookup"><span data-stu-id="89f8c-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="89f8c-109">您應為您的作業系統安裝可使用的[最新版 PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core)。</span><span class="sxs-lookup"><span data-stu-id="89f8c-109">You should install the [latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core) available for your operating system.</span></span> <span data-ttu-id="89f8c-110">在 PowerShell Core 上執行時，Azure PowerShell 沒有額外的需求。</span><span class="sxs-lookup"><span data-stu-id="89f8c-110">Azure PowerShell has no additional requirements when run on PowerShell Core.</span></span>

<span data-ttu-id="89f8c-111">若要檢查 PowerShell 版本，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="89f8c-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="89f8c-112">在 Windows 上的 PowerShell 5.1 中使用 Azure PowerShell：</span><span class="sxs-lookup"><span data-stu-id="89f8c-112">To use Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="89f8c-113">視需要更新至 [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell)。</span><span class="sxs-lookup"><span data-stu-id="89f8c-113">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="89f8c-114">如果您是在 Windows 10 上，則已安裝 PowerShell 5.1。</span><span class="sxs-lookup"><span data-stu-id="89f8c-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="89f8c-115">安裝 [.NET Framework 4.7.2 或更新版本](/dotnet/framework/install)。</span><span class="sxs-lookup"><span data-stu-id="89f8c-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>
3. <span data-ttu-id="89f8c-116">確定您有最新版的 PowerShellGet。</span><span class="sxs-lookup"><span data-stu-id="89f8c-116">Make sure you have the latest version of PowerShellGet.</span></span> <span data-ttu-id="89f8c-117">執行 `Update-Module PowerShellGet -Force`。</span><span class="sxs-lookup"><span data-stu-id="89f8c-117">Run `Update-Module PowerShellGet -Force`.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="89f8c-118">安裝 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="89f8c-118">Install the Azure PowerShell module</span></span>

<span data-ttu-id="89f8c-119">使用 PowerShellGet Cmdlet 是慣用的安裝方法。</span><span class="sxs-lookup"><span data-stu-id="89f8c-119">Using the PowerShellGet cmdlets is the preferred installation method.</span></span> <span data-ttu-id="89f8c-120">這個方法在 Windows、macOS、Linux 平台上的做法相同。</span><span class="sxs-lookup"><span data-stu-id="89f8c-120">This method works the same on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="89f8c-121">從 PowerShell 工作階段執行下列命令︰</span><span class="sxs-lookup"><span data-stu-id="89f8c-121">Run the following command from a PowerShell session:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="89f8c-122">根據預設，PowerShell 資源庫未設為 PowerShellGet 的信任存放庫。</span><span class="sxs-lookup"><span data-stu-id="89f8c-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="89f8c-123">第一次使用 PSGallery 時，您會看到下列提示：</span><span class="sxs-lookup"><span data-stu-id="89f8c-123">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="89f8c-124">請回答 `Yes` 或 `Yes to All` 以繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="89f8c-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="89f8c-125">Az 模組是 Azure PowerShell Cmdlet 的彙總套件模組。</span><span class="sxs-lookup"><span data-stu-id="89f8c-125">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="89f8c-126">安裝此項目會下載所有可用的 Azure Resource Manager 模組，並使這些模組的 Cmdlet 可供使用。</span><span class="sxs-lookup"><span data-stu-id="89f8c-126">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

> [!WARNING]
> <span data-ttu-id="89f8c-127">我們不支援同時為 PowerShell 5.1 for Windows 安裝 AzureRM 和 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="89f8c-127">We do not support having both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="89f8c-128">如果您需要在系統上保留可用的 AzureRM，請安裝適用於 PowerShell Core 6.x 或更新版本的 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="89f8c-128">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span>

<span data-ttu-id="89f8c-129">首先，[下載 PowerShell Core 6.x 或更新版本](/powershell/scripting/install/installing-powershell-core-on-windows)。</span><span class="sxs-lookup"><span data-stu-id="89f8c-129">First, [install PowerShell Core 6.x or later](/powershell/scripting/install/installing-powershell-core-on-windows)</span></span>

<span data-ttu-id="89f8c-130">然後，從 PowerShell Core 工作階段中，只為目前使用安裝 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="89f8c-130">Then, from a PowerShell Core session, install the Az module for the current user only.</span></span> <span data-ttu-id="89f8c-131">這是建議的安裝範圍。</span><span class="sxs-lookup"><span data-stu-id="89f8c-131">This is the recommended installation scope.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="89f8c-132">為系統上的所有使用者安裝模組需要較高的權限。</span><span class="sxs-lookup"><span data-stu-id="89f8c-132">Installing the module for all users on a system requires elevated privileges.</span></span> <span data-ttu-id="89f8c-133">在 Windows 中使用 **Run as administrator**，在 macOS 或 Linux 上使用 `sudo` 命令，以啟動 PowerShell 工作階段：</span><span class="sxs-lookup"><span data-stu-id="89f8c-133">Start the PowerShell session using **Run as administrator** in Windows or use the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

## <a name="install-offline"></a><span data-ttu-id="89f8c-134">離線安裝</span><span class="sxs-lookup"><span data-stu-id="89f8c-134">Install offline</span></span>

<span data-ttu-id="89f8c-135">在某些環境中，無法連線到 PowerShell 資源庫。</span><span class="sxs-lookup"><span data-stu-id="89f8c-135">In some environments it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="89f8c-136">在這些情況下，您仍然可以使用下列其中一種方法來離線安裝：</span><span class="sxs-lookup"><span data-stu-id="89f8c-136">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="89f8c-137">將模組下載到您網路中的另一個位置，並使用該位置做為安裝來源。</span><span class="sxs-lookup"><span data-stu-id="89f8c-137">Download the modules to another location in your network and use that as an installation source.</span></span>
  <span data-ttu-id="89f8c-138">這可讓您將單一伺服器或檔案共用上的 PowerShell 模組 (已使用 PowerShellGet 部署) 快取到任何已中斷連線的系統上。</span><span class="sxs-lookup"><span data-stu-id="89f8c-138">This allows you to cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="89f8c-139">了解如何透過[使用本機 PowerShellGet 存放庫](/powershell/scripting/gallery/how-to/working-with-local-psrepositories)設定本機存放庫，並安裝在中斷連線的系統上。</span><span class="sxs-lookup"><span data-stu-id="89f8c-139">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="89f8c-140">[將 Azure PowerShell MSI 下載到連線至網路的電腦](install-az-ps-msi.md)，然後將安裝程式複製到系統，無需存取 PowerShell 資源庫。</span><span class="sxs-lookup"><span data-stu-id="89f8c-140">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="89f8c-141">請記住，MSI 安裝程式僅適用於 Windows 上的 PowerShell 5.1。</span><span class="sxs-lookup"><span data-stu-id="89f8c-141">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="89f8c-142">使用 [Save-Module](/powershell/module/PowershellGet/Save-Module) 將模組儲存至檔案共用，或將儲存至另一個來源，並手動將模組複製到其他電腦：</span><span class="sxs-lookup"><span data-stu-id="89f8c-142">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="89f8c-143">疑難排解</span><span class="sxs-lookup"><span data-stu-id="89f8c-143">Troubleshooting</span></span>

<span data-ttu-id="89f8c-144">以下是安裝 Azure PowerShell 模組時常見的一些問題。</span><span class="sxs-lookup"><span data-stu-id="89f8c-144">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="89f8c-145">如果您遇到此處未列出的問題，請[在 GitHub 上提出問題](https://github.com/azure/azure-powershell/issues)。</span><span class="sxs-lookup"><span data-stu-id="89f8c-145">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="89f8c-146">Proxy 封鎖連線</span><span class="sxs-lookup"><span data-stu-id="89f8c-146">Proxy blocks connection</span></span>

<span data-ttu-id="89f8c-147">如果 `Install-Module` 顯示錯誤指出無法連線到 PowerShell 資源庫，表示您可能在 Proxy 後方。</span><span class="sxs-lookup"><span data-stu-id="89f8c-147">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="89f8c-148">不同的作業系統和網路環境在設定全系統的 Proxy 時會有不同的需求。</span><span class="sxs-lookup"><span data-stu-id="89f8c-148">Different operating systems and network environment have different requirements for configuring a system-wide proxy.</span></span> <span data-ttu-id="89f8c-149">請連絡系統管理員以取得您的 Proxy 設定，並詢問如何為您的作業系統進行其設定。</span><span class="sxs-lookup"><span data-stu-id="89f8c-149">Contact your system administrator for your proxy settings and how to configure them for your environment.</span></span>

<span data-ttu-id="89f8c-150">PowerShell 本身不一定會設定為自動使用此 Proxy。</span><span class="sxs-lookup"><span data-stu-id="89f8c-150">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="89f8c-151">使用 PowerShell 5.1 和更新版本，並使用下列命令，將 PowerShell 工作階段設定為使用 Proxy：</span><span class="sxs-lookup"><span data-stu-id="89f8c-151">With PowerShell 5.1 and later, configure the PowerShell session to use a proxy using the following commands:</span></span>

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="89f8c-152">如果您的作業系統認證已正確設定，此設定將會透過 Proxy 路由傳送 PowerShell 要求。</span><span class="sxs-lookup"><span data-stu-id="89f8c-152">If your operating system credentials are configured correctly, this configuration routes PowerShell requests through the proxy.</span></span> <span data-ttu-id="89f8c-153">若要在工作階段之間保存此設定，請將命令新增至您的 [PowerShell 設定檔](/powershell/module/microsoft.powershell.core/about/about_profiles)。</span><span class="sxs-lookup"><span data-stu-id="89f8c-153">To have this setting persist between sessions, add the commands to your [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="89f8c-154">若要安裝此套件，您的 Proxy 必須允許下列位址的 HTTPS 連線：</span><span class="sxs-lookup"><span data-stu-id="89f8c-154">To install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="89f8c-155">登入</span><span class="sxs-lookup"><span data-stu-id="89f8c-155">Sign in</span></span>

<span data-ttu-id="89f8c-156">若要開始使用 Azure PowerShell，請使用您的 Azure 認證登入。</span><span class="sxs-lookup"><span data-stu-id="89f8c-156">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="89f8c-157">如果您已停用自動載入模組功能，則必須透過 `Import-Module Az` 手動匯入模組。</span><span class="sxs-lookup"><span data-stu-id="89f8c-157">If you've disabled module autoloading, manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="89f8c-158">因為模組的結構化方式，這可能需要幾秒鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="89f8c-158">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="89f8c-159">您必須針對每個啟動的新 PowerShell 工作階段重複這些步驟。</span><span class="sxs-lookup"><span data-stu-id="89f8c-159">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="89f8c-160">若要了解如何在 PowerShell 工作階段之間保存您的 Azure 登入，請參閱[在 PowerShell 工作階段之間保存使用者認證](context-persistence.md)。</span><span class="sxs-lookup"><span data-stu-id="89f8c-160">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="89f8c-161">更新 Azure PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="89f8c-161">Update the Azure PowerShell module</span></span>

<span data-ttu-id="89f8c-162">若要更新任何 PowerShell 模組，您應該使用先前安裝該模組的相同方法。</span><span class="sxs-lookup"><span data-stu-id="89f8c-162">To update any PowerShell module, you should use the same method used to install the module.</span></span> <span data-ttu-id="89f8c-163">例如，如果您最初是使用 `Install-Module`，則應該使用 [Update-Module](/powershell/module/powershellget/update-module) 來取得最新版本。</span><span class="sxs-lookup"><span data-stu-id="89f8c-163">For example, if you originally used `Install-Module`, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="89f8c-164">如果您最初使用的是 MSI 套件，則應該下載並安裝新的 MSI 套件。</span><span class="sxs-lookup"><span data-stu-id="89f8c-164">If you originally used the MSI package then you should download and install the new MSI package.</span></span>

<span data-ttu-id="89f8c-165">PowerShellGet Cmdlet 無法更新從 MSI 套件安裝的模組。</span><span class="sxs-lookup"><span data-stu-id="89f8c-165">The PowerShellGet cmdlets cannot update modules that were installed from an MSI package.</span></span> <span data-ttu-id="89f8c-166">MSI 套件不會更新使用 PowerShellGet 安裝的模組。</span><span class="sxs-lookup"><span data-stu-id="89f8c-166">MSI packages do not update modules that were installed using PowerShellGet.</span></span> <span data-ttu-id="89f8c-167">如果您有任何使用 PowershellGet 進行更新的問題，請**重新安裝**，不要只是**更新**。</span><span class="sxs-lookup"><span data-stu-id="89f8c-167">If you have any issues updating using PowershellGet then you should **reinstall**, rather than **update**.</span></span> <span data-ttu-id="89f8c-168">重新安裝的操作方式與安裝相同，但您可能需要新增 `-Force` 參數：</span><span class="sxs-lookup"><span data-stu-id="89f8c-168">Reinstalling is done the same way as installing, but you need to add the `-Force` parameter:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="89f8c-169">和 MSI 型安裝不同，使用 PowerShellGet 進行安裝或更新，不會移除您的系統上可能存在的較舊版本。</span><span class="sxs-lookup"><span data-stu-id="89f8c-169">Unlike MSI-based installations, installing or updating using PowerShellGet does not remove older versions that may exist on your system.</span></span> <span data-ttu-id="89f8c-170">若要移除系統中的舊版 Azure PowerShell，請參閱[將 Azure PowerShell 模組解除安裝](uninstall-az-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="89f8c-170">To remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span> <span data-ttu-id="89f8c-171">如需有關 MSI 型安裝的詳細資訊，請參閱[使用 MSI 安裝 Azure PowerShell](install-az-ps-msi.md)。</span><span class="sxs-lookup"><span data-stu-id="89f8c-171">For more information about MSI-based installations, see [Install Azure PowerShell with an MSI](install-az-ps-msi.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="89f8c-172">使用多個版本的 Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="89f8c-172">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="89f8c-173">您可以安裝多個版本的 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="89f8c-173">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="89f8c-174">若要檢查是否安裝了多個 Azure PowerShell 版本，請使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="89f8c-174">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="89f8c-175">若想移除 Azure PowerShell 版本，請參閱[解除安裝 Azure PowerShell 模組](uninstall-az-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="89f8c-175">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="89f8c-176">如果您安裝了多個模組版本，模組會自動載入，`Import-Module` 則預設會載入最新的版本。</span><span class="sxs-lookup"><span data-stu-id="89f8c-176">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

<span data-ttu-id="89f8c-177">您可使用 `-RequiredVersion` 參數來安裝或載入特定版本的 `Az` 模組：</span><span class="sxs-lookup"><span data-stu-id="89f8c-177">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` parameter:</span></span>

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="provide-feedback"></a><span data-ttu-id="89f8c-178">提供意見反應</span><span class="sxs-lookup"><span data-stu-id="89f8c-178">Provide feedback</span></span>

<span data-ttu-id="89f8c-179">如果您發現 Azure PowerShell 有錯誤，請[在 GitHub 上提出問題](https://github.com/Azure/azure-powershell/issues)。</span><span class="sxs-lookup"><span data-stu-id="89f8c-179">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="89f8c-180">若要從命令列提供意見反應，請使用 [Send-Feedback](/powershell/module/az.accounts/send-feedback) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89f8c-180">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="89f8c-181">後續步驟</span><span class="sxs-lookup"><span data-stu-id="89f8c-181">Next Steps</span></span>

<span data-ttu-id="89f8c-182">若要深入了解 Azure PowerShell 模組和其功能，請參閱[開始使用 Azure PowerShell](get-started-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="89f8c-182">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="89f8c-183">如果您熟悉 Azure PowerShell 且需要從 AzureRM 遷移，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。</span><span class="sxs-lookup"><span data-stu-id="89f8c-183">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>