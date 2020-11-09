---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285867"
---
# <span data-ttu-id="d5c32-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="d5c32-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="d5c32-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5c32-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c32-103">建立傳遞動作。</span><span class="sxs-lookup"><span data-stu-id="d5c32-103">Creates a delivery action.</span></span>

## <span data-ttu-id="d5c32-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5c32-104">SYNTAX</span></span>

### <span data-ttu-id="d5c32-105">CacheExpirationActionParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d5c32-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5c32-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5c32-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5c32-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5c32-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5c32-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5c32-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5c32-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5c32-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5c32-110">說明</span><span class="sxs-lookup"><span data-stu-id="d5c32-110">DESCRIPTION</span></span>
<span data-ttu-id="d5c32-111">**新的-AzCdnDeliveryRule** Cmdlet 會建立 CDN 端點建立的傳遞規則。</span><span class="sxs-lookup"><span data-stu-id="d5c32-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="d5c32-112">示例</span><span class="sxs-lookup"><span data-stu-id="d5c32-112">EXAMPLES</span></span>

### <span data-ttu-id="d5c32-113">範例1</span><span class="sxs-lookup"><span data-stu-id="d5c32-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="d5c32-114">建立簡單的傳遞規則。</span><span class="sxs-lookup"><span data-stu-id="d5c32-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="d5c32-115">參數</span><span class="sxs-lookup"><span data-stu-id="d5c32-115">PARAMETERS</span></span>

### <span data-ttu-id="d5c32-116">-動作</span><span class="sxs-lookup"><span data-stu-id="d5c32-116">-Action</span></span>
<span data-ttu-id="d5c32-117">要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="d5c32-117">Action to perform.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="d5c32-118">-CacheBehavior</span></span>
<span data-ttu-id="d5c32-119">動作的快取行為</span><span class="sxs-lookup"><span data-stu-id="d5c32-119">Caching behavior for the action</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="d5c32-120">-CacheDuration</span></span>
<span data-ttu-id="d5c32-121">內容需要緩存的持續時間。</span><span class="sxs-lookup"><span data-stu-id="d5c32-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="d5c32-122">允許的格式為 \[ d。 \]hh： mm： ss</span><span class="sxs-lookup"><span data-stu-id="d5c32-122">Allowed format is \[d.\]hh:mm:ss</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="d5c32-123">-CustomFragment</span></span>
<span data-ttu-id="d5c32-124">要新增至重新導向 URL 的片段。</span><span class="sxs-lookup"><span data-stu-id="d5c32-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="d5c32-125">[片段] 是位於 # 之後的 URL 部分。</span><span class="sxs-lookup"><span data-stu-id="d5c32-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="d5c32-126">請勿包含 #。</span><span class="sxs-lookup"><span data-stu-id="d5c32-126">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="d5c32-127">-CustomHostname</span></span>
<span data-ttu-id="d5c32-128">要重新導向的主機。</span><span class="sxs-lookup"><span data-stu-id="d5c32-128">Host to redirect.</span></span>
<span data-ttu-id="d5c32-129">[留空] 可將傳入主機做為目的地主機。</span><span class="sxs-lookup"><span data-stu-id="d5c32-129">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="d5c32-130">-CustomPath</span></span>
<span data-ttu-id="d5c32-131">要重新導向的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="d5c32-131">The full path to redirect.</span></span>
<span data-ttu-id="d5c32-132">Path 不能為空白，且必須以/開頭。</span><span class="sxs-lookup"><span data-stu-id="d5c32-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="d5c32-133">[留空] 可使用傳入路徑做為目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="d5c32-133">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="d5c32-134">-CustomQueryString</span></span>
<span data-ttu-id="d5c32-135">要放在重新導向 URL 中的一組查詢字串。</span><span class="sxs-lookup"><span data-stu-id="d5c32-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="d5c32-136">設定此值會取代任何現有的查詢字串;保留空白以保留傳入查詢字串。</span><span class="sxs-lookup"><span data-stu-id="d5c32-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="d5c32-137">查詢字串必須是 \<key\> = \<value\> 格式。</span><span class="sxs-lookup"><span data-stu-id="d5c32-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="d5c32-138">?</span><span class="sxs-lookup"><span data-stu-id="d5c32-138">?</span></span> <span data-ttu-id="d5c32-139">而且 & 將會自動新增，因此不包含它們。</span><span class="sxs-lookup"><span data-stu-id="d5c32-139">and & will be added automatically so do not include them.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c32-140">-DefaultProfile</span></span>
<span data-ttu-id="d5c32-141">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d5c32-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5c32-142">-目的地</span><span class="sxs-lookup"><span data-stu-id="d5c32-142">-Destination</span></span>
<span data-ttu-id="d5c32-143">定義上述要求將會重新寫入的相對 URL。</span><span class="sxs-lookup"><span data-stu-id="d5c32-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="d5c32-144">-DestinationProtocol</span></span>
<span data-ttu-id="d5c32-145">要用於重新導向的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d5c32-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="d5c32-146">預設值為 MatchRequest。</span><span class="sxs-lookup"><span data-stu-id="d5c32-146">The default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="d5c32-147">-HeaderActionType</span></span>
<span data-ttu-id="d5c32-148">是否修改要求標頭或回應標頭</span><span class="sxs-lookup"><span data-stu-id="d5c32-148">Whether to modify request header or response header</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="d5c32-149">-HeaderName</span></span>
<span data-ttu-id="d5c32-150">要修改之標頭的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5c32-150">Name of the header to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="d5c32-151">-PreservePath</span></span>
<span data-ttu-id="d5c32-152">是否保留不成對的路徑。</span><span class="sxs-lookup"><span data-stu-id="d5c32-152">Whether to preserve unmatched path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="d5c32-153">-QueryParameter</span></span>
<span data-ttu-id="d5c32-154">包含或排除 (逗號分隔) 的查詢參數。</span><span class="sxs-lookup"><span data-stu-id="d5c32-154">Query parameters to include or exclude (comma separated).</span></span>

```yaml
Type: System.String[]
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="d5c32-155">-QueryStringBehavior</span></span>
<span data-ttu-id="d5c32-156">要求的 QueryString 行為</span><span class="sxs-lookup"><span data-stu-id="d5c32-156">QueryString behavior for the requests</span></span>

```yaml
Type: System.String
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="d5c32-157">-RedirectType</span></span>
<span data-ttu-id="d5c32-158">當您重新導向流量時，規則將使用的重定向類型</span><span class="sxs-lookup"><span data-stu-id="d5c32-158">The redirect type the rule will use when redirecting traffic</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="d5c32-159">-SourcePattern</span></span>
<span data-ttu-id="d5c32-160">定義標識可能要重新寫入之要求類型的要求 URI 模式。</span><span class="sxs-lookup"><span data-stu-id="d5c32-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="d5c32-161">如果 value 為空白，則會與所有字串相符。</span><span class="sxs-lookup"><span data-stu-id="d5c32-161">If value is blank, all strings are matched.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-162">-值</span><span class="sxs-lookup"><span data-stu-id="d5c32-162">-Value</span></span>
<span data-ttu-id="d5c32-163">指定動作的值。</span><span class="sxs-lookup"><span data-stu-id="d5c32-163">Value for the specified action.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c32-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c32-164">CommonParameters</span></span>
<span data-ttu-id="d5c32-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5c32-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c32-166">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d5c32-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c32-167">輸入</span><span class="sxs-lookup"><span data-stu-id="d5c32-167">INPUTS</span></span>

### <span data-ttu-id="d5c32-168">所有</span><span class="sxs-lookup"><span data-stu-id="d5c32-168">None</span></span>

## <span data-ttu-id="d5c32-169">輸出</span><span class="sxs-lookup"><span data-stu-id="d5c32-169">OUTPUTS</span></span>

### <span data-ttu-id="d5c32-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="d5c32-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="d5c32-171">筆記</span><span class="sxs-lookup"><span data-stu-id="d5c32-171">NOTES</span></span>

## <span data-ttu-id="d5c32-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5c32-172">RELATED LINKS</span></span>