---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: fd01dea04043d8d68009f89823fe34f3695a6d47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274700"
---
# <span data-ttu-id="ede9c-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="ede9c-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="ede9c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ede9c-102">SYNOPSIS</span></span>
<span data-ttu-id="ede9c-103">移除 HPC 快取。</span><span class="sxs-lookup"><span data-stu-id="ede9c-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="ede9c-104">句法</span><span class="sxs-lookup"><span data-stu-id="ede9c-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ede9c-105">說明</span><span class="sxs-lookup"><span data-stu-id="ede9c-105">DESCRIPTION</span></span>
<span data-ttu-id="ede9c-106">**AzHpcCache** Cmdlet 會移除 Azure HPC 緩存。</span><span class="sxs-lookup"><span data-stu-id="ede9c-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="ede9c-107">示例</span><span class="sxs-lookup"><span data-stu-id="ede9c-107">EXAMPLES</span></span>

### <span data-ttu-id="ede9c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ede9c-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="ede9c-109">參數</span><span class="sxs-lookup"><span data-stu-id="ede9c-109">PARAMETERS</span></span>

### <span data-ttu-id="ede9c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ede9c-110">-AsJob</span></span>
<span data-ttu-id="ede9c-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ede9c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ede9c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ede9c-112">-DefaultProfile</span></span>
<span data-ttu-id="ede9c-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ede9c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ede9c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ede9c-114">-Force</span></span>
<span data-ttu-id="ede9c-115">表示 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ede9c-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="ede9c-116">根據預設，這個 Cmdlet 會提示您確認要移除快取。</span><span class="sxs-lookup"><span data-stu-id="ede9c-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="ede9c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ede9c-117">-Name</span></span>
<span data-ttu-id="ede9c-118">快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="ede9c-118">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ede9c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ede9c-119">-PassThru</span></span>
<span data-ttu-id="ede9c-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ede9c-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ede9c-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ede9c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ede9c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ede9c-122">-ResourceGroupName</span></span>
<span data-ttu-id="ede9c-123">您要在其上移除快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ede9c-123">Name of resource group under which you want to remove cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ede9c-124">-確認</span><span class="sxs-lookup"><span data-stu-id="ede9c-124">-Confirm</span></span>
<span data-ttu-id="ede9c-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ede9c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ede9c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ede9c-126">-WhatIf</span></span>
<span data-ttu-id="ede9c-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ede9c-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ede9c-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ede9c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ede9c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ede9c-129">CommonParameters</span></span>
<span data-ttu-id="ede9c-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ede9c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ede9c-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ede9c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ede9c-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ede9c-132">INPUTS</span></span>

### <span data-ttu-id="ede9c-133">System.object</span><span class="sxs-lookup"><span data-stu-id="ede9c-133">System.String</span></span>

## <span data-ttu-id="ede9c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ede9c-134">OUTPUTS</span></span>

## <span data-ttu-id="ede9c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ede9c-135">NOTES</span></span>

## <span data-ttu-id="ede9c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ede9c-136">RELATED LINKS</span></span>