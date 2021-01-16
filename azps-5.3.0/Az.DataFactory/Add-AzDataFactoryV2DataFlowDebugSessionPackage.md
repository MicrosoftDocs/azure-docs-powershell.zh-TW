---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2dataflowdebugsessionpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
ms.openlocfilehash: c319ee7fba1bddff8e93e56601c623658094253d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439560"
---
# <span data-ttu-id="10de2-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="10de2-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>

## <span data-ttu-id="10de2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10de2-102">SYNOPSIS</span></span>
<span data-ttu-id="10de2-103">在特定的資料流程調試會話中，新增資料流程資源及其相依性。</span><span class="sxs-lookup"><span data-stu-id="10de2-103">Add data flow resource and its dependencies into specific data flow debug session.</span></span>

## <span data-ttu-id="10de2-104">句法</span><span class="sxs-lookup"><span data-stu-id="10de2-104">SYNTAX</span></span>

### <span data-ttu-id="10de2-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="10de2-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10de2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="10de2-106">ByFactoryObject</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10de2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="10de2-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10de2-108">說明</span><span class="sxs-lookup"><span data-stu-id="10de2-108">DESCRIPTION</span></span>
<span data-ttu-id="10de2-109">這個命令會將資料流程資源及其相依性附加到特定的調試會話：資料流程調試工作流程的 PowerShell 命令序列應該是：</span><span class="sxs-lookup"><span data-stu-id="10de2-109">This command attaches data flow resource and its dependencies to the specific debug session The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="10de2-110">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="10de2-110">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="10de2-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="10de2-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="10de2-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (針對不同的命令/目標重複這個步驟，或重複步驟2-3 來變更套件檔案) </span><span class="sxs-lookup"><span data-stu-id="10de2-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="10de2-113">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="10de2-113">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="10de2-114">示例</span><span class="sxs-lookup"><span data-stu-id="10de2-114">EXAMPLES</span></span>

### <span data-ttu-id="10de2-115">範例1</span><span class="sxs-lookup"><span data-stu-id="10de2-115">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Add-AzDataFactoryV2DataFlowDebugSessionPackage -ResourceGroupName adf -DataFactoryName WikiADF -PackageFile "D:\dataflowps\addpackage.json" -SessionId 550effe4-93a3-485c-8525-eaf25259efbd
```

<span data-ttu-id="10de2-116">將資料流程封裝新增至調試會話 "550effe4-93a3-485c-8525-eaf25259efbd" 的 "WikiADF" 資料工廠中。</span><span class="sxs-lookup"><span data-stu-id="10de2-116">Add data flow package into debug session "550effe4-93a3-485c-8525-eaf25259efbd" of "WikiADF" data factory.</span></span>
<span data-ttu-id="10de2-117">Pakcage 檔案包含資料流程程調試資源、資料集調試資源清單、連結服務調試資源清單、調試設定和會話 ID。</span><span class="sxs-lookup"><span data-stu-id="10de2-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span></span> <span data-ttu-id="10de2-118">例如：</span><span class="sxs-lookup"><span data-stu-id="10de2-118">For instance:</span></span>

<span data-ttu-id="10de2-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource (output (\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t) ,\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": " \\ ", "firstRowAsHeader": true, "quoteChar": " \" " }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=HTTPs;AccountName = name;AccountKey = key;EndpointSuffix = core. net "}}}]，" Debugsettings.isoverdrawheatmapenabled "： {" sourceSettings "： [{" "：" source1 "，" rowLimit "： 1000}"}，"sessionId"： "4f988caf-e765-47d2-82cd-430334a6b135"}</span><span class="sxs-lookup"><span data-stu-id="10de2-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": "\\", "firstRowAsHeader": true, "quoteChar": "\"" }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span></span>

<span data-ttu-id="10de2-120">SessionID 參數是用來取代封裝檔案中現有的 sessionId 屬性。</span><span class="sxs-lookup"><span data-stu-id="10de2-120">SessionID parameter is used to replace the existing sessionId property in the package file.</span></span>

## <span data-ttu-id="10de2-121">參數</span><span class="sxs-lookup"><span data-stu-id="10de2-121">PARAMETERS</span></span>

### <span data-ttu-id="10de2-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="10de2-122">-DataFactory</span></span>
<span data-ttu-id="10de2-123">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="10de2-123">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10de2-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="10de2-124">-DataFactoryName</span></span>
<span data-ttu-id="10de2-125">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="10de2-125">The data factory name.</span></span>

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

### <span data-ttu-id="10de2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10de2-126">-DefaultProfile</span></span>
<span data-ttu-id="10de2-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10de2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10de2-128">-PackageFile</span><span class="sxs-lookup"><span data-stu-id="10de2-128">-PackageFile</span></span>
<span data-ttu-id="10de2-129">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="10de2-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10de2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10de2-130">-PassThru</span></span>
<span data-ttu-id="10de2-131">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="10de2-131">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="10de2-132">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="10de2-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="10de2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10de2-133">-ResourceGroupName</span></span>
<span data-ttu-id="10de2-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="10de2-134">The resource group name.</span></span>

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

### <span data-ttu-id="10de2-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10de2-135">-ResourceId</span></span>
<span data-ttu-id="10de2-136">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="10de2-136">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10de2-137">-確認</span><span class="sxs-lookup"><span data-stu-id="10de2-137">-Confirm</span></span>
<span data-ttu-id="10de2-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10de2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10de2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10de2-139">-WhatIf</span></span>
<span data-ttu-id="10de2-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10de2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10de2-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10de2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10de2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10de2-142">CommonParameters</span></span>
<span data-ttu-id="10de2-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10de2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10de2-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="10de2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10de2-145">輸入</span><span class="sxs-lookup"><span data-stu-id="10de2-145">INPUTS</span></span>

### <span data-ttu-id="10de2-146">System.object</span><span class="sxs-lookup"><span data-stu-id="10de2-146">System.String</span></span>

### <span data-ttu-id="10de2-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="10de2-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="10de2-148">輸出</span><span class="sxs-lookup"><span data-stu-id="10de2-148">OUTPUTS</span></span>

### <span data-ttu-id="10de2-149">System.void</span><span class="sxs-lookup"><span data-stu-id="10de2-149">System.Void</span></span>

### <span data-ttu-id="10de2-150">System.object</span><span class="sxs-lookup"><span data-stu-id="10de2-150">System.Boolean</span></span>

## <span data-ttu-id="10de2-151">筆記</span><span class="sxs-lookup"><span data-stu-id="10de2-151">NOTES</span></span>
<span data-ttu-id="10de2-152">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="10de2-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="10de2-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="10de2-153">RELATED LINKS</span></span>

[<span data-ttu-id="10de2-154">開始-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="10de2-154">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="10de2-155">AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="10de2-155">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="10de2-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="10de2-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="10de2-157">停止 AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="10de2-157">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)