---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: b927e9b61e4d76795e35f2356b900b959a94e082
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795873"
---
# <span data-ttu-id="d792a-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d792a-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="d792a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d792a-102">SYNOPSIS</span></span>
<span data-ttu-id="d792a-103">修改虛擬機器資料磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="d792a-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="d792a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d792a-104">SYNTAX</span></span>

### <span data-ttu-id="d792a-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="d792a-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d792a-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="d792a-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d792a-107">說明</span><span class="sxs-lookup"><span data-stu-id="d792a-107">DESCRIPTION</span></span>
<span data-ttu-id="d792a-108">**AzVMDataDisk** Cmdlet 會修改虛擬機器資料磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="d792a-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="d792a-109">示例</span><span class="sxs-lookup"><span data-stu-id="d792a-109">EXAMPLES</span></span>

### <span data-ttu-id="d792a-110">範例1：修改資料磁片的快取模式</span><span class="sxs-lookup"><span data-stu-id="d792a-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="d792a-111">第一個命令會使用 **AzVM** 來取得名為 ContosoVM07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d792a-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="d792a-112">該命令會將它儲存在 $VM 變數中。</span><span class="sxs-lookup"><span data-stu-id="d792a-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="d792a-113">第二個命令會修改 $VM 虛擬機器上名為 DataDisk01 之資料磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="d792a-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="d792a-114">命令會將結果傳遞給 Update-AzVM Cmdlet，以執行您的變更。</span><span class="sxs-lookup"><span data-stu-id="d792a-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="d792a-115">對 cashing 模式所做的變更會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="d792a-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="d792a-116">參數</span><span class="sxs-lookup"><span data-stu-id="d792a-116">PARAMETERS</span></span>

### <span data-ttu-id="d792a-117">-快取</span><span class="sxs-lookup"><span data-stu-id="d792a-117">-Caching</span></span>
<span data-ttu-id="d792a-118">指定磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="d792a-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="d792a-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d792a-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d792a-120">唯讀</span><span class="sxs-lookup"><span data-stu-id="d792a-120">ReadOnly</span></span>
- <span data-ttu-id="d792a-121">讀</span><span class="sxs-lookup"><span data-stu-id="d792a-121">ReadWrite</span></span>

<span data-ttu-id="d792a-122">預設值為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="d792a-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="d792a-123">變更此值會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="d792a-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="d792a-124">此設定會影響磁片的一致性和效能。</span><span class="sxs-lookup"><span data-stu-id="d792a-124">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d792a-125">-DefaultProfile</span></span>
<span data-ttu-id="d792a-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d792a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="d792a-127">-DiskSizeInGB</span></span>
<span data-ttu-id="d792a-128">指定資料磁片的大小（以 gb 為數）。</span><span class="sxs-lookup"><span data-stu-id="d792a-128">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="d792a-129">-Lun</span></span>
<span data-ttu-id="d792a-130">指定此 Cmdlet 所修改之資料磁片的邏輯單元號碼 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="d792a-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: ChangeWithLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="d792a-131">-Name</span></span>
<span data-ttu-id="d792a-132">指定此 Cmdlet 所修改之資料磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="d792a-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ChangeWithName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d792a-133">-StorageAccountType</span></span>
<span data-ttu-id="d792a-134">虛擬機器受管理磁片的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="d792a-134">The virtual machine managed disk's account type.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-135">-VM</span><span class="sxs-lookup"><span data-stu-id="d792a-135">-VM</span></span>
<span data-ttu-id="d792a-136">指定此 Cmdlet 修改資料磁片的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d792a-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="d792a-137">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d792a-137">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="d792a-138">-WriteAccelerator</span></span>
<span data-ttu-id="d792a-139">指定是否應該在資料磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="d792a-139">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d792a-140">CommonParameters</span></span>
<span data-ttu-id="d792a-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d792a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d792a-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d792a-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d792a-143">輸入</span><span class="sxs-lookup"><span data-stu-id="d792a-143">INPUTS</span></span>

### <span data-ttu-id="d792a-144">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d792a-144">PSVirtualMachine</span></span>
<span data-ttu-id="d792a-145">[VM "參數從管線接受類型 ' PSVirtualMachine」的值</span><span class="sxs-lookup"><span data-stu-id="d792a-145">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="d792a-146">輸出</span><span class="sxs-lookup"><span data-stu-id="d792a-146">OUTPUTS</span></span>

### <span data-ttu-id="d792a-147">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="d792a-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d792a-148">筆記</span><span class="sxs-lookup"><span data-stu-id="d792a-148">NOTES</span></span>

## <span data-ttu-id="d792a-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="d792a-149">RELATED LINKS</span></span>

[<span data-ttu-id="d792a-150">AzVM</span><span class="sxs-lookup"><span data-stu-id="d792a-150">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d792a-151">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="d792a-151">Update-AzVM</span></span>](./Update-AzVM.md)

