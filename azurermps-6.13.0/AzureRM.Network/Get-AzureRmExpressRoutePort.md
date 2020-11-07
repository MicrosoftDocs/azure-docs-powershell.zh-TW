---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
ms.openlocfilehash: 36c15c9a0bfae9bbf3a14f59877d23c1c8778163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626070"
---
# <span data-ttu-id="14857-101">Get-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="14857-101">Get-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="14857-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14857-102">SYNOPSIS</span></span>
<span data-ttu-id="14857-103">取得 Azure ExpressRoutePort 資源。</span><span class="sxs-lookup"><span data-stu-id="14857-103">Gets an Azure ExpressRoutePort resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14857-104">句法</span><span class="sxs-lookup"><span data-stu-id="14857-104">SYNTAX</span></span>

### <span data-ttu-id="14857-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="14857-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14857-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14857-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14857-107">說明</span><span class="sxs-lookup"><span data-stu-id="14857-107">DESCRIPTION</span></span>
<span data-ttu-id="14857-108">**AzureRmExpressRoutePort** Cmdlet 是用來從您的訂閱中檢索 ExpressRoutePort 物件。</span><span class="sxs-lookup"><span data-stu-id="14857-108">The **Get-AzureRmExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="14857-109">傳回的 expressrouteport 物件可以用來做為在 ExpressRoutePort 上執行的其他 Cmdlet 的輸入。</span><span class="sxs-lookup"><span data-stu-id="14857-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="14857-110">示例</span><span class="sxs-lookup"><span data-stu-id="14857-110">EXAMPLES</span></span>

### <span data-ttu-id="14857-111">範例1</span><span class="sxs-lookup"><span data-stu-id="14857-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="14857-112">取得您訂閱中的 [資源群組] $rg 中名稱 $PortName 的 ExpressRoutePort 物件。</span><span class="sxs-lookup"><span data-stu-id="14857-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="14857-113">範例2</span><span class="sxs-lookup"><span data-stu-id="14857-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -ResourceId $id
```

<span data-ttu-id="14857-114">取得 ExpressRoutePort 物件，其中包含 ResourceId $id。</span><span class="sxs-lookup"><span data-stu-id="14857-114">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="14857-115">參數</span><span class="sxs-lookup"><span data-stu-id="14857-115">PARAMETERS</span></span>

### <span data-ttu-id="14857-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14857-116">-DefaultProfile</span></span>
<span data-ttu-id="14857-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="14857-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14857-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="14857-118">-Name</span></span>
<span data-ttu-id="14857-119">ExpressRoutePort 的名稱。</span><span class="sxs-lookup"><span data-stu-id="14857-119">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14857-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14857-120">-ResourceGroupName</span></span>
<span data-ttu-id="14857-121">ExpressRoutePort 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="14857-121">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14857-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14857-122">-ResourceId</span></span>
<span data-ttu-id="14857-123">快速路由埠的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="14857-123">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14857-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14857-124">CommonParameters</span></span>
<span data-ttu-id="14857-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14857-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14857-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="14857-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14857-127">輸入</span><span class="sxs-lookup"><span data-stu-id="14857-127">INPUTS</span></span>

### <span data-ttu-id="14857-128">System.object</span><span class="sxs-lookup"><span data-stu-id="14857-128">System.String</span></span>

## <span data-ttu-id="14857-129">輸出</span><span class="sxs-lookup"><span data-stu-id="14857-129">OUTPUTS</span></span>

### <span data-ttu-id="14857-130">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="14857-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="14857-131">筆記</span><span class="sxs-lookup"><span data-stu-id="14857-131">NOTES</span></span>

## <span data-ttu-id="14857-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="14857-132">RELATED LINKS</span></span>