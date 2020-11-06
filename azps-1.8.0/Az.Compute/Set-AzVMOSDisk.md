---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: ff6945369f16e9c7996ab9be80dcefce759926a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622672"
---
# <span data-ttu-id="71c61-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="71c61-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="71c61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71c61-102">SYNOPSIS</span></span>
<span data-ttu-id="71c61-103">在虛擬機器上設定作業系統磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="71c61-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="71c61-104">句法</span><span class="sxs-lookup"><span data-stu-id="71c61-104">SYNTAX</span></span>

### <span data-ttu-id="71c61-105">DefaultParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="71c61-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71c61-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="71c61-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71c61-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="71c61-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71c61-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="71c61-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71c61-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="71c61-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71c61-110">說明</span><span class="sxs-lookup"><span data-stu-id="71c61-110">DESCRIPTION</span></span>
<span data-ttu-id="71c61-111">**AzVMOSDisk** Cmdlet 會在虛擬機器上設定作業系統磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="71c61-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="71c61-112">示例</span><span class="sxs-lookup"><span data-stu-id="71c61-112">EXAMPLES</span></span>

### <span data-ttu-id="71c61-113">範例1：從平臺影像設定虛擬機器上的屬性</span><span class="sxs-lookup"><span data-stu-id="71c61-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="71c61-114">第一個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailablitySet13 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="71c61-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="71c61-115">第二個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="71c61-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="71c61-116">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="71c61-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="71c61-117">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="71c61-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="71c61-118">最終命令會在 $VirtualMachine 的虛擬機器上設定屬性。</span><span class="sxs-lookup"><span data-stu-id="71c61-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="71c61-119">範例2：從通用使用者影像設定虛擬機器上的屬性</span><span class="sxs-lookup"><span data-stu-id="71c61-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="71c61-120">第一個命令會在名為 ResourceGroup11 的資源群組中取得名為 AvailablitySet13 的可用性集，並將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="71c61-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="71c61-121">第二個命令會建立一個虛擬電腦物件，並將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="71c61-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="71c61-122">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="71c61-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="71c61-123">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="71c61-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="71c61-124">最終命令會在 $VirtualMachine 的虛擬機器上設定屬性。</span><span class="sxs-lookup"><span data-stu-id="71c61-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="71c61-125">範例3：從特殊的使用者影像設定虛擬機器上的屬性</span><span class="sxs-lookup"><span data-stu-id="71c61-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="71c61-126">第一個命令會在名為 ResourceGroup11 的資源群組中取得名為 AvailablitySet13 的可用性集，並將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="71c61-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="71c61-127">第二個命令會建立一個虛擬電腦物件，並將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="71c61-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="71c61-128">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="71c61-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="71c61-129">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="71c61-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="71c61-130">最終命令會在 $VirtualMachine 的虛擬機器上設定屬性。</span><span class="sxs-lookup"><span data-stu-id="71c61-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="71c61-131">範例4：在虛擬機器作業系統磁片上設定磁片加密設定</span><span class="sxs-lookup"><span data-stu-id="71c61-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="71c61-132">這個範例會設定虛擬機器作業系統磁片上的磁片加密設定。</span><span class="sxs-lookup"><span data-stu-id="71c61-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="71c61-133">參數</span><span class="sxs-lookup"><span data-stu-id="71c61-133">PARAMETERS</span></span>

### <span data-ttu-id="71c61-134">-快取</span><span class="sxs-lookup"><span data-stu-id="71c61-134">-Caching</span></span>
<span data-ttu-id="71c61-135">指定作業系統磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="71c61-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="71c61-136">有效值為：</span><span class="sxs-lookup"><span data-stu-id="71c61-136">Valid values are:</span></span> 
- <span data-ttu-id="71c61-137">唯讀</span><span class="sxs-lookup"><span data-stu-id="71c61-137">ReadOnly</span></span>
- <span data-ttu-id="71c61-138">ReadWrite 的預設值是 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="71c61-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="71c61-139">變更快取值會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="71c61-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="71c61-140">此設定會影響磁片的效能。</span><span class="sxs-lookup"><span data-stu-id="71c61-140">This setting affects the performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c61-141">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="71c61-141">-CreateOption</span></span>
<span data-ttu-id="71c61-142">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片，或附加現有的磁片。</span><span class="sxs-lookup"><span data-stu-id="71c61-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="71c61-143">有效值為：</span><span class="sxs-lookup"><span data-stu-id="71c61-143">Valid values are:</span></span> 
- <span data-ttu-id="71c61-144">選用.</span><span class="sxs-lookup"><span data-stu-id="71c61-144">Attach.</span></span>
<span data-ttu-id="71c61-145">指定此選項以從專用磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="71c61-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="71c61-146">當您指定此選項時，請勿指定 *SourceImageUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="71c61-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="71c61-147">請改為使用 Set-AzVMSourceImage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71c61-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="71c61-148">您也必須使用 *Windows* 或 *Linux* 參數，告知 azure 平臺在 VHD 上的作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="71c61-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="71c61-149">*VhdUri* 參數足以告知 azure 平臺要附加磁片的位置。</span><span class="sxs-lookup"><span data-stu-id="71c61-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="71c61-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="71c61-150">FromImage.</span></span>
<span data-ttu-id="71c61-151">指定此選項以從平臺影像或一般化使用者影像建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="71c61-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="71c61-152">在通用使用者影像的情況下，您也需要指定 *SourceImageUri* 參數，以及 *Windows* 或 *Linux* 參數，以告知 Azure 平臺是作業系統磁片 VHD 的位置和類型，而不是使用 **AzVMSourceImage** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71c61-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="71c61-153">如果是平臺影像，則 *VhdUri* 參數就足夠了。</span><span class="sxs-lookup"><span data-stu-id="71c61-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="71c61-154">有空.</span><span class="sxs-lookup"><span data-stu-id="71c61-154">Empty.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c61-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71c61-155">-DefaultProfile</span></span>
<span data-ttu-id="71c61-156">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71c61-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71c61-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="71c61-157">-DiffDiskSetting</span></span>
<span data-ttu-id="71c61-158">指定作業系統磁片的差異磁片設定。</span><span class="sxs-lookup"><span data-stu-id="71c61-158">Specifies the differencing disk settings for operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71c61-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="71c61-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="71c61-160">指定磁片加密金鑰的位置。</span><span class="sxs-lookup"><span data-stu-id="71c61-160">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c61-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="71c61-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="71c61-162">指定包含磁片加密金鑰之主要電子倉庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="71c61-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c61-163">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="71c61-163">-DiskSizeInGB</span></span>
<span data-ttu-id="71c61-164">指定作業系統磁片的大小（以 GB 為來）。</span><span class="sxs-lookup"><span data-stu-id="71c61-164">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c61-165">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="71c61-165">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="71c61-166">指定金鑰加密金鑰的位置。</span><span class="sxs-lookup"><span data-stu-id="71c61-166">Specifies the location of the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c61-167">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="71c61-167">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="71c61-168">指定包含金鑰加密金鑰的主要保存庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="71c61-168">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c61-169">-Linux</span><span class="sxs-lookup"><span data-stu-id="71c61-169">-Linux</span></span>
<span data-ttu-id="71c61-170">表示使用者影像上的作業系統是 Linux。</span><span class="sxs-lookup"><span data-stu-id="71c61-170">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="71c61-171">針對以使用者映射為基礎的虛擬機器部署指定此參數。</span><span class="sxs-lookup"><span data-stu-id="71c61-171">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c61-172">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="71c61-172">-ManagedDiskId</span></span>
<span data-ttu-id="71c61-173">指定受管理磁片的 ID。</span><span class="sxs-lookup"><span data-stu-id="71c61-173">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="71c61-174">-名稱</span><span class="sxs-lookup"><span data-stu-id="71c61-174">-Name</span></span>
<span data-ttu-id="71c61-175">指定作業系統磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="71c61-175">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c61-176">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="71c61-176">-SourceImageUri</span></span>
<span data-ttu-id="71c61-177">指定使用者影像案例的 VHD URI。</span><span class="sxs-lookup"><span data-stu-id="71c61-177">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c61-178">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="71c61-178">-StorageAccountType</span></span>
<span data-ttu-id="71c61-179">指定受管理磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="71c61-179">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="71c61-180">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="71c61-180">-VhdUri</span></span>
<span data-ttu-id="71c61-181">指定虛擬硬碟 (VHD)  (URI) 的統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="71c61-181">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="71c61-182">針對以影像為基礎的虛擬機器，此參數會指定要在指定平臺影像或使用者影像時建立的 VHD 檔案。</span><span class="sxs-lookup"><span data-stu-id="71c61-182">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="71c61-183">此位置是複製影像二進位大型物件 (BLOB) 的位置，以啟動虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="71c61-183">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="71c61-184">針對以磁片為基礎的虛擬電腦啟動案例，此參數會指定虛擬機器直接用來啟動的 VHD 檔案。</span><span class="sxs-lookup"><span data-stu-id="71c61-184">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c61-185">-VM</span><span class="sxs-lookup"><span data-stu-id="71c61-185">-VM</span></span>
<span data-ttu-id="71c61-186">指定要設定作業系統磁片屬性的本機虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="71c61-186">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="71c61-187">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71c61-187">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71c61-188">-Windows</span><span class="sxs-lookup"><span data-stu-id="71c61-188">-Windows</span></span>
<span data-ttu-id="71c61-189">表示使用者影像上的作業系統是 Windows。</span><span class="sxs-lookup"><span data-stu-id="71c61-189">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c61-190">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="71c61-190">-WriteAccelerator</span></span>
<span data-ttu-id="71c61-191">指定是否應該在 OS 磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="71c61-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="71c61-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c61-192">CommonParameters</span></span>
<span data-ttu-id="71c61-193">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71c61-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c61-194">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="71c61-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c61-195">輸入</span><span class="sxs-lookup"><span data-stu-id="71c61-195">INPUTS</span></span>

### <span data-ttu-id="71c61-196">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="71c61-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="71c61-197">System.object</span><span class="sxs-lookup"><span data-stu-id="71c61-197">System.String</span></span>

## <span data-ttu-id="71c61-198">輸出</span><span class="sxs-lookup"><span data-stu-id="71c61-198">OUTPUTS</span></span>

### <span data-ttu-id="71c61-199">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="71c61-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="71c61-200">筆記</span><span class="sxs-lookup"><span data-stu-id="71c61-200">NOTES</span></span>

## <span data-ttu-id="71c61-201">相關連結</span><span class="sxs-lookup"><span data-stu-id="71c61-201">RELATED LINKS</span></span>

[<span data-ttu-id="71c61-202">AzVM</span><span class="sxs-lookup"><span data-stu-id="71c61-202">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="71c61-203">AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="71c61-203">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="71c61-204">新-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="71c61-204">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

