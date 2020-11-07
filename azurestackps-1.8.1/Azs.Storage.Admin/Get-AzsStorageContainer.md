---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34d5c967154f08526a0002f187b8cb869d933d39
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93794040"
---
# <span data-ttu-id="1d83c-101">Get-AzsStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1d83c-101">Get-AzsStorageContainer</span></span>

## <span data-ttu-id="1d83c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d83c-102">SYNOPSIS</span></span>
<span data-ttu-id="1d83c-103">傳回可在指定的共用中遷移的容器清單。</span><span class="sxs-lookup"><span data-stu-id="1d83c-103">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="1d83c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d83c-104">SYNTAX</span></span>

```
Get-AzsStorageContainer [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-MaxCount] <Int32>] [[-StartIndex] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="1d83c-105">說明</span><span class="sxs-lookup"><span data-stu-id="1d83c-105">DESCRIPTION</span></span>
<span data-ttu-id="1d83c-106">傳回可在指定的共用中遷移的容器清單。</span><span class="sxs-lookup"><span data-stu-id="1d83c-106">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="1d83c-107">示例</span><span class="sxs-lookup"><span data-stu-id="1d83c-107">EXAMPLES</span></span>

### <span data-ttu-id="1d83c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1d83c-108">EXAMPLE 1</span></span>
```
Get-AzsStorageContainer -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="1d83c-109">取得可在指定的共用中遷移的容器清單。</span><span class="sxs-lookup"><span data-stu-id="1d83c-109">Get a list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="1d83c-110">參數</span><span class="sxs-lookup"><span data-stu-id="1d83c-110">PARAMETERS</span></span>

### <span data-ttu-id="1d83c-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="1d83c-111">-FarmName</span></span>
<span data-ttu-id="1d83c-112">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="1d83c-112">Farm Id.</span></span>

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

### <span data-ttu-id="1d83c-113">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="1d83c-113">-ShareName</span></span>
<span data-ttu-id="1d83c-114">存放儲存容器的共用名稱稱。</span><span class="sxs-lookup"><span data-stu-id="1d83c-114">Share name which holds the storage containers.</span></span>

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

### <span data-ttu-id="1d83c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d83c-115">-ResourceGroupName</span></span>
<span data-ttu-id="1d83c-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1d83c-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d83c-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1d83c-117">-MaxCount</span></span>
<span data-ttu-id="1d83c-118">容器的最大數目。</span><span class="sxs-lookup"><span data-stu-id="1d83c-118">The max count of containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 100000000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d83c-119">-StartIndex</span><span class="sxs-lookup"><span data-stu-id="1d83c-119">-StartIndex</span></span>
<span data-ttu-id="1d83c-120">[取得容器] 的起始索引。</span><span class="sxs-lookup"><span data-stu-id="1d83c-120">The start index of get containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d83c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d83c-121">CommonParameters</span></span>
<span data-ttu-id="1d83c-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d83c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d83c-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1d83c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d83c-124">輸入</span><span class="sxs-lookup"><span data-stu-id="1d83c-124">INPUTS</span></span>

## <span data-ttu-id="1d83c-125">輸出</span><span class="sxs-lookup"><span data-stu-id="1d83c-125">OUTPUTS</span></span>

## <span data-ttu-id="1d83c-126">筆記</span><span class="sxs-lookup"><span data-stu-id="1d83c-126">NOTES</span></span>

## <span data-ttu-id="1d83c-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d83c-127">RELATED LINKS</span></span>