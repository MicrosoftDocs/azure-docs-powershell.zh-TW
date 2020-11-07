---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: fffc77c4cfdd74a910086befb88d665351ae36a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789481"
---
# <span data-ttu-id="96bed-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="96bed-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="96bed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96bed-102">SYNOPSIS</span></span>
<span data-ttu-id="96bed-103">取得虛擬網路的目前使用量。</span><span class="sxs-lookup"><span data-stu-id="96bed-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="96bed-104">句法</span><span class="sxs-lookup"><span data-stu-id="96bed-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96bed-105">說明</span><span class="sxs-lookup"><span data-stu-id="96bed-105">DESCRIPTION</span></span>
<span data-ttu-id="96bed-106">**AzVirtualNetworkUsageList** Cmdlet 會取得指定虛擬網路的每個子網使用量。</span><span class="sxs-lookup"><span data-stu-id="96bed-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="96bed-107">示例</span><span class="sxs-lookup"><span data-stu-id="96bed-107">EXAMPLES</span></span>

### <span data-ttu-id="96bed-108">範例1</span><span class="sxs-lookup"><span data-stu-id="96bed-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet
CurrentValue : 1
Limit        : 65531
Unit         : Count

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet11
CurrentValue : 0
Limit        : 251
Unit         : Count
```

<span data-ttu-id="96bed-109">針對 usagetest 虛擬網路的使用方式，取得每個子網上的目前值。</span><span class="sxs-lookup"><span data-stu-id="96bed-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="96bed-110">參數</span><span class="sxs-lookup"><span data-stu-id="96bed-110">PARAMETERS</span></span>

### <span data-ttu-id="96bed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96bed-111">-DefaultProfile</span></span>
<span data-ttu-id="96bed-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96bed-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96bed-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="96bed-113">-Name</span></span>
<span data-ttu-id="96bed-114">指定虛擬網路的名稱以顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="96bed-114">Specifies the name of the virtual network to show usages for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96bed-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96bed-115">-ResourceGroupName</span></span>
<span data-ttu-id="96bed-116">指定虛擬網路所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="96bed-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96bed-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96bed-117">CommonParameters</span></span>
<span data-ttu-id="96bed-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96bed-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96bed-119">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="96bed-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96bed-120">輸入</span><span class="sxs-lookup"><span data-stu-id="96bed-120">INPUTS</span></span>

### <span data-ttu-id="96bed-121">System.object</span><span class="sxs-lookup"><span data-stu-id="96bed-121">System.String</span></span>

## <span data-ttu-id="96bed-122">輸出</span><span class="sxs-lookup"><span data-stu-id="96bed-122">OUTPUTS</span></span>

### <span data-ttu-id="96bed-123">PSVirtualNetworkUsage 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="96bed-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="96bed-124">筆記</span><span class="sxs-lookup"><span data-stu-id="96bed-124">NOTES</span></span>

## <span data-ttu-id="96bed-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="96bed-125">RELATED LINKS</span></span>