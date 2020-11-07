---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 4d78d6e6a1b0ae5ea9f8815d537bca1496e24bbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786970"
---
# <span data-ttu-id="41ffe-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="41ffe-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="41ffe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="41ffe-103">檢索指定承諾方案的使用狀況歷程記錄資訊。</span><span class="sxs-lookup"><span data-stu-id="41ffe-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="41ffe-104">句法</span><span class="sxs-lookup"><span data-stu-id="41ffe-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41ffe-105">說明</span><span class="sxs-lookup"><span data-stu-id="41ffe-105">DESCRIPTION</span></span>
<span data-ttu-id="41ffe-106">檢索指定承諾方案的使用方式歷程記錄資訊，包括所使用的資源，以及方案中剩餘的資源。</span><span class="sxs-lookup"><span data-stu-id="41ffe-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="41ffe-107">示例</span><span class="sxs-lookup"><span data-stu-id="41ffe-107">EXAMPLES</span></span>

### <span data-ttu-id="41ffe-108">範例1：取得特定承諾方案的使用狀況歷程記錄</span><span class="sxs-lookup"><span data-stu-id="41ffe-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="41ffe-109">參數</span><span class="sxs-lookup"><span data-stu-id="41ffe-109">PARAMETERS</span></span>

### <span data-ttu-id="41ffe-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41ffe-110">-DefaultProfile</span></span>
<span data-ttu-id="41ffe-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="41ffe-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41ffe-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="41ffe-112">-Name</span></span>
<span data-ttu-id="41ffe-113">Azure ML 提交方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="41ffe-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="41ffe-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41ffe-114">-ResourceGroupName</span></span>
<span data-ttu-id="41ffe-115">Azure ML 承諾方案之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="41ffe-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="41ffe-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41ffe-116">CommonParameters</span></span>
<span data-ttu-id="41ffe-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41ffe-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41ffe-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="41ffe-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41ffe-119">輸入</span><span class="sxs-lookup"><span data-stu-id="41ffe-119">INPUTS</span></span>

### <span data-ttu-id="41ffe-120">所有</span><span class="sxs-lookup"><span data-stu-id="41ffe-120">None</span></span>

## <span data-ttu-id="41ffe-121">輸出</span><span class="sxs-lookup"><span data-stu-id="41ffe-121">OUTPUTS</span></span>

### <span data-ttu-id="41ffe-122">MachineLearning CommitmentPlans. PlanUsageHistory （）</span><span class="sxs-lookup"><span data-stu-id="41ffe-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="41ffe-123">筆記</span><span class="sxs-lookup"><span data-stu-id="41ffe-123">NOTES</span></span>
<span data-ttu-id="41ffe-124">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="41ffe-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="41ffe-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="41ffe-125">RELATED LINKS</span></span>