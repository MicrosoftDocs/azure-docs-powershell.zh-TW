---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragesharestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: a3abd3a6e0b3c3dcc04de6ca4bc69c6ed80bcab9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801450"
---
# <span data-ttu-id="b50b0-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b50b0-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="b50b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b50b0-102">SYNOPSIS</span></span>
<span data-ttu-id="b50b0-103">在儲存空間共用上建立儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="b50b0-103">Creates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b50b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="b50b0-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b50b0-105">說明</span><span class="sxs-lookup"><span data-stu-id="b50b0-105">DESCRIPTION</span></span>
<span data-ttu-id="b50b0-106">**新的-AzureStorageShareStoredAccessPolicy** Cmdlet 會在 Azure 儲存空間共用上建立儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="b50b0-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="b50b0-107">示例</span><span class="sxs-lookup"><span data-stu-id="b50b0-107">EXAMPLES</span></span>

### <span data-ttu-id="b50b0-108">範例1：在共用中建立儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="b50b0-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="b50b0-109">這個命令會建立一個在共用中擁有完整許可權的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="b50b0-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="b50b0-110">參數</span><span class="sxs-lookup"><span data-stu-id="b50b0-110">PARAMETERS</span></span>

### <span data-ttu-id="b50b0-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b50b0-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b50b0-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b50b0-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b50b0-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="b50b0-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b50b0-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b50b0-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b50b0-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b50b0-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b50b0-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="b50b0-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b50b0-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="b50b0-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b50b0-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="b50b0-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b50b0-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="b50b0-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b50b0-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="b50b0-120">The default value is 10.</span></span>

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

### <span data-ttu-id="b50b0-121">-內容</span><span class="sxs-lookup"><span data-stu-id="b50b0-121">-Context</span></span>
<span data-ttu-id="b50b0-122">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="b50b0-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b50b0-123">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b50b0-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b50b0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b50b0-124">-DefaultProfile</span></span>
<span data-ttu-id="b50b0-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b50b0-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b50b0-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b50b0-126">-ExpiryTime</span></span>
<span data-ttu-id="b50b0-127">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="b50b0-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b50b0-128">-許可權</span><span class="sxs-lookup"><span data-stu-id="b50b0-128">-Permission</span></span>
<span data-ttu-id="b50b0-129">指定儲存的存取原則中的許可權，以存取儲存空間共用或其下的檔案。</span><span class="sxs-lookup"><span data-stu-id="b50b0-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="b50b0-130">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="b50b0-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="b50b0-131">-原則</span><span class="sxs-lookup"><span data-stu-id="b50b0-131">-Policy</span></span>
<span data-ttu-id="b50b0-132">指定儲存的存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b50b0-132">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b50b0-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b50b0-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b50b0-134">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="b50b0-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b50b0-135">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="b50b0-135">-ShareName</span></span>
<span data-ttu-id="b50b0-136">指定儲存空間共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="b50b0-136">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b50b0-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b50b0-137">-StartTime</span></span>
<span data-ttu-id="b50b0-138">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="b50b0-138">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b50b0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b50b0-139">CommonParameters</span></span>
<span data-ttu-id="b50b0-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b50b0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b50b0-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b50b0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b50b0-142">輸入</span><span class="sxs-lookup"><span data-stu-id="b50b0-142">INPUTS</span></span>

### <span data-ttu-id="b50b0-143">System.object</span><span class="sxs-lookup"><span data-stu-id="b50b0-143">System.String</span></span>

### <span data-ttu-id="b50b0-144">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="b50b0-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b50b0-145">輸出</span><span class="sxs-lookup"><span data-stu-id="b50b0-145">OUTPUTS</span></span>

### <span data-ttu-id="b50b0-146">System.object</span><span class="sxs-lookup"><span data-stu-id="b50b0-146">System.String</span></span>

## <span data-ttu-id="b50b0-147">筆記</span><span class="sxs-lookup"><span data-stu-id="b50b0-147">NOTES</span></span>

## <span data-ttu-id="b50b0-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="b50b0-148">RELATED LINKS</span></span>

[<span data-ttu-id="b50b0-149">AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b50b0-149">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="b50b0-150">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="b50b0-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b50b0-151">移除-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b50b0-151">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="b50b0-152">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b50b0-152">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)