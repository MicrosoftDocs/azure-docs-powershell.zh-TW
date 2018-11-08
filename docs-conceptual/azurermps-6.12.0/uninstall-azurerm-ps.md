---
title: 將 Azure PowerShell 解除安裝
description: 如何執行 Azure PowerShell 完全解除安裝
ms.date: 09/11/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 5f51683896fffe56332ac0a43179ad1f894d8d75
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/07/2018
ms.locfileid: "51212605"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="28e33-103">將 Azure PowerShell 模組解除安裝</span><span class="sxs-lookup"><span data-stu-id="28e33-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="28e33-104">本文說明如何將較舊版的 Azure PowerShell 解除安裝，或從您的系統將它完全移除。</span><span class="sxs-lookup"><span data-stu-id="28e33-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="28e33-105">如果您已決定要將 Azure PowerShell 完全解除安裝，請透過 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) Cmdlet 提供意見反應給我們。</span><span class="sxs-lookup"><span data-stu-id="28e33-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="28e33-106">如果發生錯誤 (bug)，希望您[提出 GitHub 問題](https://github.com/azure/azure-powershell/issues)，非常感謝您。</span><span class="sxs-lookup"><span data-stu-id="28e33-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi"></a><span data-ttu-id="28e33-107">解除安裝 MSI</span><span class="sxs-lookup"><span data-stu-id="28e33-107">Uninstall MSI</span></span>

<span data-ttu-id="28e33-108">如果您使用 MSI 套件安裝 Azure PowerShell，則必須透過 Windows 系統而非 PowerShell 來解除安裝。</span><span class="sxs-lookup"><span data-stu-id="28e33-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="28e33-109">平台</span><span class="sxs-lookup"><span data-stu-id="28e33-109">Platform</span></span> | <span data-ttu-id="28e33-110">範例的指示</span><span class="sxs-lookup"><span data-stu-id="28e33-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="28e33-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="28e33-111">Windows 10</span></span> | <span data-ttu-id="28e33-112">[開始] > [設定] > [應用程式]</span><span class="sxs-lookup"><span data-stu-id="28e33-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="28e33-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="28e33-113">Windows 7</span></span> </br><span data-ttu-id="28e33-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="28e33-114">Windows 8</span></span> | <span data-ttu-id="28e33-115">[開啟] > [控制台] > [程式] > [解除安裝程式]</span><span class="sxs-lookup"><span data-stu-id="28e33-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="28e33-116">您在此畫面上應該會看到程式清單中的 "Azure PowerShell"，並可從該處解除安裝。</span><span class="sxs-lookup"><span data-stu-id="28e33-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="28e33-117">從 PowerShell 解除安裝</span><span class="sxs-lookup"><span data-stu-id="28e33-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="28e33-118">如果您使用 PowerShellGet 安裝 Azure PowerShell，則可以使用 [Uninstall-Module](/powershell/module/powershellget/uninstall-module) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28e33-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="28e33-119">不過，`Uninstall-Module` 只會解除安裝一個模組。</span><span class="sxs-lookup"><span data-stu-id="28e33-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="28e33-120">若要完全移除 Azure PowerShell，您必須個別將每個模組解除安裝。</span><span class="sxs-lookup"><span data-stu-id="28e33-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="28e33-121">如果您安裝了多個版本的 Azure PowerShell，則解除安裝可能會很複雜。</span><span class="sxs-lookup"><span data-stu-id="28e33-121">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="28e33-122">下列指令碼會查詢 PowerShell 資源庫來取得相依子模組的清單。</span><span class="sxs-lookup"><span data-stu-id="28e33-122">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="28e33-123">然後，指令碼會將每個子模組的正確版本解除安裝。</span><span class="sxs-lookup"><span data-stu-id="28e33-123">Then, the script uninstalls the correct version of each submodule.</span></span>

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force
  )

  $AllModules = @()

  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredversion}
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

<span data-ttu-id="28e33-124">若要使用此函式，請複製程式碼，然後貼到您的 PowerShell 工作階段。</span><span class="sxs-lookup"><span data-stu-id="28e33-124">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="28e33-125">下列範例示範如何執行函式，以將舊版的 Azure PowerShell 移除。</span><span class="sxs-lookup"><span data-stu-id="28e33-125">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="28e33-126">指令碼在執行時，會顯示要解除安裝的每個子模組名稱及版本。</span><span class="sxs-lookup"><span data-stu-id="28e33-126">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="28e33-127">請針對您要解除安裝的 Azure PowerShell 每個版本執行此命令。</span><span class="sxs-lookup"><span data-stu-id="28e33-127">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="28e33-128">為了方便起見，下列指令碼會將所有版本的 AzureRM 解除安裝，__只留下__最新版本。</span><span class="sxs-lookup"><span data-stu-id="28e33-128">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```