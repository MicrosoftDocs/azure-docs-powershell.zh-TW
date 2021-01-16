---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: ded757d1e81ef5db94157f4676ed91dc11680fd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274508"
---
# <span data-ttu-id="07695-101">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="07695-101">Remove-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="07695-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07695-102">SYNOPSIS</span></span>
<span data-ttu-id="07695-103">從應用程式閘道移除 ssl 設定檔。</span><span class="sxs-lookup"><span data-stu-id="07695-103">Removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="07695-104">句法</span><span class="sxs-lookup"><span data-stu-id="07695-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfile -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07695-105">說明</span><span class="sxs-lookup"><span data-stu-id="07695-105">DESCRIPTION</span></span>
<span data-ttu-id="07695-106">**AzApplicationGatewaySslProfile** Cmdlet 會從應用程式閘道中移除 ssl 設定檔。</span><span class="sxs-lookup"><span data-stu-id="07695-106">The **Remove-AzApplicationGatewaySslProfile** cmdlet removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="07695-107">示例</span><span class="sxs-lookup"><span data-stu-id="07695-107">EXAMPLES</span></span>

### <span data-ttu-id="07695-108">範例1</span><span class="sxs-lookup"><span data-stu-id="07695-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "SslProfile01"
```

<span data-ttu-id="07695-109">第一個命令會取得一個名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="07695-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="07695-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 SslProfile01 的 ssl 設定檔。</span><span class="sxs-lookup"><span data-stu-id="07695-110">The second command removes the ssl profile named SslProfile01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="07695-111">參數</span><span class="sxs-lookup"><span data-stu-id="07695-111">PARAMETERS</span></span>

### <span data-ttu-id="07695-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07695-112">-ApplicationGateway</span></span>
<span data-ttu-id="07695-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07695-113">The applicationGateway</span></span>

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

### <span data-ttu-id="07695-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07695-114">-DefaultProfile</span></span>
<span data-ttu-id="07695-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="07695-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07695-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="07695-116">-Name</span></span>
<span data-ttu-id="07695-117">Ssl 設定檔的名稱</span><span class="sxs-lookup"><span data-stu-id="07695-117">The name of the ssl profile</span></span>

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

### <span data-ttu-id="07695-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07695-118">CommonParameters</span></span>
<span data-ttu-id="07695-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07695-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07695-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="07695-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07695-121">輸入</span><span class="sxs-lookup"><span data-stu-id="07695-121">INPUTS</span></span>

### <span data-ttu-id="07695-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="07695-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="07695-123">輸出</span><span class="sxs-lookup"><span data-stu-id="07695-123">OUTPUTS</span></span>

### <span data-ttu-id="07695-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="07695-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="07695-125">筆記</span><span class="sxs-lookup"><span data-stu-id="07695-125">NOTES</span></span>

## <span data-ttu-id="07695-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="07695-126">RELATED LINKS</span></span>

[<span data-ttu-id="07695-127">新-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="07695-127">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="07695-128">附加 AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="07695-128">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="07695-129">AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="07695-129">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="07695-130">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="07695-130">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)