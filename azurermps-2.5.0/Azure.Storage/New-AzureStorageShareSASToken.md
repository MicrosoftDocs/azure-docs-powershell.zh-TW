---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragesharesastoken
schema: 2.0.0
ms.openlocfilehash: dbfee49f6e6fcd083350a5ab818ac33309e4b672
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801457"
---
# <span data-ttu-id="affa3-101">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="affa3-101">New-AzureStorageShareSASToken</span></span>

## <span data-ttu-id="affa3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="affa3-102">SYNOPSIS</span></span>
<span data-ttu-id="affa3-103">產生 Azure 儲存空間共用的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="affa3-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="affa3-104">句法</span><span class="sxs-lookup"><span data-stu-id="affa3-104">SYNTAX</span></span>

### <span data-ttu-id="affa3-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="affa3-105">SasPolicy</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="affa3-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="affa3-106">SasPermission</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="affa3-107">說明</span><span class="sxs-lookup"><span data-stu-id="affa3-107">DESCRIPTION</span></span>
<span data-ttu-id="affa3-108">**新的-AzureStorageShareSASToken** Cmdlet 會針對 Azure 儲存空間共用產生共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="affa3-108">The **New-AzureStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="affa3-109">示例</span><span class="sxs-lookup"><span data-stu-id="affa3-109">EXAMPLES</span></span>

### <span data-ttu-id="affa3-110">範例1：為共用產生共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="affa3-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="affa3-111">這個命令會建立名為 ContosoShare 的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="affa3-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="affa3-112">範例2：使用管線產生多個共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="affa3-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="affa3-113">這個命令會取得符合前置詞測試的所有儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="affa3-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="affa3-114">命令會使用管線運算子將它們傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="affa3-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="affa3-115">目前的 Cmdlet 會為具有指定許可權的每個儲存空間共用建立共用存取權杖。</span><span class="sxs-lookup"><span data-stu-id="affa3-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="affa3-116">範例3：產生使用共用存取原則的共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="affa3-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="affa3-117">這個命令會為擁有名為 ContosoPolicy03 原則之名為 ContosoShare 的儲存空間共用建立共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="affa3-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="affa3-118">參數</span><span class="sxs-lookup"><span data-stu-id="affa3-118">PARAMETERS</span></span>

### <span data-ttu-id="affa3-119">-內容</span><span class="sxs-lookup"><span data-stu-id="affa3-119">-Context</span></span>
<span data-ttu-id="affa3-120">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="affa3-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="affa3-121">若要取得內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="affa3-121">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="affa3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="affa3-122">-DefaultProfile</span></span>
<span data-ttu-id="affa3-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="affa3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="affa3-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="affa3-124">-ExpiryTime</span></span>
<span data-ttu-id="affa3-125">指定共用存取簽名失效的時間。</span><span class="sxs-lookup"><span data-stu-id="affa3-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="affa3-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="affa3-126">-FullUri</span></span>
<span data-ttu-id="affa3-127">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="affa3-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="affa3-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="affa3-128">-IPAddressOrRange</span></span>
<span data-ttu-id="affa3-129">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="affa3-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="affa3-130">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="affa3-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="affa3-131">-許可權</span><span class="sxs-lookup"><span data-stu-id="affa3-131">-Permission</span></span>
<span data-ttu-id="affa3-132">指定權杖中的許可權，以存取共用中的共用和檔案。</span><span class="sxs-lookup"><span data-stu-id="affa3-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="affa3-133">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="affa3-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affa3-134">-原則</span><span class="sxs-lookup"><span data-stu-id="affa3-134">-Policy</span></span>
<span data-ttu-id="affa3-135">指定共用的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="affa3-135">Specifies the stored access policy for a share.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affa3-136">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="affa3-136">-Protocol</span></span>
<span data-ttu-id="affa3-137">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="affa3-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="affa3-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="affa3-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="affa3-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="affa3-139">HttpsOnly</span></span>
* <span data-ttu-id="affa3-140">HttpsOrHttp 預設值是 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="affa3-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affa3-141">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="affa3-141">-ShareName</span></span>
<span data-ttu-id="affa3-142">指定儲存空間共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="affa3-142">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="affa3-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="affa3-143">-StartTime</span></span>
<span data-ttu-id="affa3-144">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="affa3-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="affa3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="affa3-145">CommonParameters</span></span>
<span data-ttu-id="affa3-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="affa3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="affa3-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="affa3-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="affa3-148">輸入</span><span class="sxs-lookup"><span data-stu-id="affa3-148">INPUTS</span></span>

### <span data-ttu-id="affa3-149">System.object</span><span class="sxs-lookup"><span data-stu-id="affa3-149">System.String</span></span>

### <span data-ttu-id="affa3-150">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="affa3-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="affa3-151">輸出</span><span class="sxs-lookup"><span data-stu-id="affa3-151">OUTPUTS</span></span>

### <span data-ttu-id="affa3-152">System.object</span><span class="sxs-lookup"><span data-stu-id="affa3-152">System.String</span></span>

## <span data-ttu-id="affa3-153">筆記</span><span class="sxs-lookup"><span data-stu-id="affa3-153">NOTES</span></span>
* <span data-ttu-id="affa3-154">關鍵字：常見、azure、services、data、storage、blob、queue、table</span><span class="sxs-lookup"><span data-stu-id="affa3-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="affa3-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="affa3-155">RELATED LINKS</span></span>

[<span data-ttu-id="affa3-156">AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="affa3-156">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="affa3-157">新-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="affa3-157">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)