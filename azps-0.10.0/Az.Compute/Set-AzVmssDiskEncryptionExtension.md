---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: 15453163918854dd0efa7440209164007335aced
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795821"
---
# <span data-ttu-id="bd040-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="bd040-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="bd040-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd040-102">SYNOPSIS</span></span>
<span data-ttu-id="bd040-103">在 VM 比例集上啟用磁片加密。</span><span class="sxs-lookup"><span data-stu-id="bd040-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="bd040-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd040-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd040-105">說明</span><span class="sxs-lookup"><span data-stu-id="bd040-105">DESCRIPTION</span></span>
<span data-ttu-id="bd040-106">**AzVmssDiskEncryptionExtension** Cmdlet 可在 VM 規模集中進行加密。</span><span class="sxs-lookup"><span data-stu-id="bd040-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span>
<span data-ttu-id="bd040-107">這個 Cmdlet 可在 VM 規模集上安裝磁片加密延伸來啟用加密。</span><span class="sxs-lookup"><span data-stu-id="bd040-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>
<span data-ttu-id="bd040-108">如果未指定 *Name* 參數，則會安裝針對執行 Windows 作業系統或 AzureDiskEncryptionForLinux for Linux 虛擬機器的虛擬機器使用預設名稱 AzureDiskEncryption 的副檔名。</span><span class="sxs-lookup"><span data-stu-id="bd040-108">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>

## <span data-ttu-id="bd040-109">示例</span><span class="sxs-lookup"><span data-stu-id="bd040-109">EXAMPLES</span></span>

### <span data-ttu-id="bd040-110">範例1</span><span class="sxs-lookup"><span data-stu-id="bd040-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="bd040-111">這個命令會在 VM 規模集中所有 Vm 的所有磁片上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="bd040-111">This command enables encryption on all disks of all VMs in the VM scale set.</span></span>

## <span data-ttu-id="bd040-112">參數</span><span class="sxs-lookup"><span data-stu-id="bd040-112">PARAMETERS</span></span>

### <span data-ttu-id="bd040-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd040-113">-DefaultProfile</span></span>
<span data-ttu-id="bd040-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd040-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd040-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="bd040-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="bd040-116">停用次要版本的自動升級</span><span class="sxs-lookup"><span data-stu-id="bd040-116">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="bd040-117">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="bd040-117">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="bd040-118">要放置產生的加密金鑰之 KeyVault 的 ResourceID</span><span class="sxs-lookup"><span data-stu-id="bd040-118">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd040-119">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="bd040-119">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="bd040-120">要放置產生的加密金鑰之 KeyVault 的 URL</span><span class="sxs-lookup"><span data-stu-id="bd040-120">URL of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd040-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="bd040-121">-ExtensionName</span></span>
<span data-ttu-id="bd040-122">副檔名。</span><span class="sxs-lookup"><span data-stu-id="bd040-122">The extension name.</span></span>
<span data-ttu-id="bd040-123">如果未指定此參數，則使用的預設值是適用于 windows Vm 的 AzureDiskEncryption，以及適用于 Linux Vm 的 AzureDiskEncryptionForLinux</span><span class="sxs-lookup"><span data-stu-id="bd040-123">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="bd040-124">-Force</span><span class="sxs-lookup"><span data-stu-id="bd040-124">-Force</span></span>
<span data-ttu-id="bd040-125">在虛擬機器規模集上強制啟用加密。</span><span class="sxs-lookup"><span data-stu-id="bd040-125">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="bd040-126">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="bd040-126">-ForceUpdate</span></span>
<span data-ttu-id="bd040-127">產生 [強制更新] 的標記。</span><span class="sxs-lookup"><span data-stu-id="bd040-127">Generate a tag for force update.</span></span>  <span data-ttu-id="bd040-128">這應該是為了在同一個 VM 上執行重複的加密作業。</span><span class="sxs-lookup"><span data-stu-id="bd040-128">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="bd040-129">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="bd040-129">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="bd040-130">用來加密大量加密金鑰的 KeyEncryption 演算法</span><span class="sxs-lookup"><span data-stu-id="bd040-130">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd040-131">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="bd040-131">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="bd040-132">用來加密磁片加密金鑰之 KeyEncryptionKey 的版本控制 KeyVault URL</span><span class="sxs-lookup"><span data-stu-id="bd040-132">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="bd040-133">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="bd040-133">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="bd040-134">包含用來加密磁片加密金鑰之 KeyEncryptionKey 的 KeyVault ResourceID</span><span class="sxs-lookup"><span data-stu-id="bd040-134">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="bd040-135">-密碼</span><span class="sxs-lookup"><span data-stu-id="bd040-135">-Passphrase</span></span>
<span data-ttu-id="bd040-136">[參數] 中指定的密碼。</span><span class="sxs-lookup"><span data-stu-id="bd040-136">The passphrase specified in parameters.</span></span>
<span data-ttu-id="bd040-137">這個參數只適用于 Linux VM。</span><span class="sxs-lookup"><span data-stu-id="bd040-137">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="bd040-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd040-138">-ResourceGroupName</span></span>
<span data-ttu-id="bd040-139">VM 比例集所屬的資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="bd040-139">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="bd040-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="bd040-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="bd040-141">類型處理常式版本。</span><span class="sxs-lookup"><span data-stu-id="bd040-141">The type handler version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd040-142">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bd040-142">-VMScaleSetName</span></span>
<span data-ttu-id="bd040-143">虛擬機器規模集的名稱</span><span class="sxs-lookup"><span data-stu-id="bd040-143">Name of the virtual machine scale set</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd040-144">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="bd040-144">-VolumeType</span></span>
<span data-ttu-id="bd040-145">要執行加密作業 (OS 或資料) 的音量類型</span><span class="sxs-lookup"><span data-stu-id="bd040-145">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd040-146">-確認</span><span class="sxs-lookup"><span data-stu-id="bd040-146">-Confirm</span></span>
<span data-ttu-id="bd040-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bd040-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd040-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd040-148">-WhatIf</span></span>
<span data-ttu-id="bd040-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bd040-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd040-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd040-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd040-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd040-151">CommonParameters</span></span>
<span data-ttu-id="bd040-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd040-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd040-153">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd040-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd040-154">輸入</span><span class="sxs-lookup"><span data-stu-id="bd040-154">INPUTS</span></span>

### <span data-ttu-id="bd040-155">System.object</span><span class="sxs-lookup"><span data-stu-id="bd040-155">System.String</span></span>
<span data-ttu-id="bd040-156">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="bd040-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bd040-157">輸出</span><span class="sxs-lookup"><span data-stu-id="bd040-157">OUTPUTS</span></span>

### <span data-ttu-id="bd040-158">PSVirtualMachineScaleSetExtension 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="bd040-158">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="bd040-159">筆記</span><span class="sxs-lookup"><span data-stu-id="bd040-159">NOTES</span></span>

## <span data-ttu-id="bd040-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd040-160">RELATED LINKS</span></span>
