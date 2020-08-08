---
title: 將 Azure PowerShell 解除安裝
description: 如何執行 Azure PowerShell 完全解除安裝
ms.date: 05/28/2020
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: d99b40121deca0a4817c3a6364ad55020dadbda1
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566111"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="b25a7-103">將 Azure PowerShell 模組解除安裝</span><span class="sxs-lookup"><span data-stu-id="b25a7-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="b25a7-104">本文說明如何將較舊版的 Azure PowerShell 解除安裝，或從您的系統將它完全移除。</span><span class="sxs-lookup"><span data-stu-id="b25a7-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="b25a7-105">如果您已決定要將 Azure PowerShell 完全解除安裝，請透過 [Send-Feedback](/powershell/module/az.accounts/send-feedback) Cmdlet 提供意見反應給我們。</span><span class="sxs-lookup"><span data-stu-id="b25a7-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="b25a7-106">如果發生錯誤 (bug)，希望您[提出 GitHub 問題](https://github.com/azure/azure-powershell/issues)加以解決，非常感謝您。</span><span class="sxs-lookup"><span data-stu-id="b25a7-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-powershell-module-from-msi"></a><span data-ttu-id="b25a7-107">透過 MSI 解除安裝 Az PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="b25a7-107">Uninstall the Az PowerShell module from MSI</span></span>

<span data-ttu-id="b25a7-108">如果您使用 MSI 套件安裝 Az PowerShell 模組，則必須透過 Windows 系統而非 PowerShell 來解除安裝。</span><span class="sxs-lookup"><span data-stu-id="b25a7-108">If you installed Az PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="b25a7-109">平台</span><span class="sxs-lookup"><span data-stu-id="b25a7-109">Platform</span></span>         |                      <span data-ttu-id="b25a7-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="b25a7-110">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="b25a7-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="b25a7-111">Windows 10</span></span>               | <span data-ttu-id="b25a7-112">[開始] > [設定] > [應用程式]</span><span class="sxs-lookup"><span data-stu-id="b25a7-112">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="b25a7-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b25a7-113">Windows 7</span></span> </br><span data-ttu-id="b25a7-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b25a7-114">Windows 8</span></span> | <span data-ttu-id="b25a7-115">[啟動] > [控制台] -> [程式集] -> [解除安裝程式]</span><span class="sxs-lookup"><span data-stu-id="b25a7-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="b25a7-116">您在此畫面上應該會看到程式清單中的 **Azure PowerShell**。</span><span class="sxs-lookup"><span data-stu-id="b25a7-116">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="b25a7-117">這是要解除安裝的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b25a7-117">This is the app to uninstall.</span></span> <span data-ttu-id="b25a7-118">如果並未列出此程式，而您是透過 PowerShellGet 安裝，則應遵循下一組指示。</span><span class="sxs-lookup"><span data-stu-id="b25a7-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-the-az-powershell-module-from-powershellget"></a><span data-ttu-id="b25a7-119">透過 PowerShellGet 解除安裝 Az PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="b25a7-119">Uninstall the Az PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="b25a7-120">若要將 Az 模組解除安裝，請使用 [Uninstall-Module](/powershell/module/powershellget/uninstall-module) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b25a7-120">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="b25a7-121">不過，`Uninstall-Module` 只會解除安裝一個模組。</span><span class="sxs-lookup"><span data-stu-id="b25a7-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="b25a7-122">若要完全移除 Az PowerShell 模組，您必須個別將每個模組解除安裝。</span><span class="sxs-lookup"><span data-stu-id="b25a7-122">To remove the Az PowerShell module completely, you must uninstall each module individually.</span></span> <span data-ttu-id="b25a7-123">如果您安裝了多個版本的 Azure PowerShell，則解除安裝可能會很複雜。</span><span class="sxs-lookup"><span data-stu-id="b25a7-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="b25a7-124">若要檢查您安裝的 Az PowerShell 模組版本，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="b25a7-124">To check which versions of the Az PowerShell module you've installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<a name="uninstall-script"/>

<span data-ttu-id="b25a7-125">下列指令碼會查詢 PowerShell 資源庫來取得相依子模組的清單。</span><span class="sxs-lookup"><span data-stu-id="b25a7-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="b25a7-126">然後，指令碼會將每個子模組的正確版本解除安裝。</span><span class="sxs-lookup"><span data-stu-id="b25a7-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="b25a7-127">您需要擁有系統管理員權限，才能在**流程**或**目前使用者**以外的範圍執行此指令碼。</span><span class="sxs-lookup"><span data-stu-id="b25a7-127">You need to have administrator access to run this script in a scope other than **Process** or **Current User**.</span></span>

```powershell-interactive
function Uninstall-AzModule {
  [CmdletBinding(SupportsShouldProcess)]
  param(
    [ValidateNotNullOrEmpty()]
    [ValidateSet('Az','AzureRM','Azure')]
    [string]$Name = 'Az',

    [Parameter(Mandatory)]
    [string]$Version,

    [switch]$AllowPrerelease
  )

  $Params = @{}

  if ($PSBoundParameters.AllowPrerelease) {
    $Params.AllowPrerelease = $true
  }

  $IsAdmin = ([Security.Principal.WindowsPrincipal] [Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole] 'Administrator')

  if (-not(Get-InstalledModule -Name $Name -RequiredVersion $Version -ErrorAction SilentlyContinue -OutVariable RootModule @Params)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version not found."

  } elseif (($RootModule.InstalledLocation -notlike "*$env:USERPROFILE*") -and ($IsAdmin -eq $false)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version exists in a system path. PowerShell must be run elevated as an admin to remove it."

  } elseif ((Get-Process -Name powershell, pwsh -OutVariable Sessions -ErrorAction SilentlyContinue).Count -gt 1) {

    Write-Warning -Message "Uninstall aborted. Please close all other PowerShell sessions before continuing. There are currently $($Sessions.Count) PowerShell sessions running."

  } else {
    Write-Verbose -Message 'Creating list of dependencies...'
    $target = Find-Module -Name $Name -RequiredVersion $Version @Params

    $AllModules = @([pscustomobject]@{
      Name = $Name
      Version = $Version
    })

    $AllModules += foreach ($dependency in $target.Dependencies) {
      switch ($dependency.keys) {
        {$_ -contains 'RequiredVersion'} {$UninstallVersion = $dependency.RequiredVersion; break}
        {$_ -contains 'MinimumVersion'} {$UninstallVersion = $dependency.MinimumVersion; break}
      }

      [pscustomobject]@{
        Name = $dependency.Name
        Version = $UninstallVersion
      }
    }

    [int]$i = 100 / $AllModules.Count

    foreach ($module in $AllModules) {
      Write-Progress -Activity 'Uninstallation in Progress' -Status "$i% Complete:" -PercentComplete $i
      $i++

      if (Get-InstalledModule -Name $module.Name -RequiredVersion $module.Version -ErrorAction SilentlyContinue @Params) {
        Write-Verbose -Message "Uninstalling $($module.Name) version $($module.Version)"

        Remove-Module -FullyQualifiedName @{ModuleName=$module.Name;ModuleVersion=$module.Version} -ErrorAction SilentlyContinue

        try {
          if ($PSCmdlet.ShouldProcess("$($module.Name) version $($module.Version)")) {
            Uninstall-Module -Name $module.Name -RequiredVersion $module.Version -Force -ErrorAction Stop @Params
          }
          $State = 'Uninstalled'
        } Catch {
          $State = 'Manual uninstall required'
          Write-Verbose -Message "$($module.Name) version: $($module.Version) may require manual uninstallation."
        }

      } else {
        $State = 'Not found'
        Write-Verbose -Message "$($module.Name) version: $($module.Version) not found."
      }

      if (-not $PSBoundParameters.WhatIf) {
        [pscustomobject]@{
          ModuleName = $module.Name
          Version = $module.Version
          State = $State
        }
      }

    }
  }
}
```

<span data-ttu-id="b25a7-128">若要使用此函式，請複製程式碼，然後貼到您的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="b25a7-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="b25a7-129">下列範例示範如何執行函式，以將舊版的 Az PowerShell 模組和其子模組移除。</span><span class="sxs-lookup"><span data-stu-id="b25a7-129">The following example shows how to run the function to remove an older version of the Az PowerShell module and its submodules.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="b25a7-130">指令碼在執行時，會顯示要解除安裝每個子模組的**名稱**、**版本**及**狀態**。</span><span class="sxs-lookup"><span data-stu-id="b25a7-130">As the script runs, it displays the **Name**, **Version**, and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="b25a7-131">若執行指令碼只是查看會刪除的項目，而不要真正移除項目，請指定 `-WhatIf` 參數。</span><span class="sxs-lookup"><span data-stu-id="b25a7-131">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

```output
ModuleName              Version  State
----------              -------  -----
Az.Accounts             1.5.1    Not found
Az.Aks                  1.0.1    Uninstalled
Az.AnalysisServices     1.1.0    Uninstalled
Az.ApiManagement        1.0.0    Uninstalled
Az.ApplicationInsights  1.0.0    Uninstalled
...
```

> [!IMPORTANT]
> <span data-ttu-id="b25a7-132">若此指令碼與要解除安裝之相同版本的相依性不完全相符，系統不會解除安裝該相依性的_任何_版本。</span><span class="sxs-lookup"><span data-stu-id="b25a7-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="b25a7-133">這是因為您的系統上可能有其他版本的目標模組需要使用這些相依性。</span><span class="sxs-lookup"><span data-stu-id="b25a7-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="b25a7-134">針對您要解除安裝的 Az PowerShell 模組每個版本執行下列範例。</span><span class="sxs-lookup"><span data-stu-id="b25a7-134">Run the following example for every version of the Az PowerShell module that you want to uninstall.</span></span>
<span data-ttu-id="b25a7-135">為了方便起見，下列指令碼會將所有版本的 Az 解除安裝，**只留下**最新版本。</span><span class="sxs-lookup"><span data-stu-id="b25a7-135">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="b25a7-136">將 AzureRM 模組解除安裝</span><span class="sxs-lookup"><span data-stu-id="b25a7-136">Uninstall the AzureRM module</span></span>

<span data-ttu-id="b25a7-137">如果您的系統上安裝了 Az 模組，並想要將 AzureRM 解除安裝，有兩個選項。</span><span class="sxs-lookup"><span data-stu-id="b25a7-137">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options.</span></span> <span data-ttu-id="b25a7-138">您要遵循哪個方法取決於您安裝 AzureRM 模組的方式。</span><span class="sxs-lookup"><span data-stu-id="b25a7-138">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="b25a7-139">如果您不確定原始安裝方法，請先依照解除安裝 MSI 的步驟操作。</span><span class="sxs-lookup"><span data-stu-id="b25a7-139">If you're not sure of your original installation method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-the-azurerm-powershell-module-from-msi"></a><span data-ttu-id="b25a7-140">透過 MSI 解除安裝 AzureRM PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="b25a7-140">Uninstall the AzureRM PowerShell module from MSI</span></span>

<span data-ttu-id="b25a7-141">如果您使用 MSI 套件安裝 AzureRM PowerShell 模組，則必須透過 Windows 系統而非 PowerShell 來解除安裝。</span><span class="sxs-lookup"><span data-stu-id="b25a7-141">If you installed the AzureRM PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="b25a7-142">平台</span><span class="sxs-lookup"><span data-stu-id="b25a7-142">Platform</span></span>         |                      <span data-ttu-id="b25a7-143">Instructions</span><span class="sxs-lookup"><span data-stu-id="b25a7-143">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="b25a7-144">Windows 10</span><span class="sxs-lookup"><span data-stu-id="b25a7-144">Windows 10</span></span>               | <span data-ttu-id="b25a7-145">[開始] > [設定] > [應用程式]</span><span class="sxs-lookup"><span data-stu-id="b25a7-145">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="b25a7-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b25a7-146">Windows 7</span></span> </br><span data-ttu-id="b25a7-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b25a7-147">Windows 8</span></span> | <span data-ttu-id="b25a7-148">[啟動] > [控制台] -> [程式集] -> [解除安裝程式]</span><span class="sxs-lookup"><span data-stu-id="b25a7-148">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="b25a7-149">您在此畫面上應該會看到程式清單中的 **Azure PowerShell** 或 **Microsoft Azure PowerShell - 月份年份**。</span><span class="sxs-lookup"><span data-stu-id="b25a7-149">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="b25a7-150">這是要解除安裝的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b25a7-150">This is the app to uninstall.</span></span> <span data-ttu-id="b25a7-151">如果並未列出此程式，而您是透過 PowerShellGet 安裝，則應遵循下一組指示。</span><span class="sxs-lookup"><span data-stu-id="b25a7-151">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-the-azurerm-powershell-module-from-powershellget"></a><span data-ttu-id="b25a7-152">透過 PowerShellGet 解除安裝 AzureRM PowerShell 模組</span><span class="sxs-lookup"><span data-stu-id="b25a7-152">Uninstall the AzureRM PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="b25a7-153">如果透過 PowerShellGet 安裝了 AzureRM，您可以使用 [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) Cmdlet 移除模組，您可以在 `Az.Accounts` 模組中找到這個命令。</span><span class="sxs-lookup"><span data-stu-id="b25a7-153">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="b25a7-154">下列範例會從您的電腦移除 _所有_ AzureRM 模組。</span><span class="sxs-lookup"><span data-stu-id="b25a7-154">The following example removes _all_ AzureRM modules from your machine.</span></span> <span data-ttu-id="b25a7-155">此動作需要系統管理員權限。</span><span class="sxs-lookup"><span data-stu-id="b25a7-155">It requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```