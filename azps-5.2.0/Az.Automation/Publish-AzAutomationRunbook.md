---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: feca8adfbfe24ce006c2fc5f52618f43591fa0b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285271"
---
# <span data-ttu-id="e0850-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0850-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="e0850-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0850-102">SYNOPSIS</span></span>
<span data-ttu-id="e0850-103">發佈 runbook。</span><span class="sxs-lookup"><span data-stu-id="e0850-103">Publishes a runbook.</span></span>

## <span data-ttu-id="e0850-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0850-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0850-105">說明</span><span class="sxs-lookup"><span data-stu-id="e0850-105">DESCRIPTION</span></span>
<span data-ttu-id="e0850-106">**AzAutomationRunbook** Cmdlet 發佈 runbook，以用於 Azure 自動化的生產環境。</span><span class="sxs-lookup"><span data-stu-id="e0850-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="e0850-107">示例</span><span class="sxs-lookup"><span data-stu-id="e0850-107">EXAMPLES</span></span>

### <span data-ttu-id="e0850-108">範例1：發佈 runbook</span><span class="sxs-lookup"><span data-stu-id="e0850-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e0850-109">這個命令會在名為 Contoso17 的 Azure 自動化帳戶中發佈名為 Runbk01 的 runbook。</span><span class="sxs-lookup"><span data-stu-id="e0850-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="e0850-110">參數</span><span class="sxs-lookup"><span data-stu-id="e0850-110">PARAMETERS</span></span>

### <span data-ttu-id="e0850-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e0850-111">-AutomationAccountName</span></span>
<span data-ttu-id="e0850-112">指定此 Cmdlet 發佈 runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e0850-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="e0850-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0850-113">-DefaultProfile</span></span>
<span data-ttu-id="e0850-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e0850-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0850-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e0850-115">-Name</span></span>
<span data-ttu-id="e0850-116">指定此 Cmdlet 發佈的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="e0850-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="e0850-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0850-117">-ResourceGroupName</span></span>
<span data-ttu-id="e0850-118">指定此 Cmdlet 發佈 runbook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0850-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="e0850-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0850-119">CommonParameters</span></span>
<span data-ttu-id="e0850-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0850-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0850-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0850-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0850-122">輸入</span><span class="sxs-lookup"><span data-stu-id="e0850-122">INPUTS</span></span>

### <span data-ttu-id="e0850-123">System.object</span><span class="sxs-lookup"><span data-stu-id="e0850-123">System.String</span></span>

## <span data-ttu-id="e0850-124">輸出</span><span class="sxs-lookup"><span data-stu-id="e0850-124">OUTPUTS</span></span>

### <span data-ttu-id="e0850-125">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="e0850-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="e0850-126">筆記</span><span class="sxs-lookup"><span data-stu-id="e0850-126">NOTES</span></span>

## <span data-ttu-id="e0850-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0850-127">RELATED LINKS</span></span>

[<span data-ttu-id="e0850-128">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0850-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="e0850-129">AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0850-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="e0850-130">匯入-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0850-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="e0850-131">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0850-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="e0850-132">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0850-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="e0850-133">移除-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0850-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="e0850-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0850-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="e0850-135">開始-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0850-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)

