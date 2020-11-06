---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
ms.openlocfilehash: 69b1ef139569a4a89c5c0f11d54ddbf5407fa653
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93623304"
---
# <span data-ttu-id="db43b-101">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="db43b-101">New-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="db43b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db43b-102">SYNOPSIS</span></span>
<span data-ttu-id="db43b-103">在批次計算節點上建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="db43b-103">Creates a user account on a Batch compute node.</span></span>

## <span data-ttu-id="db43b-104">句法</span><span class="sxs-lookup"><span data-stu-id="db43b-104">SYNTAX</span></span>

### <span data-ttu-id="db43b-105">標識號</span><span class="sxs-lookup"><span data-stu-id="db43b-105">Id</span></span>
```
New-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db43b-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="db43b-106">ParentObject</span></span>
```
New-AzBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db43b-107">說明</span><span class="sxs-lookup"><span data-stu-id="db43b-107">DESCRIPTION</span></span>
<span data-ttu-id="db43b-108">**新的 AzBatchComputeNodeUser** Cmdlet 會在 Azure Batch 計算節點上建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="db43b-108">The **New-AzBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="db43b-109">示例</span><span class="sxs-lookup"><span data-stu-id="db43b-109">EXAMPLES</span></span>

### <span data-ttu-id="db43b-110">範例1：建立擁有管理認證的使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="db43b-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="db43b-111">這個命令會在具有識別碼 ComputeNode01 的 [計算] 節點上建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="db43b-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="db43b-112">節點位於 ID 為 MyPool01 的池中。</span><span class="sxs-lookup"><span data-stu-id="db43b-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="db43b-113">使用者名稱為 TestUser、密碼為 Password、帳戶在七天后到期，且帳戶具有管理認證。</span><span class="sxs-lookup"><span data-stu-id="db43b-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="db43b-114">範例2：使用管線在計算節點上建立使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="db43b-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="db43b-115">這個命令會使用 **AzBatchComputeNode** Cmdlet 取得名為 ComputeNode01 的計算節點。</span><span class="sxs-lookup"><span data-stu-id="db43b-115">This command gets the compute node named ComputeNode01 by using the **Get-AzBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="db43b-116">該節點位於 ID 為 MyPool01 的池中。</span><span class="sxs-lookup"><span data-stu-id="db43b-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="db43b-117">命令會使用管線運算子，將該計算節點傳到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db43b-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="db43b-118">此命令會建立一個使用者帳戶，並將使用者名稱 TestUserand 密碼密碼。</span><span class="sxs-lookup"><span data-stu-id="db43b-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="db43b-119">參數</span><span class="sxs-lookup"><span data-stu-id="db43b-119">PARAMETERS</span></span>

### <span data-ttu-id="db43b-120">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="db43b-120">-BatchContext</span></span>
<span data-ttu-id="db43b-121">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="db43b-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="db43b-122">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="db43b-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="db43b-123">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="db43b-123">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="db43b-124">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="db43b-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="db43b-125">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="db43b-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="db43b-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="db43b-126">-ComputeNode</span></span>
<span data-ttu-id="db43b-127">將此 Cmdlet 建立使用者帳戶的計算節點指定為 **PSComputeNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="db43b-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db43b-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="db43b-128">-ComputeNodeId</span></span>
<span data-ttu-id="db43b-129">指定此 Cmdlet 建立使用者帳戶的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="db43b-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db43b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db43b-130">-DefaultProfile</span></span>
<span data-ttu-id="db43b-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="db43b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db43b-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="db43b-132">-ExpiryTime</span></span>
<span data-ttu-id="db43b-133">指定新使用者帳戶的到期時間。</span><span class="sxs-lookup"><span data-stu-id="db43b-133">Specifies the expiry time for the new user account.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db43b-134">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="db43b-134">-IsAdmin</span></span>
<span data-ttu-id="db43b-135">表示 Cmdlet 會建立擁有管理認證的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="db43b-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="db43b-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="db43b-136">-Name</span></span>
<span data-ttu-id="db43b-137">指定新的本機 Windows 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="db43b-137">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="db43b-138">-Password</span><span class="sxs-lookup"><span data-stu-id="db43b-138">-Password</span></span>
<span data-ttu-id="db43b-139">指定使用者帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="db43b-139">Specifies the user account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db43b-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="db43b-140">-PoolId</span></span>
<span data-ttu-id="db43b-141">指定包含要在其上建立使用者帳戶之計算節點的 pool 的 ID。</span><span class="sxs-lookup"><span data-stu-id="db43b-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db43b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db43b-142">CommonParameters</span></span>
<span data-ttu-id="db43b-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db43b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db43b-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="db43b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db43b-145">輸入</span><span class="sxs-lookup"><span data-stu-id="db43b-145">INPUTS</span></span>

### <span data-ttu-id="db43b-146">Microsoft.Azure.Commands.Batch。PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="db43b-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="db43b-147">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="db43b-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="db43b-148">輸出</span><span class="sxs-lookup"><span data-stu-id="db43b-148">OUTPUTS</span></span>

### <span data-ttu-id="db43b-149">System.void</span><span class="sxs-lookup"><span data-stu-id="db43b-149">System.Void</span></span>

## <span data-ttu-id="db43b-150">筆記</span><span class="sxs-lookup"><span data-stu-id="db43b-150">NOTES</span></span>

## <span data-ttu-id="db43b-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="db43b-151">RELATED LINKS</span></span>

[<span data-ttu-id="db43b-152">AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="db43b-152">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="db43b-153">AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="db43b-153">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="db43b-154">移除-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="db43b-154">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="db43b-155">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db43b-155">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

