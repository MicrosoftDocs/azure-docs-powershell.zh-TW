---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: cf2d0140933523c9bb9963ca04f17262117c8c44
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957539"
---
# <span data-ttu-id="4c6f2-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="4c6f2-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="4c6f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c6f2-102">SYNOPSIS</span></span>
<span data-ttu-id="4c6f2-103">取得 Azure 安全中心將針對特定訂閱自動儲存資料的位置</span><span class="sxs-lookup"><span data-stu-id="4c6f2-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="4c6f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c6f2-104">SYNTAX</span></span>

### <span data-ttu-id="4c6f2-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="4c6f2-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c6f2-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="4c6f2-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c6f2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c6f2-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c6f2-108">說明</span><span class="sxs-lookup"><span data-stu-id="4c6f2-108">DESCRIPTION</span></span>
<span data-ttu-id="4c6f2-109">Azure 安全中心會自動決定要儲存部分資料的位置。</span><span class="sxs-lookup"><span data-stu-id="4c6f2-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="4c6f2-110">使用此 Cmdlet 來探索該位置。</span><span class="sxs-lookup"><span data-stu-id="4c6f2-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="4c6f2-111">示例</span><span class="sxs-lookup"><span data-stu-id="4c6f2-111">EXAMPLES</span></span>

### <span data-ttu-id="4c6f2-112">範例1</span><span class="sxs-lookup"><span data-stu-id="4c6f2-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="4c6f2-113">取得 Azure 安全中心儲存計算安全性資料的位置。</span><span class="sxs-lookup"><span data-stu-id="4c6f2-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="4c6f2-114">參數</span><span class="sxs-lookup"><span data-stu-id="4c6f2-114">PARAMETERS</span></span>

### <span data-ttu-id="4c6f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c6f2-115">-DefaultProfile</span></span>
<span data-ttu-id="4c6f2-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c6f2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c6f2-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4c6f2-117">-Name</span></span>
<span data-ttu-id="4c6f2-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4c6f2-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6f2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c6f2-119">-ResourceId</span></span>
<span data-ttu-id="4c6f2-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="4c6f2-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6f2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c6f2-121">CommonParameters</span></span>
<span data-ttu-id="4c6f2-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c6f2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c6f2-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4c6f2-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c6f2-124">輸入</span><span class="sxs-lookup"><span data-stu-id="4c6f2-124">INPUTS</span></span>

### <span data-ttu-id="4c6f2-125">System.object</span><span class="sxs-lookup"><span data-stu-id="4c6f2-125">System.String</span></span>

## <span data-ttu-id="4c6f2-126">輸出</span><span class="sxs-lookup"><span data-stu-id="4c6f2-126">OUTPUTS</span></span>

### <span data-ttu-id="4c6f2-127">PSSecurityLocation （Security..。</span><span class="sxs-lookup"><span data-stu-id="4c6f2-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="4c6f2-128">筆記</span><span class="sxs-lookup"><span data-stu-id="4c6f2-128">NOTES</span></span>

## <span data-ttu-id="4c6f2-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c6f2-129">RELATED LINKS</span></span>