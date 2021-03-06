---
title: 將 Azure PowerShell 解除安裝
description: 如何執行 Azure PowerShell 完全解除安裝
ms.date: 06/10/2019
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 58d861f09eef04638cfa7e784ef0e28e9f4751d4
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244257"
---
# <a name="uninstall-the-azure-powershell-module"></a>將 Azure PowerShell 模組解除安裝

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

本文說明如何將較舊版的 Azure PowerShell 解除安裝，或從您的系統將它完全移除。 如果您已決定要將 Azure PowerShell 完全解除安裝，請透過 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) Cmdlet 提供意見反應給我們。
如果發生錯誤 (bug)，希望您[提出 GitHub 問題](https://github.com/azure/azure-powershell/issues)，非常感謝您。


## <a name="uninstall-azure-powershell-msi"></a>解除安裝 Azure PowerShell MSI

如果您使用 MSI 套件安裝 Azure PowerShell，則必須透過 Windows 系統而非 PowerShell 來解除安裝。

| 平台 | Instructions |
|----------|--------------|
| Windows 10 | [開始] > [設定] > [應用程式] |
| Windows 7 </br>Windows 8 | [啟動] > [控制台] -> [程式集] -> [解除安裝程式] |

您在此畫面上應該會看到程式清單中的 __Azure PowerShell__。 這是要解除安裝的應用程式。

## <a name="uninstall-from-powershell"></a>從 PowerShell 解除安裝

如果您使用 PowerShellGet 安裝 Azure PowerShell，則可以使用 [Uninstall-Module](/powershell/module/powershellget/uninstall-module) Cmdlet。 不過，`Uninstall-Module` 只會解除安裝一個模組。 若要完全移除 Azure PowerShell，您必須個別將每個模組解除安裝。 如果您安裝了多個版本的 Azure PowerShell，則解除安裝可能會很複雜。

若要檢查您目前安裝的 Azure PowerShell 版本，請執行下列命令：

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

```output
Version              Name                                Repository           Description
-------              ----                                ----------           -----------
6.11.0               AzureRM                             PSGallery            Azure Resource Manager Module
6.13.1               AzureRM                             PSGallery            Azure Resource Manager Module
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
    if ($_.PSObject.Properties.Name -contains 'requiredVersion') {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version -ErrorAction Ignore
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        $availableModules = Get-InstalledModule $_.name -AllVersions
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall. Available versions are: {2}" -f $_.name,$version,($availableModules.Version -join ', '))
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
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

指令碼在執行時，會顯示要解除安裝的每個子模組名稱及版本。 若只想執行指令碼以查看會刪除的項目，而不要真正移除項目，請使用 `-WhatIf` 選項。

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> 若此指令碼與要解除安裝之相同版本的相依性不完全相符，系統不會解除安裝該相依性的_任何_版本。 這是因為您的系統上可能有其他版本的目標模組需要使用這些相依性。 在此情況下，會列出可用的相依性版本。
> 然後您就可以使用 `Uninstall-Module` 手動移除任何舊版本。


請針對您要解除安裝的 Azure PowerShell 每個版本執行此命令。 為了方便起見，下列指令碼會將所有版本的 AzureRM 解除安裝，__只留下__最新版本。

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
