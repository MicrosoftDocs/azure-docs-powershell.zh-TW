---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragefilecontent
schema: 2.0.0
ms.openlocfilehash: 74fbb0d5336eb5c3f9f34efb5724f8a86b8868ba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802634"
---
# Set-AzureStorageFileContent

## 摘要
上傳檔案的內容。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 共用名稱 (預設) 
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### 共用
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### 空目錄
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
**AzureStorageFileContent** Cmdlet 會將檔案的內容上傳到指定共用上的檔案。

## 示例

### 範例1：上傳目前資料夾中的檔案
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

這個命令會將目前資料夾中的名為 DataFile37 的檔案，上傳為名為 CurrentDataFile 的檔案，該檔案名為 [ContosoWorkingFolder] 資料夾。

### 範例2：上傳目前資料夾中的所有檔案
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

這個範例使用幾個常見的 Windows PowerShell Cmdlet 和目前的 Cmdlet，將目前資料夾中的所有檔案上傳到容器 ContosoShare06 的根資料夾。
第一個命令會取得目前資料夾的名稱，並將它儲存在 $CurrentFolder 變數中。
第二個命令使用 **AzureStorageShare** Cmdlet 來取得名為 ContosoShare06 的檔案共用，然後將它儲存在 $Container 變數中。
最後一個命令會透過使用管線運算子來取得目前資料夾的內容，並將每個專案傳遞給 Where-Object Cmdlet。
該 Cmdlet 會篩選掉不是檔案的物件，然後將檔案傳遞到 ForEach-Object Cmdlet。
該 Cmdlet 會針對針對其建立適當路徑的每個檔案執行腳本區塊，然後使用目前的 Cmdlet 來上傳檔案。
結果的名稱與此範例上傳之其他檔案的相對位置相同。
如需腳本區塊的詳細資訊，請輸入 `Get-Help about_Script_Blocks` 。

## 參數

### -ClientTimeoutPerRequest
指定一個服務要求的用戶端超時間隔（以秒為單位）。
如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。
如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。

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

### -ConcurrentTaskCount
指定最大併發網路通話數。
您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。
指定的值是絕對計數，不會乘以核心計數。
這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。
預設值為10。

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

### -內容
指定 Azure 儲存區內容。
若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -Directory
將資料夾指定為 **CloudFileDirectory** 物件。
這個 Cmdlet 會將檔案上傳到此參數指定的資料夾中。
若要取得目錄，請使用 New-AzureStorageDirectory Cmdlet。
您也可以使用 Get-AzureStorageFile Cmdlet 來取得目錄。

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
表示此 Cmdlet 會覆寫現有的 Azure 儲存空間檔案。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
表示此 Cmdlet 會傳回它所建立或上傳的 **AzureStorageFile** 物件。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
指定檔案或資料夾的路徑。
這個 Cmdlet 會將內容上傳到此參數指定的檔案，或傳給此參數指定之資料夾中的檔案。
如果您指定資料夾，這個 Cmdlet 會建立與來源檔案同名的檔案。
如果您指定不存在之檔案的路徑，這個 Cmdlet 會建立該檔案，並將內容儲存到該檔案。
如果您指定的檔案已經存在，而且您指定了 _Force_ 參數，這個 Cmdlet 會覆寫檔案的內容。
如果您指定的檔案已經存在，而您沒有指定 _Force_ ，這個 Cmdlet 不會變更，而且會傳回錯誤。
如果您指定的資料夾路徑不存在，這個 Cmdlet 不會變更，而且會傳回錯誤。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
指定要求中伺服器部分的超時時間長度。

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

### -共用
指定 **CloudFileShare** 物件。
這個 Cmdlet 會在檔案共用此參數指定的檔案上傳到檔案。
若要取得 **CloudFileShare** 物件，請使用 Get-AzureStorageShare Cmdlet。
此物件包含儲存內容。
如果您指定此參數，請勿指定 *CoNtext* 參數。

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -共用名稱
指定檔案共用的名稱。
這個 Cmdlet 會在檔案共用此參數指定的檔案上傳到檔案。

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -來源
指定此 Cmdlet 上傳的來源檔案。
如果您指定的檔案不存在，這個 Cmdlet 會傳回錯誤。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### [WindowsAzure] CloudFileShare
參數：共用 (ByValue) 

### [WindowsAzure] CloudFileDirectory
參數：目錄 (ByValue) 

### System.object

### IStorageCoNtext 中的 [Common.]

## 輸出

### [WindowsAzure] CloudFile

## 筆記

## 相關連結

[移除-AzureStorageDirectory](./Remove-AzureStorageDirectory.md)

[新-AzureStorageDirectory](./New-AzureStorageDirectory.md)

[AzureStorageFileContent](./Get-AzureStorageFileContent.md)
