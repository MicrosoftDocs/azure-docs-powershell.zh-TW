---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95d5afafbed6ab6e3ba81cbfd509fd7b531217e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623254"
---
# New-AzureStorageContainerStoredAccessPolicy

## 摘要
建立 Azure 儲存空間容器的儲存存取原則。

## 句法

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## 說明
**新的-AzureStorageContainerStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間容器建立儲存的存取原則。

## 示例

### 範例1：在儲存空間容器中建立儲存的存取原則
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

這個命令會在名為 MyContainer 的存儲容器中建立名為 Policy01 的訪問原則。

## 參數

### -ClientTimeoutPerRequest
指定一個服務要求的用戶端超時間隔（以秒為單位）。
如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。
如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
指定最大併發網路通話數。
您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。
指定的值是絕對計數，不會乘以核心計數。
這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。
預設值為10。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -容器
指定 Azure 儲存空間容器名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -內容
指定 Azure 儲存區內容。
若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ExpiryTime
指定儲存的存取原則失效的時間。

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -許可權
指定此容器的公開存取層級。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -原則
指定儲存的存取原則，包括此 SAS 權杖的許可權。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
指定一個服務要求的用戶端超時間隔（以秒為單位）。
如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。
如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
指定儲存的存取原則生效的時間。

```yaml
Type: DateTime
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

## 輸出

## 筆記

## 相關連結

[AzureStorageContainerStoredAccessPolicy](./Get-AzureStorageContainerStoredAccessPolicy.md)

[新-AzureStorageCoNtext](./New-AzureStorageContext.md)

[移除-AzureStorageContainerStoredAccessPolicy](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[Set-AzureStorageContainerStoredAccessPolicy](./Set-AzureStorageContainerStoredAccessPolicy.md)


