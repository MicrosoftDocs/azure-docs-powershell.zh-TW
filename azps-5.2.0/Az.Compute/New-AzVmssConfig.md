---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285048"
---
# <span data-ttu-id="fb7aa-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="fb7aa-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="fb7aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb7aa-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7aa-103">建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="fb7aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb7aa-104">SYNTAX</span></span>

### <span data-ttu-id="fb7aa-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fb7aa-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] [-EncryptionAtHost]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7aa-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb7aa-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb7aa-107">說明</span><span class="sxs-lookup"><span data-stu-id="fb7aa-107">DESCRIPTION</span></span>
<span data-ttu-id="fb7aa-108">**新的-AzVmssConfig** Cmdlet 會建立可設定的本機視覺管理員縮放比例集， (VMSS) 物件。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="fb7aa-109">需要其他 Cmdlet 來設定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="fb7aa-110">這些 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="fb7aa-110">These cmdlets are:</span></span>
- <span data-ttu-id="fb7aa-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="fb7aa-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="fb7aa-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="fb7aa-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="fb7aa-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb7aa-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="fb7aa-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="fb7aa-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="fb7aa-115">示例</span><span class="sxs-lookup"><span data-stu-id="fb7aa-115">EXAMPLES</span></span>

### <span data-ttu-id="fb7aa-116">範例1：建立 VMSS 設定物件</span><span class="sxs-lookup"><span data-stu-id="fb7aa-116">Example 1: Create a VMSS configuration object</span></span>
```powershell
PS C:\> $VMSS = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="fb7aa-117">這個範例會建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="fb7aa-118">第一個命令使用 **新的 AzVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="fb7aa-119">第二個命令使用 **AzVmss** Cmdlet 來建立使用在第一個命令中建立之 VMSS 設定物件的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="fb7aa-120">範例2</span><span class="sxs-lookup"><span data-stu-id="fb7aa-120">Example 2</span></span>

<span data-ttu-id="fb7aa-121">建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="fb7aa-122"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="fb7aa-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="fb7aa-123">參數</span><span class="sxs-lookup"><span data-stu-id="fb7aa-123">PARAMETERS</span></span>

### <span data-ttu-id="fb7aa-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="fb7aa-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="fb7aa-125">因 VM 上狀態變更而暫停自動修復的時間長度。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="fb7aa-126">當狀態變更完成後，寬限期即會開始。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="fb7aa-127">這有助於避免過早或意外的修復。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="fb7aa-128">應以 ISO 8601 格式指定持續時間。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="fb7aa-129">[允許的最小寬限期] 是30分鐘 (PT30M) ，也是預設值。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="fb7aa-130">所允許的最大寬限期是90分鐘 (PT90M) 。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="fb7aa-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="fb7aa-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="fb7aa-132">設定更新版本的影像時，是否應該將作業系統升級自動套用到縮放集實例，以滾動的方式進行。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="fb7aa-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fb7aa-133">-BootDiagnostic</span></span>
<span data-ttu-id="fb7aa-134">指定虛擬機器縮放設定啟動診斷設定檔。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.BootDiagnostics
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7aa-135">-DefaultProfile</span></span>
<span data-ttu-id="fb7aa-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb7aa-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="fb7aa-137">-DisableAutoRollback</span></span>
<span data-ttu-id="fb7aa-138">針對自動 OS 升級原則停用自動復原</span><span class="sxs-lookup"><span data-stu-id="fb7aa-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="fb7aa-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="fb7aa-140">在虛擬機器規模集上啟用自動修復。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-140">Enables automatic repairs on the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-141">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="fb7aa-141">-EnableUltraSSD</span></span>
<span data-ttu-id="fb7aa-142">可讓一或多個受管理的資料磁片使用一或多個在虛擬機器縮放設定上擁有 UltraSSD_LRS 儲存帳戶類型的功能。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="fb7aa-143">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="fb7aa-144">-EncryptionAtHost</span></span>
<span data-ttu-id="fb7aa-145">這個參數會針對所有磁片啟用加密，包括主機本身的資源/Temp 磁片。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="fb7aa-146">預設：除非針對資源將此屬性設為 true，否則將停用主機上的加密。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-147">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="fb7aa-147">-EvictionPolicy</span></span>
<span data-ttu-id="fb7aa-148">針對規模集中的虛擬機器指定逐出原則。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="fb7aa-149">-延伸</span><span class="sxs-lookup"><span data-stu-id="fb7aa-149">-Extension</span></span>
<span data-ttu-id="fb7aa-150">指定 VMSS 的延伸資訊物件。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="fb7aa-151">您可以使用 **AzVmssExtension** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="fb7aa-152">-HealthProbeId</span></span>
<span data-ttu-id="fb7aa-153">指定負載平衡器探測的識別碼，這些探測器用來判斷虛擬機器規模集中的實例健康情況。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="fb7aa-154">HealthProbeId 的形式為「/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}」。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="fb7aa-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="fb7aa-155">-IdentityId</span></span>
<span data-ttu-id="fb7aa-156">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="fb7aa-157">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="fb7aa-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="fb7aa-158">-IdentityType</span></span>
<span data-ttu-id="fb7aa-159">指定用於虛擬機器規模集的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="fb7aa-160">"SystemAssignedUserAssigned" 類型包含隱含建立的身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="fb7aa-161">"None" 類型將會移除虛擬機器小單位集中的任何身分識別。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="fb7aa-162">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fb7aa-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb7aa-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="fb7aa-163">SystemAssigned</span></span>
- <span data-ttu-id="fb7aa-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="fb7aa-164">UserAssigned</span></span>
- <span data-ttu-id="fb7aa-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="fb7aa-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="fb7aa-166">所有</span><span class="sxs-lookup"><span data-stu-id="fb7aa-166">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fb7aa-167">-LicenseType</span></span>
<span data-ttu-id="fb7aa-168">指定授權類型，這是用來提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="fb7aa-169">-位置</span><span class="sxs-lookup"><span data-stu-id="fb7aa-169">-Location</span></span>
<span data-ttu-id="fb7aa-170">指定建立 VMSS 的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-170">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="fb7aa-171">-MaxPrice</span></span>
<span data-ttu-id="fb7aa-172">指定您想要為某個專色 VM/VMSS 支付的最大價格。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="fb7aa-173">這個價格是美元。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-173">This price is in US Dollars.</span></span> <span data-ttu-id="fb7aa-174">此價格將與 VM 大小的目前價位進行比較。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="fb7aa-175">此外，價格會在建立/更新專色 VM/VMSS 時進行比較，而且只有在 maxPrice 大於目前的價位時，才能成功執行該作業。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="fb7aa-176">如果在建立 VM/VMSS 之後，目前的價位超出 maxPrice 的範圍，則 maxPrice 也會用於逐出 [專色 VM/VMSS]。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="fb7aa-177">可能的值為：任何大於零的十進位值。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="fb7aa-178">範例：0.01538。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-178">Example: 0.01538.</span></span>  <span data-ttu-id="fb7aa-179">-1 表示出於價格考慮，不應逐出污點 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="fb7aa-180">此外，如果您沒有提供預設的最大價格，就是-1。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-180">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb7aa-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="fb7aa-182">指定包含 VMSS 設定之網路屬性的網路設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="fb7aa-183">您可以使用 **AzVmssNetworkInterfaceConfiguration** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="fb7aa-184">-OsProfile</span></span>
<span data-ttu-id="fb7aa-185">指定作業系統設定檔物件，其中包含 VMSS 設定的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="fb7aa-186">您可以使用 **AzVmssOsProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-187">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="fb7aa-187">-Overprovision</span></span>
<span data-ttu-id="fb7aa-188">指示 Cmdlet 是否 overprovisions VMSS。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="fb7aa-189">-PlanName</span></span>
<span data-ttu-id="fb7aa-190">指定方案名稱。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="fb7aa-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="fb7aa-191">-PlanProduct</span></span>
<span data-ttu-id="fb7aa-192">指定方案產品。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="fb7aa-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="fb7aa-193">-PlanPromotionCode</span></span>
<span data-ttu-id="fb7aa-194">指定方案促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="fb7aa-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="fb7aa-195">-PlanPublisher</span></span>
<span data-ttu-id="fb7aa-196">指定方案發行者。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="fb7aa-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="fb7aa-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="fb7aa-198">每個位置群組的錯誤網域計數。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-198">Fault Domain count for each placement group.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-199">-優先順序</span><span class="sxs-lookup"><span data-stu-id="fb7aa-199">-Priority</span></span>
<span data-ttu-id="fb7aa-200">規模集中虛擬 machien 的優先順序。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="fb7aa-201">僅支援的值為 "Regular"、"點" 和 "低"。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="fb7aa-202">"Regular" 是適用于一般虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="fb7aa-203">「點」是用於找出虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="fb7aa-204">「低」也適用于 [專色虛擬機器]，但會以「點」取代。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="fb7aa-205">請使用「污點」，而不是「低」。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="fb7aa-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="fb7aa-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="fb7aa-207">要與此比例集搭配使用之鄰近性位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="fb7aa-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="fb7aa-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="fb7aa-209">指定輪流升級原則。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-209">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="fb7aa-210">-ScaleInPolicy</span></span>
<span data-ttu-id="fb7aa-211">在虛擬電腦規模集中進行伸縮時遵循的規則。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="fb7aa-212">可能的值為： "Default"、"OldestVM" 和 "NewestVM"。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="fb7aa-213">[預設值] 當虛擬電腦縮放比例設定為放大時，如果區域為區域性比例集，則比例集會先平衡在各個區域。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="fb7aa-214">接著，它會盡可能在故障網域之間平衡。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="fb7aa-215">在每個容錯網域中，選取要移除的虛擬機器將是無法從擴展保護的最新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="fb7aa-216">"OldestVM" 當虛擬電腦縮放比例設定為放大時，系統將不會選擇要移除的最舊虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="fb7aa-217">針對 [區塊虛擬電腦] 規模集，比例集將在各個區域之間進行平衡。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="fb7aa-218">在每個區域中，將會選取未受保護的舊虛擬機器，以供移除。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="fb7aa-219">"NewestVM" 當虛擬電腦縮放比例設定為放大時，系統將不會選取任何不受放大的虛擬機器來進行移除。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="fb7aa-220">針對 [區塊虛擬電腦] 規模集，比例集將在各個區域之間進行平衡。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="fb7aa-221">在每個區域中，將會選取未受到保護的新虛擬機器電腦來移除。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="fb7aa-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="fb7aa-223">指定單一位置群組。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-223">Specifies the single placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="fb7aa-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="fb7aa-225">指定延伸不會在額外的 overprovisioned Vm 上執行。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="fb7aa-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="fb7aa-226">-SkuCapacity</span></span>
<span data-ttu-id="fb7aa-227">指定 VMSS 中的實例數。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-227">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-228">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fb7aa-228">-SkuName</span></span>
<span data-ttu-id="fb7aa-229">指定 VMSS 的所有實例大小。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-229">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="fb7aa-230">-SkuTier</span></span>
<span data-ttu-id="fb7aa-231">指定 VMSS 的層級。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="fb7aa-232">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fb7aa-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb7aa-233">標準</span><span class="sxs-lookup"><span data-stu-id="fb7aa-233">Standard</span></span>
- <span data-ttu-id="fb7aa-234">空白</span><span class="sxs-lookup"><span data-stu-id="fb7aa-234">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="fb7aa-235">-StorageProfile</span></span>
<span data-ttu-id="fb7aa-236">指定包含 VMSS 設定之磁片摘要資訊的儲存空間物件。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="fb7aa-237">您可以使用 **AzVmssStorageProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-238">-Tag</span><span class="sxs-lookup"><span data-stu-id="fb7aa-238">-Tag</span></span>
<span data-ttu-id="fb7aa-239">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fb7aa-240">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fb7aa-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="fb7aa-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="fb7aa-242">已刪除的虛擬機器 (數分鐘內可設定的時間長度) ，必須先核准終止排程事件，然後才能自動核准 (超時) 。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="fb7aa-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="fb7aa-244">啟用終止排程事件</span><span class="sxs-lookup"><span data-stu-id="fb7aa-244">Enable the Terminate Scheduled events</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="fb7aa-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="fb7aa-246">已指定升級模式至規模集中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="fb7aa-247">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fb7aa-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb7aa-248">自動</span><span class="sxs-lookup"><span data-stu-id="fb7aa-248">Automatic</span></span>
- <span data-ttu-id="fb7aa-249">手動</span><span class="sxs-lookup"><span data-stu-id="fb7aa-249">Manual</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.UpgradeMode]
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-250">-Zone</span><span class="sxs-lookup"><span data-stu-id="fb7aa-250">-Zone</span></span>
<span data-ttu-id="fb7aa-251">指定虛擬機器縮放集的區域清單。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-251">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7aa-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="fb7aa-252">-ZoneBalance</span></span>
<span data-ttu-id="fb7aa-253">在發生區域中斷時，是否要強制嚴格地根據 x 個區域進行虛擬電腦發佈。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="fb7aa-254">-確認</span><span class="sxs-lookup"><span data-stu-id="fb7aa-254">-Confirm</span></span>
<span data-ttu-id="fb7aa-255">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb7aa-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb7aa-256">-WhatIf</span></span>
<span data-ttu-id="fb7aa-257">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb7aa-258">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb7aa-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7aa-259">CommonParameters</span></span>
<span data-ttu-id="fb7aa-260">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7aa-261">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7aa-262">輸入</span><span class="sxs-lookup"><span data-stu-id="fb7aa-262">INPUTS</span></span>

### <span data-ttu-id="fb7aa-263">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fb7aa-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fb7aa-264">System.object</span><span class="sxs-lookup"><span data-stu-id="fb7aa-264">System.String</span></span>

### <span data-ttu-id="fb7aa-265">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fb7aa-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fb7aa-266">System.object</span><span class="sxs-lookup"><span data-stu-id="fb7aa-266">System.Int32</span></span>

### <span data-ttu-id="fb7aa-267">"UpgradeMode" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="fb7aa-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="fb7aa-268">VirtualMachineScaleSetOSProfile 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="fb7aa-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="fb7aa-269">VirtualMachineScaleSetStorageProfile 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="fb7aa-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="fb7aa-270">VirtualMachineScaleSetNetworkConfiguration [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="fb7aa-271">VirtualMachineScaleSetExtension [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="fb7aa-272">System.object []</span><span class="sxs-lookup"><span data-stu-id="fb7aa-272">System.String[]</span></span>

### <span data-ttu-id="fb7aa-273">RollingUpgradePolicy 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="fb7aa-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="fb7aa-274">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="fb7aa-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="fb7aa-275">BootDiagnostics 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="fb7aa-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="fb7aa-276">"ResourceIdentityType" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="fb7aa-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="fb7aa-277">輸出</span><span class="sxs-lookup"><span data-stu-id="fb7aa-277">OUTPUTS</span></span>

### <span data-ttu-id="fb7aa-278">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="fb7aa-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="fb7aa-279">筆記</span><span class="sxs-lookup"><span data-stu-id="fb7aa-279">NOTES</span></span>

## <span data-ttu-id="fb7aa-280">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb7aa-280">RELATED LINKS</span></span>

[<span data-ttu-id="fb7aa-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="fb7aa-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="fb7aa-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="fb7aa-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="fb7aa-283">附加 AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb7aa-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="fb7aa-284">附加 AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="fb7aa-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="fb7aa-285">新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fb7aa-285">New-AzVmss</span></span>](./New-AzVmss.md)