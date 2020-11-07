---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 079ff61475405407fc2f6864d9fda43b1a5fc4cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787946"
---
# <span data-ttu-id="39b7e-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="39b7e-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="39b7e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="39b7e-103">取得指定資料 Lake Store 中指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="39b7e-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="39b7e-104">如果未指定虛擬網路規則，則會列出該帳戶的所有虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="39b7e-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="39b7e-105">句法</span><span class="sxs-lookup"><span data-stu-id="39b7e-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39b7e-106">說明</span><span class="sxs-lookup"><span data-stu-id="39b7e-106">DESCRIPTION</span></span>
<span data-ttu-id="39b7e-107">Get-AzDataLakeStoreVirtualNetworkRule Cmdlet 會在指定的 Data Lake Store 中取得指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="39b7e-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="39b7e-108">如果未指定虛擬網路規則，則會列出該帳戶的所有虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="39b7e-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="39b7e-109">示例</span><span class="sxs-lookup"><span data-stu-id="39b7e-109">EXAMPLES</span></span>

### <span data-ttu-id="39b7e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="39b7e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="39b7e-111">從帳戶 "dls" 傳回名為 "myVNET" 的虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="39b7e-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="39b7e-112">參數</span><span class="sxs-lookup"><span data-stu-id="39b7e-112">PARAMETERS</span></span>

### <span data-ttu-id="39b7e-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="39b7e-113">-Account</span></span>
<span data-ttu-id="39b7e-114">要從中取得虛擬網路規則的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="39b7e-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="39b7e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39b7e-115">-DefaultProfile</span></span>
<span data-ttu-id="39b7e-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39b7e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39b7e-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="39b7e-117">-Name</span></span>
<span data-ttu-id="39b7e-118">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="39b7e-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="39b7e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b7e-119">CommonParameters</span></span>
<span data-ttu-id="39b7e-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39b7e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b7e-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="39b7e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b7e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="39b7e-122">INPUTS</span></span>

### <span data-ttu-id="39b7e-123">System.object</span><span class="sxs-lookup"><span data-stu-id="39b7e-123">System.String</span></span>

## <span data-ttu-id="39b7e-124">輸出</span><span class="sxs-lookup"><span data-stu-id="39b7e-124">OUTPUTS</span></span>

### <span data-ttu-id="39b7e-125">DataLakeStoreVirtualNetworkRule 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="39b7e-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="39b7e-126">筆記</span><span class="sxs-lookup"><span data-stu-id="39b7e-126">NOTES</span></span>

## <span data-ttu-id="39b7e-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="39b7e-127">RELATED LINKS</span></span>