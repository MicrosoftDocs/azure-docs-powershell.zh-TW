---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
ms.openlocfilehash: ffbfad973e881c3ae88e961517d097d7c8d6cedd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958247"
---
# <span data-ttu-id="93b2c-101">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="93b2c-101">Get-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="93b2c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="93b2c-103">取得檔案系統中檔案或目錄的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="93b2c-103">Gets the details of a file or directory in a filesystem.</span></span>

## <span data-ttu-id="93b2c-104">句法</span><span class="sxs-lookup"><span data-stu-id="93b2c-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93b2c-105">說明</span><span class="sxs-lookup"><span data-stu-id="93b2c-105">DESCRIPTION</span></span>
<span data-ttu-id="93b2c-106">**AzDataLakeGen2Item** Cmdlet 會取得 Azure 儲存空間帳戶之檔案系統中檔案或目錄的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="93b2c-106">The **Get-AzDataLakeGen2Item** cmdlet gets the details of a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="93b2c-107">這個 Cmdlet 只有在已針對儲存空間帳戶啟用階層命名空間時才適用。</span><span class="sxs-lookup"><span data-stu-id="93b2c-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="93b2c-108">此類型的帳戶可使用「-EnableHierarchicalNamespace $true」執行「新-AzStorageAccount」 Cmdlet 來建立。</span><span class="sxs-lookup"><span data-stu-id="93b2c-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="93b2c-109">示例</span><span class="sxs-lookup"><span data-stu-id="93b2c-109">EXAMPLES</span></span>

### <span data-ttu-id="93b2c-110">範例1：從 Filesystem 取得目錄，並顯示詳細資料</span><span class="sxs-lookup"><span data-stu-id="93b2c-110">Example 1: Get a directory from a Filesystem, and show the details</span></span>
```
PS C:\> $dir1 = Get-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
PS C:\> $dir1

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser     
 
PS C:\WINDOWS\system32> $dir1.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      ---        
False        Other                      rwx      

PS C:\WINDOWS\system32> $dir1.Permissions

Owner        : Execute, Write, Read
Group        : None
Other        : Execute, Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\WINDOWS\system32> $dir1.Properties.Metadata

Key          Value 
---          ----- 
hdi_isfolder true  
tag1         value1
tag2         value2

PS C:\WINDOWS\system32> $dir1.Properties

LastModified          : 3/23/2020 9:15:56 AM +00:00
CreatedOn             : 3/23/2020 9:15:56 AM +00:00
Metadata              : {[hdi_isfolder, true], [tag1, value1], [tag2, value2]}
CopyCompletedOn       : 1/1/0001 12:00:00 AM +00:00
CopyStatusDescription : 
CopyId                : 
CopyProgress          : 
CopySource            : 
CopyStatus            : Pending
IsIncrementalCopy     : False
LeaseDuration         : Infinite
LeaseState            : Available
LeaseStatus           : Unlocked
ContentLength         : 0
ContentType           : application/octet-stream
ETag                  : "0x8D7CF0ACBA35FA8"
ContentHash           : 
ContentEncoding       : UDF12
ContentDisposition    : 
ContentLanguage       : 
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="93b2c-111">這個命令會從 Filesystem 中取得目錄，並顯示詳細資料。</span><span class="sxs-lookup"><span data-stu-id="93b2c-111">This command gets a directory from a Filesystem, and show the details.</span></span>

### <span data-ttu-id="93b2c-112">範例2：從檔案檔取得檔案</span><span class="sxs-lookup"><span data-stu-id="93b2c-112">Example 2: Get a file from a Filesystem</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:20:37Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="93b2c-113">這個命令會從檔案檔中取得檔案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="93b2c-113">This command gets the details of a file from a Filesystem.</span></span> 

## <span data-ttu-id="93b2c-114">參數</span><span class="sxs-lookup"><span data-stu-id="93b2c-114">PARAMETERS</span></span>

### <span data-ttu-id="93b2c-115">-內容</span><span class="sxs-lookup"><span data-stu-id="93b2c-115">-Context</span></span>
<span data-ttu-id="93b2c-116">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="93b2c-116">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93b2c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93b2c-117">-DefaultProfile</span></span>
<span data-ttu-id="93b2c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="93b2c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b2c-119">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="93b2c-119">-FileSystem</span></span>
<span data-ttu-id="93b2c-120">FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="93b2c-120">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93b2c-121">-Path</span><span class="sxs-lookup"><span data-stu-id="93b2c-121">-Path</span></span>
<span data-ttu-id="93b2c-122">要在指定的 Filesystem 中檢索的路徑。</span><span class="sxs-lookup"><span data-stu-id="93b2c-122">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="93b2c-123">可以是 "directory/file.txt" 格式或 "directory1/directory2/" 格式的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="93b2c-123">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="93b2c-124">請勿指定此參數來取得 Filesystem 的根目錄。</span><span class="sxs-lookup"><span data-stu-id="93b2c-124">Not specify this parameter to get the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93b2c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b2c-125">CommonParameters</span></span>
<span data-ttu-id="93b2c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93b2c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b2c-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="93b2c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b2c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="93b2c-128">INPUTS</span></span>

### <span data-ttu-id="93b2c-129">System.object</span><span class="sxs-lookup"><span data-stu-id="93b2c-129">System.String</span></span>

### <span data-ttu-id="93b2c-130">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="93b2c-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="93b2c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="93b2c-131">OUTPUTS</span></span>

### <span data-ttu-id="93b2c-132">AzureDataLakeGen2Item WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="93b2c-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="93b2c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="93b2c-133">NOTES</span></span>

## <span data-ttu-id="93b2c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="93b2c-134">RELATED LINKS</span></span>