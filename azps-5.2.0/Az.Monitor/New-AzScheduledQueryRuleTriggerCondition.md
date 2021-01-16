---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 0fffbc11291fcf3cd7d3989e211bcbb0d202ea9b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273439"
---
# <span data-ttu-id="11690-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="11690-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="11690-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11690-102">SYNOPSIS</span></span>
<span data-ttu-id="11690-103">建立觸發條件類型的物件</span><span class="sxs-lookup"><span data-stu-id="11690-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="11690-104">句法</span><span class="sxs-lookup"><span data-stu-id="11690-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11690-105">說明</span><span class="sxs-lookup"><span data-stu-id="11690-105">DESCRIPTION</span></span>
<span data-ttu-id="11690-106">建立觸發條件類型的物件。</span><span class="sxs-lookup"><span data-stu-id="11690-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="11690-107">這個物件會傳遞到建立警示動作物件的命令</span><span class="sxs-lookup"><span data-stu-id="11690-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="11690-108">示例</span><span class="sxs-lookup"><span data-stu-id="11690-108">EXAMPLES</span></span>

### <span data-ttu-id="11690-109">範例1</span><span class="sxs-lookup"><span data-stu-id="11690-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="11690-110">參數</span><span class="sxs-lookup"><span data-stu-id="11690-110">PARAMETERS</span></span>

### <span data-ttu-id="11690-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11690-111">-DefaultProfile</span></span>
<span data-ttu-id="11690-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11690-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11690-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="11690-113">-MetricTrigger</span></span>
<span data-ttu-id="11690-114">公制查詢規則的觸發條件</span><span class="sxs-lookup"><span data-stu-id="11690-114">Trigger condition for metric query rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11690-115">-閾值</span><span class="sxs-lookup"><span data-stu-id="11690-115">-Threshold</span></span>
<span data-ttu-id="11690-116">觸發警報的閾值</span><span class="sxs-lookup"><span data-stu-id="11690-116">The threshold above which alert gets fired</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11690-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="11690-117">-ThresholdOperator</span></span>
<span data-ttu-id="11690-118">閾值運算子： GreaterThan、小於或等於</span><span class="sxs-lookup"><span data-stu-id="11690-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11690-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11690-119">CommonParameters</span></span>
<span data-ttu-id="11690-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11690-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11690-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="11690-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11690-122">輸入</span><span class="sxs-lookup"><span data-stu-id="11690-122">INPUTS</span></span>

### <span data-ttu-id="11690-123">所有</span><span class="sxs-lookup"><span data-stu-id="11690-123">None</span></span>

## <span data-ttu-id="11690-124">輸出</span><span class="sxs-lookup"><span data-stu-id="11690-124">OUTPUTS</span></span>

### <span data-ttu-id="11690-125">PSScheduledQueryRuleTriggerCondition 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="11690-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="11690-126">筆記</span><span class="sxs-lookup"><span data-stu-id="11690-126">NOTES</span></span>

## <span data-ttu-id="11690-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="11690-127">RELATED LINKS</span></span>