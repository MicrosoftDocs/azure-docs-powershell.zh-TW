---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: 9c92156f3fe739cd4f4285d536bd8a4c79cd3ec2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624272"
---
# <span data-ttu-id="bda4f-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="bda4f-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="bda4f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bda4f-102">SYNOPSIS</span></span>
<span data-ttu-id="bda4f-103">取得有關資料流程分析作業轉換的資訊。</span><span class="sxs-lookup"><span data-stu-id="bda4f-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bda4f-104">句法</span><span class="sxs-lookup"><span data-stu-id="bda4f-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bda4f-105">說明</span><span class="sxs-lookup"><span data-stu-id="bda4f-105">DESCRIPTION</span></span>
<span data-ttu-id="bda4f-106">**AzureRmStreamAnalyticsTransformation** Cmdlet 會取得對流分析作業上所定義轉換的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bda4f-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="bda4f-107">示例</span><span class="sxs-lookup"><span data-stu-id="bda4f-107">EXAMPLES</span></span>

### <span data-ttu-id="bda4f-108">範例1：取得資料流程分析轉換的相關資訊</span><span class="sxs-lookup"><span data-stu-id="bda4f-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="bda4f-109">這個命令會傳回稱為 StreamingJob 的作業上稱為 StreamingJob 轉換的資訊。</span><span class="sxs-lookup"><span data-stu-id="bda4f-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="bda4f-110">參數</span><span class="sxs-lookup"><span data-stu-id="bda4f-110">PARAMETERS</span></span>

### <span data-ttu-id="bda4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bda4f-111">-DefaultProfile</span></span>
<span data-ttu-id="bda4f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bda4f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bda4f-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="bda4f-113">-JobName</span></span>
<span data-ttu-id="bda4f-114">指定 Azure 資料流程分析轉換所屬之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="bda4f-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda4f-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="bda4f-115">-Name</span></span>
<span data-ttu-id="bda4f-116">指定要檢索之 Azure 串流分析轉換的名稱。</span><span class="sxs-lookup"><span data-stu-id="bda4f-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda4f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bda4f-117">-ResourceGroupName</span></span>
<span data-ttu-id="bda4f-118">指定 Azure 資料流程分析轉換所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bda4f-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda4f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda4f-119">CommonParameters</span></span>
<span data-ttu-id="bda4f-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bda4f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda4f-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bda4f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda4f-122">輸入</span><span class="sxs-lookup"><span data-stu-id="bda4f-122">INPUTS</span></span>

### <span data-ttu-id="bda4f-123">所有</span><span class="sxs-lookup"><span data-stu-id="bda4f-123">None</span></span>
<span data-ttu-id="bda4f-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="bda4f-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bda4f-125">輸出</span><span class="sxs-lookup"><span data-stu-id="bda4f-125">OUTPUTS</span></span>

### <span data-ttu-id="bda4f-126">[System.object]. 清單 ' 1 [StreamAnalytics. PSTransformation，StreamAnalytics]]]]]]]]]]]]</span><span class="sxs-lookup"><span data-stu-id="bda4f-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="bda4f-127">筆記</span><span class="sxs-lookup"><span data-stu-id="bda4f-127">NOTES</span></span>

## <span data-ttu-id="bda4f-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="bda4f-128">RELATED LINKS</span></span>

[<span data-ttu-id="bda4f-129">新-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="bda4f-129">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)

