---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: ddb291a72d3c35c79321ddefa0832d46c489998f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285119"
---
# <span data-ttu-id="a41c0-101">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a41c0-101">Add-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="a41c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a41c0-102">SYNOPSIS</span></span>
<span data-ttu-id="a41c0-103">將資料來源新增至 Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="a41c0-103">Adds a data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="a41c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="a41c0-104">SYNTAX</span></span>

### <span data-ttu-id="a41c0-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a41c0-105">AddDataLakeStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a41c0-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a41c0-106">AddBlobStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a41c0-107">說明</span><span class="sxs-lookup"><span data-stu-id="a41c0-107">DESCRIPTION</span></span>
<span data-ttu-id="a41c0-108">**載入 AzDataLakeAnalyticsDataSource** Cmdlet 會將資料來源新增至 Azure Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="a41c0-108">The **Add-AzDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="a41c0-109">示例</span><span class="sxs-lookup"><span data-stu-id="a41c0-109">EXAMPLES</span></span>

### <span data-ttu-id="a41c0-110">範例1：新增資料來源至帳戶</span><span class="sxs-lookup"><span data-stu-id="a41c0-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="a41c0-111">這個命令會將 Data Lake Store 資料來源新增到 Data Lake Analytics 帳戶。</span><span class="sxs-lookup"><span data-stu-id="a41c0-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="a41c0-112">參數</span><span class="sxs-lookup"><span data-stu-id="a41c0-112">PARAMETERS</span></span>

### <span data-ttu-id="a41c0-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="a41c0-113">-AccessKey</span></span>
<span data-ttu-id="a41c0-114">指定要新增之 Azure Blob 儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="a41c0-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a41c0-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="a41c0-115">-Account</span></span>
<span data-ttu-id="a41c0-116">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a41c0-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a41c0-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="a41c0-117">-Blob</span></span>
<span data-ttu-id="a41c0-118">指定要新增之 Azure Blob 儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a41c0-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a41c0-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a41c0-119">-DataLakeStore</span></span>
<span data-ttu-id="a41c0-120">指定要新增之 Azure Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a41c0-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a41c0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a41c0-121">-DefaultProfile</span></span>
<span data-ttu-id="a41c0-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a41c0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a41c0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a41c0-123">-ResourceGroupName</span></span>
<span data-ttu-id="a41c0-124">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a41c0-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a41c0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a41c0-125">CommonParameters</span></span>
<span data-ttu-id="a41c0-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a41c0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a41c0-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a41c0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a41c0-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a41c0-128">INPUTS</span></span>

### <span data-ttu-id="a41c0-129">System.object</span><span class="sxs-lookup"><span data-stu-id="a41c0-129">System.String</span></span>

## <span data-ttu-id="a41c0-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a41c0-130">OUTPUTS</span></span>

### <span data-ttu-id="a41c0-131">System.object</span><span class="sxs-lookup"><span data-stu-id="a41c0-131">System.Object</span></span>
## <span data-ttu-id="a41c0-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a41c0-132">NOTES</span></span>

## <span data-ttu-id="a41c0-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a41c0-133">RELATED LINKS</span></span>

[<span data-ttu-id="a41c0-134">移除-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a41c0-134">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="a41c0-135">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a41c0-135">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)

