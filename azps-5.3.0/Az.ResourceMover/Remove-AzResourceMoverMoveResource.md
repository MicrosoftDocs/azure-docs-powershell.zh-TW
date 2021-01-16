---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: f718f3c133f25a8b7fb401bfb9a390724090ccc4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435567"
---
# <span data-ttu-id="df28f-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="df28f-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="df28f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df28f-102">SYNOPSIS</span></span>
<span data-ttu-id="df28f-103">從移動收藏集中刪除移動資源。</span><span class="sxs-lookup"><span data-stu-id="df28f-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="df28f-104">句法</span><span class="sxs-lookup"><span data-stu-id="df28f-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="df28f-105">說明</span><span class="sxs-lookup"><span data-stu-id="df28f-105">DESCRIPTION</span></span>
<span data-ttu-id="df28f-106">從移動收藏集中刪除移動資源。</span><span class="sxs-lookup"><span data-stu-id="df28f-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="df28f-107">示例</span><span class="sxs-lookup"><span data-stu-id="df28f-107">EXAMPLES</span></span>

### <span data-ttu-id="df28f-108">範例1：從移動收藏中移除資源</span><span class="sxs-lookup"><span data-stu-id="df28f-108">Example 1: Remove the resource from the Move collection</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -Name "psdemorm"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/11/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                     ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866c5
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/11/2020 3:27:27 PM
    Status         : Succeeded

```

<span data-ttu-id="df28f-109">在指定的訂閱內，從移動集合中移除資源。</span><span class="sxs-lookup"><span data-stu-id="df28f-109">Remove the resource from the Move collection within the specified subscription.</span></span>

## <span data-ttu-id="df28f-110">參數</span><span class="sxs-lookup"><span data-stu-id="df28f-110">PARAMETERS</span></span>

### <span data-ttu-id="df28f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df28f-111">-AsJob</span></span>
<span data-ttu-id="df28f-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="df28f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="df28f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df28f-113">-DefaultProfile</span></span>
<span data-ttu-id="df28f-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="df28f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df28f-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="df28f-115">-MoveCollectionName</span></span>
<span data-ttu-id="df28f-116">[移動集合名稱]。</span><span class="sxs-lookup"><span data-stu-id="df28f-116">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df28f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="df28f-117">-Name</span></span>
<span data-ttu-id="df28f-118">移動資源名稱。</span><span class="sxs-lookup"><span data-stu-id="df28f-118">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df28f-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="df28f-119">-NoWait</span></span>
<span data-ttu-id="df28f-120">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="df28f-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="df28f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df28f-121">-PassThru</span></span>
<span data-ttu-id="df28f-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="df28f-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="df28f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df28f-123">-ResourceGroupName</span></span>
<span data-ttu-id="df28f-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df28f-124">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df28f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df28f-125">-SubscriptionId</span></span>
<span data-ttu-id="df28f-126">訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="df28f-126">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df28f-127">-確認</span><span class="sxs-lookup"><span data-stu-id="df28f-127">-Confirm</span></span>
<span data-ttu-id="df28f-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="df28f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df28f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df28f-129">-WhatIf</span></span>
<span data-ttu-id="df28f-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="df28f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df28f-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df28f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df28f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df28f-132">CommonParameters</span></span>
<span data-ttu-id="df28f-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df28f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df28f-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="df28f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df28f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="df28f-135">INPUTS</span></span>

## <span data-ttu-id="df28f-136">輸出</span><span class="sxs-lookup"><span data-stu-id="df28f-136">OUTPUTS</span></span>

### <span data-ttu-id="df28f-137">IOperationStatus （ResourceMover）。 Api20191001Preview。</span><span class="sxs-lookup"><span data-stu-id="df28f-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="df28f-138">筆記</span><span class="sxs-lookup"><span data-stu-id="df28f-138">NOTES</span></span>

<span data-ttu-id="df28f-139">別名</span><span class="sxs-lookup"><span data-stu-id="df28f-139">ALIASES</span></span>

## <span data-ttu-id="df28f-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="df28f-140">RELATED LINKS</span></span>
