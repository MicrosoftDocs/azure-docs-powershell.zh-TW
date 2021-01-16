---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288888"
---
# <span data-ttu-id="572fc-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="572fc-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="572fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="572fc-102">SYNOPSIS</span></span>
<span data-ttu-id="572fc-103">將 web 服務定義物件匯出為 JSON 格式字串。</span><span class="sxs-lookup"><span data-stu-id="572fc-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="572fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="572fc-104">SYNTAX</span></span>

### <span data-ttu-id="572fc-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="572fc-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="572fc-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="572fc-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="572fc-107">說明</span><span class="sxs-lookup"><span data-stu-id="572fc-107">DESCRIPTION</span></span>
<span data-ttu-id="572fc-108">以 JSON 格式字串的形式匯出指定 web 服務的定義物件。</span><span class="sxs-lookup"><span data-stu-id="572fc-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="572fc-109">您可以立即傳回字串，或將它儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="572fc-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="572fc-110">示例</span><span class="sxs-lookup"><span data-stu-id="572fc-110">EXAMPLES</span></span>

### <span data-ttu-id="572fc-111">範例1：匯出為字串</span><span class="sxs-lookup"><span data-stu-id="572fc-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="572fc-112">範例2：匯出至檔案</span><span class="sxs-lookup"><span data-stu-id="572fc-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="572fc-113">參數</span><span class="sxs-lookup"><span data-stu-id="572fc-113">PARAMETERS</span></span>

### <span data-ttu-id="572fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="572fc-114">-DefaultProfile</span></span>
<span data-ttu-id="572fc-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="572fc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="572fc-116">-Force</span><span class="sxs-lookup"><span data-stu-id="572fc-116">-Force</span></span>
<span data-ttu-id="572fc-117">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="572fc-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="572fc-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="572fc-118">-OutputFile</span></span>
<span data-ttu-id="572fc-119">匯出定義的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="572fc-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572fc-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="572fc-120">-ToJsonString</span></span>
<span data-ttu-id="572fc-121">指定定義將匯出為 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="572fc-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToJSON
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572fc-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="572fc-122">-WebService</span></span>
<span data-ttu-id="572fc-123">要匯出的 web 服務定義物件。</span><span class="sxs-lookup"><span data-stu-id="572fc-123">The web service definition object to be exported.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="572fc-124">-確認</span><span class="sxs-lookup"><span data-stu-id="572fc-124">-Confirm</span></span>
<span data-ttu-id="572fc-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="572fc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="572fc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="572fc-126">-WhatIf</span></span>
<span data-ttu-id="572fc-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="572fc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="572fc-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="572fc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="572fc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="572fc-129">CommonParameters</span></span>
<span data-ttu-id="572fc-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="572fc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="572fc-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="572fc-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="572fc-132">輸入</span><span class="sxs-lookup"><span data-stu-id="572fc-132">INPUTS</span></span>

### <span data-ttu-id="572fc-133">[MachineLearning] WebServices 的 Web 元件</span><span class="sxs-lookup"><span data-stu-id="572fc-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="572fc-134">輸出</span><span class="sxs-lookup"><span data-stu-id="572fc-134">OUTPUTS</span></span>

### <span data-ttu-id="572fc-135">System.object</span><span class="sxs-lookup"><span data-stu-id="572fc-135">System.String</span></span>

## <span data-ttu-id="572fc-136">筆記</span><span class="sxs-lookup"><span data-stu-id="572fc-136">NOTES</span></span>
<span data-ttu-id="572fc-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="572fc-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="572fc-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="572fc-138">RELATED LINKS</span></span>