---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287932"
---
# <span data-ttu-id="971ed-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="971ed-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="971ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="971ed-102">SYNOPSIS</span></span>
<span data-ttu-id="971ed-103">建立圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="971ed-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="971ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="971ed-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-DisallowedDiskType <String[]>]
 [-EndOfLifeDate <DateTime>] [-Eula <String>] [-HyperVGeneration <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="971ed-105">說明</span><span class="sxs-lookup"><span data-stu-id="971ed-105">DESCRIPTION</span></span>
<span data-ttu-id="971ed-106">建立圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="971ed-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="971ed-107">示例</span><span class="sxs-lookup"><span data-stu-id="971ed-107">EXAMPLES</span></span>

### <span data-ttu-id="971ed-108">範例1</span><span class="sxs-lookup"><span data-stu-id="971ed-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="971ed-109">建立圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="971ed-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="971ed-110">參數</span><span class="sxs-lookup"><span data-stu-id="971ed-110">PARAMETERS</span></span>

### <span data-ttu-id="971ed-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="971ed-111">-AsJob</span></span>
<span data-ttu-id="971ed-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="971ed-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="971ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="971ed-113">-DefaultProfile</span></span>
<span data-ttu-id="971ed-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="971ed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="971ed-115">-描述</span><span class="sxs-lookup"><span data-stu-id="971ed-115">-Description</span></span>
<span data-ttu-id="971ed-116">圖庫影像定義資源的描述。</span><span class="sxs-lookup"><span data-stu-id="971ed-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="971ed-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="971ed-117">-DisallowedDiskType</span></span>
<span data-ttu-id="971ed-118">非許可的磁片類型。</span><span class="sxs-lookup"><span data-stu-id="971ed-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="971ed-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="971ed-119">-EndOfLifeDate</span></span>
<span data-ttu-id="971ed-120">圖庫影像定義的生命循環結束日期</span><span class="sxs-lookup"><span data-stu-id="971ed-120">The end of life date of the gallery Image Definition</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971ed-121">-Eula</span><span class="sxs-lookup"><span data-stu-id="971ed-121">-Eula</span></span>
<span data-ttu-id="971ed-122">畫廊影像定義的 Eula 合約。</span><span class="sxs-lookup"><span data-stu-id="971ed-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="971ed-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="971ed-123">-GalleryName</span></span>
<span data-ttu-id="971ed-124">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="971ed-124">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971ed-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="971ed-125">-HyperVGeneration</span></span>
<span data-ttu-id="971ed-126">虛擬機器的虛擬機器監控程式產生。</span><span class="sxs-lookup"><span data-stu-id="971ed-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="971ed-127">僅適用于作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="971ed-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="971ed-128">允許的值為 V1 和 V2。</span><span class="sxs-lookup"><span data-stu-id="971ed-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="971ed-129">-位置</span><span class="sxs-lookup"><span data-stu-id="971ed-129">-Location</span></span>
<span data-ttu-id="971ed-130">資源位置</span><span class="sxs-lookup"><span data-stu-id="971ed-130">Resource location</span></span>

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

### <span data-ttu-id="971ed-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="971ed-131">-MaximumMemory</span></span>
<span data-ttu-id="971ed-132">建議的記憶體上限</span><span class="sxs-lookup"><span data-stu-id="971ed-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="971ed-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="971ed-133">-MaximumVCPU</span></span>
<span data-ttu-id="971ed-134">建議的 CPU 核心最大值</span><span class="sxs-lookup"><span data-stu-id="971ed-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="971ed-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="971ed-135">-MinimumMemory</span></span>
<span data-ttu-id="971ed-136">建議的記憶體最小值</span><span class="sxs-lookup"><span data-stu-id="971ed-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="971ed-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="971ed-137">-MinimumVCPU</span></span>
<span data-ttu-id="971ed-138">建議的 CPU 核心最小值</span><span class="sxs-lookup"><span data-stu-id="971ed-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="971ed-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="971ed-139">-Name</span></span>
<span data-ttu-id="971ed-140">圖庫影像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="971ed-140">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971ed-141">-優惠</span><span class="sxs-lookup"><span data-stu-id="971ed-141">-Offer</span></span>
<span data-ttu-id="971ed-142">圖庫影像定義優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="971ed-142">The name of the gallery Image Definition offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971ed-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="971ed-143">-OsState</span></span>
<span data-ttu-id="971ed-144">OS 的狀態</span><span class="sxs-lookup"><span data-stu-id="971ed-144">The state of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971ed-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="971ed-145">-OsType</span></span>
<span data-ttu-id="971ed-146">OS 類型</span><span class="sxs-lookup"><span data-stu-id="971ed-146">The type of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971ed-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="971ed-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="971ed-148">隱私權語句 uri。</span><span class="sxs-lookup"><span data-stu-id="971ed-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="971ed-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="971ed-149">-Publisher</span></span>
<span data-ttu-id="971ed-150">圖庫影像定義發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="971ed-150">The name of the gallery Image Definition publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971ed-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="971ed-151">-PurchasePlanName</span></span>
<span data-ttu-id="971ed-152">採購方案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="971ed-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="971ed-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="971ed-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="971ed-154">採購方案的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="971ed-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="971ed-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="971ed-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="971ed-156">採購方案的發行者識別碼。</span><span class="sxs-lookup"><span data-stu-id="971ed-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="971ed-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="971ed-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="971ed-158">版本記事 uri。</span><span class="sxs-lookup"><span data-stu-id="971ed-158">The release note uri.</span></span>

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

### <span data-ttu-id="971ed-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="971ed-159">-ResourceGroupName</span></span>
<span data-ttu-id="971ed-160">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="971ed-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="971ed-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="971ed-161">-Sku</span></span>
<span data-ttu-id="971ed-162">圖庫影像定義 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="971ed-162">The name of the gallery Image Definition SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971ed-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="971ed-163">-Tag</span></span>
<span data-ttu-id="971ed-164">資源標記</span><span class="sxs-lookup"><span data-stu-id="971ed-164">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971ed-165">-確認</span><span class="sxs-lookup"><span data-stu-id="971ed-165">-Confirm</span></span>
<span data-ttu-id="971ed-166">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="971ed-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="971ed-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="971ed-167">-WhatIf</span></span>
<span data-ttu-id="971ed-168">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="971ed-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="971ed-169">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="971ed-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="971ed-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="971ed-170">CommonParameters</span></span>
<span data-ttu-id="971ed-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="971ed-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="971ed-172">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="971ed-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="971ed-173">輸入</span><span class="sxs-lookup"><span data-stu-id="971ed-173">INPUTS</span></span>

### <span data-ttu-id="971ed-174">System.object</span><span class="sxs-lookup"><span data-stu-id="971ed-174">System.String</span></span>

### <span data-ttu-id="971ed-175">OperatingSystemStateTypes 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="971ed-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="971ed-176">OperatingSystemTypes 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="971ed-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="971ed-177">System.object</span><span class="sxs-lookup"><span data-stu-id="971ed-177">System.DateTime</span></span>

### <span data-ttu-id="971ed-178">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="971ed-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="971ed-179">System.object</span><span class="sxs-lookup"><span data-stu-id="971ed-179">System.Int32</span></span>

### <span data-ttu-id="971ed-180">System.object []</span><span class="sxs-lookup"><span data-stu-id="971ed-180">System.String[]</span></span>

## <span data-ttu-id="971ed-181">輸出</span><span class="sxs-lookup"><span data-stu-id="971ed-181">OUTPUTS</span></span>

### <span data-ttu-id="971ed-182">PSGalleryImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="971ed-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="971ed-183">筆記</span><span class="sxs-lookup"><span data-stu-id="971ed-183">NOTES</span></span>

## <span data-ttu-id="971ed-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="971ed-184">RELATED LINKS</span></span>