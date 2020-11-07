---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 4da5387d5506733ff5046fc34f43bcc003c2b8be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788177"
---
# <span data-ttu-id="21d7f-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="21d7f-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="21d7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21d7f-102">SYNOPSIS</span></span>
<span data-ttu-id="21d7f-103">取得整合執行時間節點資訊。</span><span class="sxs-lookup"><span data-stu-id="21d7f-103">Gets an integration runtime node infomation.</span></span>

## <span data-ttu-id="21d7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="21d7f-104">SYNTAX</span></span>

### <span data-ttu-id="21d7f-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="21d7f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21d7f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="21d7f-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21d7f-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="21d7f-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21d7f-108">說明</span><span class="sxs-lookup"><span data-stu-id="21d7f-108">DESCRIPTION</span></span>
<span data-ttu-id="21d7f-109">**AzDataFactoryV2IntegrationRuntimeNode** Cmdlet 會取得整合執行時間節點的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="21d7f-109">The **Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="21d7f-110">示例</span><span class="sxs-lookup"><span data-stu-id="21d7f-110">EXAMPLES</span></span>

### <span data-ttu-id="21d7f-111">範例1：取得整合執行時間節點的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="21d7f-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              :
```

<span data-ttu-id="21d7f-112">此 Cmdlet 會在資料工廠 "test-eu2" 中的自託管整合執行時間 "test-selfhost-ir" 中，取得名為「Node_1」的節點資訊。</span><span class="sxs-lookup"><span data-stu-id="21d7f-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="21d7f-113">範例2：取得整合執行時間節點的詳細資訊及 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="21d7f-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              : 167.220.1.167
```

<span data-ttu-id="21d7f-114">此 Cmdlet 會在自託管整合執行時間 "test-eu2" 中，取得名為「Node_1」的節點資訊，包括 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="21d7f-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="21d7f-115">參數</span><span class="sxs-lookup"><span data-stu-id="21d7f-115">PARAMETERS</span></span>

### <span data-ttu-id="21d7f-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="21d7f-116">-DataFactoryName</span></span>
<span data-ttu-id="21d7f-117">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="21d7f-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21d7f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d7f-118">-DefaultProfile</span></span>
<span data-ttu-id="21d7f-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21d7f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21d7f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21d7f-120">-InputObject</span></span>
<span data-ttu-id="21d7f-121">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="21d7f-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21d7f-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="21d7f-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="21d7f-123">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="21d7f-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21d7f-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="21d7f-124">-IpAddress</span></span>
<span data-ttu-id="21d7f-125">整合執行時間節點的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="21d7f-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="21d7f-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="21d7f-126">-Name</span></span>
<span data-ttu-id="21d7f-127">整合執行時間節點名稱。</span><span class="sxs-lookup"><span data-stu-id="21d7f-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="21d7f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21d7f-128">-ResourceGroupName</span></span>
<span data-ttu-id="21d7f-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="21d7f-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21d7f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21d7f-130">-ResourceId</span></span>
<span data-ttu-id="21d7f-131">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="21d7f-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21d7f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d7f-132">CommonParameters</span></span>
<span data-ttu-id="21d7f-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21d7f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d7f-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="21d7f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d7f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="21d7f-135">INPUTS</span></span>

### <span data-ttu-id="21d7f-136">System.object</span><span class="sxs-lookup"><span data-stu-id="21d7f-136">System.String</span></span>

### <span data-ttu-id="21d7f-137">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="21d7f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="21d7f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="21d7f-138">OUTPUTS</span></span>

### <span data-ttu-id="21d7f-139">PSManagedIntegrationRuntimeNode 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="21d7f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="21d7f-140">PSSelfHostedIntegrationRuntimeNode 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="21d7f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="21d7f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="21d7f-141">NOTES</span></span>
<span data-ttu-id="21d7f-142">關鍵字： azure、azurerm、arm、資源、管理、管理員、資料、工廠、複本、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="21d7f-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="21d7f-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="21d7f-143">RELATED LINKS</span></span>

[<span data-ttu-id="21d7f-144">AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="21d7f-144">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()