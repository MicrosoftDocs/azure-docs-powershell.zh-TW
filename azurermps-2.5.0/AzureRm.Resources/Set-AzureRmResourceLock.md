---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: ccb491742d9a66a7e6eb300d7e75be0dcfac687e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799729"
---
# <span data-ttu-id="e73a1-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="e73a1-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="e73a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e73a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e73a1-103">修改資源鎖。</span><span class="sxs-lookup"><span data-stu-id="e73a1-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e73a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="e73a1-104">SYNTAX</span></span>

### <span data-ttu-id="e73a1-105">BySpecifiedScope (預設) </span><span class="sxs-lookup"><span data-stu-id="e73a1-105">BySpecifiedScope (Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e73a1-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e73a1-106">ByResourceGroup</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e73a1-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="e73a1-107">ByResourceGroupLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e73a1-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="e73a1-108">BySubscription</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e73a1-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e73a1-109">BySubscriptionLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e73a1-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="e73a1-110">ByTenantLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e73a1-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="e73a1-111">ByLockId</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e73a1-112">說明</span><span class="sxs-lookup"><span data-stu-id="e73a1-112">DESCRIPTION</span></span>
<span data-ttu-id="e73a1-113">**AzureRmResourceLock** Cmdlet 會修改資源鎖。</span><span class="sxs-lookup"><span data-stu-id="e73a1-113">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="e73a1-114">示例</span><span class="sxs-lookup"><span data-stu-id="e73a1-114">EXAMPLES</span></span>

### <span data-ttu-id="e73a1-115">範例1：更新鎖定的筆記</span><span class="sxs-lookup"><span data-stu-id="e73a1-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="e73a1-116">這個命令會更新名為 ContosoSiteLock 之鎖定的筆記。</span><span class="sxs-lookup"><span data-stu-id="e73a1-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="e73a1-117">參數</span><span class="sxs-lookup"><span data-stu-id="e73a1-117">PARAMETERS</span></span>

### <span data-ttu-id="e73a1-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e73a1-118">-ApiVersion</span></span>
<span data-ttu-id="e73a1-119">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e73a1-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e73a1-120">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="e73a1-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e73a1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e73a1-121">-DefaultProfile</span></span>
<span data-ttu-id="e73a1-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e73a1-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73a1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e73a1-123">-Force</span></span>
<span data-ttu-id="e73a1-124">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e73a1-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e73a1-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e73a1-125">-InformationAction</span></span>
<span data-ttu-id="e73a1-126">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="e73a1-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="e73a1-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e73a1-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e73a1-128">持續</span><span class="sxs-lookup"><span data-stu-id="e73a1-128">Continue</span></span>
- <span data-ttu-id="e73a1-129">理會</span><span class="sxs-lookup"><span data-stu-id="e73a1-129">Ignore</span></span>
- <span data-ttu-id="e73a1-130">看</span><span class="sxs-lookup"><span data-stu-id="e73a1-130">Inquire</span></span>
- <span data-ttu-id="e73a1-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e73a1-131">SilentlyContinue</span></span>
- <span data-ttu-id="e73a1-132">停止</span><span class="sxs-lookup"><span data-stu-id="e73a1-132">Stop</span></span>
- <span data-ttu-id="e73a1-133">封存</span><span class="sxs-lookup"><span data-stu-id="e73a1-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73a1-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e73a1-134">-InformationVariable</span></span>
<span data-ttu-id="e73a1-135">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="e73a1-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73a1-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="e73a1-136">-LockId</span></span>
<span data-ttu-id="e73a1-137">指定此 Cmdlet 所修改之鎖定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e73a1-137">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73a1-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="e73a1-138">-LockLevel</span></span>
<span data-ttu-id="e73a1-139">指定鎖定的層級。</span><span class="sxs-lookup"><span data-stu-id="e73a1-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="e73a1-140">目前唯一有效的值是 CanNotDelete。</span><span class="sxs-lookup"><span data-stu-id="e73a1-140">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73a1-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="e73a1-141">-LockName</span></span>
<span data-ttu-id="e73a1-142">指定此 Cmdlet 修改的鎖定名稱。</span><span class="sxs-lookup"><span data-stu-id="e73a1-142">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73a1-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="e73a1-143">-LockNotes</span></span>
<span data-ttu-id="e73a1-144">指定鎖定的備忘稿。</span><span class="sxs-lookup"><span data-stu-id="e73a1-144">Specifies the notes for the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73a1-145">-預先</span><span class="sxs-lookup"><span data-stu-id="e73a1-145">-Pre</span></span>
<span data-ttu-id="e73a1-146">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e73a1-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e73a1-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e73a1-147">-ResourceGroupName</span></span>
<span data-ttu-id="e73a1-148">指定要套用鎖定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e73a1-148">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73a1-149">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="e73a1-149">-ResourceName</span></span>
<span data-ttu-id="e73a1-150">指定要套用鎖定之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e73a1-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="e73a1-151">例如，若要指定資料庫，請使用下列格式：伺服器 `/` 資料庫</span><span class="sxs-lookup"><span data-stu-id="e73a1-151">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73a1-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e73a1-152">-ResourceType</span></span>
<span data-ttu-id="e73a1-153">指定要套用鎖定的資源類型。</span><span class="sxs-lookup"><span data-stu-id="e73a1-153">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73a1-154">-範圍</span><span class="sxs-lookup"><span data-stu-id="e73a1-154">-Scope</span></span>
<span data-ttu-id="e73a1-155">指定要套用鎖定的範圍。</span><span class="sxs-lookup"><span data-stu-id="e73a1-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="e73a1-156">例如，若要指定資料庫，請使用下列格式： `/subscriptions/` 訂閱識別碼 `/resourceGroups/` 資源組名稱 `/providers/Microsoft.Sql/servers/` 伺服器名稱 `/databases/` 資料庫名稱若要指定資源群組，請使用下列格式： `/subscriptions/` 訂閱識別碼 `/resourceGroups/` 資源組名稱</span><span class="sxs-lookup"><span data-stu-id="e73a1-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73a1-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="e73a1-157">-TenantLevel</span></span>
<span data-ttu-id="e73a1-158">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="e73a1-158">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73a1-159">-確認</span><span class="sxs-lookup"><span data-stu-id="e73a1-159">-Confirm</span></span>
<span data-ttu-id="e73a1-160">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e73a1-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e73a1-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e73a1-161">-WhatIf</span></span>
<span data-ttu-id="e73a1-162">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e73a1-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e73a1-163">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e73a1-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e73a1-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e73a1-164">CommonParameters</span></span>
<span data-ttu-id="e73a1-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e73a1-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e73a1-166">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e73a1-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e73a1-167">輸入</span><span class="sxs-lookup"><span data-stu-id="e73a1-167">INPUTS</span></span>

## <span data-ttu-id="e73a1-168">輸出</span><span class="sxs-lookup"><span data-stu-id="e73a1-168">OUTPUTS</span></span>

## <span data-ttu-id="e73a1-169">筆記</span><span class="sxs-lookup"><span data-stu-id="e73a1-169">NOTES</span></span>

## <span data-ttu-id="e73a1-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="e73a1-170">RELATED LINKS</span></span>

[<span data-ttu-id="e73a1-171">AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="e73a1-171">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="e73a1-172">新-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="e73a1-172">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="e73a1-173">移除-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="e73a1-173">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

