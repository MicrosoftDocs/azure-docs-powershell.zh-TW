---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797106"
---
# <span data-ttu-id="7d20b-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7d20b-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="7d20b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d20b-102">SYNOPSIS</span></span> 
<span data-ttu-id="7d20b-103">在已連接的 vpn 用戶端連線中，斷開與指定的虛擬閘道的連接。</span><span class="sxs-lookup"><span data-stu-id="7d20b-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="7d20b-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d20b-104">SYNTAX</span></span>
### <span data-ttu-id="7d20b-105">ByVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="7d20b-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="7d20b-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7d20b-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="7d20b-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7d20b-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="7d20b-108">說明</span><span class="sxs-lookup"><span data-stu-id="7d20b-108">DESCRIPTION</span></span>
<span data-ttu-id="7d20b-109">**AzVirtualNetworkGatewayVpnConnection** Cmdlet 可讓您中斷已連接之 vpn 用戶端連線的連接。</span><span class="sxs-lookup"><span data-stu-id="7d20b-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="7d20b-110">示例</span><span class="sxs-lookup"><span data-stu-id="7d20b-110">EXAMPLES</span></span>

### <span data-ttu-id="7d20b-111">範例</span><span class="sxs-lookup"><span data-stu-id="7d20b-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="7d20b-112">參數</span><span class="sxs-lookup"><span data-stu-id="7d20b-112">PARAMETERS</span></span>

### <span data-ttu-id="7d20b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d20b-113">-ResourceGroupName</span></span>
<span data-ttu-id="7d20b-114">虛擬網路閘道資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="7d20b-114">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d20b-115">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="7d20b-115">-ResourceName</span></span>
<span data-ttu-id="7d20b-116">虛擬網路閘道名稱</span><span class="sxs-lookup"><span data-stu-id="7d20b-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d20b-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d20b-117">-ResourceId</span></span>
<span data-ttu-id="7d20b-118">虛擬網路閘道資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7d20b-118">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d20b-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="7d20b-119">-VpnConnectionId</span></span>
<span data-ttu-id="7d20b-120">Vpn 連線識別碼</span><span class="sxs-lookup"><span data-stu-id="7d20b-120">Vpn Connection Ids</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d20b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d20b-121">-InputObject</span></span>
<span data-ttu-id="7d20b-122">虛擬網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="7d20b-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d20b-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d20b-123">-AsJob</span></span>
<span data-ttu-id="7d20b-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7d20b-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d20b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d20b-125">CommonParameters</span></span>
<span data-ttu-id="7d20b-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d20b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d20b-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7d20b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d20b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="7d20b-128">INPUTS</span></span>

### <span data-ttu-id="7d20b-129">System.object</span><span class="sxs-lookup"><span data-stu-id="7d20b-129">System.String</span></span>

## <span data-ttu-id="7d20b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="7d20b-130">OUTPUTS</span></span>

### <span data-ttu-id="7d20b-131">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7d20b-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7d20b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="7d20b-132">NOTES</span></span>

## <span data-ttu-id="7d20b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d20b-133">RELATED LINKS</span></span>