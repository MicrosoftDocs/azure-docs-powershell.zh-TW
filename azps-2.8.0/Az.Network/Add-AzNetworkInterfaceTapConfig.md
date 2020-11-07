---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: c5c2481244de752a76eb1a1863d1fcc49d93ddb2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790257"
---
# <span data-ttu-id="436ae-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="436ae-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="436ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="436ae-102">SYNOPSIS</span></span>
<span data-ttu-id="436ae-103">建立與 NetworkInterface 相關聯的 TapConfiguration 資源。</span><span class="sxs-lookup"><span data-stu-id="436ae-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="436ae-104">這會參照現有的 VirtualNetworkTap 資源。</span><span class="sxs-lookup"><span data-stu-id="436ae-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="436ae-105">句法</span><span class="sxs-lookup"><span data-stu-id="436ae-105">SYNTAX</span></span>

### <span data-ttu-id="436ae-106">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="436ae-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="436ae-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="436ae-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="436ae-108">說明</span><span class="sxs-lookup"><span data-stu-id="436ae-108">DESCRIPTION</span></span>
<span data-ttu-id="436ae-109">**AzNetworkInterfaceTapConfig** Cmdlet 會建立與 NetworkInterface 相關聯的 TapConfiguration 資源。</span><span class="sxs-lookup"><span data-stu-id="436ae-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="436ae-110">這會參照現有的 VirtualNetworkTap 資源。</span><span class="sxs-lookup"><span data-stu-id="436ae-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="436ae-111">示例</span><span class="sxs-lookup"><span data-stu-id="436ae-111">EXAMPLES</span></span>

### <span data-ttu-id="436ae-112">範例1：在指定 NetworkInterface 中新增 TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="436ae-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="436ae-113">將 TapConfiguration 新增到 sourceNic。</span><span class="sxs-lookup"><span data-stu-id="436ae-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="436ae-114">來自 sourceNic VM 的流量將會鏡像到 vVirtualNetworkTap 資源中所參照的目的地 VM。</span><span class="sxs-lookup"><span data-stu-id="436ae-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="436ae-115">參數</span><span class="sxs-lookup"><span data-stu-id="436ae-115">PARAMETERS</span></span>

### <span data-ttu-id="436ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="436ae-116">-DefaultProfile</span></span>
<span data-ttu-id="436ae-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="436ae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="436ae-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="436ae-118">-Name</span></span>
<span data-ttu-id="436ae-119">攻絲配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="436ae-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="436ae-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="436ae-120">-NetworkInterface</span></span>
<span data-ttu-id="436ae-121">網路介面資源的參照。</span><span class="sxs-lookup"><span data-stu-id="436ae-121">The reference of the network interface resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="436ae-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="436ae-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="436ae-123">虛擬網路攻絲資源的參照。</span><span class="sxs-lookup"><span data-stu-id="436ae-123">The reference of the virtual network tap resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="436ae-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="436ae-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="436ae-125">虛擬網路攻絲資源的參照。</span><span class="sxs-lookup"><span data-stu-id="436ae-125">The reference of the virtual network tap resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="436ae-126">-確認</span><span class="sxs-lookup"><span data-stu-id="436ae-126">-Confirm</span></span>
<span data-ttu-id="436ae-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="436ae-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="436ae-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="436ae-128">-WhatIf</span></span>
<span data-ttu-id="436ae-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="436ae-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="436ae-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="436ae-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="436ae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="436ae-131">CommonParameters</span></span>
<span data-ttu-id="436ae-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="436ae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="436ae-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="436ae-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="436ae-134">輸入</span><span class="sxs-lookup"><span data-stu-id="436ae-134">INPUTS</span></span>

### <span data-ttu-id="436ae-135">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="436ae-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="436ae-136">System.object</span><span class="sxs-lookup"><span data-stu-id="436ae-136">System.String</span></span>

### <span data-ttu-id="436ae-137">PSVirtualNetworkTap 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="436ae-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="436ae-138">輸出</span><span class="sxs-lookup"><span data-stu-id="436ae-138">OUTPUTS</span></span>

### <span data-ttu-id="436ae-139">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="436ae-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="436ae-140">筆記</span><span class="sxs-lookup"><span data-stu-id="436ae-140">NOTES</span></span>

## <span data-ttu-id="436ae-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="436ae-141">RELATED LINKS</span></span>

[<span data-ttu-id="436ae-142">AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="436ae-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="436ae-143">移除-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="436ae-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="436ae-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="436ae-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)