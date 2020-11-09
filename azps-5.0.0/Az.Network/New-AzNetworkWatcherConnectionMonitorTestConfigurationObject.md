---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: d46cba5a939a2054bc8cc40975647a198808ca09
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287452"
---
# <span data-ttu-id="286db-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="286db-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="286db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="286db-102">SYNOPSIS</span></span>
<span data-ttu-id="286db-103">建立連線監視測試組態。</span><span class="sxs-lookup"><span data-stu-id="286db-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="286db-104">句法</span><span class="sxs-lookup"><span data-stu-id="286db-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Double>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="286db-105">說明</span><span class="sxs-lookup"><span data-stu-id="286db-105">DESCRIPTION</span></span>
<span data-ttu-id="286db-106">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject Cmdlet 會建立連線監視器測試組態。</span><span class="sxs-lookup"><span data-stu-id="286db-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="286db-107">示例</span><span class="sxs-lookup"><span data-stu-id="286db-107">EXAMPLES</span></span>

### <span data-ttu-id="286db-108">範例1</span><span class="sxs-lookup"><span data-stu-id="286db-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="286db-109">Name （名稱）： HTTPTC TestFrequencySec： 120 PreferredIPVersion： ProtocolConfiguration： {"Port"：443，"方法"： "取得"，"RequestHeaders"： [{"Name"： "Allow"，"ValidStatusCodeRanges"： ["，" 300-308 "]，" PreferHTTPS "： true} SuccessThreshold： {" ChecksFailedPercent "：20，" RoundTripTimeMs "： 30}</span><span class="sxs-lookup"><span data-stu-id="286db-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="286db-110">參數</span><span class="sxs-lookup"><span data-stu-id="286db-110">PARAMETERS</span></span>

### <span data-ttu-id="286db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="286db-111">-DefaultProfile</span></span>
<span data-ttu-id="286db-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="286db-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="286db-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="286db-113">-Name</span></span>
<span data-ttu-id="286db-114">連線監視測試組態的名稱。</span><span class="sxs-lookup"><span data-stu-id="286db-114">The name of the connection monitor test configuration.</span></span>

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

### <span data-ttu-id="286db-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="286db-115">-PreferredIPVersion</span></span>
<span data-ttu-id="286db-116">要在測試評估中使用的首選 IP 版本。</span><span class="sxs-lookup"><span data-stu-id="286db-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="286db-117">根據其他參數，連接監視器可能會選擇使用不同的版本。</span><span class="sxs-lookup"><span data-stu-id="286db-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286db-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="286db-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="286db-119">用來對某個通訊協定執行測試評估的參數。</span><span class="sxs-lookup"><span data-stu-id="286db-119">The parameters used to perform test evaluation over some protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286db-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="286db-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="286db-121">測試在成功評估時所允許的失敗檢查的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="286db-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286db-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="286db-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="286db-123">測試可評估為成功的最大往返時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="286db-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286db-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="286db-124">-TestFrequencySec</span></span>
<span data-ttu-id="286db-125">測試評估的頻率（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="286db-125">The frequency of test evaluation, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: TestFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286db-126">-確認</span><span class="sxs-lookup"><span data-stu-id="286db-126">-Confirm</span></span>
<span data-ttu-id="286db-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="286db-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="286db-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="286db-128">-WhatIf</span></span>
<span data-ttu-id="286db-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="286db-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="286db-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="286db-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="286db-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286db-131">CommonParameters</span></span>
<span data-ttu-id="286db-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="286db-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286db-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="286db-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286db-134">輸入</span><span class="sxs-lookup"><span data-stu-id="286db-134">INPUTS</span></span>

### <span data-ttu-id="286db-135">所有</span><span class="sxs-lookup"><span data-stu-id="286db-135">None</span></span>

## <span data-ttu-id="286db-136">輸出</span><span class="sxs-lookup"><span data-stu-id="286db-136">OUTPUTS</span></span>

### <span data-ttu-id="286db-137">PSNetworkWatcherConnectionMonitorTestConfigurationObject 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="286db-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="286db-138">筆記</span><span class="sxs-lookup"><span data-stu-id="286db-138">NOTES</span></span>

## <span data-ttu-id="286db-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="286db-139">RELATED LINKS</span></span>