---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 93c4c86fec18ac13622078cbc17f7a0d895fd50b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626425"
---
# <span data-ttu-id="6311a-101">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6311a-101">Remove-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="6311a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6311a-102">SYNOPSIS</span></span>
<span data-ttu-id="6311a-103">從應用程式閘道移除前端埠。</span><span class="sxs-lookup"><span data-stu-id="6311a-103">Removes a front-end port from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6311a-104">句法</span><span class="sxs-lookup"><span data-stu-id="6311a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6311a-105">說明</span><span class="sxs-lookup"><span data-stu-id="6311a-105">DESCRIPTION</span></span>
<span data-ttu-id="6311a-106">**AzureRmApplicationGatewayFrontendPort** Cmdlet 會將前端埠從 Azure 應用程式閘道中移除。</span><span class="sxs-lookup"><span data-stu-id="6311a-106">The **Remove-AzureRmApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="6311a-107">示例</span><span class="sxs-lookup"><span data-stu-id="6311a-107">EXAMPLES</span></span>

### <span data-ttu-id="6311a-108">範例：從應用程式閘道移除前端埠</span><span class="sxs-lookup"><span data-stu-id="6311a-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="6311a-109">第一個命令會取得一個名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並將閘道儲存 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="6311a-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>

<span data-ttu-id="6311a-110">第二個命令會從應用程式閘道移除名為 FrontEndPort02 的埠。</span><span class="sxs-lookup"><span data-stu-id="6311a-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="6311a-111">參數</span><span class="sxs-lookup"><span data-stu-id="6311a-111">PARAMETERS</span></span>

### <span data-ttu-id="6311a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6311a-112">-ApplicationGateway</span></span>
<span data-ttu-id="6311a-113">指定要移除前端埠的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="6311a-113">Specifies the application gateway from which to remove a front-end port.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6311a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6311a-114">-DefaultProfile</span></span>
<span data-ttu-id="6311a-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6311a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6311a-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="6311a-116">-Name</span></span>
<span data-ttu-id="6311a-117">指定要移除之前端埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="6311a-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="6311a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6311a-118">CommonParameters</span></span>
<span data-ttu-id="6311a-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6311a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6311a-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6311a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6311a-121">輸入</span><span class="sxs-lookup"><span data-stu-id="6311a-121">INPUTS</span></span>

### <span data-ttu-id="6311a-122">System.object</span><span class="sxs-lookup"><span data-stu-id="6311a-122">System.String</span></span>

## <span data-ttu-id="6311a-123">輸出</span><span class="sxs-lookup"><span data-stu-id="6311a-123">OUTPUTS</span></span>

### <span data-ttu-id="6311a-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6311a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6311a-125">筆記</span><span class="sxs-lookup"><span data-stu-id="6311a-125">NOTES</span></span>

## <span data-ttu-id="6311a-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="6311a-126">RELATED LINKS</span></span>

[<span data-ttu-id="6311a-127">附加 AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6311a-127">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6311a-128">AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6311a-128">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6311a-129">新-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6311a-129">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6311a-130">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6311a-130">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)

