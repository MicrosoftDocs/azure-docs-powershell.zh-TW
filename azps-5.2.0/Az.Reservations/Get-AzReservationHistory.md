---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cfc7ab08904f007f874e1b45fd6d27a5712abee9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284339"
---
# <span data-ttu-id="9a60d-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="9a60d-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="9a60d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a60d-102">SYNOPSIS</span></span>
<span data-ttu-id="9a60d-103">取得 `Reservation` 修訂歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="9a60d-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="9a60d-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a60d-104">SYNTAX</span></span>

### <span data-ttu-id="9a60d-105">[命令列 (預設) </span><span class="sxs-lookup"><span data-stu-id="9a60d-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a60d-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="9a60d-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a60d-107">說明</span><span class="sxs-lookup"><span data-stu-id="9a60d-107">DESCRIPTION</span></span>
<span data-ttu-id="9a60d-108">所有修訂版本的清單 `Reservation` 。</span><span class="sxs-lookup"><span data-stu-id="9a60d-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="9a60d-109">示例</span><span class="sxs-lookup"><span data-stu-id="9a60d-109">EXAMPLES</span></span>

### <span data-ttu-id="9a60d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="9a60d-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="9a60d-111">取得特定保留的修訂歷程記錄</span><span class="sxs-lookup"><span data-stu-id="9a60d-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="9a60d-112">參數</span><span class="sxs-lookup"><span data-stu-id="9a60d-112">PARAMETERS</span></span>

### <span data-ttu-id="9a60d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a60d-113">-DefaultProfile</span></span>
<span data-ttu-id="9a60d-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a60d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a60d-115">預留</span><span class="sxs-lookup"><span data-stu-id="9a60d-115">-Reservation</span></span>
<span data-ttu-id="9a60d-116">S 的管道物件參數 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="9a60d-116">Pipe object parameter for `Reservation`s</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a60d-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="9a60d-117">-ReservationId</span></span>
<span data-ttu-id="9a60d-118">`Reservation`要顯示其記錄的 ReservationId</span><span class="sxs-lookup"><span data-stu-id="9a60d-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a60d-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="9a60d-119">-ReservationOrderId</span></span>
<span data-ttu-id="9a60d-120">ReservationOrderId `ReservationOrder` 包含 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="9a60d-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a60d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a60d-121">CommonParameters</span></span>
<span data-ttu-id="9a60d-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a60d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a60d-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9a60d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a60d-124">輸入</span><span class="sxs-lookup"><span data-stu-id="9a60d-124">INPUTS</span></span>

### <span data-ttu-id="9a60d-125">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="9a60d-125">System.Guid</span></span>

### <span data-ttu-id="9a60d-126">PSReservation 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="9a60d-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="9a60d-127">輸出</span><span class="sxs-lookup"><span data-stu-id="9a60d-127">OUTPUTS</span></span>

### <span data-ttu-id="9a60d-128">PSReservationPage 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="9a60d-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="9a60d-129">筆記</span><span class="sxs-lookup"><span data-stu-id="9a60d-129">NOTES</span></span>

## <span data-ttu-id="9a60d-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a60d-130">RELATED LINKS</span></span>