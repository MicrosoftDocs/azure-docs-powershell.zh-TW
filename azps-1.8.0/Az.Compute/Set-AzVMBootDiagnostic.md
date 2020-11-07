---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: 407119856fa670bc4561e06adae32ee806437b1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788314"
---
# <span data-ttu-id="ef7c1-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ef7c1-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="ef7c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef7c1-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7c1-103">修改虛擬機器的啟動診斷屬性。</span><span class="sxs-lookup"><span data-stu-id="ef7c1-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="ef7c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef7c1-104">SYNTAX</span></span>

### <span data-ttu-id="ef7c1-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ef7c1-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef7c1-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ef7c1-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef7c1-107">說明</span><span class="sxs-lookup"><span data-stu-id="ef7c1-107">DESCRIPTION</span></span>
<span data-ttu-id="ef7c1-108">**AzVMBootDiagnostic** Cmdlet 會修改虛擬機器的啟動診斷屬性。</span><span class="sxs-lookup"><span data-stu-id="ef7c1-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="ef7c1-109">示例</span><span class="sxs-lookup"><span data-stu-id="ef7c1-109">EXAMPLES</span></span>

### <span data-ttu-id="ef7c1-110">範例1：啟用啟動診斷程式</span><span class="sxs-lookup"><span data-stu-id="ef7c1-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="ef7c1-111">第一個命令會使用 **AzVM** 來取得名為 ContosoVM07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ef7c1-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="ef7c1-112">該命令會將它儲存在 $VM 變數中。</span><span class="sxs-lookup"><span data-stu-id="ef7c1-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="ef7c1-113">第二個命令會在 $VM 中啟用虛擬機器的引導診斷程式。</span><span class="sxs-lookup"><span data-stu-id="ef7c1-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="ef7c1-114">診斷資料會儲存在指定的帳號中。</span><span class="sxs-lookup"><span data-stu-id="ef7c1-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="ef7c1-115">參數</span><span class="sxs-lookup"><span data-stu-id="ef7c1-115">PARAMETERS</span></span>

### <span data-ttu-id="ef7c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef7c1-116">-DefaultProfile</span></span>
<span data-ttu-id="ef7c1-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef7c1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef7c1-118">-停用</span><span class="sxs-lookup"><span data-stu-id="ef7c1-118">-Disable</span></span>
<span data-ttu-id="ef7c1-119">表示此 Cmdlet 會停用虛擬機器的啟動診斷程式。</span><span class="sxs-lookup"><span data-stu-id="ef7c1-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7c1-120">-啟用</span><span class="sxs-lookup"><span data-stu-id="ef7c1-120">-Enable</span></span>
<span data-ttu-id="ef7c1-121">表示此 Cmdlet 會啟用虛擬機器的啟動診斷程式。</span><span class="sxs-lookup"><span data-stu-id="ef7c1-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7c1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef7c1-122">-ResourceGroupName</span></span>
<span data-ttu-id="ef7c1-123">指定儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef7c1-123">Specifies the name of the resource group of storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef7c1-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ef7c1-124">-StorageAccountName</span></span>
<span data-ttu-id="ef7c1-125">指定儲存啟動診斷資料之儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef7c1-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef7c1-126">-VM</span><span class="sxs-lookup"><span data-stu-id="ef7c1-126">-VM</span></span>
<span data-ttu-id="ef7c1-127">指定此 Cmdlet 變更其啟動診斷的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ef7c1-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="ef7c1-128">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef7c1-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef7c1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7c1-129">CommonParameters</span></span>
<span data-ttu-id="ef7c1-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef7c1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7c1-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ef7c1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7c1-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ef7c1-132">INPUTS</span></span>

### <span data-ttu-id="ef7c1-133">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="ef7c1-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="ef7c1-134">System.object</span><span class="sxs-lookup"><span data-stu-id="ef7c1-134">System.String</span></span>

## <span data-ttu-id="ef7c1-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ef7c1-135">OUTPUTS</span></span>

### <span data-ttu-id="ef7c1-136">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="ef7c1-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ef7c1-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ef7c1-137">NOTES</span></span>

## <span data-ttu-id="ef7c1-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef7c1-138">RELATED LINKS</span></span>

[<span data-ttu-id="ef7c1-139">AzVM</span><span class="sxs-lookup"><span data-stu-id="ef7c1-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ef7c1-140">AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="ef7c1-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)

