---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 0265a273cb575d2cc3a165afae8f7a2090499cdc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623101"
---
# <span data-ttu-id="0a80d-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="0a80d-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="0a80d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a80d-102">SYNOPSIS</span></span>
<span data-ttu-id="0a80d-103">在 application insights 資源中移除 cotinuous 匯出配置</span><span class="sxs-lookup"><span data-stu-id="0a80d-103">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="0a80d-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a80d-104">SYNTAX</span></span>

### <span data-ttu-id="0a80d-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0a80d-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a80d-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a80d-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a80d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a80d-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a80d-108">說明</span><span class="sxs-lookup"><span data-stu-id="0a80d-108">DESCRIPTION</span></span>
<span data-ttu-id="0a80d-109">在 application insights 資源中移除 cotinuous 匯出配置</span><span class="sxs-lookup"><span data-stu-id="0a80d-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="0a80d-110">示例</span><span class="sxs-lookup"><span data-stu-id="0a80d-110">EXAMPLES</span></span>

### <span data-ttu-id="0a80d-111">範例1在 application insights 資源中移除 cotinuous 匯出配置</span><span class="sxs-lookup"><span data-stu-id="0a80d-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="0a80d-112">針對資源群組 "testgroup" 中名為 "test" 的資源，移除含匯出 id "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" 的 application insights 連續匯出設定</span><span class="sxs-lookup"><span data-stu-id="0a80d-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="0a80d-113">參數</span><span class="sxs-lookup"><span data-stu-id="0a80d-113">PARAMETERS</span></span>

### <span data-ttu-id="0a80d-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0a80d-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="0a80d-115">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="0a80d-115">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a80d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a80d-116">-DefaultProfile</span></span>
<span data-ttu-id="0a80d-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a80d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a80d-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="0a80d-118">-ExportId</span></span>
<span data-ttu-id="0a80d-119">Application Insights 連續匯出 ID。</span><span class="sxs-lookup"><span data-stu-id="0a80d-119">Application Insights Continuous Export ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a80d-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a80d-120">-Name</span></span>
<span data-ttu-id="0a80d-121">Application Insights 元件名稱。</span><span class="sxs-lookup"><span data-stu-id="0a80d-121">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a80d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a80d-122">-PassThru</span></span>
<span data-ttu-id="0a80d-123">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="0a80d-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="0a80d-124">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="0a80d-124">This parameter is optional.</span></span> <span data-ttu-id="0a80d-125">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="0a80d-125">Default value is false.</span></span>

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

### <span data-ttu-id="0a80d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a80d-126">-ResourceGroupName</span></span>
<span data-ttu-id="0a80d-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0a80d-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a80d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a80d-128">-ResourceId</span></span>
<span data-ttu-id="0a80d-129">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a80d-129">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a80d-130">-確認</span><span class="sxs-lookup"><span data-stu-id="0a80d-130">-Confirm</span></span>
<span data-ttu-id="0a80d-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0a80d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a80d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a80d-132">-WhatIf</span></span>
<span data-ttu-id="0a80d-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a80d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a80d-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a80d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a80d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a80d-135">CommonParameters</span></span>
<span data-ttu-id="0a80d-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a80d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a80d-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0a80d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a80d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0a80d-138">INPUTS</span></span>

### <span data-ttu-id="0a80d-139">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="0a80d-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="0a80d-140">System.object</span><span class="sxs-lookup"><span data-stu-id="0a80d-140">System.String</span></span>

## <span data-ttu-id="0a80d-141">輸出</span><span class="sxs-lookup"><span data-stu-id="0a80d-141">OUTPUTS</span></span>

### <span data-ttu-id="0a80d-142">System.object</span><span class="sxs-lookup"><span data-stu-id="0a80d-142">System.Boolean</span></span>

## <span data-ttu-id="0a80d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="0a80d-143">NOTES</span></span>

## <span data-ttu-id="0a80d-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a80d-144">RELATED LINKS</span></span>