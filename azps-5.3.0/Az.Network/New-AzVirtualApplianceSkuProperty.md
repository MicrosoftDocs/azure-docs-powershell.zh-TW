---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288692"
---
# <span data-ttu-id="c78d6-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="c78d6-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="c78d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c78d6-102">SYNOPSIS</span></span>
<span data-ttu-id="c78d6-103">定義資源的網路虛擬裝置 sku。</span><span class="sxs-lookup"><span data-stu-id="c78d6-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="c78d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="c78d6-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c78d6-105">說明</span><span class="sxs-lookup"><span data-stu-id="c78d6-105">DESCRIPTION</span></span>
<span data-ttu-id="c78d6-106">[New-AzVirtualApplianceSkuProperties] 命令會定義網路虛擬裝置資源的 Sku。</span><span class="sxs-lookup"><span data-stu-id="c78d6-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="c78d6-107">示例</span><span class="sxs-lookup"><span data-stu-id="c78d6-107">EXAMPLES</span></span>

### <span data-ttu-id="c78d6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c78d6-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="c78d6-109">建立要與 New-AzNetworkVirtualAppliance 命令搭配使用的虛擬裝置 Sku 屬性物件。</span><span class="sxs-lookup"><span data-stu-id="c78d6-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="c78d6-110">參數</span><span class="sxs-lookup"><span data-stu-id="c78d6-110">PARAMETERS</span></span>

### <span data-ttu-id="c78d6-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c78d6-111">-BundledScaleUnit</span></span>
<span data-ttu-id="c78d6-112">已捆綁比例單位。</span><span class="sxs-lookup"><span data-stu-id="c78d6-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="c78d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c78d6-113">-DefaultProfile</span></span>
<span data-ttu-id="c78d6-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c78d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c78d6-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="c78d6-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="c78d6-116">市場位置版本。</span><span class="sxs-lookup"><span data-stu-id="c78d6-116">The market place version.</span></span>

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

### <span data-ttu-id="c78d6-117">-VendorName</span><span class="sxs-lookup"><span data-stu-id="c78d6-117">-VendorName</span></span>
<span data-ttu-id="c78d6-118">供應商的名稱。</span><span class="sxs-lookup"><span data-stu-id="c78d6-118">The name of the vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78d6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c78d6-119">CommonParameters</span></span>
<span data-ttu-id="c78d6-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c78d6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c78d6-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c78d6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c78d6-122">輸入</span><span class="sxs-lookup"><span data-stu-id="c78d6-122">INPUTS</span></span>

### <span data-ttu-id="c78d6-123">所有</span><span class="sxs-lookup"><span data-stu-id="c78d6-123">None</span></span>

## <span data-ttu-id="c78d6-124">輸出</span><span class="sxs-lookup"><span data-stu-id="c78d6-124">OUTPUTS</span></span>

### <span data-ttu-id="c78d6-125">PSVirtualApplianceSkuProperties 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c78d6-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="c78d6-126">筆記</span><span class="sxs-lookup"><span data-stu-id="c78d6-126">NOTES</span></span>

## <span data-ttu-id="c78d6-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="c78d6-127">RELATED LINKS</span></span>