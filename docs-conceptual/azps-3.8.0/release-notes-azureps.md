---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a9c5394a5fac8a8a3de96925b3563776783ea9fe
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/05/2020
ms.locfileid: "82080193"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="738ee-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="738ee-103">Azure PowerShell release notes</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="738ee-104">3.8.0 - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="738ee-104">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="738ee-105">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="738ee-105">Highlights since the last release</span></span>
* <span data-ttu-id="738ee-106">Az.Storage 支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="738ee-106">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="738ee-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-107">Az.Accounts</span></span>
* <span data-ttu-id="738ee-108">更新 'Resolve-AzError' 中的 Azure PowerShell 問卷 URL [#11507]</span><span class="sxs-lookup"><span data-stu-id="738ee-108">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="738ee-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="738ee-109">Az.ApiManagement</span></span>
* <span data-ttu-id="738ee-110">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="738ee-110">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="738ee-111">'Set-AzApiManagementGroup' 已更新文件以指定 GroupId 參數</span><span class="sxs-lookup"><span data-stu-id="738ee-111">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="738ee-112">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="738ee-112">Az.Cdn</span></span>
* <span data-ttu-id="738ee-113">已修正 ChinaCDN 相關的定價 SKU 顯示</span><span class="sxs-lookup"><span data-stu-id="738ee-113">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="738ee-114">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="738ee-114">Az.CognitiveServices</span></span>
* <span data-ttu-id="738ee-115">支援身分識別、加密、UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="738ee-115">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-116">Az.Compute</span></span>
* <span data-ttu-id="738ee-117">已新增 'Set-AzVmssOrchestrationServiceState' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="738ee-117">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="738ee-118">具有 -InstanceView 的 'Get-AzVmss' 會顯示 OrchestrationService 狀態。</span><span class="sxs-lookup"><span data-stu-id="738ee-118">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="738ee-119">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="738ee-119">Az.IotHub</span></span>
* <span data-ttu-id="738ee-120">管理 IoT 裝置對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="738ee-120">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="738ee-121">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="738ee-121">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="738ee-122">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="738ee-122">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="738ee-123">已新增 Cmdlet，可在 IoT 中樞的裝置上叫用直接方法。</span><span class="sxs-lookup"><span data-stu-id="738ee-123">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="738ee-124">管理 IoT 裝置模組對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="738ee-124">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="738ee-125">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="738ee-125">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="738ee-126">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="738ee-126">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="738ee-127">大規模管理 IoT 自動裝置管理設定。</span><span class="sxs-lookup"><span data-stu-id="738ee-127">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="738ee-128">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="738ee-128">New cmdlets are:</span></span>
    - <span data-ttu-id="738ee-129">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="738ee-129">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="738ee-130">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="738ee-130">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="738ee-131">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="738ee-131">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="738ee-132">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="738ee-132">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="738ee-133">已新增 Cmdlet，叫用 IoT 中樞的邊緣模組方法。</span><span class="sxs-lookup"><span data-stu-id="738ee-133">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="738ee-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="738ee-134">Az.KeyVault</span></span>
* <span data-ttu-id="738ee-135">已新增可在保存庫上啟用虛刪除和清除保護的新 Cmdlet 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="738ee-135">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="738ee-136">已將支援新增至 Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="738ee-136">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="738ee-137">已修正 'Remove-AzKeyVaultManagedStorageSasDefinition' 範例中的錯誤 [#11479]</span><span class="sxs-lookup"><span data-stu-id="738ee-137">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="738ee-138">已將支援新增至私人端點</span><span class="sxs-lookup"><span data-stu-id="738ee-138">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="738ee-139">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="738ee-139">Az.Maintenance</span></span>
* <span data-ttu-id="738ee-140">發行用於 GA 的維護 Cmdlet 版本</span><span class="sxs-lookup"><span data-stu-id="738ee-140">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="738ee-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="738ee-141">Az.Monitor</span></span>
* <span data-ttu-id="738ee-142">已新增私人連結範圍的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-142">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="738ee-143">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="738ee-143">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="738ee-144">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="738ee-144">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="738ee-145">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="738ee-145">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="738ee-146">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="738ee-146">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="738ee-147">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="738ee-147">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="738ee-148">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="738ee-148">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="738ee-149">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="738ee-149">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-150">Az.Network</span></span>
* <span data-ttu-id="738ee-151">已更新 Cmdlet，可在私人 IP 上啟用虛擬網路閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="738ee-151">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="738ee-152">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="738ee-152">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="738ee-153">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="738ee-153">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="738ee-154">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="738ee-154">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="738ee-155">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="738ee-155">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="738ee-156">已更新 Cmdlet，可啟用以 FQDN 為基礎的 LocalNetworkGateways 和 VpnSites</span><span class="sxs-lookup"><span data-stu-id="738ee-156">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="738ee-157">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="738ee-157">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="738ee-158">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="738ee-158">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="738ee-159">已在 ExpressRouteCircuitConnectionConfig 中新增對 IPv6 位址系列的支援 (全球適用)</span><span class="sxs-lookup"><span data-stu-id="738ee-159">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="738ee-160">已新增 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="738ee-160">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="738ee-161">允許設定所有現有屬性，包括 IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="738ee-161">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="738ee-162">已更新 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="738ee-162">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="738ee-163">已新增另一個選擇性參數 AddressPrefixType 來指定位址首碼的位址系列</span><span class="sxs-lookup"><span data-stu-id="738ee-163">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="738ee-164">已更新 Cmdlet，可啟用虛擬網路閘道連線上的 DPD 逾時設定。</span><span class="sxs-lookup"><span data-stu-id="738ee-164">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="738ee-165">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-165">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="738ee-166">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-166">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="738ee-167">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="738ee-167">Az.PolicyInsights</span></span>
* <span data-ttu-id="738ee-168">已新增用於觸發原則合規性掃描的 'Start-AzPolicyComplianceScan' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-168">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="738ee-169">已將原則定義、設定定義和指派版本新增至 'Get-AzPolicyState' 輸出</span><span class="sxs-lookup"><span data-stu-id="738ee-169">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="738ee-170">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="738ee-170">Az.ServiceFabric</span></span>
* <span data-ttu-id="738ee-171">已改善 'New-AzServiceFabricCluster' 範例的程式碼格式設定和可用性</span><span class="sxs-lookup"><span data-stu-id="738ee-171">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-172">Az.Sql</span></span>
* <span data-ttu-id="738ee-173">已新增 'Get-AzSqlInstanceOperation' 和 'Stop-AzSqlInstanceOperation' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-173">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="738ee-174">支援對 VNet 中的儲存體帳戶進行稽核。</span><span class="sxs-lookup"><span data-stu-id="738ee-174">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-175">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-175">Az.Storage</span></span>
* <span data-ttu-id="738ee-176">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="738ee-176">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="738ee-177">建立/更新儲存體帳戶時，支援新的 SkuName StandardGZRS、StandardRAGZRS</span><span class="sxs-lookup"><span data-stu-id="738ee-177">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="738ee-178">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="738ee-178">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="738ee-179">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="738ee-179">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="738ee-180">支援 DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="738ee-180">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="738ee-181">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="738ee-181">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="738ee-182">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="738ee-182">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="738ee-183">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="738ee-183">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="738ee-184">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="738ee-184">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="738ee-185">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="738ee-185">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="738ee-186">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="738ee-186">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="738ee-187">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="738ee-187">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="738ee-188">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="738ee-188">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="738ee-189">0.10.0-preview - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="738ee-189">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="738ee-190">一般</span><span class="sxs-lookup"><span data-stu-id="738ee-190">General</span></span>
* <span data-ttu-id="738ee-191">Az 模組現已在 Azure Stack Hub 中提供預覽。</span><span class="sxs-lookup"><span data-stu-id="738ee-191">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="738ee-192">此模組具有 Linux 和 macOs 的跨平台相容性。</span><span class="sxs-lookup"><span data-stu-id="738ee-192">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="738ee-193">Azure Stack Hub 現在支援使用 Az 模組的 PowerShell Core，如需詳細資訊，請參閱[這裡](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="738ee-193">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="738ee-194">Az 模組支援 2019-03-01-hybrid 設定檔：</span><span class="sxs-lookup"><span data-stu-id="738ee-194">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="738ee-195">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="738ee-195">Az.Billing</span></span>
  - <span data-ttu-id="738ee-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-196">Az.Compute</span></span>
  - <span data-ttu-id="738ee-197">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="738ee-197">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="738ee-198">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="738ee-198">Az.EventHub</span></span>
  - <span data-ttu-id="738ee-199">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="738ee-199">Az.IotHub</span></span>
  - <span data-ttu-id="738ee-200">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="738ee-200">Az.KeyVault</span></span>
  - <span data-ttu-id="738ee-201">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="738ee-201">Az.Monitor</span></span>
  - <span data-ttu-id="738ee-202">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-202">Az.Network</span></span>
  - <span data-ttu-id="738ee-203">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-203">Az.Resources</span></span>
  - <span data-ttu-id="738ee-204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-204">Az.Storage</span></span>
  - <span data-ttu-id="738ee-205">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-205">Az.Websites</span></span>
* <span data-ttu-id="738ee-206">已引進三個可搭配 Azure Stack Hub 且適用於 az 的新 PowerShell 模組，包括 Az.Databox、Az.IotHub 和 Az. EventHub</span><span class="sxs-lookup"><span data-stu-id="738ee-206">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="738ee-207">命令維持不變，但有次要變更，例如將 AzureRM 變更為 Az</span><span class="sxs-lookup"><span data-stu-id="738ee-207">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="738ee-208">您可以在[這裡](https://aka.ms/InstallASHPowerShell)找到 Azure Stack Hub 的 PowerShell 文件更新連結</span><span class="sxs-lookup"><span data-stu-id="738ee-208">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="738ee-209">3.7.0 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="738ee-209">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="738ee-210">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-210">Az.Accounts</span></span>
* <span data-ttu-id="738ee-211">已修正 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' 在未登入時擲回 NullReferenceException [#10292]</span><span class="sxs-lookup"><span data-stu-id="738ee-211">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-212">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-212">Az.Compute</span></span>
* <span data-ttu-id="738ee-213">已將下列參數新增至 'New-AzDiskConfig' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-213">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="738ee-214">DiskIOPSReadOnly、DiskMBpsReadOnly、MaxSharesCount、GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="738ee-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="738ee-215">允許 'New-AzGalleryImageVersion' Cmdlet 目標參數的加密屬性。</span><span class="sxs-lookup"><span data-stu-id="738ee-215">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="738ee-216">已修正 'Set-AzVmss' -Reimage 和 'Invoke-AzVMReimage' Cmdlet 的 tempDisk 問題。</span><span class="sxs-lookup"><span data-stu-id="738ee-216">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="738ee-217">[#11354]</span><span class="sxs-lookup"><span data-stu-id="738ee-217">[#11354]</span></span>
* <span data-ttu-id="738ee-218">已針對新的 SAP 延伸模組，將支援新增至下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-218">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="738ee-219">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="738ee-219">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="738ee-220">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="738ee-220">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="738ee-221">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="738ee-221">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="738ee-222">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="738ee-222">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="738ee-223">已修正說明文件範例中的錯誤</span><span class="sxs-lookup"><span data-stu-id="738ee-223">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="738ee-224">以表格格式顯示 VM PowerState 的確切字串值。</span><span class="sxs-lookup"><span data-stu-id="738ee-224">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="738ee-225">'New-AzVmssConfig'：已修正當 SinglePlacementGroup 停用時 AutomaticRepairs 屬性的序列化。</span><span class="sxs-lookup"><span data-stu-id="738ee-225">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="738ee-226">[#11257]</span><span class="sxs-lookup"><span data-stu-id="738ee-226">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="738ee-227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="738ee-227">Az.DataFactory</span></span>
* <span data-ttu-id="738ee-228">已將 ADF .Net SDK 版本更新為 4.8.0</span><span class="sxs-lookup"><span data-stu-id="738ee-228">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="738ee-229">已將選擇性參數新增至 'Invoke-AzDataFactoryV2Pipeline' 命令以支援重新執行</span><span class="sxs-lookup"><span data-stu-id="738ee-229">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="738ee-230">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="738ee-230">Az.DataLakeStore</span></span>
* <span data-ttu-id="738ee-231">已新增 'Export-AzDataLakeStoreItem' 和 'Import-AzDataLakeStoreItem' 的中斷性變更描述</span><span class="sxs-lookup"><span data-stu-id="738ee-231">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="738ee-232">已新增 'New-AzDataLakeStoreItem'、'Add-AzDAtaLakeStoreItemContent' 和 'Get-AzDAtaLakeStoreItemContent' 的位元組編碼選項</span><span class="sxs-lookup"><span data-stu-id="738ee-232">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="738ee-233">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="738ee-233">Az.HDInsight</span></span>
* <span data-ttu-id="738ee-234">支援在建立叢集時指定支援的最低 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="738ee-234">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="738ee-235">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="738ee-235">Az.IotHub</span></span>
* <span data-ttu-id="738ee-236">已新增管理每一部裝置的分散式設定支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-236">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="738ee-237">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="738ee-237">New Cmdlets are:</span></span>
    - <span data-ttu-id="738ee-238">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="738ee-238">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="738ee-239">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="738ee-239">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="738ee-240">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="738ee-240">Az.KeyVault</span></span>
* <span data-ttu-id="738ee-241">已將中斷性變更屬性新增至 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="738ee-241">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="738ee-242">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="738ee-242">Az.Monitor</span></span>
* <span data-ttu-id="738ee-243">已更新 'New-AzScheduledQueryRuleLogMetricTrigger' 的文件</span><span class="sxs-lookup"><span data-stu-id="738ee-243">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-244">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-244">Az.Network</span></span>
* <span data-ttu-id="738ee-245">已更新 Cmdlet 以允許跨租用戶 VirtualHubVnetConnections</span><span class="sxs-lookup"><span data-stu-id="738ee-245">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="738ee-246">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="738ee-246">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="738ee-247">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="738ee-247">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="738ee-248">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="738ee-248">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="738ee-249">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="738ee-249">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="738ee-250">已移除 SQL 管理 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="738ee-250">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="738ee-251">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="738ee-251">Az.PolicyInsights</span></span>
* <span data-ttu-id="738ee-252">改善錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="738ee-252">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="738ee-254">Azure Site Recovery 已新增重新保護的支援，並且已更新 Azure 磁碟加密虛擬機器的 VM 屬性。</span><span class="sxs-lookup"><span data-stu-id="738ee-254">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="738ee-255">已新增 Azure Site Recovery VmwareToAzure 屬性 DR 監視</span><span class="sxs-lookup"><span data-stu-id="738ee-255">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="738ee-256">Azure 備份已新增針對失敗項目重試原則更新的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-256">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="738ee-257">Azure 備份已新增在備份和還原期間對磁碟排除設定的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-257">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="738ee-258">Azure 備份已新增在 AzureFileShare 中還原多個檔案/資料夾的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-258">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="738ee-259">Azure 備份已新增在更新 IaasVM 原則時對使用者指定 Resourcegroup 支援的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-259">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-260">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-260">Az.Resources</span></span>
* <span data-ttu-id="738ee-261">已修正 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' 以使用實際的資源 apiVersion，而不是預設 apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="738ee-261">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="738ee-262">已新增對於錯誤案例的 correlationId 記錄</span><span class="sxs-lookup"><span data-stu-id="738ee-262">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="738ee-263">小型文件變更為 'Get-AzResourceLock'。</span><span class="sxs-lookup"><span data-stu-id="738ee-263">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="738ee-264">已新增範例。</span><span class="sxs-lookup"><span data-stu-id="738ee-264">Added example.</span></span>
* <span data-ttu-id="738ee-265">已逸出 'Get-AzADUser' 參數值中的單引號 [#11317]</span><span class="sxs-lookup"><span data-stu-id="738ee-265">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="738ee-266">已新增部署指令碼 ('Get-AzDeploymentScript'、'Get-AzDeploymentScriptLog'、'Save-AzDeploymentScriptLog'、'Remove-AzDeploymentScript') 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-266">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-267">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-267">Az.Sql</span></span>
* <span data-ttu-id="738ee-268">已將可讀取次要參數新增至 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="738ee-268">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="738ee-269">已新增 Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="738ee-269">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="738ee-270">已儲存在資料庫中分類資料行時的敏感度等級。</span><span class="sxs-lookup"><span data-stu-id="738ee-270">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="738ee-271">Az.Support</span><span class="sxs-lookup"><span data-stu-id="738ee-271">Az.Support</span></span>
* <span data-ttu-id="738ee-272">'Az.Support' 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="738ee-272">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="738ee-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-273">Az.Websites</span></span>
* <span data-ttu-id="738ee-274">已透過以下新 Cmdlet 新增使用 webapp 流量路由規則的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-274">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="738ee-275">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="738ee-275">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="738ee-276">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="738ee-276">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="738ee-277">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="738ee-277">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="738ee-278">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="738ee-278">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="738ee-279">3.6.1 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="738ee-279">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="738ee-280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-280">Az.Accounts</span></span>
* <span data-ttu-id="738ee-281">在 'Send-Feedback' 中開啟 Azure PowerShell 問卷頁面 [#11020]</span><span class="sxs-lookup"><span data-stu-id="738ee-281">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="738ee-282">在 'Resolve-Error' 中顯示 Azure PowerShell 問卷 URL [#11021]</span><span class="sxs-lookup"><span data-stu-id="738ee-282">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="738ee-283">已在 UserAgent 中新增 Az 版本</span><span class="sxs-lookup"><span data-stu-id="738ee-283">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="738ee-284">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="738ee-284">Az.ApiManagement</span></span>
* <span data-ttu-id="738ee-285">已新增可在 DeveloperPortal 端點上擷取和設定自訂網域的支援 [#11007]</span><span class="sxs-lookup"><span data-stu-id="738ee-285">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="738ee-286">'Export-AzApiManagementApi' 已新增以 JSON 格式下載 API 定義的支援 [#9987]</span><span class="sxs-lookup"><span data-stu-id="738ee-286">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="738ee-287">'Import-AzApiManagementApi' 已新增從 JSON 文件匯入 OpenAPI 3.0 定義的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-287">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="738ee-288">'New-AzApiManagementIdentityProvider' 和 'Set-AzApiManagementIdentityProvider' 已新增為 AAD B2C 提供者設定「登入租用戶」的支援 [#9784]</span><span class="sxs-lookup"><span data-stu-id="738ee-288">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="738ee-289">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="738ee-289">Az.DataLakeStore</span></span>
* <span data-ttu-id="738ee-290">已在 csproj 和 psd1 中明確新增對 System.Buffers 的參考。</span><span class="sxs-lookup"><span data-stu-id="738ee-290">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="738ee-291">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="738ee-291">Az.IotHub</span></span>
* <span data-ttu-id="738ee-292">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-292">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="738ee-293">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="738ee-293">New Cmdlets are:</span></span>
    - <span data-ttu-id="738ee-294">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="738ee-294">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="738ee-295">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="738ee-295">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="738ee-296">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="738ee-296">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="738ee-297">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="738ee-297">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="738ee-298">已新增可在 Iot 中樞的目標 Iot 裝置上管理模組的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-298">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="738ee-299">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="738ee-299">New Cmdlets are:</span></span>
    - <span data-ttu-id="738ee-300">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="738ee-300">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="738ee-301">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="738ee-301">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="738ee-302">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="738ee-302">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="738ee-303">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="738ee-303">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="738ee-304">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置的連接字串。</span><span class="sxs-lookup"><span data-stu-id="738ee-304">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="738ee-305">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置上的模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="738ee-305">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="738ee-306">已新增可取得/設定 IoT 裝置父系裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-306">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="738ee-307">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="738ee-307">New Cmdlets are:</span></span>
    - <span data-ttu-id="738ee-308">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="738ee-308">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="738ee-309">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="738ee-309">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="738ee-310">已新增可管理裝置父子關聯性的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-310">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="738ee-311">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="738ee-311">Az.Monitor</span></span>
* <span data-ttu-id="738ee-312">已修正 'Get-AzMetricDefinition' 的輸出值 [#9714]</span><span class="sxs-lookup"><span data-stu-id="738ee-312">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-313">Az.Network</span></span>
* <span data-ttu-id="738ee-314">已更新 Sql Management SDK。</span><span class="sxs-lookup"><span data-stu-id="738ee-314">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="738ee-315">已修正 PrivateLinkServiceConnectionState 類別中的命名差異問題。</span><span class="sxs-lookup"><span data-stu-id="738ee-315">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="738ee-316">將欄位 ActionsRequired 對應至 ActionRequired。</span><span class="sxs-lookup"><span data-stu-id="738ee-316">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="738ee-317">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="738ee-317">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-318">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-318">Az.Resources</span></span>
* <span data-ttu-id="738ee-319">已修正 'Get-AzRoleAssignment' 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="738ee-319">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="738ee-320">已將 'Remove-AzADGroup' 中的 '-Force' 和 '-PassThru' 參數標記為選擇性 [#10849]</span><span class="sxs-lookup"><span data-stu-id="738ee-320">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="738ee-321">已修正 'MailNickname' 不會在 'Remove-AzADGroup' 中傳回的問題 [#11167]</span><span class="sxs-lookup"><span data-stu-id="738ee-321">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="738ee-322">已修正 'Remove-AzADGroup' 管道作業無法運作的問題 [#11171]</span><span class="sxs-lookup"><span data-stu-id="738ee-322">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="738ee-323">已修正 GetAzureRoleAssignmentCommand 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="738ee-323">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="738ee-324">已針對原則 Cmdlet 即將來臨的變更新增重大變更屬性</span><span class="sxs-lookup"><span data-stu-id="738ee-324">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="738ee-325">已更新 'Get-AzResourceGroup' 以在伺服器端執行資源群組標籤篩選</span><span class="sxs-lookup"><span data-stu-id="738ee-325">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="738ee-326">已擴充標籤 Cmdlet 以接受 -ResourceId</span><span class="sxs-lookup"><span data-stu-id="738ee-326">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="738ee-327">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="738ee-327">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="738ee-328">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="738ee-328">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="738ee-329">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="738ee-329">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="738ee-330">已新增標籤 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-330">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="738ee-331">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="738ee-331">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="738ee-332">從 SDK 3.3.0 引進 ScopedDeployment</span><span class="sxs-lookup"><span data-stu-id="738ee-332">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-333">Az.Sql</span></span>
* <span data-ttu-id="738ee-334">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="738ee-334">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="738ee-335">已針對受控資料庫新增對於長期保留備份設定的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-335">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="738ee-336">在受控資料庫上取得/設定 LTR 原則</span><span class="sxs-lookup"><span data-stu-id="738ee-336">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="738ee-337">依受控資料庫、受控執行個體或位置取得 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="738ee-337">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="738ee-338">移除 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="738ee-338">Remove an LTR backup</span></span>
    - <span data-ttu-id="738ee-339">還原 LTR 備份以建立新的受控資料庫</span><span class="sxs-lookup"><span data-stu-id="738ee-339">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="738ee-340">已將 MinimalTlsVersion 新增至 New-AzSqlServer 和 Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="738ee-340">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="738ee-341">已將 MinimalTlsVersion 新增至 New-AzSqlInstance 和 Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="738ee-341">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="738ee-342">已提高適用於 Az.Network 的 SQL SDK 版本</span><span class="sxs-lookup"><span data-stu-id="738ee-342">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-343">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-343">Az.Storage</span></span>
* <span data-ttu-id="738ee-344">已在 ImmutabilityPolicy 中支援 AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="738ee-344">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="738ee-345">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="738ee-345">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="738ee-346">已針對未來版本中的 AzureStorageTable 類型變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="738ee-346">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="738ee-347">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="738ee-347">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="738ee-348">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="738ee-348">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="738ee-349">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-349">Az.Websites</span></span>
* <span data-ttu-id="738ee-350">已為 'New-AzAppServicePlan' 和 'Set-AzAppServicePlan' 新增標籤參數</span><span class="sxs-lookup"><span data-stu-id="738ee-350">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="738ee-351">將自訂網域新增至網站時如果擲回例外狀況，則會停止執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-351">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="738ee-352">已新增支援而可針對未和 App Service 方案位於相同資源群組中的 App Service 執行作業</span><span class="sxs-lookup"><span data-stu-id="738ee-352">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="738ee-353">已將存取限制套用至不同資源群組中的 WebApp/函式</span><span class="sxs-lookup"><span data-stu-id="738ee-353">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="738ee-354">已修正為 WebAppSlots 設定自訂主機名稱的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-354">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="738ee-355">3.5.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="738ee-355">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="738ee-356">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="738ee-356">Highlights since the last major release</span></span>
* <span data-ttu-id="738ee-357">更新用戶端遙測。</span><span class="sxs-lookup"><span data-stu-id="738ee-357">Updated client side telemetry.</span></span>
* <span data-ttu-id="738ee-358">Az.IotHub 已新增 Cmdlet 來支援裝置管理。</span><span class="sxs-lookup"><span data-stu-id="738ee-358">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="738ee-359">Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="738ee-359">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="738ee-360">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-360">Az.Accounts</span></span>
* <span data-ttu-id="738ee-361">已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料</span><span class="sxs-lookup"><span data-stu-id="738ee-361">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="738ee-362">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="738ee-362">Az.Automation</span></span>
* <span data-ttu-id="738ee-363">已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字</span><span class="sxs-lookup"><span data-stu-id="738ee-363">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="738ee-364">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="738ee-364">Az.CognitiveServices</span></span>
* <span data-ttu-id="738ee-365">已將 SDK 更新至 7.0</span><span class="sxs-lookup"><span data-stu-id="738ee-365">Updated SDK to 7.0</span></span>
* <span data-ttu-id="738ee-366">已改善伺服器回應空白主體時的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="738ee-366">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-367">Az.Compute</span></span>
* <span data-ttu-id="738ee-368">已允許 ProximityPlacementGroupId 在更新期間為空白值</span><span class="sxs-lookup"><span data-stu-id="738ee-368">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="738ee-369">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="738ee-369">Az.FrontDoor</span></span>
* <span data-ttu-id="738ee-370">已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義</span><span class="sxs-lookup"><span data-stu-id="738ee-370">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="738ee-371">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="738ee-371">Az.IotHub</span></span>
* <span data-ttu-id="738ee-372">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-372">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="738ee-373">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="738ee-373">New Cmdlets are:</span></span>
    - <span data-ttu-id="738ee-374">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="738ee-374">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="738ee-375">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="738ee-375">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="738ee-376">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="738ee-376">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="738ee-377">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="738ee-377">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="738ee-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="738ee-378">Az.KeyVault</span></span>
* <span data-ttu-id="738ee-379">已修正 Add-AzKeyVaultKey.md 的重複文字</span><span class="sxs-lookup"><span data-stu-id="738ee-379">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="738ee-380">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="738ee-380">Az.Monitor</span></span>
* <span data-ttu-id="738ee-381">已修正 Get-AzLog Cmdlet 的描述。</span><span class="sxs-lookup"><span data-stu-id="738ee-381">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="738ee-382">已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。</span><span class="sxs-lookup"><span data-stu-id="738ee-382">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="738ee-383">使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。</span><span class="sxs-lookup"><span data-stu-id="738ee-383">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-384">Az.Network</span></span>
* <span data-ttu-id="738ee-385">已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。</span><span class="sxs-lookup"><span data-stu-id="738ee-385">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="738ee-386">已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。</span><span class="sxs-lookup"><span data-stu-id="738ee-386">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="738ee-387">已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。</span><span class="sxs-lookup"><span data-stu-id="738ee-387">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="738ee-388">支援 VNet 防火牆上的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="738ee-388">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="738ee-389">未新增任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="738ee-389">No new cmdlets are added.</span></span> <span data-ttu-id="738ee-390">放寬 VNet 防火牆上的防火牆原則限制</span><span class="sxs-lookup"><span data-stu-id="738ee-390">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="738ee-392">已為 SQL Database 新增「還原為檔案」支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-392">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-393">Az.Resources</span></span>
* <span data-ttu-id="738ee-394">已重構範本部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-394">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="738ee-395">已新增用於在管理群組上管理部署的 Cmdlet：\*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="738ee-395">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="738ee-396">已新增用於在租用戶範圍上管理部署的 Cmdlet：\*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="738ee-396">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="738ee-397">已重構 \*-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作</span><span class="sxs-lookup"><span data-stu-id="738ee-397">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="738ee-398">為 \*-AzDeployment Cmdlet 建立別名 \*-AzSubscriptionDeployment</span><span class="sxs-lookup"><span data-stu-id="738ee-398">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="738ee-399">已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'</span><span class="sxs-lookup"><span data-stu-id="738ee-399">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="738ee-400">已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。</span><span class="sxs-lookup"><span data-stu-id="738ee-400">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="738ee-401">已重新產生說明檔</span><span class="sxs-lookup"><span data-stu-id="738ee-401">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-402">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-402">Az.Sql</span></span>
* <span data-ttu-id="738ee-403">已在受控執行個體上新增跨訂用帳戶的時間點還原支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-403">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="738ee-404">已新增變更現有 SQL 受控執行個體硬體世代的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-404">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="738ee-405">已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="738ee-405">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="738ee-406">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="738ee-406">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="738ee-407">已新增用於可用性群組接聽程式的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-407">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="738ee-408">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="738ee-408">Az.StorageSync</span></span>
* <span data-ttu-id="738ee-409">已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。</span><span class="sxs-lookup"><span data-stu-id="738ee-409">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="738ee-410">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="738ee-410">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="738ee-411">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="738ee-411">Highlights since the last major release</span></span>
* <span data-ttu-id="738ee-412">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="738ee-412">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="738ee-413">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="738ee-413">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="738ee-414">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-414">Az.Accounts</span></span>
* <span data-ttu-id="738ee-415">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="738ee-415">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="738ee-416">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="738ee-416">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="738ee-417">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="738ee-417">Az.ApiManagement</span></span>
* <span data-ttu-id="738ee-418">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="738ee-418">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="738ee-419">**New-AzApiManagementProduct**\* 和 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="738ee-419">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="738ee-420">https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="738ee-420">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="738ee-421">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="738ee-421">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-422">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-422">Az.Compute</span></span>
* <span data-ttu-id="738ee-423">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="738ee-423">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="738ee-424">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-424">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="738ee-425">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-425">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="738ee-426">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="738ee-427">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="738ee-427">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="738ee-428">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="738ee-428">Az.DataFactory</span></span>
* <span data-ttu-id="738ee-429">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="738ee-429">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="738ee-430">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="738ee-430">Az.DeploymentManager</span></span>
* <span data-ttu-id="738ee-431">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="738ee-431">Adds LIST operations for resources</span></span>
* <span data-ttu-id="738ee-432">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="738ee-432">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="738ee-433">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="738ee-433">Az.HDInsight</span></span>
* <span data-ttu-id="738ee-434">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="738ee-434">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="738ee-435">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="738ee-435">Az.KeyVault</span></span>
* <span data-ttu-id="738ee-436">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="738ee-436">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-437">Az.Network</span></span>
* <span data-ttu-id="738ee-438">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="738ee-438">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="738ee-439">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="738ee-439">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="738ee-440">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-440">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="738ee-441">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="738ee-441">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="738ee-442">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="738ee-442">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="738ee-443">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="738ee-443">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="738ee-444">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="738ee-444">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="738ee-445">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-445">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="738ee-446">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-446">New cmdlets added:</span></span>
        - <span data-ttu-id="738ee-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="738ee-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="738ee-448">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-448">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="738ee-449">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="738ee-449">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="738ee-450">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-450">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="738ee-451">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="738ee-451">Az.PolicyInsights</span></span>
* <span data-ttu-id="738ee-452">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="738ee-452">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="738ee-453">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="738ee-453">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="738ee-454">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="738ee-454">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="738ee-455">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="738ee-455">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-456">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-456">Az.RecoveryServices</span></span>
* <span data-ttu-id="738ee-457">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="738ee-457">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="738ee-458">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-458">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-459">Az.Resources</span></span>
* <span data-ttu-id="738ee-460">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="738ee-460">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="738ee-461">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="738ee-461">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-462">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-462">Az.Sql</span></span>
<span data-ttu-id="738ee-463">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="738ee-463">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-464">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-464">Az.Storage</span></span>
* <span data-ttu-id="738ee-465">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="738ee-465">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="738ee-466">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="738ee-466">New-AzStorageAccount</span></span>
* <span data-ttu-id="738ee-467">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="738ee-467">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="738ee-468">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="738ee-468">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="738ee-469">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-469">Az.Websites</span></span>
* <span data-ttu-id="738ee-470">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="738ee-470">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="738ee-471">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-471">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="738ee-472">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="738ee-472">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="738ee-473">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-473">Az.Accounts</span></span>
* <span data-ttu-id="738ee-474">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="738ee-474">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="738ee-475">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="738ee-475">Az.Cdn</span></span>
* <span data-ttu-id="738ee-476">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="738ee-476">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-477">Az.Compute</span></span>
* <span data-ttu-id="738ee-478">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="738ee-478">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="738ee-479">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="738ee-479">Az.ContainerInstance</span></span>
* <span data-ttu-id="738ee-480">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="738ee-480">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="738ee-481">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="738ee-481">Az.DataBoxEdge</span></span>
* <span data-ttu-id="738ee-482">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="738ee-482">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="738ee-483">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="738ee-483">Get the Edge Storage Container</span></span>
* <span data-ttu-id="738ee-484">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="738ee-484">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="738ee-485">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="738ee-485">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="738ee-486">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="738ee-486">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="738ee-487">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="738ee-487">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="738ee-488">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="738ee-488">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="738ee-489">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="738ee-489">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="738ee-490">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="738ee-490">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="738ee-491">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="738ee-491">Get the Edge Storage Account</span></span>
* <span data-ttu-id="738ee-492">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="738ee-492">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="738ee-493">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="738ee-493">Create new Edge Storage Account</span></span>
* <span data-ttu-id="738ee-494">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="738ee-494">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="738ee-495">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="738ee-495">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="738ee-496">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="738ee-496">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="738ee-497">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="738ee-497">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="738ee-498">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="738ee-498">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="738ee-499">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="738ee-499">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="738ee-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="738ee-500">Az.DataFactory</span></span>
* <span data-ttu-id="738ee-501">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="738ee-501">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="738ee-502">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="738ee-502">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="738ee-503">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="738ee-503">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="738ee-504">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="738ee-504">Az.DevTestLabs</span></span>
* <span data-ttu-id="738ee-505">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="738ee-505">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="738ee-506">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="738ee-506">Az.EventHub</span></span>
* <span data-ttu-id="738ee-507">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="738ee-507">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="738ee-508">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="738ee-508">Az.HDInsight</span></span>
* <span data-ttu-id="738ee-509">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="738ee-509">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="738ee-510">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="738ee-510">Az.MachineLearning</span></span>
* <span data-ttu-id="738ee-511">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-511">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="738ee-512">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="738ee-512">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="738ee-513">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="738ee-513">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="738ee-514">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="738ee-514">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="738ee-515">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="738ee-515">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="738ee-516">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="738ee-516">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="738ee-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="738ee-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="738ee-518">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="738ee-518">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-519">Az.Network</span></span>
* <span data-ttu-id="738ee-520">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="738ee-520">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-521">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-521">Az.RecoveryServices</span></span>
* <span data-ttu-id="738ee-522">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="738ee-522">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="738ee-523">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="738ee-523">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="738ee-524">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="738ee-524">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="738ee-525">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="738ee-525">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-526">Az.Resources</span></span>
* <span data-ttu-id="738ee-527">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="738ee-527">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-528">Az.Sql</span></span>
* <span data-ttu-id="738ee-529">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="738ee-529">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="738ee-530">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="738ee-530">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="738ee-531">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="738ee-531">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="738ee-532">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="738ee-532">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-533">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-533">Az.Storage</span></span>
* <span data-ttu-id="738ee-534">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="738ee-534">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="738ee-535">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="738ee-535">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="738ee-536">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="738ee-536">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="738ee-537">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="738ee-537">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="738ee-538">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="738ee-538">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="738ee-539">一般</span><span class="sxs-lookup"><span data-stu-id="738ee-539">General</span></span>
* <span data-ttu-id="738ee-540">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="738ee-540">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="738ee-541">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-541">Az.Accounts</span></span>
* <span data-ttu-id="738ee-542">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="738ee-542">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="738ee-543">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="738ee-543">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="738ee-544">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="738ee-544">Az.Batch</span></span>
* <span data-ttu-id="738ee-545">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="738ee-545">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="738ee-546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="738ee-546">Az.DataFactory</span></span>
* <span data-ttu-id="738ee-547">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="738ee-547">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="738ee-548">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="738ee-548">Az.FrontDoor</span></span>
* <span data-ttu-id="738ee-549">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="738ee-549">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="738ee-550">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="738ee-550">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="738ee-551">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="738ee-551">Az.HealthcareApis</span></span>
* <span data-ttu-id="738ee-552">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="738ee-552">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="738ee-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="738ee-553">Az.KeyVault</span></span>
* <span data-ttu-id="738ee-554">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="738ee-554">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="738ee-555">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="738ee-555">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="738ee-556">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-556">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="738ee-557">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="738ee-557">Az.Monitor</span></span>
* <span data-ttu-id="738ee-558">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="738ee-558">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="738ee-559">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="738ee-559">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="738ee-560">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="738ee-560">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-561">Az.Network</span></span>
* <span data-ttu-id="738ee-562">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="738ee-562">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-563">Az.Resources</span></span>
* <span data-ttu-id="738ee-564">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="738ee-564">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="738ee-565">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-565">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-566">Az.Sql</span></span>
* <span data-ttu-id="738ee-567">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="738ee-567">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-568">Az.Storage</span></span>
* <span data-ttu-id="738ee-569">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="738ee-569">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="738ee-570">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="738ee-570">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="738ee-571">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="738ee-571">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="738ee-572">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="738ee-572">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="738ee-573">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="738ee-573">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="738ee-574">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="738ee-574">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="738ee-575">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="738ee-575">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="738ee-576">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="738ee-576">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="738ee-577">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="738ee-577">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="738ee-578">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="738ee-578">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="738ee-579">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="738ee-579">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="738ee-580">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="738ee-580">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="738ee-581">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="738ee-581">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="738ee-582">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="738ee-582">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="738ee-583">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="738ee-583">Highlights since the last major release</span></span>
* <span data-ttu-id="738ee-584">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="738ee-584">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="738ee-585">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="738ee-585">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-586">Az.Compute</span></span>
* <span data-ttu-id="738ee-587">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="738ee-587">VM Reapply feature</span></span>
    - <span data-ttu-id="738ee-588">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-588">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="738ee-589">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="738ee-589">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="738ee-590">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="738ee-590">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="738ee-591">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="738ee-591">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="738ee-592">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="738ee-592">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="738ee-593">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-593">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="738ee-594">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="738ee-594">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="738ee-595">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-595">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="738ee-596">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-596">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="738ee-597">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-597">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="738ee-598">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="738ee-598">Az.DataBoxEdge</span></span>
* <span data-ttu-id="738ee-599">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="738ee-599">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="738ee-600">取得訂單</span><span class="sxs-lookup"><span data-stu-id="738ee-600">Get the Order</span></span>
* <span data-ttu-id="738ee-601">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="738ee-601">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="738ee-602">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="738ee-602">Create new Order</span></span>
* <span data-ttu-id="738ee-603">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="738ee-603">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="738ee-604">移除訂單</span><span class="sxs-lookup"><span data-stu-id="738ee-604">Remove the Order</span></span>
* <span data-ttu-id="738ee-605">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="738ee-605">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="738ee-606">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="738ee-606">Now creates Local Share</span></span>
* <span data-ttu-id="738ee-607">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="738ee-607">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="738ee-608">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="738ee-608">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="738ee-609">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="738ee-609">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="738ee-610">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="738ee-610">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="738ee-611">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="738ee-611">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="738ee-612">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="738ee-612">Gets the information about Triggers</span></span>
* <span data-ttu-id="738ee-613">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="738ee-613">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="738ee-614">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="738ee-614">Create new Triggers</span></span>
* <span data-ttu-id="738ee-615">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="738ee-615">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="738ee-616">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="738ee-616">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="738ee-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="738ee-617">Az.DataFactory</span></span>
* <span data-ttu-id="738ee-618">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="738ee-618">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="738ee-619">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="738ee-619">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="738ee-620">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="738ee-620">Az.DataLakeStore</span></span>
* <span data-ttu-id="738ee-621">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="738ee-621">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="738ee-622">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="738ee-622">Az.EventHub</span></span>
* <span data-ttu-id="738ee-623">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="738ee-623">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="738ee-624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="738ee-624">Az.FrontDoor</span></span>
* <span data-ttu-id="738ee-625">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="738ee-625">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="738ee-626">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="738ee-626">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="738ee-627">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="738ee-627">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="738ee-628">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="738ee-628">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-629">Az.Network</span></span>
* <span data-ttu-id="738ee-630">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="738ee-630">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="738ee-631">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="738ee-631">Az.PrivateDns</span></span>
* <span data-ttu-id="738ee-632">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="738ee-632">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-633">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-633">Az.RecoveryServices</span></span>
* <span data-ttu-id="738ee-634">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="738ee-634">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="738ee-635">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="738ee-635">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="738ee-636">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="738ee-636">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="738ee-637">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="738ee-637">Az.RedisCache</span></span>
* <span data-ttu-id="738ee-638">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="738ee-638">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="738ee-639">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="738ee-639">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="738ee-640">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="738ee-640">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-641">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-641">Az.Resources</span></span>
- <span data-ttu-id="738ee-642">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="738ee-642">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="738ee-643">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="738ee-643">Updated create policy definition help example</span></span>
- <span data-ttu-id="738ee-644">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="738ee-644">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="738ee-645">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="738ee-645">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="738ee-646">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="738ee-646">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-647">Az.Sql</span></span>
* <span data-ttu-id="738ee-648">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-648">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="738ee-649">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="738ee-649">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="738ee-650">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="738ee-650">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="738ee-651">一般</span><span class="sxs-lookup"><span data-stu-id="738ee-651">General</span></span>
* <span data-ttu-id="738ee-652">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="738ee-652">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="738ee-653">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-653">Az.Accounts</span></span>
* <span data-ttu-id="738ee-654">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="738ee-654">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="738ee-655">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="738ee-655">Az.Advisor</span></span>
* <span data-ttu-id="738ee-656">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="738ee-656">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="738ee-657">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="738ee-657">Az.Batch</span></span>
* <span data-ttu-id="738ee-658">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="738ee-658">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="738ee-659">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="738ee-659">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="738ee-660">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="738ee-660">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="738ee-661">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="738ee-661">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="738ee-662">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="738ee-662">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="738ee-663">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="738ee-663">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="738ee-664">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="738ee-664">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="738ee-665">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="738ee-665">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="738ee-666">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="738ee-666">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="738ee-667">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="738ee-667">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="738ee-668">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="738ee-668">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="738ee-669">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="738ee-669">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="738ee-670">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="738ee-670">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="738ee-671">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="738ee-671">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="738ee-672">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="738ee-672">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="738ee-673">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="738ee-673">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="738ee-674">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="738ee-674">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="738ee-675">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="738ee-675">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="738ee-676">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="738ee-676">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="738ee-677">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="738ee-677">This operation is no longer supported.</span></span>
* <span data-ttu-id="738ee-678">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="738ee-678">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="738ee-679">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="738ee-679">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="738ee-680">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="738ee-680">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="738ee-681">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="738ee-681">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="738ee-682">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="738ee-682">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="738ee-683">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="738ee-683">New non-verified images are also now returned.</span></span> <span data-ttu-id="738ee-684">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="738ee-684">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="738ee-685">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="738ee-685">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="738ee-686">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="738ee-686">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="738ee-687">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="738ee-687">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="738ee-688">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="738ee-688">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="738ee-689">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="738ee-689">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="738ee-690">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="738ee-690">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="738ee-691">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="738ee-691">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="738ee-692">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="738ee-692">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="738ee-693">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="738ee-693">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="738ee-694">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="738ee-694">Az.Cdn</span></span>
* <span data-ttu-id="738ee-695">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="738ee-695">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="738ee-696">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="738ee-696">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-697">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-697">Az.Compute</span></span>
* <span data-ttu-id="738ee-698">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="738ee-698">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="738ee-699">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="738ee-699">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="738ee-700">DiskEncryptionSetId 參數已新增至下列 Cmdlet： Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="738ee-700">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="738ee-701">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-701">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="738ee-702">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-702">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="738ee-703">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="738ee-703">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="738ee-704">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-704">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="738ee-705">重大變更</span><span class="sxs-lookup"><span data-stu-id="738ee-705">Breaking changes</span></span>
    - <span data-ttu-id="738ee-706">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="738ee-706">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="738ee-707">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="738ee-707">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="738ee-708">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="738ee-708">Az.DataFactory</span></span>
* <span data-ttu-id="738ee-709">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="738ee-709">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="738ee-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="738ee-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="738ee-711">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="738ee-711">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="738ee-712">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="738ee-712">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="738ee-713">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="738ee-713">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="738ee-714">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="738ee-714">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="738ee-715">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="738ee-715">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="738ee-716">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="738ee-716">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="738ee-717">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="738ee-717">Az.FrontDoor</span></span>
* <span data-ttu-id="738ee-718">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="738ee-718">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="738ee-719">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="738ee-719">Az.HDInsight</span></span>
* <span data-ttu-id="738ee-720">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="738ee-720">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="738ee-721">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="738ee-721">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="738ee-722">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="738ee-722">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="738ee-723">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-723">Removed five cmdlets:</span></span>
    - <span data-ttu-id="738ee-724">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="738ee-724">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="738ee-725">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="738ee-725">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="738ee-726">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="738ee-726">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="738ee-727">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="738ee-727">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="738ee-728">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="738ee-728">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="738ee-729">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-729">Added three cmdlets:</span></span>
    - <span data-ttu-id="738ee-730">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="738ee-730">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="738ee-731">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="738ee-731">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="738ee-732">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="738ee-732">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="738ee-733">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="738ee-733">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="738ee-734">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="738ee-734">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="738ee-735">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="738ee-735">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="738ee-736">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="738ee-736">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="738ee-737">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="738ee-737">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="738ee-738">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="738ee-738">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="738ee-739">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="738ee-739">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="738ee-740">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="738ee-740">Added some scenario test cases.</span></span>
* <span data-ttu-id="738ee-741">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="738ee-741">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="738ee-742">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="738ee-742">Az.IotHub</span></span>
* <span data-ttu-id="738ee-743">重大變更：</span><span class="sxs-lookup"><span data-stu-id="738ee-743">Breaking changes:</span></span>
    - <span data-ttu-id="738ee-744">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="738ee-744">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="738ee-745">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="738ee-745">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="738ee-746">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="738ee-746">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="738ee-747">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="738ee-747">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="738ee-748">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="738ee-748">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="738ee-749">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="738ee-749">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="738ee-750">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="738ee-750">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="738ee-751">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="738ee-751">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="738ee-752">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="738ee-752">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="738ee-753">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="738ee-753">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="738ee-754">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="738ee-754">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="738ee-755">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="738ee-755">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-756">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-756">Az.RecoveryServices</span></span>
* <span data-ttu-id="738ee-757">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="738ee-757">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="738ee-758">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="738ee-758">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="738ee-759">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="738ee-759">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="738ee-760">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="738ee-760">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="738ee-761">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="738ee-761">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="738ee-762">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="738ee-762">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="738ee-763">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="738ee-763">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="738ee-764">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-764">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="738ee-765">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="738ee-765">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-766">Az.Resources</span></span>
* <span data-ttu-id="738ee-767">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="738ee-767">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-768">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-768">Az.Network</span></span>
* <span data-ttu-id="738ee-769">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="738ee-769">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="738ee-770">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-770">Updated cmdlet:</span></span>
        - <span data-ttu-id="738ee-771">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-771">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="738ee-772">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-772">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="738ee-773">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-773">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="738ee-774">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-774">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="738ee-775">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-775">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="738ee-776">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="738ee-776">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="738ee-777">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-777">New cmdlet:</span></span>
        - <span data-ttu-id="738ee-778">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="738ee-778">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="738ee-779">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="738ee-779">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="738ee-780">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="738ee-780">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="738ee-781">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="738ee-781">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="738ee-782">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="738ee-782">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="738ee-783">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="738ee-783">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="738ee-784">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="738ee-784">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="738ee-785">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="738ee-785">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="738ee-786">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-786">New cmdlets added:</span></span>
        - <span data-ttu-id="738ee-787">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="738ee-787">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="738ee-788">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="738ee-788">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="738ee-789">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="738ee-789">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="738ee-790">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="738ee-790">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="738ee-791">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="738ee-791">Set-AzVirtualHub</span></span>
* <span data-ttu-id="738ee-792">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="738ee-792">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="738ee-793">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="738ee-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="738ee-794">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="738ee-794">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="738ee-795">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="738ee-795">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="738ee-796">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="738ee-796">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="738ee-797">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="738ee-797">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="738ee-798">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-798">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="738ee-799">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-799">New cmdlets added:</span></span>
        - <span data-ttu-id="738ee-800">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-800">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="738ee-801">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="738ee-801">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="738ee-802">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="738ee-802">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="738ee-803">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="738ee-803">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="738ee-804">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="738ee-804">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="738ee-805">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="738ee-805">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="738ee-806">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="738ee-806">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="738ee-807">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-807">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="738ee-808">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-808">New cmdlets added:</span></span>
        - <span data-ttu-id="738ee-809">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="738ee-809">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="738ee-810">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="738ee-810">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="738ee-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="738ee-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="738ee-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="738ee-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="738ee-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="738ee-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="738ee-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="738ee-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="738ee-815">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="738ee-815">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="738ee-816">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="738ee-816">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="738ee-817">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-817">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="738ee-818">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="738ee-818">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="738ee-819">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-819">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="738ee-820">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="738ee-820">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="738ee-821">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="738ee-821">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="738ee-822">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="738ee-822">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="738ee-823">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="738ee-823">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="738ee-824">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="738ee-824">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="738ee-825">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="738ee-825">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="738ee-826">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-826">New cmdlets added:</span></span>
        - <span data-ttu-id="738ee-827">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="738ee-827">New-AzIpGroup</span></span>
        - <span data-ttu-id="738ee-828">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="738ee-828">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="738ee-829">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="738ee-829">Get-AzIpGroup</span></span>
        - <span data-ttu-id="738ee-830">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="738ee-830">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="738ee-831">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="738ee-831">Az.ServiceFabric</span></span>
* <span data-ttu-id="738ee-832">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="738ee-832">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-833">Az.Sql</span></span>
* <span data-ttu-id="738ee-834">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-834">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="738ee-835">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="738ee-835">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="738ee-836">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="738ee-836">Removed deprecated aliases:</span></span>
* <span data-ttu-id="738ee-837">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="738ee-837">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="738ee-838">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="738ee-838">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="738ee-839">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-839">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="738ee-840">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="738ee-840">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="738ee-841">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-841">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="738ee-842">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="738ee-842">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-843">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-843">Az.Storage</span></span>
* <span data-ttu-id="738ee-844">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="738ee-844">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="738ee-845">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="738ee-845">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="738ee-846">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="738ee-846">Set-AzStorageAccount</span></span>
* <span data-ttu-id="738ee-847">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="738ee-847">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="738ee-848">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="738ee-848">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="738ee-849">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="738ee-849">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="738ee-850">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="738ee-850">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="738ee-851">一般</span><span class="sxs-lookup"><span data-stu-id="738ee-851">General</span></span>
* <span data-ttu-id="738ee-852">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="738ee-852">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="738ee-853">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-853">Az.Accounts</span></span>
* <span data-ttu-id="738ee-854">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="738ee-854">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="738ee-855">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="738ee-855">Az.ApiManagement</span></span>
* <span data-ttu-id="738ee-856">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-856">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="738ee-857">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-857">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="738ee-858">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="738ee-858">Az.Automation</span></span>
* <span data-ttu-id="738ee-859">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="738ee-859">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="738ee-860">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="738ee-860">Az.Batch</span></span>
* <span data-ttu-id="738ee-861">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="738ee-861">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-862">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-862">Az.Compute</span></span>
* <span data-ttu-id="738ee-863">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="738ee-863">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="738ee-864">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="738ee-864">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="738ee-865">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="738ee-865">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="738ee-866">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="738ee-866">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="738ee-867">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="738ee-867">Az.DataFactory</span></span>
* <span data-ttu-id="738ee-868">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="738ee-868">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="738ee-869">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="738ee-869">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="738ee-870">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="738ee-870">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="738ee-871">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="738ee-871">Az.DataLakeStore</span></span>
* <span data-ttu-id="738ee-872">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="738ee-872">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="738ee-873">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="738ee-873">Az.HealthcareApis</span></span>
* <span data-ttu-id="738ee-874">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="738ee-874">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="738ee-875">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="738ee-875">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="738ee-876">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="738ee-876">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="738ee-877">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="738ee-877">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="738ee-878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="738ee-878">Az.IotHub</span></span>
* <span data-ttu-id="738ee-879">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="738ee-879">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="738ee-880">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="738ee-880">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="738ee-881">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="738ee-881">Az.Monitor</span></span>
* <span data-ttu-id="738ee-882">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="738ee-882">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="738ee-883">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="738ee-883">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="738ee-884">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="738ee-884">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="738ee-885">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="738ee-885">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-886">Az.Network</span></span>
* <span data-ttu-id="738ee-887">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="738ee-887">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="738ee-888">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-888">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="738ee-889">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-889">New cmdlets added:</span></span>
        - <span data-ttu-id="738ee-890">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="738ee-890">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="738ee-891">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-891">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="738ee-892">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-892">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="738ee-893">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-893">Updated cmdlets:</span></span>
        - <span data-ttu-id="738ee-894">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-894">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="738ee-895">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-895">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="738ee-896">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-896">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="738ee-897">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="738ee-897">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="738ee-898">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="738ee-898">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="738ee-899">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="738ee-899">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="738ee-900">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="738ee-900">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="738ee-901">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="738ee-901">Az.RedisCache</span></span>
* <span data-ttu-id="738ee-902">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="738ee-902">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-903">Az.Sql</span></span>
* <span data-ttu-id="738ee-904">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-904">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-905">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-905">Az.Storage</span></span>
* <span data-ttu-id="738ee-906">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="738ee-906">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="738ee-907">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="738ee-907">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="738ee-908">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="738ee-908">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="738ee-909">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="738ee-909">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="738ee-910">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="738ee-910">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="738ee-911">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="738ee-911">Az.StorageSync</span></span>
* <span data-ttu-id="738ee-912">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="738ee-912">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="738ee-913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-913">Az.Websites</span></span>
* <span data-ttu-id="738ee-914">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="738ee-914">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="738ee-915">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="738ee-915">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="738ee-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="738ee-916">Az.ApiManagement</span></span>
* <span data-ttu-id="738ee-917">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="738ee-917">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="738ee-918">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="738ee-918">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="738ee-919">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="738ee-919">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="738ee-920">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="738ee-920">Az.Automation</span></span>
* <span data-ttu-id="738ee-921">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="738ee-921">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="738ee-922">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="738ee-922">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="738ee-923">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="738ee-923">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-924">Az.Compute</span></span>
* <span data-ttu-id="738ee-925">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="738ee-925">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="738ee-926">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="738ee-926">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="738ee-927">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="738ee-927">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="738ee-928">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="738ee-928">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="738ee-929">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="738ee-929">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="738ee-930">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="738ee-930">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="738ee-931">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="738ee-931">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="738ee-932">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="738ee-932">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="738ee-933">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="738ee-933">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="738ee-934">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="738ee-934">Az.DataFactory</span></span>
* <span data-ttu-id="738ee-935">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="738ee-935">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="738ee-936">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="738ee-936">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="738ee-937">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="738ee-937">Az.HDInsight</span></span>
* <span data-ttu-id="738ee-938">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="738ee-938">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="738ee-939">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="738ee-939">Az.IotHub</span></span>
* <span data-ttu-id="738ee-940">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-940">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="738ee-941">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-941">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="738ee-942">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="738ee-942">New cmdlets are:</span></span>
    - <span data-ttu-id="738ee-943">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="738ee-943">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="738ee-944">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="738ee-944">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="738ee-945">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="738ee-945">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="738ee-946">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="738ee-946">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="738ee-947">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="738ee-947">Az.Monitor</span></span>
* <span data-ttu-id="738ee-948">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="738ee-948">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="738ee-949">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="738ee-949">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="738ee-950">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="738ee-950">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="738ee-951">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="738ee-951">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="738ee-952">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="738ee-952">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="738ee-953">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="738ee-953">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="738ee-954">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="738ee-954">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="738ee-955">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="738ee-955">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="738ee-956">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="738ee-956">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="738ee-957">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="738ee-957">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="738ee-958">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="738ee-958">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="738ee-959">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="738ee-959">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="738ee-960">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="738ee-960">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="738ee-961">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="738ee-961">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="738ee-962">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="738ee-962">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="738ee-963">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="738ee-963">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="738ee-964">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="738ee-964">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="738ee-965">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="738ee-965">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="738ee-966">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="738ee-966">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="738ee-967">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="738ee-967">Overall improved help files</span></span>
* <span data-ttu-id="738ee-968">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="738ee-968">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-969">Az.Network</span></span>
* <span data-ttu-id="738ee-970">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="738ee-970">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="738ee-971">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="738ee-971">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="738ee-972">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="738ee-972">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="738ee-973">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="738ee-973">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="738ee-974">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="738ee-974">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="738ee-975">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="738ee-975">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="738ee-976">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="738ee-976">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="738ee-977">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="738ee-977">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="738ee-978">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="738ee-978">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="738ee-979">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="738ee-979">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="738ee-980">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="738ee-980">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="738ee-981">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="738ee-981">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="738ee-982">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-982">New cmdlets</span></span>
        - <span data-ttu-id="738ee-983">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="738ee-983">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="738ee-984">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-984">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="738ee-985">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-985">Updated cmdlet:</span></span>
        - <span data-ttu-id="738ee-986">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="738ee-986">New-VpnSite</span></span>
        - <span data-ttu-id="738ee-987">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="738ee-987">Update-VpnSite</span></span>
        - <span data-ttu-id="738ee-988">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-988">New-VpnConnection</span></span>
        - <span data-ttu-id="738ee-989">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-989">Update-VpnConnection</span></span>
* <span data-ttu-id="738ee-990">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-990">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="738ee-992">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="738ee-992">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="738ee-993">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="738ee-993">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-994">Az.Resources</span></span>
* <span data-ttu-id="738ee-995">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="738ee-995">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="738ee-996">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="738ee-996">Az.ServiceFabric</span></span>
* <span data-ttu-id="738ee-997">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="738ee-997">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="738ee-998">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="738ee-998">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="738ee-999">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="738ee-999">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="738ee-1000">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="738ee-1000">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="738ee-1001">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="738ee-1001">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="738ee-1002">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="738ee-1002">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="738ee-1003">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="738ee-1003">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="738ee-1004">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="738ee-1004">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="738ee-1005">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="738ee-1005">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="738ee-1006">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="738ee-1006">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="738ee-1007">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="738ee-1007">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="738ee-1008">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="738ee-1008">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="738ee-1009">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="738ee-1009">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="738ee-1010">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="738ee-1010">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="738ee-1011">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="738ee-1011">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="738ee-1012">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="738ee-1012">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="738ee-1013">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="738ee-1013">Az.SignalR</span></span>
* <span data-ttu-id="738ee-1014">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1014">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-1015">Az.Sql</span></span>
* <span data-ttu-id="738ee-1016">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="738ee-1016">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="738ee-1017">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="738ee-1017">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="738ee-1018">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="738ee-1018">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="738ee-1019">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="738ee-1019">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="738ee-1020">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="738ee-1020">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-1021">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-1021">Az.Storage</span></span>
* <span data-ttu-id="738ee-1022">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="738ee-1022">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="738ee-1023">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="738ee-1023">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="738ee-1024">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="738ee-1024">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="738ee-1025">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="738ee-1025">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="738ee-1026">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="738ee-1026">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="738ee-1027">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="738ee-1027">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="738ee-1028">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="738ee-1028">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="738ee-1029">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="738ee-1029">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="738ee-1030">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="738ee-1030">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="738ee-1031">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="738ee-1031">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="738ee-1032">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="738ee-1032">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="738ee-1033">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-1033">Az.Websites</span></span>
* <span data-ttu-id="738ee-1034">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1034">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="738ee-1035">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="738ee-1035">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="738ee-1036">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="738ee-1036">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="738ee-1037">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="738ee-1037">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="738ee-1038">一般</span><span class="sxs-lookup"><span data-stu-id="738ee-1038">General</span></span>
* <span data-ttu-id="738ee-1039">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1039">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="738ee-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-1040">Az.Accounts</span></span>
* <span data-ttu-id="738ee-1041">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="738ee-1041">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="738ee-1042">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="738ee-1042">Az.Aks</span></span>
* <span data-ttu-id="738ee-1043">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1043">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="738ee-1044">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="738ee-1044">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="738ee-1045">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="738ee-1045">Az.ApiManagement</span></span>
* <span data-ttu-id="738ee-1046">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1046">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="738ee-1047">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="738ee-1047">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="738ee-1048">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-1048">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="738ee-1049">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="738ee-1049">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="738ee-1050">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="738ee-1050">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="738ee-1051">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="738ee-1051">Az.Batch</span></span>
* <span data-ttu-id="738ee-1052">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="738ee-1052">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="738ee-1053">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="738ee-1053">Az.Cdn</span></span>
* <span data-ttu-id="738ee-1054">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="738ee-1054">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-1055">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-1055">Az.Compute</span></span>
* <span data-ttu-id="738ee-1056">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1056">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="738ee-1057">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="738ee-1057">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="738ee-1058">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="738ee-1058">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="738ee-1059">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="738ee-1059">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="738ee-1060">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="738ee-1060">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="738ee-1061">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="738ee-1061">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="738ee-1062">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="738ee-1062">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="738ee-1063">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="738ee-1063">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="738ee-1064">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="738ee-1064">Az.DataFactory</span></span>
* <span data-ttu-id="738ee-1065">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="738ee-1065">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="738ee-1066">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="738ee-1066">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="738ee-1067">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="738ee-1067">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="738ee-1068">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="738ee-1068">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="738ee-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="738ee-1069">Az.DataLakeStore</span></span>
* <span data-ttu-id="738ee-1070">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="738ee-1070">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="738ee-1071">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="738ee-1071">Az.EventHub</span></span>
* <span data-ttu-id="738ee-1072">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1072">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="738ee-1073">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="738ee-1073">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="738ee-1074">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1074">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="738ee-1075">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="738ee-1075">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="738ee-1076">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="738ee-1076">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="738ee-1077">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1077">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="738ee-1078">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="738ee-1078">Az.Monitor</span></span>
* <span data-ttu-id="738ee-1079">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="738ee-1079">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-1080">Az.Network</span></span>
* <span data-ttu-id="738ee-1081">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-1081">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="738ee-1082">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="738ee-1082">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="738ee-1083">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="738ee-1083">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="738ee-1084">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1084">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="738ee-1085">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="738ee-1085">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="738ee-1086">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="738ee-1086">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="738ee-1087">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="738ee-1087">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="738ee-1088">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="738ee-1088">Az.OperationalInsights</span></span>
* <span data-ttu-id="738ee-1089">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="738ee-1089">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="738ee-1090">新增了範例</span><span class="sxs-lookup"><span data-stu-id="738ee-1090">Added example</span></span>
    - <span data-ttu-id="738ee-1091">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="738ee-1091">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="738ee-1092">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="738ee-1092">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="738ee-1093">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="738ee-1093">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-1094">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1094">Az.RecoveryServices</span></span>
* <span data-ttu-id="738ee-1095">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="738ee-1095">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-1096">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-1096">Az.Resources</span></span>
* <span data-ttu-id="738ee-1097">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1097">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="738ee-1098">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1098">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="738ee-1099">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="738ee-1099">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="738ee-1100">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="738ee-1100">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="738ee-1101">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="738ee-1101">Az.ServiceBus</span></span>
* <span data-ttu-id="738ee-1102">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="738ee-1102">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="738ee-1103">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="738ee-1103">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="738ee-1104">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="738ee-1104">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="738ee-1105">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="738ee-1105">Az.ServiceFabric</span></span>
* <span data-ttu-id="738ee-1106">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="738ee-1106">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="738ee-1107">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="738ee-1107">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="738ee-1108">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="738ee-1108">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="738ee-1109">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="738ee-1109">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="738ee-1110">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="738ee-1110">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="738ee-1111">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1111">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-1112">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-1112">Az.Sql</span></span>
* <span data-ttu-id="738ee-1113">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="738ee-1113">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-1114">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-1114">Az.Storage</span></span>
* <span data-ttu-id="738ee-1115">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="738ee-1115">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="738ee-1116">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="738ee-1116">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="738ee-1117">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="738ee-1117">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="738ee-1118">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="738ee-1118">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="738ee-1119">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="738ee-1119">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="738ee-1120">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="738ee-1120">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="738ee-1121">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-1121">Az.Websites</span></span>
* <span data-ttu-id="738ee-1122">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="738ee-1122">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="738ee-1123">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="738ee-1123">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="738ee-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-1124">Az.Accounts</span></span>
* <span data-ttu-id="738ee-1125">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="738ee-1125">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="738ee-1126">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="738ee-1126">Az.ApplicationInsights</span></span>
* <span data-ttu-id="738ee-1127">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="738ee-1127">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="738ee-1128">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="738ee-1128">Az.Automation</span></span>
* <span data-ttu-id="738ee-1129">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="738ee-1129">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="738ee-1130">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1130">Az.CognitiveServices</span></span>
* <span data-ttu-id="738ee-1131">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-1131">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-1132">Az.Compute</span></span>
* <span data-ttu-id="738ee-1133">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="738ee-1133">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="738ee-1134">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="738ee-1134">Az.ContainerRegistry</span></span>
* <span data-ttu-id="738ee-1135">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="738ee-1135">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="738ee-1136">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="738ee-1136">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="738ee-1137">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="738ee-1137">Az.DataFactory</span></span>
* <span data-ttu-id="738ee-1138">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="738ee-1138">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="738ee-1139">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="738ee-1139">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="738ee-1140">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="738ee-1140">Az.EventHub</span></span>
* <span data-ttu-id="738ee-1141">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="738ee-1141">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="738ee-1142">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="738ee-1142">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="738ee-1143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="738ee-1143">Az.KeyVault</span></span>
* <span data-ttu-id="738ee-1144">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1144">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="738ee-1145">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="738ee-1145">Az.LogicApp</span></span>
* <span data-ttu-id="738ee-1146">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="738ee-1146">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="738ee-1147">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="738ee-1147">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="738ee-1148">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1148">Az.ManagedServices</span></span>
* <span data-ttu-id="738ee-1149">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1149">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-1150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-1150">Az.Network</span></span>
* <span data-ttu-id="738ee-1151">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1151">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="738ee-1152">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1152">New cmdlets</span></span>
        - <span data-ttu-id="738ee-1153">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="738ee-1153">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="738ee-1154">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="738ee-1154">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="738ee-1155">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-1155">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="738ee-1156">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-1156">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="738ee-1157">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-1157">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="738ee-1158">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-1158">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="738ee-1159">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="738ee-1159">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="738ee-1160">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="738ee-1160">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="738ee-1161">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="738ee-1161">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="738ee-1162">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-1162">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="738ee-1163">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="738ee-1163">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="738ee-1164">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="738ee-1164">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="738ee-1165">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="738ee-1165">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="738ee-1166">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="738ee-1166">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="738ee-1167">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1167">Updated cmdlets</span></span>
        - <span data-ttu-id="738ee-1168">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-1168">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="738ee-1169">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-1169">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="738ee-1170">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-1170">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="738ee-1171">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="738ee-1171">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="738ee-1172">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="738ee-1172">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="738ee-1173">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-1173">Updated cmdlet:</span></span>
        - <span data-ttu-id="738ee-1174">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-1174">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="738ee-1175">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-1175">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="738ee-1176">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-1176">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="738ee-1177">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="738ee-1177">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="738ee-1178">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="738ee-1178">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="738ee-1179">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="738ee-1179">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="738ee-1180">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="738ee-1180">Az.OperationalInsights</span></span>
* <span data-ttu-id="738ee-1181">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="738ee-1181">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="738ee-1182">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="738ee-1182">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-1183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1183">Az.RecoveryServices</span></span>
* <span data-ttu-id="738ee-1184">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="738ee-1184">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="738ee-1185">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="738ee-1185">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="738ee-1186">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="738ee-1186">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="738ee-1187">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="738ee-1187">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="738ee-1188">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="738ee-1188">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="738ee-1189">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="738ee-1189">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="738ee-1190">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="738ee-1190">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="738ee-1191">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="738ee-1191">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="738ee-1192">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="738ee-1192">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="738ee-1193">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="738ee-1193">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-1194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-1194">Az.Resources</span></span>
- <span data-ttu-id="738ee-1195">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1195">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="738ee-1196">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="738ee-1196">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="738ee-1197">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="738ee-1197">Az.ServiceBus</span></span>
* <span data-ttu-id="738ee-1198">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="738ee-1198">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="738ee-1199">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="738ee-1199">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-1200">Az.Sql</span></span>
* <span data-ttu-id="738ee-1201">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="738ee-1201">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="738ee-1202">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1202">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="738ee-1203">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="738ee-1203">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-1204">Az.Storage</span></span>
* <span data-ttu-id="738ee-1205">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="738ee-1205">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="738ee-1206">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="738ee-1206">Az.StorageSync</span></span>
* <span data-ttu-id="738ee-1207">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="738ee-1207">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="738ee-1208">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="738ee-1208">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="738ee-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-1209">Az.Websites</span></span>
* <span data-ttu-id="738ee-1210">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="738ee-1210">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="738ee-1211">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="738ee-1211">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="738ee-1212">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="738ee-1212">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="738ee-1213">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="738ee-1213">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="738ee-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-1214">Az.Accounts</span></span>
* <span data-ttu-id="738ee-1215">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1215">Add support for profile cmdlets</span></span>
* <span data-ttu-id="738ee-1216">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1216">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="738ee-1217">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1217">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="738ee-1218">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="738ee-1218">Az.Advisor</span></span>
* <span data-ttu-id="738ee-1219">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="738ee-1219">GA release of Az.Advisor</span></span>
* <span data-ttu-id="738ee-1220">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="738ee-1220">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="738ee-1221">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="738ee-1221">Az.ApiManagement</span></span>
* <span data-ttu-id="738ee-1222">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1222">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="738ee-1223">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="738ee-1223">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="738ee-1224">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1224">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="738ee-1225">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1225">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="738ee-1226">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1226">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="738ee-1227">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="738ee-1227">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="738ee-1228">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1228">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="738ee-1229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="738ee-1229">Az.Automation</span></span>
* <span data-ttu-id="738ee-1230">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="738ee-1230">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-1231">Az.Compute</span></span>
* <span data-ttu-id="738ee-1232">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-1232">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="738ee-1233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="738ee-1233">Az.DataFactory</span></span>
* <span data-ttu-id="738ee-1234">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="738ee-1234">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="738ee-1235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="738ee-1235">Az.EventGrid</span></span>
* <span data-ttu-id="738ee-1236">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="738ee-1236">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="738ee-1237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="738ee-1237">Az.IotHub</span></span>
* <span data-ttu-id="738ee-1238">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-1238">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-1239">Az.Network</span></span>
* <span data-ttu-id="738ee-1240">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="738ee-1240">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="738ee-1241">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="738ee-1241">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="738ee-1242">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="738ee-1242">Az.PolicyInsights</span></span>
* <span data-ttu-id="738ee-1243">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1243">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="738ee-1244">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="738ee-1244">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="738ee-1245">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="738ee-1245">Az.OperationalInsights</span></span>
* <span data-ttu-id="738ee-1246">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="738ee-1246">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-1247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1247">Az.RecoveryServices</span></span>
* <span data-ttu-id="738ee-1248">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="738ee-1248">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-1249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-1249">Az.Resources</span></span>
    - <span data-ttu-id="738ee-1250">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="738ee-1250">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="738ee-1251">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1251">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="738ee-1252">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="738ee-1252">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="738ee-1253">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="738ee-1253">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="738ee-1254">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="738ee-1254">Az.ServiceBus</span></span>
* <span data-ttu-id="738ee-1255">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="738ee-1255">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-1256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-1256">Az.Sql</span></span>
* <span data-ttu-id="738ee-1257">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="738ee-1257">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="738ee-1258">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="738ee-1258">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="738ee-1259">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="738ee-1259">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="738ee-1260">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="738ee-1260">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="738ee-1261">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="738ee-1261">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="738ee-1262">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="738ee-1262">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="738ee-1263">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="738ee-1263">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="738ee-1264">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="738ee-1264">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="738ee-1265">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="738ee-1265">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-1266">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-1266">Az.Storage</span></span>
* <span data-ttu-id="738ee-1267">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="738ee-1267">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="738ee-1268">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="738ee-1268">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="738ee-1269">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="738ee-1269">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="738ee-1270">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="738ee-1270">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="738ee-1271">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="738ee-1271">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="738ee-1272">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="738ee-1272">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="738ee-1273">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="738ee-1273">Set-AzStorageAccount</span></span>
* <span data-ttu-id="738ee-1274">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="738ee-1274">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="738ee-1275">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="738ee-1275">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="738ee-1276">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="738ee-1276">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="738ee-1277">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="738ee-1277">Az.StorageSync</span></span>
* <span data-ttu-id="738ee-1278">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="738ee-1278">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="738ee-1279">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="738ee-1279">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="738ee-1280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-1280">Az.Accounts</span></span>
* <span data-ttu-id="738ee-1281">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="738ee-1281">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="738ee-1282">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="738ee-1282">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="738ee-1283">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1283">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="738ee-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="738ee-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="738ee-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="738ee-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-1286">Az.Compute</span></span>
* <span data-ttu-id="738ee-1287">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="738ee-1287">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="738ee-1288">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="738ee-1288">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="738ee-1289">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="738ee-1289">Az.Dns</span></span>
* <span data-ttu-id="738ee-1290">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="738ee-1290">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="738ee-1291">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="738ee-1291">Az.EventGrid</span></span>
* <span data-ttu-id="738ee-1292">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="738ee-1292">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="738ee-1293">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-1293">New cmdlets:</span></span>
    - <span data-ttu-id="738ee-1294">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="738ee-1294">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="738ee-1295">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="738ee-1295">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="738ee-1296">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="738ee-1296">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="738ee-1297">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="738ee-1297">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="738ee-1298">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="738ee-1298">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="738ee-1299">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="738ee-1299">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="738ee-1300">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="738ee-1300">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="738ee-1301">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="738ee-1301">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="738ee-1302">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="738ee-1302">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="738ee-1303">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="738ee-1303">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="738ee-1304">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="738ee-1304">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="738ee-1305">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="738ee-1305">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="738ee-1306">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="738ee-1306">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="738ee-1307">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="738ee-1307">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="738ee-1308">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="738ee-1308">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="738ee-1309">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="738ee-1309">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="738ee-1310">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-1310">Updated cmdlets:</span></span>
    - <span data-ttu-id="738ee-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="738ee-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="738ee-1312">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="738ee-1312">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="738ee-1313">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="738ee-1313">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="738ee-1314">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="738ee-1314">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="738ee-1315">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="738ee-1315">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="738ee-1316">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="738ee-1316">Event subscription expiration date,</span></span>
            - <span data-ttu-id="738ee-1317">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="738ee-1317">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="738ee-1318">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="738ee-1318">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="738ee-1319">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="738ee-1319">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="738ee-1320">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="738ee-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="738ee-1321">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="738ee-1321">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="738ee-1322">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="738ee-1322">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="738ee-1323">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="738ee-1323">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="738ee-1324">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="738ee-1324">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="738ee-1325">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="738ee-1325">Az.FrontDoor</span></span>
* <span data-ttu-id="738ee-1326">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="738ee-1326">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="738ee-1327">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="738ee-1327">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="738ee-1328">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="738ee-1328">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="738ee-1329">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="738ee-1329">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-1330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-1330">Az.Network</span></span>
* <span data-ttu-id="738ee-1331">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1331">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="738ee-1332">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1332">New cmdlets</span></span>
        - <span data-ttu-id="738ee-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="738ee-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="738ee-1334">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="738ee-1334">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="738ee-1335">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1335">New cmdlets</span></span>
        - <span data-ttu-id="738ee-1336">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="738ee-1336">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="738ee-1337">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="738ee-1337">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="738ee-1338">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1338">New cmdlets</span></span>
        - <span data-ttu-id="738ee-1339">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="738ee-1339">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="738ee-1340">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="738ee-1340">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="738ee-1341">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="738ee-1341">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="738ee-1342">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-1342">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="738ee-1343">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-1343">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="738ee-1344">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="738ee-1344">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="738ee-1345">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1345">New cmdlets</span></span>
        - <span data-ttu-id="738ee-1346">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="738ee-1346">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="738ee-1347">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="738ee-1347">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="738ee-1348">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="738ee-1348">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="738ee-1349">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="738ee-1349">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="738ee-1350">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="738ee-1350">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="738ee-1351">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="738ee-1351">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="738ee-1352">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="738ee-1352">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="738ee-1353">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="738ee-1353">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="738ee-1354">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="738ee-1354">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="738ee-1355">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="738ee-1355">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="738ee-1356">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="738ee-1356">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="738ee-1357">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="738ee-1357">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="738ee-1358">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1358">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="738ee-1359">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="738ee-1359">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="738ee-1360">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="738ee-1360">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="738ee-1361">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1361">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="738ee-1362">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="738ee-1362">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="738ee-1363">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1363">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="738ee-1364">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-1364">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="738ee-1365">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="738ee-1365">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="738ee-1366">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="738ee-1366">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="738ee-1367">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="738ee-1367">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="738ee-1368">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="738ee-1368">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="738ee-1369">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="738ee-1369">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="738ee-1370">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="738ee-1370">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="738ee-1371">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="738ee-1371">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="738ee-1372">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="738ee-1372">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="738ee-1373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="738ee-1373">Az.OperationalInsights</span></span>
* <span data-ttu-id="738ee-1374">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="738ee-1374">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-1375">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-1375">Az.Resources</span></span>
* <span data-ttu-id="738ee-1376">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="738ee-1376">Support for additional Template Export options</span></span>
    - <span data-ttu-id="738ee-1377">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="738ee-1377">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="738ee-1378">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="738ee-1378">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="738ee-1379">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="738ee-1379">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="738ee-1380">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="738ee-1380">Az.ServiceFabric</span></span>
* <span data-ttu-id="738ee-1381">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1381">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-1382">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-1382">Az.Sql</span></span>
* <span data-ttu-id="738ee-1383">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="738ee-1383">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="738ee-1384">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="738ee-1384">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="738ee-1385">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="738ee-1385">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="738ee-1386">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="738ee-1386">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="738ee-1387">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="738ee-1387">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="738ee-1388">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="738ee-1388">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="738ee-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="738ee-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="738ee-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="738ee-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-1391">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-1391">Az.Storage</span></span>
* <span data-ttu-id="738ee-1392">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="738ee-1392">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="738ee-1393">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="738ee-1393">New-AzStorageAccount</span></span>
* <span data-ttu-id="738ee-1394">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="738ee-1394">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="738ee-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="738ee-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="738ee-1396">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-1396">Az.Websites</span></span>
* <span data-ttu-id="738ee-1397">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="738ee-1397">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="738ee-1398">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="738ee-1398">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="738ee-1399">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="738ee-1399">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="738ee-1400">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="738ee-1400">Az.Cdn</span></span>
* <span data-ttu-id="738ee-1401">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="738ee-1401">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-1402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-1402">Az.Compute</span></span>
* <span data-ttu-id="738ee-1403">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="738ee-1403">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="738ee-1404">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="738ee-1404">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="738ee-1405">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="738ee-1405">Az.EventHub</span></span>
* <span data-ttu-id="738ee-1406">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="738ee-1406">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="738ee-1407">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="738ee-1407">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-1408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-1408">Az.Network</span></span>
* <span data-ttu-id="738ee-1409">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="738ee-1409">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="738ee-1410">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="738ee-1410">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="738ee-1411">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="738ee-1411">Az.PolicyInsights</span></span>
* <span data-ttu-id="738ee-1412">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1412">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-1413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1413">Az.RecoveryServices</span></span>
* <span data-ttu-id="738ee-1414">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="738ee-1414">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="738ee-1415">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="738ee-1415">Az.ServiceBus</span></span>
* <span data-ttu-id="738ee-1416">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="738ee-1416">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="738ee-1417">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="738ee-1417">Az.ServiceFabric</span></span>
* <span data-ttu-id="738ee-1418">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="738ee-1418">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="738ee-1419">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="738ee-1419">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-1420">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-1420">Az.Sql</span></span>
* <span data-ttu-id="738ee-1421">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="738ee-1421">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="738ee-1422">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1422">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="738ee-1423">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="738ee-1423">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="738ee-1424">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="738ee-1424">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="738ee-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-1425">Az.Websites</span></span>
* <span data-ttu-id="738ee-1426">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1426">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="738ee-1427">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="738ee-1427">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="738ee-1428">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="738ee-1428">Az.ApiManagement</span></span>
* <span data-ttu-id="738ee-1429">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="738ee-1429">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="738ee-1430">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="738ee-1430">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="738ee-1431">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="738ee-1431">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="738ee-1432">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="738ee-1432">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="738ee-1433">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="738ee-1433">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="738ee-1434">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="738ee-1434">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="738ee-1435">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="738ee-1435">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="738ee-1436">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="738ee-1436">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="738ee-1437">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="738ee-1437">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="738ee-1438">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="738ee-1438">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="738ee-1439">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="738ee-1439">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="738ee-1440">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="738ee-1440">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="738ee-1441">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="738ee-1441">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="738ee-1442">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="738ee-1442">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="738ee-1443">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="738ee-1443">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="738ee-1444">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="738ee-1444">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="738ee-1445">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="738ee-1445">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="738ee-1446">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="738ee-1446">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="738ee-1447">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="738ee-1447">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="738ee-1448">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="738ee-1448">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="738ee-1449">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="738ee-1449">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="738ee-1450">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="738ee-1450">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="738ee-1451">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="738ee-1451">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="738ee-1452">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="738ee-1452">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="738ee-1453">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1453">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="738ee-1454">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1454">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="738ee-1455">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="738ee-1455">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="738ee-1456">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="738ee-1456">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="738ee-1457">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-1457">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="738ee-1458">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="738ee-1458">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="738ee-1459">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="738ee-1459">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="738ee-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="738ee-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="738ee-1461">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="738ee-1461">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="738ee-1462">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="738ee-1462">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="738ee-1463">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="738ee-1463">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="738ee-1464">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="738ee-1464">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="738ee-1465">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="738ee-1465">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="738ee-1466">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="738ee-1466">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="738ee-1467">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="738ee-1467">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="738ee-1468">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="738ee-1468">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="738ee-1469">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="738ee-1469">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="738ee-1470">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="738ee-1470">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="738ee-1471">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="738ee-1471">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="738ee-1472">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="738ee-1472">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="738ee-1473">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="738ee-1473">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="738ee-1474">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="738ee-1474">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="738ee-1475">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="738ee-1475">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="738ee-1476">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="738ee-1476">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="738ee-1477">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="738ee-1477">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="738ee-1478">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="738ee-1478">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="738ee-1479">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="738ee-1479">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="738ee-1480">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="738ee-1480">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="738ee-1481">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="738ee-1481">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="738ee-1482">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="738ee-1482">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="738ee-1483">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="738ee-1483">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="738ee-1484">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="738ee-1484">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="738ee-1485">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="738ee-1485">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="738ee-1486">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="738ee-1486">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="738ee-1487">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="738ee-1487">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="738ee-1488">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-1488">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="738ee-1489">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="738ee-1489">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="738ee-1490">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="738ee-1490">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="738ee-1491">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="738ee-1491">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="738ee-1492">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-1492">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="738ee-1493">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="738ee-1493">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="738ee-1494">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="738ee-1494">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="738ee-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="738ee-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="738ee-1496">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="738ee-1496">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="738ee-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="738ee-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="738ee-1498">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="738ee-1498">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="738ee-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="738ee-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="738ee-1500">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="738ee-1500">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="738ee-1501">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="738ee-1501">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="738ee-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="738ee-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="738ee-1503">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="738ee-1503">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="738ee-1504">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="738ee-1504">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="738ee-1505">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="738ee-1505">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="738ee-1506">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="738ee-1506">Az.Automation</span></span>
* <span data-ttu-id="738ee-1507">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="738ee-1507">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="738ee-1508">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1508">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="738ee-1509">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1509">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="738ee-1510">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="738ee-1510">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="738ee-1511">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1511">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="738ee-1512">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="738ee-1512">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="738ee-1513">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="738ee-1513">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-1514">Az.Compute</span></span>
* <span data-ttu-id="738ee-1515">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="738ee-1515">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="738ee-1516">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="738ee-1516">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="738ee-1517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="738ee-1517">Az.DataLakeStore</span></span>
* <span data-ttu-id="738ee-1518">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="738ee-1518">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="738ee-1519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="738ee-1519">Az.Monitor</span></span>
* <span data-ttu-id="738ee-1520">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="738ee-1520">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-1521">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-1521">Az.Network</span></span>
* <span data-ttu-id="738ee-1522">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="738ee-1522">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="738ee-1523">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-1523">Updated cmdlet:</span></span>
        - <span data-ttu-id="738ee-1524">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="738ee-1524">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="738ee-1525">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="738ee-1525">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-1526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-1526">Az.Resources</span></span>
* <span data-ttu-id="738ee-1527">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="738ee-1527">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-1528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-1528">Az.Sql</span></span>
* <span data-ttu-id="738ee-1529">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="738ee-1529">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="738ee-1530">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="738ee-1530">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="738ee-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-1531">Az.Accounts</span></span>
* <span data-ttu-id="738ee-1532">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1532">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="738ee-1533">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1533">Az.CognitiveServices</span></span>
* <span data-ttu-id="738ee-1534">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="738ee-1534">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="738ee-1535">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="738ee-1535">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-1536">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-1536">Az.Compute</span></span>
* <span data-ttu-id="738ee-1537">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="738ee-1537">Proximity placement group feature.</span></span>
    - <span data-ttu-id="738ee-1538">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="738ee-1538">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="738ee-1539">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-1539">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="738ee-1540">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="738ee-1540">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="738ee-1541">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="738ee-1541">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="738ee-1542">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="738ee-1542">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="738ee-1543">重大變更</span><span class="sxs-lookup"><span data-stu-id="738ee-1543">Breaking changes</span></span>
    - <span data-ttu-id="738ee-1544">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="738ee-1544">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="738ee-1545">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="738ee-1545">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="738ee-1546">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="738ee-1546">Az.DeploymentManager</span></span>
* <span data-ttu-id="738ee-1547">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1547">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="738ee-1548">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="738ee-1548">Az.Dns</span></span>
* <span data-ttu-id="738ee-1549">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="738ee-1549">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="738ee-1550">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="738ee-1550">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="738ee-1551">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="738ee-1551">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="738ee-1552">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="738ee-1552">Az.FrontDoor</span></span>
* <span data-ttu-id="738ee-1553">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1553">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="738ee-1554">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="738ee-1554">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="738ee-1555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="738ee-1555">Az.HDInsight</span></span>
* <span data-ttu-id="738ee-1556">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-1556">Removed two cmdlets:</span></span>
    - <span data-ttu-id="738ee-1557">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="738ee-1557">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="738ee-1558">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="738ee-1558">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="738ee-1559">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="738ee-1559">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="738ee-1560">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="738ee-1560">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="738ee-1561">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="738ee-1561">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="738ee-1562">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="738ee-1562">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="738ee-1563">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="738ee-1563">Az.Monitor</span></span>
* <span data-ttu-id="738ee-1564">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="738ee-1564">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="738ee-1565">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="738ee-1565">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="738ee-1566">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="738ee-1566">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="738ee-1567">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="738ee-1567">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="738ee-1568">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="738ee-1568">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="738ee-1569">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="738ee-1569">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="738ee-1570">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="738ee-1570">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="738ee-1571">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="738ee-1571">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="738ee-1572">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="738ee-1572">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="738ee-1573">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="738ee-1573">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="738ee-1574">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="738ee-1574">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="738ee-1575">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="738ee-1575">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="738ee-1576">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="738ee-1576">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="738ee-1577">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1577">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-1578">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-1578">Az.Network</span></span>
* <span data-ttu-id="738ee-1579">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1579">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="738ee-1580">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1580">New cmdlets</span></span>
        - <span data-ttu-id="738ee-1581">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="738ee-1581">New-AzNatGateway</span></span>
        - <span data-ttu-id="738ee-1582">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="738ee-1582">Get-AzNatGateway</span></span>
        - <span data-ttu-id="738ee-1583">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="738ee-1583">Set-AzNatGateway</span></span>
        - <span data-ttu-id="738ee-1584">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="738ee-1584">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="738ee-1585">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1585">Updated cmdlets</span></span>
        - <span data-ttu-id="738ee-1586">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="738ee-1586">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="738ee-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="738ee-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="738ee-1588">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="738ee-1588">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="738ee-1589">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="738ee-1589">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="738ee-1590">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="738ee-1590">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="738ee-1591">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="738ee-1591">Az.PolicyInsights</span></span>
* <span data-ttu-id="738ee-1592">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="738ee-1592">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="738ee-1593">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="738ee-1593">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="738ee-1594">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="738ee-1594">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-1595">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1595">Az.RecoveryServices</span></span>
* <span data-ttu-id="738ee-1596">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="738ee-1596">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="738ee-1597">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="738ee-1597">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="738ee-1598">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="738ee-1598">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="738ee-1599">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="738ee-1599">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="738ee-1600">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="738ee-1600">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="738ee-1601">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="738ee-1601">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="738ee-1602">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="738ee-1602">Az.Relay</span></span>
* <span data-ttu-id="738ee-1603">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="738ee-1603">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="738ee-1604">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="738ee-1604">Az.ServiceBus</span></span>
* <span data-ttu-id="738ee-1605">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1605">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-1606">Az.Storage</span></span>
* <span data-ttu-id="738ee-1607">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="738ee-1607">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="738ee-1608">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="738ee-1608">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="738ee-1609">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="738ee-1609">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="738ee-1610">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="738ee-1610">New-AzStorageAccount</span></span>
* <span data-ttu-id="738ee-1611">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="738ee-1611">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="738ee-1612">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="738ee-1612">New-AzStorageAccount</span></span>
    - <span data-ttu-id="738ee-1613">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="738ee-1613">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="738ee-1614">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="738ee-1614">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="738ee-1615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-1615">Az.Websites</span></span>
* <span data-ttu-id="738ee-1616">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="738ee-1616">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="738ee-1617">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="738ee-1617">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="738ee-1618">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="738ee-1618">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="738ee-1619">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="738ee-1619">Highlights since the last major release</span></span>
* <span data-ttu-id="738ee-1620">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="738ee-1620">General availability of `Az` module</span></span>
* <span data-ttu-id="738ee-1621">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="738ee-1621">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="738ee-1622">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="738ee-1622">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="738ee-1623">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1623">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="738ee-1624">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="738ee-1624">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="738ee-1625">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1625">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="738ee-1626">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1626">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="738ee-1627">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-1627">Az.Accounts</span></span>
* <span data-ttu-id="738ee-1628">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="738ee-1628">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="738ee-1629">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="738ee-1629">Az.Batch</span></span>
* <span data-ttu-id="738ee-1630">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="738ee-1631">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="738ee-1631">Az.Cdn</span></span>
* <span data-ttu-id="738ee-1632">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1632">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="738ee-1633">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1633">Az.CognitiveServices</span></span>
* <span data-ttu-id="738ee-1634">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1634">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-1635">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-1635">Az.Compute</span></span>
* <span data-ttu-id="738ee-1636">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1636">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="738ee-1637">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1637">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="738ee-1638">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="738ee-1638">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="738ee-1639">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="738ee-1639">Az.DataFactory</span></span>
* <span data-ttu-id="738ee-1640">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="738ee-1640">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="738ee-1641">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="738ee-1641">Az.DataLakeStore</span></span>
* <span data-ttu-id="738ee-1642">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1642">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="738ee-1643">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="738ee-1643">Az.EventGrid</span></span>
* <span data-ttu-id="738ee-1644">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="738ee-1644">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="738ee-1645">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="738ee-1645">Az.EventHub</span></span>
* <span data-ttu-id="738ee-1646">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1646">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="738ee-1647">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="738ee-1647">Az.HDInsight</span></span>
* <span data-ttu-id="738ee-1648">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="738ee-1649">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="738ee-1649">Az.IotHub</span></span>
* <span data-ttu-id="738ee-1650">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="738ee-1651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="738ee-1651">Az.KeyVault</span></span>
* <span data-ttu-id="738ee-1652">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="738ee-1653">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="738ee-1653">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="738ee-1654">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="738ee-1654">Az.MachineLearning</span></span>
* <span data-ttu-id="738ee-1655">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1655">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="738ee-1656">Az.Media</span><span class="sxs-lookup"><span data-stu-id="738ee-1656">Az.Media</span></span>
* <span data-ttu-id="738ee-1657">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1657">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="738ee-1658">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="738ee-1658">Az.Monitor</span></span>
  * <span data-ttu-id="738ee-1659">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1659">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="738ee-1660">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="738ee-1660">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="738ee-1661">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="738ee-1661">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="738ee-1662">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="738ee-1662">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="738ee-1663">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="738ee-1663">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="738ee-1664">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="738ee-1664">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="738ee-1665">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="738ee-1665">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-1666">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-1666">Az.Network</span></span>
* <span data-ttu-id="738ee-1667">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1667">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="738ee-1668">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="738ee-1668">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="738ee-1669">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="738ee-1669">Az.NotificationHubs</span></span>
* <span data-ttu-id="738ee-1670">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1670">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="738ee-1671">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="738ee-1671">Az.OperationalInsights</span></span>
* <span data-ttu-id="738ee-1672">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="738ee-1673">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="738ee-1673">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="738ee-1674">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1674">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-1675">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1675">Az.RecoveryServices</span></span>
* <span data-ttu-id="738ee-1676">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1676">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="738ee-1677">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="738ee-1677">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="738ee-1678">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="738ee-1678">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="738ee-1679">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="738ee-1679">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="738ee-1680">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="738ee-1680">Az.RedisCache</span></span>
* <span data-ttu-id="738ee-1681">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1681">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-1682">Az.Resources</span></span>
* <span data-ttu-id="738ee-1683">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="738ee-1683">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-1684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-1684">Az.Sql</span></span>
* <span data-ttu-id="738ee-1685">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="738ee-1685">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="738ee-1686">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1686">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="738ee-1687">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="738ee-1687">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="738ee-1688">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="738ee-1688">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="738ee-1689">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="738ee-1689">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="738ee-1690">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="738ee-1690">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="738ee-1691">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="738ee-1691">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="738ee-1692">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-1692">Az.Websites</span></span>
* <span data-ttu-id="738ee-1693">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="738ee-1693">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="738ee-1694">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="738ee-1695">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="738ee-1695">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="738ee-1696">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="738ee-1696">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="738ee-1697">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="738ee-1697">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="738ee-1698">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="738ee-1698">Highlights since the last major release</span></span>
* <span data-ttu-id="738ee-1699">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="738ee-1699">General availability of `Az` module</span></span>
* <span data-ttu-id="738ee-1700">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="738ee-1700">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="738ee-1701">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="738ee-1701">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="738ee-1702">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1702">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="738ee-1703">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="738ee-1703">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="738ee-1704">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1704">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="738ee-1705">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1705">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="738ee-1706">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-1706">Az.Accounts</span></span>
* <span data-ttu-id="738ee-1707">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="738ee-1707">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="738ee-1708">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1708">Az.AnalysisServices</span></span>
* <span data-ttu-id="738ee-1709">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="738ee-1709">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="738ee-1710">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="738ee-1710">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="738ee-1711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="738ee-1711">Az.Automation</span></span>
* <span data-ttu-id="738ee-1712">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="738ee-1712">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="738ee-1713">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="738ee-1713">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="738ee-1714">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="738ee-1714">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-1715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-1715">Az.Compute</span></span>
* <span data-ttu-id="738ee-1716">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-1716">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="738ee-1717">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="738ee-1717">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="738ee-1718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="738ee-1718">Az.ContainerInstance</span></span>
* <span data-ttu-id="738ee-1719">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="738ee-1719">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="738ee-1720">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="738ee-1720">Az.DataFactory</span></span>
* <span data-ttu-id="738ee-1721">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="738ee-1721">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="738ee-1722">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="738ee-1722">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-1723">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-1723">Az.Resources</span></span>
* <span data-ttu-id="738ee-1724">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="738ee-1724">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="738ee-1725">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="738ee-1725">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="738ee-1726">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="738ee-1726">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="738ee-1727">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="738ee-1727">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="738ee-1728">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="738ee-1728">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="738ee-1729">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="738ee-1729">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-1730">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-1730">Az.Sql</span></span>
* <span data-ttu-id="738ee-1731">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="738ee-1731">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-1732">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-1732">Az.Storage</span></span>
* <span data-ttu-id="738ee-1733">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="738ee-1733">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="738ee-1734">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="738ee-1734">New-AzStorageContext</span></span>
* <span data-ttu-id="738ee-1735">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="738ee-1735">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="738ee-1736">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="738ee-1736">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="738ee-1737">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="738ee-1737">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="738ee-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="738ee-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="738ee-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="738ee-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="738ee-1740">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1740">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="738ee-1741">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="738ee-1741">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="738ee-1742">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="738ee-1742">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="738ee-1743">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="738ee-1743">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="738ee-1744">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="738ee-1744">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="738ee-1745">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="738ee-1745">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="738ee-1746">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="738ee-1746">Highlights since the last major release</span></span>
* <span data-ttu-id="738ee-1747">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="738ee-1747">General availability of `Az` module</span></span>
* <span data-ttu-id="738ee-1748">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="738ee-1748">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="738ee-1749">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="738ee-1749">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="738ee-1750">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1750">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="738ee-1751">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="738ee-1751">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="738ee-1752">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1752">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="738ee-1753">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1753">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="738ee-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="738ee-1754">Az.Automation</span></span>
* <span data-ttu-id="738ee-1755">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="738ee-1755">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="738ee-1756">動態分組</span><span class="sxs-lookup"><span data-stu-id="738ee-1756">Dynamic grouping</span></span>
    * <span data-ttu-id="738ee-1757">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="738ee-1757">Pre-Post script</span></span>
    * <span data-ttu-id="738ee-1758">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="738ee-1758">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-1759">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-1759">Az.Compute</span></span>
* <span data-ttu-id="738ee-1760">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1760">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="738ee-1761">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="738ee-1761">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="738ee-1762">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="738ee-1762">Az.KeyVault</span></span>
* <span data-ttu-id="738ee-1763">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1763">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-1764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-1764">Az.Network</span></span>
* <span data-ttu-id="738ee-1765">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1765">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="738ee-1766">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="738ee-1766">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-1767">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1767">Az.RecoveryServices</span></span>
* <span data-ttu-id="738ee-1768">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="738ee-1768">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="738ee-1769">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1769">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-1770">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-1770">Az.Resources</span></span>
* <span data-ttu-id="738ee-1771">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1771">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="738ee-1772">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="738ee-1772">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-1773">Az.Sql</span></span>
* <span data-ttu-id="738ee-1774">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="738ee-1774">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-1775">Az.Storage</span></span>
* <span data-ttu-id="738ee-1776">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="738ee-1776">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="738ee-1777">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="738ee-1777">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="738ee-1778">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="738ee-1778">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="738ee-1779">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="738ee-1779">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="738ee-1780">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="738ee-1780">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="738ee-1781">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="738ee-1781">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="738ee-1782">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="738ee-1782">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="738ee-1783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-1783">Az.Websites</span></span>
* <span data-ttu-id="738ee-1784">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="738ee-1784">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="738ee-1785">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="738ee-1785">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="738ee-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-1786">Az.Accounts</span></span>
* <span data-ttu-id="738ee-1787">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1787">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="738ee-1788">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="738ee-1788">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="738ee-1789">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="738ee-1789">Az.Automation</span></span>
* <span data-ttu-id="738ee-1790">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1790">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="738ee-1791">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="738ee-1791">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="738ee-1792">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="738ee-1792">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="738ee-1793">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="738ee-1793">Az.Cdn</span></span>
* <span data-ttu-id="738ee-1794">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1794">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-1795">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-1795">Az.Compute</span></span>
* <span data-ttu-id="738ee-1796">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1796">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="738ee-1797">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="738ee-1797">Az.DataFactory</span></span>
* <span data-ttu-id="738ee-1798">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="738ee-1798">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="738ee-1799">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="738ee-1799">Az.LogicApp</span></span>
* <span data-ttu-id="738ee-1800">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="738ee-1800">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-1801">Az.Network</span></span>
* <span data-ttu-id="738ee-1802">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1802">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-1803">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1803">Az.RecoveryServices</span></span>
* <span data-ttu-id="738ee-1804">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1804">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="738ee-1805">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="738ee-1805">SDK Update</span></span>
* <span data-ttu-id="738ee-1806">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="738ee-1806">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="738ee-1807">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="738ee-1807">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-1808">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-1808">Az.Resources</span></span>
* <span data-ttu-id="738ee-1809">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1809">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="738ee-1810">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="738ee-1810">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="738ee-1811">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1811">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="738ee-1812">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="738ee-1812">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="738ee-1813">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1813">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="738ee-1814">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="738ee-1814">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-1815">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-1815">Az.Sql</span></span>
* <span data-ttu-id="738ee-1816">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="738ee-1816">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="738ee-1817">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="738ee-1817">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-1818">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-1818">Az.Storage</span></span>
* <span data-ttu-id="738ee-1819">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="738ee-1819">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="738ee-1820">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="738ee-1820">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="738ee-1821">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1821">Az.AnalysisServices</span></span>
* <span data-ttu-id="738ee-1822">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1822">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="738ee-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="738ee-1823">Az.Automation</span></span>
* <span data-ttu-id="738ee-1824">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="738ee-1824">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="738ee-1825">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1825">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="738ee-1826">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="738ee-1826">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="738ee-1827">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1827">Az.CognitiveServices</span></span>
* <span data-ttu-id="738ee-1828">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="738ee-1828">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-1829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-1829">Az.Compute</span></span>
* <span data-ttu-id="738ee-1830">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1830">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="738ee-1831">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="738ee-1831">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="738ee-1832">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1832">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="738ee-1833">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="738ee-1833">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="738ee-1834">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="738ee-1834">Az.DataLakeStore</span></span>
* <span data-ttu-id="738ee-1835">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1835">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="738ee-1836">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="738ee-1836">Az.EventHub</span></span>
* <span data-ttu-id="738ee-1837">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="738ee-1837">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="738ee-1838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="738ee-1838">Az.KeyVault</span></span>
* <span data-ttu-id="738ee-1839">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="738ee-1839">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="738ee-1840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="738ee-1840">Az.LogicApp</span></span>
* <span data-ttu-id="738ee-1841">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="738ee-1841">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="738ee-1842">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="738ee-1842">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="738ee-1843">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1843">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="738ee-1844">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="738ee-1844">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="738ee-1845">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="738ee-1845">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="738ee-1846">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="738ee-1846">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="738ee-1847">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="738ee-1847">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="738ee-1848">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1848">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="738ee-1849">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="738ee-1849">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="738ee-1850">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="738ee-1850">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="738ee-1851">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="738ee-1851">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="738ee-1852">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="738ee-1852">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="738ee-1853">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="738ee-1853">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="738ee-1854">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="738ee-1854">Az.Monitor</span></span>
* <span data-ttu-id="738ee-1855">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="738ee-1855">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-1856">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-1856">Az.Network</span></span>
* <span data-ttu-id="738ee-1857">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="738ee-1857">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="738ee-1858">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="738ee-1858">Az.OperationalInsights</span></span>
* <span data-ttu-id="738ee-1859">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-1859">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="738ee-1860">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="738ee-1860">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="738ee-1861">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="738ee-1861">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-1862">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-1862">Az.Resources</span></span>
* <span data-ttu-id="738ee-1863">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1863">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="738ee-1864">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1864">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="738ee-1865">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1865">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="738ee-1866">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="738ee-1866">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-1867">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-1867">Az.Sql</span></span>
* <span data-ttu-id="738ee-1868">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1868">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="738ee-1869">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="738ee-1869">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="738ee-1870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-1870">Az.Websites</span></span>
* <span data-ttu-id="738ee-1871">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="738ee-1871">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="738ee-1872">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="738ee-1872">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="738ee-1873">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-1873">Az.Accounts</span></span>
* <span data-ttu-id="738ee-1874">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="738ee-1874">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="738ee-1875">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1875">Az.AnalysisServices</span></span>
<span data-ttu-id="738ee-1876">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="738ee-1876">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-1877">Az.Compute</span></span>
* <span data-ttu-id="738ee-1878">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1878">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="738ee-1879">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="738ee-1879">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="738ee-1880">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="738ee-1880">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-1881">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1881">Az.RecoveryServices</span></span>
<span data-ttu-id="738ee-1882">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="738ee-1882">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-1883">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-1883">Az.Resources</span></span>
* <span data-ttu-id="738ee-1884">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="738ee-1884">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="738ee-1885">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="738ee-1885">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="738ee-1886">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1886">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="738ee-1887">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="738ee-1887">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-1888">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-1888">Az.Sql</span></span>
* <span data-ttu-id="738ee-1889">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="738ee-1889">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="738ee-1890">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1890">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="738ee-1891">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="738ee-1891">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="738ee-1892">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="738ee-1892">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="738ee-1893">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-1893">Az.Accounts</span></span>
* <span data-ttu-id="738ee-1894">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="738ee-1894">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="738ee-1895">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1895">Az.AnalysisServices</span></span>
* <span data-ttu-id="738ee-1896">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="738ee-1896">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-1897">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-1897">Az.RecoveryServices</span></span>
* <span data-ttu-id="738ee-1898">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="738ee-1898">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="738ee-1899">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="738ee-1899">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="738ee-1900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-1900">Az.Accounts</span></span>
* <span data-ttu-id="738ee-1901">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="738ee-1901">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="738ee-1902">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="738ee-1902">Update incorrect online help URLs</span></span>
* <span data-ttu-id="738ee-1903">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="738ee-1903">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="738ee-1904">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="738ee-1904">Az.Aks</span></span>
* <span data-ttu-id="738ee-1905">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="738ee-1905">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="738ee-1906">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="738ee-1906">Az.Automation</span></span>
* <span data-ttu-id="738ee-1907">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-1907">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="738ee-1908">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="738ee-1908">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="738ee-1909">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="738ee-1909">Az.Cdn</span></span>
* <span data-ttu-id="738ee-1910">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="738ee-1910">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-1911">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-1911">Az.Compute</span></span>
* <span data-ttu-id="738ee-1912">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-1912">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="738ee-1913">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="738ee-1913">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="738ee-1914">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="738ee-1914">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="738ee-1915">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="738ee-1915">Az.ContainerRegistry</span></span>
* <span data-ttu-id="738ee-1916">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="738ee-1916">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="738ee-1917">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="738ee-1917">Az.DataFactory</span></span>
* <span data-ttu-id="738ee-1918">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="738ee-1918">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="738ee-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="738ee-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="738ee-1920">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1920">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="738ee-1921">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="738ee-1921">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="738ee-1922">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="738ee-1922">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="738ee-1923">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="738ee-1923">Az.IotHub</span></span>
* <span data-ttu-id="738ee-1924">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="738ee-1924">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="738ee-1925">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="738ee-1925">Az.KeyVault</span></span>
* <span data-ttu-id="738ee-1926">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="738ee-1926">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-1927">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-1927">Az.Network</span></span>
* <span data-ttu-id="738ee-1928">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="738ee-1928">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-1929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-1929">Az.Resources</span></span>
* <span data-ttu-id="738ee-1930">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="738ee-1930">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="738ee-1931">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1931">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="738ee-1932">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="738ee-1932">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="738ee-1933">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1933">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="738ee-1934">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1934">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="738ee-1935">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1935">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="738ee-1936">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="738ee-1936">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="738ee-1937">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="738ee-1937">Az.ServiceFabric</span></span>
* <span data-ttu-id="738ee-1938">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="738ee-1938">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="738ee-1939">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="738ee-1939">Fix some error messages.</span></span>
* <span data-ttu-id="738ee-1940">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="738ee-1940">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="738ee-1941">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="738ee-1941">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="738ee-1942">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="738ee-1942">Az.SignalR</span></span>
* <span data-ttu-id="738ee-1943">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="738ee-1943">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-1944">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-1944">Az.Sql</span></span>
* <span data-ttu-id="738ee-1945">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="738ee-1945">Update incorrect online help URLs</span></span>
* <span data-ttu-id="738ee-1946">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="738ee-1946">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="738ee-1947">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1947">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="738ee-1948">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="738ee-1948">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-1949">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-1949">Az.Storage</span></span>
* <span data-ttu-id="738ee-1950">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="738ee-1950">Update incorrect online help URLs</span></span>
* <span data-ttu-id="738ee-1951">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="738ee-1951">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="738ee-1952">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="738ee-1952">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="738ee-1953">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="738ee-1953">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="738ee-1954">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="738ee-1954">Az.TrafficManager</span></span>
* <span data-ttu-id="738ee-1955">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="738ee-1955">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="738ee-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-1956">Az.Websites</span></span>
* <span data-ttu-id="738ee-1957">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="738ee-1957">Update incorrect online help URLs</span></span>
* <span data-ttu-id="738ee-1958">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="738ee-1958">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="738ee-1959">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="738ee-1959">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="738ee-1960">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="738ee-1960">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="738ee-1961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-1961">Az.Accounts</span></span>
* <span data-ttu-id="738ee-1962">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="738ee-1962">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-1963">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-1963">Az.Compute</span></span>
* <span data-ttu-id="738ee-1964">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="738ee-1964">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="738ee-1965">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="738ee-1965">Updated the description of ID in help files</span></span>
* <span data-ttu-id="738ee-1966">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1966">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="738ee-1967">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="738ee-1967">Az.DataLakeStore</span></span>
* <span data-ttu-id="738ee-1968">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="738ee-1968">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="738ee-1969">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="738ee-1969">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="738ee-1970">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="738ee-1970">Az.EventGrid</span></span>
* <span data-ttu-id="738ee-1971">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="738ee-1971">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="738ee-1972">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="738ee-1972">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="738ee-1973">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="738ee-1973">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="738ee-1974">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="738ee-1974">Event Time-To-Live,</span></span>
        - <span data-ttu-id="738ee-1975">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="738ee-1975">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="738ee-1976">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="738ee-1976">Dead letter endpoint.</span></span>
    - <span data-ttu-id="738ee-1977">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="738ee-1977">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="738ee-1978">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="738ee-1978">Event Time-To-Live,</span></span>
        - <span data-ttu-id="738ee-1979">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="738ee-1979">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="738ee-1980">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="738ee-1980">Dead letter endpoint.</span></span>
* <span data-ttu-id="738ee-1981">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="738ee-1981">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="738ee-1982">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="738ee-1982">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="738ee-1983">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="738ee-1983">Az.IotHub</span></span>
* <span data-ttu-id="738ee-1984">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="738ee-1984">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="738ee-1985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="738ee-1985">Az.LogicApp</span></span>
* <span data-ttu-id="738ee-1986">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="738ee-1986">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-1987">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-1987">Az.Resources</span></span>
* <span data-ttu-id="738ee-1988">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1988">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="738ee-1989">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="738ee-1989">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="738ee-1990">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="738ee-1990">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="738ee-1991">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="738ee-1991">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="738ee-1992">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="738ee-1992">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="738ee-1993">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="738ee-1993">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="738ee-1994">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="738ee-1994">Az.SignalR</span></span>
* <span data-ttu-id="738ee-1995">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="738ee-1995">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-1996">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-1996">Az.Sql</span></span>
* <span data-ttu-id="738ee-1997">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="738ee-1997">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="738ee-1998">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-1998">Az.Storage</span></span>
* <span data-ttu-id="738ee-1999">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="738ee-1999">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="738ee-2000">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="738ee-2000">New-AzStorageContext</span></span>
* <span data-ttu-id="738ee-2001">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="738ee-2001">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="738ee-2002">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="738ee-2002">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="738ee-2003">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-2003">Az.Websites</span></span>
* <span data-ttu-id="738ee-2004">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="738ee-2004">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="738ee-2005">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="738ee-2005">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="738ee-2006">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="738ee-2006">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="738ee-2007">一般</span><span class="sxs-lookup"><span data-stu-id="738ee-2007">General</span></span>

- <span data-ttu-id="738ee-2008">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="738ee-2008">General Availability of Az Module</span></span>
- <span data-ttu-id="738ee-2009">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="738ee-2009">Online help for each module</span></span>
- <span data-ttu-id="738ee-2010">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="738ee-2010">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="738ee-2011">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="738ee-2011">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="738ee-2012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-2012">Az.Accounts</span></span>
- <span data-ttu-id="738ee-2013">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="738ee-2013">Changed from Az.Profile</span></span>
- <span data-ttu-id="738ee-2014">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="738ee-2014">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="738ee-2015">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="738ee-2015">Az.ApiManagement</span></span>
- <span data-ttu-id="738ee-2016">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="738ee-2016">Fixes for #7002</span></span>
- <span data-ttu-id="738ee-2017">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="738ee-2017">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="738ee-2018">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="738ee-2018">Az.Batch</span></span>
- <span data-ttu-id="738ee-2019">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="738ee-2019">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="738ee-2020">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="738ee-2020">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="738ee-2021">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="738ee-2021">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="738ee-2022">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="738ee-2022">Az.Billing</span></span>
- <span data-ttu-id="738ee-2023">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="738ee-2023">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="738ee-2024">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="738ee-2024">Az.CognitivServices</span></span>
- <span data-ttu-id="738ee-2025">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="738ee-2025">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="738ee-2026">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="738ee-2026">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="738ee-2027">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="738ee-2027">Az.ContainerInstance</span></span>
- <span data-ttu-id="738ee-2028">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="738ee-2028">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="738ee-2029">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="738ee-2029">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="738ee-2030">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="738ee-2030">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="738ee-2031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="738ee-2031">Az.DataLakeStore</span></span>
- <span data-ttu-id="738ee-2032">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="738ee-2032">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="738ee-2033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="738ee-2033">Az.Monitor</span></span>
- <span data-ttu-id="738ee-2034">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="738ee-2034">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="738ee-2035">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="738ee-2035">Az.KeyVault</span></span>
- <span data-ttu-id="738ee-2036">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="738ee-2036">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="738ee-2037">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="738ee-2037">Az.MachineLearning</span></span>
- <span data-ttu-id="738ee-2038">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-2038">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="738ee-2039">Az.Media</span><span class="sxs-lookup"><span data-stu-id="738ee-2039">Az.Media</span></span>
- <span data-ttu-id="738ee-2040">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="738ee-2040">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="738ee-2041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-2041">Az.Network</span></span>
<span data-ttu-id="738ee-2042">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-2042">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="738ee-2043">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="738ee-2043">New cmdlets added:</span></span>
        - <span data-ttu-id="738ee-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="738ee-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="738ee-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="738ee-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="738ee-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="738ee-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="738ee-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="738ee-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="738ee-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="738ee-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="738ee-2049">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="738ee-2049">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="738ee-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="738ee-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="738ee-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="738ee-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="738ee-2052">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="738ee-2052">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="738ee-2053">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="738ee-2053">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="738ee-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="738ee-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="738ee-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="738ee-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="738ee-2056">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-2056">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="738ee-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="738ee-2058">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-2058">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="738ee-2059">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-2059">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="738ee-2060">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="738ee-2060">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="738ee-2061">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="738ee-2061">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="738ee-2062">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="738ee-2062">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="738ee-2063">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-2063">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="738ee-2064">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="738ee-2064">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="738ee-2065">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="738ee-2065">Az.OperationalInsights</span></span>
- <span data-ttu-id="738ee-2066">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="738ee-2066">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="738ee-2067">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="738ee-2067">Az.Profile</span></span>
- <span data-ttu-id="738ee-2068">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="738ee-2068">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-2069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-2069">Az.RecoveryServices</span></span>
- <span data-ttu-id="738ee-2070">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="738ee-2070">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="738ee-2071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-2071">Az.Resources</span></span>
- <span data-ttu-id="738ee-2072">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="738ee-2072">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="738ee-2073">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="738ee-2073">Az.ServiceFabric</span></span>
- <span data-ttu-id="738ee-2074">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="738ee-2074">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="738ee-2075">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="738ee-2075">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="738ee-2076">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="738ee-2076">Az.SIgnalR</span></span>
- <span data-ttu-id="738ee-2077">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="738ee-2077">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="738ee-2078">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-2078">Az.Sql</span></span>
- <span data-ttu-id="738ee-2079">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="738ee-2079">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="738ee-2080">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="738ee-2080">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="738ee-2081">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="738ee-2081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="738ee-2082">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-2082">Az.Storage</span></span>
- <span data-ttu-id="738ee-2083">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="738ee-2083">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="738ee-2084">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-2084">Az.Websites</span></span>
- <span data-ttu-id="738ee-2085">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="738ee-2085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="738ee-2086">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="738ee-2086">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="738ee-2087">一般</span><span class="sxs-lookup"><span data-stu-id="738ee-2087">General</span></span>

* <span data-ttu-id="738ee-2088">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="738ee-2088">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="738ee-2089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-2089">Az.Compute</span></span>

* <span data-ttu-id="738ee-2090">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="738ee-2090">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="738ee-2091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="738ee-2091">Az.DataLakeStore</span></span>

* <span data-ttu-id="738ee-2092">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="738ee-2092">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="738ee-2093">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="738ee-2093">Az.FrontDoor</span></span>

* <span data-ttu-id="738ee-2094">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="738ee-2094">Fixed some broken links</span></span>
    - <span data-ttu-id="738ee-2095">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="738ee-2095">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="738ee-2096">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="738ee-2096">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="738ee-2097">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="738ee-2097">Az.RecoveryServices</span></span>

* <span data-ttu-id="738ee-2098">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="738ee-2098">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="738ee-2099">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="738ee-2099">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="738ee-2100">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-2100">Az.Resources</span></span>

* <span data-ttu-id="738ee-2101">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="738ee-2101">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="738ee-2102">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="738ee-2102">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="738ee-2103">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-2103">Az.Sql</span></span>

* <span data-ttu-id="738ee-2104">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="738ee-2104">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="738ee-2105">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-2105">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="738ee-2106">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="738ee-2106">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="738ee-2107">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-2107">Az.Storage</span></span>

* <span data-ttu-id="738ee-2108">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="738ee-2108">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="738ee-2109">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="738ee-2109">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="738ee-2110">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="738ee-2110">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="738ee-2111">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="738ee-2111">Support Static Website configuration</span></span>
    - <span data-ttu-id="738ee-2112">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="738ee-2112">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="738ee-2113">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="738ee-2113">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="738ee-2114">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-2114">Az.Websites</span></span>

* <span data-ttu-id="738ee-2115">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="738ee-2115">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="738ee-2116">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="738ee-2116">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="738ee-2117">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="738ee-2117">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="738ee-2118">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="738ee-2118">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="738ee-2119">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="738ee-2119">Az.ApiManagement</span></span>
* <span data-ttu-id="738ee-2120">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="738ee-2120">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="738ee-2121">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="738ee-2121">Az.Automation</span></span>
* <span data-ttu-id="738ee-2122">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-2122">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="738ee-2123">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-2123">Added Update Management cmdlets</span></span>
* <span data-ttu-id="738ee-2124">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-2124">Added Source Control cmdlets</span></span>
* <span data-ttu-id="738ee-2125">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-2125">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="738ee-2126">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="738ee-2126">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="738ee-2127">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-2127">Az.Compute</span></span>
* <span data-ttu-id="738ee-2128">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="738ee-2128">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="738ee-2129">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="738ee-2129">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="738ee-2130">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="738ee-2130">Az.ContainerInstance</span></span>
* <span data-ttu-id="738ee-2131">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="738ee-2131">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="738ee-2132">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="738ee-2132">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="738ee-2133">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="738ee-2133">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="738ee-2134">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-2134">Az.Network</span></span>
* <span data-ttu-id="738ee-2135">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="738ee-2135">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="738ee-2136">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="738ee-2136">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="738ee-2137">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="738ee-2137">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="738ee-2138">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="738ee-2138">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="738ee-2139">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="738ee-2139">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="738ee-2140">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="738ee-2140">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="738ee-2141">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="738ee-2141">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="738ee-2142">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="738ee-2142">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="738ee-2143">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="738ee-2143">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="738ee-2144">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="738ee-2144">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="738ee-2145">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="738ee-2145">Az.Relay</span></span>
* <span data-ttu-id="738ee-2146">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="738ee-2146">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="738ee-2147">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-2147">Az.Resources</span></span>
* <span data-ttu-id="738ee-2148">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="738ee-2148">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="738ee-2149">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="738ee-2149">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="738ee-2150">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="738ee-2150">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="738ee-2151">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="738ee-2151">Az.ServiceFabric</span></span>
* <span data-ttu-id="738ee-2152">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="738ee-2152">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="738ee-2153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-2153">Az.Sql</span></span>
* <span data-ttu-id="738ee-2154">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-2154">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="738ee-2155">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="738ee-2155">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="738ee-2156">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="738ee-2156">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="738ee-2157">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="738ee-2157">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="738ee-2158">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="738ee-2158">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="738ee-2159">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="738ee-2159">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="738ee-2160">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="738ee-2160">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="738ee-2161">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="738ee-2161">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="738ee-2162">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="738ee-2162">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="738ee-2163">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="738ee-2163">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="738ee-2164">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="738ee-2164">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="738ee-2165">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="738ee-2165">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="738ee-2166">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="738ee-2166">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="738ee-2167">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="738ee-2167">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="738ee-2168">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="738ee-2168">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="738ee-2169">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="738ee-2169">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="738ee-2170">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-2170">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="738ee-2171">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="738ee-2171">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="738ee-2172">一般</span><span class="sxs-lookup"><span data-stu-id="738ee-2172">General</span></span>
* <span data-ttu-id="738ee-2173">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="738ee-2173">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="738ee-2174">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="738ee-2174">Az.Profile</span></span>
* <span data-ttu-id="738ee-2175">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="738ee-2175">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="738ee-2176">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="738ee-2176">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="738ee-2177">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="738ee-2177">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="738ee-2178">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="738ee-2178">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="738ee-2179">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-2179">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="738ee-2180">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-2180">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="738ee-2181">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-2181">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="738ee-2182">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="738ee-2182">Az.CognitiveServices</span></span>
* <span data-ttu-id="738ee-2183">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="738ee-2183">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-2184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-2184">Az.Compute</span></span>
* <span data-ttu-id="738ee-2185">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-2185">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="738ee-2186">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="738ee-2186">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="738ee-2187">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="738ee-2187">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="738ee-2188">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="738ee-2188">Az.DataLakeStore</span></span>
* <span data-ttu-id="738ee-2189">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="738ee-2189">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="738ee-2190">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="738ee-2190">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="738ee-2191">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="738ee-2191">Az.Insights</span></span>
* <span data-ttu-id="738ee-2192">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="738ee-2192">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="738ee-2193">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="738ee-2193">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="738ee-2194">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="738ee-2194">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="738ee-2195">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="738ee-2195">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-2196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-2196">Az.Network</span></span>
* <span data-ttu-id="738ee-2197">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="738ee-2197">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="738ee-2198">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="738ee-2198">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="738ee-2199">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="738ee-2199">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="738ee-2200">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="738ee-2200">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="738ee-2201">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="738ee-2201">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="738ee-2202">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="738ee-2202">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="738ee-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="738ee-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="738ee-2204">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="738ee-2204">Az.PolicyInsights</span></span>
* <span data-ttu-id="738ee-2205">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-2205">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-2206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-2206">Az.Resources</span></span>
* <span data-ttu-id="738ee-2207">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="738ee-2207">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="738ee-2208">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="738ee-2208">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="738ee-2209">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="738ee-2209">Az.ServiceBus</span></span>
* <span data-ttu-id="738ee-2210">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="738ee-2210">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="738ee-2211">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="738ee-2211">Az.ServiceFabric</span></span>
* <span data-ttu-id="738ee-2212">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="738ee-2212">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="738ee-2213">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="738ee-2213">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="738ee-2214">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="738ee-2214">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="738ee-2215">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="738ee-2215">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="738ee-2216">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="738ee-2216">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="738ee-2217">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="738ee-2217">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="738ee-2218">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="738ee-2218">Az.Profile</span></span>
* <span data-ttu-id="738ee-2219">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-2219">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="738ee-2220">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="738ee-2220">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-2221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-2221">Az.Compute</span></span>
* <span data-ttu-id="738ee-2222">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="738ee-2222">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="738ee-2223">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="738ee-2223">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="738ee-2224">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="738ee-2224">Az.DataLakeStore</span></span>
* <span data-ttu-id="738ee-2225">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="738ee-2225">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="738ee-2226">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="738ee-2226">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="738ee-2227">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="738ee-2227">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="738ee-2228">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="738ee-2228">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="738ee-2229">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="738ee-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-2230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-2230">Az.Network</span></span>
* <span data-ttu-id="738ee-2231">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="738ee-2231">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="738ee-2232">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="738ee-2232">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-2233">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-2233">Az.Resources</span></span>
* <span data-ttu-id="738ee-2234">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="738ee-2234">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="738ee-2235">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="738ee-2235">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="738ee-2236">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="738ee-2236">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="738ee-2237">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="738ee-2237">Azure.Storage</span></span>
* <span data-ttu-id="738ee-2238">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-2238">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="738ee-2239">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="738ee-2239">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="738ee-2240">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="738ee-2240">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="738ee-2241">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="738ee-2241">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="738ee-2242">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="738ee-2242">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="738ee-2243">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="738ee-2243">Az.CognitiveServices</span></span>
* <span data-ttu-id="738ee-2244">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="738ee-2244">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="738ee-2245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="738ee-2245">Az.Compute</span></span>
* <span data-ttu-id="738ee-2246">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="738ee-2246">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="738ee-2247">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="738ee-2247">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="738ee-2248">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="738ee-2248">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="738ee-2249">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="738ee-2249">Az.DataFactoryV2</span></span>
* <span data-ttu-id="738ee-2250">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="738ee-2250">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="738ee-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="738ee-2251">Az.Network</span></span>
* <span data-ttu-id="738ee-2252">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="738ee-2252">Added NetworkProfile functionality.</span></span> <span data-ttu-id="738ee-2253">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-2253">new cmdlets added</span></span>
    - <span data-ttu-id="738ee-2254">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="738ee-2254">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="738ee-2255">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="738ee-2255">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="738ee-2256">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="738ee-2256">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="738ee-2257">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="738ee-2257">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="738ee-2258">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-2258">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="738ee-2259">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="738ee-2259">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="738ee-2260">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="738ee-2260">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="738ee-2261">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-2261">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="738ee-2262">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="738ee-2262">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="738ee-2263">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="738ee-2263">Az.RedisCache</span></span>
* <span data-ttu-id="738ee-2264">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="738ee-2264">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="738ee-2265">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="738ee-2265">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="738ee-2266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="738ee-2266">Az.Resources</span></span>
* <span data-ttu-id="738ee-2267">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="738ee-2267">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="738ee-2268">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="738ee-2268">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="738ee-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="738ee-2269">Az.Sql</span></span>
* <span data-ttu-id="738ee-2270">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="738ee-2270">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="738ee-2271">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="738ee-2271">Az.Websites</span></span>
* <span data-ttu-id="738ee-2272">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="738ee-2272">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="738ee-2273">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="738ee-2273">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="738ee-2274">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="738ee-2274">0.2.0 - September 2018</span></span>
 <span data-ttu-id="738ee-2275">初始版本</span><span class="sxs-lookup"><span data-stu-id="738ee-2275">Initial Release</span></span>