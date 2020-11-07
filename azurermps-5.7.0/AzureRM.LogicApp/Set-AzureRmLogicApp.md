---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
ms.openlocfilehash: 1f98fb17f6dc5604dfd19faeb9b9d6ec54e859c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626440"
---
# <span data-ttu-id="2a75f-101">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2a75f-101">Set-AzureRmLogicApp</span></span>

## <span data-ttu-id="2a75f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a75f-102">SYNOPSIS</span></span>
<span data-ttu-id="2a75f-103">修改資源群組中的邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="2a75f-103">Modifies a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a75f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a75f-104">SYNTAX</span></span>

### <span data-ttu-id="2a75f-105">預設)  (消耗量</span><span class="sxs-lookup"><span data-stu-id="2a75f-105">Consumption (Default)</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a75f-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="2a75f-106">HostingPlan</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a75f-107">說明</span><span class="sxs-lookup"><span data-stu-id="2a75f-107">DESCRIPTION</span></span>
<span data-ttu-id="2a75f-108">**AzureRmLogicApp** Cmdlet 會使用邏輯應用程式功能來修改邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="2a75f-108">The **Set-AzureRmLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="2a75f-109">邏輯 app 是在邏輯應用程式定義中定義的動作或觸發程式的集合。</span><span class="sxs-lookup"><span data-stu-id="2a75f-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="2a75f-110">這個 Cmdlet 會傳回 **工作流程** 物件。</span><span class="sxs-lookup"><span data-stu-id="2a75f-110">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="2a75f-111">您可以透過指定名稱、位置、邏輯應用程式定義、資源群組和規劃來修改邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="2a75f-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="2a75f-112">邏輯應用程式定義和參數的格式設定為 JavaScript 物件符號 (JSON) 。</span><span class="sxs-lookup"><span data-stu-id="2a75f-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="2a75f-113">您可以使用邏輯 app 做為定義與參數的範本。</span><span class="sxs-lookup"><span data-stu-id="2a75f-113">You can use a logic app as a template for definition and parameters.</span></span>

<span data-ttu-id="2a75f-114">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="2a75f-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2a75f-115">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="2a75f-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2a75f-116">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="2a75f-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2a75f-117">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="2a75f-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="2a75f-118">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="2a75f-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="2a75f-119">示例</span><span class="sxs-lookup"><span data-stu-id="2a75f-119">EXAMPLES</span></span>

### <span data-ttu-id="2a75f-120">範例1：修改邏輯 app</span><span class="sxs-lookup"><span data-stu-id="2a75f-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp1
Name                         : LogicApp17
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp17
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan17
Version                      : 08587489107859952120
```

<span data-ttu-id="2a75f-121">這個命令會修改邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="2a75f-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="2a75f-122">參數</span><span class="sxs-lookup"><span data-stu-id="2a75f-122">PARAMETERS</span></span>

### <span data-ttu-id="2a75f-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2a75f-123">-AppServicePlan</span></span>
<span data-ttu-id="2a75f-124">指定方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a75f-124">Specifies the name of a plan.</span></span>

```yaml
Type: String
Parameter Sets: HostingPlan
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a75f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a75f-125">-DefaultProfile</span></span>
<span data-ttu-id="2a75f-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2a75f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a75f-127">-定義</span><span class="sxs-lookup"><span data-stu-id="2a75f-127">-Definition</span></span>
<span data-ttu-id="2a75f-128">將邏輯 app 的定義指定為 JavaScript 物件符號 (JSON) 格式中的物件或字串。</span><span class="sxs-lookup"><span data-stu-id="2a75f-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a75f-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="2a75f-129">-DefinitionFilePath</span></span>
<span data-ttu-id="2a75f-130">將邏輯 app 的定義指定為 JSON 格式的定義檔路徑。</span><span class="sxs-lookup"><span data-stu-id="2a75f-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a75f-131">-Force</span><span class="sxs-lookup"><span data-stu-id="2a75f-131">-Force</span></span>
<span data-ttu-id="2a75f-132">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2a75f-132">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a75f-133">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="2a75f-133">-IntegrationAccountId</span></span>
<span data-ttu-id="2a75f-134">指定邏輯 app 的整合帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="2a75f-134">Specifies an integration account ID for the logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a75f-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a75f-135">-Name</span></span>
<span data-ttu-id="2a75f-136">指定邏輯應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a75f-136">Specifies the name of a logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a75f-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="2a75f-137">-ParameterFilePath</span></span>
<span data-ttu-id="2a75f-138">指定 JSON 格式化參數檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="2a75f-138">Specifies the path of a JSON formatted parameter file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a75f-139">-參數</span><span class="sxs-lookup"><span data-stu-id="2a75f-139">-Parameters</span></span>
<span data-ttu-id="2a75f-140">指定邏輯 App 的參數集合物件。</span><span class="sxs-lookup"><span data-stu-id="2a75f-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="2a75f-141">指定雜湊資料表、字典 \<string\> 或字典 \<string, WorkflowParameter\> 。</span><span class="sxs-lookup"><span data-stu-id="2a75f-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a75f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a75f-142">-ResourceGroupName</span></span>
<span data-ttu-id="2a75f-143">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a75f-143">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a75f-144">-State</span><span class="sxs-lookup"><span data-stu-id="2a75f-144">-State</span></span>
<span data-ttu-id="2a75f-145">指定邏輯 app 的狀態。</span><span class="sxs-lookup"><span data-stu-id="2a75f-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="2a75f-146">此參數可接受的值為： [已啟用] 和 [已停用]。</span><span class="sxs-lookup"><span data-stu-id="2a75f-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a75f-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="2a75f-147">-UseConsumptionModel</span></span>
<span data-ttu-id="2a75f-148">表示邏輯 app 帳單使用的是以消耗量為基礎的模型。</span><span class="sxs-lookup"><span data-stu-id="2a75f-148">Indicates that the logic app billing use the consumption based model.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Consumption
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a75f-149">-確認</span><span class="sxs-lookup"><span data-stu-id="2a75f-149">-Confirm</span></span>
<span data-ttu-id="2a75f-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2a75f-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a75f-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a75f-151">-WhatIf</span></span>
<span data-ttu-id="2a75f-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a75f-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a75f-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a75f-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a75f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a75f-154">CommonParameters</span></span>
<span data-ttu-id="2a75f-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a75f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a75f-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a75f-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a75f-157">輸入</span><span class="sxs-lookup"><span data-stu-id="2a75f-157">INPUTS</span></span>

### <span data-ttu-id="2a75f-158">所有</span><span class="sxs-lookup"><span data-stu-id="2a75f-158">None</span></span>
<span data-ttu-id="2a75f-159">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2a75f-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2a75f-160">輸出</span><span class="sxs-lookup"><span data-stu-id="2a75f-160">OUTPUTS</span></span>

### <span data-ttu-id="2a75f-161">[Azure. 管理]。工作流程</span><span class="sxs-lookup"><span data-stu-id="2a75f-161">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="2a75f-162">筆記</span><span class="sxs-lookup"><span data-stu-id="2a75f-162">NOTES</span></span>

## <span data-ttu-id="2a75f-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a75f-163">RELATED LINKS</span></span>

[<span data-ttu-id="2a75f-164">AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2a75f-164">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="2a75f-165">新-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2a75f-165">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="2a75f-166">移除-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2a75f-166">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="2a75f-167">開始-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2a75f-167">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)

