---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 6f1eb79b7c740cae437e28af8153a4c14532871e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287292"
---
# <span data-ttu-id="8d4d9-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="8d4d9-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="8d4d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d4d9-102">SYNOPSIS</span></span>
<span data-ttu-id="8d4d9-103">取得可用保留的目錄</span><span class="sxs-lookup"><span data-stu-id="8d4d9-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="8d4d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d4d9-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d4d9-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d4d9-105">DESCRIPTION</span></span>
<span data-ttu-id="8d4d9-106">取得適用于指定 Azure 訂閱之保留實例購買的地區和 sku。</span><span class="sxs-lookup"><span data-stu-id="8d4d9-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="8d4d9-107">示例</span><span class="sxs-lookup"><span data-stu-id="8d4d9-107">EXAMPLES</span></span>

### <span data-ttu-id="8d4d9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8d4d9-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="8d4d9-109">在 westus 中取得預設訂閱的 VirtualMachines 目錄</span><span class="sxs-lookup"><span data-stu-id="8d4d9-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="8d4d9-110">範例2</span><span class="sxs-lookup"><span data-stu-id="8d4d9-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="8d4d9-111">取得指定訂閱的 SuseLinux 目錄</span><span class="sxs-lookup"><span data-stu-id="8d4d9-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="8d4d9-112">參數</span><span class="sxs-lookup"><span data-stu-id="8d4d9-112">PARAMETERS</span></span>

### <span data-ttu-id="8d4d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d4d9-113">-DefaultProfile</span></span>
<span data-ttu-id="8d4d9-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d4d9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d4d9-115">-位置</span><span class="sxs-lookup"><span data-stu-id="8d4d9-115">-Location</span></span>
<span data-ttu-id="8d4d9-116">指定保留資源在目錄中的位置</span><span class="sxs-lookup"><span data-stu-id="8d4d9-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="8d4d9-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="8d4d9-117">-ReservedResourceType</span></span>
<span data-ttu-id="8d4d9-118">指定目錄中保留資源的類型</span><span class="sxs-lookup"><span data-stu-id="8d4d9-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="8d4d9-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d4d9-119">-SubscriptionId</span></span>
<span data-ttu-id="8d4d9-120">訂閱的識別碼</span><span class="sxs-lookup"><span data-stu-id="8d4d9-120">Id of the subscription</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d4d9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d4d9-121">CommonParameters</span></span>
<span data-ttu-id="8d4d9-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d4d9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d4d9-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d4d9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d4d9-124">輸入</span><span class="sxs-lookup"><span data-stu-id="8d4d9-124">INPUTS</span></span>

### <span data-ttu-id="8d4d9-125">所有</span><span class="sxs-lookup"><span data-stu-id="8d4d9-125">None</span></span>

## <span data-ttu-id="8d4d9-126">輸出</span><span class="sxs-lookup"><span data-stu-id="8d4d9-126">OUTPUTS</span></span>

### <span data-ttu-id="8d4d9-127">PSCatalog 中的 [命令]。</span><span class="sxs-lookup"><span data-stu-id="8d4d9-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="8d4d9-128">筆記</span><span class="sxs-lookup"><span data-stu-id="8d4d9-128">NOTES</span></span>

## <span data-ttu-id="8d4d9-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d4d9-129">RELATED LINKS</span></span>