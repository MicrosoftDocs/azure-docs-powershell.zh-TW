---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1c998ee5f577a8e8ccbfa64d92316e6a9f0782f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623232"
---
# <span data-ttu-id="0be46-101">Get-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="0be46-101">Get-AzsSubscription</span></span>

## <span data-ttu-id="0be46-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0be46-102">SYNOPSIS</span></span>
<span data-ttu-id="0be46-103">取得訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="0be46-103">Get the list of subscriptions.</span></span>

## <span data-ttu-id="0be46-104">句法</span><span class="sxs-lookup"><span data-stu-id="0be46-104">SYNTAX</span></span>

### <span data-ttu-id="0be46-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="0be46-105">List (Default)</span></span>
```
Get-AzsSubscription [<CommonParameters>]
```

### <span data-ttu-id="0be46-106">獲取</span><span class="sxs-lookup"><span data-stu-id="0be46-106">Get</span></span>
```
Get-AzsSubscription [-SubscriptionId] <String> [<CommonParameters>]
```

## <span data-ttu-id="0be46-107">說明</span><span class="sxs-lookup"><span data-stu-id="0be46-107">DESCRIPTION</span></span>
<span data-ttu-id="0be46-108">取得訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="0be46-108">Get the list of subscriptions.</span></span>

## <span data-ttu-id="0be46-109">示例</span><span class="sxs-lookup"><span data-stu-id="0be46-109">EXAMPLES</span></span>

### <span data-ttu-id="0be46-110">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0be46-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscription
```

<span data-ttu-id="0be46-111">取得訂閱清單。</span><span class="sxs-lookup"><span data-stu-id="0be46-111">Get the list of subscriptions.</span></span>

## <span data-ttu-id="0be46-112">參數</span><span class="sxs-lookup"><span data-stu-id="0be46-112">PARAMETERS</span></span>

### <span data-ttu-id="0be46-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0be46-113">-SubscriptionId</span></span>
<span data-ttu-id="0be46-114">訂閱的 Id。</span><span class="sxs-lookup"><span data-stu-id="0be46-114">Id of the subscription.</span></span>

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

### <span data-ttu-id="0be46-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be46-115">CommonParameters</span></span>
<span data-ttu-id="0be46-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0be46-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be46-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0be46-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be46-118">輸入</span><span class="sxs-lookup"><span data-stu-id="0be46-118">INPUTS</span></span>

## <span data-ttu-id="0be46-119">輸出</span><span class="sxs-lookup"><span data-stu-id="0be46-119">OUTPUTS</span></span>

### <span data-ttu-id="0be46-120">AzureStack. SubscriptionModel 的 [訂閱]。</span><span class="sxs-lookup"><span data-stu-id="0be46-120">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="0be46-121">筆記</span><span class="sxs-lookup"><span data-stu-id="0be46-121">NOTES</span></span>

## <span data-ttu-id="0be46-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="0be46-122">RELATED LINKS</span></span>
