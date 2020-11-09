---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: a553f5e1e6b4929997cbd850ca199e6fd7acef08
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287144"
---
# <span data-ttu-id="891d0-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="891d0-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="891d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="891d0-102">SYNOPSIS</span></span>
<span data-ttu-id="891d0-103">取得 Synapse 分析 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="891d0-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="891d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="891d0-104">SYNTAX</span></span>

### <span data-ttu-id="891d0-105">GetSparkStatementsByIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="891d0-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="891d0-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="891d0-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="891d0-107">說明</span><span class="sxs-lookup"><span data-stu-id="891d0-107">DESCRIPTION</span></span>
<span data-ttu-id="891d0-108">**AzSynapseSparkStatement** Cmdlet 會取得有關 Azure Synapse 分析 Spark 語句的資訊。</span><span class="sxs-lookup"><span data-stu-id="891d0-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="891d0-109">示例</span><span class="sxs-lookup"><span data-stu-id="891d0-109">EXAMPLES</span></span>

### <span data-ttu-id="891d0-110">範例1</span><span class="sxs-lookup"><span data-stu-id="891d0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="891d0-111">這個命令會在 Spark 會話下取得所有的 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="891d0-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="891d0-112">範例2</span><span class="sxs-lookup"><span data-stu-id="891d0-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="891d0-113">這個命令會取得具有指定 livy 識別碼的 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="891d0-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="891d0-114">範例3</span><span class="sxs-lookup"><span data-stu-id="891d0-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="891d0-115">這個命令會透過管線透過觸發會話來取得所有的 Spark 語句。</span><span class="sxs-lookup"><span data-stu-id="891d0-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="891d0-116">參數</span><span class="sxs-lookup"><span data-stu-id="891d0-116">PARAMETERS</span></span>

### <span data-ttu-id="891d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="891d0-117">-DefaultProfile</span></span>
<span data-ttu-id="891d0-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="891d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="891d0-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="891d0-119">-LivyId</span></span>
<span data-ttu-id="891d0-120">Spark 語句的識別碼。</span><span class="sxs-lookup"><span data-stu-id="891d0-120">Identifier of Spark statement.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891d0-121">-SessionId</span><span class="sxs-lookup"><span data-stu-id="891d0-121">-SessionId</span></span>
<span data-ttu-id="891d0-122">Spark 會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="891d0-122">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891d0-123">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="891d0-123">-SessionObject</span></span>
<span data-ttu-id="891d0-124">Spark 池輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="891d0-124">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="891d0-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="891d0-125">-SparkPoolName</span></span>
<span data-ttu-id="891d0-126">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="891d0-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891d0-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="891d0-127">-WorkspaceName</span></span>
<span data-ttu-id="891d0-128">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="891d0-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891d0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="891d0-129">CommonParameters</span></span>
<span data-ttu-id="891d0-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="891d0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="891d0-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="891d0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="891d0-132">輸入</span><span class="sxs-lookup"><span data-stu-id="891d0-132">INPUTS</span></span>

### <span data-ttu-id="891d0-133">PSSynapseSparkSession 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="891d0-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="891d0-134">輸出</span><span class="sxs-lookup"><span data-stu-id="891d0-134">OUTPUTS</span></span>

### <span data-ttu-id="891d0-135">PSSynapseSparkStatement 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="891d0-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="891d0-136">筆記</span><span class="sxs-lookup"><span data-stu-id="891d0-136">NOTES</span></span>

## <span data-ttu-id="891d0-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="891d0-137">RELATED LINKS</span></span>