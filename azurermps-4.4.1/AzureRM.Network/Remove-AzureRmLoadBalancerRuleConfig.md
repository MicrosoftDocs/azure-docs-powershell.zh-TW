---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 38f6223fdf1dc230dbd34310b7eda2ab45e2d4b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623499"
---
# <span data-ttu-id="d8a49-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d8a49-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="d8a49-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8a49-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a49-103">移除負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="d8a49-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8a49-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8a49-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8a49-105">說明</span><span class="sxs-lookup"><span data-stu-id="d8a49-105">DESCRIPTION</span></span>
<span data-ttu-id="d8a49-106">**AzureRmLoadBalancerRuleConfig** Cmdlet 會移除 Azure 負載平衡器的規則配置。</span><span class="sxs-lookup"><span data-stu-id="d8a49-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="d8a49-107">示例</span><span class="sxs-lookup"><span data-stu-id="d8a49-107">EXAMPLES</span></span>

### <span data-ttu-id="d8a49-108">範例1：從負載平衡器移除規則配置</span><span class="sxs-lookup"><span data-stu-id="d8a49-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="d8a49-109">第一個命令會取得名為 MyLoadBalancer 的負載平衡器，然後將它儲存在 $loadbalancer 變數中。</span><span class="sxs-lookup"><span data-stu-id="d8a49-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="d8a49-110">第二個命令會從 $loadbalancer 中的負載平衡器移除名為 MyLBruleName 的規則配置。</span><span class="sxs-lookup"><span data-stu-id="d8a49-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="d8a49-111">參數</span><span class="sxs-lookup"><span data-stu-id="d8a49-111">PARAMETERS</span></span>

### <span data-ttu-id="d8a49-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d8a49-112">-LoadBalancer</span></span>
<span data-ttu-id="d8a49-113">指定包含此 Cmdlet 移除之規則配置的 **LoadBalancer** 物件。</span><span class="sxs-lookup"><span data-stu-id="d8a49-113">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a49-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8a49-114">-Name</span></span>
<span data-ttu-id="d8a49-115">指定此 Cmdlet 移除的負載等化器規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="d8a49-115">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8a49-116">-DefaultProfile</span></span>
<span data-ttu-id="d8a49-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8a49-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a49-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a49-118">CommonParameters</span></span>
<span data-ttu-id="d8a49-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8a49-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a49-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d8a49-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a49-121">輸入</span><span class="sxs-lookup"><span data-stu-id="d8a49-121">INPUTS</span></span>

### <span data-ttu-id="d8a49-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d8a49-122">PSLoadBalancer</span></span>
<span data-ttu-id="d8a49-123">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d8a49-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d8a49-124">輸出</span><span class="sxs-lookup"><span data-stu-id="d8a49-124">OUTPUTS</span></span>

### <span data-ttu-id="d8a49-125">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d8a49-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d8a49-126">筆記</span><span class="sxs-lookup"><span data-stu-id="d8a49-126">NOTES</span></span>

## <span data-ttu-id="d8a49-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8a49-127">RELATED LINKS</span></span>

[<span data-ttu-id="d8a49-128">附加 AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d8a49-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="d8a49-129">AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d8a49-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="d8a49-130">AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d8a49-130">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="d8a49-131">新-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d8a49-131">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="d8a49-132">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d8a49-132">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)

