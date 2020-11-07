---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86b9e7574344e1b4724648ce55fa2e36aed6591b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793359"
---
# <span data-ttu-id="cfd66-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="cfd66-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="cfd66-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cfd66-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd66-103">傳回特定位置上所有結構檔案共用的清單。</span><span class="sxs-lookup"><span data-stu-id="cfd66-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="cfd66-104">句法</span><span class="sxs-lookup"><span data-stu-id="cfd66-104">SYNTAX</span></span>

### <span data-ttu-id="cfd66-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="cfd66-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="cfd66-106">獲取</span><span class="sxs-lookup"><span data-stu-id="cfd66-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="cfd66-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfd66-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="cfd66-108">說明</span><span class="sxs-lookup"><span data-stu-id="cfd66-108">DESCRIPTION</span></span>
<span data-ttu-id="cfd66-109">傳回特定位置上所有結構檔案共用的清單。</span><span class="sxs-lookup"><span data-stu-id="cfd66-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="cfd66-110">示例</span><span class="sxs-lookup"><span data-stu-id="cfd66-110">EXAMPLES</span></span>

### <span data-ttu-id="cfd66-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cfd66-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="cfd66-112">傳回所有檔案共用的清單。</span><span class="sxs-lookup"><span data-stu-id="cfd66-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="cfd66-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="cfd66-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="cfd66-114">根據名稱返回檔案共用。</span><span class="sxs-lookup"><span data-stu-id="cfd66-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="cfd66-115">參數</span><span class="sxs-lookup"><span data-stu-id="cfd66-115">PARAMETERS</span></span>

### <span data-ttu-id="cfd66-116">-篩選</span><span class="sxs-lookup"><span data-stu-id="cfd66-116">-Filter</span></span>
<span data-ttu-id="cfd66-117">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="cfd66-117">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd66-118">-位置</span><span class="sxs-lookup"><span data-stu-id="cfd66-118">-Location</span></span>
<span data-ttu-id="cfd66-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="cfd66-119">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd66-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="cfd66-120">-Name</span></span>
<span data-ttu-id="cfd66-121">Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="cfd66-121">Fabric file share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd66-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfd66-122">-ResourceGroupName</span></span>
<span data-ttu-id="cfd66-123">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="cfd66-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd66-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfd66-124">-ResourceId</span></span>
<span data-ttu-id="cfd66-125">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="cfd66-125">The resource id.</span></span>

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

### <span data-ttu-id="cfd66-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfd66-126">CommonParameters</span></span>
<span data-ttu-id="cfd66-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cfd66-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfd66-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cfd66-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfd66-129">輸入</span><span class="sxs-lookup"><span data-stu-id="cfd66-129">INPUTS</span></span>

## <span data-ttu-id="cfd66-130">輸出</span><span class="sxs-lookup"><span data-stu-id="cfd66-130">OUTPUTS</span></span>

### <span data-ttu-id="cfd66-131">AzureStack. 系統管理.............。</span><span class="sxs-lookup"><span data-stu-id="cfd66-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="cfd66-132">筆記</span><span class="sxs-lookup"><span data-stu-id="cfd66-132">NOTES</span></span>

## <span data-ttu-id="cfd66-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="cfd66-133">RELATED LINKS</span></span>
