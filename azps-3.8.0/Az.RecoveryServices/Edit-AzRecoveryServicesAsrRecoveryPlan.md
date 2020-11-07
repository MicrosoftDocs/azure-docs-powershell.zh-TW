---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/edit-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: be66887225ee78b31497bbd8918faae9535731de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798645"
---
# <span data-ttu-id="57481-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="57481-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="57481-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57481-102">SYNOPSIS</span></span>
<span data-ttu-id="57481-103">編輯網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="57481-103">Edits a Site Recovery plan.</span></span>

## <span data-ttu-id="57481-104">句法</span><span class="sxs-lookup"><span data-stu-id="57481-104">SYNTAX</span></span>

### <span data-ttu-id="57481-105">AppendGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="57481-105">AppendGroup (Default)</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57481-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="57481-106">RemoveGroup</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57481-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="57481-107">AddReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57481-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="57481-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57481-109">說明</span><span class="sxs-lookup"><span data-stu-id="57481-109">DESCRIPTION</span></span>
<span data-ttu-id="57481-110">**AzRecoveryServicesAsrRecoveryPlan** Cmdlet 編輯 Azure 網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="57481-110">The **Edit-AzRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="57481-111">示例</span><span class="sxs-lookup"><span data-stu-id="57481-111">EXAMPLES</span></span>

### <span data-ttu-id="57481-112">範例1</span><span class="sxs-lookup"><span data-stu-id="57481-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="57481-113">將群組附加至現有的 Azure 網站復原方案，並傳回記憶體更新的復原方案。</span><span class="sxs-lookup"><span data-stu-id="57481-113">Appends a group to existing Azure Site Recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="57481-114">參數</span><span class="sxs-lookup"><span data-stu-id="57481-114">PARAMETERS</span></span>

### <span data-ttu-id="57481-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="57481-115">-AddProtectedItem</span></span>
<span data-ttu-id="57481-116">要新增到復原方案物件之復原方案群組的 ASR 複製受保護專案清單。</span><span class="sxs-lookup"><span data-stu-id="57481-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57481-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="57481-117">-AppendGroup</span></span>
<span data-ttu-id="57481-118">[切換參數]，將復原方案群組附加到復原方案物件。</span><span class="sxs-lookup"><span data-stu-id="57481-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AppendGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57481-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57481-119">-DefaultProfile</span></span>
<span data-ttu-id="57481-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="57481-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="57481-121">-群組</span><span class="sxs-lookup"><span data-stu-id="57481-121">-Group</span></span>
<span data-ttu-id="57481-122">指定復原方案群組。</span><span class="sxs-lookup"><span data-stu-id="57481-122">Specifies a recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57481-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57481-123">-InputObject</span></span>
<span data-ttu-id="57481-124">要在記憶體作業中 (編輯的 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="57481-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="57481-125">若要更新復原方案，請執行 Update-AzASRRecoveryPlan 與已編輯的復原方案物件。 ) </span><span class="sxs-lookup"><span data-stu-id="57481-125">To update the recovery plan run Update-AzASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57481-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="57481-126">-RemoveGroup</span></span>
<span data-ttu-id="57481-127">從復原方案物件中移除指定的群組。</span><span class="sxs-lookup"><span data-stu-id="57481-127">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57481-128">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="57481-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="57481-129">要從復原方案物件的復原方案群組中移除的 ASR 複製受保護專案清單。</span><span class="sxs-lookup"><span data-stu-id="57481-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57481-130">-確認</span><span class="sxs-lookup"><span data-stu-id="57481-130">-Confirm</span></span>
<span data-ttu-id="57481-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="57481-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57481-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57481-132">-WhatIf</span></span>
<span data-ttu-id="57481-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57481-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57481-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57481-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57481-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57481-135">CommonParameters</span></span>
<span data-ttu-id="57481-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57481-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57481-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="57481-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57481-138">輸入</span><span class="sxs-lookup"><span data-stu-id="57481-138">INPUTS</span></span>

### <span data-ttu-id="57481-139">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="57481-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="57481-140">輸出</span><span class="sxs-lookup"><span data-stu-id="57481-140">OUTPUTS</span></span>

### <span data-ttu-id="57481-141">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="57481-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="57481-142">筆記</span><span class="sxs-lookup"><span data-stu-id="57481-142">NOTES</span></span>

## <span data-ttu-id="57481-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="57481-143">RELATED LINKS</span></span>

[<span data-ttu-id="57481-144">AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="57481-144">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="57481-145">新-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="57481-145">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)