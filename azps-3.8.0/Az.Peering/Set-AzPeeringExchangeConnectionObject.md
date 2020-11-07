---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: c09ff4ad7762eafc18d7890f9611c9b989841c95
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797982"
---
# <span data-ttu-id="b9a89-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b9a89-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="b9a89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9a89-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a89-103">設定或更新 Exchange 連線資訊。</span><span class="sxs-lookup"><span data-stu-id="b9a89-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="b9a89-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9a89-104">SYNTAX</span></span>

### <span data-ttu-id="b9a89-105">IPv6Address (預設) </span><span class="sxs-lookup"><span data-stu-id="b9a89-105">IPv6Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9a89-106">IPv4Address</span><span class="sxs-lookup"><span data-stu-id="b9a89-106">IPv4Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9a89-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="b9a89-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9a89-108">說明</span><span class="sxs-lookup"><span data-stu-id="b9a89-108">DESCRIPTION</span></span>
<span data-ttu-id="b9a89-109">與更新 AzPeering 搭配使用，這是記憶體中的作業，只會持續保持 `Update-AzPeering` 。</span><span class="sxs-lookup"><span data-stu-id="b9a89-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="b9a89-110">示例</span><span class="sxs-lookup"><span data-stu-id="b9a89-110">EXAMPLES</span></span>

### <span data-ttu-id="b9a89-111">更新 Md5 雜湊</span><span class="sxs-lookup"><span data-stu-id="b9a89-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="b9a89-112">在記憶體中，更新對等物件中第一個連接的 Md5 雜湊。</span><span class="sxs-lookup"><span data-stu-id="b9a89-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="b9a89-113">更新 Bgp 會話位址</span><span class="sxs-lookup"><span data-stu-id="b9a89-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="b9a89-114">更新記憶體中對等物件的第一個連接的對等位址。</span><span class="sxs-lookup"><span data-stu-id="b9a89-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="b9a89-115">參數</span><span class="sxs-lookup"><span data-stu-id="b9a89-115">PARAMETERS</span></span>

### <span data-ttu-id="b9a89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a89-116">-DefaultProfile</span></span>
<span data-ttu-id="b9a89-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9a89-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9a89-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9a89-118">-InputObject</span></span>
<span data-ttu-id="b9a89-119">Exchange 連線物件</span><span class="sxs-lookup"><span data-stu-id="b9a89-119">The exchange connection object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9a89-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="b9a89-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="b9a89-121">播發的最大 IPv4</span><span class="sxs-lookup"><span data-stu-id="b9a89-121">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a89-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="b9a89-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="b9a89-123">播發的最大 IPv6</span><span class="sxs-lookup"><span data-stu-id="b9a89-123">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a89-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="b9a89-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="b9a89-125">[會話] 的 [MD5 驗證金鑰]。</span><span class="sxs-lookup"><span data-stu-id="b9a89-125">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: Md5Authentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a89-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="b9a89-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="b9a89-127">點對點工作階段 IPv4 位址</span><span class="sxs-lookup"><span data-stu-id="b9a89-127">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a89-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="b9a89-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="b9a89-129">點對點工作階段 IPv6 位址</span><span class="sxs-lookup"><span data-stu-id="b9a89-129">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a89-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a89-130">CommonParameters</span></span>
<span data-ttu-id="b9a89-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9a89-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a89-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b9a89-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a89-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b9a89-133">INPUTS</span></span>

### <span data-ttu-id="b9a89-134">PSExchangeConnection 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="b9a89-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="b9a89-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b9a89-135">OUTPUTS</span></span>

### <span data-ttu-id="b9a89-136">PSExchangeConnection 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="b9a89-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="b9a89-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b9a89-137">NOTES</span></span>

## <span data-ttu-id="b9a89-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9a89-138">RELATED LINKS</span></span>