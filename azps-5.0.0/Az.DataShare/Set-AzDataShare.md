---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: 69d44ea88b34aba027933cb3015a203bf06070fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284859"
---
# <span data-ttu-id="66cc2-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="66cc2-101">Set-AzDataShare</span></span>

## <span data-ttu-id="66cc2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="66cc2-103">更新現有的資料共用</span><span class="sxs-lookup"><span data-stu-id="66cc2-103">Updates an existing data share</span></span>

## <span data-ttu-id="66cc2-104">句法</span><span class="sxs-lookup"><span data-stu-id="66cc2-104">SYNTAX</span></span>

### <span data-ttu-id="66cc2-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="66cc2-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66cc2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66cc2-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66cc2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66cc2-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66cc2-108">說明</span><span class="sxs-lookup"><span data-stu-id="66cc2-108">DESCRIPTION</span></span>
<span data-ttu-id="66cc2-109">**AzDataShare** Cmdlet 會更新在指定的 azure 資料共用帳戶中存在的資料共用。</span><span class="sxs-lookup"><span data-stu-id="66cc2-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="66cc2-110">示例</span><span class="sxs-lookup"><span data-stu-id="66cc2-110">EXAMPLES</span></span>

### <span data-ttu-id="66cc2-111">範例1</span><span class="sxs-lookup"><span data-stu-id="66cc2-111">Example 1</span></span>
```
PS C:\> Set-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -Description "Updated description" -TermsOfUse "Updated terms"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Updated description
ProvisioningState   : Succeeded
Terms               : Updated terms
```

<span data-ttu-id="66cc2-112">這個命令會更新一個名為 AdsShare 的現有資料共用</span><span class="sxs-lookup"><span data-stu-id="66cc2-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="66cc2-113">參數</span><span class="sxs-lookup"><span data-stu-id="66cc2-113">PARAMETERS</span></span>

### <span data-ttu-id="66cc2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="66cc2-114">-AccountName</span></span>
<span data-ttu-id="66cc2-115">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="66cc2-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66cc2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66cc2-116">-DefaultProfile</span></span>
<span data-ttu-id="66cc2-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66cc2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66cc2-118">-描述</span><span class="sxs-lookup"><span data-stu-id="66cc2-118">-Description</span></span>
<span data-ttu-id="66cc2-119">資料共用的描述</span><span class="sxs-lookup"><span data-stu-id="66cc2-119">Description of Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66cc2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66cc2-120">-InputObject</span></span>
<span data-ttu-id="66cc2-121">Azure data share 物件</span><span class="sxs-lookup"><span data-stu-id="66cc2-121">Azure data share object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66cc2-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="66cc2-122">-Name</span></span>
<span data-ttu-id="66cc2-123">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="66cc2-123">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66cc2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66cc2-124">-ResourceGroupName</span></span>
<span data-ttu-id="66cc2-125">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="66cc2-125">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66cc2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66cc2-126">-ResourceId</span></span>
<span data-ttu-id="66cc2-127">Azure 資料共用的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="66cc2-127">The resource id of the azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66cc2-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="66cc2-128">-TermsOfUse</span></span>
<span data-ttu-id="66cc2-129">資料共用的使用條款</span><span class="sxs-lookup"><span data-stu-id="66cc2-129">Terms of Use for Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66cc2-130">-確認</span><span class="sxs-lookup"><span data-stu-id="66cc2-130">-Confirm</span></span>
<span data-ttu-id="66cc2-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="66cc2-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66cc2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66cc2-132">-WhatIf</span></span>
<span data-ttu-id="66cc2-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66cc2-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66cc2-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66cc2-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66cc2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66cc2-135">CommonParameters</span></span>
<span data-ttu-id="66cc2-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66cc2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66cc2-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="66cc2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66cc2-138">輸入</span><span class="sxs-lookup"><span data-stu-id="66cc2-138">INPUTS</span></span>

### <span data-ttu-id="66cc2-139">System.object</span><span class="sxs-lookup"><span data-stu-id="66cc2-139">System.String</span></span>

### <span data-ttu-id="66cc2-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="66cc2-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="66cc2-141">輸出</span><span class="sxs-lookup"><span data-stu-id="66cc2-141">OUTPUTS</span></span>

### <span data-ttu-id="66cc2-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="66cc2-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="66cc2-143">筆記</span><span class="sxs-lookup"><span data-stu-id="66cc2-143">NOTES</span></span>

## <span data-ttu-id="66cc2-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="66cc2-144">RELATED LINKS</span></span>