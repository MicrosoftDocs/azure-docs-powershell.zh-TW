---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: d5871a9e1a99a27cc0b2728ca3638a0548f42fc6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796638"
---
# <span data-ttu-id="1d663-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1d663-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="1d663-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d663-102">SYNOPSIS</span></span>
<span data-ttu-id="1d663-103">建立新的 Azure 防火牆原則篩選規則集合</span><span class="sxs-lookup"><span data-stu-id="1d663-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="1d663-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d663-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d663-105">說明</span><span class="sxs-lookup"><span data-stu-id="1d663-105">DESCRIPTION</span></span>
<span data-ttu-id="1d663-106">**新的-AzFirewallPolicyFilterRuleCollection** Cmdlet 會建立 Azure 防火牆原則的篩選規則集合。</span><span class="sxs-lookup"><span data-stu-id="1d663-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="1d663-107">示例</span><span class="sxs-lookup"><span data-stu-id="1d663-107">EXAMPLES</span></span>

### <span data-ttu-id="1d663-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1d663-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="1d663-109">這個範例會建立含2個規則條件的篩選規則</span><span class="sxs-lookup"><span data-stu-id="1d663-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="1d663-110">參數</span><span class="sxs-lookup"><span data-stu-id="1d663-110">PARAMETERS</span></span>

### <span data-ttu-id="1d663-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="1d663-111">-ActionType</span></span>
<span data-ttu-id="1d663-112">規則集合的動作</span><span class="sxs-lookup"><span data-stu-id="1d663-112">The action of the rule collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d663-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d663-113">-DefaultProfile</span></span>
<span data-ttu-id="1d663-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1d663-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d663-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="1d663-115">-Name</span></span>
<span data-ttu-id="1d663-116">應用程式規則集合的名稱</span><span class="sxs-lookup"><span data-stu-id="1d663-116">The name of the Application Rule Collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d663-117">-優先順序</span><span class="sxs-lookup"><span data-stu-id="1d663-117">-Priority</span></span>
<span data-ttu-id="1d663-118">規則集合的優先順序</span><span class="sxs-lookup"><span data-stu-id="1d663-118">The priority of the rule collection</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d663-119">-規則</span><span class="sxs-lookup"><span data-stu-id="1d663-119">-Rule</span></span>
<span data-ttu-id="1d663-120">應用程式規則清單</span><span class="sxs-lookup"><span data-stu-id="1d663-120">The list of application rules</span></span>

```yaml
Type: PSAzureFirewallPolicyRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d663-121">-確認</span><span class="sxs-lookup"><span data-stu-id="1d663-121">-Confirm</span></span>
<span data-ttu-id="1d663-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1d663-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d663-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d663-123">-WhatIf</span></span>
<span data-ttu-id="1d663-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1d663-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d663-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d663-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d663-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d663-126">CommonParameters</span></span>
<span data-ttu-id="1d663-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d663-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d663-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1d663-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d663-129">輸入</span><span class="sxs-lookup"><span data-stu-id="1d663-129">INPUTS</span></span>

### <span data-ttu-id="1d663-130">所有</span><span class="sxs-lookup"><span data-stu-id="1d663-130">None</span></span>

## <span data-ttu-id="1d663-131">輸出</span><span class="sxs-lookup"><span data-stu-id="1d663-131">OUTPUTS</span></span>

### <span data-ttu-id="1d663-132">PSAzureFirewallPolicyRuleCollectionGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1d663-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="1d663-133">筆記</span><span class="sxs-lookup"><span data-stu-id="1d663-133">NOTES</span></span>

## <span data-ttu-id="1d663-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d663-134">RELATED LINKS</span></span>