---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: fc0b04049184334c59a38226e031342fc29207b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284315"
---
# <span data-ttu-id="c4bfc-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="c4bfc-101">Merge-AzReservation</span></span>

## <span data-ttu-id="c4bfc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="c4bfc-103">合併兩個 `Reservation` s。</span><span class="sxs-lookup"><span data-stu-id="c4bfc-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="c4bfc-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4bfc-104">SYNTAX</span></span>

### <span data-ttu-id="c4bfc-105">[命令列 (預設) </span><span class="sxs-lookup"><span data-stu-id="c4bfc-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4bfc-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="c4bfc-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4bfc-107">說明</span><span class="sxs-lookup"><span data-stu-id="c4bfc-107">DESCRIPTION</span></span>
<span data-ttu-id="c4bfc-108">將指定 `Reservation` 的 s 合併至新的 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="c4bfc-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="c4bfc-109">要合併的兩個 `Reservation` 都必須有相同的屬性。</span><span class="sxs-lookup"><span data-stu-id="c4bfc-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="c4bfc-110">示例</span><span class="sxs-lookup"><span data-stu-id="c4bfc-110">EXAMPLES</span></span>

### <span data-ttu-id="c4bfc-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c4bfc-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="c4bfc-112">將兩個指定的 `Reservation` s 合併成一個 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="c4bfc-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="c4bfc-113">參數</span><span class="sxs-lookup"><span data-stu-id="c4bfc-113">PARAMETERS</span></span>

### <span data-ttu-id="c4bfc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4bfc-114">-DefaultProfile</span></span>
<span data-ttu-id="c4bfc-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4bfc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4bfc-116">預留</span><span class="sxs-lookup"><span data-stu-id="c4bfc-116">-Reservation</span></span>
<span data-ttu-id="c4bfc-117">要合併的兩個 ReservationIds 的逗號分隔字串</span><span class="sxs-lookup"><span data-stu-id="c4bfc-117">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation[]
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4bfc-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="c4bfc-118">-ReservationId</span></span>
<span data-ttu-id="c4bfc-119">`ReservationOrder`包含兩個 s 的 ReservationOrderId `Reservation`</span><span class="sxs-lookup"><span data-stu-id="c4bfc-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4bfc-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="c4bfc-120">-ReservationOrderId</span></span>
<span data-ttu-id="c4bfc-121">{{Fill ReservationOrderId 說明}}</span><span class="sxs-lookup"><span data-stu-id="c4bfc-121">{{Fill ReservationOrderId Description}}</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4bfc-122">-確認</span><span class="sxs-lookup"><span data-stu-id="c4bfc-122">-Confirm</span></span>
<span data-ttu-id="c4bfc-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c4bfc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4bfc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4bfc-124">-WhatIf</span></span>
<span data-ttu-id="c4bfc-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c4bfc-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4bfc-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c4bfc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4bfc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4bfc-127">CommonParameters</span></span>
<span data-ttu-id="c4bfc-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4bfc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4bfc-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c4bfc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4bfc-130">輸入</span><span class="sxs-lookup"><span data-stu-id="c4bfc-130">INPUTS</span></span>

### <span data-ttu-id="c4bfc-131">所有</span><span class="sxs-lookup"><span data-stu-id="c4bfc-131">None</span></span>

## <span data-ttu-id="c4bfc-132">輸出</span><span class="sxs-lookup"><span data-stu-id="c4bfc-132">OUTPUTS</span></span>

### <span data-ttu-id="c4bfc-133">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="c4bfc-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="c4bfc-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c4bfc-134">NOTES</span></span>

## <span data-ttu-id="c4bfc-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4bfc-135">RELATED LINKS</span></span>