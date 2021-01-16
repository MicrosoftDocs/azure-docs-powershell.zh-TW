---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/stop-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
ms.openlocfilehash: d5e38cf3edb89801b630735dee1ce0dbd1d62d41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273164"
---
# <span data-ttu-id="54a84-101">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="54a84-101">Stop-AzHDInsightJob</span></span>

## <span data-ttu-id="54a84-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54a84-102">SYNOPSIS</span></span>
<span data-ttu-id="54a84-103">在群集上停止指定的執行作業。</span><span class="sxs-lookup"><span data-stu-id="54a84-103">Stops a specified running job on a cluster.</span></span>

## <span data-ttu-id="54a84-104">句法</span><span class="sxs-lookup"><span data-stu-id="54a84-104">SYNTAX</span></span>

```
Stop-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54a84-105">說明</span><span class="sxs-lookup"><span data-stu-id="54a84-105">DESCRIPTION</span></span>
<span data-ttu-id="54a84-106">**AzHDInsightJob** Cmdlet 會停止 Azure HDInsight 群集上指定的執行作業。</span><span class="sxs-lookup"><span data-stu-id="54a84-106">The **Stop-AzHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="54a84-107">示例</span><span class="sxs-lookup"><span data-stu-id="54a84-107">EXAMPLES</span></span>

### <span data-ttu-id="54a84-108">範例1：在指定的群集上停止作業</span><span class="sxs-lookup"><span data-stu-id="54a84-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="54a84-109">這個命令會停止名為-hadoop-001 的群集上的工作。</span><span class="sxs-lookup"><span data-stu-id="54a84-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="54a84-110">參數</span><span class="sxs-lookup"><span data-stu-id="54a84-110">PARAMETERS</span></span>

### <span data-ttu-id="54a84-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="54a84-111">-ClusterName</span></span>
<span data-ttu-id="54a84-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="54a84-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="54a84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54a84-113">-DefaultProfile</span></span>
<span data-ttu-id="54a84-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="54a84-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54a84-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="54a84-115">-HttpCredential</span></span>
<span data-ttu-id="54a84-116">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="54a84-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="54a84-117">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="54a84-117">-JobId</span></span>
<span data-ttu-id="54a84-118">指定作業的作業 ID。</span><span class="sxs-lookup"><span data-stu-id="54a84-118">Specifies the job ID of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54a84-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54a84-119">-ResourceGroupName</span></span>
<span data-ttu-id="54a84-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="54a84-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="54a84-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a84-121">CommonParameters</span></span>
<span data-ttu-id="54a84-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54a84-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a84-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54a84-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a84-124">輸入</span><span class="sxs-lookup"><span data-stu-id="54a84-124">INPUTS</span></span>

### <span data-ttu-id="54a84-125">System.object</span><span class="sxs-lookup"><span data-stu-id="54a84-125">System.String</span></span>

## <span data-ttu-id="54a84-126">輸出</span><span class="sxs-lookup"><span data-stu-id="54a84-126">OUTPUTS</span></span>

### <span data-ttu-id="54a84-127">AzureHDInsightJob （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="54a84-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="54a84-128">筆記</span><span class="sxs-lookup"><span data-stu-id="54a84-128">NOTES</span></span>

## <span data-ttu-id="54a84-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="54a84-129">RELATED LINKS</span></span>

[<span data-ttu-id="54a84-130">AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="54a84-130">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="54a84-131">開始-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="54a84-131">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="54a84-132">稍候-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="54a84-132">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)

