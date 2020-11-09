---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: 9d36169439a2466ca50858f5b438822461259cf3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288047"
---
# <span data-ttu-id="c51d9-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="c51d9-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="c51d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c51d9-102">SYNOPSIS</span></span>
<span data-ttu-id="c51d9-103">取得應用程式控制項 VM/伺服器群組。</span><span class="sxs-lookup"><span data-stu-id="c51d9-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="c51d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="c51d9-104">SYNTAX</span></span>

### <span data-ttu-id="c51d9-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="c51d9-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c51d9-106">說明</span><span class="sxs-lookup"><span data-stu-id="c51d9-106">DESCRIPTION</span></span>
<span data-ttu-id="c51d9-107">彈性應用程式控制項是由 Azure 安全中心自動計算，使用此 Cmdlet 來取得應用程式控制項 VM/伺服器群組。</span><span class="sxs-lookup"><span data-stu-id="c51d9-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="c51d9-108">示例</span><span class="sxs-lookup"><span data-stu-id="c51d9-108">EXAMPLES</span></span>

### <span data-ttu-id="c51d9-109">範例1</span><span class="sxs-lookup"><span data-stu-id="c51d9-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="c51d9-110">取得應用程式控制項 VM/伺服器群組。</span><span class="sxs-lookup"><span data-stu-id="c51d9-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="c51d9-111">參數</span><span class="sxs-lookup"><span data-stu-id="c51d9-111">PARAMETERS</span></span>

### <span data-ttu-id="c51d9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c51d9-112">-DefaultProfile</span></span>
<span data-ttu-id="c51d9-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c51d9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c51d9-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="c51d9-114">-AscLocation</span></span>
<span data-ttu-id="c51d9-115">ASC 儲存訂閱資料的位置。</span><span class="sxs-lookup"><span data-stu-id="c51d9-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="c51d9-116">可從 [取得位置] 進行檢索。</span><span class="sxs-lookup"><span data-stu-id="c51d9-116">can be retrieved from Get locations.</span></span>

```yaml
Type: System.String
Parameter Sets: AscLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c51d9-117">-[名]</span><span class="sxs-lookup"><span data-stu-id="c51d9-117">-GroupName</span></span>
<span data-ttu-id="c51d9-118">應用程式控制項 VM/伺服器群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c51d9-118">Name of an application control VM/server group.</span></span>

```yaml
Type: System.String
Parameter Sets: GroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c51d9-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c51d9-119">-SubscriptionId</span></span>
<span data-ttu-id="c51d9-120">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="c51d9-120">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="c51d9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c51d9-121">CommonParameters</span></span>
<span data-ttu-id="c51d9-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c51d9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c51d9-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c51d9-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c51d9-124">輸入</span><span class="sxs-lookup"><span data-stu-id="c51d9-124">INPUTS</span></span>

### <span data-ttu-id="c51d9-125">System.object</span><span class="sxs-lookup"><span data-stu-id="c51d9-125">System.String</span></span>

## <span data-ttu-id="c51d9-126">輸出</span><span class="sxs-lookup"><span data-stu-id="c51d9-126">OUTPUTS</span></span>

### <span data-ttu-id="c51d9-127">PSSecurityAdaptiveApplicationControls 中的 AdaptiveApplicationControls （Security..。</span><span class="sxs-lookup"><span data-stu-id="c51d9-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="c51d9-128">筆記</span><span class="sxs-lookup"><span data-stu-id="c51d9-128">NOTES</span></span>

## <span data-ttu-id="c51d9-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="c51d9-129">RELATED LINKS</span></span>