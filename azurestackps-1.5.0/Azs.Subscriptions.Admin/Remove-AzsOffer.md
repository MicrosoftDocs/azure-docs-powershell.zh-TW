---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2ac9f85896c1ae0a8eb7e060600ba5b4eb0e792
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623199"
---
# <span data-ttu-id="357bb-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="357bb-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="357bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="357bb-102">SYNOPSIS</span></span>
<span data-ttu-id="357bb-103">刪除指定的優惠。</span><span class="sxs-lookup"><span data-stu-id="357bb-103">Delete the specified offer.</span></span>

## <span data-ttu-id="357bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="357bb-104">SYNTAX</span></span>

### <span data-ttu-id="357bb-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="357bb-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="357bb-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="357bb-106">ResourceId</span></span>
```
Remove-AzsOffer -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="357bb-107">說明</span><span class="sxs-lookup"><span data-stu-id="357bb-107">DESCRIPTION</span></span>
<span data-ttu-id="357bb-108">刪除指定的優惠。</span><span class="sxs-lookup"><span data-stu-id="357bb-108">Delete the specified offer.</span></span>

## <span data-ttu-id="357bb-109">示例</span><span class="sxs-lookup"><span data-stu-id="357bb-109">EXAMPLES</span></span>

### <span data-ttu-id="357bb-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="357bb-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOffer -Name offername1 -ResourceGroupName rg1
```

<span data-ttu-id="357bb-111">刪除指定的優惠。</span><span class="sxs-lookup"><span data-stu-id="357bb-111">Delete the specified offer.</span></span>

## <span data-ttu-id="357bb-112">參數</span><span class="sxs-lookup"><span data-stu-id="357bb-112">PARAMETERS</span></span>

### <span data-ttu-id="357bb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="357bb-113">-Force</span></span>
<span data-ttu-id="357bb-114">[標誌] 可移除專案而不需確認。</span><span class="sxs-lookup"><span data-stu-id="357bb-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="357bb-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="357bb-115">-Name</span></span>
<span data-ttu-id="357bb-116">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="357bb-116">Name of an offer.</span></span>

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

### <span data-ttu-id="357bb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="357bb-117">-ResourceGroupName</span></span>
<span data-ttu-id="357bb-118">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="357bb-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="357bb-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="357bb-119">-ResourceId</span></span>
<span data-ttu-id="357bb-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="357bb-120">The resource id.</span></span>

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

### <span data-ttu-id="357bb-121">-確認</span><span class="sxs-lookup"><span data-stu-id="357bb-121">-Confirm</span></span>
<span data-ttu-id="357bb-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="357bb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="357bb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="357bb-123">-WhatIf</span></span>
<span data-ttu-id="357bb-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="357bb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="357bb-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="357bb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="357bb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="357bb-126">CommonParameters</span></span>
<span data-ttu-id="357bb-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="357bb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="357bb-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="357bb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="357bb-129">輸入</span><span class="sxs-lookup"><span data-stu-id="357bb-129">INPUTS</span></span>

## <span data-ttu-id="357bb-130">輸出</span><span class="sxs-lookup"><span data-stu-id="357bb-130">OUTPUTS</span></span>

## <span data-ttu-id="357bb-131">筆記</span><span class="sxs-lookup"><span data-stu-id="357bb-131">NOTES</span></span>

## <span data-ttu-id="357bb-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="357bb-132">RELATED LINKS</span></span>
