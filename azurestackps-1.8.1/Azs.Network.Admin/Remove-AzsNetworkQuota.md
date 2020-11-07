---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94609250696a99a337153e9e0d3a1d092e380c40
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793963"
---
# <span data-ttu-id="20e54-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="20e54-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="20e54-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20e54-102">SYNOPSIS</span></span>
<span data-ttu-id="20e54-103">依名稱刪除配額。</span><span class="sxs-lookup"><span data-stu-id="20e54-103">Delete a quota by name.</span></span>

## <span data-ttu-id="20e54-104">句法</span><span class="sxs-lookup"><span data-stu-id="20e54-104">SYNTAX</span></span>

### <span data-ttu-id="20e54-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="20e54-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20e54-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="20e54-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20e54-107">說明</span><span class="sxs-lookup"><span data-stu-id="20e54-107">DESCRIPTION</span></span>
<span data-ttu-id="20e54-108">依名稱刪除配額。</span><span class="sxs-lookup"><span data-stu-id="20e54-108">Delete a quota by name.</span></span>

## <span data-ttu-id="20e54-109">示例</span><span class="sxs-lookup"><span data-stu-id="20e54-109">EXAMPLES</span></span>

### <span data-ttu-id="20e54-110">範例1</span><span class="sxs-lookup"><span data-stu-id="20e54-110">EXAMPLE 1</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="20e54-111">依名稱移除網路配額。</span><span class="sxs-lookup"><span data-stu-id="20e54-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="20e54-112">範例2</span><span class="sxs-lookup"><span data-stu-id="20e54-112">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="20e54-113">使用管道移除網路配額。</span><span class="sxs-lookup"><span data-stu-id="20e54-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="20e54-114">範例3</span><span class="sxs-lookup"><span data-stu-id="20e54-114">EXAMPLE 3</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="20e54-115">移除網路配額。</span><span class="sxs-lookup"><span data-stu-id="20e54-115">Remove a network quota.</span></span>

## <span data-ttu-id="20e54-116">參數</span><span class="sxs-lookup"><span data-stu-id="20e54-116">PARAMETERS</span></span>

### <span data-ttu-id="20e54-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="20e54-117">-Name</span></span>
<span data-ttu-id="20e54-118">資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="20e54-118">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20e54-119">-位置</span><span class="sxs-lookup"><span data-stu-id="20e54-119">-Location</span></span>
<span data-ttu-id="20e54-120">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="20e54-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20e54-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20e54-121">-ResourceId</span></span>
<span data-ttu-id="20e54-122">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="20e54-122">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20e54-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20e54-123">-AsJob</span></span>
<span data-ttu-id="20e54-124">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="20e54-124">Run asynchronous as a job and return the job object.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20e54-125">-Force</span><span class="sxs-lookup"><span data-stu-id="20e54-125">-Force</span></span>
<span data-ttu-id="20e54-126">不要求確認的切換參數。</span><span class="sxs-lookup"><span data-stu-id="20e54-126">Switch parameter for not asking confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20e54-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20e54-127">-WhatIf</span></span>
<span data-ttu-id="20e54-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="20e54-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20e54-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="20e54-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20e54-130">-確認</span><span class="sxs-lookup"><span data-stu-id="20e54-130">-Confirm</span></span>
<span data-ttu-id="20e54-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="20e54-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20e54-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20e54-132">CommonParameters</span></span>
<span data-ttu-id="20e54-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20e54-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20e54-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="20e54-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20e54-135">輸入</span><span class="sxs-lookup"><span data-stu-id="20e54-135">INPUTS</span></span>

## <span data-ttu-id="20e54-136">輸出</span><span class="sxs-lookup"><span data-stu-id="20e54-136">OUTPUTS</span></span>

## <span data-ttu-id="20e54-137">筆記</span><span class="sxs-lookup"><span data-stu-id="20e54-137">NOTES</span></span>

## <span data-ttu-id="20e54-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="20e54-138">RELATED LINKS</span></span>