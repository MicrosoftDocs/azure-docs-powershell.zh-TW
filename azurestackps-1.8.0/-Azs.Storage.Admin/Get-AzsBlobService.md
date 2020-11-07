---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d9ff0746de44d2e5c3c67ea95b66dd3bd3902ca
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793736"
---
# <span data-ttu-id="9ee2a-101">Get-AzsBlobService</span><span class="sxs-lookup"><span data-stu-id="9ee2a-101">Get-AzsBlobService</span></span>

## <span data-ttu-id="9ee2a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ee2a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee2a-103">傳回 blob 服務。</span><span class="sxs-lookup"><span data-stu-id="9ee2a-103">Returns the blob service.</span></span>

## <span data-ttu-id="9ee2a-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ee2a-104">SYNTAX</span></span>

```
Get-AzsBlobService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="9ee2a-105">說明</span><span class="sxs-lookup"><span data-stu-id="9ee2a-105">DESCRIPTION</span></span>
<span data-ttu-id="9ee2a-106">傳回 blob 服務。</span><span class="sxs-lookup"><span data-stu-id="9ee2a-106">Returns the blob service.</span></span>

## <span data-ttu-id="9ee2a-107">示例</span><span class="sxs-lookup"><span data-stu-id="9ee2a-107">EXAMPLES</span></span>

### <span data-ttu-id="9ee2a-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9ee2a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBlobService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="9ee2a-109">取得 blob 服務。</span><span class="sxs-lookup"><span data-stu-id="9ee2a-109">Get the blob service.</span></span>

## <span data-ttu-id="9ee2a-110">參數</span><span class="sxs-lookup"><span data-stu-id="9ee2a-110">PARAMETERS</span></span>

### <span data-ttu-id="9ee2a-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="9ee2a-111">-FarmName</span></span>
<span data-ttu-id="9ee2a-112">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="9ee2a-112">Farm Id.</span></span>

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

### <span data-ttu-id="9ee2a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ee2a-113">-ResourceGroupName</span></span>
<span data-ttu-id="9ee2a-114">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9ee2a-114">Resource group name.</span></span>

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

### <span data-ttu-id="9ee2a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee2a-115">CommonParameters</span></span>
<span data-ttu-id="9ee2a-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ee2a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee2a-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9ee2a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee2a-118">輸入</span><span class="sxs-lookup"><span data-stu-id="9ee2a-118">INPUTS</span></span>

## <span data-ttu-id="9ee2a-119">輸出</span><span class="sxs-lookup"><span data-stu-id="9ee2a-119">OUTPUTS</span></span>

### <span data-ttu-id="9ee2a-120">AzureStack （BlobService）的</span><span class="sxs-lookup"><span data-stu-id="9ee2a-120">Microsoft.AzureStack.Management.Storage.Admin.Models.BlobService</span></span>

## <span data-ttu-id="9ee2a-121">筆記</span><span class="sxs-lookup"><span data-stu-id="9ee2a-121">NOTES</span></span>

## <span data-ttu-id="9ee2a-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ee2a-122">RELATED LINKS</span></span>
