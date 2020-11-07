---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: 3d8445c78ae2f11fef734db0b24319b524f55704
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957680"
---
# <span data-ttu-id="80ddd-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="80ddd-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="80ddd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="80ddd-103">更新受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="80ddd-103">Updates managed application</span></span>

## <span data-ttu-id="80ddd-104">句法</span><span class="sxs-lookup"><span data-stu-id="80ddd-104">SYNTAX</span></span>

### <span data-ttu-id="80ddd-105">SetByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="80ddd-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80ddd-106">SetById</span><span class="sxs-lookup"><span data-stu-id="80ddd-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80ddd-107">說明</span><span class="sxs-lookup"><span data-stu-id="80ddd-107">DESCRIPTION</span></span>
<span data-ttu-id="80ddd-108">**AzManagedApplication** Cmdlet 會更新受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="80ddd-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="80ddd-109">示例</span><span class="sxs-lookup"><span data-stu-id="80ddd-109">EXAMPLES</span></span>

### <span data-ttu-id="80ddd-110">範例1：更新受管理的應用程式定義描述</span><span class="sxs-lookup"><span data-stu-id="80ddd-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="80ddd-111">這個命令會更新受管理的應用程式描述</span><span class="sxs-lookup"><span data-stu-id="80ddd-111">This command updates the managed application description</span></span>

## <span data-ttu-id="80ddd-112">參數</span><span class="sxs-lookup"><span data-stu-id="80ddd-112">PARAMETERS</span></span>

### <span data-ttu-id="80ddd-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="80ddd-113">-ApiVersion</span></span>
<span data-ttu-id="80ddd-114">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="80ddd-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="80ddd-115">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="80ddd-115">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ddd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80ddd-116">-DefaultProfile</span></span>
<span data-ttu-id="80ddd-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80ddd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80ddd-118">-識別碼</span><span class="sxs-lookup"><span data-stu-id="80ddd-118">-Id</span></span>
<span data-ttu-id="80ddd-119">完全限定的管理應用程式識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="80ddd-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="80ddd-120">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80ddd-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80ddd-121">類型</span><span class="sxs-lookup"><span data-stu-id="80ddd-121">-Kind</span></span>
<span data-ttu-id="80ddd-122">受管理的應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="80ddd-122">The managed application kind.</span></span>
<span data-ttu-id="80ddd-123">其中一個 marketplace 或 servicecatalog</span><span class="sxs-lookup"><span data-stu-id="80ddd-123">One of marketplace or servicecatalog</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ddd-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="80ddd-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="80ddd-125">受管理的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="80ddd-125">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80ddd-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80ddd-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="80ddd-127">受管理的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="80ddd-127">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80ddd-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="80ddd-128">-Name</span></span>
<span data-ttu-id="80ddd-129">受管理的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="80ddd-129">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80ddd-130">-參數</span><span class="sxs-lookup"><span data-stu-id="80ddd-130">-Parameter</span></span>
<span data-ttu-id="80ddd-131">受管理的應用程式之參數的 JSON 格式字串。</span><span class="sxs-lookup"><span data-stu-id="80ddd-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="80ddd-132">此路徑可以是包含參數的檔案名或 uri 路徑，或字串形式的參數。</span><span class="sxs-lookup"><span data-stu-id="80ddd-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80ddd-133">-方案</span><span class="sxs-lookup"><span data-stu-id="80ddd-133">-Plan</span></span>
<span data-ttu-id="80ddd-134">代表受管理的應用程式方案屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="80ddd-134">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ddd-135">-預先</span><span class="sxs-lookup"><span data-stu-id="80ddd-135">-Pre</span></span>
<span data-ttu-id="80ddd-136">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="80ddd-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="80ddd-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80ddd-137">-ResourceGroupName</span></span>
<span data-ttu-id="80ddd-138">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="80ddd-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80ddd-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="80ddd-139">-Tag</span></span>
<span data-ttu-id="80ddd-140">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="80ddd-140">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80ddd-141">-確認</span><span class="sxs-lookup"><span data-stu-id="80ddd-141">-Confirm</span></span>
<span data-ttu-id="80ddd-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="80ddd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80ddd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80ddd-143">-WhatIf</span></span>
<span data-ttu-id="80ddd-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80ddd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80ddd-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80ddd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80ddd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ddd-146">CommonParameters</span></span>
<span data-ttu-id="80ddd-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80ddd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ddd-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="80ddd-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ddd-149">輸入</span><span class="sxs-lookup"><span data-stu-id="80ddd-149">INPUTS</span></span>

### <span data-ttu-id="80ddd-150">System.object</span><span class="sxs-lookup"><span data-stu-id="80ddd-150">System.String</span></span>

### <span data-ttu-id="80ddd-151">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="80ddd-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="80ddd-152">輸出</span><span class="sxs-lookup"><span data-stu-id="80ddd-152">OUTPUTS</span></span>

### <span data-ttu-id="80ddd-153">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="80ddd-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="80ddd-154">筆記</span><span class="sxs-lookup"><span data-stu-id="80ddd-154">NOTES</span></span>

## <span data-ttu-id="80ddd-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="80ddd-155">RELATED LINKS</span></span>