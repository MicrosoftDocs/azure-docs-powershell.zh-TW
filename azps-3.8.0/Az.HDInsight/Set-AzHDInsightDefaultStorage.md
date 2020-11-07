---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: e4ecdb86d3c8b055f76303af5c3b86fc9813e167
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797706"
---
# <span data-ttu-id="c0db1-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="c0db1-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="c0db1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0db1-102">SYNOPSIS</span></span>
<span data-ttu-id="c0db1-103">在群集設定物件中設定預設儲存空間帳戶設定。</span><span class="sxs-lookup"><span data-stu-id="c0db1-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="c0db1-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0db1-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0db1-105">說明</span><span class="sxs-lookup"><span data-stu-id="c0db1-105">DESCRIPTION</span></span>
<span data-ttu-id="c0db1-106">**AzHDInsightDefaultStorage** Cmdlet 會在由 New-AzHDInsightClusterConfig Cmdlet 建立的 Azure HDInsight 群集設定物件中，設定預設儲存空間帳戶設定。</span><span class="sxs-lookup"><span data-stu-id="c0db1-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="c0db1-107">示例</span><span class="sxs-lookup"><span data-stu-id="c0db1-107">EXAMPLES</span></span>

### <span data-ttu-id="c0db1-108">範例1：設定 [群集] 設定物件的預設儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="c0db1-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Set-AzHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="c0db1-109">這個命令會設定群集設定物件的預設儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c0db1-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="c0db1-110">參數</span><span class="sxs-lookup"><span data-stu-id="c0db1-110">PARAMETERS</span></span>

### <span data-ttu-id="c0db1-111">-Config</span><span class="sxs-lookup"><span data-stu-id="c0db1-111">-Config</span></span>
<span data-ttu-id="c0db1-112">指定此 Cmdlet 修改的 HDInsight 群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="c0db1-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="c0db1-113">這個物件是由 **新的-AzHDInsightClusterConfig** Cmdlet 建立的。</span><span class="sxs-lookup"><span data-stu-id="c0db1-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="c0db1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0db1-114">-DefaultProfile</span></span>
<span data-ttu-id="c0db1-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c0db1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0db1-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c0db1-116">-StorageAccountKey</span></span>
<span data-ttu-id="c0db1-117">指定 HDInsight 群集將使用的預設 Azure 儲存空間帳戶的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="c0db1-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0db1-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c0db1-118">-StorageAccountName</span></span>
<span data-ttu-id="c0db1-119">指定 HDInsight 群集將使用的預設儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c0db1-119">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0db1-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c0db1-120">-StorageAccountType</span></span>
<span data-ttu-id="c0db1-121">取得或設定預設儲存空間帳戶的類型。</span><span class="sxs-lookup"><span data-stu-id="c0db1-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="c0db1-122">預設為 AzureStorage</span><span class="sxs-lookup"><span data-stu-id="c0db1-122">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0db1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0db1-123">CommonParameters</span></span>
<span data-ttu-id="c0db1-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0db1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0db1-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0db1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0db1-126">輸入</span><span class="sxs-lookup"><span data-stu-id="c0db1-126">INPUTS</span></span>

### <span data-ttu-id="c0db1-127">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="c0db1-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c0db1-128">輸出</span><span class="sxs-lookup"><span data-stu-id="c0db1-128">OUTPUTS</span></span>

### <span data-ttu-id="c0db1-129">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="c0db1-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c0db1-130">筆記</span><span class="sxs-lookup"><span data-stu-id="c0db1-130">NOTES</span></span>

## <span data-ttu-id="c0db1-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0db1-131">RELATED LINKS</span></span>