---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 29062aa6ae5a69e44973fbdc29c6e9c6d2a583fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791721"
---
# <span data-ttu-id="8ec1b-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="8ec1b-101">New-AzPeeringService</span></span>

## <span data-ttu-id="8ec1b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ec1b-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec1b-103">建立新的對等服務。</span><span class="sxs-lookup"><span data-stu-id="8ec1b-103">Creates a new peering service.</span></span>

## <span data-ttu-id="8ec1b-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ec1b-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ec1b-105">說明</span><span class="sxs-lookup"><span data-stu-id="8ec1b-105">DESCRIPTION</span></span>
<span data-ttu-id="8ec1b-106">建立對等服務。</span><span class="sxs-lookup"><span data-stu-id="8ec1b-106">Creates peering service.</span></span>

## <span data-ttu-id="8ec1b-107">示例</span><span class="sxs-lookup"><span data-stu-id="8ec1b-107">EXAMPLES</span></span>

### <span data-ttu-id="8ec1b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8ec1b-108">Example 1</span></span>
```powershell
PS C:\> New-AzPeeringService -ResourceGroupName $resourceGroup -Name $name -Location $loc -PeeringServiceProvider $provider

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="8ec1b-109">使用提供者和對等位置建立對等服務物件。</span><span class="sxs-lookup"><span data-stu-id="8ec1b-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="8ec1b-110">搭配與 conjuction 搭配使用 `Get-AzPeeringServiceProvider``Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="8ec1b-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="8ec1b-111">參數</span><span class="sxs-lookup"><span data-stu-id="8ec1b-111">PARAMETERS</span></span>

### <span data-ttu-id="8ec1b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ec1b-112">-AsJob</span></span>
<span data-ttu-id="8ec1b-113">在背景中執行。</span><span class="sxs-lookup"><span data-stu-id="8ec1b-113">Run in the background.</span></span>

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

### <span data-ttu-id="8ec1b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec1b-114">-DefaultProfile</span></span>
<span data-ttu-id="8ec1b-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ec1b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ec1b-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="8ec1b-116">-Name</span></span>
<span data-ttu-id="8ec1b-117">PSPeering 的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="8ec1b-117">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ec1b-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="8ec1b-118">-PeeringLocation</span></span>
<span data-ttu-id="8ec1b-119">不同于 Azure 區域的物理位置。</span><span class="sxs-lookup"><span data-stu-id="8ec1b-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="8ec1b-120">使用 Get-AzPeeringServiceLocation [-Country <country> ]</span><span class="sxs-lookup"><span data-stu-id="8ec1b-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ec1b-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="8ec1b-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="8ec1b-122">對等服務提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="8ec1b-122">The peering service provider name.</span></span>
<span data-ttu-id="8ec1b-123">在清單中使用 Get-AzPeeringServiceProvider Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ec1b-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ec1b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ec1b-124">-ResourceGroupName</span></span>
<span data-ttu-id="8ec1b-125">建立或使用現有的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8ec1b-125">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ec1b-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="8ec1b-126">-Tag</span></span>
<span data-ttu-id="8ec1b-127">要與 Microsoft InputObject 服務相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="8ec1b-127">The tags to associate with the Microsoft InputObject Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ec1b-128">-確認</span><span class="sxs-lookup"><span data-stu-id="8ec1b-128">-Confirm</span></span>
<span data-ttu-id="8ec1b-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8ec1b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ec1b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ec1b-130">-WhatIf</span></span>
<span data-ttu-id="8ec1b-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ec1b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ec1b-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ec1b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ec1b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec1b-133">CommonParameters</span></span>
<span data-ttu-id="8ec1b-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ec1b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec1b-135">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8ec1b-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec1b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8ec1b-136">INPUTS</span></span>

### <span data-ttu-id="8ec1b-137">所有</span><span class="sxs-lookup"><span data-stu-id="8ec1b-137">None</span></span>

## <span data-ttu-id="8ec1b-138">輸出</span><span class="sxs-lookup"><span data-stu-id="8ec1b-138">OUTPUTS</span></span>

### <span data-ttu-id="8ec1b-139">PSPeeringService 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="8ec1b-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="8ec1b-140">筆記</span><span class="sxs-lookup"><span data-stu-id="8ec1b-140">NOTES</span></span>

## <span data-ttu-id="8ec1b-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ec1b-141">RELATED LINKS</span></span>