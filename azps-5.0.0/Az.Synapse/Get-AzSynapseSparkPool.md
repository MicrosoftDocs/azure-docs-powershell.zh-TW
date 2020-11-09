---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287148"
---
# <span data-ttu-id="a9b47-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="a9b47-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="a9b47-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9b47-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b47-103">取得 Synapse 分析 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="a9b47-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="a9b47-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9b47-104">SYNTAX</span></span>

### <span data-ttu-id="a9b47-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a9b47-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9b47-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9b47-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9b47-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9b47-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9b47-108">說明</span><span class="sxs-lookup"><span data-stu-id="a9b47-108">DESCRIPTION</span></span>
<span data-ttu-id="a9b47-109">**AzSynapseSparkPool** Cmdlet 會取得 Azure Synapse 分析 Spark 池的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a9b47-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="a9b47-110">示例</span><span class="sxs-lookup"><span data-stu-id="a9b47-110">EXAMPLES</span></span>

### <span data-ttu-id="a9b47-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a9b47-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a9b47-112">這個命令會取得工作區底下的所有 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="a9b47-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="a9b47-113">範例2</span><span class="sxs-lookup"><span data-stu-id="a9b47-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="a9b47-114">這個命令會在 [工作區 ContosoWorkspace] 下取得 [名稱 ContosoSparkPool] 底下的 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="a9b47-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="a9b47-115">範例3</span><span class="sxs-lookup"><span data-stu-id="a9b47-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="a9b47-116">這個命令會透過流水線取得工作區底下的所有 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="a9b47-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="a9b47-117">範例4</span><span class="sxs-lookup"><span data-stu-id="a9b47-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="a9b47-118">這個命令會取得具有指定資源識別碼的 Spark 池。</span><span class="sxs-lookup"><span data-stu-id="a9b47-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="a9b47-119">參數</span><span class="sxs-lookup"><span data-stu-id="a9b47-119">PARAMETERS</span></span>

### <span data-ttu-id="a9b47-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b47-120">-DefaultProfile</span></span>
<span data-ttu-id="a9b47-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9b47-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9b47-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9b47-122">-Name</span></span>
<span data-ttu-id="a9b47-123">Synapse Spark 池的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9b47-123">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SparkPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b47-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9b47-124">-ResourceGroupName</span></span>
<span data-ttu-id="a9b47-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a9b47-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b47-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9b47-126">-ResourceId</span></span>
<span data-ttu-id="a9b47-127">Synapse Spark 池的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9b47-127">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b47-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a9b47-128">-WorkspaceName</span></span>
<span data-ttu-id="a9b47-129">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9b47-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b47-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a9b47-130">-WorkspaceObject</span></span>
<span data-ttu-id="a9b47-131">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="a9b47-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b47-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b47-132">CommonParameters</span></span>
<span data-ttu-id="a9b47-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9b47-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b47-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a9b47-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b47-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a9b47-135">INPUTS</span></span>

### <span data-ttu-id="a9b47-136">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a9b47-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a9b47-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a9b47-137">OUTPUTS</span></span>

### <span data-ttu-id="a9b47-138">PSSynapseSparkPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="a9b47-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="a9b47-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a9b47-139">NOTES</span></span>

## <span data-ttu-id="a9b47-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9b47-140">RELATED LINKS</span></span>