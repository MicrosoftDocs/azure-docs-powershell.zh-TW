---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 494995a97ccb74df9ad9a9fc1f88272505598bb9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286068"
---
# <span data-ttu-id="75265-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="75265-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="75265-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75265-102">SYNOPSIS</span></span>
<span data-ttu-id="75265-103">從儲存 blob 容器中移除合法保留標籤</span><span class="sxs-lookup"><span data-stu-id="75265-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="75265-104">句法</span><span class="sxs-lookup"><span data-stu-id="75265-104">SYNTAX</span></span>

### <span data-ttu-id="75265-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="75265-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75265-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="75265-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75265-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="75265-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75265-108">說明</span><span class="sxs-lookup"><span data-stu-id="75265-108">DESCRIPTION</span></span>
<span data-ttu-id="75265-109">**AzRmStorageContainerLegalHold** Cmdlet 會從儲存 blob 容器中移除合法保留標籤</span><span class="sxs-lookup"><span data-stu-id="75265-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="75265-110">示例</span><span class="sxs-lookup"><span data-stu-id="75265-110">EXAMPLES</span></span>

### <span data-ttu-id="75265-111">範例1：從含儲存空間帳戶名稱和容器名稱的儲存 blob 容器中移除合法保留標記</span><span class="sxs-lookup"><span data-stu-id="75265-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="75265-112">這個命令會從儲存區名稱和容器名稱中移除儲存 blob 容器中的合法保留標籤。</span><span class="sxs-lookup"><span data-stu-id="75265-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="75265-113">範例2：從含儲存空間帳戶物件和容器名稱的儲存 blob 容器中移除合法保留標記</span><span class="sxs-lookup"><span data-stu-id="75265-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="75265-114">這個命令會從含儲存空間帳戶物件和容器名稱的儲存 blob 容器中移除合法保留標籤。</span><span class="sxs-lookup"><span data-stu-id="75265-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="75265-115">範例3：從含管線的儲存空間帳戶中的所有儲存區 blob 容器移除合法保留標籤</span><span class="sxs-lookup"><span data-stu-id="75265-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="75265-116">這個命令會從含管線的儲存空間帳戶中的所有儲存區 blob 容器中移除合法保留標籤。</span><span class="sxs-lookup"><span data-stu-id="75265-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="75265-117">參數</span><span class="sxs-lookup"><span data-stu-id="75265-117">PARAMETERS</span></span>

### <span data-ttu-id="75265-118">-容器</span><span class="sxs-lookup"><span data-stu-id="75265-118">-Container</span></span>
<span data-ttu-id="75265-119">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="75265-119">Storage container object</span></span>

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

### <span data-ttu-id="75265-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75265-120">-DefaultProfile</span></span>
<span data-ttu-id="75265-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="75265-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75265-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="75265-122">-Name</span></span>
<span data-ttu-id="75265-123">容器名稱</span><span class="sxs-lookup"><span data-stu-id="75265-123">Container Name</span></span>

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

### <span data-ttu-id="75265-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75265-124">-ResourceGroupName</span></span>
<span data-ttu-id="75265-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="75265-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="75265-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="75265-126">-StorageAccount</span></span>
<span data-ttu-id="75265-127">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="75265-127">Storage account object</span></span>

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

### <span data-ttu-id="75265-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="75265-128">-StorageAccountName</span></span>
<span data-ttu-id="75265-129">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="75265-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="75265-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="75265-130">-Tag</span></span>
<span data-ttu-id="75265-131">容器 LegalHold 標記</span><span class="sxs-lookup"><span data-stu-id="75265-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="75265-132">-確認</span><span class="sxs-lookup"><span data-stu-id="75265-132">-Confirm</span></span>
<span data-ttu-id="75265-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="75265-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75265-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75265-134">-WhatIf</span></span>
<span data-ttu-id="75265-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="75265-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75265-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="75265-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75265-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75265-137">CommonParameters</span></span>
<span data-ttu-id="75265-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75265-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75265-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="75265-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75265-140">輸入</span><span class="sxs-lookup"><span data-stu-id="75265-140">INPUTS</span></span>

### <span data-ttu-id="75265-141">System.object</span><span class="sxs-lookup"><span data-stu-id="75265-141">System.String</span></span>

### <span data-ttu-id="75265-142">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="75265-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="75265-143">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="75265-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="75265-144">輸出</span><span class="sxs-lookup"><span data-stu-id="75265-144">OUTPUTS</span></span>

### <span data-ttu-id="75265-145">PSLegalHold 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="75265-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="75265-146">筆記</span><span class="sxs-lookup"><span data-stu-id="75265-146">NOTES</span></span>

## <span data-ttu-id="75265-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="75265-147">RELATED LINKS</span></span>