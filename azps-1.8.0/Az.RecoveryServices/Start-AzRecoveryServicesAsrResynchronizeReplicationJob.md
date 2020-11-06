---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 48a17c0b2bd8c1d62de1b3ebd5eccc5171d65837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621047"
---
# <span data-ttu-id="30a0a-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="30a0a-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="30a0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="30a0a-103">開始複製重新同步。</span><span class="sxs-lookup"><span data-stu-id="30a0a-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="30a0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="30a0a-104">SYNTAX</span></span>

### <span data-ttu-id="30a0a-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="30a0a-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30a0a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="30a0a-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30a0a-107">說明</span><span class="sxs-lookup"><span data-stu-id="30a0a-107">DESCRIPTION</span></span>
<span data-ttu-id="30a0a-108">如果受保護的狀態為重新同步需要的狀態，則 **AzRecoveryServicesAsrResynchronizeReplicationJob** Cmdlet 會開始重新同步複製指定的受保護專案。</span><span class="sxs-lookup"><span data-stu-id="30a0a-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="30a0a-109">示例</span><span class="sxs-lookup"><span data-stu-id="30a0a-109">EXAMPLES</span></span>

### <span data-ttu-id="30a0a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="30a0a-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="30a0a-111">啟動工作以在已傳送的複製受保護的專案上重新同步處理複製。</span><span class="sxs-lookup"><span data-stu-id="30a0a-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="30a0a-112">參數</span><span class="sxs-lookup"><span data-stu-id="30a0a-112">PARAMETERS</span></span>

### <span data-ttu-id="30a0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a0a-113">-DefaultProfile</span></span>
<span data-ttu-id="30a0a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="30a0a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30a0a-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="30a0a-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="30a0a-116">要重新同步複製的 ASR 複製受保護專案。</span><span class="sxs-lookup"><span data-stu-id="30a0a-116">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30a0a-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30a0a-117">-ResourceId</span></span>
<span data-ttu-id="30a0a-118">要重新同步複製受保護專案的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="30a0a-118">Resource Id of replication protected item to resynchronize.</span></span>

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

### <span data-ttu-id="30a0a-119">-確認</span><span class="sxs-lookup"><span data-stu-id="30a0a-119">-Confirm</span></span>
<span data-ttu-id="30a0a-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="30a0a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30a0a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30a0a-121">-WhatIf</span></span>
<span data-ttu-id="30a0a-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30a0a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30a0a-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30a0a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30a0a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a0a-124">CommonParameters</span></span>
<span data-ttu-id="30a0a-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30a0a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a0a-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="30a0a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a0a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="30a0a-127">INPUTS</span></span>

### <span data-ttu-id="30a0a-128">System.object</span><span class="sxs-lookup"><span data-stu-id="30a0a-128">System.String</span></span>

### <span data-ttu-id="30a0a-129">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="30a0a-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="30a0a-130">輸出</span><span class="sxs-lookup"><span data-stu-id="30a0a-130">OUTPUTS</span></span>

### <span data-ttu-id="30a0a-131">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="30a0a-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="30a0a-132">筆記</span><span class="sxs-lookup"><span data-stu-id="30a0a-132">NOTES</span></span>

## <span data-ttu-id="30a0a-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="30a0a-133">RELATED LINKS</span></span>