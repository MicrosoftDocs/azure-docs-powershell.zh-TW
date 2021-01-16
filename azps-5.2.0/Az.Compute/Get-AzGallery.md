---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: baa3730ee03dd8f871e64e7964659c62f60e8032
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276159"
---
# <span data-ttu-id="53975-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="53975-101">Get-AzGallery</span></span>

## <span data-ttu-id="53975-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53975-102">SYNOPSIS</span></span>
<span data-ttu-id="53975-103">[取得] 或 [清單] 樣式庫。</span><span class="sxs-lookup"><span data-stu-id="53975-103">Get or list galleries.</span></span>

## <span data-ttu-id="53975-104">句法</span><span class="sxs-lookup"><span data-stu-id="53975-104">SYNTAX</span></span>

### <span data-ttu-id="53975-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="53975-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53975-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="53975-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53975-107">說明</span><span class="sxs-lookup"><span data-stu-id="53975-107">DESCRIPTION</span></span>
<span data-ttu-id="53975-108">[取得] 或 [清單] 樣式庫。</span><span class="sxs-lookup"><span data-stu-id="53975-108">Get or list galleries.</span></span>

## <span data-ttu-id="53975-109">示例</span><span class="sxs-lookup"><span data-stu-id="53975-109">EXAMPLES</span></span>

### <span data-ttu-id="53975-110">範例1</span><span class="sxs-lookup"><span data-stu-id="53975-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="53975-111">取得圖庫 "gallery1"</span><span class="sxs-lookup"><span data-stu-id="53975-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="53975-112">範例2</span><span class="sxs-lookup"><span data-stu-id="53975-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="53975-113">在 rg1 中取得所有圖庫。</span><span class="sxs-lookup"><span data-stu-id="53975-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="53975-114">範例3</span><span class="sxs-lookup"><span data-stu-id="53975-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGallery

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="53975-115">取得訂閱中的所有圖庫。</span><span class="sxs-lookup"><span data-stu-id="53975-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="53975-116">範例4</span><span class="sxs-lookup"><span data-stu-id="53975-116">Example 4</span></span>
```powershell
PS C:\> Get-AzGallery -Name gallery*

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="53975-117">取得所有以 "圖庫" 開頭的訂閱中的所有圖庫。</span><span class="sxs-lookup"><span data-stu-id="53975-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="53975-118">參數</span><span class="sxs-lookup"><span data-stu-id="53975-118">PARAMETERS</span></span>

### <span data-ttu-id="53975-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53975-119">-DefaultProfile</span></span>
<span data-ttu-id="53975-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53975-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53975-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="53975-121">-Name</span></span>
<span data-ttu-id="53975-122">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="53975-122">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="53975-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53975-123">-ResourceGroupName</span></span>
<span data-ttu-id="53975-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="53975-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="53975-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53975-125">-ResourceId</span></span>
<span data-ttu-id="53975-126">圖庫的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="53975-126">The resource id for Gallery</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53975-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53975-127">CommonParameters</span></span>
<span data-ttu-id="53975-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53975-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53975-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="53975-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53975-130">輸入</span><span class="sxs-lookup"><span data-stu-id="53975-130">INPUTS</span></span>

### <span data-ttu-id="53975-131">System.object</span><span class="sxs-lookup"><span data-stu-id="53975-131">System.String</span></span>

## <span data-ttu-id="53975-132">輸出</span><span class="sxs-lookup"><span data-stu-id="53975-132">OUTPUTS</span></span>

### <span data-ttu-id="53975-133">PSGallery 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="53975-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="53975-134">筆記</span><span class="sxs-lookup"><span data-stu-id="53975-134">NOTES</span></span>

## <span data-ttu-id="53975-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="53975-135">RELATED LINKS</span></span>