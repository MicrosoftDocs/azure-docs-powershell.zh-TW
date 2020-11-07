---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 77ac953e1b67ea896f15b13a2695505aabc05bbb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957424"
---
# <span data-ttu-id="2b97a-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="2b97a-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="2b97a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b97a-102">SYNOPSIS</span></span>
<span data-ttu-id="2b97a-103">在 VM 上執行命令。</span><span class="sxs-lookup"><span data-stu-id="2b97a-103">Run a command on the VM.</span></span>

## <span data-ttu-id="2b97a-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b97a-104">SYNTAX</span></span>

### <span data-ttu-id="2b97a-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="2b97a-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b97a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2b97a-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b97a-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="2b97a-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b97a-108">說明</span><span class="sxs-lookup"><span data-stu-id="2b97a-108">DESCRIPTION</span></span>
<span data-ttu-id="2b97a-109">在 VM 上喚醒 [執行] 命令。</span><span class="sxs-lookup"><span data-stu-id="2b97a-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="2b97a-110">示例</span><span class="sxs-lookup"><span data-stu-id="2b97a-110">EXAMPLES</span></span>

### <span data-ttu-id="2b97a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2b97a-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -VMName 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="2b97a-112">在資源群組 [rgname] 中，sample.ps1 使用 [vmname] 的 VM 中的 [RunPowerShellScript] 和 [VM] 中的參數，來喚醒呼叫 [執行] 命令。</span><span class="sxs-lookup"><span data-stu-id="2b97a-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="2b97a-113">參數</span><span class="sxs-lookup"><span data-stu-id="2b97a-113">PARAMETERS</span></span>

### <span data-ttu-id="2b97a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b97a-114">-AsJob</span></span>
<span data-ttu-id="2b97a-115">在背景中執行 Cmdlet，然後返回工作物件來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="2b97a-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="2b97a-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="2b97a-116">-CommandId</span></span>
<span data-ttu-id="2b97a-117">[執行] 命令 ID。</span><span class="sxs-lookup"><span data-stu-id="2b97a-117">The run command ID.</span></span>

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

### <span data-ttu-id="2b97a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b97a-118">-DefaultProfile</span></span>
<span data-ttu-id="2b97a-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b97a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b97a-120">-參數</span><span class="sxs-lookup"><span data-stu-id="2b97a-120">-Parameter</span></span>
<span data-ttu-id="2b97a-121">Run 命令參數。</span><span class="sxs-lookup"><span data-stu-id="2b97a-121">The run command parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b97a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b97a-122">-ResourceGroupName</span></span>
<span data-ttu-id="2b97a-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b97a-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="2b97a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b97a-124">-ResourceId</span></span>
<span data-ttu-id="2b97a-125">VM 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b97a-125">The resource ID for the VM.</span></span>

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

### <span data-ttu-id="2b97a-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="2b97a-126">-ScriptPath</span></span>
<span data-ttu-id="2b97a-127">要執行之腳本的路徑。</span><span class="sxs-lookup"><span data-stu-id="2b97a-127">Path of the script to be executed.</span></span>  <span data-ttu-id="2b97a-128">指定此值時，指定的腳本會覆寫命令的預設腳本。</span><span class="sxs-lookup"><span data-stu-id="2b97a-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="2b97a-129">-VM</span><span class="sxs-lookup"><span data-stu-id="2b97a-129">-VM</span></span>
<span data-ttu-id="2b97a-130">PS 虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="2b97a-130">The PS virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b97a-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="2b97a-131">-VMName</span></span>
<span data-ttu-id="2b97a-132">虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b97a-132">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="2b97a-133">-確認</span><span class="sxs-lookup"><span data-stu-id="2b97a-133">-Confirm</span></span>
<span data-ttu-id="2b97a-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2b97a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b97a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b97a-135">-WhatIf</span></span>
<span data-ttu-id="2b97a-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2b97a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b97a-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b97a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b97a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b97a-138">CommonParameters</span></span>
<span data-ttu-id="2b97a-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b97a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b97a-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2b97a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b97a-141">輸入</span><span class="sxs-lookup"><span data-stu-id="2b97a-141">INPUTS</span></span>

### <span data-ttu-id="2b97a-142">System.object</span><span class="sxs-lookup"><span data-stu-id="2b97a-142">System.String</span></span>

### <span data-ttu-id="2b97a-143">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="2b97a-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2b97a-144">輸出</span><span class="sxs-lookup"><span data-stu-id="2b97a-144">OUTPUTS</span></span>

### <span data-ttu-id="2b97a-145">PSRunCommandResult 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="2b97a-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="2b97a-146">筆記</span><span class="sxs-lookup"><span data-stu-id="2b97a-146">NOTES</span></span>

## <span data-ttu-id="2b97a-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b97a-147">RELATED LINKS</span></span>