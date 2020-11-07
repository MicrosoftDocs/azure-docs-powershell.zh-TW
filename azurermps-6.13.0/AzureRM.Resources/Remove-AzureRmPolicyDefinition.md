---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 9d59a974a29743004228efb414a92627782bd8e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625251"
---
# <span data-ttu-id="14486-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="14486-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="14486-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14486-102">SYNOPSIS</span></span>
<span data-ttu-id="14486-103">移除原則定義。</span><span class="sxs-lookup"><span data-stu-id="14486-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14486-104">句法</span><span class="sxs-lookup"><span data-stu-id="14486-104">SYNTAX</span></span>

### <span data-ttu-id="14486-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="14486-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14486-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="14486-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14486-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14486-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14486-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14486-108">IdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14486-109">說明</span><span class="sxs-lookup"><span data-stu-id="14486-109">DESCRIPTION</span></span>
<span data-ttu-id="14486-110">**AzureRmPolicyDefinition** Cmdlet 會移除原則定義。</span><span class="sxs-lookup"><span data-stu-id="14486-110">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="14486-111">示例</span><span class="sxs-lookup"><span data-stu-id="14486-111">EXAMPLES</span></span>

### <span data-ttu-id="14486-112">範例1：依名稱移除原則定義</span><span class="sxs-lookup"><span data-stu-id="14486-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="14486-113">這個命令會移除指定的原則定義。</span><span class="sxs-lookup"><span data-stu-id="14486-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="14486-114">範例2：依資源識別碼移除原則定義</span><span class="sxs-lookup"><span data-stu-id="14486-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="14486-115">第一個命令會使用 Get-AzureRmPolicyDefinition Cmdlet 來取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="14486-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="14486-116">該命令會將它儲存在 $PolicyDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="14486-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="14486-117">第二個命令會移除由 $PolicyDefinition 的 **ResourceId** 屬性所識別的原則定義。</span><span class="sxs-lookup"><span data-stu-id="14486-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="14486-118">參數</span><span class="sxs-lookup"><span data-stu-id="14486-118">PARAMETERS</span></span>

### <span data-ttu-id="14486-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="14486-119">-ApiVersion</span></span>
<span data-ttu-id="14486-120">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="14486-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="14486-121">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="14486-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="14486-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14486-122">-DefaultProfile</span></span>
<span data-ttu-id="14486-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="14486-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14486-124">-Force</span><span class="sxs-lookup"><span data-stu-id="14486-124">-Force</span></span>
<span data-ttu-id="14486-125">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="14486-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="14486-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="14486-126">-Id</span></span>
<span data-ttu-id="14486-127">指定此 Cmdlet 移除之原則定義的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="14486-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14486-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="14486-128">-InformationAction</span></span>
<span data-ttu-id="14486-129">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="14486-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="14486-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="14486-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14486-131">持續</span><span class="sxs-lookup"><span data-stu-id="14486-131">Continue</span></span>
- <span data-ttu-id="14486-132">理會</span><span class="sxs-lookup"><span data-stu-id="14486-132">Ignore</span></span>
- <span data-ttu-id="14486-133">看</span><span class="sxs-lookup"><span data-stu-id="14486-133">Inquire</span></span>
- <span data-ttu-id="14486-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="14486-134">SilentlyContinue</span></span>
- <span data-ttu-id="14486-135">停止</span><span class="sxs-lookup"><span data-stu-id="14486-135">Stop</span></span>
- <span data-ttu-id="14486-136">封存</span><span class="sxs-lookup"><span data-stu-id="14486-136">Suspend</span></span>

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

### <span data-ttu-id="14486-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="14486-137">-InformationVariable</span></span>
<span data-ttu-id="14486-138">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="14486-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="14486-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="14486-139">-ManagementGroupName</span></span>
<span data-ttu-id="14486-140">要刪除之原則定義之管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="14486-140">The name of the management group of the policy definition to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14486-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="14486-141">-Name</span></span>
<span data-ttu-id="14486-142">指定此 Cmdlet 移除之原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="14486-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14486-143">-預先</span><span class="sxs-lookup"><span data-stu-id="14486-143">-Pre</span></span>
<span data-ttu-id="14486-144">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="14486-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="14486-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14486-145">-SubscriptionId</span></span>
<span data-ttu-id="14486-146">要刪除之原則定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="14486-146">The subscription ID of the policy definition to delete.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14486-147">-確認</span><span class="sxs-lookup"><span data-stu-id="14486-147">-Confirm</span></span>
<span data-ttu-id="14486-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="14486-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14486-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14486-149">-WhatIf</span></span>
<span data-ttu-id="14486-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="14486-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14486-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="14486-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14486-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14486-152">CommonParameters</span></span>
<span data-ttu-id="14486-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14486-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14486-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="14486-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14486-155">輸入</span><span class="sxs-lookup"><span data-stu-id="14486-155">INPUTS</span></span>

## <span data-ttu-id="14486-156">輸出</span><span class="sxs-lookup"><span data-stu-id="14486-156">OUTPUTS</span></span>

## <span data-ttu-id="14486-157">筆記</span><span class="sxs-lookup"><span data-stu-id="14486-157">NOTES</span></span>

## <span data-ttu-id="14486-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="14486-158">RELATED LINKS</span></span>

[<span data-ttu-id="14486-159">AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="14486-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="14486-160">新-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="14486-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="14486-161">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="14486-161">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)

