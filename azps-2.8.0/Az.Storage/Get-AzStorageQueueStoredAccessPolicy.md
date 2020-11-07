---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 9c740dec8cc2e3f3666d00c12def3eefb7cafce9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793023"
---
# <span data-ttu-id="c518d-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c518d-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="c518d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c518d-102">SYNOPSIS</span></span>
<span data-ttu-id="c518d-103">取得 Azure 儲存空間佇列的儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="c518d-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="c518d-104">句法</span><span class="sxs-lookup"><span data-stu-id="c518d-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c518d-105">說明</span><span class="sxs-lookup"><span data-stu-id="c518d-105">DESCRIPTION</span></span>
<span data-ttu-id="c518d-106">**AzStorageQueueStoredAccessPolicy** Cmdlet 會列出 Azure 儲存空間佇列的已儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="c518d-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="c518d-107">示例</span><span class="sxs-lookup"><span data-stu-id="c518d-107">EXAMPLES</span></span>

### <span data-ttu-id="c518d-108">範例1：在佇列中取得儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="c518d-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="c518d-109">這個命令會在名為 MyQueue 的儲存佇列中取得名為 Policy12 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="c518d-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="c518d-110">範例2：取得佇列中所有已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="c518d-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="c518d-111">這個命令會取得名為 MyQueue 的佇列中所有已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="c518d-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="c518d-112">參數</span><span class="sxs-lookup"><span data-stu-id="c518d-112">PARAMETERS</span></span>

### <span data-ttu-id="c518d-113">-內容</span><span class="sxs-lookup"><span data-stu-id="c518d-113">-Context</span></span>
<span data-ttu-id="c518d-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="c518d-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="c518d-115">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c518d-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c518d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c518d-116">-DefaultProfile</span></span>
<span data-ttu-id="c518d-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c518d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c518d-118">-原則</span><span class="sxs-lookup"><span data-stu-id="c518d-118">-Policy</span></span>
<span data-ttu-id="c518d-119">指定儲存的存取原則，包括此共用存取簽名 (SAS) 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="c518d-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c518d-120">-佇列</span><span class="sxs-lookup"><span data-stu-id="c518d-120">-Queue</span></span>
<span data-ttu-id="c518d-121">指定 Azure 儲存空間佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="c518d-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="c518d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c518d-122">CommonParameters</span></span>
<span data-ttu-id="c518d-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c518d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c518d-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c518d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c518d-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c518d-125">INPUTS</span></span>

### <span data-ttu-id="c518d-126">System.object</span><span class="sxs-lookup"><span data-stu-id="c518d-126">System.String</span></span>

### <span data-ttu-id="c518d-127">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="c518d-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c518d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="c518d-128">OUTPUTS</span></span>

### <span data-ttu-id="c518d-129">SharedAccessQueuePolicy 的存儲。</span><span class="sxs-lookup"><span data-stu-id="c518d-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="c518d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="c518d-130">NOTES</span></span>

## <span data-ttu-id="c518d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="c518d-131">RELATED LINKS</span></span>

[<span data-ttu-id="c518d-132">新-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c518d-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c518d-133">移除-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c518d-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c518d-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c518d-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c518d-135">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="c518d-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

