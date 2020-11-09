---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: 4b96ec4fb263d262419d1c545cd9b1f0c35da413
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286952"
---
# <span data-ttu-id="dd55b-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd55b-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="dd55b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd55b-102">SYNOPSIS</span></span>
<span data-ttu-id="dd55b-103">取得現有的網路設定檔頂層資源</span><span class="sxs-lookup"><span data-stu-id="dd55b-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="dd55b-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd55b-104">SYNTAX</span></span>

### <span data-ttu-id="dd55b-105">GetByResourceNameNoExpandParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dd55b-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd55b-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd55b-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd55b-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd55b-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd55b-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd55b-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd55b-109">說明</span><span class="sxs-lookup"><span data-stu-id="dd55b-109">DESCRIPTION</span></span>
<span data-ttu-id="dd55b-110">**AzNetworkProfile** Cmdlet 會檢索現有的網路設定檔頂層資源</span><span class="sxs-lookup"><span data-stu-id="dd55b-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="dd55b-111">示例</span><span class="sxs-lookup"><span data-stu-id="dd55b-111">EXAMPLES</span></span>

### <span data-ttu-id="dd55b-112">範例1</span><span class="sxs-lookup"><span data-stu-id="dd55b-112">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1
```

<span data-ttu-id="dd55b-113">這會在資源群組 rg1 中檢索網路設定檔 np1</span><span class="sxs-lookup"><span data-stu-id="dd55b-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="dd55b-114">範例2</span><span class="sxs-lookup"><span data-stu-id="dd55b-114">Example 2</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np*

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np2
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np2
```

<span data-ttu-id="dd55b-115">這會檢索以 "np" 開頭的網路設定檔</span><span class="sxs-lookup"><span data-stu-id="dd55b-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="dd55b-116">參數</span><span class="sxs-lookup"><span data-stu-id="dd55b-116">PARAMETERS</span></span>

### <span data-ttu-id="dd55b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd55b-117">-DefaultProfile</span></span>
<span data-ttu-id="dd55b-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd55b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd55b-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="dd55b-119">-ExpandResource</span></span>
<span data-ttu-id="dd55b-120">要展開的資源參照。</span><span class="sxs-lookup"><span data-stu-id="dd55b-120">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceIdExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd55b-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd55b-121">-Name</span></span>
<span data-ttu-id="dd55b-122">網路設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd55b-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dd55b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd55b-123">-ResourceGroupName</span></span>
<span data-ttu-id="dd55b-124">網路設定檔的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="dd55b-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dd55b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd55b-125">-ResourceId</span></span>
<span data-ttu-id="dd55b-126">網路設定檔的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd55b-126">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd55b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd55b-127">CommonParameters</span></span>
<span data-ttu-id="dd55b-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd55b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd55b-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dd55b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd55b-130">輸入</span><span class="sxs-lookup"><span data-stu-id="dd55b-130">INPUTS</span></span>

### <span data-ttu-id="dd55b-131">System.object</span><span class="sxs-lookup"><span data-stu-id="dd55b-131">System.String</span></span>

## <span data-ttu-id="dd55b-132">輸出</span><span class="sxs-lookup"><span data-stu-id="dd55b-132">OUTPUTS</span></span>

### <span data-ttu-id="dd55b-133">PSNetworkProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dd55b-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="dd55b-134">筆記</span><span class="sxs-lookup"><span data-stu-id="dd55b-134">NOTES</span></span>

## <span data-ttu-id="dd55b-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd55b-135">RELATED LINKS</span></span>

[<span data-ttu-id="dd55b-136">新-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd55b-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="dd55b-137">移除-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd55b-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="dd55b-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd55b-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)