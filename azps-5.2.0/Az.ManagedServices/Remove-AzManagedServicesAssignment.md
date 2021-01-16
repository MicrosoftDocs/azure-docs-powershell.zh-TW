---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: a3a39db5f110f247ab58f2b4c6afcdb4536f4f50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283787"
---
# <span data-ttu-id="ce662-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="ce662-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="ce662-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce662-102">SYNOPSIS</span></span>
<span data-ttu-id="ce662-103">刪除註冊作業。</span><span class="sxs-lookup"><span data-stu-id="ce662-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="ce662-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce662-104">SYNTAX</span></span>

### <span data-ttu-id="ce662-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="ce662-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [-Scope <String>] -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce662-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ce662-106">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce662-107">說明</span><span class="sxs-lookup"><span data-stu-id="ce662-107">DESCRIPTION</span></span>
<span data-ttu-id="ce662-108">刪除註冊作業。</span><span class="sxs-lookup"><span data-stu-id="ce662-108">Deletes a registration assignment.</span></span>

## <span data-ttu-id="ce662-109">示例</span><span class="sxs-lookup"><span data-stu-id="ce662-109">EXAMPLES</span></span>

### <span data-ttu-id="ce662-110">範例1</span><span class="sxs-lookup"><span data-stu-id="ce662-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80
PS C:\>
```

<span data-ttu-id="ce662-111">依名稱在預設範圍中刪除登記指派。</span><span class="sxs-lookup"><span data-stu-id="ce662-111">Deletes the registration assignment by name at the default scope.</span></span>

### <span data-ttu-id="ce662-112">範例2</span><span class="sxs-lookup"><span data-stu-id="ce662-112">Example 2</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 12b05f0f-3426-48da-9e67-738e1dbf775f
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
PS C:\>
```

<span data-ttu-id="ce662-113">使用提供的輸入物件刪除註冊作業。</span><span class="sxs-lookup"><span data-stu-id="ce662-113">Deletes the registration assignment using the input object provided.</span></span>

### <span data-ttu-id="ce662-114">範例3</span><span class="sxs-lookup"><span data-stu-id="ce662-114">Example 3</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinition $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b279ec53-b42f-4952-bd62-cd49982e9572 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/b279ec53-b42f-4952-bd62-cd49982e9572 Succeeded


PS C:\> Remove-AzManagedServicesAssignment -Name b279ec53-b42f-4952-bd62-cd49982e9572 -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8
PS C:\>
```

<span data-ttu-id="ce662-115">在指定的範圍內，依名稱刪除註冊作業。</span><span class="sxs-lookup"><span data-stu-id="ce662-115">Deletes the registration assignment by name at the given scope.</span></span>

## <span data-ttu-id="ce662-116">參數</span><span class="sxs-lookup"><span data-stu-id="ce662-116">PARAMETERS</span></span>

### <span data-ttu-id="ce662-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce662-117">-DefaultProfile</span></span>
<span data-ttu-id="ce662-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce662-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce662-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce662-119">-InputObject</span></span>
<span data-ttu-id="ce662-120">[註冊指派] 物件。</span><span class="sxs-lookup"><span data-stu-id="ce662-120">The registration assignment object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce662-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce662-121">-Name</span></span>
<span data-ttu-id="ce662-122">註冊作業的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="ce662-122">The unique name of the Registration Assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce662-123">-範圍</span><span class="sxs-lookup"><span data-stu-id="ce662-123">-Scope</span></span>
<span data-ttu-id="ce662-124">註冊作業的範圍。</span><span class="sxs-lookup"><span data-stu-id="ce662-124">The scope of the registration assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce662-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce662-125">-AsJob</span></span>
<span data-ttu-id="ce662-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce662-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce662-127">-確認</span><span class="sxs-lookup"><span data-stu-id="ce662-127">-Confirm</span></span>
<span data-ttu-id="ce662-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce662-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce662-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce662-129">-WhatIf</span></span>
<span data-ttu-id="ce662-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce662-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce662-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce662-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce662-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce662-132">CommonParameters</span></span>
<span data-ttu-id="ce662-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce662-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce662-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ce662-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce662-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ce662-135">INPUTS</span></span>

### <span data-ttu-id="ce662-136">PSRegistrationAssignment （ManagedServices）的</span><span class="sxs-lookup"><span data-stu-id="ce662-136">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="ce662-137">輸出</span><span class="sxs-lookup"><span data-stu-id="ce662-137">OUTPUTS</span></span>

### <span data-ttu-id="ce662-138">System.void</span><span class="sxs-lookup"><span data-stu-id="ce662-138">System.Void</span></span>
## <span data-ttu-id="ce662-139">筆記</span><span class="sxs-lookup"><span data-stu-id="ce662-139">NOTES</span></span>

## <span data-ttu-id="ce662-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce662-140">RELATED LINKS</span></span>