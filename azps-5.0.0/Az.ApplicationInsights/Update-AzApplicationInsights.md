---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286171"
---
# <span data-ttu-id="0ed61-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="0ed61-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="0ed61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0ed61-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed61-103">更新現有的 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="0ed61-103">update an existing application insights resource</span></span>

## <span data-ttu-id="0ed61-104">句法</span><span class="sxs-lookup"><span data-stu-id="0ed61-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ed61-105">說明</span><span class="sxs-lookup"><span data-stu-id="0ed61-105">DESCRIPTION</span></span>
<span data-ttu-id="0ed61-106">更新現有的 application insights 資源</span><span class="sxs-lookup"><span data-stu-id="0ed61-106">update an existing application insights resource</span></span>

## <span data-ttu-id="0ed61-107">示例</span><span class="sxs-lookup"><span data-stu-id="0ed61-107">EXAMPLES</span></span>

### <span data-ttu-id="0ed61-108">範例1更新 application insights 元件</span><span class="sxs-lookup"><span data-stu-id="0ed61-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="0ed61-109">將 application insights 元件 "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery 更新為 "Disabled"</span><span class="sxs-lookup"><span data-stu-id="0ed61-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="0ed61-110">參數</span><span class="sxs-lookup"><span data-stu-id="0ed61-110">PARAMETERS</span></span>

### <span data-ttu-id="0ed61-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed61-111">-DefaultProfile</span></span>
<span data-ttu-id="0ed61-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0ed61-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ed61-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="0ed61-113">-Name</span></span>
<span data-ttu-id="0ed61-114">Application Insights 資源名稱。</span><span class="sxs-lookup"><span data-stu-id="0ed61-114">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed61-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="0ed61-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="0ed61-116">存取 Application Insights 攝取的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="0ed61-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="0ed61-117">值應為 [Enabled] 或 "Disabled"</span><span class="sxs-lookup"><span data-stu-id="0ed61-117">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed61-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="0ed61-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="0ed61-119">存取 Application Insights 查詢的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="0ed61-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="0ed61-120">值應為 [Enabled] 或 "Disabled"</span><span class="sxs-lookup"><span data-stu-id="0ed61-120">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed61-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ed61-121">-ResourceGroupName</span></span>
<span data-ttu-id="0ed61-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0ed61-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed61-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="0ed61-123">-RetentionInDays</span></span>
<span data-ttu-id="0ed61-124">保留天數、預設值為90。</span><span class="sxs-lookup"><span data-stu-id="0ed61-124">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed61-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="0ed61-125">-Tag</span></span>
<span data-ttu-id="0ed61-126">元件標記。</span><span class="sxs-lookup"><span data-stu-id="0ed61-126">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed61-127">-確認</span><span class="sxs-lookup"><span data-stu-id="0ed61-127">-Confirm</span></span>
<span data-ttu-id="0ed61-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0ed61-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ed61-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ed61-129">-WhatIf</span></span>
<span data-ttu-id="0ed61-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0ed61-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ed61-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0ed61-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ed61-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed61-132">CommonParameters</span></span>
<span data-ttu-id="0ed61-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0ed61-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed61-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0ed61-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed61-135">輸入</span><span class="sxs-lookup"><span data-stu-id="0ed61-135">INPUTS</span></span>

### <span data-ttu-id="0ed61-136">System.object</span><span class="sxs-lookup"><span data-stu-id="0ed61-136">System.String</span></span>

## <span data-ttu-id="0ed61-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0ed61-137">OUTPUTS</span></span>

### <span data-ttu-id="0ed61-138">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="0ed61-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="0ed61-139">筆記</span><span class="sxs-lookup"><span data-stu-id="0ed61-139">NOTES</span></span>

## <span data-ttu-id="0ed61-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ed61-140">RELATED LINKS</span></span>