---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: fdbb023c6796a780bfe9e6474191185a58489c91
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286940"
---
# <span data-ttu-id="4bb29-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4bb29-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="4bb29-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4bb29-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb29-103">取得私人連結服務</span><span class="sxs-lookup"><span data-stu-id="4bb29-103">Gets private link service</span></span>

## <span data-ttu-id="4bb29-104">句法</span><span class="sxs-lookup"><span data-stu-id="4bb29-104">SYNTAX</span></span>

### <span data-ttu-id="4bb29-105">NoExpand (預設) </span><span class="sxs-lookup"><span data-stu-id="4bb29-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bb29-106">擴充</span><span class="sxs-lookup"><span data-stu-id="4bb29-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bb29-107">說明</span><span class="sxs-lookup"><span data-stu-id="4bb29-107">DESCRIPTION</span></span>
<span data-ttu-id="4bb29-108">**AzPrivateLinkService** Cmdlet 會取得一或多個私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="4bb29-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="4bb29-109">示例</span><span class="sxs-lookup"><span data-stu-id="4bb29-109">EXAMPLES</span></span>

### <span data-ttu-id="4bb29-110">範例</span><span class="sxs-lookup"><span data-stu-id="4bb29-110">Example</span></span>
```
Get-AzPrivateLinkService -Name MyPLS -ResourceGroupName TestResourceGroup

Name                                 : MyPLS
ResourceGroupName                    : TestResourceGroup
Id                                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/prov
                                       iders/Microsoft.Network/privateLinkServices/MyPLS
Location                             : eastus2euap
Type                                 : Microsoft.Network/privateLinkServices
Etag                                 : W/"00000000-0000-0000-0000-000000000000"
Tag                                  : {}
ProvisioningState                    : Succeeded
Visibility                           : 
AutoApproval                         : 
Alias                                :
LoadBalancerFrontendIpConfigurations : []
IpConfigurations                     : [
                                         {
                                           "PrivateIPAddress": "10.0.2.5",
                                           "PrivateIPAllocationMethod": "Static",
                                           "ProvisioningState": "Failed",
                                           "PrivateIPAddressVersion": "IPv4",
                                           "Name": "IP-Config",
                                           "Subnet": {
                                             "Delegations": [],
                                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/
                                       TestResourceGroup/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/backendSubne
                                       t",
                                             "ServiceAssociationLinks": []
                                           }
                                         }
                                       ]
PrivateEndpointConnections           : []
NetworkInterfaces                    : [
                                         {
                                           "TapConfigurations": [],
                                           "HostedWorkloads": [],
                                           "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/mytestinterface"
                                         }
                                       ]
```

<span data-ttu-id="4bb29-111">這個 commandlet 會取得 [資源] 群組中的私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="4bb29-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="4bb29-112">參數</span><span class="sxs-lookup"><span data-stu-id="4bb29-112">PARAMETERS</span></span>

### <span data-ttu-id="4bb29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb29-113">-DefaultProfile</span></span>
<span data-ttu-id="4bb29-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4bb29-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bb29-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4bb29-115">-ExpandResource</span></span>
<span data-ttu-id="4bb29-116">要展開的資源參照。</span><span class="sxs-lookup"><span data-stu-id="4bb29-116">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb29-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4bb29-117">-Name</span></span>
<span data-ttu-id="4bb29-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4bb29-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb29-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bb29-119">-ResourceGroupName</span></span>
<span data-ttu-id="4bb29-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bb29-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb29-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb29-121">CommonParameters</span></span>
<span data-ttu-id="4bb29-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4bb29-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb29-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4bb29-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb29-124">輸入</span><span class="sxs-lookup"><span data-stu-id="4bb29-124">INPUTS</span></span>

### <span data-ttu-id="4bb29-125">System.object</span><span class="sxs-lookup"><span data-stu-id="4bb29-125">System.String</span></span>

## <span data-ttu-id="4bb29-126">輸出</span><span class="sxs-lookup"><span data-stu-id="4bb29-126">OUTPUTS</span></span>

### <span data-ttu-id="4bb29-127">PSPrivateLinkService 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4bb29-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="4bb29-128">筆記</span><span class="sxs-lookup"><span data-stu-id="4bb29-128">NOTES</span></span>

## <span data-ttu-id="4bb29-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bb29-129">RELATED LINKS</span></span>