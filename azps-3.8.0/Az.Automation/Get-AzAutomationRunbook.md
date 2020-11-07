---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: edae476893de5a64e950902d2de7b31fe53b51ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958695"
---
# <span data-ttu-id="53bcc-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="53bcc-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="53bcc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="53bcc-103">取得 runbook。</span><span class="sxs-lookup"><span data-stu-id="53bcc-103">Gets a runbook.</span></span>

## <span data-ttu-id="53bcc-104">句法</span><span class="sxs-lookup"><span data-stu-id="53bcc-104">SYNTAX</span></span>

### <span data-ttu-id="53bcc-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="53bcc-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53bcc-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="53bcc-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53bcc-107">說明</span><span class="sxs-lookup"><span data-stu-id="53bcc-107">DESCRIPTION</span></span>
<span data-ttu-id="53bcc-108">**AzAutomationRunbook** Cmdlet 會取得 Azure 自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="53bcc-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="53bcc-109">若要取得特定的 runbook，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="53bcc-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="53bcc-110">示例</span><span class="sxs-lookup"><span data-stu-id="53bcc-110">EXAMPLES</span></span>

### <span data-ttu-id="53bcc-111">範例1：取得所有 runbook</span><span class="sxs-lookup"><span data-stu-id="53bcc-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="53bcc-112">這個命令會取得 Azure 自動化帳戶（名為 Contoso17）中的所有 runbook。</span><span class="sxs-lookup"><span data-stu-id="53bcc-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="53bcc-113">參數</span><span class="sxs-lookup"><span data-stu-id="53bcc-113">PARAMETERS</span></span>

### <span data-ttu-id="53bcc-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="53bcc-114">-AutomationAccountName</span></span>
<span data-ttu-id="53bcc-115">指定此 Cmdlet 在其中取得 runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="53bcc-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="53bcc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53bcc-116">-DefaultProfile</span></span>
<span data-ttu-id="53bcc-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="53bcc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53bcc-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="53bcc-118">-Name</span></span>
<span data-ttu-id="53bcc-119">指定此 Cmdlet 取得的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="53bcc-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bcc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53bcc-120">-ResourceGroupName</span></span>
<span data-ttu-id="53bcc-121">指定此 Cmdlet 取得 runbook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="53bcc-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="53bcc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bcc-122">CommonParameters</span></span>
<span data-ttu-id="53bcc-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53bcc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53bcc-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53bcc-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bcc-125">輸入</span><span class="sxs-lookup"><span data-stu-id="53bcc-125">INPUTS</span></span>

### <span data-ttu-id="53bcc-126">System.object</span><span class="sxs-lookup"><span data-stu-id="53bcc-126">System.String</span></span>

## <span data-ttu-id="53bcc-127">輸出</span><span class="sxs-lookup"><span data-stu-id="53bcc-127">OUTPUTS</span></span>

### <span data-ttu-id="53bcc-128">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="53bcc-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="53bcc-129">筆記</span><span class="sxs-lookup"><span data-stu-id="53bcc-129">NOTES</span></span>

## <span data-ttu-id="53bcc-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="53bcc-130">RELATED LINKS</span></span>

[<span data-ttu-id="53bcc-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="53bcc-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="53bcc-132">匯入-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="53bcc-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="53bcc-133">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="53bcc-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="53bcc-134">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="53bcc-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="53bcc-135">發佈-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="53bcc-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="53bcc-136">移除-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="53bcc-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="53bcc-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="53bcc-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="53bcc-138">開始-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="53bcc-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)

