---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 61bb846067127b8e7d0a4deca0dd9a726d9dd1f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275503"
---
# <span data-ttu-id="1900f-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="1900f-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="1900f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1900f-102">SYNOPSIS</span></span>
<span data-ttu-id="1900f-103">啟動未計畫的容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="1900f-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="1900f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1900f-104">SYNTAX</span></span>

### <span data-ttu-id="1900f-105">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="1900f-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1900f-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="1900f-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1900f-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="1900f-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1900f-108">說明</span><span class="sxs-lookup"><span data-stu-id="1900f-108">DESCRIPTION</span></span>
<span data-ttu-id="1900f-109">**AzRecoveryServicesAsrUnplannedFailoverJob** Cmdlet 會啟動 Azure Site Recovery 複製受保護的專案或復原方案的未計畫式容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="1900f-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="1900f-110">您可以使用 Get-AzRecoveryServicesAsrJob Cmdlet 來檢查作業是否已成功完成。</span><span class="sxs-lookup"><span data-stu-id="1900f-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="1900f-111">示例</span><span class="sxs-lookup"><span data-stu-id="1900f-111">EXAMPLES</span></span>

### <span data-ttu-id="1900f-112">範例1</span><span class="sxs-lookup"><span data-stu-id="1900f-112">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="1900f-113">使用指定的參數為復原方案啟動未計畫的容錯移轉作業，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="1900f-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="1900f-114">範例2</span><span class="sxs-lookup"><span data-stu-id="1900f-114">Example 2</span></span>

<span data-ttu-id="1900f-115">啟動未計畫的容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="1900f-115">Starts an unplanned failover operation.</span></span> <span data-ttu-id="1900f-116"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="1900f-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrUnplannedFailoverJob -Direction PrimaryToRecovery -RecoveryPoint $rp[0] -ReplicationProtectedItem $ReplicationProtectedItem
```

## <span data-ttu-id="1900f-117">參數</span><span class="sxs-lookup"><span data-stu-id="1900f-117">PARAMETERS</span></span>

### <span data-ttu-id="1900f-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1900f-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="1900f-119">指定受保護專案容錯移轉的資料加密主要憑證檔路徑。</span><span class="sxs-lookup"><span data-stu-id="1900f-119">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="1900f-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1900f-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="1900f-121">指定受保護專案容錯移轉的資料加密次要憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="1900f-121">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="1900f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1900f-122">-DefaultProfile</span></span>
<span data-ttu-id="1900f-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1900f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1900f-124">方向</span><span class="sxs-lookup"><span data-stu-id="1900f-124">-Direction</span></span>
<span data-ttu-id="1900f-125">指定容錯移轉方向。</span><span class="sxs-lookup"><span data-stu-id="1900f-125">Specifies the failover direction.</span></span>
<span data-ttu-id="1900f-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1900f-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1900f-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="1900f-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="1900f-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="1900f-128">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1900f-129">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="1900f-129">-PerformSourceSideAction</span></span>
<span data-ttu-id="1900f-130">在開始未計畫的容錯移轉前，請在源端執行操作。</span><span class="sxs-lookup"><span data-stu-id="1900f-130">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1900f-131">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1900f-131">-RecoveryPlan</span></span>
<span data-ttu-id="1900f-132">指定 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="1900f-132">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="1900f-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1900f-133">-RecoveryPoint</span></span>
<span data-ttu-id="1900f-134">指定要將受保護電腦容錯移轉至其中的自訂復原點。</span><span class="sxs-lookup"><span data-stu-id="1900f-134">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1900f-135">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="1900f-135">-RecoveryTag</span></span>
<span data-ttu-id="1900f-136">指定要容錯移轉至的復原標記。</span><span class="sxs-lookup"><span data-stu-id="1900f-136">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1900f-137">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1900f-137">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1900f-138">指定 azure site recovery 複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="1900f-138">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1900f-139">-確認</span><span class="sxs-lookup"><span data-stu-id="1900f-139">-Confirm</span></span>
<span data-ttu-id="1900f-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1900f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1900f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1900f-141">-WhatIf</span></span>
<span data-ttu-id="1900f-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1900f-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1900f-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1900f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1900f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1900f-144">CommonParameters</span></span>
<span data-ttu-id="1900f-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1900f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1900f-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1900f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1900f-147">輸入</span><span class="sxs-lookup"><span data-stu-id="1900f-147">INPUTS</span></span>

### <span data-ttu-id="1900f-148">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1900f-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="1900f-149">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1900f-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1900f-150">輸出</span><span class="sxs-lookup"><span data-stu-id="1900f-150">OUTPUTS</span></span>

### <span data-ttu-id="1900f-151">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1900f-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1900f-152">筆記</span><span class="sxs-lookup"><span data-stu-id="1900f-152">NOTES</span></span>

## <span data-ttu-id="1900f-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="1900f-153">RELATED LINKS</span></span>

[<span data-ttu-id="1900f-154">AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="1900f-154">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)