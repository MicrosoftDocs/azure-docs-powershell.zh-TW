---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
ms.openlocfilehash: c5e1f69e8a11f09e4f7b838c5e489c8a240d40e6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275384"
---
# <span data-ttu-id="3f9e0-101">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f9e0-101">New-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="3f9e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f9e0-102">SYNOPSIS</span></span>
<span data-ttu-id="3f9e0-103">建立流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="3f9e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f9e0-104">SYNTAX</span></span>

```
New-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f9e0-105">說明</span><span class="sxs-lookup"><span data-stu-id="3f9e0-105">DESCRIPTION</span></span>
<span data-ttu-id="3f9e0-106">**新的-AzTrafficManagerProfile** Cmdlet 會建立 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-106">The **New-AzTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="3f9e0-107">指定 *Name* 參數及必要的設定。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="3f9e0-108">這個 Cmdlet 會傳回代表新設定檔的本機物件。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="3f9e0-109">這個 Cmdlet 不會設定流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="3f9e0-110">您可以使用 Add-AzTrafficManagerEndpointConfig Cmdlet 來更新本機設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-110">You can update the local profile object by using the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="3f9e0-111">然後使用 Set-AzTrafficManagerProfile Cmdlet 將變更上傳到流量管理器。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-111">Then upload changes to Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="3f9e0-112">或者，您也可以使用 New-AzTrafficManagerEndpoint Cmdlet 來新增端點。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-112">Alternatively, you can add endpoints by using the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="3f9e0-113">示例</span><span class="sxs-lookup"><span data-stu-id="3f9e0-113">EXAMPLES</span></span>

### <span data-ttu-id="3f9e0-114">範例1：建立設定檔</span><span class="sxs-lookup"><span data-stu-id="3f9e0-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="3f9e0-115">這個命令會在資源群組 ResourceGroup11 中建立名為 ContosoProfile 的 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="3f9e0-116">DNS FQDN 是 contosoapp.trafficmanager.net。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="3f9e0-117">參數</span><span class="sxs-lookup"><span data-stu-id="3f9e0-117">PARAMETERS</span></span>

### <span data-ttu-id="3f9e0-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="3f9e0-118">-CustomHeader</span></span>
<span data-ttu-id="3f9e0-119">針對探測要求的自訂標頭名稱和值對清單。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-119">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f9e0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f9e0-120">-DefaultProfile</span></span>
<span data-ttu-id="3f9e0-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f9e0-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="3f9e0-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="3f9e0-123">探測要求的預期 HTTP 狀態碼範圍清單。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-123">List of expected HTTP status code ranges for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f9e0-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="3f9e0-124">-MaxReturn</span></span>
<span data-ttu-id="3f9e0-125">針對具有多值路由方法之設定檔所傳回的最大答卷數。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f9e0-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="3f9e0-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="3f9e0-127">間隔 (以秒為單位) 流量管理員將在此設定檔中檢查每個端點的健康情況。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="3f9e0-128">預設值為30。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-128">The default is 30.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f9e0-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="3f9e0-129">-MonitorPath</span></span>
<span data-ttu-id="3f9e0-130">指定用來監視端點健康情況的路徑。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="3f9e0-131">指定相對於端點網功能變數名稱稱的值。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="3f9e0-132">此值必須以斜線 (/) 開頭。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-132">This value must begin with a slash (/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f9e0-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="3f9e0-133">-MonitorPort</span></span>
<span data-ttu-id="3f9e0-134">指定用來監視端點健康情況的 TCP 埠。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="3f9e0-135">有效的值是從1到65535的整數。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-135">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f9e0-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="3f9e0-136">-MonitorProtocol</span></span>
<span data-ttu-id="3f9e0-137">指定用來監視端點健康情況的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="3f9e0-138">有效值為：</span><span class="sxs-lookup"><span data-stu-id="3f9e0-138">Valid values are:</span></span>

- <span data-ttu-id="3f9e0-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="3f9e0-139">HTTP</span></span>
- <span data-ttu-id="3f9e0-140">IP-HTTPS</span><span class="sxs-lookup"><span data-stu-id="3f9e0-140">HTTPS</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f9e0-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="3f9e0-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="3f9e0-142">流量管理器允許此設定檔中的端點回應健康情況檢查的時間 (以秒為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="3f9e0-143">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-143">The default is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f9e0-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="3f9e0-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="3f9e0-145">在此設定檔中宣告端點前，在下一個連續失敗狀況檢查已降級之後，通信量 Manager tolerates 的連續失敗狀況檢查次數。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="3f9e0-146">預設值為3。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-146">The default is 3.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f9e0-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="3f9e0-147">-Name</span></span>
<span data-ttu-id="3f9e0-148">指定此 Cmdlet 所建立之流量管理器設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3f9e0-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="3f9e0-149">-ProfileStatus</span></span>
<span data-ttu-id="3f9e0-150">指定設定檔的狀態。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="3f9e0-151">有效值為： Enabled 和 Disabled。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-151">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f9e0-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="3f9e0-152">-RelativeDnsName</span></span>
<span data-ttu-id="3f9e0-153">指定此流量管理器設定檔所提供的相對 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="3f9e0-154">流量管理器結合此值與 DNS 功能變數名稱，而 Azure 流量 Manager 會使用該名稱來構成設定檔的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="3f9e0-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f9e0-155">-ResourceGroupName</span></span>
<span data-ttu-id="3f9e0-156">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3f9e0-157">這個 Cmdlet 會在此參數指定的群組中建立流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3f9e0-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="3f9e0-158">-Tag</span></span>
<span data-ttu-id="3f9e0-159">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="3f9e0-160">例如：</span><span class="sxs-lookup"><span data-stu-id="3f9e0-160">For example:</span></span>

<span data-ttu-id="3f9e0-161">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3f9e0-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f9e0-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="3f9e0-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="3f9e0-163">指定流量路由方法。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="3f9e0-164">這個方法會判斷哪個端點流量主管會傳回，以回應傳入的 DNS 查詢。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="3f9e0-165">有效值為：</span><span class="sxs-lookup"><span data-stu-id="3f9e0-165">Valid values are:</span></span>

- <span data-ttu-id="3f9e0-166">提高</span><span class="sxs-lookup"><span data-stu-id="3f9e0-166">Performance</span></span>
- <span data-ttu-id="3f9e0-167">加</span><span class="sxs-lookup"><span data-stu-id="3f9e0-167">Weighted</span></span>
- <span data-ttu-id="3f9e0-168">優先順序</span><span class="sxs-lookup"><span data-stu-id="3f9e0-168">Priority</span></span>
- <span data-ttu-id="3f9e0-169">位置</span><span class="sxs-lookup"><span data-stu-id="3f9e0-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic, Subnet, MultiValue

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f9e0-170">-Ttl</span><span class="sxs-lookup"><span data-stu-id="3f9e0-170">-Ttl</span></span>
<span data-ttu-id="3f9e0-171">指定 (TTL) 值的 DNS 時間。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-171">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f9e0-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f9e0-172">CommonParameters</span></span>
<span data-ttu-id="3f9e0-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f9e0-174">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f9e0-175">輸入</span><span class="sxs-lookup"><span data-stu-id="3f9e0-175">INPUTS</span></span>

### <span data-ttu-id="3f9e0-176">所有</span><span class="sxs-lookup"><span data-stu-id="3f9e0-176">None</span></span>

## <span data-ttu-id="3f9e0-177">輸出</span><span class="sxs-lookup"><span data-stu-id="3f9e0-177">OUTPUTS</span></span>

### <span data-ttu-id="3f9e0-178">TrafficManagerProfile 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="3f9e0-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="3f9e0-179">筆記</span><span class="sxs-lookup"><span data-stu-id="3f9e0-179">NOTES</span></span>

## <span data-ttu-id="3f9e0-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f9e0-180">RELATED LINKS</span></span>

[<span data-ttu-id="3f9e0-181">附加 AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="3f9e0-181">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="3f9e0-182">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f9e0-182">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="3f9e0-183">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f9e0-183">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="3f9e0-184">AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f9e0-184">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="3f9e0-185">移除-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f9e0-185">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="3f9e0-186">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f9e0-186">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

