---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285390"
---
# <span data-ttu-id="b9809-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="b9809-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="b9809-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9809-102">SYNOPSIS</span></span>
<span data-ttu-id="b9809-103">取得關聯性。</span><span class="sxs-lookup"><span data-stu-id="b9809-103">Get an association.</span></span>

## <span data-ttu-id="b9809-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9809-104">SYNTAX</span></span>

### <span data-ttu-id="b9809-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="b9809-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b9809-106">獲取</span><span class="sxs-lookup"><span data-stu-id="b9809-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9809-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b9809-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9809-108">說明</span><span class="sxs-lookup"><span data-stu-id="b9809-108">DESCRIPTION</span></span>
<span data-ttu-id="b9809-109">取得關聯性。</span><span class="sxs-lookup"><span data-stu-id="b9809-109">Get an association.</span></span>

## <span data-ttu-id="b9809-110">示例</span><span class="sxs-lookup"><span data-stu-id="b9809-110">EXAMPLES</span></span>

### <span data-ttu-id="b9809-111">範例1：清單自訂提供者關聯</span><span class="sxs-lookup"><span data-stu-id="b9809-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="b9809-112">列出指定範圍的所有自訂提供者關聯。</span><span class="sxs-lookup"><span data-stu-id="b9809-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="b9809-113">範例2：取得關聯</span><span class="sxs-lookup"><span data-stu-id="b9809-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="b9809-114">取得單一 CustomProvider 關聯的詳細資料</span><span class="sxs-lookup"><span data-stu-id="b9809-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="b9809-115">參數</span><span class="sxs-lookup"><span data-stu-id="b9809-115">PARAMETERS</span></span>

### <span data-ttu-id="b9809-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9809-116">-DefaultProfile</span></span>
<span data-ttu-id="b9809-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9809-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9809-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9809-118">-InputObject</span></span>
<span data-ttu-id="b9809-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b9809-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9809-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="b9809-120">-Name</span></span>
<span data-ttu-id="b9809-121">關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9809-121">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9809-122">-範圍</span><span class="sxs-lookup"><span data-stu-id="b9809-122">-Scope</span></span>
<span data-ttu-id="b9809-123">關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="b9809-123">The scope of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9809-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9809-124">CommonParameters</span></span>
<span data-ttu-id="b9809-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9809-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9809-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b9809-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9809-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b9809-127">INPUTS</span></span>

### <span data-ttu-id="b9809-128">ICustomProvidersIdentity （CustomProviders）的</span><span class="sxs-lookup"><span data-stu-id="b9809-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="b9809-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b9809-129">OUTPUTS</span></span>

### <span data-ttu-id="b9809-130">IAssociation （CustomProviders）。 Api20180901Preview。</span><span class="sxs-lookup"><span data-stu-id="b9809-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="b9809-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b9809-131">NOTES</span></span>

<span data-ttu-id="b9809-132">別名</span><span class="sxs-lookup"><span data-stu-id="b9809-132">ALIASES</span></span>

<span data-ttu-id="b9809-133">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b9809-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b9809-134">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b9809-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b9809-135">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b9809-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b9809-136">INPUTOBJECT <ICustomProvidersIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b9809-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b9809-137">`[AssociationName <String>]`：關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9809-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="b9809-138">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b9809-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b9809-139">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9809-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b9809-140">`[ResourceProviderName <String>]`：資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9809-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="b9809-141">`[Scope <String>]`：關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="b9809-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="b9809-142">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="b9809-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="b9809-143">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="b9809-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="b9809-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9809-144">RELATED LINKS</span></span>
