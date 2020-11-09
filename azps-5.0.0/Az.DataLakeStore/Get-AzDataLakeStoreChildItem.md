---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: 6123cacd35eb0a683ec2103ea00e2e06a2d80cd2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285036"
---
# <span data-ttu-id="79a1c-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="79a1c-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="79a1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="79a1c-103">取得 Data Lake Store 中資料夾中的專案清單。</span><span class="sxs-lookup"><span data-stu-id="79a1c-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="79a1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="79a1c-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79a1c-105">說明</span><span class="sxs-lookup"><span data-stu-id="79a1c-105">DESCRIPTION</span></span>
<span data-ttu-id="79a1c-106">**AzDataLakeStoreChildItem** Cmdlet 會取得 Data Lake store 中資料夾中的專案清單。</span><span class="sxs-lookup"><span data-stu-id="79a1c-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="79a1c-107">示例</span><span class="sxs-lookup"><span data-stu-id="79a1c-107">EXAMPLES</span></span>

### <span data-ttu-id="79a1c-108">範例1：取得資料夾的子專案</span><span class="sxs-lookup"><span data-stu-id="79a1c-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="79a1c-109">這個命令會取得 MyFiles 資料夾的子專案。</span><span class="sxs-lookup"><span data-stu-id="79a1c-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="79a1c-110">參數</span><span class="sxs-lookup"><span data-stu-id="79a1c-110">PARAMETERS</span></span>

### <span data-ttu-id="79a1c-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="79a1c-111">-Account</span></span>
<span data-ttu-id="79a1c-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="79a1c-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="79a1c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a1c-113">-DefaultProfile</span></span>
<span data-ttu-id="79a1c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="79a1c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79a1c-115">-Path</span><span class="sxs-lookup"><span data-stu-id="79a1c-115">-Path</span></span>
<span data-ttu-id="79a1c-116">指定資料夾的 Data Lake Store 路徑，從 root 目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="79a1c-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="79a1c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a1c-117">CommonParameters</span></span>
<span data-ttu-id="79a1c-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79a1c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a1c-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="79a1c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a1c-120">輸入</span><span class="sxs-lookup"><span data-stu-id="79a1c-120">INPUTS</span></span>

### <span data-ttu-id="79a1c-121">System.object</span><span class="sxs-lookup"><span data-stu-id="79a1c-121">System.String</span></span>

### <span data-ttu-id="79a1c-122">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="79a1c-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="79a1c-123">輸出</span><span class="sxs-lookup"><span data-stu-id="79a1c-123">OUTPUTS</span></span>

### <span data-ttu-id="79a1c-124">DataLakeStoreItem 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="79a1c-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="79a1c-125">筆記</span><span class="sxs-lookup"><span data-stu-id="79a1c-125">NOTES</span></span>

## <span data-ttu-id="79a1c-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="79a1c-126">RELATED LINKS</span></span>