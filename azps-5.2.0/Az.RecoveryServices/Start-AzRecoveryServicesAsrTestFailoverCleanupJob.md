---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 5d147ac47b2f53aa48f8989884b99c519e5ffb08
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274627"
---
# <span data-ttu-id="5c005-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="5c005-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="5c005-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c005-102">SYNOPSIS</span></span>
<span data-ttu-id="5c005-103">啟動測試容錯移轉清除操作。</span><span class="sxs-lookup"><span data-stu-id="5c005-103">Starts the test failover cleanup operation.</span></span>

## <span data-ttu-id="5c005-104">句法</span><span class="sxs-lookup"><span data-stu-id="5c005-104">SYNTAX</span></span>

### <span data-ttu-id="5c005-105">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="5c005-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c005-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5c005-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c005-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="5c005-107">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c005-108">說明</span><span class="sxs-lookup"><span data-stu-id="5c005-108">DESCRIPTION</span></span>
<span data-ttu-id="5c005-109">**AzRecoveryServicesAsrTestFailoverCleanupJob** Cmdlet 會在已執行測試容錯移轉的複製受保護專案或復原方案上啟動測試容錯移轉清除作業。</span><span class="sxs-lookup"><span data-stu-id="5c005-109">The **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="5c005-110">示例</span><span class="sxs-lookup"><span data-stu-id="5c005-110">EXAMPLES</span></span>

### <span data-ttu-id="5c005-111">範例1</span><span class="sxs-lookup"><span data-stu-id="5c005-111">Example 1</span></span>

<span data-ttu-id="5c005-112">追蹤 Azure 網站復原 recoveryPlan 的測試容錯移轉清除的工作。</span><span class="sxs-lookup"><span data-stu-id="5c005-112">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

```powershell
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan $recoveryPlan -Comment "testing done"
```

### <span data-ttu-id="5c005-113">範例2</span><span class="sxs-lookup"><span data-stu-id="5c005-113">Example 2</span></span>

<span data-ttu-id="5c005-114">啟動測試容錯移轉清除操作。</span><span class="sxs-lookup"><span data-stu-id="5c005-114">Starts the test failover cleanup operation.</span></span> <span data-ttu-id="5c005-115"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="5c005-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -Comment 'testing done' -ReplicationProtectedItem $rpi
```

## <span data-ttu-id="5c005-116">參數</span><span class="sxs-lookup"><span data-stu-id="5c005-116">PARAMETERS</span></span>

### <span data-ttu-id="5c005-117">-批註</span><span class="sxs-lookup"><span data-stu-id="5c005-117">-Comment</span></span>
<span data-ttu-id="5c005-118">測試容錯移轉的使用者意見。</span><span class="sxs-lookup"><span data-stu-id="5c005-118">User Comment for Test Failover.</span></span>

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

### <span data-ttu-id="5c005-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c005-119">-DefaultProfile</span></span>
<span data-ttu-id="5c005-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c005-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c005-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5c005-121">-RecoveryPlan</span></span>
<span data-ttu-id="5c005-122">執行測試容錯移轉清除的復原方案。</span><span class="sxs-lookup"><span data-stu-id="5c005-122">Recovery Plan to perform the test failover cleanup on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c005-123">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5c005-123">-ReplicationProtectedItem</span></span>
<span data-ttu-id="5c005-124">複製受保護的專案，以執行測試容錯移轉清除。</span><span class="sxs-lookup"><span data-stu-id="5c005-124">Replication Protected Item to perform the test failover cleanup on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c005-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c005-125">-ResourceId</span></span>
<span data-ttu-id="5c005-126">Cleaningup 測試容錯移轉的複製受保護專案/復原方案的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c005-126">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c005-127">-確認</span><span class="sxs-lookup"><span data-stu-id="5c005-127">-Confirm</span></span>
<span data-ttu-id="5c005-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5c005-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c005-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c005-129">-WhatIf</span></span>
<span data-ttu-id="5c005-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c005-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c005-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c005-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c005-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c005-132">CommonParameters</span></span>
<span data-ttu-id="5c005-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5c005-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c005-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5c005-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c005-135">輸入</span><span class="sxs-lookup"><span data-stu-id="5c005-135">INPUTS</span></span>

### <span data-ttu-id="5c005-136">System.object</span><span class="sxs-lookup"><span data-stu-id="5c005-136">System.String</span></span>

### <span data-ttu-id="5c005-137">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5c005-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="5c005-138">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5c005-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="5c005-139">輸出</span><span class="sxs-lookup"><span data-stu-id="5c005-139">OUTPUTS</span></span>

### <span data-ttu-id="5c005-140">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5c005-140">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5c005-141">筆記</span><span class="sxs-lookup"><span data-stu-id="5c005-141">NOTES</span></span>

## <span data-ttu-id="5c005-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c005-142">RELATED LINKS</span></span>