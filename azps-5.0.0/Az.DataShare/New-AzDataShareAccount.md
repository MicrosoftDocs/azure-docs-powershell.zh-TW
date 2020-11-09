---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: b24fe9e6587fe50a41d601c70c2687891bea2f16
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284894"
---
# <span data-ttu-id="8885d-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="8885d-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="8885d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8885d-102">SYNOPSIS</span></span>
<span data-ttu-id="8885d-103">建立新的資料共用帳戶</span><span class="sxs-lookup"><span data-stu-id="8885d-103">Creates new data share account</span></span>

## <span data-ttu-id="8885d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8885d-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8885d-105">說明</span><span class="sxs-lookup"><span data-stu-id="8885d-105">DESCRIPTION</span></span>
<span data-ttu-id="8885d-106">**AzDataShareAccount** Cmdlet 會在指定的 Azure 資源群組中建立 datashare 帳戶。</span><span class="sxs-lookup"><span data-stu-id="8885d-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="8885d-107">示例</span><span class="sxs-lookup"><span data-stu-id="8885d-107">EXAMPLES</span></span>

### <span data-ttu-id="8885d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8885d-108">Example 1</span></span>
```
PS C:\> New-AzDataShareAccount -ResourceGroupName "ADS" -Name "WikiADS" -Location "WestUS"
DataShareAccountName   : WikiADS
ResourceGroupName : ADS
Location          : WestUS
ProvisioningState : Succeeded
Tags              : {}
Identity          : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type              : Microsoft.DataShare/accounts
Id                : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="8885d-109">在資源群組 "ADS" 中建立名為 "WikiADS" 的帳戶</span><span class="sxs-lookup"><span data-stu-id="8885d-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="8885d-110">參數</span><span class="sxs-lookup"><span data-stu-id="8885d-110">PARAMETERS</span></span>

### <span data-ttu-id="8885d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8885d-111">-AsJob</span></span>
<span data-ttu-id="8885d-112">{{Fill AsJob 描述}}</span><span class="sxs-lookup"><span data-stu-id="8885d-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="8885d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8885d-113">-DefaultProfile</span></span>
<span data-ttu-id="8885d-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8885d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8885d-115">-位置</span><span class="sxs-lookup"><span data-stu-id="8885d-115">-Location</span></span>
<span data-ttu-id="8885d-116">建立資料共用帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="8885d-116">The location in which to create the data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8885d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="8885d-117">-Name</span></span>
<span data-ttu-id="8885d-118">Azure 資料共用帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8885d-118">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8885d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8885d-119">-ResourceGroupName</span></span>
<span data-ttu-id="8885d-120">將會在其中建立 azure 資料共用帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8885d-120">The resource group name of the azure data share account will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8885d-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="8885d-121">-Tag</span></span>
<span data-ttu-id="8885d-122">要與 azure 資料共用帳戶相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="8885d-122">The tags to associate with the azure data share account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8885d-123">-確認</span><span class="sxs-lookup"><span data-stu-id="8885d-123">-Confirm</span></span>
<span data-ttu-id="8885d-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8885d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8885d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8885d-125">-WhatIf</span></span>
<span data-ttu-id="8885d-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8885d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8885d-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8885d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8885d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8885d-128">CommonParameters</span></span>
<span data-ttu-id="8885d-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8885d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8885d-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8885d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8885d-131">輸入</span><span class="sxs-lookup"><span data-stu-id="8885d-131">INPUTS</span></span>

### <span data-ttu-id="8885d-132">所有</span><span class="sxs-lookup"><span data-stu-id="8885d-132">None</span></span>

## <span data-ttu-id="8885d-133">輸出</span><span class="sxs-lookup"><span data-stu-id="8885d-133">OUTPUTS</span></span>

### <span data-ttu-id="8885d-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="8885d-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="8885d-135">筆記</span><span class="sxs-lookup"><span data-stu-id="8885d-135">NOTES</span></span>

## <span data-ttu-id="8885d-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="8885d-136">RELATED LINKS</span></span>