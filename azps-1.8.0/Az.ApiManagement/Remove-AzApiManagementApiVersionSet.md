---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 681ce525d1d00802cc226539fd9c3014c1786098
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788874"
---
# <span data-ttu-id="5e813-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="5e813-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="5e813-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e813-102">SYNOPSIS</span></span>
<span data-ttu-id="5e813-103">移除特定 Api 版本集</span><span class="sxs-lookup"><span data-stu-id="5e813-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="5e813-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e813-104">SYNTAX</span></span>

### <span data-ttu-id="5e813-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="5e813-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e813-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5e813-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e813-107">說明</span><span class="sxs-lookup"><span data-stu-id="5e813-107">DESCRIPTION</span></span>

<span data-ttu-id="5e813-108">AzAzureRmApiManagementApiVersionSet Cmdlet 會移除現有 **的** API 版本集。</span><span class="sxs-lookup"><span data-stu-id="5e813-108">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="5e813-109">示例</span><span class="sxs-lookup"><span data-stu-id="5e813-109">EXAMPLES</span></span>

### <span data-ttu-id="5e813-110">範例1：移除 API 版本集</span><span class="sxs-lookup"><span data-stu-id="5e813-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="5e813-111">這個命令會以指定的 ApiVersionSetId 移除 API 版本設定。</span><span class="sxs-lookup"><span data-stu-id="5e813-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="5e813-112">參數</span><span class="sxs-lookup"><span data-stu-id="5e813-112">PARAMETERS</span></span>

### <span data-ttu-id="5e813-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="5e813-113">-ApiVersionSetId</span></span>
<span data-ttu-id="5e813-114">API 版本集的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e813-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="5e813-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="5e813-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e813-116">-內容</span><span class="sxs-lookup"><span data-stu-id="5e813-116">-Context</span></span>
<span data-ttu-id="5e813-117">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="5e813-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5e813-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="5e813-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e813-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e813-119">-DefaultProfile</span></span>
<span data-ttu-id="5e813-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e813-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e813-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e813-121">-InputObject</span></span>
<span data-ttu-id="5e813-122">PsApiManagementApiVersionSet 的實例。</span><span class="sxs-lookup"><span data-stu-id="5e813-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="5e813-123">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="5e813-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e813-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e813-124">-PassThru</span></span>
<span data-ttu-id="5e813-125">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="5e813-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="5e813-126">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="5e813-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="5e813-127">-確認</span><span class="sxs-lookup"><span data-stu-id="5e813-127">-Confirm</span></span>
<span data-ttu-id="5e813-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5e813-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e813-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e813-129">-WhatIf</span></span>
<span data-ttu-id="5e813-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5e813-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e813-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5e813-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e813-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e813-132">CommonParameters</span></span>
<span data-ttu-id="5e813-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e813-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e813-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e813-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e813-135">輸入</span><span class="sxs-lookup"><span data-stu-id="5e813-135">INPUTS</span></span>

### <span data-ttu-id="5e813-136">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="5e813-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5e813-137">ServiceManagement. PsApiManagementApiVersionSet （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="5e813-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="5e813-138">System.object</span><span class="sxs-lookup"><span data-stu-id="5e813-138">System.String</span></span>

## <span data-ttu-id="5e813-139">輸出</span><span class="sxs-lookup"><span data-stu-id="5e813-139">OUTPUTS</span></span>

### <span data-ttu-id="5e813-140">System.object</span><span class="sxs-lookup"><span data-stu-id="5e813-140">System.Boolean</span></span>

## <span data-ttu-id="5e813-141">筆記</span><span class="sxs-lookup"><span data-stu-id="5e813-141">NOTES</span></span>

## <span data-ttu-id="5e813-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e813-142">RELATED LINKS</span></span>

[<span data-ttu-id="5e813-143">AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="5e813-143">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="5e813-144">新-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="5e813-144">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="5e813-145">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="5e813-145">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)