---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 76bb062105567303baac72f0b27f14f36bdb120d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794732"
---
# <span data-ttu-id="72d73-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="72d73-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="72d73-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72d73-102">SYNOPSIS</span></span>
<span data-ttu-id="72d73-103">這個作業會停用災害復原，並停止將主要的變更複製到次要命名空間</span><span class="sxs-lookup"><span data-stu-id="72d73-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="72d73-104">句法</span><span class="sxs-lookup"><span data-stu-id="72d73-104">SYNTAX</span></span>

### <span data-ttu-id="72d73-105">GeoDRParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="72d73-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72d73-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="72d73-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72d73-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="72d73-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72d73-108">說明</span><span class="sxs-lookup"><span data-stu-id="72d73-108">DESCRIPTION</span></span>
<span data-ttu-id="72d73-109">**AzEventHubGeoDRConfigurationBreakPair** Cmdlet 會停用災害復原，並停止將主要的變更複製到次要命名空間</span><span class="sxs-lookup"><span data-stu-id="72d73-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="72d73-110">示例</span><span class="sxs-lookup"><span data-stu-id="72d73-110">EXAMPLES</span></span>

### <span data-ttu-id="72d73-111">範例</span><span class="sxs-lookup"><span data-stu-id="72d73-111">Example</span></span>
```
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="72d73-112">這個作業會停用災害復原，並停止將主要的變更複製到次要命名空間</span><span class="sxs-lookup"><span data-stu-id="72d73-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="72d73-113">參數</span><span class="sxs-lookup"><span data-stu-id="72d73-113">PARAMETERS</span></span>

### <span data-ttu-id="72d73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72d73-114">-DefaultProfile</span></span>
<span data-ttu-id="72d73-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="72d73-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72d73-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72d73-116">-InputObject</span></span>
<span data-ttu-id="72d73-117">Eventhub GeoDR Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="72d73-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72d73-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="72d73-118">-Name</span></span>
<span data-ttu-id="72d73-119">DR 配置名稱</span><span class="sxs-lookup"><span data-stu-id="72d73-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72d73-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="72d73-120">-Namespace</span></span>
<span data-ttu-id="72d73-121">命名空間名稱-主要命名空間</span><span class="sxs-lookup"><span data-stu-id="72d73-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72d73-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72d73-122">-PassThru</span></span>
<span data-ttu-id="72d73-123">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="72d73-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="72d73-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="72d73-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="72d73-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72d73-125">-ResourceGroupName</span></span>
<span data-ttu-id="72d73-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="72d73-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72d73-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72d73-127">-ResourceId</span></span>
<span data-ttu-id="72d73-128">GeoDRConfiguration 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="72d73-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72d73-129">-確認</span><span class="sxs-lookup"><span data-stu-id="72d73-129">-Confirm</span></span>
<span data-ttu-id="72d73-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="72d73-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72d73-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72d73-131">-WhatIf</span></span>
<span data-ttu-id="72d73-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="72d73-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72d73-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72d73-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72d73-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72d73-134">CommonParameters</span></span>
<span data-ttu-id="72d73-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72d73-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72d73-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="72d73-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72d73-137">輸入</span><span class="sxs-lookup"><span data-stu-id="72d73-137">INPUTS</span></span>

### <span data-ttu-id="72d73-138">System.object</span><span class="sxs-lookup"><span data-stu-id="72d73-138">System.String</span></span>

### <span data-ttu-id="72d73-139">PSEventHubDRConfigurationAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="72d73-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="72d73-140">輸出</span><span class="sxs-lookup"><span data-stu-id="72d73-140">OUTPUTS</span></span>

### <span data-ttu-id="72d73-141">System.object</span><span class="sxs-lookup"><span data-stu-id="72d73-141">System.Boolean</span></span>

## <span data-ttu-id="72d73-142">筆記</span><span class="sxs-lookup"><span data-stu-id="72d73-142">NOTES</span></span>

## <span data-ttu-id="72d73-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="72d73-143">RELATED LINKS</span></span>