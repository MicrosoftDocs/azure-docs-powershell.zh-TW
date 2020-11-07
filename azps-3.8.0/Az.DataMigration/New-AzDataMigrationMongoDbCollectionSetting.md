---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796997"
---
# <span data-ttu-id="80514-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="80514-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="80514-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80514-102">SYNOPSIS</span></span>
<span data-ttu-id="80514-103">根據 mongoDb 遷移建立要遷移的集合設定</span><span class="sxs-lookup"><span data-stu-id="80514-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="80514-104">句法</span><span class="sxs-lookup"><span data-stu-id="80514-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="80514-105">說明</span><span class="sxs-lookup"><span data-stu-id="80514-105">DESCRIPTION</span></span>
<span data-ttu-id="80514-106">New-AzDataMigrationMongoDbCollectionSetting Cmdlet 會建立可指定輸送量與刪除行為的 [遷移設定] 物件。</span><span class="sxs-lookup"><span data-stu-id="80514-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="80514-107">輸出 Cmdlet 是具有集合名稱的 key 值對，以及設定的值。</span><span class="sxs-lookup"><span data-stu-id="80514-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="80514-108">輸出是用來將 [遷移] 的資料庫層級設定組合在一起。</span><span class="sxs-lookup"><span data-stu-id="80514-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="80514-109">示例</span><span class="sxs-lookup"><span data-stu-id="80514-109">EXAMPLES</span></span>

### <span data-ttu-id="80514-110">範例1</span><span class="sxs-lookup"><span data-stu-id="80514-110">Example 1</span></span>
```
PS C:\> $x = New-AzDataMigrationMongoDbCollectionSetting -Name myCollection -TargetRequestUnit 1000 -CanDelete -ShardKey "_id:-1,age:1,name"
PS C:\> $x

Name         Setting
----         -------
myCollection Microsoft.Azure.Management.DataMigration.Models.MongoDbCollectionSettings

PS C:\> $x.Setting

CanDelete ShardKey                                                               TargetRUs
--------- --------                                                               ---------
     True Microsoft.Azure.Management.DataMigration.Models.MongoDbShardKeySetting      1000

```

## <span data-ttu-id="80514-111">參數</span><span class="sxs-lookup"><span data-stu-id="80514-111">PARAMETERS</span></span>

### <span data-ttu-id="80514-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="80514-112">-Name</span></span>
<span data-ttu-id="80514-113">收藏的名稱</span><span class="sxs-lookup"><span data-stu-id="80514-113">Name of the collection</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80514-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="80514-114">-ShardKey</span></span>
<span data-ttu-id="80514-115">以逗號分隔的 shard 鍵清單。</span><span class="sxs-lookup"><span data-stu-id="80514-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="80514-116">對於 mongoDb 目標，您可以指定 shard 的 [ShardKeyName：順序] 順序，其中順序為1、-1 或空，以進行雜湊運算，例如「_id、email：-1」。</span><span class="sxs-lookup"><span data-stu-id="80514-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

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

### <span data-ttu-id="80514-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="80514-117">-TargetRequestUnit</span></span>
<span data-ttu-id="80514-118">專用集合要求單位值。</span><span class="sxs-lookup"><span data-stu-id="80514-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="80514-119">如果未設定，該集合會使用共用資料庫 RU。</span><span class="sxs-lookup"><span data-stu-id="80514-119">If not set, that collection uses shared database RU.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: RU

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80514-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="80514-120">-CanDelete</span></span>
<span data-ttu-id="80514-121">是否應該刪除目標資料（如果已設定），系統會在遷移時清除該選項</span><span class="sxs-lookup"><span data-stu-id="80514-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="80514-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80514-122">CommonParameters</span></span>
<span data-ttu-id="80514-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80514-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80514-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80514-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80514-125">輸入</span><span class="sxs-lookup"><span data-stu-id="80514-125">INPUTS</span></span>

### <span data-ttu-id="80514-126">所有</span><span class="sxs-lookup"><span data-stu-id="80514-126">None</span></span>

## <span data-ttu-id="80514-127">輸出</span><span class="sxs-lookup"><span data-stu-id="80514-127">OUTPUTS</span></span>

### <span data-ttu-id="80514-128">[DataMigration MongoDbCollectionSetting] 的></span><span class="sxs-lookup"><span data-stu-id="80514-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="80514-129">筆記</span><span class="sxs-lookup"><span data-stu-id="80514-129">NOTES</span></span>

## <span data-ttu-id="80514-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="80514-130">RELATED LINKS</span></span>