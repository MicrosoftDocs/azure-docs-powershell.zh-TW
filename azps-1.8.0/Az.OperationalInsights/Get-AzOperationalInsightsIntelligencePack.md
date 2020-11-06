---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: fa4df1d2b2149a0bc9c637ffefd5c60e52fa0059
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93623394"
---
# <span data-ttu-id="fb77f-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="fb77f-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="fb77f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb77f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb77f-103">取得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="fb77f-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="fb77f-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb77f-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb77f-105">說明</span><span class="sxs-lookup"><span data-stu-id="fb77f-105">DESCRIPTION</span></span>
<span data-ttu-id="fb77f-106">**AzOperationalInsightsIntelligencePack** Cmdlet 會取得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="fb77f-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="fb77f-107">示例</span><span class="sxs-lookup"><span data-stu-id="fb77f-107">EXAMPLES</span></span>

### <span data-ttu-id="fb77f-108">範例1：取得智慧套件</span><span class="sxs-lookup"><span data-stu-id="fb77f-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="fb77f-109">這個命令會取得可用的智慧套件。</span><span class="sxs-lookup"><span data-stu-id="fb77f-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="fb77f-110">參數</span><span class="sxs-lookup"><span data-stu-id="fb77f-110">PARAMETERS</span></span>

### <span data-ttu-id="fb77f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb77f-111">-DefaultProfile</span></span>
<span data-ttu-id="fb77f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fb77f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb77f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb77f-113">-ResourceGroupName</span></span>
<span data-ttu-id="fb77f-114">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb77f-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb77f-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fb77f-115">-WorkspaceName</span></span>
<span data-ttu-id="fb77f-116">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="fb77f-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb77f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb77f-117">CommonParameters</span></span>
<span data-ttu-id="fb77f-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb77f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb77f-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fb77f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb77f-120">輸入</span><span class="sxs-lookup"><span data-stu-id="fb77f-120">INPUTS</span></span>

### <span data-ttu-id="fb77f-121">System.object</span><span class="sxs-lookup"><span data-stu-id="fb77f-121">System.String</span></span>

## <span data-ttu-id="fb77f-122">輸出</span><span class="sxs-lookup"><span data-stu-id="fb77f-122">OUTPUTS</span></span>

### <span data-ttu-id="fb77f-123">PSIntelligencePack 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="fb77f-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="fb77f-124">筆記</span><span class="sxs-lookup"><span data-stu-id="fb77f-124">NOTES</span></span>

## <span data-ttu-id="fb77f-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb77f-125">RELATED LINKS</span></span>

[<span data-ttu-id="fb77f-126">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fb77f-126">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

