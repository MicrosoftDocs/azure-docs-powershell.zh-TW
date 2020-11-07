---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermcurrentstorageaccount
schema: 2.0.0
ms.openlocfilehash: 6a7ef50e6e95a30140549343d14d4a75ad340cbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624981"
---
# <span data-ttu-id="7c158-101">Set-AzureRmCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c158-101">Set-AzureRmCurrentStorageAccount</span></span>

## <span data-ttu-id="7c158-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c158-102">SYNOPSIS</span></span>
<span data-ttu-id="7c158-103">修改指定訂閱的目前儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="7c158-103">Modifies the current Storage account of the specified subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c158-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c158-104">SYNTAX</span></span>

### <span data-ttu-id="7c158-105">UsingResourceGroupAndNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7c158-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzureRmCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c158-106">UsingStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="7c158-106">UsingStorageContext</span></span>
```
Set-AzureRmCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c158-107">說明</span><span class="sxs-lookup"><span data-stu-id="7c158-107">DESCRIPTION</span></span>
<span data-ttu-id="7c158-108">**AzureRmCurrentStorageAccount** Cmdlet 會修改 azure PowerShell 中指定 azure 訂閱的目前 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="7c158-108">The **Set-AzureRmCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="7c158-109">當您存取儲存空間而不指定儲存空間帳戶名稱時，會使用目前的儲存空間帳戶作為預設值。</span><span class="sxs-lookup"><span data-stu-id="7c158-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="7c158-110">示例</span><span class="sxs-lookup"><span data-stu-id="7c158-110">EXAMPLES</span></span>

### <span data-ttu-id="7c158-111">範例1：設定目前的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="7c158-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzureRmCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="7c158-112">這個命令會設定指定訂閱的預設儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="7c158-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="7c158-113">參數</span><span class="sxs-lookup"><span data-stu-id="7c158-113">PARAMETERS</span></span>

### <span data-ttu-id="7c158-114">-內容</span><span class="sxs-lookup"><span data-stu-id="7c158-114">-Context</span></span>
<span data-ttu-id="7c158-115">指定目前儲存空間帳戶的 **AzureStorageCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="7c158-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="7c158-116">若要取得儲存內容物件，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c158-116">To obtain a storage context object, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: UsingStorageContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c158-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c158-117">-DefaultProfile</span></span>
<span data-ttu-id="7c158-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c158-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c158-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7c158-119">-Name</span></span>
<span data-ttu-id="7c158-120">指定此 Cmdlet 修改的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7c158-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c158-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c158-121">-ResourceGroupName</span></span>
<span data-ttu-id="7c158-122">指定包含要修改之儲存空間帳戶的資源群組。</span><span class="sxs-lookup"><span data-stu-id="7c158-122">Specifies the resource group that contains the Storage account to modify.</span></span>

```yaml
Type: String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c158-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c158-123">CommonParameters</span></span>
<span data-ttu-id="7c158-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c158-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c158-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c158-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c158-126">輸入</span><span class="sxs-lookup"><span data-stu-id="7c158-126">INPUTS</span></span>

### <span data-ttu-id="7c158-127">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="7c158-127">IStorageContext</span></span>
<span data-ttu-id="7c158-128">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="7c158-128">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="7c158-129">輸出</span><span class="sxs-lookup"><span data-stu-id="7c158-129">OUTPUTS</span></span>

### <span data-ttu-id="7c158-130">System.object</span><span class="sxs-lookup"><span data-stu-id="7c158-130">System.String</span></span>

## <span data-ttu-id="7c158-131">筆記</span><span class="sxs-lookup"><span data-stu-id="7c158-131">NOTES</span></span>

## <span data-ttu-id="7c158-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c158-132">RELATED LINKS</span></span>

[<span data-ttu-id="7c158-133">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c158-133">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)

