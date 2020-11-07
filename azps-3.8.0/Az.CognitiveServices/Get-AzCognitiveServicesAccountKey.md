---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 8150abc726f990b699237dbaad3641a99bae2e2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956259"
---
# <span data-ttu-id="e8eea-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e8eea-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="e8eea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8eea-102">SYNOPSIS</span></span>
<span data-ttu-id="e8eea-103">取得帳戶的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="e8eea-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="e8eea-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8eea-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8eea-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8eea-105">DESCRIPTION</span></span>
<span data-ttu-id="e8eea-106">**AzCognitiveServicesAccountKey** Cmdlet 會取得已預配的認知服務帳戶的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="e8eea-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="e8eea-107">認知服務帳戶有兩個 API 金鑰： Key1 和 Key2。</span><span class="sxs-lookup"><span data-stu-id="e8eea-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="e8eea-108">金鑰可讓您與認知服務帳戶端點互動。</span><span class="sxs-lookup"><span data-stu-id="e8eea-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="e8eea-109">使用 New-AzCognitiveServicesAccountKey 重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="e8eea-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="e8eea-110">示例</span><span class="sxs-lookup"><span data-stu-id="e8eea-110">EXAMPLES</span></span>

### <span data-ttu-id="e8eea-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e8eea-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="e8eea-112">參數</span><span class="sxs-lookup"><span data-stu-id="e8eea-112">PARAMETERS</span></span>

### <span data-ttu-id="e8eea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8eea-113">-DefaultProfile</span></span>
<span data-ttu-id="e8eea-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e8eea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8eea-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8eea-115">-Name</span></span>
<span data-ttu-id="e8eea-116">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8eea-116">Specifies the name of the account.</span></span>
<span data-ttu-id="e8eea-117">這個 Cmdlet 會取得這個帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="e8eea-117">This cmdlet gets the keys for this account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8eea-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8eea-118">-ResourceGroupName</span></span>
<span data-ttu-id="e8eea-119">指定將帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8eea-119">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8eea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8eea-120">CommonParameters</span></span>
<span data-ttu-id="e8eea-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8eea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8eea-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8eea-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8eea-123">輸入</span><span class="sxs-lookup"><span data-stu-id="e8eea-123">INPUTS</span></span>

### <span data-ttu-id="e8eea-124">System.object</span><span class="sxs-lookup"><span data-stu-id="e8eea-124">System.String</span></span>

## <span data-ttu-id="e8eea-125">輸出</span><span class="sxs-lookup"><span data-stu-id="e8eea-125">OUTPUTS</span></span>

### <span data-ttu-id="e8eea-126">PSCognitiveServicesAccountKeys （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="e8eea-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="e8eea-127">筆記</span><span class="sxs-lookup"><span data-stu-id="e8eea-127">NOTES</span></span>

## <span data-ttu-id="e8eea-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8eea-128">RELATED LINKS</span></span>

[<span data-ttu-id="e8eea-129">新-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e8eea-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)

