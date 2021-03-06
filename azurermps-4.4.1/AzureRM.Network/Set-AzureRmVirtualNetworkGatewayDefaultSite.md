---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 4ab32ab5830356740cdb1709799b7dcb8f811c90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448094"
---
# Set-AzureRmVirtualNetworkGatewayDefaultSite

## 摘要
設定虛擬網路閘道的預設網站。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmVirtualNetworkGatewayDefaultSite** Cmdlet 會將強制隧道預設網站指派給虛擬網路閘道。
強制隧道提供一種將網際網路系結流量從 Azure 虛擬機器重新導向到您的內部部署網路的方式;這可讓您在釋放流量前先檢查並進行審核。
強制隧道是使用虛擬私人網路絡 (VPN) 隧道來執行;這個隧道需要一個預設的網站，即會重新導向所有 Azure 網際網路系結流量的本機閘道。
**Set-AzureRmVirtualNetworkGatewayDefaultSite** 提供一種變更指派給閘道之預設網站的方法。

## 示例

### 範例1：指派預設網站至虛擬網路閘道
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

這個範例會將預設網站指派給名為 ContosoVirtualGateway 的虛擬網路閘道。

第一個命令會建立名為 ContosoLocalGateway 的本機閘道的物件參考。
儲存在名為 $LocalGateway 的變數中的物件參照代表要設定為預設網站的閘道

.
然後，第二個命令會建立虛擬網路閘道的物件參照，並將結果儲存在名為 $VirtualGateway 的變數中。

第三個命令使用 **AzureRmVirtualNetworkGatewayDefaultSite** Cmdlet 將預設的網站指派給 ContosoVirtualGateway。

## 參數

### -GatewayDefaultSite
指定要指派為指定虛擬網路預設網站之本機網路閘道的物件參考。
您可以使用 Get-AzureRmLocalNetworkGateway Cmdlet 來建立本機閘道的物件參考。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
指定將指派預設網站之虛擬網路閘道的物件參照。
您可以使用 **AzureRmVirtualNetworkGateway** ，並指定閘道的名稱，來建立虛擬閘道的物件參考。

變數 $VirtualGateway 可以用來做為 *VirtualNetworkGateway* 參數的參數值：

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

###  
這個 Cmdlet 會接受 PSVirtualNetworkGateway 物件的流水線實例（ **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** 物件）。

## 輸出

###  
這個 Cmdlet 會修改 PSVirtualNetworkGateway 物件的現有實例（ **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** 物件）。

## 筆記

## 相關連結

[AzureRmLocalNetworkGateway](./Get-AzureRmLocalNetworkGateway.md)

[AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[移除-AzureRmVirtualNetworkGatewayDefaultSite](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)


