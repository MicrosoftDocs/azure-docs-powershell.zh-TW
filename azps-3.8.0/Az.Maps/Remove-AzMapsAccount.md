---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: b84a5d6cbbf090243a63ad9919a3fbb1977d77f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956848"
---
# <span data-ttu-id="73ce4-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="73ce4-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="73ce4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="73ce4-103">刪除 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="73ce4-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="73ce4-104">句法</span><span class="sxs-lookup"><span data-stu-id="73ce4-104">SYNTAX</span></span>

### <span data-ttu-id="73ce4-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="73ce4-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73ce4-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73ce4-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73ce4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73ce4-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73ce4-108">說明</span><span class="sxs-lookup"><span data-stu-id="73ce4-108">DESCRIPTION</span></span>
<span data-ttu-id="73ce4-109">Remove-AzMapsAccount Cmdlet 會刪除指定的 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="73ce4-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="73ce4-110">示例</span><span class="sxs-lookup"><span data-stu-id="73ce4-110">EXAMPLES</span></span>

### <span data-ttu-id="73ce4-111">範例1</span><span class="sxs-lookup"><span data-stu-id="73ce4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="73ce4-112">從 [資源群組] MyResourceGroup 刪除帳戶我的帳戶。</span><span class="sxs-lookup"><span data-stu-id="73ce4-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="73ce4-113">範例2</span><span class="sxs-lookup"><span data-stu-id="73ce4-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="73ce4-114">刪除指定的 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="73ce4-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="73ce4-115">參數</span><span class="sxs-lookup"><span data-stu-id="73ce4-115">PARAMETERS</span></span>

### <span data-ttu-id="73ce4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73ce4-116">-DefaultProfile</span></span>
<span data-ttu-id="73ce4-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="73ce4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73ce4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73ce4-118">-InputObject</span></span>
<span data-ttu-id="73ce4-119">從 AzMapsAccount 將 [地圖] 帳戶成管道。</span><span class="sxs-lookup"><span data-stu-id="73ce4-119">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73ce4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="73ce4-120">-Name</span></span>
<span data-ttu-id="73ce4-121">地圖帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="73ce4-121">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73ce4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73ce4-122">-PassThru</span></span>
<span data-ttu-id="73ce4-123">返回是否已成功刪除指定的帳號。</span><span class="sxs-lookup"><span data-stu-id="73ce4-123">Return whether the specified account was successfully deleted or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ce4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73ce4-124">-ResourceGroupName</span></span>
<span data-ttu-id="73ce4-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="73ce4-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73ce4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73ce4-126">-ResourceId</span></span>
<span data-ttu-id="73ce4-127">地圖帳戶 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="73ce4-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73ce4-128">-確認</span><span class="sxs-lookup"><span data-stu-id="73ce4-128">-Confirm</span></span>
<span data-ttu-id="73ce4-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="73ce4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73ce4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73ce4-130">-WhatIf</span></span>
<span data-ttu-id="73ce4-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="73ce4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73ce4-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73ce4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73ce4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ce4-133">CommonParameters</span></span>
<span data-ttu-id="73ce4-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73ce4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ce4-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="73ce4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ce4-136">輸入</span><span class="sxs-lookup"><span data-stu-id="73ce4-136">INPUTS</span></span>

### <span data-ttu-id="73ce4-137">System.object</span><span class="sxs-lookup"><span data-stu-id="73ce4-137">System.String</span></span>

### <span data-ttu-id="73ce4-138">PSMapsAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="73ce4-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="73ce4-139">輸出</span><span class="sxs-lookup"><span data-stu-id="73ce4-139">OUTPUTS</span></span>

### <span data-ttu-id="73ce4-140">System.object</span><span class="sxs-lookup"><span data-stu-id="73ce4-140">System.Boolean</span></span>

## <span data-ttu-id="73ce4-141">筆記</span><span class="sxs-lookup"><span data-stu-id="73ce4-141">NOTES</span></span>

## <span data-ttu-id="73ce4-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="73ce4-142">RELATED LINKS</span></span>