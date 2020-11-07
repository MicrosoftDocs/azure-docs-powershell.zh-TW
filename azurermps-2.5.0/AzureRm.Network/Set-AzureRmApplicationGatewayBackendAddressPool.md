---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 66ca482f2b284118ccf5095ec833a5278a5ea73d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802230"
---
# <span data-ttu-id="f9464-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f9464-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="f9464-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9464-102">SYNOPSIS</span></span>
<span data-ttu-id="f9464-103">更新應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="f9464-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9464-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9464-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9464-105">說明</span><span class="sxs-lookup"><span data-stu-id="f9464-105">DESCRIPTION</span></span>
<span data-ttu-id="f9464-106">**AzureRmApplicationGatewayBackendAddressPool** Cmdlet 會更新 Azure 應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="f9464-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="f9464-107">後端位址可以指定為 IP 位址、完全限定的功能變數名稱 (FQDN) 或 IP 配置 Id。</span><span class="sxs-lookup"><span data-stu-id="f9464-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="f9464-108">示例</span><span class="sxs-lookup"><span data-stu-id="f9464-108">EXAMPLES</span></span>

### <span data-ttu-id="f9464-109">範例1：使用 Fqdn 設定後端位址集區</span><span class="sxs-lookup"><span data-stu-id="f9464-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="f9464-110">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="f9464-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f9464-111">第二個命令會使用 Fqdn，在 $AppGw 中更新應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="f9464-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="f9464-112">範例2：使用後端伺服器 IP 位址設定後端位址集區</span><span class="sxs-lookup"><span data-stu-id="f9464-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="f9464-113">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="f9464-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f9464-114">第二個命令會在 $AppGw 中使用 IP 位址來更新應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="f9464-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="f9464-115">範例3：使用後端伺服器 IP 位址的識別碼設定後端位址集區</span><span class="sxs-lookup"><span data-stu-id="f9464-115">Example 3: Setting a back-end address pool by using the ID of the backend server?s IP address</span></span>
```
PS C:\> $Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="f9464-116">第一個命令會取得一個名為 Nic01 的網路介面物件，該物件屬於名為 ResourceGroup01 的資源群組，並儲存在 $Nic 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="f9464-116">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.</span></span>

<span data-ttu-id="f9464-117">第二個命令會取得一個名為 Nic02 的網路介面物件，該物件屬於名為 ResourceGroup02 的資源群組，並儲存在 $Nic 02 變數中。</span><span class="sxs-lookup"><span data-stu-id="f9464-117">The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.</span></span>

<span data-ttu-id="f9464-118">第三個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="f9464-118">The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f9464-119">第四個命令使用 $Nic 01 和 $Nic 02 的後端 IP 配置識別碼來更新 $AppGw 中應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="f9464-119">The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to update the back-end address pool of the application gateway in $AppGw.</span></span>

## <span data-ttu-id="f9464-120">參數</span><span class="sxs-lookup"><span data-stu-id="f9464-120">PARAMETERS</span></span>

### <span data-ttu-id="f9464-121">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9464-121">-ApplicationGateway</span></span>
<span data-ttu-id="f9464-122">指定此 Cmdlet 與後端位址集區關聯的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="f9464-122">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="f9464-123">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="f9464-123">-BackendFqdns</span></span>
<span data-ttu-id="f9464-124">指定要用來做為後端伺服器池的後端 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="f9464-124">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9464-125">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="f9464-125">-BackendIPAddresses</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9464-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9464-126">-DefaultProfile</span></span>
<span data-ttu-id="f9464-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9464-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9464-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9464-128">-Name</span></span>
<span data-ttu-id="f9464-129">指定後端位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9464-129">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="f9464-130">此後端位址集區必須存在於應用程式閘道中。</span><span class="sxs-lookup"><span data-stu-id="f9464-130">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="f9464-131">-確認</span><span class="sxs-lookup"><span data-stu-id="f9464-131">-Confirm</span></span>
<span data-ttu-id="f9464-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f9464-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9464-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9464-133">-WhatIf</span></span>
<span data-ttu-id="f9464-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9464-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9464-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9464-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9464-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9464-136">CommonParameters</span></span>
<span data-ttu-id="f9464-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9464-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9464-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f9464-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9464-139">輸入</span><span class="sxs-lookup"><span data-stu-id="f9464-139">INPUTS</span></span>

### <span data-ttu-id="f9464-140">System.object</span><span class="sxs-lookup"><span data-stu-id="f9464-140">System.String</span></span>

## <span data-ttu-id="f9464-141">輸出</span><span class="sxs-lookup"><span data-stu-id="f9464-141">OUTPUTS</span></span>

### <span data-ttu-id="f9464-142">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f9464-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f9464-143">筆記</span><span class="sxs-lookup"><span data-stu-id="f9464-143">NOTES</span></span>

## <span data-ttu-id="f9464-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9464-144">RELATED LINKS</span></span>

[<span data-ttu-id="f9464-145">附加 AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f9464-145">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f9464-146">AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f9464-146">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f9464-147">新-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f9464-147">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f9464-148">移除-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f9464-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

