---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: d6a17588b5718f9a6d735521a7a136cba472ead0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958367"
---
# <span data-ttu-id="0b5e0-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b5e0-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="0b5e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b5e0-102">SYNOPSIS</span></span>
<span data-ttu-id="0b5e0-103">設定作業排程。</span><span class="sxs-lookup"><span data-stu-id="0b5e0-103">Sets a job schedule.</span></span>

## <span data-ttu-id="0b5e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b5e0-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b5e0-105">說明</span><span class="sxs-lookup"><span data-stu-id="0b5e0-105">DESCRIPTION</span></span>
<span data-ttu-id="0b5e0-106">**AzBatchJobSchedule** Cmdlet 會在 Azure Batch service 中設定作業排程。</span><span class="sxs-lookup"><span data-stu-id="0b5e0-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="0b5e0-107">示例</span><span class="sxs-lookup"><span data-stu-id="0b5e0-107">EXAMPLES</span></span>

### <span data-ttu-id="0b5e0-108">範例1：更新作業排程</span><span class="sxs-lookup"><span data-stu-id="0b5e0-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="0b5e0-109">第一個命令會使用 **AzBatchJobSchedule** 來取得作業，然後將它儲存在 $JobSchedule 變數中。</span><span class="sxs-lookup"><span data-stu-id="0b5e0-109">The first command gets a job by using **Get-AzBatchJobSchedule** , and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="0b5e0-110">第二個命令會修改物件上的定期間隔 `$JobSchedule.Schedule` 。</span><span class="sxs-lookup"><span data-stu-id="0b5e0-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="0b5e0-111">最後一個命令會更新批次服務，以符合 $JobSchedule 中的本機物件。</span><span class="sxs-lookup"><span data-stu-id="0b5e0-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="0b5e0-112">參數</span><span class="sxs-lookup"><span data-stu-id="0b5e0-112">PARAMETERS</span></span>

### <span data-ttu-id="0b5e0-113">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="0b5e0-113">-BatchContext</span></span>
<span data-ttu-id="0b5e0-114">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="0b5e0-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0b5e0-115">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="0b5e0-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0b5e0-116">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="0b5e0-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0b5e0-117">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="0b5e0-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0b5e0-118">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="0b5e0-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5e0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b5e0-119">-DefaultProfile</span></span>
<span data-ttu-id="0b5e0-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b5e0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b5e0-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b5e0-121">-JobSchedule</span></span>
<span data-ttu-id="0b5e0-122">指定代表作業排程的 **PSCloudJobSchedule** 物件。</span><span class="sxs-lookup"><span data-stu-id="0b5e0-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="0b5e0-123">若要取得 **PSCloudJobSchedule** 物件，請使用 Get-AzBatchJobSchedule Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b5e0-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b5e0-124">CommonParameters</span></span>
<span data-ttu-id="0b5e0-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b5e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b5e0-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0b5e0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b5e0-127">輸入</span><span class="sxs-lookup"><span data-stu-id="0b5e0-127">INPUTS</span></span>

### <span data-ttu-id="0b5e0-128">Microsoft.Azure.Commands.Batch。PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b5e0-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="0b5e0-129">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="0b5e0-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0b5e0-130">輸出</span><span class="sxs-lookup"><span data-stu-id="0b5e0-130">OUTPUTS</span></span>

### <span data-ttu-id="0b5e0-131">System.void</span><span class="sxs-lookup"><span data-stu-id="0b5e0-131">System.Void</span></span>

## <span data-ttu-id="0b5e0-132">筆記</span><span class="sxs-lookup"><span data-stu-id="0b5e0-132">NOTES</span></span>

## <span data-ttu-id="0b5e0-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b5e0-133">RELATED LINKS</span></span>

[<span data-ttu-id="0b5e0-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b5e0-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="0b5e0-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b5e0-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="0b5e0-136">AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b5e0-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="0b5e0-137">新-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b5e0-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="0b5e0-138">移除-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b5e0-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="0b5e0-139">停止 AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b5e0-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

