---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: d053bc60390c43c3409bb7adfad5a3ff3720f5b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288396"
---
# <span data-ttu-id="40bd1-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="40bd1-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="40bd1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40bd1-102">SYNOPSIS</span></span>
<span data-ttu-id="40bd1-103">配置 API 管理閘道。</span><span class="sxs-lookup"><span data-stu-id="40bd1-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="40bd1-104">句法</span><span class="sxs-lookup"><span data-stu-id="40bd1-104">SYNTAX</span></span>

### <span data-ttu-id="40bd1-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="40bd1-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40bd1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="40bd1-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40bd1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="40bd1-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40bd1-108">說明</span><span class="sxs-lookup"><span data-stu-id="40bd1-108">DESCRIPTION</span></span>
<span data-ttu-id="40bd1-109">**AzApiManagementGateway** Cmdlet 會配置 API 管理閘道。</span><span class="sxs-lookup"><span data-stu-id="40bd1-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="40bd1-110">示例</span><span class="sxs-lookup"><span data-stu-id="40bd1-110">EXAMPLES</span></span>

### <span data-ttu-id="40bd1-111">範例1：設定管理群組</span><span class="sxs-lookup"><span data-stu-id="40bd1-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="40bd1-112">這個命令會配置閘道。</span><span class="sxs-lookup"><span data-stu-id="40bd1-112">This command configures a gateway.</span></span>

## <span data-ttu-id="40bd1-113">參數</span><span class="sxs-lookup"><span data-stu-id="40bd1-113">PARAMETERS</span></span>

### <span data-ttu-id="40bd1-114">-內容</span><span class="sxs-lookup"><span data-stu-id="40bd1-114">-Context</span></span>
<span data-ttu-id="40bd1-115">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="40bd1-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="40bd1-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="40bd1-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40bd1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40bd1-117">-DefaultProfile</span></span>
<span data-ttu-id="40bd1-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="40bd1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40bd1-119">-描述</span><span class="sxs-lookup"><span data-stu-id="40bd1-119">-Description</span></span>
<span data-ttu-id="40bd1-120">閘道描述。</span><span class="sxs-lookup"><span data-stu-id="40bd1-120">Gateway description.</span></span>
<span data-ttu-id="40bd1-121">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="40bd1-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="40bd1-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="40bd1-122">-GatewayId</span></span>
<span data-ttu-id="40bd1-123">現有閘道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="40bd1-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="40bd1-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="40bd1-124">This parameter is required.</span></span>

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

### <span data-ttu-id="40bd1-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40bd1-125">-InputObject</span></span>
<span data-ttu-id="40bd1-126">PsApiManagementGateway 的實例。</span><span class="sxs-lookup"><span data-stu-id="40bd1-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="40bd1-127">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="40bd1-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40bd1-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="40bd1-128">-LocationData</span></span>
<span data-ttu-id="40bd1-129">閘道位置。</span><span class="sxs-lookup"><span data-stu-id="40bd1-129">Gateway location.</span></span>
<span data-ttu-id="40bd1-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="40bd1-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40bd1-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40bd1-131">-PassThru</span></span>
<span data-ttu-id="40bd1-132">如果已指定 ApiManagement，則 ServiceManagement 代表已修改閘道的 PsApiManagementGateway 類型。</span><span class="sxs-lookup"><span data-stu-id="40bd1-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="40bd1-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40bd1-133">-ResourceId</span></span>
<span data-ttu-id="40bd1-134">閘道的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="40bd1-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="40bd1-135">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="40bd1-135">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40bd1-136">-確認</span><span class="sxs-lookup"><span data-stu-id="40bd1-136">-Confirm</span></span>
<span data-ttu-id="40bd1-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="40bd1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40bd1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40bd1-138">-WhatIf</span></span>
<span data-ttu-id="40bd1-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40bd1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40bd1-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40bd1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40bd1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40bd1-141">CommonParameters</span></span>
<span data-ttu-id="40bd1-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40bd1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40bd1-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="40bd1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40bd1-144">輸入</span><span class="sxs-lookup"><span data-stu-id="40bd1-144">INPUTS</span></span>

### <span data-ttu-id="40bd1-145">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="40bd1-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="40bd1-146">System.object</span><span class="sxs-lookup"><span data-stu-id="40bd1-146">System.String</span></span>

### <span data-ttu-id="40bd1-147">ServiceManagement. PsApiManagementResourceLocation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="40bd1-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="40bd1-148">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="40bd1-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="40bd1-149">輸出</span><span class="sxs-lookup"><span data-stu-id="40bd1-149">OUTPUTS</span></span>

### <span data-ttu-id="40bd1-150">ServiceManagement. PsApiManagementGateway （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="40bd1-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="40bd1-151">筆記</span><span class="sxs-lookup"><span data-stu-id="40bd1-151">NOTES</span></span>

## <span data-ttu-id="40bd1-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="40bd1-152">RELATED LINKS</span></span>