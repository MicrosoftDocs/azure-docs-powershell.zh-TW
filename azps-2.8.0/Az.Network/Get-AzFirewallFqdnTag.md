---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 28a7fa45c8c6dc291f5e0c2a54c9fcf5fb5242dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790118"
---
# Get-AzFirewallFqdnTag

## 摘要
取得可用的 Azure 防火牆 Fqdn 標記。

## 句法

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzFirewallFqdnTag** Cmdlet 會取得可用於 Azure 防火牆應用程式規則的 FQDN 標記清單

## 示例

### 1：檢索所有可用的 FQDN 標記
```
Get-AzFirewallFqdnTag
```

這個範例會檢索所有可用的 FQDN 標記。

### 2：在應用程式規則中使用第一個可用的 FQDN 標記
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

這個範例會使用第一個可用的 FQDN 標記來建立防火牆應用程式規則

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### 所有

## 輸出

### PSAzureFirewallFqdnTag 中的 [.]

### System.object. IEnumerable ' 1 [PSAzureFirewallFqdnTag，#..... Network，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））

## 筆記

## 相關連結

[新-AzFirewallApplicationRule](./New-AzFirewallApplicationRule.md)

[新-AzFirewall](./New-AzFirewall.md)
