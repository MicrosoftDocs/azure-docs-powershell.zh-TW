---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: 7878932b0e7a2aad6e171c39e546ad86b2ea0a7c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791174"
---
# <span data-ttu-id="912c8-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="912c8-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="912c8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="912c8-102">SYNOPSIS</span></span>
<span data-ttu-id="912c8-103">移除 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="912c8-103">Removes a resource group.</span></span>

## <span data-ttu-id="912c8-104">句法</span><span class="sxs-lookup"><span data-stu-id="912c8-104">SYNTAX</span></span>

### <span data-ttu-id="912c8-105">RemoveByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="912c8-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="912c8-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="912c8-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup -Id <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="912c8-107">說明</span><span class="sxs-lookup"><span data-stu-id="912c8-107">DESCRIPTION</span></span>
<span data-ttu-id="912c8-108">**AzResourceGroup** Cmdlet 會從目前的訂閱中移除 Azure 資源群組及其資源。</span><span class="sxs-lookup"><span data-stu-id="912c8-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="912c8-109">若要刪除資源，但要保留資源群組，請使用 Remove-AzResource Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="912c8-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="912c8-110">示例</span><span class="sxs-lookup"><span data-stu-id="912c8-110">EXAMPLES</span></span>

### <span data-ttu-id="912c8-111">範例1：移除資源群組</span><span class="sxs-lookup"><span data-stu-id="912c8-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="912c8-112">這個命令會從訂閱中移除 ContosoRG01 資源群組。</span><span class="sxs-lookup"><span data-stu-id="912c8-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="912c8-113">此 Cmdlet 會提示您進行確認，且不會傳回輸出。</span><span class="sxs-lookup"><span data-stu-id="912c8-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="912c8-114">範例2：移除資源群組而不進行確認</span><span class="sxs-lookup"><span data-stu-id="912c8-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Verbose -Force
```

<span data-ttu-id="912c8-115">這個命令會使用 Get-AzResourceGroup Cmdlet 來取得資源群組 ContosoRG01，然後透過使用管線運算子將它傳遞給 **Remove-AzResourceGroup** 。</span><span class="sxs-lookup"><span data-stu-id="912c8-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="912c8-116">*詳細* 的常見參數會取得操作的狀態資訊，而 *Force* 參數則會取消確認提示。</span><span class="sxs-lookup"><span data-stu-id="912c8-116">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="912c8-117">範例3：移除所有資源群組</span><span class="sxs-lookup"><span data-stu-id="912c8-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="912c8-118">這個命令會使用 **AzResourceGroup** Cmdlet 取得所有資源群組，然後透過使用管線運算子將它們傳遞給 **Remove-AzResourceGroup** 。</span><span class="sxs-lookup"><span data-stu-id="912c8-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="912c8-119">參數</span><span class="sxs-lookup"><span data-stu-id="912c8-119">PARAMETERS</span></span>

### <span data-ttu-id="912c8-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="912c8-120">-ApiVersion</span></span>
<span data-ttu-id="912c8-121">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="912c8-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="912c8-122">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="912c8-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="912c8-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="912c8-123">-AsJob</span></span>
<span data-ttu-id="912c8-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="912c8-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="912c8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="912c8-125">-DefaultProfile</span></span>
<span data-ttu-id="912c8-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="912c8-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="912c8-127">-Force</span><span class="sxs-lookup"><span data-stu-id="912c8-127">-Force</span></span>
<span data-ttu-id="912c8-128">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="912c8-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="912c8-129">-識別碼</span><span class="sxs-lookup"><span data-stu-id="912c8-129">-Id</span></span>
<span data-ttu-id="912c8-130">指定要移除之資源群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="912c8-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="912c8-131">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="912c8-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912c8-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="912c8-132">-Name</span></span>
<span data-ttu-id="912c8-133">指定要移除之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="912c8-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="912c8-134">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="912c8-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912c8-135">-預先</span><span class="sxs-lookup"><span data-stu-id="912c8-135">-Pre</span></span>
<span data-ttu-id="912c8-136">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="912c8-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="912c8-137">-確認</span><span class="sxs-lookup"><span data-stu-id="912c8-137">-Confirm</span></span>
<span data-ttu-id="912c8-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="912c8-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="912c8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="912c8-139">-WhatIf</span></span>
<span data-ttu-id="912c8-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="912c8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="912c8-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="912c8-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="912c8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="912c8-142">CommonParameters</span></span>
<span data-ttu-id="912c8-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="912c8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="912c8-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="912c8-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="912c8-145">輸入</span><span class="sxs-lookup"><span data-stu-id="912c8-145">INPUTS</span></span>

### <span data-ttu-id="912c8-146">System.object</span><span class="sxs-lookup"><span data-stu-id="912c8-146">System.String</span></span>

## <span data-ttu-id="912c8-147">輸出</span><span class="sxs-lookup"><span data-stu-id="912c8-147">OUTPUTS</span></span>

### <span data-ttu-id="912c8-148">System.object</span><span class="sxs-lookup"><span data-stu-id="912c8-148">System.Boolean</span></span>

## <span data-ttu-id="912c8-149">筆記</span><span class="sxs-lookup"><span data-stu-id="912c8-149">NOTES</span></span>

## <span data-ttu-id="912c8-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="912c8-150">RELATED LINKS</span></span>

[<span data-ttu-id="912c8-151">AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="912c8-151">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="912c8-152">新-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="912c8-152">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="912c8-153">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="912c8-153">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

