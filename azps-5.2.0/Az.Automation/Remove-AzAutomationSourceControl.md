---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: e5422cc9254b8393330152bcaab880013b5ef99c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285215"
---
# <span data-ttu-id="9483a-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="9483a-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="9483a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9483a-102">SYNOPSIS</span></span>
<span data-ttu-id="9483a-103">移除 Azure 自動化來源控制。</span><span class="sxs-lookup"><span data-stu-id="9483a-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="9483a-104">句法</span><span class="sxs-lookup"><span data-stu-id="9483a-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9483a-105">說明</span><span class="sxs-lookup"><span data-stu-id="9483a-105">DESCRIPTION</span></span>
<span data-ttu-id="9483a-106">Remove-AzAutomationSourceControl Cmdlet 會從 Azure 自動化中移除來源控制。</span><span class="sxs-lookup"><span data-stu-id="9483a-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="9483a-107">示例</span><span class="sxs-lookup"><span data-stu-id="9483a-107">EXAMPLES</span></span>

### <span data-ttu-id="9483a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9483a-108">Example 1</span></span>
<span data-ttu-id="9483a-109">這個命令會在名為 devAccount 的帳戶中，移除名為 VSTSNative 的自動化來源控制。</span><span class="sxs-lookup"><span data-stu-id="9483a-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="9483a-110">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="9483a-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="9483a-111">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9483a-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="9483a-112">參數</span><span class="sxs-lookup"><span data-stu-id="9483a-112">PARAMETERS</span></span>

### <span data-ttu-id="9483a-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9483a-113">-AutomationAccountName</span></span>
<span data-ttu-id="9483a-114">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9483a-114">The automation account name.</span></span>

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

### <span data-ttu-id="9483a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9483a-115">-DefaultProfile</span></span>
<span data-ttu-id="9483a-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9483a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9483a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="9483a-117">-Name</span></span>
<span data-ttu-id="9483a-118">來源控制項名稱。</span><span class="sxs-lookup"><span data-stu-id="9483a-118">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9483a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9483a-119">-PassThru</span></span>
<span data-ttu-id="9483a-120">PassThru 會傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="9483a-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9483a-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="9483a-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9483a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9483a-122">-ResourceGroupName</span></span>
<span data-ttu-id="9483a-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9483a-123">The resource group name.</span></span>

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

### <span data-ttu-id="9483a-124">-確認</span><span class="sxs-lookup"><span data-stu-id="9483a-124">-Confirm</span></span>
<span data-ttu-id="9483a-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9483a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9483a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9483a-126">-WhatIf</span></span>
<span data-ttu-id="9483a-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9483a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9483a-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9483a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9483a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9483a-129">CommonParameters</span></span>
<span data-ttu-id="9483a-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9483a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9483a-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9483a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9483a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="9483a-132">INPUTS</span></span>

### <span data-ttu-id="9483a-133">System.object</span><span class="sxs-lookup"><span data-stu-id="9483a-133">System.String</span></span>

## <span data-ttu-id="9483a-134">輸出</span><span class="sxs-lookup"><span data-stu-id="9483a-134">OUTPUTS</span></span>

### <span data-ttu-id="9483a-135">System.void</span><span class="sxs-lookup"><span data-stu-id="9483a-135">System.Void</span></span>

### <span data-ttu-id="9483a-136">System.object</span><span class="sxs-lookup"><span data-stu-id="9483a-136">System.Boolean</span></span>

## <span data-ttu-id="9483a-137">筆記</span><span class="sxs-lookup"><span data-stu-id="9483a-137">NOTES</span></span>

## <span data-ttu-id="9483a-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="9483a-138">RELATED LINKS</span></span>