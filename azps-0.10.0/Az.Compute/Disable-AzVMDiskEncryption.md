---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 6a14a8472ca33fe9dbb15aa2ddf58208764a5a6f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796334"
---
# <span data-ttu-id="9314c-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="9314c-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="9314c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9314c-102">SYNOPSIS</span></span>
<span data-ttu-id="9314c-103">停用 IaaS 虛擬機器上的加密。</span><span class="sxs-lookup"><span data-stu-id="9314c-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="9314c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9314c-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9314c-105">說明</span><span class="sxs-lookup"><span data-stu-id="9314c-105">DESCRIPTION</span></span>
<span data-ttu-id="9314c-106">**Disable AzVMDiskEncryption** Cmdlet 會將基礎結構上的加密停成服務 (IaaS) 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="9314c-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="9314c-107">這個 Cmdlet 只在 Windows 虛擬電腦（而不是 Linux 虛擬機器）上受到支援。</span><span class="sxs-lookup"><span data-stu-id="9314c-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="9314c-108">這個 Cmdlet 會在虛擬機器上安裝擴充功能，以停用加密。</span><span class="sxs-lookup"><span data-stu-id="9314c-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="9314c-109">如果未指定 *Name* 參數，則會建立預設名稱為「AzureDiskEncryption For Windows vm」的副檔名。</span><span class="sxs-lookup"><span data-stu-id="9314c-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="9314c-110">注意：此 Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="9314c-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="9314c-111">示例</span><span class="sxs-lookup"><span data-stu-id="9314c-111">EXAMPLES</span></span>

### <span data-ttu-id="9314c-112">範例1：針對 Windows 虛擬機器上的所有磁片停用加密</span><span class="sxs-lookup"><span data-stu-id="9314c-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="9314c-113">這個命令會針對屬於名為 Group001 之資源群組的名稱為 VM002 的虛擬機器，停用對 all 類型的磁片加密。</span><span class="sxs-lookup"><span data-stu-id="9314c-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="9314c-114">由於未指定 *VolumeType* 參數，因此 Cmdlet 會將值設定為 All。</span><span class="sxs-lookup"><span data-stu-id="9314c-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="9314c-115">範例2：停用 Windows 虛擬機器上的資料量加密</span><span class="sxs-lookup"><span data-stu-id="9314c-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="9314c-116">這個命令會針對名為「Group002」資源群組的名為 VM004 的虛擬機器，停用針對類型資料的加密量。</span><span class="sxs-lookup"><span data-stu-id="9314c-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="9314c-117">參數</span><span class="sxs-lookup"><span data-stu-id="9314c-117">PARAMETERS</span></span>

### <span data-ttu-id="9314c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9314c-118">-DefaultProfile</span></span>
<span data-ttu-id="9314c-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9314c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9314c-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="9314c-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="9314c-121">表示此 Cmdlet 會停用延伸次要版本的自動升級。</span><span class="sxs-lookup"><span data-stu-id="9314c-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9314c-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="9314c-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="9314c-123">延伸發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="9314c-123">The extension publisher name.</span></span> <span data-ttu-id="9314c-124">指定此參數，只會覆寫「Microsoft Azure. Security」的預設值。</span><span class="sxs-lookup"><span data-stu-id="9314c-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9314c-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="9314c-125">-ExtensionType</span></span>
<span data-ttu-id="9314c-126">延伸類型。</span><span class="sxs-lookup"><span data-stu-id="9314c-126">The extension type.</span></span> <span data-ttu-id="9314c-127">指定此參數可覆寫 Windows Vm 的 "AzureDiskEncryption" 的預設值，以及 Linux Vm 的 "AzureDiskEncryptionForLinux"。</span><span class="sxs-lookup"><span data-stu-id="9314c-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9314c-128">-Force</span><span class="sxs-lookup"><span data-stu-id="9314c-128">-Force</span></span>
<span data-ttu-id="9314c-129">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="9314c-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9314c-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="9314c-130">-Name</span></span>
<span data-ttu-id="9314c-131">Specifes 代表副檔名的 Azure 資源管理器 (ARM) 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="9314c-131">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="9314c-132">如果未指定此參數，此 Cmdlet 預設為「Windows Vm 的 AzureDiskEncryption」。</span><span class="sxs-lookup"><span data-stu-id="9314c-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9314c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9314c-133">-ResourceGroupName</span></span>
<span data-ttu-id="9314c-134">指定虛擬機器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9314c-134">Specifies the resource group name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9314c-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="9314c-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="9314c-136">指定加密延伸的版本。</span><span class="sxs-lookup"><span data-stu-id="9314c-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="9314c-137">如果您沒有指定此參數的值，就會使用最新版本的延伸。</span><span class="sxs-lookup"><span data-stu-id="9314c-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9314c-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="9314c-138">-VMName</span></span>
<span data-ttu-id="9314c-139">指定此 Cmdlet 停用加密的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="9314c-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9314c-140">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="9314c-140">-VolumeType</span></span>
<span data-ttu-id="9314c-141">指定要執行加密操作的虛擬機器體積類型。</span><span class="sxs-lookup"><span data-stu-id="9314c-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="9314c-142">針對 Windows 虛擬機器，有效值為：</span><span class="sxs-lookup"><span data-stu-id="9314c-142">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="9314c-143">同時</span><span class="sxs-lookup"><span data-stu-id="9314c-143">All</span></span>
- <span data-ttu-id="9314c-144">OS</span><span class="sxs-lookup"><span data-stu-id="9314c-144">OS</span></span>
- <span data-ttu-id="9314c-145">資料.</span><span class="sxs-lookup"><span data-stu-id="9314c-145">Data.</span></span>
<span data-ttu-id="9314c-146">如果您沒有指定此參數的值，則會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="9314c-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="9314c-147">Linux 目前不支援 [停用加密]。</span><span class="sxs-lookup"><span data-stu-id="9314c-147">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9314c-148">-確認</span><span class="sxs-lookup"><span data-stu-id="9314c-148">-Confirm</span></span>
<span data-ttu-id="9314c-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9314c-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9314c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9314c-150">-WhatIf</span></span>
<span data-ttu-id="9314c-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9314c-151">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9314c-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9314c-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9314c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9314c-153">CommonParameters</span></span>
<span data-ttu-id="9314c-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9314c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9314c-155">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9314c-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9314c-156">輸入</span><span class="sxs-lookup"><span data-stu-id="9314c-156">INPUTS</span></span>

### <span data-ttu-id="9314c-157">所有</span><span class="sxs-lookup"><span data-stu-id="9314c-157">None</span></span>
<span data-ttu-id="9314c-158">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9314c-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9314c-159">輸出</span><span class="sxs-lookup"><span data-stu-id="9314c-159">OUTPUTS</span></span>

### <span data-ttu-id="9314c-160">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="9314c-160">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="9314c-161">筆記</span><span class="sxs-lookup"><span data-stu-id="9314c-161">NOTES</span></span>

## <span data-ttu-id="9314c-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="9314c-162">RELATED LINKS</span></span>

[<span data-ttu-id="9314c-163">AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="9314c-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="9314c-164">移除-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="9314c-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="9314c-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="9314c-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)

