---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: 17d1c7c94726543aa30a032423576c8a7dcb6fcc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285667"
---
# <span data-ttu-id="2ac85-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="2ac85-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="2ac85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ac85-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac85-103">建立自動化來源控制項。</span><span class="sxs-lookup"><span data-stu-id="2ac85-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="2ac85-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ac85-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ac85-105">說明</span><span class="sxs-lookup"><span data-stu-id="2ac85-105">DESCRIPTION</span></span>
<span data-ttu-id="2ac85-106">New-AzAutomationSourceControl Cmdlet 會建立一個設定，以將我的 Azure 自動化帳戶與我的 VSTS TFVC、VSTS Git 或 GitHub 連結在一起。</span><span class="sxs-lookup"><span data-stu-id="2ac85-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="2ac85-107">示例</span><span class="sxs-lookup"><span data-stu-id="2ac85-107">EXAMPLES</span></span>

### <span data-ttu-id="2ac85-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2ac85-108">Example 1</span></span>
<span data-ttu-id="2ac85-109">建立來源控制設定，以將我的 Azure 自動化帳戶與我的 VSTS TFVC 專案連結在一起。</span><span class="sxs-lookup"><span data-stu-id="2ac85-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="2ac85-110">TFVC 專案沒有分支，因此沒有指定 Branch 參數。</span><span class="sxs-lookup"><span data-stu-id="2ac85-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://contoso.visualstudio.com/ContosoProduction/_versionControl" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://contoso.visualstudio.com/ContosoProduc...
```

### <span data-ttu-id="2ac85-111">範例2</span><span class="sxs-lookup"><span data-stu-id="2ac85-111">Example 2</span></span>
<span data-ttu-id="2ac85-112">建立來源控制設定，以將 Azure 自動化帳戶與我的 VSTS Git 專案連結在一起。</span><span class="sxs-lookup"><span data-stu-id="2ac85-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://contoso.visualstudio.com/_git/Finance" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://contoso.visualstudio.com/_git/Finan...
```

### <span data-ttu-id="2ac85-113">範例3</span><span class="sxs-lookup"><span data-stu-id="2ac85-113">Example 3</span></span>
<span data-ttu-id="2ac85-114">建立來源控制設定以將 Azure 自動化帳戶與我的 GitHub 專案連結。</span><span class="sxs-lookup"><span data-stu-id="2ac85-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


```powershell
PS C:\> # GitHub access token
PS C:\> $token = "68b08011223aac8bdd3388913a44rrsaa84fdf"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "GitHub1" `
                                           -RepoUrl "https://github.com/Contoso/TestSourceControl.git" `
                                           -SourceType "GitHub" `
                                           -Branch "master" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name    SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------ ---------- -------- -------------- -------
GitHub1 GitHub     master /Runbooks  True     True           https://github.com/Contoso/TestSourceControl...
```

## <span data-ttu-id="2ac85-115">參數</span><span class="sxs-lookup"><span data-stu-id="2ac85-115">PARAMETERS</span></span>

### <span data-ttu-id="2ac85-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="2ac85-116">-AccessToken</span></span>
<span data-ttu-id="2ac85-117">來源控制項存取權杖。</span><span class="sxs-lookup"><span data-stu-id="2ac85-117">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac85-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2ac85-118">-AutomationAccountName</span></span>
<span data-ttu-id="2ac85-119">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2ac85-119">The automation account name.</span></span>

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

### <span data-ttu-id="2ac85-120">-分支</span><span class="sxs-lookup"><span data-stu-id="2ac85-120">-Branch</span></span>
<span data-ttu-id="2ac85-121">來源控制項分支。</span><span class="sxs-lookup"><span data-stu-id="2ac85-121">The source control branch.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac85-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac85-122">-DefaultProfile</span></span>
<span data-ttu-id="2ac85-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ac85-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ac85-124">-描述</span><span class="sxs-lookup"><span data-stu-id="2ac85-124">-Description</span></span>
<span data-ttu-id="2ac85-125">來源控制項描述。</span><span class="sxs-lookup"><span data-stu-id="2ac85-125">The source control description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac85-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="2ac85-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="2ac85-127">來源控制項的 publishRunbook 屬性。</span><span class="sxs-lookup"><span data-stu-id="2ac85-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="2ac85-128">如果已設定 DoNotPublishRunbook，這表示使用者 runbook 將匯入為「草稿」。</span><span class="sxs-lookup"><span data-stu-id="2ac85-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac85-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="2ac85-129">-EnableAutoSync</span></span>
<span data-ttu-id="2ac85-130">來源控制項的 autoSync 屬性。</span><span class="sxs-lookup"><span data-stu-id="2ac85-130">The autoSync property for the source control.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac85-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="2ac85-131">-FolderPath</span></span>
<span data-ttu-id="2ac85-132">[來源] 控制資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="2ac85-132">The source control folder path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac85-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ac85-133">-Name</span></span>
<span data-ttu-id="2ac85-134">來源控制項名稱。</span><span class="sxs-lookup"><span data-stu-id="2ac85-134">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac85-135">-RepoUrl</span><span class="sxs-lookup"><span data-stu-id="2ac85-135">-RepoUrl</span></span>
<span data-ttu-id="2ac85-136">來源控制項存放庫 url。</span><span class="sxs-lookup"><span data-stu-id="2ac85-136">The source control repo url.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac85-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac85-137">-ResourceGroupName</span></span>
<span data-ttu-id="2ac85-138">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ac85-138">The resource group name.</span></span>

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

### <span data-ttu-id="2ac85-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="2ac85-139">-SourceType</span></span>
<span data-ttu-id="2ac85-140">來源控制項類型。</span><span class="sxs-lookup"><span data-stu-id="2ac85-140">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac85-141">-確認</span><span class="sxs-lookup"><span data-stu-id="2ac85-141">-Confirm</span></span>
<span data-ttu-id="2ac85-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2ac85-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ac85-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ac85-143">-WhatIf</span></span>
<span data-ttu-id="2ac85-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2ac85-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ac85-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ac85-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ac85-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac85-146">CommonParameters</span></span>
<span data-ttu-id="2ac85-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ac85-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac85-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2ac85-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac85-149">輸入</span><span class="sxs-lookup"><span data-stu-id="2ac85-149">INPUTS</span></span>

### <span data-ttu-id="2ac85-150">System.object</span><span class="sxs-lookup"><span data-stu-id="2ac85-150">System.String</span></span>

## <span data-ttu-id="2ac85-151">輸出</span><span class="sxs-lookup"><span data-stu-id="2ac85-151">OUTPUTS</span></span>

### <span data-ttu-id="2ac85-152">SourceControl 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2ac85-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="2ac85-153">筆記</span><span class="sxs-lookup"><span data-stu-id="2ac85-153">NOTES</span></span>

## <span data-ttu-id="2ac85-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ac85-154">RELATED LINKS</span></span>