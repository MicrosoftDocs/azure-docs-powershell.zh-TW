---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 15023fbbb0576f99f66519198c893080ebe1c92f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621407"
---
# <span data-ttu-id="bc5fe-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bc5fe-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="bc5fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc5fe-102">SYNOPSIS</span></span>
<span data-ttu-id="bc5fe-103">配置虛擬網路閘道連線。</span><span class="sxs-lookup"><span data-stu-id="bc5fe-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="bc5fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc5fe-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc5fe-105">說明</span><span class="sxs-lookup"><span data-stu-id="bc5fe-105">DESCRIPTION</span></span>
<span data-ttu-id="bc5fe-106">AzVirtualNetworkGatewayConnection Cmdlet 會 **設定** 虛擬網路閘道連線。</span><span class="sxs-lookup"><span data-stu-id="bc5fe-106">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="bc5fe-107">示例</span><span class="sxs-lookup"><span data-stu-id="bc5fe-107">EXAMPLES</span></span>

### <span data-ttu-id="bc5fe-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="bc5fe-108">Example 1:</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

## <span data-ttu-id="bc5fe-109">參數</span><span class="sxs-lookup"><span data-stu-id="bc5fe-109">PARAMETERS</span></span>

### <span data-ttu-id="bc5fe-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc5fe-110">-AsJob</span></span>
<span data-ttu-id="bc5fe-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bc5fe-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc5fe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc5fe-112">-DefaultProfile</span></span>
<span data-ttu-id="bc5fe-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc5fe-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc5fe-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="bc5fe-114">-EnableBgp</span></span>
<span data-ttu-id="bc5fe-115">是否要在 S2S VPN 隧道上使用 BGP 會話</span><span class="sxs-lookup"><span data-stu-id="bc5fe-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc5fe-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bc5fe-116">-Force</span></span>
<span data-ttu-id="bc5fe-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="bc5fe-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bc5fe-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="bc5fe-118">-IpsecPolicies</span></span>
<span data-ttu-id="bc5fe-119">IPSec 原則清單。</span><span class="sxs-lookup"><span data-stu-id="bc5fe-119">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc5fe-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="bc5fe-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="bc5fe-121">是否要針對 S2S 連線使用原則流量選擇器</span><span class="sxs-lookup"><span data-stu-id="bc5fe-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5fe-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bc5fe-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="bc5fe-123">指定此 Cmdlet 用來修改虛擬網路閘道連線的 PSVirtualNetworkGatewayConnection 物件。</span><span class="sxs-lookup"><span data-stu-id="bc5fe-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc5fe-124">-確認</span><span class="sxs-lookup"><span data-stu-id="bc5fe-124">-Confirm</span></span>
<span data-ttu-id="bc5fe-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bc5fe-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5fe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc5fe-126">-WhatIf</span></span>
<span data-ttu-id="bc5fe-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bc5fe-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc5fe-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bc5fe-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5fe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc5fe-129">CommonParameters</span></span>
<span data-ttu-id="bc5fe-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc5fe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc5fe-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bc5fe-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc5fe-132">輸入</span><span class="sxs-lookup"><span data-stu-id="bc5fe-132">INPUTS</span></span>

### <span data-ttu-id="bc5fe-133">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bc5fe-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="bc5fe-134">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bc5fe-134">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bc5fe-135">PSIpsecPolicy [] （[]）</span><span class="sxs-lookup"><span data-stu-id="bc5fe-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="bc5fe-136">輸出</span><span class="sxs-lookup"><span data-stu-id="bc5fe-136">OUTPUTS</span></span>

### <span data-ttu-id="bc5fe-137">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bc5fe-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="bc5fe-138">筆記</span><span class="sxs-lookup"><span data-stu-id="bc5fe-138">NOTES</span></span>

## <span data-ttu-id="bc5fe-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc5fe-139">RELATED LINKS</span></span>

[<span data-ttu-id="bc5fe-140">AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bc5fe-140">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="bc5fe-141">新-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bc5fe-141">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="bc5fe-142">移除-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bc5fe-142">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

