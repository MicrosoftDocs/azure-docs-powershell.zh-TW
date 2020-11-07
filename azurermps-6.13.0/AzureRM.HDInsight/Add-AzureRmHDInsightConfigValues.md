---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightconfigvalues
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
ms.openlocfilehash: dd577b5ae4aa61ff988b872bcd37eab1c911e6cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624058"
---
# <span data-ttu-id="abbf2-101">Add-AzureRmHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="abbf2-101">Add-AzureRmHDInsightConfigValues</span></span>

## <span data-ttu-id="abbf2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="abbf2-102">SYNOPSIS</span></span>
<span data-ttu-id="abbf2-103">將 Hadoop 設定值自訂和/或配置單元共用文件庫自訂新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="abbf2-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abbf2-104">句法</span><span class="sxs-lookup"><span data-stu-id="abbf2-104">SYNTAX</span></span>

### <span data-ttu-id="abbf2-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="abbf2-105">Spark1</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="abbf2-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="abbf2-106">Spark2</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="abbf2-107">說明</span><span class="sxs-lookup"><span data-stu-id="abbf2-107">DESCRIPTION</span></span>
<span data-ttu-id="abbf2-108">**AzureRmHDInsightConfigValues** Cmdlet 會將 Hadoop 設定值自訂（例如 core-site.xml 或 hive-site.xml）及/或配置單元共用文件庫自訂新增至 New-AzureRmHDInsightClusterConfig Cmdlet 建立的 HDInsight 設定物件。</span><span class="sxs-lookup"><span data-stu-id="abbf2-108">The **Add-AzureRmHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="abbf2-109">示例</span><span class="sxs-lookup"><span data-stu-id="abbf2-109">EXAMPLES</span></span>

### <span data-ttu-id="abbf2-110">範例1：將自訂設定值新增至 [群集設定] 物件</span><span class="sxs-lookup"><span data-stu-id="abbf2-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightConfigValues `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="abbf2-111">這個命令會將 Hadoop 設定值新增到名為 [hadoop-001] 的群集中。</span><span class="sxs-lookup"><span data-stu-id="abbf2-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="abbf2-112">參數</span><span class="sxs-lookup"><span data-stu-id="abbf2-112">PARAMETERS</span></span>

### <span data-ttu-id="abbf2-113">-Config</span><span class="sxs-lookup"><span data-stu-id="abbf2-113">-Config</span></span>
<span data-ttu-id="abbf2-114">指定此 Cmdlet 修改的 HDInsight 群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="abbf2-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="abbf2-115">這個物件是由 New-AzureRmHDInsightClusterConfig Cmdlet 建立的。</span><span class="sxs-lookup"><span data-stu-id="abbf2-115">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-116">核心</span><span class="sxs-lookup"><span data-stu-id="abbf2-116">-Core</span></span>
<span data-ttu-id="abbf2-117">指定此 HDInsight 群集的核心網站設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abbf2-118">-DefaultProfile</span></span>
<span data-ttu-id="abbf2-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="abbf2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abbf2-120">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="abbf2-120">-HBaseEnv</span></span>
<span data-ttu-id="abbf2-121">指定此 HDInsight 群集的 HBase 配置。</span><span class="sxs-lookup"><span data-stu-id="abbf2-121">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-122">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="abbf2-122">-HBaseSite</span></span>
<span data-ttu-id="abbf2-123">指定此 HDInsight 群集的 HBase 網站設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-123">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-124">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="abbf2-124">-Hdfs</span></span>
<span data-ttu-id="abbf2-125">指定此 HDInsight 群集的 HDFS 設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-125">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-126">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="abbf2-126">-HiveEnv</span></span>
<span data-ttu-id="abbf2-127">指定此 HDInsight 群集的 Hive 配置環境設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-127">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-128">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="abbf2-128">-HiveSite</span></span>
<span data-ttu-id="abbf2-129">指定此 HDInsight 群集的 Hive 網站設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-129">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-130">-MapRed</span><span class="sxs-lookup"><span data-stu-id="abbf2-130">-MapRed</span></span>
<span data-ttu-id="abbf2-131">指定此 HDInsight 群集的 MapRed 網站設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-131">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-132">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="abbf2-132">-OozieEnv</span></span>
<span data-ttu-id="abbf2-133">指定此 HDInsight 群集的 Oozie 環境設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-133">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-134">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="abbf2-134">-OozieSite</span></span>
<span data-ttu-id="abbf2-135">指定此 HDInsight 群集的 Oozie 網站設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-135">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-136">-RServer</span><span class="sxs-lookup"><span data-stu-id="abbf2-136">-RServer</span></span>
<span data-ttu-id="abbf2-137">指定 RServer 設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-137">Specifies the RServer configurations.</span></span> <span data-ttu-id="abbf2-138">僅對 RServer 群集有效。</span><span class="sxs-lookup"><span data-stu-id="abbf2-138">Valid only for RServer clusters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-139">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="abbf2-139">-Spark2Defaults</span></span>
<span data-ttu-id="abbf2-140">指定此 HDInsight 群集的 Spark2 預設設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-140">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-141">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="abbf2-141">-Spark2ThriftConf</span></span>
<span data-ttu-id="abbf2-142">指定此 HDInsight 群集的 Spark2 Thrift SparkConf 設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-142">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-143">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="abbf2-143">-SparkDefaults</span></span>
<span data-ttu-id="abbf2-144">指定此 HDInsight 群集的 Spark 預設設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-144">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-145">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="abbf2-145">-SparkThriftConf</span></span>
<span data-ttu-id="abbf2-146">指定此 HDInsight 群集的 Spark Thrift SparkConf 設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-146">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-147">-風暴</span><span class="sxs-lookup"><span data-stu-id="abbf2-147">-Storm</span></span>
<span data-ttu-id="abbf2-148">指定此 HDInsight 群集的風暴網站設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-148">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-149">-Tez</span><span class="sxs-lookup"><span data-stu-id="abbf2-149">-Tez</span></span>
<span data-ttu-id="abbf2-150">指定此 HDInsight 群集的 Tez 網站設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-150">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-151">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="abbf2-151">-WebHCat</span></span>
<span data-ttu-id="abbf2-152">指定此 HDInsight 群集的 WebHCat 網站設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-152">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-153">-Yarn</span><span class="sxs-lookup"><span data-stu-id="abbf2-153">-Yarn</span></span>
<span data-ttu-id="abbf2-154">指定此 HDInsight 群集的 YARN 網站設定。</span><span class="sxs-lookup"><span data-stu-id="abbf2-154">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbf2-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abbf2-155">CommonParameters</span></span>
<span data-ttu-id="abbf2-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="abbf2-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abbf2-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="abbf2-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abbf2-158">輸入</span><span class="sxs-lookup"><span data-stu-id="abbf2-158">INPUTS</span></span>

### <span data-ttu-id="abbf2-159">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="abbf2-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="abbf2-160">參數： Config (ByValue) </span><span class="sxs-lookup"><span data-stu-id="abbf2-160">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="abbf2-161">輸出</span><span class="sxs-lookup"><span data-stu-id="abbf2-161">OUTPUTS</span></span>

### <span data-ttu-id="abbf2-162">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="abbf2-162">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="abbf2-163">筆記</span><span class="sxs-lookup"><span data-stu-id="abbf2-163">NOTES</span></span>

## <span data-ttu-id="abbf2-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="abbf2-164">RELATED LINKS</span></span>

[<span data-ttu-id="abbf2-165">新-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="abbf2-165">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

