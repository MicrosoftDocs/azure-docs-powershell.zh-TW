---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 007fb7a309b9dd305f58d2f947d3d2dfc55078e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614344"
---
# New-AzTrafficManagerEndpoint

## 摘要
在流量管理器設定檔中建立端點。

## 句法

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**新的 AzTrafficManagerEndpoint** Cmdlet 會在 Azure 流量管理器設定檔中建立端點。

這個 Cmdlet 會將每個新端點提交至流量管理器服務。
若要在本機流量管理器設定檔物件中新增多個端點，並在單一作業中提交變更，請使用 Add-AzTrafficManagerEndpointConfig Cmdlet。

## 示例

### 範例1：建立設定檔的外部端點
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

這個命令會在名為 ResourceGroup11 的資源群組中，在名為 ContosoProfile 的設定檔中建立名為 contoso 的外部端點。

### 範例2：建立設定檔的 Azure 端點
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

這個命令會在資源群組 ResouceGroup11 中，在名為 ContosoProfile 的設定檔中建立名為 contoso 的 Azure 端點。
Azure 端點指向 azure Web 應用程式，其 Azure 資源管理器 ID 是由 *TargetResourceId* 中的 URI 路徑所提供。
因為 Web App 資源提供位置，所以命令不會指定 *EndpointLocation* 參數。

## 參數

### -CustomHeader
針對探測要求的自訂標頭名稱和值對清單。

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

### -EndpointLocation
指定要在效能流量路由方法中使用的端點位置。
這個參數只適用于 ExternalEndpoints 或 NestedEndpoints 類型的端點。
使用效能流量路由方法時，您必須指定此參數。

指定 Azure 地區名稱。
如需 Azure 區域的完整清單，請參閱 Azure 地區 https://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/) 。

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

### -EndpointStatus
指定端點的狀態。
有效值為： 

- 後 
- 禁止 

如果狀態為 [已啟用]，則會針對端點健康情況探測端點，並包含在流量路由方法中。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GeoMapping
使用 ' 地理 ' 流量路由方法時，對應到此端點的地區清單。 如需可接受值的完整清單，請參閱流量管理器檔。

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

### -MinChildEndpoints
指定 Azure 地區名稱。
如需 Azure 區域的完整清單，請參閱 Azure 地區 https://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/) 。

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 建立之流量管理器端點的名稱。

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

### -優先順序
指定流量管理器指派給端點的優先順序。
只有在流量管理器設定檔是以優先順序流量路由方法設定的情況下，才能使用這個參數。
有效的值是從1到1000的整數。
較低的值代表較高的優先順序。

如果您指定優先順序，您必須在設定檔中的所有端點上指定優先順序，而且任何兩個端點都不能共用相同的優先順序值。
如果您沒有指定優先順序，流量主管會將預設的優先順序值指派給端點，並從一個 (1) 開始，並依照設定檔列出端點的順序進行。

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProfileName
指定此 Cmdlet 新增端點的流量管理器設定檔名稱。
若要取得設定檔，請使用 New-AzTrafficManagerProfile 或 Get-AzTrafficManagerProfile Cmdlet。

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

### -ResourceGroupName
指定資源群組的名稱。
這個 Cmdlet 會在此參數指定的群組中建立流量管理器端點。

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

### -SubnetMapping
使用 [™̃Subnetâ] 流量路由方法時，對應至此端點的位址範圍或子網清單。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -目標
指定端點的完整 DNS 名稱。
當流量主管將流量導向到此端點時，會在 DNS 回應中傳回這個值。
請僅針對 ExternalEndpoints 端點類型指定此參數。
針對其他端點類型，請改為指定 *TargetResourceId* 參數。

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

### -TargetResourceId
指定目標的資源識別碼。
僅針對 AzureEndpoints 和 NestedEndpoints 端點類型指定此參數。
針對 ExternalEndpoints 端點類型，請改為指定 *目標* 參數。

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

### -類型
指定此 Cmdlet 新增至流量管理器設定檔的端點類型。
有效值為： 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 寬度
指定流量主管指派給端點的權重。
有效的值是從1到1000的整數。
預設值是一個 (1) 。
只有在流量管理器設定檔是使用加權流量路由方法設定的情況下，才能使用這個參數。

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### TrafficManagerEndpoint 中的 TrafficManager。

## 筆記

## 相關連結

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[新-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[移除-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)

