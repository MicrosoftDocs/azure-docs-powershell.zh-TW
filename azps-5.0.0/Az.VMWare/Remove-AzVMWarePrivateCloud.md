---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
ms.openlocfilehash: accf225acfb05fdcaf49eb5dde4d1bae0332d300
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286080"
---
# <span data-ttu-id="64be4-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="64be4-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="64be4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64be4-102">SYNOPSIS</span></span>
<span data-ttu-id="64be4-103">刪除私有雲端</span><span class="sxs-lookup"><span data-stu-id="64be4-103">Delete a private cloud</span></span>

## <span data-ttu-id="64be4-104">句法</span><span class="sxs-lookup"><span data-stu-id="64be4-104">SYNTAX</span></span>

### <span data-ttu-id="64be4-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="64be4-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64be4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="64be4-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64be4-107">說明</span><span class="sxs-lookup"><span data-stu-id="64be4-107">DESCRIPTION</span></span>
<span data-ttu-id="64be4-108">刪除私有雲端</span><span class="sxs-lookup"><span data-stu-id="64be4-108">Delete a private cloud</span></span>

## <span data-ttu-id="64be4-109">示例</span><span class="sxs-lookup"><span data-stu-id="64be4-109">EXAMPLES</span></span>

### <span data-ttu-id="64be4-110">範例1：刪除私有雲端</span><span class="sxs-lookup"><span data-stu-id="64be4-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="64be4-111">刪除私有雲端</span><span class="sxs-lookup"><span data-stu-id="64be4-111">Delete private cloud</span></span>

## <span data-ttu-id="64be4-112">參數</span><span class="sxs-lookup"><span data-stu-id="64be4-112">PARAMETERS</span></span>

### <span data-ttu-id="64be4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64be4-113">-AsJob</span></span>
<span data-ttu-id="64be4-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="64be4-114">Run the command as a job</span></span>

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

### <span data-ttu-id="64be4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64be4-115">-DefaultProfile</span></span>
<span data-ttu-id="64be4-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="64be4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64be4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64be4-117">-InputObject</span></span>
<span data-ttu-id="64be4-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="64be4-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64be4-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="64be4-119">-Name</span></span>
<span data-ttu-id="64be4-120">私有雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="64be4-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64be4-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="64be4-121">-NoWait</span></span>
<span data-ttu-id="64be4-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="64be4-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="64be4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64be4-123">-PassThru</span></span>
<span data-ttu-id="64be4-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="64be4-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="64be4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64be4-125">-ResourceGroupName</span></span>
<span data-ttu-id="64be4-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="64be4-126">The name of the resource group.</span></span>
<span data-ttu-id="64be4-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="64be4-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64be4-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64be4-128">-SubscriptionId</span></span>
<span data-ttu-id="64be4-129">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="64be4-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64be4-130">-確認</span><span class="sxs-lookup"><span data-stu-id="64be4-130">-Confirm</span></span>
<span data-ttu-id="64be4-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="64be4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64be4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64be4-132">-WhatIf</span></span>
<span data-ttu-id="64be4-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="64be4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64be4-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64be4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64be4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64be4-135">CommonParameters</span></span>
<span data-ttu-id="64be4-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64be4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64be4-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="64be4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64be4-138">輸入</span><span class="sxs-lookup"><span data-stu-id="64be4-138">INPUTS</span></span>

### <span data-ttu-id="64be4-139">IVMWareIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="64be4-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="64be4-140">輸出</span><span class="sxs-lookup"><span data-stu-id="64be4-140">OUTPUTS</span></span>

### <span data-ttu-id="64be4-141">System.object</span><span class="sxs-lookup"><span data-stu-id="64be4-141">System.Boolean</span></span>

## <span data-ttu-id="64be4-142">筆記</span><span class="sxs-lookup"><span data-stu-id="64be4-142">NOTES</span></span>

<span data-ttu-id="64be4-143">別名</span><span class="sxs-lookup"><span data-stu-id="64be4-143">ALIASES</span></span>

<span data-ttu-id="64be4-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="64be4-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64be4-145">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="64be4-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64be4-146">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="64be4-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64be4-147">INPUTOBJECT <IVMWareIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="64be4-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64be4-148">`[AuthorizationName <String>]`：私人雲端中 ExpressRoute 線路授權的名稱</span><span class="sxs-lookup"><span data-stu-id="64be4-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="64be4-149">`[ClusterName <String>]`：私人雲端中的群集名稱</span><span class="sxs-lookup"><span data-stu-id="64be4-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="64be4-150">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="64be4-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="64be4-151">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="64be4-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64be4-152">`[Location <String>]`： Azure region</span><span class="sxs-lookup"><span data-stu-id="64be4-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="64be4-153">`[PrivateCloudName <String>]`：私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="64be4-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="64be4-154">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="64be4-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="64be4-155">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="64be4-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="64be4-156">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="64be4-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="64be4-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="64be4-157">RELATED LINKS</span></span>
