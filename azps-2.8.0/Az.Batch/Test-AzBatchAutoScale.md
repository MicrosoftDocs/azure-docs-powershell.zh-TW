---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/test-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
ms.openlocfilehash: dcac72f8ca362ea87d464e024d6e77b2b3b61425
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93799606"
---
# <span data-ttu-id="9b504-101">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="9b504-101">Test-AzBatchAutoScale</span></span>

## <span data-ttu-id="9b504-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b504-102">SYNOPSIS</span></span>
<span data-ttu-id="9b504-103">取得池中自動縮放公式的結果。</span><span class="sxs-lookup"><span data-stu-id="9b504-103">Gets the result of an automatic scaling formula on a pool.</span></span>

## <span data-ttu-id="9b504-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b504-104">SYNTAX</span></span>

```
Test-AzBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b504-105">說明</span><span class="sxs-lookup"><span data-stu-id="9b504-105">DESCRIPTION</span></span>
<span data-ttu-id="9b504-106">**Test AzBatchAutoScale** Cmdlet 會在指定的池中取得自動縮放公式的結果。</span><span class="sxs-lookup"><span data-stu-id="9b504-106">The **Test-AzBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="9b504-107">示例</span><span class="sxs-lookup"><span data-stu-id="9b504-107">EXAMPLES</span></span>

### <span data-ttu-id="9b504-108">範例1：評估資源庫上的自動縮放公式</span><span class="sxs-lookup"><span data-stu-id="9b504-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="9b504-109">第一個命令會將公式儲存在 $Formula 變數中，以供在範例中使用。</span><span class="sxs-lookup"><span data-stu-id="9b504-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="9b504-110">第二個命令會針對具有識別碼 ContosoPool 的池中評估自動縮放公式。</span><span class="sxs-lookup"><span data-stu-id="9b504-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="9b504-111">最後一個命令會使用標準的點語法來顯示 **結果** 。</span><span class="sxs-lookup"><span data-stu-id="9b504-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="9b504-112">參數</span><span class="sxs-lookup"><span data-stu-id="9b504-112">PARAMETERS</span></span>

### <span data-ttu-id="9b504-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="9b504-113">-AutoScaleFormula</span></span>
<span data-ttu-id="9b504-114">在池中指定所需計算節點數的公式。</span><span class="sxs-lookup"><span data-stu-id="9b504-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b504-115">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="9b504-115">-BatchContext</span></span>
<span data-ttu-id="9b504-116">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="9b504-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9b504-117">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="9b504-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9b504-118">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="9b504-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9b504-119">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="9b504-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9b504-120">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="9b504-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9b504-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b504-121">-DefaultProfile</span></span>
<span data-ttu-id="9b504-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b504-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b504-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="9b504-123">-Id</span></span>
<span data-ttu-id="9b504-124">指定要測試自動縮放比例的 [池] 物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b504-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b504-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b504-125">CommonParameters</span></span>
<span data-ttu-id="9b504-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b504-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b504-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b504-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b504-128">輸入</span><span class="sxs-lookup"><span data-stu-id="9b504-128">INPUTS</span></span>

### <span data-ttu-id="9b504-129">System.object</span><span class="sxs-lookup"><span data-stu-id="9b504-129">System.String</span></span>

### <span data-ttu-id="9b504-130">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="9b504-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9b504-131">輸出</span><span class="sxs-lookup"><span data-stu-id="9b504-131">OUTPUTS</span></span>

### <span data-ttu-id="9b504-132">Microsoft.Azure.Commands.Batch。PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="9b504-132">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="9b504-133">筆記</span><span class="sxs-lookup"><span data-stu-id="9b504-133">NOTES</span></span>

## <span data-ttu-id="9b504-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b504-134">RELATED LINKS</span></span>

[<span data-ttu-id="9b504-135">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="9b504-135">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="9b504-136">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="9b504-136">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="9b504-137">AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9b504-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9b504-138">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9b504-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

