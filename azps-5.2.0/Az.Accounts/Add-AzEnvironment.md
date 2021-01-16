---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 92a8c816f1c5a76b0f3725b70a627b798b9de2b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274935"
---
# <span data-ttu-id="1de1b-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1de1b-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="1de1b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1de1b-102">SYNOPSIS</span></span>
<span data-ttu-id="1de1b-103">新增 Azure 資源管理員實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="1de1b-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="1de1b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1de1b-104">SYNTAX</span></span>

### <span data-ttu-id="1de1b-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="1de1b-105">Name (Default)</span></span>
```
Add-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>]
 [-AzureAnalysisServicesEndpointResourceId <String>] [-AzureAttestationServiceEndpointSuffix <String>]
 [-AzureAttestationServiceEndpointResourceId <String>] [-AzureSynapseAnalyticsEndpointSuffix <String>]
 [-ContainerRegistryEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1de1b-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="1de1b-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-ContainerRegistryEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1de1b-107">搜索</span><span class="sxs-lookup"><span data-stu-id="1de1b-107">Discovery</span></span>
```
Add-AzEnvironment [-AutoDiscover] [-Uri <Uri>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1de1b-108">說明</span><span class="sxs-lookup"><span data-stu-id="1de1b-108">DESCRIPTION</span></span>
<span data-ttu-id="1de1b-109">Add-AzEnvironment Cmdlet 會新增端點和中繼資料，以啟用 Azure 資源管理器 Cmdlet 與新的 Azure 資源管理器實例連線。</span><span class="sxs-lookup"><span data-stu-id="1de1b-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="1de1b-110">內建的環境 AzureCloud 和 AzureChinaCloud 會以現有的 Azure 資源管理器公用實例為目標。</span><span class="sxs-lookup"><span data-stu-id="1de1b-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="1de1b-111">示例</span><span class="sxs-lookup"><span data-stu-id="1de1b-111">EXAMPLES</span></span>

### <span data-ttu-id="1de1b-112">範例1：建立及修改新的環境</span><span class="sxs-lookup"><span data-stu-id="1de1b-112">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint NewTestADEndpoint `
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
OnPremise                                         : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              :
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : NewTestADEndpoint
GraphUrl                                          : NewTestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
DataLakeEndpointResourceId                        :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
AzureOperationalInsightsEndpointResourceId        :
AzureOperationalInsightsEndpoint                  :
AzureAnalysisServicesEndpointSuffix               :
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :
```

<span data-ttu-id="1de1b-113">在這個範例中，我們會使用 [載入 AzEnvironment] 來建立含範例端點的新 Azure 環境，然後使用 Cmdlet Set-AzEnvironment 變更已建立之環境的 ActiveDirectoryEndpoint 和 GraphEndpoint 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1de1b-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="1de1b-114">範例2：透過 Uri 探索新的環境</span><span class="sxs-lookup"><span data-stu-id="1de1b-114">Example 2: Discovering a new environment via Uri</span></span>
```
<#
Uri https://configuredmetadata.net returns an array of environment metadata. The following example contains a payload for the AzureCloud default environment.

[
  {
    "portal": "https://portal.azure.com",
    "authentication": {
      "loginEndpoint": "https://login.microsoftonline.com/",
      "audiences": [
        "https://management.core.windows.net/"
      ],
      "tenant": "common",
      "identityProvider": "AAD"
    },
    "media": "https://rest.media.azure.net",
    "graphAudience": "https://graph.windows.net/",
    "graph": "https://graph.windows.net/",
    "name": "AzureCloud",
    "suffixes": {
      "azureDataLakeStoreFileSystem": "azuredatalakestore.net",
      "acrLoginServer": "azurecr.io",
      "sqlServerHostname": ".database.windows.net",
      "azureDataLakeAnalyticsCatalogAndJob": "azuredatalakeanalytics.net",
      "keyVaultDns": "vault.azure.net",
      "storage": "core.windows.net",
      "azureFrontDoorEndpointSuffix": "azurefd.net"
    },
    "batch": "https://batch.core.windows.net/",
    "resourceManager": "https://management.azure.com/",
    "vmImageAliasDoc": "https://raw.githubusercontent.com/Azure/azure-rest-api-specs/master/arm-compute/quickstart-templates/aliases.json",
    "activeDirectoryDataLake": "https://datalake.azure.net/",
    "sqlManagement": "https://management.core.windows.net:8443/",
    "gallery": "https://gallery.azure.com/"
  },
……
]
#>

PS C:\> Add-AzEnvironment -AutoDiscover -Uri https://configuredmetadata.net

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="1de1b-115">在這個範例中，我們會從 Uri 探索新的 Azure 環境 `https://configuredmetadata.net` 。</span><span class="sxs-lookup"><span data-stu-id="1de1b-115">In this example, we are discovering a new Azure environment from the `https://configuredmetadata.net` Uri.</span></span>

## <span data-ttu-id="1de1b-116">參數</span><span class="sxs-lookup"><span data-stu-id="1de1b-116">PARAMETERS</span></span>

### <span data-ttu-id="1de1b-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="1de1b-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="1de1b-118">指定 Azure Active Directory 驗證的基本機構。</span><span class="sxs-lookup"><span data-stu-id="1de1b-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1de1b-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="1de1b-120">針對將要求傳送到 Azure 資源管理器或服務管理 (RDFE) 端點的標記指定物件。</span><span class="sxs-lookup"><span data-stu-id="1de1b-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-121">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="1de1b-121">-AdTenant</span></span>
<span data-ttu-id="1de1b-122">指定預設的 Active Directory 租使用者。</span><span class="sxs-lookup"><span data-stu-id="1de1b-122">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-123">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="1de1b-123">-ARMEndpoint</span></span>
<span data-ttu-id="1de1b-124">Azure 資源管理器端點</span><span class="sxs-lookup"><span data-stu-id="1de1b-124">The Azure Resource Manager endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-125">-自動探索</span><span class="sxs-lookup"><span data-stu-id="1de1b-125">-AutoDiscover</span></span>
<span data-ttu-id="1de1b-126">透過預設或設定的端點探索環境。</span><span class="sxs-lookup"><span data-stu-id="1de1b-126">Discovers environments via default or configured endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Discovery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1de1b-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="1de1b-128">Azure Analysis Services 資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1de1b-128">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1de1b-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="1de1b-130">與 Azure Log Analytics API 進行通訊時要使用的端點。</span><span class="sxs-lookup"><span data-stu-id="1de1b-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-131">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1de1b-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="1de1b-132">所要求權杖之收件者之 Azure 認證服務的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1de1b-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1de1b-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="1de1b-134">Azure 認證服務的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="1de1b-134">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1de1b-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="1de1b-136">Azure Data Lake Analytics 作業與目錄服務的 Dns 尾碼</span><span class="sxs-lookup"><span data-stu-id="1de1b-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1de1b-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="1de1b-138">Azure Data Lake Store FileSystem 的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="1de1b-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="1de1b-139">範例： azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="1de1b-139">Example: azuredatalake.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="1de1b-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="1de1b-141">Azure 金鑰保存庫服務的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="1de1b-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="1de1b-142">範例是 vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="1de1b-142">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1de1b-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="1de1b-144">Azure 金鑰保存庫資料服務的資源識別碼，是所要求權杖的收件者。</span><span class="sxs-lookup"><span data-stu-id="1de1b-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="1de1b-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="1de1b-146">與 Azure Log Analytics API 進行通訊時要使用的端點。</span><span class="sxs-lookup"><span data-stu-id="1de1b-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1de1b-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="1de1b-148">針對 Azure Log Analytics API 進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="1de1b-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1de1b-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="1de1b-150">所要求權杖之收件者之 Azure Synapse 分析的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1de1b-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1de1b-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="1de1b-152">Azure Synapse Analytics 的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="1de1b-152">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1de1b-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="1de1b-154">作為所請求標記之收件者之 Azure Batch 服務的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1de1b-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-155">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1de1b-155">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="1de1b-156">Azure 容器註冊的尾碼。</span><span class="sxs-lookup"><span data-stu-id="1de1b-156">Suffix of Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-157">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="1de1b-157">-DataLakeAudience</span></span>
<span data-ttu-id="1de1b-158">針對 AD Data Lake services 端點進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="1de1b-158">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1de1b-159">-DefaultProfile</span></span>
<span data-ttu-id="1de1b-160">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="1de1b-160">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1de1b-161">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="1de1b-161">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="1de1b-162">表示允許 Active Directory Federation Services (ADFS) 內部部署驗證。</span><span class="sxs-lookup"><span data-stu-id="1de1b-162">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-163">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="1de1b-163">-GalleryEndpoint</span></span>
<span data-ttu-id="1de1b-164">指定 [部署範本] 的 [Azure 資源管理器] 圖庫的端點。</span><span class="sxs-lookup"><span data-stu-id="1de1b-164">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-165">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="1de1b-165">-GraphAudience</span></span>
<span data-ttu-id="1de1b-166">使用廣告圖端點進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="1de1b-166">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-167">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="1de1b-167">-GraphEndpoint</span></span>
<span data-ttu-id="1de1b-168">指定 (Active Directory 中繼資料) 要求的圖形 URL。</span><span class="sxs-lookup"><span data-stu-id="1de1b-168">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-169">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="1de1b-169">-ManagementPortalUrl</span></span>
<span data-ttu-id="1de1b-170">指定管理入口網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="1de1b-170">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-171">-名稱</span><span class="sxs-lookup"><span data-stu-id="1de1b-171">-Name</span></span>
<span data-ttu-id="1de1b-172">指定要新增之環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="1de1b-172">Specifies the name of the environment to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-173">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="1de1b-173">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="1de1b-174">指定可從中下載 publishsettings 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="1de1b-174">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-175">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1de1b-175">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="1de1b-176">指定 Azure 資源管理員要求的 URL。</span><span class="sxs-lookup"><span data-stu-id="1de1b-176">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-177">-範圍</span><span class="sxs-lookup"><span data-stu-id="1de1b-177">-Scope</span></span>
<span data-ttu-id="1de1b-178">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="1de1b-178">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-179">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1de1b-179">-ServiceEndpoint</span></span>
<span data-ttu-id="1de1b-180">指定服務管理 (RDFE) 要求的端點。</span><span class="sxs-lookup"><span data-stu-id="1de1b-180">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-181">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="1de1b-181">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="1de1b-182">指定 Azure SQL 資料庫伺服器的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="1de1b-182">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-183">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="1de1b-183">-StorageEndpoint</span></span>
<span data-ttu-id="1de1b-184">指定儲存 (blob、資料表、佇列及檔案) 存取的端點。</span><span class="sxs-lookup"><span data-stu-id="1de1b-184">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-185">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="1de1b-185">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="1de1b-186">指定 Azure 流量管理器服務的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="1de1b-186">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-187">-Uri</span><span class="sxs-lookup"><span data-stu-id="1de1b-187">-Uri</span></span>
<span data-ttu-id="1de1b-188">指定要取得環境之網際網路資源的 URI。</span><span class="sxs-lookup"><span data-stu-id="1de1b-188">Specifies URI of the internet resource to fetch environments.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Discovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-189">-確認</span><span class="sxs-lookup"><span data-stu-id="1de1b-189">-Confirm</span></span>
<span data-ttu-id="1de1b-190">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1de1b-190">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1de1b-191">-WhatIf</span></span>
<span data-ttu-id="1de1b-192">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1de1b-192">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1de1b-193">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1de1b-193">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de1b-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1de1b-194">CommonParameters</span></span>
<span data-ttu-id="1de1b-195">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1de1b-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1de1b-196">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1de1b-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1de1b-197">輸入</span><span class="sxs-lookup"><span data-stu-id="1de1b-197">INPUTS</span></span>

### <span data-ttu-id="1de1b-198">System.object</span><span class="sxs-lookup"><span data-stu-id="1de1b-198">System.String</span></span>

### <span data-ttu-id="1de1b-199">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="1de1b-199">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1de1b-200">輸出</span><span class="sxs-lookup"><span data-stu-id="1de1b-200">OUTPUTS</span></span>

### <span data-ttu-id="1de1b-201">PSAzureEnvironment 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="1de1b-201">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="1de1b-202">筆記</span><span class="sxs-lookup"><span data-stu-id="1de1b-202">NOTES</span></span>

## <span data-ttu-id="1de1b-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="1de1b-203">RELATED LINKS</span></span>

[<span data-ttu-id="1de1b-204">AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1de1b-204">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="1de1b-205">移除-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1de1b-205">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="1de1b-206">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1de1b-206">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)
