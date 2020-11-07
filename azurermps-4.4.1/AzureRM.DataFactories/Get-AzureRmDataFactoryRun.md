---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
ms.openlocfilehash: db3992a8df2cbd27c560827a702f9562e64ddcb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626326"
---
# <span data-ttu-id="a8220-101">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="a8220-101">Get-AzureRmDataFactoryRun</span></span>

## <span data-ttu-id="a8220-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8220-102">SYNOPSIS</span></span>
<span data-ttu-id="a8220-103">針對 Azure 資料工廠中的資料集，取得資料切片的執行。</span><span class="sxs-lookup"><span data-stu-id="a8220-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8220-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8220-104">SYNTAX</span></span>

### <span data-ttu-id="a8220-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="a8220-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8220-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a8220-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8220-107">說明</span><span class="sxs-lookup"><span data-stu-id="a8220-107">DESCRIPTION</span></span>
<span data-ttu-id="a8220-108">**AzureRmDataFactoryRun** Cmdlet 會取得 Azure 資料工廠中資料集的資料切片執行。</span><span class="sxs-lookup"><span data-stu-id="a8220-108">The **Get-AzureRmDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="a8220-109">資料工廠中的資料集是由在時間軸上的扇面組成。</span><span class="sxs-lookup"><span data-stu-id="a8220-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="a8220-110">扇面的寬度是依排程（每小時或每天）來決定。</span><span class="sxs-lookup"><span data-stu-id="a8220-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="a8220-111">Run 是切片的處理單位。</span><span class="sxs-lookup"><span data-stu-id="a8220-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="a8220-112">如果發生重試，可能會有一個或多個切片執行，或因失敗而重新執行您的切片時。</span><span class="sxs-lookup"><span data-stu-id="a8220-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="a8220-113">切片是由它的開始時間所識別。</span><span class="sxs-lookup"><span data-stu-id="a8220-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="a8220-114">若要取得扇面的開始時間，請使用 Get-AzureRmDataFactorySlice Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8220-114">To obtain the start time of a slice, use the Get-AzureRmDataFactorySlice cmdlet.</span></span>

<span data-ttu-id="a8220-115">例如，若要取得下列扇面的執行，請使用「開始時間 2015-04-02T20：00：00。</span><span class="sxs-lookup"><span data-stu-id="a8220-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>

<span data-ttu-id="a8220-116">ResourceGroupName： ADF DataFactoryName： SPDataFactory0924 DatasetName： MarketingCampaignEffectivenessBlobDataset Start： 5/2/2014 8:00:00 PM 結束： 5/3/2014 8:00:00 PM RetryCount：0狀態：就緒 LatencyStatus：</span><span class="sxs-lookup"><span data-stu-id="a8220-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="a8220-117">示例</span><span class="sxs-lookup"><span data-stu-id="a8220-117">EXAMPLES</span></span>

### <span data-ttu-id="a8220-118">範例1：取得資料集</span><span class="sxs-lookup"><span data-stu-id="a8220-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
Id                  : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ResourceGroupName   : ADF
DataFactoryName     : WikiADF
DatasetName           : DAWikiAggregatedData
PipelineName        : 249ea141-ca00-8597-fad9-a148e5e7bdba
ActivityId          : fcefe2bd-39b1-2d7a-7b35-bcc2b0432300
ResumptionToken     : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ContinuationToken   : 
ProcessingStartTime : 5/21/2014 5:02:41 PM
ProcessingEndTime   : 5/21/2014 5:04:12 PM
PercentComplete     : 100
DataSliceStart      : 5/21/2014 4:00:00 PM
DataSliceEnd        : 5/21/2014 5:00:00 PM
Status              : Succeeded
Timestamp           : 5/21/2014 5:02:41 PM
RetryAttempt        : 0
Properties          : {[errors, ]} 
ErrorMessage        :
```

<span data-ttu-id="a8220-119">這個命令會從05/21/2014 上從 4 PM GMT 開始的資料工廠中，取得名為 DAWikiAggregatedData 之資料集的所有執行。</span><span class="sxs-lookup"><span data-stu-id="a8220-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="a8220-120">參數</span><span class="sxs-lookup"><span data-stu-id="a8220-120">PARAMETERS</span></span>

### <span data-ttu-id="a8220-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a8220-121">-DataFactory</span></span>
<span data-ttu-id="a8220-122">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="a8220-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a8220-123">這個 Cmdlet 會針對屬於此參數指定之資料工廠的扇面執行。</span><span class="sxs-lookup"><span data-stu-id="a8220-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8220-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a8220-124">-DataFactoryName</span></span>
<span data-ttu-id="a8220-125">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8220-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a8220-126">這個 Cmdlet 會針對屬於此參數指定之資料工廠的扇面執行。</span><span class="sxs-lookup"><span data-stu-id="a8220-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8220-127">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="a8220-127">-DatasetName</span></span>
<span data-ttu-id="a8220-128">指定資料集的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8220-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="a8220-129">這個 Cmdlet 會針對屬於此參數指定之資料集的扇面執行。</span><span class="sxs-lookup"><span data-stu-id="a8220-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8220-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8220-130">-ResourceGroupName</span></span>
<span data-ttu-id="a8220-131">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8220-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a8220-132">這個 Cmdlet 會針對屬於此參數指定之群組的扇面取得工廠執行。</span><span class="sxs-lookup"><span data-stu-id="a8220-132">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8220-133">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="a8220-133">-StartDateTime</span></span>
<span data-ttu-id="a8220-134">指定時段的開頭作為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="a8220-134">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="a8220-135">這個 Cmdlet 會針對符合此時間範圍的資料切片執行。</span><span class="sxs-lookup"><span data-stu-id="a8220-135">This cmdlet gets runs for the data slices that match this time period.</span></span>

<span data-ttu-id="a8220-136">*StartDateTime* 必須以 ISO8601 格式指定，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="a8220-136">*StartDateTime* must be specified in the ISO8601 format, as in the following examples:</span></span> 

<span data-ttu-id="a8220-137">2015-01-01Z 2015-01-01T00：00： 00Z 2015-01-01T00：00： 00.000 Z (UTC) 2015-01-01T00：00： 00-08： 00 (太平洋標準時間) </span><span class="sxs-lookup"><span data-stu-id="a8220-137">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="a8220-138">預設時區指示符為 UTC。</span><span class="sxs-lookup"><span data-stu-id="a8220-138">The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8220-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8220-139">-DefaultProfile</span></span>
<span data-ttu-id="a8220-140">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8220-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8220-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8220-141">CommonParameters</span></span>
<span data-ttu-id="a8220-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8220-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8220-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a8220-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8220-144">輸入</span><span class="sxs-lookup"><span data-stu-id="a8220-144">INPUTS</span></span>

## <span data-ttu-id="a8220-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a8220-145">OUTPUTS</span></span>

### <span data-ttu-id="a8220-146">[System.object]。清單 ' 1 [Microsoft.WindowsAzure.Commands.Utilities.PSDataSliceRun，WindowsAzure. 實用程式，版本 = 0.8.2.0，Culture = 中性，PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a8220-146">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataSliceRun, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="a8220-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a8220-147">NOTES</span></span>
* <span data-ttu-id="a8220-148">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="a8220-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a8220-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8220-149">RELATED LINKS</span></span>

[<span data-ttu-id="a8220-150">AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="a8220-150">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)

