---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: 4c93528c8cf89d64dd99640ce9eca4668d4093c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275144"
---
# <span data-ttu-id="7c734-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7c734-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="7c734-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c734-102">SYNOPSIS</span></span>
<span data-ttu-id="7c734-103">從 ExpressRoute 交叉連接取得路由表。</span><span class="sxs-lookup"><span data-stu-id="7c734-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="7c734-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c734-104">SYNTAX</span></span>

### <span data-ttu-id="7c734-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="7c734-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c734-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="7c734-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c734-107">說明</span><span class="sxs-lookup"><span data-stu-id="7c734-107">DESCRIPTION</span></span>
<span data-ttu-id="7c734-108">**AzExpressRouteCrossConnectionRouteTable** Cmdlet 會檢索 ExpressRoute 回路的詳細路由表。</span><span class="sxs-lookup"><span data-stu-id="7c734-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="7c734-109">[路由] 表格會顯示所有路由，或可以篩選，以顯示特定對等類型的路線。</span><span class="sxs-lookup"><span data-stu-id="7c734-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="7c734-110">您可以使用路由表來驗證對等設定和連線性。</span><span class="sxs-lookup"><span data-stu-id="7c734-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="7c734-111">示例</span><span class="sxs-lookup"><span data-stu-id="7c734-111">EXAMPLES</span></span>

### <span data-ttu-id="7c734-112">範例1：顯示主要路徑的路由資料表</span><span class="sxs-lookup"><span data-stu-id="7c734-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="7c734-113">參數</span><span class="sxs-lookup"><span data-stu-id="7c734-113">PARAMETERS</span></span>

### <span data-ttu-id="7c734-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="7c734-114">-CrossConnectionName</span></span>
<span data-ttu-id="7c734-115">快速路由的名稱交叉連接</span><span class="sxs-lookup"><span data-stu-id="7c734-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c734-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c734-116">-DefaultProfile</span></span>
<span data-ttu-id="7c734-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c734-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c734-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="7c734-118">-DevicePath</span></span>
<span data-ttu-id="7c734-119">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="7c734-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c734-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7c734-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="7c734-121">快速路由的交叉連接</span><span class="sxs-lookup"><span data-stu-id="7c734-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c734-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="7c734-122">-PeeringType</span></span>
<span data-ttu-id="7c734-123">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="7c734-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c734-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c734-124">-ResourceGroupName</span></span>
<span data-ttu-id="7c734-125">包含 ExpressRoute 交叉連線的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c734-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c734-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c734-126">CommonParameters</span></span>
<span data-ttu-id="7c734-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c734-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c734-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7c734-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c734-129">輸入</span><span class="sxs-lookup"><span data-stu-id="7c734-129">INPUTS</span></span>

### <span data-ttu-id="7c734-130">所有</span><span class="sxs-lookup"><span data-stu-id="7c734-130">None</span></span>
<span data-ttu-id="7c734-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="7c734-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7c734-132">輸出</span><span class="sxs-lookup"><span data-stu-id="7c734-132">OUTPUTS</span></span>

### <span data-ttu-id="7c734-133">PSExpressRouteCircuitRoutesTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7c734-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="7c734-134">筆記</span><span class="sxs-lookup"><span data-stu-id="7c734-134">NOTES</span></span>

## <span data-ttu-id="7c734-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c734-135">RELATED LINKS</span></span>

[<span data-ttu-id="7c734-136">AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="7c734-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="7c734-137">AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7c734-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)