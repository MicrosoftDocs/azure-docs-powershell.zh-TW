---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: b89772c1afe621e456dfb269fe869b6cd3fa8a8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790782"
---
# <span data-ttu-id="6cd76-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6cd76-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="6cd76-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6cd76-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd76-103">建立路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="6cd76-103">Creates a route filter.</span></span>

## <span data-ttu-id="6cd76-104">句法</span><span class="sxs-lookup"><span data-stu-id="6cd76-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6cd76-105">說明</span><span class="sxs-lookup"><span data-stu-id="6cd76-105">DESCRIPTION</span></span>
<span data-ttu-id="6cd76-106">New-AzRouteFilter Cmdlet 會建立 Azure 路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="6cd76-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="6cd76-107">示例</span><span class="sxs-lookup"><span data-stu-id="6cd76-107">EXAMPLES</span></span>

### <span data-ttu-id="6cd76-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6cd76-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="6cd76-109">該命令會建立新的路由篩選器。</span><span class="sxs-lookup"><span data-stu-id="6cd76-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="6cd76-110">參數</span><span class="sxs-lookup"><span data-stu-id="6cd76-110">PARAMETERS</span></span>

### <span data-ttu-id="6cd76-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cd76-111">-AsJob</span></span>
<span data-ttu-id="6cd76-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6cd76-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6cd76-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd76-113">-DefaultProfile</span></span>
<span data-ttu-id="6cd76-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6cd76-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cd76-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6cd76-115">-Force</span></span>
<span data-ttu-id="6cd76-116">表示此 Cmdlet 會建立路由資料表，即使已存在具有相同名稱的路由篩選器也一樣。</span><span class="sxs-lookup"><span data-stu-id="6cd76-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="6cd76-117">-位置</span><span class="sxs-lookup"><span data-stu-id="6cd76-117">-Location</span></span>
<span data-ttu-id="6cd76-118">指定此 Cmdlet 建立路由篩選器的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="6cd76-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="6cd76-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6cd76-119">-Name</span></span>
<span data-ttu-id="6cd76-120">指定路由篩選的名稱。</span><span class="sxs-lookup"><span data-stu-id="6cd76-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="6cd76-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cd76-121">-ResourceGroupName</span></span>
<span data-ttu-id="6cd76-122">指定此 Cmdlet 用來建立路由篩選器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6cd76-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="6cd76-123">-規則</span><span class="sxs-lookup"><span data-stu-id="6cd76-123">-Rule</span></span>
<span data-ttu-id="6cd76-124">指定路由篩選規則物件的陣列，以與路由篩選器建立關聯。</span><span class="sxs-lookup"><span data-stu-id="6cd76-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cd76-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="6cd76-125">-Tag</span></span>
<span data-ttu-id="6cd76-126">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="6cd76-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6cd76-127">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6cd76-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cd76-128">-確認</span><span class="sxs-lookup"><span data-stu-id="6cd76-128">-Confirm</span></span>
<span data-ttu-id="6cd76-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6cd76-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cd76-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cd76-130">-WhatIf</span></span>
<span data-ttu-id="6cd76-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6cd76-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6cd76-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6cd76-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cd76-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd76-133">CommonParameters</span></span>
<span data-ttu-id="6cd76-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6cd76-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd76-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6cd76-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd76-136">輸入</span><span class="sxs-lookup"><span data-stu-id="6cd76-136">INPUTS</span></span>

### <span data-ttu-id="6cd76-137">System.object</span><span class="sxs-lookup"><span data-stu-id="6cd76-137">System.String</span></span>

### <span data-ttu-id="6cd76-138">PSRouteFilterRule [] （[]）</span><span class="sxs-lookup"><span data-stu-id="6cd76-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="6cd76-139">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6cd76-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6cd76-140">輸出</span><span class="sxs-lookup"><span data-stu-id="6cd76-140">OUTPUTS</span></span>

### <span data-ttu-id="6cd76-141">PSRouteFilter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6cd76-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="6cd76-142">筆記</span><span class="sxs-lookup"><span data-stu-id="6cd76-142">NOTES</span></span>
<span data-ttu-id="6cd76-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="6cd76-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6cd76-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="6cd76-144">RELATED LINKS</span></span>

[<span data-ttu-id="6cd76-145">AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6cd76-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="6cd76-146">移除-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6cd76-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="6cd76-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6cd76-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="6cd76-148">附加 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cd76-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6cd76-149">AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cd76-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6cd76-150">新-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cd76-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6cd76-151">移除-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cd76-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6cd76-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cd76-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)