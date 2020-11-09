---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: c1fbc45a9d82733f73a13b13985bdd6746f4c075
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284543"
---
# <span data-ttu-id="653ed-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="653ed-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="653ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="653ed-102">SYNOPSIS</span></span>
<span data-ttu-id="653ed-103">設定 VMSS 的 orchestration 服務狀態。</span><span class="sxs-lookup"><span data-stu-id="653ed-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="653ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="653ed-104">SYNTAX</span></span>

### <span data-ttu-id="653ed-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="653ed-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="653ed-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="653ed-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="653ed-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="653ed-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="653ed-108">說明</span><span class="sxs-lookup"><span data-stu-id="653ed-108">DESCRIPTION</span></span>
<span data-ttu-id="653ed-109">設定 VMSS 的 orchestration 服務狀態。</span><span class="sxs-lookup"><span data-stu-id="653ed-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="653ed-110">示例</span><span class="sxs-lookup"><span data-stu-id="653ed-110">EXAMPLES</span></span>

### <span data-ttu-id="653ed-111">範例1</span><span class="sxs-lookup"><span data-stu-id="653ed-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="653ed-112">這個命令會在資源群組 "rg" 中的 VMSS "vmss1" 暫停自動修復服務。</span><span class="sxs-lookup"><span data-stu-id="653ed-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="653ed-113">範例2</span><span class="sxs-lookup"><span data-stu-id="653ed-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="653ed-114">這個命令會在資源群組 "rg" 中的 VMSS "vmss1" 上，繼續執行自動修復服務。</span><span class="sxs-lookup"><span data-stu-id="653ed-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="653ed-115">參數</span><span class="sxs-lookup"><span data-stu-id="653ed-115">PARAMETERS</span></span>

### <span data-ttu-id="653ed-116">-動作</span><span class="sxs-lookup"><span data-stu-id="653ed-116">-Action</span></span>
<span data-ttu-id="653ed-117">要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="653ed-117">The action to be performed.</span></span>  <span data-ttu-id="653ed-118">可能的值為： [繼續]、[暫停]。</span><span class="sxs-lookup"><span data-stu-id="653ed-118">Possible values are: Resume, Suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="653ed-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="653ed-119">-AsJob</span></span>
<span data-ttu-id="653ed-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="653ed-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="653ed-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="653ed-121">-DefaultProfile</span></span>
<span data-ttu-id="653ed-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="653ed-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="653ed-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="653ed-123">-InputObject</span></span>
<span data-ttu-id="653ed-124">虛擬機器縮放集的本機物件。</span><span class="sxs-lookup"><span data-stu-id="653ed-124">The local object of the virtual machine scale set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="653ed-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="653ed-125">-ResourceGroupName</span></span>
<span data-ttu-id="653ed-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="653ed-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="653ed-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="653ed-127">-ResourceId</span></span>
<span data-ttu-id="653ed-128">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="653ed-128">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="653ed-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="653ed-129">-ServiceName</span></span>
<span data-ttu-id="653ed-130">服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="653ed-130">The name of the service.</span></span>

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

### <span data-ttu-id="653ed-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="653ed-131">-VMScaleSetName</span></span>
<span data-ttu-id="653ed-132">虛擬機器規模集的名稱。</span><span class="sxs-lookup"><span data-stu-id="653ed-132">The name of the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="653ed-133">-確認</span><span class="sxs-lookup"><span data-stu-id="653ed-133">-Confirm</span></span>
<span data-ttu-id="653ed-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="653ed-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="653ed-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="653ed-135">-WhatIf</span></span>
<span data-ttu-id="653ed-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="653ed-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="653ed-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="653ed-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="653ed-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="653ed-138">CommonParameters</span></span>
<span data-ttu-id="653ed-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="653ed-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="653ed-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="653ed-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="653ed-141">輸入</span><span class="sxs-lookup"><span data-stu-id="653ed-141">INPUTS</span></span>

### <span data-ttu-id="653ed-142">System.object</span><span class="sxs-lookup"><span data-stu-id="653ed-142">System.String</span></span>

### <span data-ttu-id="653ed-143">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="653ed-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="653ed-144">輸出</span><span class="sxs-lookup"><span data-stu-id="653ed-144">OUTPUTS</span></span>

### <span data-ttu-id="653ed-145">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="653ed-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="653ed-146">筆記</span><span class="sxs-lookup"><span data-stu-id="653ed-146">NOTES</span></span>

## <span data-ttu-id="653ed-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="653ed-147">RELATED LINKS</span></span>