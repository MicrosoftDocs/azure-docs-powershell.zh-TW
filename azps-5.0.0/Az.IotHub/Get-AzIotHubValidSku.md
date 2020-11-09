---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: e0f178c10fa74d8fa230472397d7bcc835f98bf4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141716"
---
# <span data-ttu-id="1cdf3-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="1cdf3-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="1cdf3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1cdf3-102">SYNOPSIS</span></span>
<span data-ttu-id="1cdf3-103">取得此 IotHub 可轉至的所有有效 sku。</span><span class="sxs-lookup"><span data-stu-id="1cdf3-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="1cdf3-104">句法</span><span class="sxs-lookup"><span data-stu-id="1cdf3-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1cdf3-105">說明</span><span class="sxs-lookup"><span data-stu-id="1cdf3-105">DESCRIPTION</span></span>
<span data-ttu-id="1cdf3-106">取得此 IotHub 可轉至的所有有效 sku。</span><span class="sxs-lookup"><span data-stu-id="1cdf3-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="1cdf3-107">IotHub 無法在免費和付費的 sku 之間轉換，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="1cdf3-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="1cdf3-108">如果您想要達到這個目的，您必須刪除並重新建立 iothub。</span><span class="sxs-lookup"><span data-stu-id="1cdf3-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="1cdf3-109">示例</span><span class="sxs-lookup"><span data-stu-id="1cdf3-109">EXAMPLES</span></span>

### <span data-ttu-id="1cdf3-110">範例1取得有效的 sku</span><span class="sxs-lookup"><span data-stu-id="1cdf3-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="1cdf3-111">取得名為 "myiothub" 的 IotHub 的所有 sku 清單</span><span class="sxs-lookup"><span data-stu-id="1cdf3-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="1cdf3-112">參數</span><span class="sxs-lookup"><span data-stu-id="1cdf3-112">PARAMETERS</span></span>

### <span data-ttu-id="1cdf3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cdf3-113">-DefaultProfile</span></span>
<span data-ttu-id="1cdf3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1cdf3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1cdf3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="1cdf3-115">-Name</span></span>
<span data-ttu-id="1cdf3-116">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="1cdf3-116">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cdf3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cdf3-117">-ResourceGroupName</span></span>
<span data-ttu-id="1cdf3-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="1cdf3-118">Resource Group Name</span></span>

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

### <span data-ttu-id="1cdf3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cdf3-119">CommonParameters</span></span>
<span data-ttu-id="1cdf3-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1cdf3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cdf3-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1cdf3-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cdf3-122">輸入</span><span class="sxs-lookup"><span data-stu-id="1cdf3-122">INPUTS</span></span>

### <span data-ttu-id="1cdf3-123">System.object</span><span class="sxs-lookup"><span data-stu-id="1cdf3-123">System.String</span></span>

## <span data-ttu-id="1cdf3-124">輸出</span><span class="sxs-lookup"><span data-stu-id="1cdf3-124">OUTPUTS</span></span>

### <span data-ttu-id="1cdf3-125">PSIotHubSkuDescription （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="1cdf3-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="1cdf3-126">筆記</span><span class="sxs-lookup"><span data-stu-id="1cdf3-126">NOTES</span></span>

## <span data-ttu-id="1cdf3-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="1cdf3-127">RELATED LINKS</span></span>