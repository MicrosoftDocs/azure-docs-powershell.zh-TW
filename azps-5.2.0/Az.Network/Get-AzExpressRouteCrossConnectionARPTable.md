---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
ms.openlocfilehash: 30addde4594c7b67fd5ba9c1358d64ac206a4531
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275152"
---
# <span data-ttu-id="ad444-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ad444-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="ad444-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad444-102">SYNOPSIS</span></span>
<span data-ttu-id="ad444-103">從 ExpressRoute 交叉連接取得 ARP 資料表。</span><span class="sxs-lookup"><span data-stu-id="ad444-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="ad444-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad444-104">SYNTAX</span></span>

### <span data-ttu-id="ad444-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="ad444-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad444-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="ad444-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad444-107">說明</span><span class="sxs-lookup"><span data-stu-id="ad444-107">DESCRIPTION</span></span>
<span data-ttu-id="ad444-108">**AzExpressRouteCrossConnectionARPTable** Cmdlet 會從 ExpressRoute 叉式連接的兩個介面中檢索 ARP 資料表。</span><span class="sxs-lookup"><span data-stu-id="ad444-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="ad444-109">ARP 表格提供特定對等的 IPv4 位址到 MAC 位址的對應。</span><span class="sxs-lookup"><span data-stu-id="ad444-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="ad444-110">您可以使用 ARP 資料表來驗證第2層設定和連線性。</span><span class="sxs-lookup"><span data-stu-id="ad444-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="ad444-111">示例</span><span class="sxs-lookup"><span data-stu-id="ad444-111">EXAMPLES</span></span>

### <span data-ttu-id="ad444-112">範例1：顯示 ExpressRoute 對等的 ARP 資料表</span><span class="sxs-lookup"><span data-stu-id="ad444-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="ad444-113">參數</span><span class="sxs-lookup"><span data-stu-id="ad444-113">PARAMETERS</span></span>

### <span data-ttu-id="ad444-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="ad444-114">-CrossConnectionName</span></span>
<span data-ttu-id="ad444-115">快速路由的名稱交叉連接</span><span class="sxs-lookup"><span data-stu-id="ad444-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="ad444-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad444-116">-DefaultProfile</span></span>
<span data-ttu-id="ad444-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad444-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad444-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="ad444-118">-DevicePath</span></span>
<span data-ttu-id="ad444-119">此參數可接受的值為： `Primary` 或 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="ad444-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="ad444-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ad444-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="ad444-121">快速路由的交叉連接</span><span class="sxs-lookup"><span data-stu-id="ad444-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="ad444-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="ad444-122">-PeeringType</span></span>
<span data-ttu-id="ad444-123">此參數可接受的值為： `AzurePrivatePeering` 、 `AzurePublicPeering` 和 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="ad444-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="ad444-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad444-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad444-125">包含 ExpressRoute 交叉連線的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad444-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="ad444-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad444-126">CommonParameters</span></span>
<span data-ttu-id="ad444-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad444-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad444-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ad444-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad444-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ad444-129">INPUTS</span></span>

### <span data-ttu-id="ad444-130">所有</span><span class="sxs-lookup"><span data-stu-id="ad444-130">None</span></span>
<span data-ttu-id="ad444-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ad444-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad444-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ad444-132">OUTPUTS</span></span>

### <span data-ttu-id="ad444-133">PSExpressRouteCircuitArpTable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ad444-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="ad444-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ad444-134">NOTES</span></span>

## <span data-ttu-id="ad444-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad444-135">RELATED LINKS</span></span>

[<span data-ttu-id="ad444-136">AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ad444-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="ad444-137">AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ad444-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)