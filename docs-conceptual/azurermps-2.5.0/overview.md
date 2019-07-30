---
title: Azure Stack PowerShell 概觀 | Microsoft Docs
description: Azure Stack PowerShell 的概觀以及有關安裝和設定的指示。
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: 55f19ac5e6767df1312e0b531184e8621b60a011
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038188"
---
# <a name="azurerm-module-250"></a><span data-ttu-id="26845-103">AzureRM Module 2.5.0</span><span class="sxs-lookup"><span data-stu-id="26845-103">AzureRM Module 2.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="26845-104">需求：</span><span class="sxs-lookup"><span data-stu-id="26845-104">Requirements:</span></span>
<span data-ttu-id="26845-105">最低支援的 Azure Stack 版本為 1904 版。</span><span class="sxs-lookup"><span data-stu-id="26845-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="26845-106">注意：如果您使用的是舊版，請安裝版本 1.2.11</span><span class="sxs-lookup"><span data-stu-id="26845-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="26845-107">Install</span><span class="sxs-lookup"><span data-stu-id="26845-107">Install</span></span>
```powershell-interactive
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

## <a name="release-notes"></a><span data-ttu-id="26845-108">版本資訊</span><span class="sxs-lookup"><span data-stu-id="26845-108">Release Notes</span></span>
* <span data-ttu-id="26845-109">AzureRm.Resources</span><span class="sxs-lookup"><span data-stu-id="26845-109">AzureRm.Resources</span></span>
    * <span data-ttu-id="26845-110">新的資源模組支援 2018-05-01 API 版本搭配 2019-03-01-hybrid 設定檔</span><span class="sxs-lookup"><span data-stu-id="26845-110">New Resources module supporting 2018-05-01 api version with 2019-03-01-hybrid profile</span></span>
    * <span data-ttu-id="26845-111">PolicyDefinition(2016-12-01) 和 PolicyAssisgment(2017-06-01-預覽) 作業仍然使用舊版 API</span><span class="sxs-lookup"><span data-stu-id="26845-111">PolicyDefinition(2016-12-01) and PolicyAssisgment(2017-06-01-preview) operations are still with old api versions</span></span>
* <span data-ttu-id="26845-112">AzureRm.Compute</span><span class="sxs-lookup"><span data-stu-id="26845-112">AzureRm.Compute</span></span>
    * <span data-ttu-id="26845-113">新的計算模組支援 2017-12-01 API 版本。'</span><span class="sxs-lookup"><span data-stu-id="26845-113">New compute module supporting 2017-12-01 api version.'</span></span>


* <span data-ttu-id="26845-114">此版本對應至 azurestack 特定 API 設定檔 2019-03-01-hybrid</span><span class="sxs-lookup"><span data-stu-id="26845-114">This release corresponds to the azurestack specific api profile 2019-03-01-hybrid</span></span>
* <span data-ttu-id="26845-115">所有模組皆取用比 AzureRm.Profile 模組上更大或相等的相依性。</span><span class="sxs-lookup"><span data-stu-id="26845-115">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="26845-116">每個模組支援的 API 版本都會更新。</span><span class="sxs-lookup"><span data-stu-id="26845-116">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="26845-117">計算 - 2017-12-30</span><span class="sxs-lookup"><span data-stu-id="26845-117">Compute - 2017-12-30</span></span>
    * <span data-ttu-id="26845-118">網路 - 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="26845-118">Network - 2017-10-01</span></span>
    * <span data-ttu-id="26845-119">儲存體 2016-01-01</span><span class="sxs-lookup"><span data-stu-id="26845-119">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="26845-120">資源 - 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="26845-120">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="26845-121">KeyVault - 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="26845-121">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="26845-122">DNS - 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="26845-122">Dns - 2016-04-01</span></span>
* <span data-ttu-id="26845-123">您可以在 https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json 中找到每個資源類型的完整 API 版本對應</span><span class="sxs-lookup"><span data-stu-id="26845-123">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="26845-124">內容：</span><span class="sxs-lookup"><span data-stu-id="26845-124">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="26845-125">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="26845-125">Azure Bridge</span></span>
<span data-ttu-id="26845-126">Azure Stack AzureBridge 管理員模組的預覽版本可讓您從 Azure 同步發佈映像。</span><span class="sxs-lookup"><span data-stu-id="26845-126">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="26845-127">Backup</span><span class="sxs-lookup"><span data-stu-id="26845-127">Backup</span></span>
<span data-ttu-id="26845-128">備份管理員模組的預覽版本可允許管理員：</span><span class="sxs-lookup"><span data-stu-id="26845-128">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="26845-129">設定備份的儲存位置</span><span class="sxs-lookup"><span data-stu-id="26845-129">Configure where backups are stored</span></span>
- <span data-ttu-id="26845-130">執行備份</span><span class="sxs-lookup"><span data-stu-id="26845-130">Perform backups</span></span>
- <span data-ttu-id="26845-131">列出並還原已完成的備份</span><span class="sxs-lookup"><span data-stu-id="26845-131">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="26845-132">商業</span><span class="sxs-lookup"><span data-stu-id="26845-132">Commerce</span></span>
<span data-ttu-id="26845-133">Azure Stack 商務管理員模組的預覽版本可提供方法來檢視 Azure Stack 系統間的彙總資料使用量。</span><span class="sxs-lookup"><span data-stu-id="26845-133">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="26845-134">計算</span><span class="sxs-lookup"><span data-stu-id="26845-134">Compute</span></span>
<span data-ttu-id="26845-135">Azure Stack 計算管理員模組的預覽版本可提供功能來管理計算配額、平台映像、受控磁碟和虛擬機器擴充功能。</span><span class="sxs-lookup"><span data-stu-id="26845-135">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="26845-136">網狀架構</span><span class="sxs-lookup"><span data-stu-id="26845-136">Fabric</span></span>
<span data-ttu-id="26845-137">Azure Stack 網狀架構管理員模組的預覽版本可讓系統管理員檢視和管理基礎結構元件：</span><span class="sxs-lookup"><span data-stu-id="26845-137">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="26845-138">縮放單位節點的停止、啟動和關閉</span><span class="sxs-lookup"><span data-stu-id="26845-138">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="26845-139">針對 FRU 相關活動清空和繼續縮放單位節點</span><span class="sxs-lookup"><span data-stu-id="26845-139">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="26845-140">縮放單位節點修復</span><span class="sxs-lookup"><span data-stu-id="26845-140">Repair of scale unit nodes</span></span>
- <span data-ttu-id="26845-141">基礎結構角色重新啟動</span><span class="sxs-lookup"><span data-stu-id="26845-141">Restart of Infrastructure role</span></span>
- <span data-ttu-id="26845-142">基礎結構角色執行個體的停止、啟動和關閉</span><span class="sxs-lookup"><span data-stu-id="26845-142">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="26845-143">建立新的 IP 集區</span><span class="sxs-lookup"><span data-stu-id="26845-143">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="26845-144">資源庫</span><span class="sxs-lookup"><span data-stu-id="26845-144">Gallery</span></span>
<span data-ttu-id="26845-145">Azure Stack 資源庫管理員模組的預覽版本可提供功能來管理 Azure Stack 市集中的資源庫項目。</span><span class="sxs-lookup"><span data-stu-id="26845-145">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="26845-146">基礎結構深入解析</span><span class="sxs-lookup"><span data-stu-id="26845-146">Infrastructure Insights</span></span>
<span data-ttu-id="26845-147">基礎結構深入解析管理員模組的預覽版本可讓系統管理員：</span><span class="sxs-lookup"><span data-stu-id="26845-147">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="26845-148">檢視其 Azure Stack 戳記資源的健康情況</span><span class="sxs-lookup"><span data-stu-id="26845-148">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="26845-149">檢視和管理警示</span><span class="sxs-lookup"><span data-stu-id="26845-149">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="26845-150">KeyVault</span><span class="sxs-lookup"><span data-stu-id="26845-150">KeyVault</span></span>
<span data-ttu-id="26845-151">Azure Stack KeyVault 管理員模組的預覽版本可讓系統管理員檢視 KeyVault 配額。</span><span class="sxs-lookup"><span data-stu-id="26845-151">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="26845-152">網路</span><span class="sxs-lookup"><span data-stu-id="26845-152">Network</span></span>
<span data-ttu-id="26845-153">網路管理員模組的預覽版本可以執行：</span><span class="sxs-lookup"><span data-stu-id="26845-153">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="26845-154">網路配額管理</span><span class="sxs-lookup"><span data-stu-id="26845-154">Management of network quotas</span></span>
- <span data-ttu-id="26845-155">檢視配置的網路資源，例如公用 IP 位址、虛擬網路、負載平衡器</span><span class="sxs-lookup"><span data-stu-id="26845-155">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="26845-156">提供 Cmdlet 以顯示系統管理員概觀</span><span class="sxs-lookup"><span data-stu-id="26845-156">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="26845-157">儲存體</span><span class="sxs-lookup"><span data-stu-id="26845-157">Storage</span></span>
<span data-ttu-id="26845-158">Azure Stack 儲存體管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="26845-158">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="26845-159">在此版本中，我們提供的功能有：</span><span class="sxs-lookup"><span data-stu-id="26845-159">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="26845-160">管理儲存體配額</span><span class="sxs-lookup"><span data-stu-id="26845-160">Manage storage quotas</span></span>
- <span data-ttu-id="26845-161">記憶體回收刪除的儲存體資源</span><span class="sxs-lookup"><span data-stu-id="26845-161">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="26845-162">還原已刪除的儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="26845-162">Restore deleted storage accounts</span></span>
- <span data-ttu-id="26845-163">將容器從一個共用遷移到另一個</span><span class="sxs-lookup"><span data-stu-id="26845-163">Migrate containers from one share to another</span></span>
- <span data-ttu-id="26845-164">檢視個別儲存元件的相關資訊</span><span class="sxs-lookup"><span data-stu-id="26845-164">View information about the individual storage components</span></span>
- <span data-ttu-id="26845-165">檢視使用量和效能資訊</span><span class="sxs-lookup"><span data-stu-id="26845-165">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="26845-166">訂用帳戶管理員</span><span class="sxs-lookup"><span data-stu-id="26845-166">Subscription Admin</span></span>
<span data-ttu-id="26845-167">Azure Stack 訂用帳戶管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="26845-167">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="26845-168">此模組可提供功能讓系統管理員：</span><span class="sxs-lookup"><span data-stu-id="26845-168">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="26845-169">管理方案和供應項目</span><span class="sxs-lookup"><span data-stu-id="26845-169">Manage plans and offers</span></span>
- <span data-ttu-id="26845-170">檢視使用量和效能資訊</span><span class="sxs-lookup"><span data-stu-id="26845-170">View usage and performance information</span></span>
- <span data-ttu-id="26845-171">管理 RBAC</span><span class="sxs-lookup"><span data-stu-id="26845-171">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="26845-172">訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="26845-172">Subscription</span></span>
<span data-ttu-id="26845-173">Azure Stack 訂用帳戶模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="26845-173">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="26845-174">此模組可提供功能讓使用者：</span><span class="sxs-lookup"><span data-stu-id="26845-174">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="26845-175">建立、刪除和更新訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="26845-175">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="26845-176">更新</span><span class="sxs-lookup"><span data-stu-id="26845-176">Update</span></span>
<span data-ttu-id="26845-177">Azure Stack 更新管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="26845-177">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="26845-178">在此模組中系統管理員可以：</span><span class="sxs-lookup"><span data-stu-id="26845-178">In this module administrators can:</span></span>
- <span data-ttu-id="26845-179">列出及安裝可用更新</span><span class="sxs-lookup"><span data-stu-id="26845-179">List and install available updates</span></span>
- <span data-ttu-id="26845-180">繼續中斷的更新</span><span class="sxs-lookup"><span data-stu-id="26845-180">Resume interrupted updates</span></span>
- <span data-ttu-id="26845-181">檢視已安裝的更新</span><span class="sxs-lookup"><span data-stu-id="26845-181">View installed updates</span></span>