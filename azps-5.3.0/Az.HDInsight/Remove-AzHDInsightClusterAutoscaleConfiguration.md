---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1dbfc382b935a9cc14dc42f85653a337f82ece38
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438287"
---
# <span data-ttu-id="a2949-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2949-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="a2949-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2949-102">SYNOPSIS</span></span>
<span data-ttu-id="a2949-103">移除 HDInsight 群集的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="a2949-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="a2949-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2949-104">SYNTAX</span></span>

### <span data-ttu-id="a2949-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a2949-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2949-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2949-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2949-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2949-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2949-108">說明</span><span class="sxs-lookup"><span data-stu-id="a2949-108">DESCRIPTION</span></span>
<span data-ttu-id="a2949-109">**AzHDInsightClusterAutoscaleConfiguration** Cmdlet 會移除 HDInsight 群集的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="a2949-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="a2949-110">示例</span><span class="sxs-lookup"><span data-stu-id="a2949-110">EXAMPLES</span></span>

### <span data-ttu-id="a2949-111">範例1：移除 HDInsight 群集的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="a2949-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="a2949-112">這個命令會移除 HDInsight 群集的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="a2949-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="a2949-113">參數</span><span class="sxs-lookup"><span data-stu-id="a2949-113">PARAMETERS</span></span>

### <span data-ttu-id="a2949-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2949-114">-AsJob</span></span>
<span data-ttu-id="a2949-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a2949-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2949-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a2949-116">-ClusterName</span></span>
<span data-ttu-id="a2949-117">取得或設定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2949-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2949-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2949-118">-DefaultProfile</span></span>
<span data-ttu-id="a2949-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2949-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2949-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2949-120">-InputObject</span></span>
<span data-ttu-id="a2949-121">取得或設定輸入物件。</span><span class="sxs-lookup"><span data-stu-id="a2949-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2949-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2949-122">-ResourceGroupName</span></span>
<span data-ttu-id="a2949-123">取得或設定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2949-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2949-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2949-124">-ResourceId</span></span>
<span data-ttu-id="a2949-125">取得或設定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2949-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2949-126">-確認</span><span class="sxs-lookup"><span data-stu-id="a2949-126">-Confirm</span></span>
<span data-ttu-id="a2949-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a2949-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2949-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2949-128">-WhatIf</span></span>
<span data-ttu-id="a2949-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2949-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2949-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2949-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2949-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2949-131">CommonParameters</span></span>
<span data-ttu-id="a2949-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2949-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2949-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a2949-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2949-134">輸入</span><span class="sxs-lookup"><span data-stu-id="a2949-134">INPUTS</span></span>

### <span data-ttu-id="a2949-135">System.object</span><span class="sxs-lookup"><span data-stu-id="a2949-135">System.String</span></span>

### <span data-ttu-id="a2949-136">AzureHDInsightCluster （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="a2949-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="a2949-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a2949-137">OUTPUTS</span></span>

### <span data-ttu-id="a2949-138">System.object</span><span class="sxs-lookup"><span data-stu-id="a2949-138">System.Boolean</span></span>

## <span data-ttu-id="a2949-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a2949-139">NOTES</span></span>

## <span data-ttu-id="a2949-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2949-140">RELATED LINKS</span></span>

<span data-ttu-id="a2949-141">[新-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
[AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a2949-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>