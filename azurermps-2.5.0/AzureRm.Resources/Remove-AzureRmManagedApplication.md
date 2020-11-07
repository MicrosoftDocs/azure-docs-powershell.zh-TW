---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagedapplication
schema: 2.0.0
ms.openlocfilehash: 3897282708c310d59dffba52b3f5abfdf78d5f77
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802217"
---
# <span data-ttu-id="39102-101">Remove-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="39102-101">Remove-AzureRmManagedApplication</span></span>

## <span data-ttu-id="39102-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39102-102">SYNOPSIS</span></span>
<span data-ttu-id="39102-103">移除受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="39102-103">Removes a managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39102-104">句法</span><span class="sxs-lookup"><span data-stu-id="39102-104">SYNTAX</span></span>

### <span data-ttu-id="39102-105">RemoveByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="39102-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39102-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="39102-106">RemoveById</span></span>
```
Remove-AzureRmManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39102-107">說明</span><span class="sxs-lookup"><span data-stu-id="39102-107">DESCRIPTION</span></span>
<span data-ttu-id="39102-108">**AzureRmManagedApplication** Cmdlet 會移除受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="39102-108">The **Remove-AzureRmManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="39102-109">示例</span><span class="sxs-lookup"><span data-stu-id="39102-109">EXAMPLES</span></span>

### <span data-ttu-id="39102-110">範例1：依資源識別碼移除受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="39102-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzureRmManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="39102-111">第一個命令會使用 Get-AzureRmManagedApplication Cmdlet 來取得名為 myApp 的受管理應用程式。</span><span class="sxs-lookup"><span data-stu-id="39102-111">The first command gets a managed application named myApp by using the Get-AzureRmManagedApplication cmdlet.</span></span>
<span data-ttu-id="39102-112">該命令會將它儲存在 $Application 變數中。</span><span class="sxs-lookup"><span data-stu-id="39102-112">The command stores it in the $Application variable.</span></span>

<span data-ttu-id="39102-113">第二個命令會移除由 $Application 的 **ResourceId** 屬性所識別的管理應用程式。</span><span class="sxs-lookup"><span data-stu-id="39102-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="39102-114">參數</span><span class="sxs-lookup"><span data-stu-id="39102-114">PARAMETERS</span></span>

### <span data-ttu-id="39102-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="39102-115">-ApiVersion</span></span>
<span data-ttu-id="39102-116">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="39102-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="39102-117">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="39102-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39102-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39102-118">-DefaultProfile</span></span>
<span data-ttu-id="39102-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39102-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39102-120">-Force</span><span class="sxs-lookup"><span data-stu-id="39102-120">-Force</span></span>
<span data-ttu-id="39102-121">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="39102-121">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39102-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="39102-122">-Id</span></span>
<span data-ttu-id="39102-123">完全限定的管理應用程式識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="39102-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="39102-124">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="39102-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39102-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="39102-125">-Name</span></span>
<span data-ttu-id="39102-126">受管理的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="39102-126">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39102-127">-預先</span><span class="sxs-lookup"><span data-stu-id="39102-127">-Pre</span></span>
<span data-ttu-id="39102-128">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="39102-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39102-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39102-129">-ResourceGroupName</span></span>
<span data-ttu-id="39102-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="39102-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39102-131">-確認</span><span class="sxs-lookup"><span data-stu-id="39102-131">-Confirm</span></span>
<span data-ttu-id="39102-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="39102-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39102-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39102-133">-WhatIf</span></span>
<span data-ttu-id="39102-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="39102-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39102-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39102-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39102-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39102-136">CommonParameters</span></span>
<span data-ttu-id="39102-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39102-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39102-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="39102-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39102-139">輸入</span><span class="sxs-lookup"><span data-stu-id="39102-139">INPUTS</span></span>

### <span data-ttu-id="39102-140">System.object</span><span class="sxs-lookup"><span data-stu-id="39102-140">System.String</span></span>

## <span data-ttu-id="39102-141">輸出</span><span class="sxs-lookup"><span data-stu-id="39102-141">OUTPUTS</span></span>

### <span data-ttu-id="39102-142">System.object</span><span class="sxs-lookup"><span data-stu-id="39102-142">System.Boolean</span></span>

## <span data-ttu-id="39102-143">筆記</span><span class="sxs-lookup"><span data-stu-id="39102-143">NOTES</span></span>

## <span data-ttu-id="39102-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="39102-144">RELATED LINKS</span></span>