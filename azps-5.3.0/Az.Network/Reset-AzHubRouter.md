---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 039d37f9d9dd7b5af026b7ce2a87113513949b67
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288623"
---
# <span data-ttu-id="8c799-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="8c799-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="8c799-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c799-102">SYNOPSIS</span></span>
<span data-ttu-id="8c799-103">重設 VirtualHub 資源的 RoutingState。</span><span class="sxs-lookup"><span data-stu-id="8c799-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="8c799-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c799-104">SYNTAX</span></span>

### <span data-ttu-id="8c799-105">ByVirtualHubName (預設) </span><span class="sxs-lookup"><span data-stu-id="8c799-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c799-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="8c799-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c799-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="8c799-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c799-108">說明</span><span class="sxs-lookup"><span data-stu-id="8c799-108">DESCRIPTION</span></span>
<span data-ttu-id="8c799-109">只有在未預配虛擬中樞的路由狀態時，才會重設現有 VirtualHub 資源的路由狀態。</span><span class="sxs-lookup"><span data-stu-id="8c799-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="8c799-110">示例</span><span class="sxs-lookup"><span data-stu-id="8c799-110">EXAMPLES</span></span>

### <span data-ttu-id="8c799-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8c799-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="8c799-112">使用其 ResourceGroupName 和 CoNtext.resourcename 來重設虛擬中心的路由狀態。</span><span class="sxs-lookup"><span data-stu-id="8c799-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="8c799-113">範例2</span><span class="sxs-lookup"><span data-stu-id="8c799-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="8c799-114">使用虛擬中心的 ResourceId 來重設其路由狀態。</span><span class="sxs-lookup"><span data-stu-id="8c799-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="8c799-115">範例3</span><span class="sxs-lookup"><span data-stu-id="8c799-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="8c799-116">使用輸入物件來重設虛擬中心的路由狀態。</span><span class="sxs-lookup"><span data-stu-id="8c799-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="8c799-117">輸入物件的類型是 PSVirtualHub。</span><span class="sxs-lookup"><span data-stu-id="8c799-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="8c799-118">範例4</span><span class="sxs-lookup"><span data-stu-id="8c799-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="8c799-119">您可以檢索現有的虛擬中心物件，然後將它作為輸入物件傳遞給 Reset-AzHubRouter。</span><span class="sxs-lookup"><span data-stu-id="8c799-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="8c799-120">參數</span><span class="sxs-lookup"><span data-stu-id="8c799-120">PARAMETERS</span></span>

### <span data-ttu-id="8c799-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c799-121">-AsJob</span></span>
<span data-ttu-id="8c799-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c799-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c799-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c799-123">-DefaultProfile</span></span>
<span data-ttu-id="8c799-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c799-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c799-125">-Force</span><span class="sxs-lookup"><span data-stu-id="8c799-125">-Force</span></span>
<span data-ttu-id="8c799-126">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="8c799-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8c799-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c799-127">-InputObject</span></span>
<span data-ttu-id="8c799-128">要修改的虛擬中心物件。</span><span class="sxs-lookup"><span data-stu-id="8c799-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c799-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c799-129">-Name</span></span>
<span data-ttu-id="8c799-130">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8c799-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c799-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c799-131">-ResourceGroupName</span></span>
<span data-ttu-id="8c799-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c799-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c799-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c799-133">-ResourceId</span></span>
<span data-ttu-id="8c799-134">要修改之虛擬中心的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c799-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c799-135">-確認</span><span class="sxs-lookup"><span data-stu-id="8c799-135">-Confirm</span></span>
<span data-ttu-id="8c799-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c799-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c799-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c799-137">-WhatIf</span></span>
<span data-ttu-id="8c799-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c799-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c799-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c799-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c799-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c799-140">CommonParameters</span></span>
<span data-ttu-id="8c799-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c799-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c799-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c799-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c799-143">輸入</span><span class="sxs-lookup"><span data-stu-id="8c799-143">INPUTS</span></span>

### <span data-ttu-id="8c799-144">System.object</span><span class="sxs-lookup"><span data-stu-id="8c799-144">System.String</span></span>

### <span data-ttu-id="8c799-145">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8c799-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="8c799-146">輸出</span><span class="sxs-lookup"><span data-stu-id="8c799-146">OUTPUTS</span></span>

### <span data-ttu-id="8c799-147">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8c799-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="8c799-148">筆記</span><span class="sxs-lookup"><span data-stu-id="8c799-148">NOTES</span></span>

## <span data-ttu-id="8c799-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c799-149">RELATED LINKS</span></span>

[<span data-ttu-id="8c799-150">AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8c799-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)