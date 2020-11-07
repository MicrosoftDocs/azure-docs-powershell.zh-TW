---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
ms.openlocfilehash: 5fcdbeee663873292b463bf774762c9de5418b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625624"
---
# <span data-ttu-id="ed4fc-101">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ed4fc-101">Remove-AzureRmRouteFilter</span></span>

## <span data-ttu-id="ed4fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed4fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ed4fc-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="ed4fc-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed4fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed4fc-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed4fc-105">說明</span><span class="sxs-lookup"><span data-stu-id="ed4fc-105">DESCRIPTION</span></span>
<span data-ttu-id="ed4fc-106">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="ed4fc-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ed4fc-107">示例</span><span class="sxs-lookup"><span data-stu-id="ed4fc-107">EXAMPLES</span></span>

### <span data-ttu-id="ed4fc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ed4fc-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ed4fc-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="ed4fc-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="ed4fc-110">參數</span><span class="sxs-lookup"><span data-stu-id="ed4fc-110">PARAMETERS</span></span>

### <span data-ttu-id="ed4fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed4fc-111">-DefaultProfile</span></span>
<span data-ttu-id="ed4fc-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed4fc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed4fc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ed4fc-113">-Force</span></span>
<span data-ttu-id="ed4fc-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="ed4fc-114">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed4fc-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed4fc-115">-Name</span></span>
<span data-ttu-id="ed4fc-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ed4fc-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed4fc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed4fc-117">-PassThru</span></span>
<span data-ttu-id="ed4fc-118">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="ed4fc-118">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed4fc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed4fc-119">-ResourceGroupName</span></span>
<span data-ttu-id="ed4fc-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed4fc-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed4fc-121">-確認</span><span class="sxs-lookup"><span data-stu-id="ed4fc-121">-Confirm</span></span>
<span data-ttu-id="ed4fc-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed4fc-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed4fc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed4fc-123">-WhatIf</span></span>
<span data-ttu-id="ed4fc-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed4fc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed4fc-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed4fc-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed4fc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed4fc-126">CommonParameters</span></span>
<span data-ttu-id="ed4fc-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed4fc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed4fc-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed4fc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed4fc-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ed4fc-129">INPUTS</span></span>

### <span data-ttu-id="ed4fc-130">System.object</span><span class="sxs-lookup"><span data-stu-id="ed4fc-130">System.String</span></span>

## <span data-ttu-id="ed4fc-131">輸出</span><span class="sxs-lookup"><span data-stu-id="ed4fc-131">OUTPUTS</span></span>

### <span data-ttu-id="ed4fc-132">System.object</span><span class="sxs-lookup"><span data-stu-id="ed4fc-132">System.Object</span></span>

## <span data-ttu-id="ed4fc-133">筆記</span><span class="sxs-lookup"><span data-stu-id="ed4fc-133">NOTES</span></span>

## <span data-ttu-id="ed4fc-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed4fc-134">RELATED LINKS</span></span>
