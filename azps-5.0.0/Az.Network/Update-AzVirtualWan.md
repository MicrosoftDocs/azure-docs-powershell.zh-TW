---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: e93bcc320f14a8311a29c6be9824da16506ea499
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287784"
---
# <span data-ttu-id="fe9b4-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="fe9b4-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="fe9b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe9b4-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9b4-103">更新 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="fe9b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe9b4-104">SYNTAX</span></span>

### <span data-ttu-id="fe9b4-105">ByVirtualWanName (預設) </span><span class="sxs-lookup"><span data-stu-id="fe9b4-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe9b4-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="fe9b4-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe9b4-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="fe9b4-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe9b4-108">說明</span><span class="sxs-lookup"><span data-stu-id="fe9b4-108">DESCRIPTION</span></span>
<span data-ttu-id="fe9b4-109">更新 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="fe9b4-110">示例</span><span class="sxs-lookup"><span data-stu-id="fe9b4-110">EXAMPLES</span></span>

### <span data-ttu-id="fe9b4-111">範例1</span><span class="sxs-lookup"><span data-stu-id="fe9b4-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="fe9b4-112">上述將會在 [West 美國] 地區建立資源群組 "testRG"，並在 Azure 中的該資源群組中建立 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="fe9b4-113">VirtualWan 已更新為新的屬性。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="fe9b4-114">參數</span><span class="sxs-lookup"><span data-stu-id="fe9b4-114">PARAMETERS</span></span>

### <span data-ttu-id="fe9b4-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="fe9b4-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="fe9b4-116">允許分支分支機搆 VirtualWan 的流量。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9b4-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="fe9b4-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="fe9b4-118">允許 vnet 至 vnet 流量以進行 VirtualWan。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9b4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe9b4-119">-AsJob</span></span>
<span data-ttu-id="fe9b4-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fe9b4-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe9b4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe9b4-121">-DefaultProfile</span></span>
<span data-ttu-id="fe9b4-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9b4-123">-Force</span><span class="sxs-lookup"><span data-stu-id="fe9b4-123">-Force</span></span>
<span data-ttu-id="fe9b4-124">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="fe9b4-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fe9b4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe9b4-125">-InputObject</span></span>
<span data-ttu-id="fe9b4-126">要修改的虛擬 wan 物件</span><span class="sxs-lookup"><span data-stu-id="fe9b4-126">The virtual wan object to be modified</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9b4-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe9b4-127">-Name</span></span>
<span data-ttu-id="fe9b4-128">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-128">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9b4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe9b4-129">-ResourceGroupName</span></span>
<span data-ttu-id="fe9b4-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9b4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe9b4-131">-ResourceId</span></span>
<span data-ttu-id="fe9b4-132">虛擬 wan 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9b4-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="fe9b4-133">-Tag</span></span>
<span data-ttu-id="fe9b4-134">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9b4-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="fe9b4-135">-VirtualWANType</span></span>
<span data-ttu-id="fe9b4-136">虛擬 Wan 的類型。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-136">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9b4-137">-確認</span><span class="sxs-lookup"><span data-stu-id="fe9b4-137">-Confirm</span></span>
<span data-ttu-id="fe9b4-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe9b4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe9b4-139">-WhatIf</span></span>
<span data-ttu-id="fe9b4-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe9b4-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe9b4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9b4-142">CommonParameters</span></span>
<span data-ttu-id="fe9b4-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9b4-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fe9b4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9b4-145">輸入</span><span class="sxs-lookup"><span data-stu-id="fe9b4-145">INPUTS</span></span>

### <span data-ttu-id="fe9b4-146">PSVirtualWan 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fe9b4-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="fe9b4-147">System.object</span><span class="sxs-lookup"><span data-stu-id="fe9b4-147">System.String</span></span>

## <span data-ttu-id="fe9b4-148">輸出</span><span class="sxs-lookup"><span data-stu-id="fe9b4-148">OUTPUTS</span></span>

### <span data-ttu-id="fe9b4-149">PSVirtualWan 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fe9b4-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="fe9b4-150">筆記</span><span class="sxs-lookup"><span data-stu-id="fe9b4-150">NOTES</span></span>

## <span data-ttu-id="fe9b4-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe9b4-151">RELATED LINKS</span></span>

[<span data-ttu-id="fe9b4-152">AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="fe9b4-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="fe9b4-153">新-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="fe9b4-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="fe9b4-154">移除-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="fe9b4-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)