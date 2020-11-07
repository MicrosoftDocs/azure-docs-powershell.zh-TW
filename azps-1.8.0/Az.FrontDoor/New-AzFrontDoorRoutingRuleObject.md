---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 02291202966ab832bf11edbd59a1504c001c948e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787786"
---
# <span data-ttu-id="66f78-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="66f78-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="66f78-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66f78-102">SYNOPSIS</span></span>
<span data-ttu-id="66f78-103">建立 PSRoutingRuleObject 以建立前門</span><span class="sxs-lookup"><span data-stu-id="66f78-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="66f78-104">句法</span><span class="sxs-lookup"><span data-stu-id="66f78-104">SYNTAX</span></span>

### <span data-ttu-id="66f78-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="66f78-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66f78-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66f78-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <PSRedirectType>] [-RedirectProtocol <PSRedirectProtocol>] [-CustomHost <String>]
 [-CustomPath <String>] [-CustomFragment <String>] [-CustomQueryString <String>]
 [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66f78-107">說明</span><span class="sxs-lookup"><span data-stu-id="66f78-107">DESCRIPTION</span></span>
<span data-ttu-id="66f78-108">建立 PSRoutingRuleObject 以建立前門</span><span class="sxs-lookup"><span data-stu-id="66f78-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="66f78-109">示例</span><span class="sxs-lookup"><span data-stu-id="66f78-109">EXAMPLES</span></span>

### <span data-ttu-id="66f78-110">範例1：建立 PSRoutingRuleObject 以使用前門建立</span><span class="sxs-lookup"><span data-stu-id="66f78-110">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
ForwardingProtocol           : MatchRequest
CustomForwardingPath         :
QueryParameterStripDirective : StripAll
DynamicCompression           : Enabled
HealthProbeSettings          :
BackendPoolId                : /subscriptions/{subid}/resourceGroups/{rgname}/prov
                               iders/Microsoft.Network/frontDoors/{frontdoorname}/BackendPools/backendPool1
EnableCaching                : Disabled
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : routingrule1
Type                         :
```

<span data-ttu-id="66f78-111">建立 PSRoutingRuleObject 以建立前門</span><span class="sxs-lookup"><span data-stu-id="66f78-111">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="66f78-112">參數</span><span class="sxs-lookup"><span data-stu-id="66f78-112">PARAMETERS</span></span>

### <span data-ttu-id="66f78-113">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="66f78-113">-AcceptedProtocol</span></span>
<span data-ttu-id="66f78-114">此規則要符合的通訊協定方案。</span><span class="sxs-lookup"><span data-stu-id="66f78-114">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="66f78-115">預設值為 {Https、Http}</span><span class="sxs-lookup"><span data-stu-id="66f78-115">Default value is {Https, Http}</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f78-116">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="66f78-116">-BackendPoolName</span></span>
<span data-ttu-id="66f78-117">此規則路由之 BackendPool 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="66f78-117">Resource id of the BackendPool which this rule routes to</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f78-118">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="66f78-118">-CustomForwardingPath</span></span>
<span data-ttu-id="66f78-119">用來重新寫入此規則所符合之資源路徑的自訂路徑。</span><span class="sxs-lookup"><span data-stu-id="66f78-119">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="66f78-120">若要使用傳入路徑，請保留空白。</span><span class="sxs-lookup"><span data-stu-id="66f78-120">Leave empty to use incoming path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f78-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="66f78-121">-CustomFragment</span></span>
<span data-ttu-id="66f78-122">要新增至重新導向 URL 的片段。</span><span class="sxs-lookup"><span data-stu-id="66f78-122">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="66f78-123">[片段] 是位於 # 之後的 URL 部分。</span><span class="sxs-lookup"><span data-stu-id="66f78-123">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="66f78-124">請勿包含 #。</span><span class="sxs-lookup"><span data-stu-id="66f78-124">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f78-125">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="66f78-125">-CustomHost</span></span>
<span data-ttu-id="66f78-126">要重新導向的主機。</span><span class="sxs-lookup"><span data-stu-id="66f78-126">Host to redirect.</span></span> <span data-ttu-id="66f78-127">[留空] 可將傳入主機做為目的地主機。</span><span class="sxs-lookup"><span data-stu-id="66f78-127">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f78-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="66f78-128">-CustomPath</span></span>
<span data-ttu-id="66f78-129">要重新導向的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="66f78-129">The full path to redirect.</span></span> <span data-ttu-id="66f78-130">Path 不能為空白，且必須以/開頭。</span><span class="sxs-lookup"><span data-stu-id="66f78-130">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="66f78-131">[留空] 可使用傳入路徑做為目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="66f78-131">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f78-132">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="66f78-132">-CustomQueryString</span></span>
<span data-ttu-id="66f78-133">要放在重新導向 URL 中的一組查詢字串。</span><span class="sxs-lookup"><span data-stu-id="66f78-133">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="66f78-134">設定此值會取代任何現有的查詢字串;保留空白以保留傳入查詢字串。</span><span class="sxs-lookup"><span data-stu-id="66f78-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="66f78-135">查詢字串必須在 <key>=</span><span class="sxs-lookup"><span data-stu-id="66f78-135">Query string must be in <key>=</span></span><value> <span data-ttu-id="66f78-136">設置.</span><span class="sxs-lookup"><span data-stu-id="66f78-136">format.</span></span> <span data-ttu-id="66f78-137">第一個？</span><span class="sxs-lookup"><span data-stu-id="66f78-137">The first ?</span></span> <span data-ttu-id="66f78-138">而且 & 將會自動新增，因此不要將它們包含在前面，但使用 & 來分隔多個查詢字串。</span><span class="sxs-lookup"><span data-stu-id="66f78-138">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f78-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f78-139">-DefaultProfile</span></span>
<span data-ttu-id="66f78-140">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66f78-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66f78-141">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="66f78-141">-DynamicCompression</span></span>
<span data-ttu-id="66f78-142">啟用快取時是否要針對快取的內容啟用動態壓縮。</span><span class="sxs-lookup"><span data-stu-id="66f78-142">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="66f78-143">已啟用預設值</span><span class="sxs-lookup"><span data-stu-id="66f78-143">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f78-144">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="66f78-144">-EnableCaching</span></span>
<span data-ttu-id="66f78-145">是否要啟用此路由的快取。</span><span class="sxs-lookup"><span data-stu-id="66f78-145">Whether to enable caching for this route.</span></span> <span data-ttu-id="66f78-146">預設值為 false</span><span class="sxs-lookup"><span data-stu-id="66f78-146">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f78-147">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="66f78-147">-EnabledState</span></span>
<span data-ttu-id="66f78-148">是否啟用此規則的使用。</span><span class="sxs-lookup"><span data-stu-id="66f78-148">Whether to enable use of this rule.</span></span>
<span data-ttu-id="66f78-149">已啟用預設值</span><span class="sxs-lookup"><span data-stu-id="66f78-149">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f78-150">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="66f78-150">-ForwardingProtocol</span></span>
<span data-ttu-id="66f78-151">當您將流量轉寄到 backends 預設值時，此規則將使用的通訊協定 MatchRequest。</span><span class="sxs-lookup"><span data-stu-id="66f78-151">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f78-152">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="66f78-152">-FrontDoorName</span></span>
<span data-ttu-id="66f78-153">此傳送規則所屬之前門的名稱。</span><span class="sxs-lookup"><span data-stu-id="66f78-153">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="66f78-154">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="66f78-154">-FrontendEndpointName</span></span>
<span data-ttu-id="66f78-155">與此規則關聯之前端端點的名稱</span><span class="sxs-lookup"><span data-stu-id="66f78-155">The names of Frontend endpoints associated with this rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f78-156">-名稱</span><span class="sxs-lookup"><span data-stu-id="66f78-156">-Name</span></span>
<span data-ttu-id="66f78-157">RoutingRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="66f78-157">RoutingRule name.</span></span>

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

### <span data-ttu-id="66f78-158">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="66f78-158">-PatternToMatch</span></span>
<span data-ttu-id="66f78-159">規則的路由模式，除了可能位於路徑最後/結尾的以外，不能有任何 \*。</span><span class="sxs-lookup"><span data-stu-id="66f78-159">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="66f78-160">預設值為/\*</span><span class="sxs-lookup"><span data-stu-id="66f78-160">Default value is /\*</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f78-161">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="66f78-161">-QueryParameterStripDirective</span></span>
<span data-ttu-id="66f78-162">在形成快取鍵時處理 URL 查詢字詞。</span><span class="sxs-lookup"><span data-stu-id="66f78-162">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="66f78-163">預設值為 StripAll</span><span class="sxs-lookup"><span data-stu-id="66f78-163">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f78-164">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="66f78-164">-RedirectProtocol</span></span>
<span data-ttu-id="66f78-165">要將流量重新導向至其中的目的地通訊協定。</span><span class="sxs-lookup"><span data-stu-id="66f78-165">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="66f78-166">預設值為 MatchRequest</span><span class="sxs-lookup"><span data-stu-id="66f78-166">Default value is MatchRequest</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectProtocol
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f78-167">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="66f78-167">-RedirectType</span></span>
<span data-ttu-id="66f78-168">當您重新導向流量時，規則將使用的重定向類型。</span><span class="sxs-lookup"><span data-stu-id="66f78-168">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="66f78-169">預設值會移動</span><span class="sxs-lookup"><span data-stu-id="66f78-169">Default Value is Moved</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectType
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: Moved, Found, TemporaryRedirect, PermanentRedirect

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f78-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66f78-170">-ResourceGroupName</span></span>
<span data-ttu-id="66f78-171">將在其中建立 RoutingRule 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="66f78-171">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="66f78-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f78-172">CommonParameters</span></span>
<span data-ttu-id="66f78-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66f78-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f78-174">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="66f78-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f78-175">輸入</span><span class="sxs-lookup"><span data-stu-id="66f78-175">INPUTS</span></span>

### <span data-ttu-id="66f78-176">所有</span><span class="sxs-lookup"><span data-stu-id="66f78-176">None</span></span>

## <span data-ttu-id="66f78-177">輸出</span><span class="sxs-lookup"><span data-stu-id="66f78-177">OUTPUTS</span></span>

### <span data-ttu-id="66f78-178">PSRoutingRule 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="66f78-178">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="66f78-179">筆記</span><span class="sxs-lookup"><span data-stu-id="66f78-179">NOTES</span></span>

## <span data-ttu-id="66f78-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="66f78-180">RELATED LINKS</span></span>

<span data-ttu-id="66f78-181">[新-AzFrontDoor](./New-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="66f78-181">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>