---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 7bca28da7b4729a414fafc5268bc4e0e02ee3c72
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795131"
---
# <span data-ttu-id="c37b3-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c37b3-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="c37b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c37b3-102">SYNOPSIS</span></span>
<span data-ttu-id="c37b3-103">取得 Azure 儲存服務的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="c37b3-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="c37b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="c37b3-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c37b3-105">說明</span><span class="sxs-lookup"><span data-stu-id="c37b3-105">DESCRIPTION</span></span>
<span data-ttu-id="c37b3-106">**AzStorageServiceMetricsProperty** Cmdlet 會取得 Azure 儲存空間服務的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="c37b3-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="c37b3-107">示例</span><span class="sxs-lookup"><span data-stu-id="c37b3-107">EXAMPLES</span></span>

### <span data-ttu-id="c37b3-108">範例1：取得 Blob 服務的度量屬性</span><span class="sxs-lookup"><span data-stu-id="c37b3-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="c37b3-109">這個命令會針對小時標準類型取得 blob 儲存空間的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="c37b3-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="c37b3-110">參數</span><span class="sxs-lookup"><span data-stu-id="c37b3-110">PARAMETERS</span></span>

### <span data-ttu-id="c37b3-111">-內容</span><span class="sxs-lookup"><span data-stu-id="c37b3-111">-Context</span></span>
<span data-ttu-id="c37b3-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="c37b3-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c37b3-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c37b3-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c37b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c37b3-114">-DefaultProfile</span></span>
<span data-ttu-id="c37b3-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c37b3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c37b3-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="c37b3-116">-MetricsType</span></span>
<span data-ttu-id="c37b3-117">指定公制類型。</span><span class="sxs-lookup"><span data-stu-id="c37b3-117">Specifies a metrics type.</span></span>
<span data-ttu-id="c37b3-118">這個 Cmdlet 會針對此參數指定的公制類型，取得 Azure Storage service 公制屬性。</span><span class="sxs-lookup"><span data-stu-id="c37b3-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="c37b3-119">此參數可接受的值為： Hour 和 Minute。</span><span class="sxs-lookup"><span data-stu-id="c37b3-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c37b3-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c37b3-120">-ServiceType</span></span>
<span data-ttu-id="c37b3-121">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="c37b3-121">Specifies the storage service type.</span></span>
<span data-ttu-id="c37b3-122">這個 Cmdlet 會取得此參數指定之類型的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="c37b3-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="c37b3-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c37b3-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c37b3-124">Blob</span><span class="sxs-lookup"><span data-stu-id="c37b3-124">Blob</span></span> 
- <span data-ttu-id="c37b3-125">張</span><span class="sxs-lookup"><span data-stu-id="c37b3-125">Table</span></span>
- <span data-ttu-id="c37b3-126">序列</span><span class="sxs-lookup"><span data-stu-id="c37b3-126">Queue</span></span>
- <span data-ttu-id="c37b3-127">檔案目前不支援檔的值。</span><span class="sxs-lookup"><span data-stu-id="c37b3-127">File The value of File is not currently supported.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c37b3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c37b3-128">CommonParameters</span></span>
<span data-ttu-id="c37b3-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c37b3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c37b3-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c37b3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c37b3-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c37b3-131">INPUTS</span></span>

### <span data-ttu-id="c37b3-132">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="c37b3-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c37b3-133">輸出</span><span class="sxs-lookup"><span data-stu-id="c37b3-133">OUTPUTS</span></span>

### <span data-ttu-id="c37b3-134">MetricsProperties 中的 WindowsAz。</span><span class="sxs-lookup"><span data-stu-id="c37b3-134">Microsoft.WindowsAz.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="c37b3-135">筆記</span><span class="sxs-lookup"><span data-stu-id="c37b3-135">NOTES</span></span>

## <span data-ttu-id="c37b3-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="c37b3-136">RELATED LINKS</span></span>

[<span data-ttu-id="c37b3-137">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="c37b3-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c37b3-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c37b3-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)

