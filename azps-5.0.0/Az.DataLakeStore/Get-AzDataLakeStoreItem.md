---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: ad741d955399b355534074737741b153d8d48690
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285027"
---
# <span data-ttu-id="c2186-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c2186-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="c2186-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2186-102">SYNOPSIS</span></span>
<span data-ttu-id="c2186-103">取得 Data Lake Store 中檔案或資料夾的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c2186-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c2186-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2186-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2186-105">說明</span><span class="sxs-lookup"><span data-stu-id="c2186-105">DESCRIPTION</span></span>
<span data-ttu-id="c2186-106">**AzDataLakeStoreItem** Cmdlet 會取得 Data Lake store 中檔案或資料夾的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c2186-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c2186-107">示例</span><span class="sxs-lookup"><span data-stu-id="c2186-107">EXAMPLES</span></span>

### <span data-ttu-id="c2186-108">範例1：從 Data Lake Store 取得檔案的詳細資料</span><span class="sxs-lookup"><span data-stu-id="c2186-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="c2186-109">這個命令會從 Data Lake Store 取得檔案 Test.csv 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c2186-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="c2186-110">參數</span><span class="sxs-lookup"><span data-stu-id="c2186-110">PARAMETERS</span></span>

### <span data-ttu-id="c2186-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="c2186-111">-Account</span></span>
<span data-ttu-id="c2186-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2186-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c2186-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2186-113">-DefaultProfile</span></span>
<span data-ttu-id="c2186-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2186-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2186-115">-Path</span><span class="sxs-lookup"><span data-stu-id="c2186-115">-Path</span></span>
<span data-ttu-id="c2186-116">指定資料 Lake Store 路徑，從根目錄 (/) 開始，可從該目錄取得專案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c2186-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2186-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2186-117">CommonParameters</span></span>
<span data-ttu-id="c2186-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2186-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2186-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2186-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2186-120">輸入</span><span class="sxs-lookup"><span data-stu-id="c2186-120">INPUTS</span></span>

### <span data-ttu-id="c2186-121">System.object</span><span class="sxs-lookup"><span data-stu-id="c2186-121">System.String</span></span>

### <span data-ttu-id="c2186-122">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="c2186-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="c2186-123">輸出</span><span class="sxs-lookup"><span data-stu-id="c2186-123">OUTPUTS</span></span>

### <span data-ttu-id="c2186-124">DataLakeStoreItem 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="c2186-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="c2186-125">筆記</span><span class="sxs-lookup"><span data-stu-id="c2186-125">NOTES</span></span>

## <span data-ttu-id="c2186-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2186-126">RELATED LINKS</span></span>

[<span data-ttu-id="c2186-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c2186-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="c2186-128">AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="c2186-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="c2186-129">匯入-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c2186-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="c2186-130">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c2186-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="c2186-131">移動流覽 AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c2186-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="c2186-132">新-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c2186-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="c2186-133">移除-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c2186-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="c2186-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c2186-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)

