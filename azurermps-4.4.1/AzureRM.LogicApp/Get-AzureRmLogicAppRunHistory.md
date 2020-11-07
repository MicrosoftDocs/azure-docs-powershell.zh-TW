---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunHistory.md
ms.openlocfilehash: 05ccc9dc237e0058665607488a5083a5295eb2f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625499"
---
# <span data-ttu-id="c8cd1-101">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="c8cd1-101">Get-AzureRmLogicAppRunHistory</span></span>

## <span data-ttu-id="c8cd1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="c8cd1-103">取得邏輯 app 的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-103">Gets the run history of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8cd1-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8cd1-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8cd1-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8cd1-105">DESCRIPTION</span></span>
<span data-ttu-id="c8cd1-106">**AzureRmLogicAppRunHistory** Cmdlet 會取得邏輯 app 的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-106">The **Get-AzureRmLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="c8cd1-107">這個 Cmdlet 會傳回 **WorkflowRun** 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="c8cd1-108">指定邏輯 app 與資源群組。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-108">Specify the logic app and resource group.</span></span>

<span data-ttu-id="c8cd1-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c8cd1-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c8cd1-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c8cd1-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c8cd1-113">示例</span><span class="sxs-lookup"><span data-stu-id="c8cd1-113">EXAMPLES</span></span>

### <span data-ttu-id="c8cd1-114">範例1：取得邏輯 app 的執行歷程記錄</span><span class="sxs-lookup"><span data-stu-id="c8cd1-114">Example 1: Get the run history of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952540

CorrelationId    : d3ddc917-9aaa-47b3-8814-c621c2ae530b
EndTime          : 1/13/2016 2:42:56 PM
Error            : {code, message}
Name             : 08587489107100664541
Outputs          : {}
StartTime        : 1/13/2016 2:42:55 PM
Status           : Failed
TriggerName      : httpTrigger
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="c8cd1-115">這個命令會取得名為 LogicApp03 的邏輯 app 的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="c8cd1-116">範例2：取得邏輯 app 執行</span><span class="sxs-lookup"><span data-stu-id="c8cd1-116">Example 2: Get a logic app run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="c8cd1-117">這個命令會針對名為 LogicApp03 的邏輯 app 取得特定的邏輯 app 執行。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

## <span data-ttu-id="c8cd1-118">參數</span><span class="sxs-lookup"><span data-stu-id="c8cd1-118">PARAMETERS</span></span>

### <span data-ttu-id="c8cd1-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8cd1-119">-Name</span></span>
<span data-ttu-id="c8cd1-120">指定此 Cmdlet 取得其 [執行歷程記錄] 的邏輯 app 名稱。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-120">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8cd1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8cd1-121">-ResourceGroupName</span></span>
<span data-ttu-id="c8cd1-122">指定包含邏輯 app 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-122">Specifies the name of a resource group that contains the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8cd1-123">-RunName</span><span class="sxs-lookup"><span data-stu-id="c8cd1-123">-RunName</span></span>
<span data-ttu-id="c8cd1-124">指定邏輯 app 的 [執行名稱]。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-124">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="c8cd1-125">這個 Cmdlet 會取得這個 Cmdlet 所指定的工作流程執行。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-125">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="c8cd1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8cd1-126">-DefaultProfile</span></span>
<span data-ttu-id="c8cd1-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8cd1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8cd1-128">CommonParameters</span></span>
<span data-ttu-id="c8cd1-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8cd1-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8cd1-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c8cd1-131">INPUTS</span></span>

## <span data-ttu-id="c8cd1-132">輸出</span><span class="sxs-lookup"><span data-stu-id="c8cd1-132">OUTPUTS</span></span>

### <span data-ttu-id="c8cd1-133">WorkflowRun 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="c8cd1-133">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="c8cd1-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c8cd1-134">NOTES</span></span>

## <span data-ttu-id="c8cd1-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8cd1-135">RELATED LINKS</span></span>

[<span data-ttu-id="c8cd1-136">AzureRmLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="c8cd1-136">Get-AzureRmLogicAppRunAction</span></span>](./Get-AzureRmLogicAppRunAction.md)

[<span data-ttu-id="c8cd1-137">開始-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c8cd1-137">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)

[<span data-ttu-id="c8cd1-138">停止 AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="c8cd1-138">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)

