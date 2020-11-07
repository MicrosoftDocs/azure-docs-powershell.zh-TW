---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: c80278e460368ca6ec78efb4f5e74e456816df47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626271"
---
# <span data-ttu-id="7cbea-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="7cbea-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="7cbea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7cbea-102">SYNOPSIS</span></span>
<span data-ttu-id="7cbea-103">檢索指定承諾方案的使用狀況歷程記錄資訊。</span><span class="sxs-lookup"><span data-stu-id="7cbea-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cbea-104">句法</span><span class="sxs-lookup"><span data-stu-id="7cbea-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cbea-105">說明</span><span class="sxs-lookup"><span data-stu-id="7cbea-105">DESCRIPTION</span></span>
<span data-ttu-id="7cbea-106">檢索指定承諾方案的使用方式歷程記錄資訊，包括所使用的資源，以及方案中剩餘的資源。</span><span class="sxs-lookup"><span data-stu-id="7cbea-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="7cbea-107">示例</span><span class="sxs-lookup"><span data-stu-id="7cbea-107">EXAMPLES</span></span>

### <span data-ttu-id="7cbea-108">--------------------------範例1：取得特定承諾方案的使用狀況歷程記錄--------------------------</span><span class="sxs-lookup"><span data-stu-id="7cbea-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
<span data-ttu-id="7cbea-109">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7cbea-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="7cbea-110">參數</span><span class="sxs-lookup"><span data-stu-id="7cbea-110">PARAMETERS</span></span>

### <span data-ttu-id="7cbea-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="7cbea-111">-Name</span></span>
<span data-ttu-id="7cbea-112">Azure ML 提交方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cbea-112">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="7cbea-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cbea-113">-ResourceGroupName</span></span>
<span data-ttu-id="7cbea-114">Azure ML 承諾方案之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cbea-114">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="7cbea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cbea-115">-DefaultProfile</span></span>
<span data-ttu-id="7cbea-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7cbea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cbea-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cbea-117">CommonParameters</span></span>
<span data-ttu-id="7cbea-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7cbea-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cbea-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7cbea-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cbea-120">輸入</span><span class="sxs-lookup"><span data-stu-id="7cbea-120">INPUTS</span></span>

## <span data-ttu-id="7cbea-121">輸出</span><span class="sxs-lookup"><span data-stu-id="7cbea-121">OUTPUTS</span></span>

### <span data-ttu-id="7cbea-122">PlanUsageHistory []. MachineLearning [CommitmentPlans]</span><span class="sxs-lookup"><span data-stu-id="7cbea-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="7cbea-123">筆記</span><span class="sxs-lookup"><span data-stu-id="7cbea-123">NOTES</span></span>
<span data-ttu-id="7cbea-124">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="7cbea-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7cbea-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="7cbea-125">RELATED LINKS</span></span>
