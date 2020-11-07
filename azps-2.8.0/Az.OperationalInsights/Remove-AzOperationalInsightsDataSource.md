---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: d8ec5eed1b6c955720822e28bf54da68e9aefcac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791755"
---
# <span data-ttu-id="f9954-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f9954-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="f9954-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9954-102">SYNOPSIS</span></span>
<span data-ttu-id="f9954-103">刪除資料來源。</span><span class="sxs-lookup"><span data-stu-id="f9954-103">Deletes a data source.</span></span>

## <span data-ttu-id="f9954-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9954-104">SYNTAX</span></span>

### <span data-ttu-id="f9954-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="f9954-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9954-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f9954-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9954-107">說明</span><span class="sxs-lookup"><span data-stu-id="f9954-107">DESCRIPTION</span></span>
<span data-ttu-id="f9954-108">**AzOperationalInsightsDataSource** Cmdlet 會刪除資料來源。</span><span class="sxs-lookup"><span data-stu-id="f9954-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="f9954-109">示例</span><span class="sxs-lookup"><span data-stu-id="f9954-109">EXAMPLES</span></span>

## <span data-ttu-id="f9954-110">參數</span><span class="sxs-lookup"><span data-stu-id="f9954-110">PARAMETERS</span></span>

### <span data-ttu-id="f9954-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9954-111">-DefaultProfile</span></span>
<span data-ttu-id="f9954-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f9954-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9954-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f9954-113">-Force</span></span>
<span data-ttu-id="f9954-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f9954-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f9954-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9954-115">-Name</span></span>
<span data-ttu-id="f9954-116">指定要刪除的資料來源名稱。</span><span class="sxs-lookup"><span data-stu-id="f9954-116">Specifies the name of a data source to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9954-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9954-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9954-118">指定包含電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9954-118">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9954-119">-工作區</span><span class="sxs-lookup"><span data-stu-id="f9954-119">-Workspace</span></span>
<span data-ttu-id="f9954-120">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="f9954-120">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9954-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f9954-121">-WorkspaceName</span></span>
<span data-ttu-id="f9954-122">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="f9954-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9954-123">-確認</span><span class="sxs-lookup"><span data-stu-id="f9954-123">-Confirm</span></span>
<span data-ttu-id="f9954-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f9954-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9954-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9954-125">-WhatIf</span></span>
<span data-ttu-id="f9954-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9954-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9954-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9954-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9954-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9954-128">CommonParameters</span></span>
<span data-ttu-id="f9954-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9954-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9954-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f9954-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9954-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f9954-131">INPUTS</span></span>

### <span data-ttu-id="f9954-132">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="f9954-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="f9954-133">System.object</span><span class="sxs-lookup"><span data-stu-id="f9954-133">System.String</span></span>

## <span data-ttu-id="f9954-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f9954-134">OUTPUTS</span></span>

### <span data-ttu-id="f9954-135">System.void</span><span class="sxs-lookup"><span data-stu-id="f9954-135">System.Void</span></span>

## <span data-ttu-id="f9954-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f9954-136">NOTES</span></span>
* <span data-ttu-id="f9954-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，作業，洞察力</span><span class="sxs-lookup"><span data-stu-id="f9954-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="f9954-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9954-138">RELATED LINKS</span></span>

[<span data-ttu-id="f9954-139">AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f9954-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="f9954-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f9954-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)

