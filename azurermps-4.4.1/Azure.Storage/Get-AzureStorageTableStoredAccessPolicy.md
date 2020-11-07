---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 85501affef70ce0cf31e62f9083d5ed383425497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623527"
---
# <span data-ttu-id="916e9-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="916e9-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="916e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="916e9-102">SYNOPSIS</span></span>
<span data-ttu-id="916e9-103">取得 Azure 儲存空間資料表的儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="916e9-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="916e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="916e9-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="916e9-105">說明</span><span class="sxs-lookup"><span data-stu-id="916e9-105">DESCRIPTION</span></span>
<span data-ttu-id="916e9-106">**AzureStorageTableStoredAccessPolicy** Cmdlet 會列出 Azure 儲存空間資料表的儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="916e9-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="916e9-107">示例</span><span class="sxs-lookup"><span data-stu-id="916e9-107">EXAMPLES</span></span>

### <span data-ttu-id="916e9-108">範例1：在儲存空間資料表中取得儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="916e9-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="916e9-109">這個命令會在名為 Table02 的儲存空間資料表中取得名為 Policy50 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="916e9-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="916e9-110">範例2：取得儲存空間資料表中所有已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="916e9-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="916e9-111">這個命令會取得名為 Table02 的資料表中的所有存取原則。</span><span class="sxs-lookup"><span data-stu-id="916e9-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="916e9-112">參數</span><span class="sxs-lookup"><span data-stu-id="916e9-112">PARAMETERS</span></span>

### <span data-ttu-id="916e9-113">-內容</span><span class="sxs-lookup"><span data-stu-id="916e9-113">-Context</span></span>
<span data-ttu-id="916e9-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="916e9-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="916e9-115">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="916e9-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="916e9-116">-原則</span><span class="sxs-lookup"><span data-stu-id="916e9-116">-Policy</span></span>
<span data-ttu-id="916e9-117">指定儲存的存取原則，包括此共用存取簽名 (SAS) 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="916e9-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="916e9-118">-資料表</span><span class="sxs-lookup"><span data-stu-id="916e9-118">-Table</span></span>
<span data-ttu-id="916e9-119">指定 Azure 儲存空間資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="916e9-119">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="916e9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="916e9-120">CommonParameters</span></span>
<span data-ttu-id="916e9-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="916e9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="916e9-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="916e9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="916e9-123">輸入</span><span class="sxs-lookup"><span data-stu-id="916e9-123">INPUTS</span></span>

### <span data-ttu-id="916e9-124">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="916e9-124">IStorageContext</span></span>

<span data-ttu-id="916e9-125">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="916e9-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="916e9-126">字串</span><span class="sxs-lookup"><span data-stu-id="916e9-126">String</span></span>

<span data-ttu-id="916e9-127">形參 "Table" 接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="916e9-127">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="916e9-128">輸出</span><span class="sxs-lookup"><span data-stu-id="916e9-128">OUTPUTS</span></span>

### <span data-ttu-id="916e9-129">[WindowsAzure] SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="916e9-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="916e9-130">筆記</span><span class="sxs-lookup"><span data-stu-id="916e9-130">NOTES</span></span>

## <span data-ttu-id="916e9-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="916e9-131">RELATED LINKS</span></span>

[<span data-ttu-id="916e9-132">新-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="916e9-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="916e9-133">移除-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="916e9-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="916e9-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="916e9-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="916e9-135">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="916e9-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

