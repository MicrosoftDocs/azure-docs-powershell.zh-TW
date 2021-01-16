---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
ms.openlocfilehash: c57b704f54eacbd9b5cac808e69f9bbf289dc0cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284463"
---
# <span data-ttu-id="ad42c-101">Stop-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="ad42c-101">Stop-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="ad42c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad42c-102">SYNOPSIS</span></span>
<span data-ttu-id="ad42c-103">停止 SQL managed 實例的作業。</span><span class="sxs-lookup"><span data-stu-id="ad42c-103">Stops a SQL managed instance's operations.</span></span>

## <span data-ttu-id="ad42c-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad42c-104">SYNTAX</span></span>

### <span data-ttu-id="ad42c-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ad42c-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Default)</span></span>
```
Stop-AzSqlInstanceOperation [-Name] <String> [-ManagedInstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad42c-106">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad42c-106">StopByResourceIdParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad42c-107">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad42c-107">StopByInputObjectParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-InputObject] <AzureSqlManagedInstanceOperationModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad42c-108">說明</span><span class="sxs-lookup"><span data-stu-id="ad42c-108">DESCRIPTION</span></span>
<span data-ttu-id="ad42c-109">Stop-AzSqlInstanceOperation Cmdlet 會在 SQL managed 實例上以提供的操作名稱停止操作。</span><span class="sxs-lookup"><span data-stu-id="ad42c-109">The Stop-AzSqlInstanceOperation cmdlet stops operation with provided operation name on a SQL managed instance.</span></span>

## <span data-ttu-id="ad42c-110">示例</span><span class="sxs-lookup"><span data-stu-id="ad42c-110">EXAMPLES</span></span>

### <span data-ttu-id="ad42c-111">範例1：取得特定的操作</span><span class="sxs-lookup"><span data-stu-id="ad42c-111">Example 1: Get a specific operation</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name d0f5bef5-e2b1-4ef8-bb42-2e54073874f9

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:49:53 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="ad42c-112">這個命令會在 SQL managed 實例上停止使用「d0f5bef5-e2b1-4ef8-bb42-2e54073874f9」的 "name" 運算。</span><span class="sxs-lookup"><span data-stu-id="ad42c-112">This command stops operation with name 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' on a SQL managed instance.</span></span>

### <span data-ttu-id="ad42c-113">範例2：使用作業資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ad42c-113">Example 2: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 4253bf58-34f1-4499-80c6-198d94c659f7
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/4253bf58-34f1-4499-80c6-198d94c659f7
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 4253bf58-34f1-4499-80c6-198d94c659f7
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:47:32 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="ad42c-114">這個命令會停止作業，並使用資源識別碼 $managedInstanceOperation. Id。</span><span class="sxs-lookup"><span data-stu-id="ad42c-114">This command stops operation with resource id $managedInstanceOperation.Id.</span></span>

### <span data-ttu-id="ad42c-115">範例3：使用 operation 物件</span><span class="sxs-lookup"><span data-stu-id="ad42c-115">Example 3: Using operation object</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name b15a2b78-c42c-4e00-bf87-7ef4737552dc
PS C:\> Stop-AzSqlInstanceOperation -InputObject $managedInstanceOperation

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/b15a2b78-c42c-4e00-bf87-7ef4737552dc
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : b15a2b78-c42c-4e00-bf87-7ef4737552dc
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:44:57 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="ad42c-116">這個命令會停止與物件 $managedInstanceOperation 的操作。</span><span class="sxs-lookup"><span data-stu-id="ad42c-116">This command stops operation with object $managedInstanceOperation.</span></span>

## <span data-ttu-id="ad42c-117">參數</span><span class="sxs-lookup"><span data-stu-id="ad42c-117">PARAMETERS</span></span>

### <span data-ttu-id="ad42c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad42c-118">-DefaultProfile</span></span>
<span data-ttu-id="ad42c-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad42c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad42c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ad42c-120">-Force</span></span>
<span data-ttu-id="ad42c-121">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="ad42c-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ad42c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad42c-122">-InputObject</span></span>
<span data-ttu-id="ad42c-123">要取消的操作</span><span class="sxs-lookup"><span data-stu-id="ad42c-123">The operation to cancel</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel
Parameter Sets: StopByInputObjectParameterSet
Aliases: SqlInstanceOperation

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad42c-124">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="ad42c-124">-ManagedInstanceName</span></span>
<span data-ttu-id="ad42c-125">實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad42c-125">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad42c-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad42c-126">-Name</span></span>
<span data-ttu-id="ad42c-127">作業名稱。</span><span class="sxs-lookup"><span data-stu-id="ad42c-127">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases: OperationName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad42c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad42c-128">-ResourceGroupName</span></span>
<span data-ttu-id="ad42c-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad42c-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad42c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad42c-130">-ResourceId</span></span>
<span data-ttu-id="ad42c-131">要停止的 operation 物件資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ad42c-131">The resource id of operation object to stop</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad42c-132">-確認</span><span class="sxs-lookup"><span data-stu-id="ad42c-132">-Confirm</span></span>
<span data-ttu-id="ad42c-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ad42c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad42c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad42c-134">-WhatIf</span></span>
<span data-ttu-id="ad42c-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ad42c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad42c-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad42c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad42c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad42c-137">CommonParameters</span></span>
<span data-ttu-id="ad42c-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad42c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad42c-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ad42c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad42c-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ad42c-140">INPUTS</span></span>

### <span data-ttu-id="ad42c-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ad42c-141">System.String</span></span>

### <span data-ttu-id="ad42c-142">AzureSqlManagedInstanceOperationModel 中的 [ManagedInstanceOperation]</span><span class="sxs-lookup"><span data-stu-id="ad42c-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="ad42c-143">輸出</span><span class="sxs-lookup"><span data-stu-id="ad42c-143">OUTPUTS</span></span>

### <span data-ttu-id="ad42c-144">AzureSqlManagedInstanceOperationModel 中的 [ManagedInstanceOperation]</span><span class="sxs-lookup"><span data-stu-id="ad42c-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="ad42c-145">筆記</span><span class="sxs-lookup"><span data-stu-id="ad42c-145">NOTES</span></span>

## <span data-ttu-id="ad42c-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad42c-146">RELATED LINKS</span></span>