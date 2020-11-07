---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: fdbbb28d69d5094b52d8ac7340839fa570bce55d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800125"
---
# <span data-ttu-id="97ca7-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="97ca7-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="97ca7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97ca7-102">SYNOPSIS</span></span>
<span data-ttu-id="97ca7-103">將要求路由規則新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="97ca7-103">Adds a request routing rule to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97ca7-104">句法</span><span class="sxs-lookup"><span data-stu-id="97ca7-104">SYNTAX</span></span>

### <span data-ttu-id="97ca7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="97ca7-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97ca7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="97ca7-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97ca7-107">說明</span><span class="sxs-lookup"><span data-stu-id="97ca7-107">DESCRIPTION</span></span>
<span data-ttu-id="97ca7-108">**AzureRmApplicationGatewayRequestRoutingRule** Cmdlet 會將要求路由規則新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="97ca7-108">The **Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="97ca7-109">示例</span><span class="sxs-lookup"><span data-stu-id="97ca7-109">EXAMPLES</span></span>

### <span data-ttu-id="97ca7-110">範例1：將要求路由規則新增至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="97ca7-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="97ca7-111">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="97ca7-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="97ca7-112">第二個命令會將要求路由規則新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="97ca7-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="97ca7-113">參數</span><span class="sxs-lookup"><span data-stu-id="97ca7-113">PARAMETERS</span></span>

### <span data-ttu-id="97ca7-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97ca7-114">-ApplicationGateway</span></span>
<span data-ttu-id="97ca7-115">指定此 Cmdlet 新增要求路由規則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="97ca7-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="97ca7-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="97ca7-116">-BackendAddressPool</span></span>
<span data-ttu-id="97ca7-117">指定應用程式閘道後端位址集區物件。</span><span class="sxs-lookup"><span data-stu-id="97ca7-117">Specifies an application gateway back-end address pool object.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ca7-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="97ca7-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="97ca7-119">指定應用程式閘道後端位址集區 ID。</span><span class="sxs-lookup"><span data-stu-id="97ca7-119">Specifies an application gateway back-end address pool ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ca7-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="97ca7-120">-BackendHttpSettings</span></span>
<span data-ttu-id="97ca7-121">指定應用程式閘道的後端 HTTP 設定物件。</span><span class="sxs-lookup"><span data-stu-id="97ca7-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ca7-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="97ca7-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="97ca7-123">指定應用程式閘道的後端 HTTP 設定 ID。</span><span class="sxs-lookup"><span data-stu-id="97ca7-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ca7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97ca7-124">-DefaultProfile</span></span>
<span data-ttu-id="97ca7-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97ca7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97ca7-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="97ca7-126">-HttpListener</span></span>
<span data-ttu-id="97ca7-127">指定應用程式閘道 HTTP 攔截器物件。</span><span class="sxs-lookup"><span data-stu-id="97ca7-127">Specifies application gateway HTTP listener object.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ca7-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="97ca7-128">-HttpListenerId</span></span>
<span data-ttu-id="97ca7-129">指定應用程式閘道 HTTP 偵聽程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="97ca7-129">Specifies application gateway HTTP listener ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ca7-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="97ca7-130">-Name</span></span>
<span data-ttu-id="97ca7-131">指定此 Cmdlet 所新增之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="97ca7-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="97ca7-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="97ca7-132">-RedirectConfiguration</span></span>
<span data-ttu-id="97ca7-133">應用程式閘道 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="97ca7-133">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ca7-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="97ca7-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="97ca7-135">應用程式閘道 RedirectConfiguration 的 ID</span><span class="sxs-lookup"><span data-stu-id="97ca7-135">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ca7-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="97ca7-136">-RuleType</span></span>
<span data-ttu-id="97ca7-137">指定要求路由規則的類型。</span><span class="sxs-lookup"><span data-stu-id="97ca7-137">Specifies the type of request routing rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ca7-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="97ca7-138">-UrlPathMap</span></span>
```yaml
Type: PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ca7-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="97ca7-139">-UrlPathMapId</span></span>
<span data-ttu-id="97ca7-140">指定路由規則的 URL 路徑對應 ID。</span><span class="sxs-lookup"><span data-stu-id="97ca7-140">Specifies the URL path map ID for the routing rule.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ca7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ca7-141">CommonParameters</span></span>
<span data-ttu-id="97ca7-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97ca7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ca7-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97ca7-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ca7-144">輸入</span><span class="sxs-lookup"><span data-stu-id="97ca7-144">INPUTS</span></span>

### <span data-ttu-id="97ca7-145">System.object</span><span class="sxs-lookup"><span data-stu-id="97ca7-145">System.String</span></span>

## <span data-ttu-id="97ca7-146">輸出</span><span class="sxs-lookup"><span data-stu-id="97ca7-146">OUTPUTS</span></span>

### <span data-ttu-id="97ca7-147">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="97ca7-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="97ca7-148">筆記</span><span class="sxs-lookup"><span data-stu-id="97ca7-148">NOTES</span></span>

## <span data-ttu-id="97ca7-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="97ca7-149">RELATED LINKS</span></span>

[<span data-ttu-id="97ca7-150">AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="97ca7-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="97ca7-151">新-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="97ca7-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="97ca7-152">移除-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="97ca7-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="97ca7-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="97ca7-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)

