---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 6eab5c80fa8c21d5b592f0e194a5aba50c4d3002
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284424"
---
# <span data-ttu-id="f73bc-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f73bc-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="f73bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f73bc-102">SYNOPSIS</span></span>
<span data-ttu-id="f73bc-103">在指定的群集上啟動已定義的 Azure HDInsight 作業。</span><span class="sxs-lookup"><span data-stu-id="f73bc-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="f73bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="f73bc-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f73bc-105">說明</span><span class="sxs-lookup"><span data-stu-id="f73bc-105">DESCRIPTION</span></span>
<span data-ttu-id="f73bc-106">**Start-AzHDInsightJob** Cmdlet 會在指定的群集上啟動已定義的 Azure HDInsight 作業。</span><span class="sxs-lookup"><span data-stu-id="f73bc-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="f73bc-107">這可以是 MapReduce 作業、流式 MapReduce 作業、Hive 作業或豬作業。</span><span class="sxs-lookup"><span data-stu-id="f73bc-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="f73bc-108">示例</span><span class="sxs-lookup"><span data-stu-id="f73bc-108">EXAMPLES</span></span>

### <span data-ttu-id="f73bc-109">範例1：在指定的群集上開始作業</span><span class="sxs-lookup"><span data-stu-id="f73bc-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="f73bc-110">這個命令會在名為 [您的-hadoop-001] 的群集上啟動作業。</span><span class="sxs-lookup"><span data-stu-id="f73bc-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="f73bc-111">參數</span><span class="sxs-lookup"><span data-stu-id="f73bc-111">PARAMETERS</span></span>

### <span data-ttu-id="f73bc-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f73bc-112">-ClusterName</span></span>
<span data-ttu-id="f73bc-113">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="f73bc-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f73bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f73bc-114">-DefaultProfile</span></span>
<span data-ttu-id="f73bc-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f73bc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f73bc-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="f73bc-116">-HttpCredential</span></span>
<span data-ttu-id="f73bc-117">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="f73bc-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f73bc-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="f73bc-118">-JobDefinition</span></span>
<span data-ttu-id="f73bc-119">指定要從 Azure HDInsight 群集上開始的工作。</span><span class="sxs-lookup"><span data-stu-id="f73bc-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f73bc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f73bc-120">-ResourceGroupName</span></span>
<span data-ttu-id="f73bc-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f73bc-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f73bc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f73bc-122">CommonParameters</span></span>
<span data-ttu-id="f73bc-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f73bc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f73bc-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f73bc-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f73bc-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f73bc-125">INPUTS</span></span>

### <span data-ttu-id="f73bc-126">AzureHDInsightJobDefinition （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="f73bc-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="f73bc-127">輸出</span><span class="sxs-lookup"><span data-stu-id="f73bc-127">OUTPUTS</span></span>

### <span data-ttu-id="f73bc-128">AzureHDInsightJob （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="f73bc-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="f73bc-129">筆記</span><span class="sxs-lookup"><span data-stu-id="f73bc-129">NOTES</span></span>

## <span data-ttu-id="f73bc-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="f73bc-130">RELATED LINKS</span></span>

[<span data-ttu-id="f73bc-131">AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f73bc-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="f73bc-132">新-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f73bc-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="f73bc-133">停止 AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f73bc-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="f73bc-134">稍候-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f73bc-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)

