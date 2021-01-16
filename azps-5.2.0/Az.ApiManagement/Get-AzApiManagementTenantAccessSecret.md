---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: ec64a339c29facdbb940b8141c72222ff932c1bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275556"
---
# <span data-ttu-id="cf8fd-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="cf8fd-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="cf8fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf8fd-102">SYNOPSIS</span></span>
<span data-ttu-id="cf8fd-103">取得租使用者的存取設定鍵。</span><span class="sxs-lookup"><span data-stu-id="cf8fd-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="cf8fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf8fd-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf8fd-105">說明</span><span class="sxs-lookup"><span data-stu-id="cf8fd-105">DESCRIPTION</span></span>
<span data-ttu-id="cf8fd-106">取得租使用者的存取設定鍵。</span><span class="sxs-lookup"><span data-stu-id="cf8fd-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="cf8fd-107">示例</span><span class="sxs-lookup"><span data-stu-id="cf8fd-107">EXAMPLES</span></span>

### <span data-ttu-id="cf8fd-108">範例1：取得租使用者存取設定金鑰</span><span class="sxs-lookup"><span data-stu-id="cf8fd-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="cf8fd-109">這個命令會取得指定內容的租使用者存取設定鍵。</span><span class="sxs-lookup"><span data-stu-id="cf8fd-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="cf8fd-110">參數</span><span class="sxs-lookup"><span data-stu-id="cf8fd-110">PARAMETERS</span></span>

### <span data-ttu-id="cf8fd-111">-內容</span><span class="sxs-lookup"><span data-stu-id="cf8fd-111">-Context</span></span>
<span data-ttu-id="cf8fd-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="cf8fd-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cf8fd-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="cf8fd-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf8fd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf8fd-114">-DefaultProfile</span></span>
<span data-ttu-id="cf8fd-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf8fd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf8fd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf8fd-116">CommonParameters</span></span>
<span data-ttu-id="cf8fd-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf8fd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf8fd-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cf8fd-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf8fd-119">輸入</span><span class="sxs-lookup"><span data-stu-id="cf8fd-119">INPUTS</span></span>

### <span data-ttu-id="cf8fd-120">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="cf8fd-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="cf8fd-121">輸出</span><span class="sxs-lookup"><span data-stu-id="cf8fd-121">OUTPUTS</span></span>

### <span data-ttu-id="cf8fd-122">ServiceManagement. PsApiManagementAccessInformation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="cf8fd-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="cf8fd-123">筆記</span><span class="sxs-lookup"><span data-stu-id="cf8fd-123">NOTES</span></span>

## <span data-ttu-id="cf8fd-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf8fd-124">RELATED LINKS</span></span>