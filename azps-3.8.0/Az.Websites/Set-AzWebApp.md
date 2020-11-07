---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 75ee07a9ce74f5b2667d8197ca141883508faa1e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958844"
---
# <span data-ttu-id="4185a-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4185a-101">Set-AzWebApp</span></span>

## <span data-ttu-id="4185a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4185a-102">SYNOPSIS</span></span>
<span data-ttu-id="4185a-103">修改 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="4185a-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="4185a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4185a-104">SYNTAX</span></span>

### <span data-ttu-id="4185a-105">S1</span><span class="sxs-lookup"><span data-stu-id="4185a-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>] [[-NetFrameworkVersion] <String>]
 [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>] [[-HttpLoggingEnabled] <Boolean>]
 [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>] [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-AzureStoragePath <WebAppAzureStoragePath[]>]
 [-AlwaysOn <Boolean>] [-MinTlsVersion <String>] [-FtpsState <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4185a-106">S2</span><span class="sxs-lookup"><span data-stu-id="4185a-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4185a-107">說明</span><span class="sxs-lookup"><span data-stu-id="4185a-107">DESCRIPTION</span></span>
<span data-ttu-id="4185a-108">**AzWebApp** Cmdlet 會設定 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="4185a-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="4185a-109">示例</span><span class="sxs-lookup"><span data-stu-id="4185a-109">EXAMPLES</span></span>

### <span data-ttu-id="4185a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="4185a-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="4185a-111">這個命令會變更與與資源群組預設-Web-WestUS 相關聯之 Web App ContosoWebApp 相關聯的 appservice 方案。</span><span class="sxs-lookup"><span data-stu-id="4185a-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="4185a-112">使用連結進一步瞭解如何變更與它相關聯的 appservice 方案和限制。</span><span class="sxs-lookup"><span data-stu-id="4185a-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="4185a-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="4185a-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="4185a-114">範例2</span><span class="sxs-lookup"><span data-stu-id="4185a-114">Example 2</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="4185a-115">這個命令會將與資源群組預設的 Web App ContosoWebApp 的 HttpLoggingEnabled 設定為 true （Web-WestUS）</span><span class="sxs-lookup"><span data-stu-id="4185a-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="4185a-116">參數</span><span class="sxs-lookup"><span data-stu-id="4185a-116">PARAMETERS</span></span>

### <span data-ttu-id="4185a-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="4185a-117">-AlwaysOn</span></span>
<span data-ttu-id="4185a-118">確保所有時間都會載入 web 應用程式，而不是在空閒後卸載。</span><span class="sxs-lookup"><span data-stu-id="4185a-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4185a-119">-AppServicePlan</span></span>
<span data-ttu-id="4185a-120">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="4185a-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="4185a-121">-AppSettings</span></span>
<span data-ttu-id="4185a-122">App 設定雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4185a-122">App Settings HashTable.</span></span> <span data-ttu-id="4185a-123">現有的應用程式設定將會取代，移除任何未提供的設定。</span><span class="sxs-lookup"><span data-stu-id="4185a-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4185a-124">-AsJob</span></span>
<span data-ttu-id="4185a-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4185a-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4185a-126">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="4185a-126">-AssignIdentity</span></span>
<span data-ttu-id="4185a-127">啟用/停用現有 azure webapp 或 functionapp 上的 MSI</span><span class="sxs-lookup"><span data-stu-id="4185a-127">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="4185a-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="4185a-129">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="4185a-129">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="4185a-130">-AzureStoragePath</span></span>
<span data-ttu-id="4185a-131">[Azure 儲存空間] 可在容器的 Web App 內裝載。</span><span class="sxs-lookup"><span data-stu-id="4185a-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="4185a-132">使用 New-AzureRmWebAppAzureStoragePath 建立</span><span class="sxs-lookup"><span data-stu-id="4185a-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-133">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="4185a-133">-ConnectionStrings</span></span>
<span data-ttu-id="4185a-134">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="4185a-134">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-135">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="4185a-135">-ContainerImageName</span></span>
<span data-ttu-id="4185a-136">容器圖像名稱</span><span class="sxs-lookup"><span data-stu-id="4185a-136">Container Image Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="4185a-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="4185a-138">私人容器註冊密碼</span><span class="sxs-lookup"><span data-stu-id="4185a-138">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="4185a-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="4185a-140">私人容器登錄伺服器 Url</span><span class="sxs-lookup"><span data-stu-id="4185a-140">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="4185a-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="4185a-142">私人容器註冊使用者名稱</span><span class="sxs-lookup"><span data-stu-id="4185a-142">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-143">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="4185a-143">-DefaultDocuments</span></span>
<span data-ttu-id="4185a-144">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="4185a-144">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4185a-145">-DefaultProfile</span></span>
<span data-ttu-id="4185a-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4185a-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4185a-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="4185a-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="4185a-148">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="4185a-148">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="4185a-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="4185a-150">啟用/停用容器連續部署 webhook</span><span class="sxs-lookup"><span data-stu-id="4185a-150">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-151">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="4185a-151">-FtpsState</span></span>
<span data-ttu-id="4185a-152">設定應用程式的 Ftps 狀態值。</span><span class="sxs-lookup"><span data-stu-id="4185a-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="4185a-153">允許的值 [AllAllowed |已停用 |FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="4185a-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="4185a-154">-HandlerMappings</span></span>
<span data-ttu-id="4185a-155">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="4185a-155">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: S1
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-156">-主機名稱</span><span class="sxs-lookup"><span data-stu-id="4185a-156">-HostNames</span></span>
<span data-ttu-id="4185a-157">WebApp 主機名稱字串陣列</span><span class="sxs-lookup"><span data-stu-id="4185a-157">WebApp HostNames String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-158">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="4185a-158">-HttpLoggingEnabled</span></span>
<span data-ttu-id="4185a-159">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="4185a-159">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-160">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="4185a-160">-HttpsOnly</span></span>
<span data-ttu-id="4185a-161">啟用/停用現有 azure webapp 或 functionapp 上的所有流量重定向至 HTTPS</span><span class="sxs-lookup"><span data-stu-id="4185a-161">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-162">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="4185a-162">-ManagedPipelineMode</span></span>
<span data-ttu-id="4185a-163">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="4185a-163">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-164">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="4185a-164">-MinTlsVersion</span></span>
<span data-ttu-id="4185a-165">SSL 要求所需的最小 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="4185a-165">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="4185a-166">允許值 [1.0 | 1.1 | 1.2]。</span><span class="sxs-lookup"><span data-stu-id="4185a-166">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-167">-名稱</span><span class="sxs-lookup"><span data-stu-id="4185a-167">-Name</span></span>
<span data-ttu-id="4185a-168">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="4185a-168">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-169">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="4185a-169">-NetFrameworkVersion</span></span>
<span data-ttu-id="4185a-170">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="4185a-170">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-171">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="4185a-171">-NumberOfWorkers</span></span>
<span data-ttu-id="4185a-172">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="4185a-172">The number of workers to be allocated</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-173">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="4185a-173">-PhpVersion</span></span>
<span data-ttu-id="4185a-174">Php 版本</span><span class="sxs-lookup"><span data-stu-id="4185a-174">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-175">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="4185a-175">-RequestTracingEnabled</span></span>
<span data-ttu-id="4185a-176">已啟用要求追蹤</span><span class="sxs-lookup"><span data-stu-id="4185a-176">Request Tracing Enabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4185a-177">-ResourceGroupName</span></span>
<span data-ttu-id="4185a-178">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="4185a-178">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="4185a-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="4185a-180">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="4185a-180">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-181">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4185a-181">-WebApp</span></span>
<span data-ttu-id="4185a-182">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="4185a-182">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="4185a-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="4185a-184">WebSocketsEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="4185a-184">WebSocketsEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4185a-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4185a-185">CommonParameters</span></span>
<span data-ttu-id="4185a-186">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4185a-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4185a-187">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4185a-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4185a-188">輸入</span><span class="sxs-lookup"><span data-stu-id="4185a-188">INPUTS</span></span>

### <span data-ttu-id="4185a-189">System.object</span><span class="sxs-lookup"><span data-stu-id="4185a-189">System.Int32</span></span>

### <span data-ttu-id="4185a-190">System.object</span><span class="sxs-lookup"><span data-stu-id="4185a-190">System.String</span></span>

### <span data-ttu-id="4185a-191">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="4185a-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4185a-192">輸出</span><span class="sxs-lookup"><span data-stu-id="4185a-192">OUTPUTS</span></span>

### <span data-ttu-id="4185a-193">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="4185a-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4185a-194">筆記</span><span class="sxs-lookup"><span data-stu-id="4185a-194">NOTES</span></span>

## <span data-ttu-id="4185a-195">相關連結</span><span class="sxs-lookup"><span data-stu-id="4185a-195">RELATED LINKS</span></span>

[<span data-ttu-id="4185a-196">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4185a-196">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="4185a-197">新-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4185a-197">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="4185a-198">移除-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4185a-198">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="4185a-199">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4185a-199">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="4185a-200">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4185a-200">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="4185a-201">停止 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4185a-201">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)