---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e2d80f6c132967e18e5a03a3a4bee4ed470f1719
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288280"
---
# <span data-ttu-id="a3ff4-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3ff4-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="a3ff4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ff4-103">從應用程式閘道移除自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="a3ff4-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="a3ff4-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3ff4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3ff4-105">說明</span><span class="sxs-lookup"><span data-stu-id="a3ff4-105">DESCRIPTION</span></span>
<span data-ttu-id="a3ff4-106">**AzApplicationGatewayAutoscaleConfiguration** Cmdlet 會從現有的應用程式閘道中移除自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="a3ff4-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="a3ff4-107">示例</span><span class="sxs-lookup"><span data-stu-id="a3ff4-107">EXAMPLES</span></span>

### <span data-ttu-id="a3ff4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a3ff4-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="a3ff4-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="a3ff4-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="a3ff4-110">第二個命令會從應用程式閘道中移除自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="a3ff4-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="a3ff4-111">第三個命令會更新 Azure 上的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="a3ff4-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="a3ff4-112">參數</span><span class="sxs-lookup"><span data-stu-id="a3ff4-112">PARAMETERS</span></span>

### <span data-ttu-id="a3ff4-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3ff4-113">-ApplicationGateway</span></span>
<span data-ttu-id="a3ff4-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3ff4-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3ff4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ff4-115">-DefaultProfile</span></span>
<span data-ttu-id="a3ff4-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3ff4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3ff4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a3ff4-117">-Force</span></span>
<span data-ttu-id="a3ff4-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="a3ff4-118">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ff4-119">-確認</span><span class="sxs-lookup"><span data-stu-id="a3ff4-119">-Confirm</span></span>
<span data-ttu-id="a3ff4-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a3ff4-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ff4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3ff4-121">-WhatIf</span></span>
<span data-ttu-id="a3ff4-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a3ff4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3ff4-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3ff4-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ff4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ff4-124">CommonParameters</span></span>
<span data-ttu-id="a3ff4-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3ff4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ff4-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a3ff4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ff4-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a3ff4-127">INPUTS</span></span>

### <span data-ttu-id="a3ff4-128">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a3ff4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a3ff4-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a3ff4-129">OUTPUTS</span></span>

### <span data-ttu-id="a3ff4-130">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a3ff4-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a3ff4-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a3ff4-131">NOTES</span></span>

## <span data-ttu-id="a3ff4-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3ff4-132">RELATED LINKS</span></span>

[<span data-ttu-id="a3ff4-133">AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3ff4-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="a3ff4-134">新-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3ff4-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="a3ff4-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3ff4-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)