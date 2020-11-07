---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: be59f9ec0728b60314f137dcc5a57c7883935e52
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801581"
---
# <span data-ttu-id="a2d74-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a2d74-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="a2d74-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2d74-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d74-103">配置虛擬網路閘道連線的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2d74-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2d74-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2d74-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2d74-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2d74-105">DESCRIPTION</span></span>
<span data-ttu-id="a2d74-106">AzureRmVirtualNetworkGatewayConnectionSharedKey Cmdlet 會 **設定** 虛擬網路閘道連線的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2d74-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="a2d74-107">示例</span><span class="sxs-lookup"><span data-stu-id="a2d74-107">EXAMPLES</span></span>

### <span data-ttu-id="a2d74-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="a2d74-108">1:</span></span>
```

```

## <span data-ttu-id="a2d74-109">參數</span><span class="sxs-lookup"><span data-stu-id="a2d74-109">PARAMETERS</span></span>

### <span data-ttu-id="a2d74-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d74-110">-DefaultProfile</span></span>
<span data-ttu-id="a2d74-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2d74-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d74-112">-Force</span><span class="sxs-lookup"><span data-stu-id="a2d74-112">-Force</span></span>
<span data-ttu-id="a2d74-113">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a2d74-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d74-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2d74-114">-Name</span></span>
<span data-ttu-id="a2d74-115">指定虛擬網路閘道共用金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2d74-115">Specifies the name of the virtual network gateway shared key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2d74-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d74-116">-ResourceGroupName</span></span>
<span data-ttu-id="a2d74-117">指定虛擬網路閘道所屬之資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="a2d74-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2d74-118">-值</span><span class="sxs-lookup"><span data-stu-id="a2d74-118">-Value</span></span>
<span data-ttu-id="a2d74-119">指定共用金鑰的值。</span><span class="sxs-lookup"><span data-stu-id="a2d74-119">Specifies the value of the shared key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2d74-120">-確認</span><span class="sxs-lookup"><span data-stu-id="a2d74-120">-Confirm</span></span>
<span data-ttu-id="a2d74-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a2d74-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d74-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2d74-122">-WhatIf</span></span>
<span data-ttu-id="a2d74-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2d74-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2d74-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2d74-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d74-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d74-125">CommonParameters</span></span>
<span data-ttu-id="a2d74-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2d74-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d74-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2d74-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d74-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a2d74-128">INPUTS</span></span>

## <span data-ttu-id="a2d74-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a2d74-129">OUTPUTS</span></span>

### <span data-ttu-id="a2d74-130">System.object</span><span class="sxs-lookup"><span data-stu-id="a2d74-130">System.String</span></span>

## <span data-ttu-id="a2d74-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a2d74-131">NOTES</span></span>

## <span data-ttu-id="a2d74-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2d74-132">RELATED LINKS</span></span>

[<span data-ttu-id="a2d74-133">AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a2d74-133">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="a2d74-134">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a2d74-134">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

