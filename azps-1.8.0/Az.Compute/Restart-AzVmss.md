---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: 61bd867f7790f47599ac10ebd6523327e4e1868a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622708"
---
# <span data-ttu-id="f6339-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f6339-101">Restart-AzVmss</span></span>

## <span data-ttu-id="f6339-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6339-102">SYNOPSIS</span></span>
<span data-ttu-id="f6339-103">重新開機 VMSS 或 VMSS 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f6339-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="f6339-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6339-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6339-105">說明</span><span class="sxs-lookup"><span data-stu-id="f6339-105">DESCRIPTION</span></span>
<span data-ttu-id="f6339-106">**Restart AzVmss** Cmdlet 會重新開機虛擬機器縮放集 (VMSS) 。</span><span class="sxs-lookup"><span data-stu-id="f6339-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="f6339-107">這個 Cmdlet 也可以用來在 VMSS 內使用 *InstanceId* 參數重新開機特定的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f6339-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="f6339-108">示例</span><span class="sxs-lookup"><span data-stu-id="f6339-108">EXAMPLES</span></span>

### <span data-ttu-id="f6339-109">範例1：重新開機 VMSS</span><span class="sxs-lookup"><span data-stu-id="f6339-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="f6339-110">這個命令會重新開機屬於名為 Group001 之資源群組的名為 VMSS001 的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="f6339-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="f6339-111">範例2：在 VMSS 中重新開機特定的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="f6339-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="f6339-112">這個命令會在屬於名為 Group001 之資源群組的名稱為 VMSS 的 VMSS001 中，重新開機實例識別碼為1的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f6339-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="f6339-113">參數</span><span class="sxs-lookup"><span data-stu-id="f6339-113">PARAMETERS</span></span>

### <span data-ttu-id="f6339-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6339-114">-AsJob</span></span>
<span data-ttu-id="f6339-115">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="f6339-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f6339-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6339-116">-DefaultProfile</span></span>
<span data-ttu-id="f6339-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6339-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6339-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f6339-118">-InstanceId</span></span>
<span data-ttu-id="f6339-119">指定為字串陣列（需要重新開機的實例識別碼）。</span><span class="sxs-lookup"><span data-stu-id="f6339-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6339-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6339-120">-ResourceGroupName</span></span>
<span data-ttu-id="f6339-121">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6339-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="f6339-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f6339-122">-VMScaleSetName</span></span>
<span data-ttu-id="f6339-123">Species 此 Cmdlet 重新開機之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6339-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6339-124">-確認</span><span class="sxs-lookup"><span data-stu-id="f6339-124">-Confirm</span></span>
<span data-ttu-id="f6339-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f6339-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6339-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6339-126">-WhatIf</span></span>
<span data-ttu-id="f6339-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6339-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6339-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6339-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6339-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6339-129">CommonParameters</span></span>
<span data-ttu-id="f6339-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6339-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6339-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6339-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6339-132">輸入</span><span class="sxs-lookup"><span data-stu-id="f6339-132">INPUTS</span></span>

### <span data-ttu-id="f6339-133">System.object</span><span class="sxs-lookup"><span data-stu-id="f6339-133">System.String</span></span>

### <span data-ttu-id="f6339-134">System.object []</span><span class="sxs-lookup"><span data-stu-id="f6339-134">System.String[]</span></span>

## <span data-ttu-id="f6339-135">輸出</span><span class="sxs-lookup"><span data-stu-id="f6339-135">OUTPUTS</span></span>

### <span data-ttu-id="f6339-136">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="f6339-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f6339-137">筆記</span><span class="sxs-lookup"><span data-stu-id="f6339-137">NOTES</span></span>

## <span data-ttu-id="f6339-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6339-138">RELATED LINKS</span></span>

[<span data-ttu-id="f6339-139">AzVmss</span><span class="sxs-lookup"><span data-stu-id="f6339-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="f6339-140">新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f6339-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="f6339-141">移除-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f6339-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="f6339-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f6339-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="f6339-143">開始-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f6339-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="f6339-144">停止 AzVmss</span><span class="sxs-lookup"><span data-stu-id="f6339-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="f6339-145">更新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f6339-145">Update-AzVmss</span></span>](./Update-AzVmss.md)

