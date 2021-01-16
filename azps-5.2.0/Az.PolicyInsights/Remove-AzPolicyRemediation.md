---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 969b764be302231f33dda00b32afb79ec04a324e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285007"
---
# <span data-ttu-id="a0200-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="a0200-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="a0200-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0200-102">SYNOPSIS</span></span>
<span data-ttu-id="a0200-103">刪除原則修正。</span><span class="sxs-lookup"><span data-stu-id="a0200-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="a0200-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0200-104">SYNTAX</span></span>

### <span data-ttu-id="a0200-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="a0200-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0200-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a0200-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0200-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a0200-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0200-108">說明</span><span class="sxs-lookup"><span data-stu-id="a0200-108">DESCRIPTION</span></span>
<span data-ttu-id="a0200-109">**AzPolicyRemediation** Cmdlet 會刪除原則修正。</span><span class="sxs-lookup"><span data-stu-id="a0200-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="a0200-110">示例</span><span class="sxs-lookup"><span data-stu-id="a0200-110">EXAMPLES</span></span>

### <span data-ttu-id="a0200-111">範例1：在資源群組範圍刪除原則修正</span><span class="sxs-lookup"><span data-stu-id="a0200-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="a0200-112">這個命令會在資源群組 ' myRG ' 中刪除名為「remediation1」的修正。</span><span class="sxs-lookup"><span data-stu-id="a0200-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="a0200-113">範例2：透過 [管道] 刪除管理群組修正</span><span class="sxs-lookup"><span data-stu-id="a0200-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="a0200-114">這個命令會從管理組 "mg1" 刪除名為「remediation1」的修正。</span><span class="sxs-lookup"><span data-stu-id="a0200-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="a0200-115">刪除資源前，會出現確認提示。</span><span class="sxs-lookup"><span data-stu-id="a0200-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="a0200-116">範例3：取消並刪除原則修正</span><span class="sxs-lookup"><span data-stu-id="a0200-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="a0200-117">這個命令會在資源群組 ' myRG ' 中刪除名為「remediation1」的修正。</span><span class="sxs-lookup"><span data-stu-id="a0200-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="a0200-118">如果修正程式正在進行中，將會取消，然後才會被刪除。</span><span class="sxs-lookup"><span data-stu-id="a0200-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="a0200-119">參數</span><span class="sxs-lookup"><span data-stu-id="a0200-119">PARAMETERS</span></span>

### <span data-ttu-id="a0200-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="a0200-120">-AllowStop</span></span>
<span data-ttu-id="a0200-121">允許修正程式在進行中時取消。</span><span class="sxs-lookup"><span data-stu-id="a0200-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="a0200-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0200-122">-AsJob</span></span>
<span data-ttu-id="a0200-123">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0200-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a0200-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0200-124">-DefaultProfile</span></span>
<span data-ttu-id="a0200-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0200-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0200-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0200-126">-InputObject</span></span>
<span data-ttu-id="a0200-127">修正物件。</span><span class="sxs-lookup"><span data-stu-id="a0200-127">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0200-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a0200-128">-ManagementGroupName</span></span>
<span data-ttu-id="a0200-129">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0200-129">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0200-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0200-130">-Name</span></span>
<span data-ttu-id="a0200-131">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a0200-131">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0200-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0200-132">-PassThru</span></span>
<span data-ttu-id="a0200-133">如果命令順利完成，則傳回 True。</span><span class="sxs-lookup"><span data-stu-id="a0200-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="a0200-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0200-134">-ResourceGroupName</span></span>
<span data-ttu-id="a0200-135">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a0200-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0200-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0200-136">-ResourceId</span></span>
<span data-ttu-id="a0200-137">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="a0200-137">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0200-138">-範圍</span><span class="sxs-lookup"><span data-stu-id="a0200-138">-Scope</span></span>
<span data-ttu-id="a0200-139">資源範圍。</span><span class="sxs-lookup"><span data-stu-id="a0200-139">Scope of the resource.</span></span>
<span data-ttu-id="a0200-140">例如.</span><span class="sxs-lookup"><span data-stu-id="a0200-140">E.g.</span></span>
<span data-ttu-id="a0200-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="a0200-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0200-142">-確認</span><span class="sxs-lookup"><span data-stu-id="a0200-142">-Confirm</span></span>
<span data-ttu-id="a0200-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0200-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0200-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0200-144">-WhatIf</span></span>
<span data-ttu-id="a0200-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0200-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0200-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0200-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0200-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0200-147">CommonParameters</span></span>
<span data-ttu-id="a0200-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0200-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0200-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a0200-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0200-150">輸入</span><span class="sxs-lookup"><span data-stu-id="a0200-150">INPUTS</span></span>

### <span data-ttu-id="a0200-151">System.object</span><span class="sxs-lookup"><span data-stu-id="a0200-151">System.String</span></span>

### <span data-ttu-id="a0200-152">PSRemediation 中的 PolicyInsights。</span><span class="sxs-lookup"><span data-stu-id="a0200-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="a0200-153">輸出</span><span class="sxs-lookup"><span data-stu-id="a0200-153">OUTPUTS</span></span>

### <span data-ttu-id="a0200-154">System.object</span><span class="sxs-lookup"><span data-stu-id="a0200-154">System.Boolean</span></span>

## <span data-ttu-id="a0200-155">筆記</span><span class="sxs-lookup"><span data-stu-id="a0200-155">NOTES</span></span>

## <span data-ttu-id="a0200-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0200-156">RELATED LINKS</span></span>