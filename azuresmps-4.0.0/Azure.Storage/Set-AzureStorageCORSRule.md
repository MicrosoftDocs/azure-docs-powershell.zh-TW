---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: ''
schema: 2.0.0
ms.openlocfilehash: 635b8e1524f6123aa6ddde4ed7a64768d6c3d791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443556"
---
# Set-AzureStorageCORSRule

## 摘要
為一種類型的儲存服務設定 CORS 規則。

## 句法

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## 說明
**AzureStorageCORSRule** Cmdlet 會針對 Azure 儲存空間服務的類型，設定跨來源資源分享 (CORS) 規則。
此 Cmdlet 的儲存服務類型為 Blob、資料表、佇列和檔案。
這個 Cmdlet 會覆寫現有的規則。
若要查看目前的規則，請使用 Get-AzureStorageCORSRule Cmdlet。

## 示例

### 範例1：將 CORS 規則指派給 blob 服務
```
PS C:\>$CorsRules = (@{
    AllowedHeaders=@("x-ms-blob-content-type","x-ms-blob-content-disposition");
    AllowedOrigins=@("*");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Get","Connect")},
    @{
    AllowedOrigins=@("http://www.fabrikam.com","http://www.contoso.com"); 
    ExposedHeaders=@("x-ms-meta-data*","x-ms-meta-customheader"); 
    AllowedHeaders=@("x-ms-meta-target*","x-ms-meta-customheader");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Put")})
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

第一個命令會將一組規則指派給 $CorsRules 變數。
這個命令使用標準延伸到此程式碼塊中的數個行。

第二個命令會將 $CorsRules 中的規則指派給 Blob 服務類型。

### 範例2：變更 blob 服務的 CORS 規則屬性
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

第一個命令會使用 **AzureStorageCORSRule** Cmdlet 取得 Blob 類型的目前 CORS 規則。
該命令會將規則儲存在 $CorsRules 陣列變數中。

第二個和第三個命令會修改 $CorsRules 中的第一個規則。

Final 命令會將 $CorsRules 中的規則指派給 Blob 服務類型。
修改後的規則會覆寫目前的 CORS 規則。

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

### -內容
指定 Azure 儲存區內容。
若要取得內容，請使用 New-AzureStorageContext Cmdlet。

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

### -CorsRules
指定 CORS 規則的陣列。
您可以使用 Get-AzureStorageCORSRule Cmdlet 來檢索現有規則。

```yaml
Type: PSCorsRule[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
表示此 Cmdlet 會傳回反映操作成功的布林值。
根據預設，這個 Cmdlet 不會傳回值。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
指定要求中伺服器部分的超時時間長度。

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

### -ServiceType
指定此 Cmdlet 指派規則的 Azure 儲存空間服務類型。
此參數可接受的值為：

- Blob 
- 張 
- 序列 
- 檔案

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
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

[AzureStorageCORSRule](./Get-AzureStorageCORSRule.md)

[新-AzureStorageCoNtext](./New-AzureStorageContext.md)

[移除-AzureStorageCORSRule](./Remove-AzureStorageCORSRule.md)

