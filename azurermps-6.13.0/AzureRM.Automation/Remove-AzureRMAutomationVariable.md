---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
ms.openlocfilehash: b336104fea097b0f5adf0993853dd6fff7bba1f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624629"
---
# <span data-ttu-id="e5bc5-101">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e5bc5-101">Remove-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="e5bc5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="e5bc5-103">移除自動化變數。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-103">Removes an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5bc5-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5bc5-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5bc5-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5bc5-105">DESCRIPTION</span></span>
<span data-ttu-id="e5bc5-106">**AzureRmAutomationVariable** Cmdlet 會從 Azure 自動化中移除變數。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-106">The **Remove-AzureRmAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="e5bc5-107">示例</span><span class="sxs-lookup"><span data-stu-id="e5bc5-107">EXAMPLES</span></span>

### <span data-ttu-id="e5bc5-108">範例1：移除變數</span><span class="sxs-lookup"><span data-stu-id="e5bc5-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e5bc5-109">這個命令會在名為 Contoso17 的自動化帳戶中移除一個名為 StringVariable22 的變數。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="e5bc5-110">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e5bc5-111">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e5bc5-112">參數</span><span class="sxs-lookup"><span data-stu-id="e5bc5-112">PARAMETERS</span></span>

### <span data-ttu-id="e5bc5-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e5bc5-113">-AutomationAccountName</span></span>
<span data-ttu-id="e5bc5-114">指定包含此 Cmdlet 所刪除變數的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e5bc5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5bc5-115">-DefaultProfile</span></span>
<span data-ttu-id="e5bc5-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e5bc5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5bc5-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5bc5-117">-Name</span></span>
<span data-ttu-id="e5bc5-118">指定此 Cmdlet 刪除的變數名稱。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e5bc5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5bc5-119">-ResourceGroupName</span></span>
<span data-ttu-id="e5bc5-120">指定此 Cmdlet 刪除其變數的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="e5bc5-121">-確認</span><span class="sxs-lookup"><span data-stu-id="e5bc5-121">-Confirm</span></span>
<span data-ttu-id="e5bc5-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5bc5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5bc5-123">-WhatIf</span></span>
<span data-ttu-id="e5bc5-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5bc5-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5bc5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5bc5-126">CommonParameters</span></span>
<span data-ttu-id="e5bc5-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5bc5-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5bc5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5bc5-129">輸入</span><span class="sxs-lookup"><span data-stu-id="e5bc5-129">INPUTS</span></span>

### <span data-ttu-id="e5bc5-130">System.object</span><span class="sxs-lookup"><span data-stu-id="e5bc5-130">System.String</span></span>

## <span data-ttu-id="e5bc5-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e5bc5-131">OUTPUTS</span></span>

### <span data-ttu-id="e5bc5-132">System.void</span><span class="sxs-lookup"><span data-stu-id="e5bc5-132">System.Void</span></span>

## <span data-ttu-id="e5bc5-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e5bc5-133">NOTES</span></span>

## <span data-ttu-id="e5bc5-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5bc5-134">RELATED LINKS</span></span>

[<span data-ttu-id="e5bc5-135">AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e5bc5-135">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="e5bc5-136">新-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e5bc5-136">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="e5bc5-137">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e5bc5-137">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)

