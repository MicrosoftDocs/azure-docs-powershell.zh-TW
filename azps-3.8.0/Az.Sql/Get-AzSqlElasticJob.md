---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
ms.openlocfilehash: 60dac0ad09f30f339da82d84cf6200a44fe11859
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957457"
---
# <span data-ttu-id="9843b-101">Get-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="9843b-101">Get-AzSqlElasticJob</span></span>

## <span data-ttu-id="9843b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9843b-102">SYNOPSIS</span></span>
<span data-ttu-id="9843b-103">取得一或多個作業</span><span class="sxs-lookup"><span data-stu-id="9843b-103">Gets one or more jobs</span></span>

## <span data-ttu-id="9843b-104">句法</span><span class="sxs-lookup"><span data-stu-id="9843b-104">SYNTAX</span></span>

### <span data-ttu-id="9843b-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9843b-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9843b-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="9843b-106">ObjectSet</span></span>
```
Get-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9843b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9843b-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJob [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9843b-108">說明</span><span class="sxs-lookup"><span data-stu-id="9843b-108">DESCRIPTION</span></span>
<span data-ttu-id="9843b-109">Get-AzSqlElasticJob Cmdlet 會取得一或多個作業</span><span class="sxs-lookup"><span data-stu-id="9843b-109">The Get-AzSqlElasticJob cmdlet gets one or more jobs</span></span>

## <span data-ttu-id="9843b-110">示例</span><span class="sxs-lookup"><span data-stu-id="9843b-110">EXAMPLES</span></span>

### <span data-ttu-id="9843b-111">範例 1-取得工作</span><span class="sxs-lookup"><span data-stu-id="9843b-111">Example 1 - Gets a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="9843b-112">取得工作</span><span class="sxs-lookup"><span data-stu-id="9843b-112">Gets a job</span></span>

## <span data-ttu-id="9843b-113">參數</span><span class="sxs-lookup"><span data-stu-id="9843b-113">PARAMETERS</span></span>

### <span data-ttu-id="9843b-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="9843b-114">-AgentName</span></span>
<span data-ttu-id="9843b-115">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="9843b-115">The agent name</span></span>

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

### <span data-ttu-id="9843b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9843b-116">-DefaultProfile</span></span>
<span data-ttu-id="9843b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9843b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9843b-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="9843b-118">-Name</span></span>
<span data-ttu-id="9843b-119">作業名稱</span><span class="sxs-lookup"><span data-stu-id="9843b-119">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9843b-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9843b-120">-ParentObject</span></span>
<span data-ttu-id="9843b-121">Agent 輸入物件</span><span class="sxs-lookup"><span data-stu-id="9843b-121">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9843b-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9843b-122">-ParentResourceId</span></span>
<span data-ttu-id="9843b-123">Agent 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9843b-123">The agent resource id</span></span>

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

### <span data-ttu-id="9843b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9843b-124">-ResourceGroupName</span></span>
<span data-ttu-id="9843b-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="9843b-125">The resource group name</span></span>

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

### <span data-ttu-id="9843b-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9843b-126">-ServerName</span></span>
<span data-ttu-id="9843b-127">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="9843b-127">The server name</span></span>

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

### <span data-ttu-id="9843b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9843b-128">CommonParameters</span></span>
<span data-ttu-id="9843b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9843b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9843b-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9843b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9843b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="9843b-131">INPUTS</span></span>

### <span data-ttu-id="9843b-132">AzureSqlElasticJobAgentModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="9843b-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="9843b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="9843b-133">OUTPUTS</span></span>

### <span data-ttu-id="9843b-134">AzureSqlElasticJobModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="9843b-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="9843b-135">筆記</span><span class="sxs-lookup"><span data-stu-id="9843b-135">NOTES</span></span>

## <span data-ttu-id="9843b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="9843b-136">RELATED LINKS</span></span>