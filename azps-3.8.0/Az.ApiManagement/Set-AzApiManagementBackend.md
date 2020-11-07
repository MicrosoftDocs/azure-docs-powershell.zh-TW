---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 30947e52e5a7afaa8bf2890b95f48f6bb6f36bce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959801"
---
# <span data-ttu-id="956c6-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="956c6-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="956c6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="956c6-102">SYNOPSIS</span></span>
<span data-ttu-id="956c6-103">更新後端。</span><span class="sxs-lookup"><span data-stu-id="956c6-103">Updates a Backend.</span></span>

## <span data-ttu-id="956c6-104">句法</span><span class="sxs-lookup"><span data-stu-id="956c6-104">SYNTAX</span></span>

### <span data-ttu-id="956c6-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="956c6-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="956c6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="956c6-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="956c6-107">說明</span><span class="sxs-lookup"><span data-stu-id="956c6-107">DESCRIPTION</span></span>
<span data-ttu-id="956c6-108">在 Api 管理中更新現有的後端。</span><span class="sxs-lookup"><span data-stu-id="956c6-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="956c6-109">示例</span><span class="sxs-lookup"><span data-stu-id="956c6-109">EXAMPLES</span></span>

### <span data-ttu-id="956c6-110">更新後端123的描述</span><span class="sxs-lookup"><span data-stu-id="956c6-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="956c6-111">參數</span><span class="sxs-lookup"><span data-stu-id="956c6-111">PARAMETERS</span></span>

### <span data-ttu-id="956c6-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="956c6-112">-BackendId</span></span>
<span data-ttu-id="956c6-113">新後端的識別碼。</span><span class="sxs-lookup"><span data-stu-id="956c6-113">Identifier of new backend.</span></span>
<span data-ttu-id="956c6-114">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="956c6-114">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956c6-115">-內容</span><span class="sxs-lookup"><span data-stu-id="956c6-115">-Context</span></span>
<span data-ttu-id="956c6-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="956c6-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="956c6-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="956c6-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="956c6-118">-認證</span><span class="sxs-lookup"><span data-stu-id="956c6-118">-Credential</span></span>
<span data-ttu-id="956c6-119">在與後端交談時應使用的認證詳細資料。</span><span class="sxs-lookup"><span data-stu-id="956c6-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="956c6-120">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="956c6-120">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956c6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="956c6-121">-DefaultProfile</span></span>
<span data-ttu-id="956c6-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="956c6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="956c6-123">-描述</span><span class="sxs-lookup"><span data-stu-id="956c6-123">-Description</span></span>
<span data-ttu-id="956c6-124">後端描述。</span><span class="sxs-lookup"><span data-stu-id="956c6-124">Backend Description.</span></span>
<span data-ttu-id="956c6-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="956c6-125">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956c6-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="956c6-126">-InputObject</span></span>
<span data-ttu-id="956c6-127">PsApiManagementBackend 的實例。</span><span class="sxs-lookup"><span data-stu-id="956c6-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="956c6-128">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="956c6-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="956c6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="956c6-129">-PassThru</span></span>
<span data-ttu-id="956c6-130">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的  **PsApiManagementBackend** 。</span><span class="sxs-lookup"><span data-stu-id="956c6-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956c6-131">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="956c6-131">-Protocol</span></span>
<span data-ttu-id="956c6-132">後端通訊通訊協定 (HTTP 或 soap) 。</span><span class="sxs-lookup"><span data-stu-id="956c6-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="956c6-133">此參數為選用。</span><span class="sxs-lookup"><span data-stu-id="956c6-133">This parameter is optional</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956c6-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="956c6-134">-Proxy</span></span>
<span data-ttu-id="956c6-135">傳送要求給後所要使用的 Proxy 伺服器詳細資料。</span><span class="sxs-lookup"><span data-stu-id="956c6-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="956c6-136">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="956c6-136">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956c6-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="956c6-137">-ResourceId</span></span>
<span data-ttu-id="956c6-138">外部系統中資源的管理 Uri。</span><span class="sxs-lookup"><span data-stu-id="956c6-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="956c6-139">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="956c6-139">This parameter is optional.</span></span>
<span data-ttu-id="956c6-140">此 url 可以是邏輯 App、函數 App 或 Api App 的 Arm 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="956c6-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956c6-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="956c6-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="956c6-142">Service Fabric 群集後端詳細資料。</span><span class="sxs-lookup"><span data-stu-id="956c6-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="956c6-143">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="956c6-143">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956c6-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="956c6-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="956c6-145">在與後端交談時，是否略過憑證連結驗證。</span><span class="sxs-lookup"><span data-stu-id="956c6-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="956c6-146">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="956c6-146">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956c6-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="956c6-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="956c6-148">在與後端交談時，是否略過憑證名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="956c6-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="956c6-149">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="956c6-149">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956c6-150">-標題</span><span class="sxs-lookup"><span data-stu-id="956c6-150">-Title</span></span>
<span data-ttu-id="956c6-151">後端標題。</span><span class="sxs-lookup"><span data-stu-id="956c6-151">Backend Title.</span></span>
<span data-ttu-id="956c6-152">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="956c6-152">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956c6-153">-Url</span><span class="sxs-lookup"><span data-stu-id="956c6-153">-Url</span></span>
<span data-ttu-id="956c6-154">後端的執行時間 Url。</span><span class="sxs-lookup"><span data-stu-id="956c6-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="956c6-155">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="956c6-155">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956c6-156">-確認</span><span class="sxs-lookup"><span data-stu-id="956c6-156">-Confirm</span></span>
<span data-ttu-id="956c6-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="956c6-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="956c6-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="956c6-158">-WhatIf</span></span>
<span data-ttu-id="956c6-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="956c6-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="956c6-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="956c6-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="956c6-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="956c6-161">CommonParameters</span></span>
<span data-ttu-id="956c6-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="956c6-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="956c6-163">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="956c6-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="956c6-164">輸入</span><span class="sxs-lookup"><span data-stu-id="956c6-164">INPUTS</span></span>

### <span data-ttu-id="956c6-165">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="956c6-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="956c6-166">System.object</span><span class="sxs-lookup"><span data-stu-id="956c6-166">System.String</span></span>

### <span data-ttu-id="956c6-167">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="956c6-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="956c6-168">ServiceManagement. PsApiManagementBackendCredential （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="956c6-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="956c6-169">ServiceManagement. PsApiManagementBackendProxy （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="956c6-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="956c6-170">ServiceManagement. PsApiManagementServiceFabric （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="956c6-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="956c6-171">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="956c6-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="956c6-172">輸出</span><span class="sxs-lookup"><span data-stu-id="956c6-172">OUTPUTS</span></span>

### <span data-ttu-id="956c6-173">ServiceManagement. PsApiManagementBackend （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="956c6-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="956c6-174">筆記</span><span class="sxs-lookup"><span data-stu-id="956c6-174">NOTES</span></span>

## <span data-ttu-id="956c6-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="956c6-175">RELATED LINKS</span></span>

[<span data-ttu-id="956c6-176">AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="956c6-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="956c6-177">新-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="956c6-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="956c6-178">新-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="956c6-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="956c6-179">新-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="956c6-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="956c6-180">移除-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="956c6-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)