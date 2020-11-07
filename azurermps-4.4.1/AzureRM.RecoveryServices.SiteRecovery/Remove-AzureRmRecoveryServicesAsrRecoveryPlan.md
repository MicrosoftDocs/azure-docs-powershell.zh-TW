---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 2d172c440163d70ef388c7de190371492767b2e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626236"
---
# <span data-ttu-id="58b03-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="58b03-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="58b03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58b03-102">SYNOPSIS</span></span>
<span data-ttu-id="58b03-103">從復原服務電子倉庫 Delets 指定的 ASR 恢復方案。</span><span class="sxs-lookup"><span data-stu-id="58b03-103">Delets the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58b03-104">句法</span><span class="sxs-lookup"><span data-stu-id="58b03-104">SYNTAX</span></span>

### <span data-ttu-id="58b03-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="58b03-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58b03-106">ByName</span><span class="sxs-lookup"><span data-stu-id="58b03-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58b03-107">說明</span><span class="sxs-lookup"><span data-stu-id="58b03-107">DESCRIPTION</span></span>
<span data-ttu-id="58b03-108">**AzureRmRecoveryServicesAsrRecoveryPlan** Cmdlet 會從 [恢復服務] 保存庫中刪除指定的復原方案。</span><span class="sxs-lookup"><span data-stu-id="58b03-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="58b03-109">示例</span><span class="sxs-lookup"><span data-stu-id="58b03-109">EXAMPLES</span></span>

### <span data-ttu-id="58b03-110">範例1</span><span class="sxs-lookup"><span data-stu-id="58b03-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="58b03-111">開始刪除指定的復原方案，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="58b03-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="58b03-112">參數</span><span class="sxs-lookup"><span data-stu-id="58b03-112">PARAMETERS</span></span>

### <span data-ttu-id="58b03-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58b03-113">-InputObject</span></span>
<span data-ttu-id="58b03-114">Cmdlet 的輸入物件：對應至要刪除之復原方案的 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="58b03-114">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58b03-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="58b03-115">-Name</span></span>
<span data-ttu-id="58b03-116">指定要刪除的復原方案名稱。</span><span class="sxs-lookup"><span data-stu-id="58b03-116">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58b03-117">-確認</span><span class="sxs-lookup"><span data-stu-id="58b03-117">-Confirm</span></span>
<span data-ttu-id="58b03-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58b03-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58b03-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58b03-119">-WhatIf</span></span>
<span data-ttu-id="58b03-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58b03-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58b03-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58b03-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58b03-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b03-122">CommonParameters</span></span>
<span data-ttu-id="58b03-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58b03-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b03-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58b03-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b03-125">輸入</span><span class="sxs-lookup"><span data-stu-id="58b03-125">INPUTS</span></span>

### <span data-ttu-id="58b03-126">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="58b03-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="58b03-127">輸出</span><span class="sxs-lookup"><span data-stu-id="58b03-127">OUTPUTS</span></span>

### <span data-ttu-id="58b03-128">System.object</span><span class="sxs-lookup"><span data-stu-id="58b03-128">System.Object</span></span>

## <span data-ttu-id="58b03-129">筆記</span><span class="sxs-lookup"><span data-stu-id="58b03-129">NOTES</span></span>

## <span data-ttu-id="58b03-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="58b03-130">RELATED LINKS</span></span>

[<span data-ttu-id="58b03-131">AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="58b03-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="58b03-132">新-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="58b03-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="58b03-133">更新-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="58b03-133">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)

