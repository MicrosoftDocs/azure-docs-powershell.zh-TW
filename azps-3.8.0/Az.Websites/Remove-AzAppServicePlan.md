---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: dfd2cfd20ab11e2e70e03dc3e166c83729ef344a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956673"
---
# <span data-ttu-id="92cc0-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="92cc0-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="92cc0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="92cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="92cc0-103">移除 Azure 應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="92cc0-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="92cc0-104">句法</span><span class="sxs-lookup"><span data-stu-id="92cc0-104">SYNTAX</span></span>

### <span data-ttu-id="92cc0-105">S1</span><span class="sxs-lookup"><span data-stu-id="92cc0-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92cc0-106">S2</span><span class="sxs-lookup"><span data-stu-id="92cc0-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92cc0-107">說明</span><span class="sxs-lookup"><span data-stu-id="92cc0-107">DESCRIPTION</span></span>
<span data-ttu-id="92cc0-108">**AzAppServicePlan** Cmdlet 會移除 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="92cc0-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="92cc0-109">示例</span><span class="sxs-lookup"><span data-stu-id="92cc0-109">EXAMPLES</span></span>

### <span data-ttu-id="92cc0-110">範例1：移除 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="92cc0-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="92cc0-111">這個命令會從屬於名為「預設-Web-WestUS」的資源群組中，移除名為 ContosoASP 的 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="92cc0-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="92cc0-112">參數</span><span class="sxs-lookup"><span data-stu-id="92cc0-112">PARAMETERS</span></span>

### <span data-ttu-id="92cc0-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="92cc0-113">-AppServicePlan</span></span>
<span data-ttu-id="92cc0-114">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="92cc0-114">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92cc0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92cc0-115">-AsJob</span></span>
<span data-ttu-id="92cc0-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="92cc0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92cc0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92cc0-117">-DefaultProfile</span></span>
<span data-ttu-id="92cc0-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="92cc0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92cc0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="92cc0-119">-Force</span></span>
<span data-ttu-id="92cc0-120">[強制移除] 選項</span><span class="sxs-lookup"><span data-stu-id="92cc0-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="92cc0-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="92cc0-121">-Name</span></span>
<span data-ttu-id="92cc0-122">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="92cc0-122">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92cc0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92cc0-123">-ResourceGroupName</span></span>
<span data-ttu-id="92cc0-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="92cc0-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92cc0-125">-確認</span><span class="sxs-lookup"><span data-stu-id="92cc0-125">-Confirm</span></span>
<span data-ttu-id="92cc0-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="92cc0-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92cc0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92cc0-127">-WhatIf</span></span>
<span data-ttu-id="92cc0-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="92cc0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92cc0-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92cc0-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92cc0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92cc0-130">CommonParameters</span></span>
<span data-ttu-id="92cc0-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="92cc0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92cc0-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="92cc0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92cc0-133">輸入</span><span class="sxs-lookup"><span data-stu-id="92cc0-133">INPUTS</span></span>

### <span data-ttu-id="92cc0-134">WebApps WebApp. PSAppServicePlan （）</span><span class="sxs-lookup"><span data-stu-id="92cc0-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="92cc0-135">輸出</span><span class="sxs-lookup"><span data-stu-id="92cc0-135">OUTPUTS</span></span>

### <span data-ttu-id="92cc0-136">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="92cc0-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="92cc0-137">筆記</span><span class="sxs-lookup"><span data-stu-id="92cc0-137">NOTES</span></span>

## <span data-ttu-id="92cc0-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="92cc0-138">RELATED LINKS</span></span>

[<span data-ttu-id="92cc0-139">AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="92cc0-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="92cc0-140">新-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="92cc0-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="92cc0-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="92cc0-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)

