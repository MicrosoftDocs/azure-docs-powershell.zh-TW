---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
ms.openlocfilehash: ab58d679e9fc3ad62baeded8622b81a0cb8b2f95
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438108"
---
# <span data-ttu-id="380ba-101">New-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="380ba-101">New-AzKustoDataConnection</span></span>

## <span data-ttu-id="380ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="380ba-102">SYNOPSIS</span></span>
<span data-ttu-id="380ba-103">建立或更新資料連線。</span><span class="sxs-lookup"><span data-stu-id="380ba-103">Creates or updates a data connection.</span></span>

## <span data-ttu-id="380ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="380ba-104">SYNTAX</span></span>

### <span data-ttu-id="380ba-105">CreateExpandedEventHub (預設) </span><span class="sxs-lookup"><span data-stu-id="380ba-105">CreateExpandedEventHub (Default)</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="380ba-106">CreateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="380ba-106">CreateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="380ba-107">CreateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="380ba-107">CreateExpandedIotHub</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="380ba-108">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="380ba-108">UpdateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="380ba-109">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="380ba-109">UpdateViaIdentityExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="380ba-110">說明</span><span class="sxs-lookup"><span data-stu-id="380ba-110">DESCRIPTION</span></span>
<span data-ttu-id="380ba-111">建立或更新資料連線。</span><span class="sxs-lookup"><span data-stu-id="380ba-111">Creates or updates a data connection.</span></span>

## <span data-ttu-id="380ba-112">示例</span><span class="sxs-lookup"><span data-stu-id="380ba-112">EXAMPLES</span></span>

### <span data-ttu-id="380ba-113">範例1：建立新的 EventHub 資料連線</span><span class="sxs-lookup"><span data-stu-id="380ba-113">Example 1: Create a new EventHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "EventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="380ba-114">上述命令會針對群集 "testnewkustocluster" 中的資料庫 "mykustodatabase" 建立名為 "myeventhubdc" 的新 EventHub 資料連線。</span><span class="sxs-lookup"><span data-stu-id="380ba-114">The above command creates a new EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="380ba-115">範例2：建立新的 EventGrid 資料連線</span><span class="sxs-lookup"><span data-stu-id="380ba-115">Example 2: Create a new EventGrid data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping" -IgnoreFirstRecord "false" -BlobStorageEventType "Microsoft.Storage.BlobRenamed"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="380ba-116">上述命令會針對群集 "testnewkustocluster" 中的資料庫 "mykustodatabase" 建立名為 "myeventgriddc" 的新 EventGrid 資料連線。</span><span class="sxs-lookup"><span data-stu-id="380ba-116">The above command creates a new EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="380ba-117">範例3：建立新的 IotHub 資料連線</span><span class="sxs-lookup"><span data-stu-id="380ba-117">Example 3: Create a new IotHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="380ba-118">上述命令會針對群集 "testnewkustocluster" 中的資料庫 "mykustodatabase" 建立名為 "myiothubdc" 的新 IotHub 資料連線。</span><span class="sxs-lookup"><span data-stu-id="380ba-118">The above command creates a new IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="380ba-119">參數</span><span class="sxs-lookup"><span data-stu-id="380ba-119">PARAMETERS</span></span>

### <span data-ttu-id="380ba-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="380ba-120">-AsJob</span></span>
<span data-ttu-id="380ba-121">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="380ba-121">Run the command as a job</span></span>

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

### <span data-ttu-id="380ba-122">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="380ba-122">-BlobStorageEventType</span></span>
<span data-ttu-id="380ba-123">要處理之 blob 儲存事件種類的名稱。</span><span class="sxs-lookup"><span data-stu-id="380ba-123">The name of blob storage event type to process.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.BlobStorageEventType
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-124">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="380ba-124">-ClusterName</span></span>
<span data-ttu-id="380ba-125">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="380ba-125">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-126">壓縮</span><span class="sxs-lookup"><span data-stu-id="380ba-126">-Compression</span></span>
<span data-ttu-id="380ba-127">事件中心訊息壓縮類型。</span><span class="sxs-lookup"><span data-stu-id="380ba-127">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: CreateExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-128">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="380ba-128">-ConsumerGroup</span></span>
<span data-ttu-id="380ba-129">[事件/iot 中心消費者] 群組。</span><span class="sxs-lookup"><span data-stu-id="380ba-129">The event/iot hub consumer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="380ba-130">-DatabaseName</span></span>
<span data-ttu-id="380ba-131">Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="380ba-131">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-132">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="380ba-132">-DataFormat</span></span>
<span data-ttu-id="380ba-133">郵件的資料格式。</span><span class="sxs-lookup"><span data-stu-id="380ba-133">The data format of the message.</span></span>
<span data-ttu-id="380ba-134">或者，您也可以在每封郵件中新增資料格式。</span><span class="sxs-lookup"><span data-stu-id="380ba-134">Optionally the data format can be added to each message.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EventGridDataFormat
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="380ba-135">-DefaultProfile</span></span>
<span data-ttu-id="380ba-136">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="380ba-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-137">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="380ba-137">-EventHubResourceId</span></span>
<span data-ttu-id="380ba-138">要用來建立資料連線/事件格線之事件中心的資源識別碼已設定為傳送事件。</span><span class="sxs-lookup"><span data-stu-id="380ba-138">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid, CreateExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-139">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="380ba-139">-EventSystemProperty</span></span>
<span data-ttu-id="380ba-140">事件/iot 中心的系統屬性。</span><span class="sxs-lookup"><span data-stu-id="380ba-140">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpandedEventHub, CreateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-141">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="380ba-141">-IgnoreFirstRecord</span></span>
<span data-ttu-id="380ba-142">如果設為 true，則表示攝取應該忽略每個檔案的第一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="380ba-142">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-143">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="380ba-143">-IotHubResourceId</span></span>
<span data-ttu-id="380ba-144">要用來建立資料連線之 Iot 中樞的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="380ba-144">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-145">類型</span><span class="sxs-lookup"><span data-stu-id="380ba-145">-Kind</span></span>
<span data-ttu-id="380ba-146">資料連線的端點類型</span><span class="sxs-lookup"><span data-stu-id="380ba-146">Kind of the endpoint for the data connection</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-147">-位置</span><span class="sxs-lookup"><span data-stu-id="380ba-147">-Location</span></span>
<span data-ttu-id="380ba-148">資源位置。</span><span class="sxs-lookup"><span data-stu-id="380ba-148">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-149">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="380ba-149">-MappingRuleName</span></span>
<span data-ttu-id="380ba-150">要用來攝取資料的對應規則。</span><span class="sxs-lookup"><span data-stu-id="380ba-150">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="380ba-151">或者，您也可以將對應資訊新增到每一封郵件。</span><span class="sxs-lookup"><span data-stu-id="380ba-151">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="380ba-152">-名稱</span><span class="sxs-lookup"><span data-stu-id="380ba-152">-Name</span></span>
<span data-ttu-id="380ba-153">資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="380ba-153">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-154">-NoWait</span><span class="sxs-lookup"><span data-stu-id="380ba-154">-NoWait</span></span>
<span data-ttu-id="380ba-155">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="380ba-155">Run the command asynchronously</span></span>

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

### <span data-ttu-id="380ba-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="380ba-156">-ResourceGroupName</span></span>
<span data-ttu-id="380ba-157">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="380ba-157">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-158">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="380ba-158">-SharedAccessPolicyName</span></span>
<span data-ttu-id="380ba-159">共用訪問原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="380ba-159">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="380ba-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="380ba-161">資料所在之儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="380ba-161">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="380ba-162">-SubscriptionId</span></span>
<span data-ttu-id="380ba-163">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="380ba-163">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="380ba-164">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="380ba-164">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ba-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="380ba-165">-TableName</span></span>
<span data-ttu-id="380ba-166">要 ingested 資料的資料表。</span><span class="sxs-lookup"><span data-stu-id="380ba-166">The table where the data should be ingested.</span></span>
<span data-ttu-id="380ba-167">或者，您也可以在每封郵件中新增表格資訊。</span><span class="sxs-lookup"><span data-stu-id="380ba-167">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="380ba-168">-確認</span><span class="sxs-lookup"><span data-stu-id="380ba-168">-Confirm</span></span>
<span data-ttu-id="380ba-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="380ba-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="380ba-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="380ba-170">-WhatIf</span></span>
<span data-ttu-id="380ba-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="380ba-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="380ba-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="380ba-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="380ba-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="380ba-173">CommonParameters</span></span>
<span data-ttu-id="380ba-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="380ba-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="380ba-175">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="380ba-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="380ba-176">輸入</span><span class="sxs-lookup"><span data-stu-id="380ba-176">INPUTS</span></span>

## <span data-ttu-id="380ba-177">輸出</span><span class="sxs-lookup"><span data-stu-id="380ba-177">OUTPUTS</span></span>

### <span data-ttu-id="380ba-178">IDataConnection （Kusto）。 Api20200918。</span><span class="sxs-lookup"><span data-stu-id="380ba-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="380ba-179">筆記</span><span class="sxs-lookup"><span data-stu-id="380ba-179">NOTES</span></span>

<span data-ttu-id="380ba-180">別名</span><span class="sxs-lookup"><span data-stu-id="380ba-180">ALIASES</span></span>

## <span data-ttu-id="380ba-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="380ba-181">RELATED LINKS</span></span>
