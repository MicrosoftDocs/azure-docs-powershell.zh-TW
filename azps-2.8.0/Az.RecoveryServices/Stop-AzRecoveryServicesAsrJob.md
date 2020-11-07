---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 867f06722e6840c9bba6065236fbf4f5f5c8b7f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792315"
---
# <span data-ttu-id="2b9d3-101">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2b9d3-101">Stop-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="2b9d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="2b9d3-103">停止 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="2b9d3-103">Stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="2b9d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b9d3-104">SYNTAX</span></span>

### <span data-ttu-id="2b9d3-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="2b9d3-105">ByObject (Default)</span></span>
```
Stop-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b9d3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2b9d3-106">ByName</span></span>
```
Stop-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b9d3-107">說明</span><span class="sxs-lookup"><span data-stu-id="2b9d3-107">DESCRIPTION</span></span>
<span data-ttu-id="2b9d3-108">**AzRecoveryServicesAsrJob** Cmdlet 會停止指定的 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="2b9d3-108">The **Stop-AzRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="2b9d3-109">示例</span><span class="sxs-lookup"><span data-stu-id="2b9d3-109">EXAMPLES</span></span>

### <span data-ttu-id="2b9d3-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2b9d3-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="2b9d3-111">嘗試停止指定的工作，並傳回更新的 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="2b9d3-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="2b9d3-112">參數</span><span class="sxs-lookup"><span data-stu-id="2b9d3-112">PARAMETERS</span></span>

### <span data-ttu-id="2b9d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b9d3-113">-DefaultProfile</span></span>
<span data-ttu-id="2b9d3-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b9d3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2b9d3-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b9d3-115">-InputObject</span></span>
<span data-ttu-id="2b9d3-116">輸入物件：指定要停止的 ASR 作業對應的 ASR 工作物件</span><span class="sxs-lookup"><span data-stu-id="2b9d3-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b9d3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b9d3-117">-Name</span></span>
<span data-ttu-id="2b9d3-118">指定 asr 作業名稱要停止的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="2b9d3-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9d3-119">-確認</span><span class="sxs-lookup"><span data-stu-id="2b9d3-119">-Confirm</span></span>
<span data-ttu-id="2b9d3-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2b9d3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b9d3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b9d3-121">-WhatIf</span></span>
<span data-ttu-id="2b9d3-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2b9d3-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b9d3-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b9d3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b9d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b9d3-124">CommonParameters</span></span>
<span data-ttu-id="2b9d3-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b9d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b9d3-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2b9d3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b9d3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2b9d3-127">INPUTS</span></span>

### <span data-ttu-id="2b9d3-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2b9d3-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2b9d3-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2b9d3-129">OUTPUTS</span></span>

### <span data-ttu-id="2b9d3-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2b9d3-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2b9d3-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2b9d3-131">NOTES</span></span>

## <span data-ttu-id="2b9d3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b9d3-132">RELATED LINKS</span></span>

[<span data-ttu-id="2b9d3-133">AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2b9d3-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="2b9d3-134">重新開機-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2b9d3-134">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="2b9d3-135">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2b9d3-135">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)