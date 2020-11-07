---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 13fc089db38bb9aa525285c61b1a2d4fecd934b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792893"
---
# <span data-ttu-id="6bea1-101">Add-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="6bea1-101">Add-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="6bea1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6bea1-102">SYNOPSIS</span></span>
<span data-ttu-id="6bea1-103">將法定保留標籤新增至儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="6bea1-103">Adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="6bea1-104">句法</span><span class="sxs-lookup"><span data-stu-id="6bea1-104">SYNTAX</span></span>

### <span data-ttu-id="6bea1-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="6bea1-105">AccountName (Default)</span></span>
```
Add-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bea1-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6bea1-106">AccountObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bea1-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="6bea1-107">ContainerObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bea1-108">說明</span><span class="sxs-lookup"><span data-stu-id="6bea1-108">DESCRIPTION</span></span>
<span data-ttu-id="6bea1-109">**AzRmStorageContainerLegalHold** Cmdlet 會將法定保留標籤新增至儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="6bea1-109">The **Add-AzRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="6bea1-110">示例</span><span class="sxs-lookup"><span data-stu-id="6bea1-110">EXAMPLES</span></span>

### <span data-ttu-id="6bea1-111">範例1：使用儲存空間帳戶名稱和容器名稱，將法律保留標籤新增至儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="6bea1-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2
```

<span data-ttu-id="6bea1-112">這個命令會將合法保留標籤新增至儲存區名稱和容器名稱的儲存區 blob 容器中。</span><span class="sxs-lookup"><span data-stu-id="6bea1-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="6bea1-113">範例2：使用儲存帳戶物件和容器名稱，將法律保留標籤新增至儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="6bea1-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="6bea1-114">這個命令會將合法保留標籤新增至儲存區中的 [存儲帳戶] 物件和容器名稱。</span><span class="sxs-lookup"><span data-stu-id="6bea1-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="6bea1-115">範例3：在含有管線的儲存空間帳戶中，將法定保留標籤新增至所有儲存區 blob 容器</span><span class="sxs-lookup"><span data-stu-id="6bea1-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="6bea1-116">這個命令會在含有管線的儲存空間帳戶中，新增法律保留標籤至所有儲存區 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="6bea1-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="6bea1-117">參數</span><span class="sxs-lookup"><span data-stu-id="6bea1-117">PARAMETERS</span></span>

### <span data-ttu-id="6bea1-118">-容器</span><span class="sxs-lookup"><span data-stu-id="6bea1-118">-Container</span></span>
<span data-ttu-id="6bea1-119">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="6bea1-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bea1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bea1-120">-DefaultProfile</span></span>
<span data-ttu-id="6bea1-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6bea1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bea1-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="6bea1-122">-Name</span></span>
<span data-ttu-id="6bea1-123">容器名稱</span><span class="sxs-lookup"><span data-stu-id="6bea1-123">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bea1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bea1-124">-ResourceGroupName</span></span>
<span data-ttu-id="6bea1-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6bea1-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bea1-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6bea1-126">-StorageAccount</span></span>
<span data-ttu-id="6bea1-127">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="6bea1-127">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bea1-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6bea1-128">-StorageAccountName</span></span>
<span data-ttu-id="6bea1-129">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6bea1-129">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bea1-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="6bea1-130">-Tag</span></span>
<span data-ttu-id="6bea1-131">容器 LegalHold 標記</span><span class="sxs-lookup"><span data-stu-id="6bea1-131">Container LegalHold Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bea1-132">-確認</span><span class="sxs-lookup"><span data-stu-id="6bea1-132">-Confirm</span></span>
<span data-ttu-id="6bea1-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6bea1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bea1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bea1-134">-WhatIf</span></span>
<span data-ttu-id="6bea1-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6bea1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bea1-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6bea1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bea1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bea1-137">CommonParameters</span></span>
<span data-ttu-id="6bea1-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6bea1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bea1-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6bea1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bea1-140">輸入</span><span class="sxs-lookup"><span data-stu-id="6bea1-140">INPUTS</span></span>

### <span data-ttu-id="6bea1-141">System.object</span><span class="sxs-lookup"><span data-stu-id="6bea1-141">System.String</span></span>

### <span data-ttu-id="6bea1-142">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="6bea1-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="6bea1-143">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="6bea1-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="6bea1-144">輸出</span><span class="sxs-lookup"><span data-stu-id="6bea1-144">OUTPUTS</span></span>

### <span data-ttu-id="6bea1-145">PSLegalHold 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="6bea1-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="6bea1-146">筆記</span><span class="sxs-lookup"><span data-stu-id="6bea1-146">NOTES</span></span>

## <span data-ttu-id="6bea1-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="6bea1-147">RELATED LINKS</span></span>