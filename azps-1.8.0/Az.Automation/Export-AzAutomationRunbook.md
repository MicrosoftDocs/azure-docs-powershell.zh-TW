---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 6d0af3f0d991d8d6b1f73c3277f9f86ac8dd0dae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623091"
---
# <span data-ttu-id="55291-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="55291-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="55291-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55291-102">SYNOPSIS</span></span>
<span data-ttu-id="55291-103">匯出自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="55291-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="55291-104">句法</span><span class="sxs-lookup"><span data-stu-id="55291-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55291-105">說明</span><span class="sxs-lookup"><span data-stu-id="55291-105">DESCRIPTION</span></span>
<span data-ttu-id="55291-106">**Export-AzAutomationRunbook** Cmdlet 會將 Azure 自動化 runbook 匯出至 wps_2 腳本 ( ps1 ) 檔案、wps_2 或 Wps_2 的工作流程 runbook，或針對圖形 runbook ( graphrunbook) 檔案。</span><span class="sxs-lookup"><span data-stu-id="55291-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="55291-107">[Runbook] 的名稱會變成匯出檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="55291-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="55291-108">示例</span><span class="sxs-lookup"><span data-stu-id="55291-108">EXAMPLES</span></span>

### <span data-ttu-id="55291-109">範例1：匯出 runbook</span><span class="sxs-lookup"><span data-stu-id="55291-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="55291-110">這個命令會將 [自動化] runbook 的已發佈版本匯出到使用者桌面。</span><span class="sxs-lookup"><span data-stu-id="55291-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="55291-111">參數</span><span class="sxs-lookup"><span data-stu-id="55291-111">PARAMETERS</span></span>

### <span data-ttu-id="55291-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="55291-112">-AutomationAccountName</span></span>
<span data-ttu-id="55291-113">指定此 Cmdlet 匯出 runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="55291-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="55291-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55291-114">-DefaultProfile</span></span>
<span data-ttu-id="55291-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="55291-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55291-116">-Force</span><span class="sxs-lookup"><span data-stu-id="55291-116">-Force</span></span>
<span data-ttu-id="55291-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="55291-117">ps_force</span></span>

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

### <span data-ttu-id="55291-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="55291-118">-Name</span></span>
<span data-ttu-id="55291-119">指定此 Cmdlet 匯出的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="55291-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="55291-120">[Runbook] 的名稱會變成匯出檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="55291-120">The name of the runbook becomes the name of the export file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55291-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="55291-121">-OutputFolder</span></span>
<span data-ttu-id="55291-122">指定此 Cmdlet 在其中建立匯出檔案的資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="55291-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55291-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55291-123">-ResourceGroupName</span></span>
<span data-ttu-id="55291-124">指定此 Cmdlet 匯出 runbook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="55291-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="55291-125">-槽</span><span class="sxs-lookup"><span data-stu-id="55291-125">-Slot</span></span>
<span data-ttu-id="55291-126">指定此 Cmdlet 是否匯出 runbook 的草稿或已發佈內容。</span><span class="sxs-lookup"><span data-stu-id="55291-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="55291-127">有效值為：</span><span class="sxs-lookup"><span data-stu-id="55291-127">Valid values are:</span></span> 
- <span data-ttu-id="55291-128">時間</span><span class="sxs-lookup"><span data-stu-id="55291-128">Published</span></span> 
- <span data-ttu-id="55291-129">草案</span><span class="sxs-lookup"><span data-stu-id="55291-129">Draft</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55291-130">-確認</span><span class="sxs-lookup"><span data-stu-id="55291-130">-Confirm</span></span>
<span data-ttu-id="55291-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="55291-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55291-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55291-132">-WhatIf</span></span>
<span data-ttu-id="55291-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55291-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55291-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55291-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55291-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55291-135">CommonParameters</span></span>
<span data-ttu-id="55291-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55291-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55291-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55291-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55291-138">輸入</span><span class="sxs-lookup"><span data-stu-id="55291-138">INPUTS</span></span>

### <span data-ttu-id="55291-139">System.object</span><span class="sxs-lookup"><span data-stu-id="55291-139">System.String</span></span>

## <span data-ttu-id="55291-140">輸出</span><span class="sxs-lookup"><span data-stu-id="55291-140">OUTPUTS</span></span>

### <span data-ttu-id="55291-141">DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="55291-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="55291-142">筆記</span><span class="sxs-lookup"><span data-stu-id="55291-142">NOTES</span></span>

## <span data-ttu-id="55291-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="55291-143">RELATED LINKS</span></span>

[<span data-ttu-id="55291-144">AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="55291-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="55291-145">匯入-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="55291-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="55291-146">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="55291-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="55291-147">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="55291-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="55291-148">發佈-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="55291-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="55291-149">移除-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="55291-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="55291-150">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="55291-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="55291-151">開始-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="55291-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)

