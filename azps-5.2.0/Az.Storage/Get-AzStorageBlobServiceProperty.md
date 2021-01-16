---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 7cdef2f35180712d0751149a85e4a422a868c389
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273796"
---
# <span data-ttu-id="89bbb-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="89bbb-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="89bbb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="89bbb-103">取得 Azure Storage Blob 服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="89bbb-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="89bbb-104">句法</span><span class="sxs-lookup"><span data-stu-id="89bbb-104">SYNTAX</span></span>

### <span data-ttu-id="89bbb-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="89bbb-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89bbb-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="89bbb-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89bbb-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="89bbb-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89bbb-108">說明</span><span class="sxs-lookup"><span data-stu-id="89bbb-108">DESCRIPTION</span></span>
<span data-ttu-id="89bbb-109">**AzStorageBlobServiceProperty** Cmdlet 會取得 Azure Storage Blob 服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="89bbb-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="89bbb-110">示例</span><span class="sxs-lookup"><span data-stu-id="89bbb-110">EXAMPLES</span></span>

### <span data-ttu-id="89bbb-111">範例1：取得指定儲存空間帳戶的 Azure 儲存體 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="89bbb-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="89bbb-112">這個命令會取得指定儲存空間帳戶的 [Blob 服務] 屬性。</span><span class="sxs-lookup"><span data-stu-id="89bbb-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="89bbb-113">參數</span><span class="sxs-lookup"><span data-stu-id="89bbb-113">PARAMETERS</span></span>

### <span data-ttu-id="89bbb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89bbb-114">-DefaultProfile</span></span>
<span data-ttu-id="89bbb-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="89bbb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89bbb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89bbb-116">-ResourceGroupName</span></span>
<span data-ttu-id="89bbb-117">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="89bbb-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89bbb-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89bbb-118">-ResourceId</span></span>
<span data-ttu-id="89bbb-119">Blob 服務屬性 [資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="89bbb-119">Blob Service Properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89bbb-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="89bbb-120">-StorageAccount</span></span>
<span data-ttu-id="89bbb-121">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="89bbb-121">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89bbb-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="89bbb-122">-StorageAccountName</span></span>
<span data-ttu-id="89bbb-123">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="89bbb-123">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89bbb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89bbb-124">CommonParameters</span></span>
<span data-ttu-id="89bbb-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89bbb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89bbb-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="89bbb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89bbb-127">輸入</span><span class="sxs-lookup"><span data-stu-id="89bbb-127">INPUTS</span></span>

### <span data-ttu-id="89bbb-128">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="89bbb-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="89bbb-129">System.object</span><span class="sxs-lookup"><span data-stu-id="89bbb-129">System.String</span></span>

## <span data-ttu-id="89bbb-130">輸出</span><span class="sxs-lookup"><span data-stu-id="89bbb-130">OUTPUTS</span></span>

### <span data-ttu-id="89bbb-131">PSBlobServiceProperties 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="89bbb-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="89bbb-132">筆記</span><span class="sxs-lookup"><span data-stu-id="89bbb-132">NOTES</span></span>

## <span data-ttu-id="89bbb-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="89bbb-133">RELATED LINKS</span></span>