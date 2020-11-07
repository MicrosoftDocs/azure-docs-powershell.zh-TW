---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWan.md
ms.openlocfilehash: d017ef97d7c8a1834a8cab2de979e017251adf7f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959207"
---
# <span data-ttu-id="cd75e-101">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cd75e-101">Get-AzVirtualWan</span></span>

## <span data-ttu-id="cd75e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cd75e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd75e-103">取得資源群組或訂閱中的虛擬 WAN 或所有虛擬 Wan。</span><span class="sxs-lookup"><span data-stu-id="cd75e-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="cd75e-104">句法</span><span class="sxs-lookup"><span data-stu-id="cd75e-104">SYNTAX</span></span>

### <span data-ttu-id="cd75e-105">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="cd75e-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd75e-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd75e-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualWan [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd75e-107">說明</span><span class="sxs-lookup"><span data-stu-id="cd75e-107">DESCRIPTION</span></span>
<span data-ttu-id="cd75e-108">取得資源群組或訂閱中的虛擬 WAN 或所有虛擬 Wan。</span><span class="sxs-lookup"><span data-stu-id="cd75e-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="cd75e-109">示例</span><span class="sxs-lookup"><span data-stu-id="cd75e-109">EXAMPLES</span></span>

### <span data-ttu-id="cd75e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="cd75e-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : myVirtualWAN
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="cd75e-111">這個命令會取得資源群組 testRG 中名為 myVirtualWAN 的虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="cd75e-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

### <span data-ttu-id="cd75e-112">範例2</span><span class="sxs-lookup"><span data-stu-id="cd75e-112">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualWan -Name test*

Name                       : test1
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test1
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded

Name                       : test2
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/test2
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="cd75e-113">這個命令會從「test」開始取得所有虛擬 Wan。</span><span class="sxs-lookup"><span data-stu-id="cd75e-113">This command gets all Virtual WANs starting with "test".</span></span>

## <span data-ttu-id="cd75e-114">參數</span><span class="sxs-lookup"><span data-stu-id="cd75e-114">PARAMETERS</span></span>

### <span data-ttu-id="cd75e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd75e-115">-DefaultProfile</span></span>
<span data-ttu-id="cd75e-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd75e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd75e-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="cd75e-117">-Name</span></span>
<span data-ttu-id="cd75e-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="cd75e-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="cd75e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd75e-119">-ResourceGroupName</span></span>
<span data-ttu-id="cd75e-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd75e-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="cd75e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd75e-121">CommonParameters</span></span>
<span data-ttu-id="cd75e-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cd75e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd75e-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cd75e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd75e-124">輸入</span><span class="sxs-lookup"><span data-stu-id="cd75e-124">INPUTS</span></span>

### <span data-ttu-id="cd75e-125">所有</span><span class="sxs-lookup"><span data-stu-id="cd75e-125">None</span></span>

## <span data-ttu-id="cd75e-126">輸出</span><span class="sxs-lookup"><span data-stu-id="cd75e-126">OUTPUTS</span></span>

### <span data-ttu-id="cd75e-127">PSVirtualWan 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cd75e-127">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="cd75e-128">筆記</span><span class="sxs-lookup"><span data-stu-id="cd75e-128">NOTES</span></span>

## <span data-ttu-id="cd75e-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd75e-129">RELATED LINKS</span></span>

[<span data-ttu-id="cd75e-130">新-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cd75e-130">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="cd75e-131">移除-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cd75e-131">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="cd75e-132">更新-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cd75e-132">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)