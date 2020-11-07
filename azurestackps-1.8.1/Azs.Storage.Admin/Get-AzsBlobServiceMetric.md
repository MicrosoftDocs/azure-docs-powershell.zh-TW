---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 822452c1c6b83669759bae2c861ee3456a13a0dc
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793950"
---
# <span data-ttu-id="38edc-101">Get-AzsBlobServiceMetric</span><span class="sxs-lookup"><span data-stu-id="38edc-101">Get-AzsBlobServiceMetric</span></span>

## <span data-ttu-id="38edc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38edc-102">SYNOPSIS</span></span>
<span data-ttu-id="38edc-103">傳回 blob 服務的規格清單。</span><span class="sxs-lookup"><span data-stu-id="38edc-103">Returns a list of metrics for blob service.</span></span>

## <span data-ttu-id="38edc-104">句法</span><span class="sxs-lookup"><span data-stu-id="38edc-104">SYNTAX</span></span>

```
Get-AzsBlobServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="38edc-105">說明</span><span class="sxs-lookup"><span data-stu-id="38edc-105">DESCRIPTION</span></span>
<span data-ttu-id="38edc-106">傳回 blob 服務的規格清單。</span><span class="sxs-lookup"><span data-stu-id="38edc-106">Returns a list of metrics for blob service.</span></span>

## <span data-ttu-id="38edc-107">示例</span><span class="sxs-lookup"><span data-stu-id="38edc-107">EXAMPLES</span></span>

### <span data-ttu-id="38edc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="38edc-108">EXAMPLE 1</span></span>
```
Get-AzsBlobServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="38edc-109">取得 blob 服務的規格清單。</span><span class="sxs-lookup"><span data-stu-id="38edc-109">Get a list of metrics for blob service.</span></span>

## <span data-ttu-id="38edc-110">參數</span><span class="sxs-lookup"><span data-stu-id="38edc-110">PARAMETERS</span></span>

### <span data-ttu-id="38edc-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="38edc-111">-FarmName</span></span>
<span data-ttu-id="38edc-112">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="38edc-112">Farm Id.</span></span>

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

### <span data-ttu-id="38edc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38edc-113">-ResourceGroupName</span></span>
<span data-ttu-id="38edc-114">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="38edc-114">Resource group name.</span></span>

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

### <span data-ttu-id="38edc-115">-略過</span><span class="sxs-lookup"><span data-stu-id="38edc-115">-Skip</span></span>
<span data-ttu-id="38edc-116">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="38edc-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38edc-117">-上方</span><span class="sxs-lookup"><span data-stu-id="38edc-117">-Top</span></span>
<span data-ttu-id="38edc-118">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="38edc-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="38edc-119">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="38edc-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38edc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38edc-120">CommonParameters</span></span>
<span data-ttu-id="38edc-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38edc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38edc-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38edc-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38edc-123">輸入</span><span class="sxs-lookup"><span data-stu-id="38edc-123">INPUTS</span></span>

## <span data-ttu-id="38edc-124">輸出</span><span class="sxs-lookup"><span data-stu-id="38edc-124">OUTPUTS</span></span>

### <span data-ttu-id="38edc-125">AzureStack （系統管理）。</span><span class="sxs-lookup"><span data-stu-id="38edc-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="38edc-126">筆記</span><span class="sxs-lookup"><span data-stu-id="38edc-126">NOTES</span></span>

## <span data-ttu-id="38edc-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="38edc-127">RELATED LINKS</span></span>