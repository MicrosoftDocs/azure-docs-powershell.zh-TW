---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
ms.openlocfilehash: 7423cbb6995430523beb137ef10eb6f1a53c959c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624515"
---
# <span data-ttu-id="075d2-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="075d2-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="075d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="075d2-102">SYNOPSIS</span></span>
<span data-ttu-id="075d2-103">移除儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="075d2-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="075d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="075d2-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="075d2-105">說明</span><span class="sxs-lookup"><span data-stu-id="075d2-105">DESCRIPTION</span></span>
<span data-ttu-id="075d2-106">**AzureStorageTable** Cmdlet 會從 Azure 中的儲存空間中移除一或多個儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="075d2-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="075d2-107">示例</span><span class="sxs-lookup"><span data-stu-id="075d2-107">EXAMPLES</span></span>

### <span data-ttu-id="075d2-108">範例1：移除表格</span><span class="sxs-lookup"><span data-stu-id="075d2-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="075d2-109">這個命令會移除表格。</span><span class="sxs-lookup"><span data-stu-id="075d2-109">This command removes a table.</span></span>

### <span data-ttu-id="075d2-110">範例2：移除多個表格</span><span class="sxs-lookup"><span data-stu-id="075d2-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="075d2-111">這個範例將萬用字元與 *Name* 參數搭配使用，以取得符合模式資料表的所有資料表，然後在管線上傳遞結果來移除資料表。</span><span class="sxs-lookup"><span data-stu-id="075d2-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="075d2-112">參數</span><span class="sxs-lookup"><span data-stu-id="075d2-112">PARAMETERS</span></span>

### <span data-ttu-id="075d2-113">-內容</span><span class="sxs-lookup"><span data-stu-id="075d2-113">-Context</span></span>
<span data-ttu-id="075d2-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="075d2-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="075d2-115">您可以使用 New-AzureStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="075d2-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="075d2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="075d2-116">-Force</span></span>
<span data-ttu-id="075d2-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="075d2-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="075d2-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="075d2-118">-Name</span></span>
<span data-ttu-id="075d2-119">指定要移除的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="075d2-119">Specifies the name of the table to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="075d2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="075d2-120">-PassThru</span></span>
<span data-ttu-id="075d2-121">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="075d2-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="075d2-122">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="075d2-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="075d2-123">-確認</span><span class="sxs-lookup"><span data-stu-id="075d2-123">-Confirm</span></span>
<span data-ttu-id="075d2-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="075d2-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="075d2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="075d2-125">-WhatIf</span></span>
<span data-ttu-id="075d2-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="075d2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="075d2-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="075d2-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="075d2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="075d2-128">CommonParameters</span></span>
<span data-ttu-id="075d2-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="075d2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="075d2-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="075d2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="075d2-131">輸入</span><span class="sxs-lookup"><span data-stu-id="075d2-131">INPUTS</span></span>

### <span data-ttu-id="075d2-132">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="075d2-132">IStorageContext</span></span>

<span data-ttu-id="075d2-133">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="075d2-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="075d2-134">字串</span><span class="sxs-lookup"><span data-stu-id="075d2-134">String</span></span>

<span data-ttu-id="075d2-135">形參 "Name" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="075d2-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="075d2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="075d2-136">OUTPUTS</span></span>

### <span data-ttu-id="075d2-137">System.object</span><span class="sxs-lookup"><span data-stu-id="075d2-137">System.Boolean</span></span>

## <span data-ttu-id="075d2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="075d2-138">NOTES</span></span>

## <span data-ttu-id="075d2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="075d2-139">RELATED LINKS</span></span>

[<span data-ttu-id="075d2-140">AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="075d2-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)