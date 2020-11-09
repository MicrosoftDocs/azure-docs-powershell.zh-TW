---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: 2662eeeeaedbac75f443bf6160c625dfdb8dd854
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288344"
---
# <span data-ttu-id="ae762-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ae762-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="ae762-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae762-102">SYNOPSIS</span></span>
<span data-ttu-id="ae762-103">取得批次帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="ae762-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="ae762-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae762-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae762-105">說明</span><span class="sxs-lookup"><span data-stu-id="ae762-105">DESCRIPTION</span></span>
<span data-ttu-id="ae762-106">**AzBatchAccountKey** Cmdlet 會在目前的訂閱中取得 Azure Batch 帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="ae762-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="ae762-107">示例</span><span class="sxs-lookup"><span data-stu-id="ae762-107">EXAMPLES</span></span>

### <span data-ttu-id="ae762-108">範例1：取得批次處理帳戶金鑰並將它儲存在 $CoNtext 變數中供日後使用</span><span class="sxs-lookup"><span data-stu-id="ae762-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="ae762-109">這個命令會取得帳戶詳細資料，並將其儲存在 `$Context` 物件中供日後使用。</span><span class="sxs-lookup"><span data-stu-id="ae762-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="ae762-110">範例2：取得 batch 帳戶金鑰並顯示它們</span><span class="sxs-lookup"><span data-stu-id="ae762-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="ae762-111">這個命令會取得帳戶金鑰並將其列印到主控台。</span><span class="sxs-lookup"><span data-stu-id="ae762-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="ae762-112">參數</span><span class="sxs-lookup"><span data-stu-id="ae762-112">PARAMETERS</span></span>

### <span data-ttu-id="ae762-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ae762-113">-AccountName</span></span>
<span data-ttu-id="ae762-114">指定此 Cmdlet 取得金鑰的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ae762-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae762-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae762-115">-DefaultProfile</span></span>
<span data-ttu-id="ae762-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae762-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae762-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae762-117">-ResourceGroupName</span></span>
<span data-ttu-id="ae762-118">指定包含此 Cmdlet 取得金鑰之帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae762-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae762-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae762-119">CommonParameters</span></span>
<span data-ttu-id="ae762-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae762-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae762-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ae762-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae762-122">輸入</span><span class="sxs-lookup"><span data-stu-id="ae762-122">INPUTS</span></span>

### <span data-ttu-id="ae762-123">System.object</span><span class="sxs-lookup"><span data-stu-id="ae762-123">System.String</span></span>

## <span data-ttu-id="ae762-124">輸出</span><span class="sxs-lookup"><span data-stu-id="ae762-124">OUTPUTS</span></span>

### <span data-ttu-id="ae762-125">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="ae762-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ae762-126">筆記</span><span class="sxs-lookup"><span data-stu-id="ae762-126">NOTES</span></span>

## <span data-ttu-id="ae762-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae762-127">RELATED LINKS</span></span>

[<span data-ttu-id="ae762-128">新-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ae762-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="ae762-129">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ae762-129">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)