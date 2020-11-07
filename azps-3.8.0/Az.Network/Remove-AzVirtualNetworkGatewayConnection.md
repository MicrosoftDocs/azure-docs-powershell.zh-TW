---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 78ba1323532faa825e80e456f5ae6544eef3c7de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959908"
---
# <span data-ttu-id="dbc02-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dbc02-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="dbc02-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dbc02-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc02-103">刪除虛擬網路閘道連線</span><span class="sxs-lookup"><span data-stu-id="dbc02-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="dbc02-104">句法</span><span class="sxs-lookup"><span data-stu-id="dbc02-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbc02-105">說明</span><span class="sxs-lookup"><span data-stu-id="dbc02-105">DESCRIPTION</span></span>
<span data-ttu-id="dbc02-106">虛擬網路閘道連線是代表連接至 Azure 中虛擬網路閘道的 IPsec 隧道 (點對點或 Vnet 到 Vnet) 的物件。</span><span class="sxs-lookup"><span data-stu-id="dbc02-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="dbc02-107">**AzVirtualNetworkGatewayConnection** Cmdlet 會根據名稱和資源組名稱來刪除連線物件。</span><span class="sxs-lookup"><span data-stu-id="dbc02-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="dbc02-108">示例</span><span class="sxs-lookup"><span data-stu-id="dbc02-108">EXAMPLES</span></span>

### <span data-ttu-id="dbc02-109">1：刪除虛擬網路閘道連線</span><span class="sxs-lookup"><span data-stu-id="dbc02-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="dbc02-110">刪除資源群組 "myRG" 中名稱為 "myTunnel" 的虛擬網路閘道連線物件</span><span class="sxs-lookup"><span data-stu-id="dbc02-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="dbc02-111">參數</span><span class="sxs-lookup"><span data-stu-id="dbc02-111">PARAMETERS</span></span>

### <span data-ttu-id="dbc02-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc02-112">-DefaultProfile</span></span>
<span data-ttu-id="dbc02-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbc02-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbc02-114">-Force</span><span class="sxs-lookup"><span data-stu-id="dbc02-114">-Force</span></span>
<span data-ttu-id="dbc02-115">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="dbc02-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dbc02-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="dbc02-116">-Name</span></span>
<span data-ttu-id="dbc02-117">指定此 Cmdlet 移除的虛擬網路閘道連線名稱。</span><span class="sxs-lookup"><span data-stu-id="dbc02-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbc02-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbc02-118">-PassThru</span></span>
<span data-ttu-id="dbc02-119">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="dbc02-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dbc02-120">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="dbc02-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dbc02-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbc02-121">-ResourceGroupName</span></span>
<span data-ttu-id="dbc02-122">指定包含虛擬網路閘道連線之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbc02-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="dbc02-123">-確認</span><span class="sxs-lookup"><span data-stu-id="dbc02-123">-Confirm</span></span>
<span data-ttu-id="dbc02-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dbc02-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbc02-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbc02-125">-WhatIf</span></span>
<span data-ttu-id="dbc02-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dbc02-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbc02-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dbc02-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbc02-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc02-128">CommonParameters</span></span>
<span data-ttu-id="dbc02-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dbc02-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc02-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dbc02-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc02-131">輸入</span><span class="sxs-lookup"><span data-stu-id="dbc02-131">INPUTS</span></span>

### <span data-ttu-id="dbc02-132">System.object</span><span class="sxs-lookup"><span data-stu-id="dbc02-132">System.String</span></span>

## <span data-ttu-id="dbc02-133">輸出</span><span class="sxs-lookup"><span data-stu-id="dbc02-133">OUTPUTS</span></span>

### <span data-ttu-id="dbc02-134">System.object</span><span class="sxs-lookup"><span data-stu-id="dbc02-134">System.Boolean</span></span>

## <span data-ttu-id="dbc02-135">筆記</span><span class="sxs-lookup"><span data-stu-id="dbc02-135">NOTES</span></span>

## <span data-ttu-id="dbc02-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbc02-136">RELATED LINKS</span></span>

[<span data-ttu-id="dbc02-137">AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dbc02-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="dbc02-138">新-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dbc02-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="dbc02-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dbc02-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)