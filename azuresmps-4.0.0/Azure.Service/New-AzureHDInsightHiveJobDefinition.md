---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0DFCB891-7431-4C00-98DD-263DC2794354
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea6fbc76a76533c07b11935e50e25418d10e38ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967363"
---
# New-AzureHDInsightHiveJobDefinition

## 摘要
為 HDInsight 服務定義新的配置單元作業。

## 句法

```
New-AzureHDInsightHiveJobDefinition [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
此版本的 Azure PowerShell HDInsight 已被否決。
這些 Cmdlet 將會在2017年1月1日移除。
請使用較新版本的 Azure PowerShell HDInsight。

如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。
如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。
如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。

**新的-AzureHDInsightHiveJobDefinition** Cmdlet 會定義 Azure HDInsight 服務的 Hive 作業。

## 示例

### 範例1：建立蜂巢作業定義
```
PS C:\>$HiveJobDefinition = New-AzureHDInsightHiveJobDefinition -Query $QueryString
```

這個命令會建立一個使用預先定義的查詢字串的 Hive 作業定義，然後將它儲存在 $HiveJobDefinition 變數中。

## 參數

### -引數
指定 Hadoop 作業的引數陣列。
引數會以命令列引數的形式傳遞給每個任務。

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -定義
指定要在作業執行時設定的 Hadoop 配置值。

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 檔案
指定包含要執行之查詢之檔案的路徑。
您可以使用這個參數，而不是 *Query* 參數。

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -檔案
指定與 Hive 作業相關聯的檔案集合。

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
指定要定義的 Hive 作業名稱。
如果您沒有指定此參數，則會使用預設名稱：「Hive：」 \<first 100 characters of query\> 。

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Query
指定 Hive 查詢。

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryText

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunAsFileJob
指示這個 Cmdlet 會在預設的 Azure 儲存空間帳戶中建立檔案，以儲存查詢。
這個 Cmdlet 會提交參照此檔案做為腳本以執行的工作。

您可以使用這個功能來處理特殊的字元，例如百分號 (% ) ，這些字元會在透過 Templeton 提交作業時失敗，因為 Templeton 會使用百分號符號作為 URL 參數來轉譯查詢。

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

### -StatusFolder
指定包含作業之標準輸出和錯誤輸出的資料夾位置，包括其結束代碼和任務記錄。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[新-AzureHDInsightMapReduceJobDefinition](./New-AzureHDInsightMapReduceJobDefinition.md)

[新-AzureHDInsightPigJobDefinition](./New-AzureHDInsightPigJobDefinition.md)

[新-AzureHDInsightSqoopJobDefinition](./New-AzureHDInsightSqoopJobDefinition.md)

[新-AzureHDInsightStreamingMapReduceJobDefinition](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


