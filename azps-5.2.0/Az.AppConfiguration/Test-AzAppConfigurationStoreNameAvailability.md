---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: c7f315d1989a6cbbfbfa08cf3f59cff8ccd811bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273236"
---
# <span data-ttu-id="ae5cf-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ae5cf-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="ae5cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae5cf-102">SYNOPSIS</span></span>
<span data-ttu-id="ae5cf-103">檢查 [配置] 儲存區名稱是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="ae5cf-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="ae5cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae5cf-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ae5cf-105">說明</span><span class="sxs-lookup"><span data-stu-id="ae5cf-105">DESCRIPTION</span></span>
<span data-ttu-id="ae5cf-106">檢查 [配置] 儲存區名稱是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="ae5cf-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="ae5cf-107">示例</span><span class="sxs-lookup"><span data-stu-id="ae5cf-107">EXAMPLES</span></span>

### <span data-ttu-id="ae5cf-108">範例1：測試應用程式設定儲存名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="ae5cf-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="ae5cf-109">這個命令會測試 app 配置儲存區名稱的可用性。</span><span class="sxs-lookup"><span data-stu-id="ae5cf-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="ae5cf-110">參數</span><span class="sxs-lookup"><span data-stu-id="ae5cf-110">PARAMETERS</span></span>

### <span data-ttu-id="ae5cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae5cf-111">-DefaultProfile</span></span>
<span data-ttu-id="ae5cf-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae5cf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5cf-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="ae5cf-113">-Name</span></span>
<span data-ttu-id="ae5cf-114">要檢查可用性的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae5cf-114">The name to check for availability.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5cf-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae5cf-115">-SubscriptionId</span></span>
<span data-ttu-id="ae5cf-116">Microsoft Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="ae5cf-116">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5cf-117">-確認</span><span class="sxs-lookup"><span data-stu-id="ae5cf-117">-Confirm</span></span>
<span data-ttu-id="ae5cf-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ae5cf-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5cf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae5cf-119">-WhatIf</span></span>
<span data-ttu-id="ae5cf-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae5cf-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae5cf-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae5cf-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5cf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae5cf-122">CommonParameters</span></span>
<span data-ttu-id="ae5cf-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae5cf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae5cf-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ae5cf-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae5cf-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ae5cf-125">INPUTS</span></span>

## <span data-ttu-id="ae5cf-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ae5cf-126">OUTPUTS</span></span>

### <span data-ttu-id="ae5cf-127">INameAvailabilityStatus （AppConfiguration）。 Api20200601。</span><span class="sxs-lookup"><span data-stu-id="ae5cf-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="ae5cf-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ae5cf-128">NOTES</span></span>

<span data-ttu-id="ae5cf-129">別名</span><span class="sxs-lookup"><span data-stu-id="ae5cf-129">ALIASES</span></span>

## <span data-ttu-id="ae5cf-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae5cf-130">RELATED LINKS</span></span>
