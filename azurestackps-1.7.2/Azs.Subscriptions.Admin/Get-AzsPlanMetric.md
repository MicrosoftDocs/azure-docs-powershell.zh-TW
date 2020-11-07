---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cadf5ad37119ab6b50191e50e8ec281fe4bce2d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793181"
---
# <span data-ttu-id="1e3a8-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="1e3a8-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="1e3a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e3a8-102">SYNOPSIS</span></span>
<span data-ttu-id="1e3a8-103">取得計畫度量單位。</span><span class="sxs-lookup"><span data-stu-id="1e3a8-103">Get the plan metrics.</span></span>

## <span data-ttu-id="1e3a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e3a8-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="1e3a8-105">說明</span><span class="sxs-lookup"><span data-stu-id="1e3a8-105">DESCRIPTION</span></span>
<span data-ttu-id="1e3a8-106">取得計畫度量單位。</span><span class="sxs-lookup"><span data-stu-id="1e3a8-106">Get the plan metrics.</span></span>

## <span data-ttu-id="1e3a8-107">示例</span><span class="sxs-lookup"><span data-stu-id="1e3a8-107">EXAMPLES</span></span>

### <span data-ttu-id="1e3a8-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1e3a8-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="1e3a8-109">取得計畫的度量單位。</span><span class="sxs-lookup"><span data-stu-id="1e3a8-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="1e3a8-110">參數</span><span class="sxs-lookup"><span data-stu-id="1e3a8-110">PARAMETERS</span></span>

### <span data-ttu-id="1e3a8-111">-PlanName</span><span class="sxs-lookup"><span data-stu-id="1e3a8-111">-PlanName</span></span>
<span data-ttu-id="1e3a8-112">方案名稱。</span><span class="sxs-lookup"><span data-stu-id="1e3a8-112">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3a8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e3a8-113">-ResourceGroupName</span></span>
<span data-ttu-id="1e3a8-114">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1e3a8-114">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3a8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e3a8-115">CommonParameters</span></span>
<span data-ttu-id="1e3a8-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e3a8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e3a8-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e3a8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e3a8-118">輸入</span><span class="sxs-lookup"><span data-stu-id="1e3a8-118">INPUTS</span></span>

## <span data-ttu-id="1e3a8-119">輸出</span><span class="sxs-lookup"><span data-stu-id="1e3a8-119">OUTPUTS</span></span>

### <span data-ttu-id="1e3a8-120">AzureStack 的訂閱. 系統管理。</span><span class="sxs-lookup"><span data-stu-id="1e3a8-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="1e3a8-121">筆記</span><span class="sxs-lookup"><span data-stu-id="1e3a8-121">NOTES</span></span>

## <span data-ttu-id="1e3a8-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e3a8-122">RELATED LINKS</span></span>
