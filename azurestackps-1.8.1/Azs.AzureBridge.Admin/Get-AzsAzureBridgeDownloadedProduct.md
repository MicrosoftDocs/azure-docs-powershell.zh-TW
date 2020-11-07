---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1780eeb2f5d03fafd056c7987f648eae989b3dd
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/22/2020
ms.locfileid: "93802717"
---
# <span data-ttu-id="e5855-101">Get-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="e5855-101">Get-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="e5855-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5855-102">SYNOPSIS</span></span>
<span data-ttu-id="e5855-103">傳回從 Azure MarketPlace 下載的產品清單。</span><span class="sxs-lookup"><span data-stu-id="e5855-103">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="e5855-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5855-104">SYNTAX</span></span>

### <span data-ttu-id="e5855-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="e5855-105">List (Default)</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e5855-106">獲取</span><span class="sxs-lookup"><span data-stu-id="e5855-106">Get</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="e5855-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5855-107">ResourceId</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e5855-108">說明</span><span class="sxs-lookup"><span data-stu-id="e5855-108">DESCRIPTION</span></span>
<span data-ttu-id="e5855-109">傳回從 Azure MarketPlace 下載的產品清單。</span><span class="sxs-lookup"><span data-stu-id="e5855-109">Returns a list of products downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="e5855-110">示例</span><span class="sxs-lookup"><span data-stu-id="e5855-110">EXAMPLES</span></span>

### <span data-ttu-id="e5855-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e5855-111">EXAMPLE 1</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="e5855-112">取得 Azure Bridge 已下載產品的清單</span><span class="sxs-lookup"><span data-stu-id="e5855-112">Get a list of Azure Bridge Downloaded products</span></span>

### <span data-ttu-id="e5855-113">範例2</span><span class="sxs-lookup"><span data-stu-id="e5855-113">EXAMPLE 2</span></span>
```
Get-AzsAzureBridgeDownloadedProduct -Name 'microsoft.docker-arm.1.1.0' -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="e5855-114">透過名稱取得 Azure Bridge 已下載產品</span><span class="sxs-lookup"><span data-stu-id="e5855-114">Get an Azure Bridge Downloaded Product by Name</span></span>

## <span data-ttu-id="e5855-115">參數</span><span class="sxs-lookup"><span data-stu-id="e5855-115">PARAMETERS</span></span>

### <span data-ttu-id="e5855-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5855-116">-Name</span></span>
<span data-ttu-id="e5855-117">產品名稱。</span><span class="sxs-lookup"><span data-stu-id="e5855-117">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5855-118">-ActivationName</span><span class="sxs-lookup"><span data-stu-id="e5855-118">-ActivationName</span></span>
<span data-ttu-id="e5855-119">啟用的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5855-119">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5855-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5855-120">-ResourceGroupName</span></span>
<span data-ttu-id="e5855-121">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e5855-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5855-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5855-122">-ResourceId</span></span>
<span data-ttu-id="e5855-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e5855-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5855-124">-略過</span><span class="sxs-lookup"><span data-stu-id="e5855-124">-Skip</span></span>
<span data-ttu-id="e5855-125">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="e5855-125">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5855-126">-上方</span><span class="sxs-lookup"><span data-stu-id="e5855-126">-Top</span></span>
<span data-ttu-id="e5855-127">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="e5855-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e5855-128">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="e5855-128">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5855-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5855-129">CommonParameters</span></span>
<span data-ttu-id="e5855-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5855-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5855-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5855-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5855-132">輸入</span><span class="sxs-lookup"><span data-stu-id="e5855-132">INPUTS</span></span>

## <span data-ttu-id="e5855-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e5855-133">OUTPUTS</span></span>

### <span data-ttu-id="e5855-134">AzureStack AzureBridge. DownloadedProductResource （）</span><span class="sxs-lookup"><span data-stu-id="e5855-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="e5855-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e5855-135">NOTES</span></span>

## <span data-ttu-id="e5855-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5855-136">RELATED LINKS</span></span>