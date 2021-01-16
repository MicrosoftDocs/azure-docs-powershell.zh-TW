---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
ms.openlocfilehash: 7061d70ca1f4bc38c9ac8cc12ad75f01a3fed8b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288928"
---
# <span data-ttu-id="af239-101">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="af239-101">Get-AzLogicAppTrigger</span></span>

## <span data-ttu-id="af239-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af239-102">SYNOPSIS</span></span>
<span data-ttu-id="af239-103">取得邏輯 app 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="af239-103">Gets the triggers of a logic app.</span></span>

## <span data-ttu-id="af239-104">句法</span><span class="sxs-lookup"><span data-stu-id="af239-104">SYNTAX</span></span>

```
Get-AzLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af239-105">說明</span><span class="sxs-lookup"><span data-stu-id="af239-105">DESCRIPTION</span></span>
<span data-ttu-id="af239-106">**AzLogicAppTrigger** Cmdlet 會從邏輯 app 取得觸發程式。</span><span class="sxs-lookup"><span data-stu-id="af239-106">The **Get-AzLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="af239-107">這個 Cmdlet 會傳回 **WorkflowTrigger** 物件。</span><span class="sxs-lookup"><span data-stu-id="af239-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="af239-108">指定工作流程、資源群組及觸發程式。</span><span class="sxs-lookup"><span data-stu-id="af239-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="af239-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="af239-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="af239-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="af239-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="af239-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="af239-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="af239-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="af239-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="af239-113">示例</span><span class="sxs-lookup"><span data-stu-id="af239-113">EXAMPLES</span></span>

### <span data-ttu-id="af239-114">範例1：取得邏輯 app 的觸發程式</span><span class="sxs-lookup"><span data-stu-id="af239-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger01
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp05
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="af239-115">這個命令會從名為 LogicApp05 的邏輯 app 取得名為 Trigger01 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="af239-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="af239-116">範例2：取得邏輯 app 的所有觸發程式</span><span class="sxs-lookup"><span data-stu-id="af239-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger02
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp07
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="af239-117">這個命令會取得名為 LogicApp07 的邏輯 app 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="af239-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="af239-118">參數</span><span class="sxs-lookup"><span data-stu-id="af239-118">PARAMETERS</span></span>

### <span data-ttu-id="af239-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af239-119">-DefaultProfile</span></span>
<span data-ttu-id="af239-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="af239-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af239-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="af239-121">-Name</span></span>
<span data-ttu-id="af239-122">指定這個 Cmdlet 取得觸發程式的邏輯 app 名稱。</span><span class="sxs-lookup"><span data-stu-id="af239-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af239-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af239-123">-ResourceGroupName</span></span>
<span data-ttu-id="af239-124">指定此 Cmdlet 取得觸發程式之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="af239-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="af239-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="af239-125">-TriggerName</span></span>
<span data-ttu-id="af239-126">指定此 Cmdlet 所取得之觸發程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="af239-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

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

### <span data-ttu-id="af239-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af239-127">CommonParameters</span></span>
<span data-ttu-id="af239-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af239-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af239-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="af239-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af239-130">輸入</span><span class="sxs-lookup"><span data-stu-id="af239-130">INPUTS</span></span>

### <span data-ttu-id="af239-131">System.object</span><span class="sxs-lookup"><span data-stu-id="af239-131">System.String</span></span>

## <span data-ttu-id="af239-132">輸出</span><span class="sxs-lookup"><span data-stu-id="af239-132">OUTPUTS</span></span>

### <span data-ttu-id="af239-133">WorkflowTrigger 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="af239-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="af239-134">筆記</span><span class="sxs-lookup"><span data-stu-id="af239-134">NOTES</span></span>

## <span data-ttu-id="af239-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="af239-135">RELATED LINKS</span></span>

[<span data-ttu-id="af239-136">AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="af239-136">Get-AzLogicAppTriggerHistory</span></span>](./Get-AzLogicAppTriggerHistory.md)

[<span data-ttu-id="af239-137">開始-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="af239-137">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

