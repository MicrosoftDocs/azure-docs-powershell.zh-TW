---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: c0ebc561a047ffe6a62722012fd7ecd3d42e472a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959130"
---
# <span data-ttu-id="c72a4-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="c72a4-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="c72a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c72a4-102">SYNOPSIS</span></span>
<span data-ttu-id="c72a4-103">移除作業步驟</span><span class="sxs-lookup"><span data-stu-id="c72a4-103">Removes the job step</span></span>

## <span data-ttu-id="c72a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="c72a4-104">SYNTAX</span></span>

### <span data-ttu-id="c72a4-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c72a4-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c72a4-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="c72a4-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c72a4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c72a4-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c72a4-108">說明</span><span class="sxs-lookup"><span data-stu-id="c72a4-108">DESCRIPTION</span></span>
<span data-ttu-id="c72a4-109">Remove-AzSqlElasticJobStep Cmdlet 會從工作中移除作業步驟</span><span class="sxs-lookup"><span data-stu-id="c72a4-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="c72a4-110">示例</span><span class="sxs-lookup"><span data-stu-id="c72a4-110">EXAMPLES</span></span>

### <span data-ttu-id="c72a4-111">範例 1-從工作中移除作業步驟</span><span class="sxs-lookup"><span data-stu-id="c72a4-111">Example 1 - Removes a job step from a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="c72a4-112">從工作中移除作業步驟</span><span class="sxs-lookup"><span data-stu-id="c72a4-112">Removes a job step from a job</span></span>

## <span data-ttu-id="c72a4-113">參數</span><span class="sxs-lookup"><span data-stu-id="c72a4-113">PARAMETERS</span></span>

### <span data-ttu-id="c72a4-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c72a4-114">-AgentName</span></span>
<span data-ttu-id="c72a4-115">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="c72a4-115">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c72a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c72a4-116">-DefaultProfile</span></span>
<span data-ttu-id="c72a4-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c72a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c72a4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c72a4-118">-InputObject</span></span>
<span data-ttu-id="c72a4-119">作業步驟輸入物件</span><span class="sxs-lookup"><span data-stu-id="c72a4-119">The job step input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c72a4-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="c72a4-120">-JobName</span></span>
<span data-ttu-id="c72a4-121">作業名稱</span><span class="sxs-lookup"><span data-stu-id="c72a4-121">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c72a4-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c72a4-122">-Name</span></span>
<span data-ttu-id="c72a4-123">作業步驟名稱</span><span class="sxs-lookup"><span data-stu-id="c72a4-123">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c72a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c72a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="c72a4-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c72a4-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c72a4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c72a4-126">-ResourceId</span></span>
<span data-ttu-id="c72a4-127">作業步驟資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c72a4-127">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c72a4-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c72a4-128">-ServerName</span></span>
<span data-ttu-id="c72a4-129">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="c72a4-129">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c72a4-130">-確認</span><span class="sxs-lookup"><span data-stu-id="c72a4-130">-Confirm</span></span>
<span data-ttu-id="c72a4-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c72a4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c72a4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c72a4-132">-WhatIf</span></span>
<span data-ttu-id="c72a4-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c72a4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c72a4-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c72a4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c72a4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c72a4-135">CommonParameters</span></span>
<span data-ttu-id="c72a4-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c72a4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c72a4-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c72a4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c72a4-138">輸入</span><span class="sxs-lookup"><span data-stu-id="c72a4-138">INPUTS</span></span>

### <span data-ttu-id="c72a4-139">AzureSqlElasticJobStepModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="c72a4-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="c72a4-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c72a4-140">OUTPUTS</span></span>

### <span data-ttu-id="c72a4-141">AzureSqlElasticJobStepModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="c72a4-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="c72a4-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c72a4-142">NOTES</span></span>

## <span data-ttu-id="c72a4-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c72a4-143">RELATED LINKS</span></span>