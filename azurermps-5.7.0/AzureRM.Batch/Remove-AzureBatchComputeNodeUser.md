---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 668abe661eebfe600625ea85d5694838ef0e12f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625481"
---
# <span data-ttu-id="463eb-101">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="463eb-101">Remove-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="463eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="463eb-102">SYNOPSIS</span></span>
<span data-ttu-id="463eb-103">從批次計算節點刪除使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="463eb-103">Deletes a user account from a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="463eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="463eb-104">SYNTAX</span></span>

```
Remove-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="463eb-105">說明</span><span class="sxs-lookup"><span data-stu-id="463eb-105">DESCRIPTION</span></span>
<span data-ttu-id="463eb-106">**AzureBatchComputeNodeUser** Cmdlet 會從 Azure Batch 計算節點刪除使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="463eb-106">The **Remove-AzureBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="463eb-107">示例</span><span class="sxs-lookup"><span data-stu-id="463eb-107">EXAMPLES</span></span>

### <span data-ttu-id="463eb-108">範例1：不需確認就能從計算節點刪除使用者</span><span class="sxs-lookup"><span data-stu-id="463eb-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzureBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="463eb-109">這個命令會從名為 ComputeNode01 的計算節點中刪除名為 User14 的使用者。</span><span class="sxs-lookup"><span data-stu-id="463eb-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="463eb-110">Compute 節點位於名為 Pool01 的 pool 中。</span><span class="sxs-lookup"><span data-stu-id="463eb-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="463eb-111">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="463eb-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="463eb-112">因此，命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="463eb-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="463eb-113">參數</span><span class="sxs-lookup"><span data-stu-id="463eb-113">PARAMETERS</span></span>

### <span data-ttu-id="463eb-114">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="463eb-114">-BatchContext</span></span>
<span data-ttu-id="463eb-115">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="463eb-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="463eb-116">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="463eb-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="463eb-117">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="463eb-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="463eb-118">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="463eb-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="463eb-119">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="463eb-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="463eb-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="463eb-120">-ComputeNodeId</span></span>
<span data-ttu-id="463eb-121">指定此 Cmdlet 刪除使用者帳戶的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="463eb-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="463eb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463eb-122">-DefaultProfile</span></span>
<span data-ttu-id="463eb-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="463eb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="463eb-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="463eb-124">-Name</span></span>
<span data-ttu-id="463eb-125">指定要刪除的使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="463eb-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="463eb-126">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="463eb-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="463eb-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="463eb-127">-PoolId</span></span>
<span data-ttu-id="463eb-128">指定包含要刪除其使用者帳戶之計算節點的池 ID。</span><span class="sxs-lookup"><span data-stu-id="463eb-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="463eb-129">-確認</span><span class="sxs-lookup"><span data-stu-id="463eb-129">-Confirm</span></span>
<span data-ttu-id="463eb-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="463eb-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="463eb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="463eb-131">-WhatIf</span></span>
<span data-ttu-id="463eb-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="463eb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="463eb-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="463eb-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="463eb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463eb-134">CommonParameters</span></span>
<span data-ttu-id="463eb-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="463eb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463eb-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="463eb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463eb-137">輸入</span><span class="sxs-lookup"><span data-stu-id="463eb-137">INPUTS</span></span>

### <span data-ttu-id="463eb-138">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="463eb-138">BatchAccountContext</span></span>
<span data-ttu-id="463eb-139">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="463eb-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="463eb-140">輸出</span><span class="sxs-lookup"><span data-stu-id="463eb-140">OUTPUTS</span></span>

## <span data-ttu-id="463eb-141">筆記</span><span class="sxs-lookup"><span data-stu-id="463eb-141">NOTES</span></span>

## <span data-ttu-id="463eb-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="463eb-142">RELATED LINKS</span></span>

[<span data-ttu-id="463eb-143">新-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="463eb-143">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="463eb-144">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="463eb-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="463eb-145">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="463eb-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

