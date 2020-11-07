---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: 534b565e7fc77b1c8764b372675a7d8c4674b571
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959597"
---
# <span data-ttu-id="4e914-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4e914-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="4e914-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e914-102">SYNOPSIS</span></span>
<span data-ttu-id="4e914-103">從虛擬電腦縮放設定 VM 中移除資料磁片</span><span class="sxs-lookup"><span data-stu-id="4e914-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="4e914-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e914-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e914-105">說明</span><span class="sxs-lookup"><span data-stu-id="4e914-105">DESCRIPTION</span></span>
<span data-ttu-id="4e914-106">**AzVmssVMDataDisk** Cmdlet 會從 vm SCALE 集合 VM 中移除資料磁片</span><span class="sxs-lookup"><span data-stu-id="4e914-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="4e914-107">示例</span><span class="sxs-lookup"><span data-stu-id="4e914-107">EXAMPLES</span></span>

### <span data-ttu-id="4e914-108">範例1：從 VM 規模集合 VM 移除資料磁片</span><span class="sxs-lookup"><span data-stu-id="4e914-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="4e914-109">由資源群組名稱指定的現有 Vmss VM （Vmss 名稱和實例識別碼）所 getsan 的第一個命令。</span><span class="sxs-lookup"><span data-stu-id="4e914-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="4e914-110">第二個命令會將資料磁片 lun 0 從儲存在 $VmssVM 最終指令中的 VM 比例集 VM 中移除，並以已移除的資料磁片來更新 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="4e914-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="4e914-111">參數</span><span class="sxs-lookup"><span data-stu-id="4e914-111">PARAMETERS</span></span>

### <span data-ttu-id="4e914-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e914-112">-DefaultProfile</span></span>
<span data-ttu-id="4e914-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e914-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e914-114">-Lun</span><span class="sxs-lookup"><span data-stu-id="4e914-114">-Lun</span></span>
<span data-ttu-id="4e914-115">指定磁片的邏輯單元號碼。</span><span class="sxs-lookup"><span data-stu-id="4e914-115">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e914-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="4e914-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="4e914-117">虛擬機器縮放設定 VM 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4e914-117">The virtual machine scale set VM profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e914-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e914-118">CommonParameters</span></span>
<span data-ttu-id="4e914-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e914-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e914-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4e914-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e914-121">輸入</span><span class="sxs-lookup"><span data-stu-id="4e914-121">INPUTS</span></span>

### <span data-ttu-id="4e914-122">PSVirtualMachineScaleSetVM 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="4e914-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="4e914-123">輸出</span><span class="sxs-lookup"><span data-stu-id="4e914-123">OUTPUTS</span></span>

### <span data-ttu-id="4e914-124">PSVirtualMachineScaleSetVM 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="4e914-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="4e914-125">筆記</span><span class="sxs-lookup"><span data-stu-id="4e914-125">NOTES</span></span>

## <span data-ttu-id="4e914-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e914-126">RELATED LINKS</span></span>