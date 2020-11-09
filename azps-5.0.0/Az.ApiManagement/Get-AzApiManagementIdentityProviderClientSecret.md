---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: d75d385bc158e0855601d3432dff79b2e4339f2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285704"
---
# <span data-ttu-id="17ac5-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="17ac5-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="17ac5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17ac5-102">SYNOPSIS</span></span>
<span data-ttu-id="17ac5-103">取得身分識別提供者的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="17ac5-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="17ac5-104">句法</span><span class="sxs-lookup"><span data-stu-id="17ac5-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17ac5-105">說明</span><span class="sxs-lookup"><span data-stu-id="17ac5-105">DESCRIPTION</span></span>
<span data-ttu-id="17ac5-106">取得身分識別提供者的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="17ac5-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="17ac5-107">示例</span><span class="sxs-lookup"><span data-stu-id="17ac5-107">EXAMPLES</span></span>

### <span data-ttu-id="17ac5-108">範例1：取得 AAD 類型身分識別提供者的用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="17ac5-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="17ac5-109">取得 Azure Active Directory 之身分識別提供者設定的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="17ac5-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="17ac5-110">參數</span><span class="sxs-lookup"><span data-stu-id="17ac5-110">PARAMETERS</span></span>

### <span data-ttu-id="17ac5-111">-內容</span><span class="sxs-lookup"><span data-stu-id="17ac5-111">-Context</span></span>
<span data-ttu-id="17ac5-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="17ac5-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="17ac5-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="17ac5-113">This parameter is required.</span></span>

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

### <span data-ttu-id="17ac5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17ac5-114">-DefaultProfile</span></span>
<span data-ttu-id="17ac5-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="17ac5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17ac5-116">-類型</span><span class="sxs-lookup"><span data-stu-id="17ac5-116">-Type</span></span>
<span data-ttu-id="17ac5-117">身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="17ac5-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="17ac5-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="17ac5-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17ac5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17ac5-119">CommonParameters</span></span>
<span data-ttu-id="17ac5-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17ac5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17ac5-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="17ac5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17ac5-122">輸入</span><span class="sxs-lookup"><span data-stu-id="17ac5-122">INPUTS</span></span>

### <span data-ttu-id="17ac5-123">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="17ac5-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="17ac5-124">ServiceManagement. PsApiManagementIdentityProviderType （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="17ac5-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="17ac5-125">輸出</span><span class="sxs-lookup"><span data-stu-id="17ac5-125">OUTPUTS</span></span>

### <span data-ttu-id="17ac5-126">ServiceManagement. PsApiManagementClientSecret （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="17ac5-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="17ac5-127">筆記</span><span class="sxs-lookup"><span data-stu-id="17ac5-127">NOTES</span></span>

## <span data-ttu-id="17ac5-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="17ac5-128">RELATED LINKS</span></span>