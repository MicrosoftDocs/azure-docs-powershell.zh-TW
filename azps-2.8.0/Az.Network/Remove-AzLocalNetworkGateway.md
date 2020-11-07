---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 3f09656caaccb103afa096ca0995489b3768e40e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790641"
---
# <span data-ttu-id="f4a20-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f4a20-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="f4a20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4a20-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a20-103">刪除局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="f4a20-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="f4a20-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4a20-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4a20-105">說明</span><span class="sxs-lookup"><span data-stu-id="f4a20-105">DESCRIPTION</span></span>
<span data-ttu-id="f4a20-106">本機網路閘道是代表您的 VPN 裝置內部部署的物件。</span><span class="sxs-lookup"><span data-stu-id="f4a20-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="f4a20-107">**AzLocalNetworkGateway** Cmdlet 會根據名稱和資源群組名稱，刪除代表您的內部部署閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="f4a20-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="f4a20-108">示例</span><span class="sxs-lookup"><span data-stu-id="f4a20-108">EXAMPLES</span></span>

### <span data-ttu-id="f4a20-109">1：刪除局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="f4a20-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="f4a20-110">在資源群組 "myRG" 中刪除名為 "myLocalGW" 的本機網路閘道物件：您必須先使用 **Remove-AzVirtualNetworkGatewayConnection** Cmdlet 刪除到本機網路閘道的所有連線。</span><span class="sxs-lookup"><span data-stu-id="f4a20-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="f4a20-111">參數</span><span class="sxs-lookup"><span data-stu-id="f4a20-111">PARAMETERS</span></span>

### <span data-ttu-id="f4a20-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4a20-112">-AsJob</span></span>
<span data-ttu-id="f4a20-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f4a20-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4a20-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a20-114">-DefaultProfile</span></span>
<span data-ttu-id="f4a20-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4a20-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4a20-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f4a20-116">-Force</span></span>
<span data-ttu-id="f4a20-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f4a20-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4a20-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4a20-118">-Name</span></span>
<span data-ttu-id="f4a20-119">指定此 Cmdlet 移除之本機網路閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4a20-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f4a20-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4a20-120">-PassThru</span></span>
<span data-ttu-id="f4a20-121">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="f4a20-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f4a20-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f4a20-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f4a20-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4a20-123">-ResourceGroupName</span></span>
<span data-ttu-id="f4a20-124">指定包含局域網閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4a20-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="f4a20-125">-確認</span><span class="sxs-lookup"><span data-stu-id="f4a20-125">-Confirm</span></span>
<span data-ttu-id="f4a20-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f4a20-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4a20-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4a20-127">-WhatIf</span></span>
<span data-ttu-id="f4a20-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4a20-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4a20-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4a20-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4a20-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a20-130">CommonParameters</span></span>
<span data-ttu-id="f4a20-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4a20-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a20-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4a20-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a20-133">輸入</span><span class="sxs-lookup"><span data-stu-id="f4a20-133">INPUTS</span></span>

### <span data-ttu-id="f4a20-134">System.object</span><span class="sxs-lookup"><span data-stu-id="f4a20-134">System.String</span></span>

## <span data-ttu-id="f4a20-135">輸出</span><span class="sxs-lookup"><span data-stu-id="f4a20-135">OUTPUTS</span></span>

### <span data-ttu-id="f4a20-136">System.object</span><span class="sxs-lookup"><span data-stu-id="f4a20-136">System.Boolean</span></span>

## <span data-ttu-id="f4a20-137">筆記</span><span class="sxs-lookup"><span data-stu-id="f4a20-137">NOTES</span></span>

## <span data-ttu-id="f4a20-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4a20-138">RELATED LINKS</span></span>

[<span data-ttu-id="f4a20-139">AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f4a20-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="f4a20-140">新-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f4a20-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="f4a20-141">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f4a20-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)