---
title: 將 Azure PowerShell 解除安裝
description: 如何執行 Azure PowerShell 完全解除安裝
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: fcec2c713d1967a5a70df9b13aa30d9ff4625e9d
ms.sourcegitcommit: 5630030c5cfa9828c3c024b69de59248263ef17f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/26/2019
ms.locfileid: "56837600"
---
# <a name="uninstall-the-azure-powershell-module"></a>將 Azure PowerShell 模組解除安裝

本文說明如何將較舊版的 Azure PowerShell 解除安裝，或從您的系統將它完全移除。 如果您已決定要將 Azure PowerShell 完全解除安裝，請透過 [Send-Feedback](/powershell/module/az.accounts/send-feedback) Cmdlet 提供意見反應給我們。
如果發生錯誤 (bug)，希望您[提出 GitHub 問題](https://github.com/azure/azure-powershell/issues)，非常感謝您。

## <a name="uninstall-the-az-module"></a>將 Az 模組解除安裝

若要將 Az 模組解除安裝，請使用 [Uninstall-module](/powershell/module/powershellget/uninstall-module) Cmdlet。 不過，`Uninstall-Module` 只會解除安裝一個模組。 若要完全移除 Azure PowerShell，您必須個別將每個模組解除安裝。 如果您安裝了多個版本的 Azure PowerShell，則解除安裝可能會很複雜。

若要檢查您目前安裝的 Azure PowerShell 版本，請執行下列命令：

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

下列指令碼會查詢 PowerShell 資源庫來取得相依子模組的清單。 然後，指令碼會將每個子模組的正確版本解除安裝。 您需要擁有系統管理員權限，才能在 `Process` 或 `CurrentUser`以外的範圍執行此指令碼。

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force,

    [switch]$WhatIf
  )
  
  $AllModules = @()
  
  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    if ($_.requiredVersion) {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall" -f $_.name,$version)
      }
    }
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}...' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop -WhatIf:$WhatIf
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

若要使用此函式，請複製程式碼，然後貼到您的 PowerShell 工作階段。 下列範例示範如何執行函式，以將舊版的 Azure PowerShell 移除。

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

指令碼在執行時，會顯示要解除安裝的每個子模組名稱及版本。 若只想執行指令碼以查看會刪除的項目，而不要真正移除項目，請使用 `-WhatIf` 選項。

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

請針對您要解除安裝的 Azure PowerShell 每個版本執行此命令。 為了方便起見，下列指令碼會將所有版本的 Az 解除安裝，__只留下__最新版本。

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a>將 AzureRM 模組解除安裝

如果您的系統上安裝了 Az 模組，並想要將 AzureRM 解除安裝，有兩個簡單的選項可讓您不必執行上述的 `Uninstall-AllModules` 指令碼。 您要遵循哪個方法取決於您安裝 AzureRM 的方式。
如果您不確定，請先查看如何將 MSI 解除安裝的步驟。

### <a name="uninstall-azure-powershell-msi"></a>解除安裝 Azure PowerShell MSI

如果您使用 MSI 套件安裝 Azure PowerShell AzureRM 模組，則必須透過 Windows 系統而非 PowerShell 來解除安裝。

| 平台 | 範例的指示 |
|----------|--------------|
| Windows 10 | [開始] > [設定] > [應用程式] |
| Windows 7 </br>Windows 8 | [開啟] > [控制台] > [程式] > [解除安裝程式] |

您在此畫面上應該會看到程式清單中的 __Azure PowerShell__。 這是要解除安裝的應用程式。

### <a name="uninstall-from-powershell"></a>從 PowerShell 解除安裝

如果您是從 PowerShellGet 安裝 AzureRM，則可以使用新的 `Uninstall-AzureRM` 命令移除模組。 這會從機器中移除「所有」AzureRM 模組，但需要系統管理員權限。

```powershell-interactive
Uninstall-AzureRm
```

如果您無法順利執行 `Uninstall-AzureRM` 命令，請改用本文所提供的 `Uninstall-AllModules` 指令碼。