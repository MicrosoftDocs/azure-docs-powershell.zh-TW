---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: f48007be3e1209cff65e46c669bce46298182247
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288139"
---
# <span data-ttu-id="d5e55-101">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="d5e55-101">Enable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="d5e55-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5e55-102">SYNOPSIS</span></span>
<span data-ttu-id="d5e55-103">從工作區中的電腦開始收集 IIS 記錄。</span><span class="sxs-lookup"><span data-stu-id="d5e55-103">Starts collection of IIS logs from computers in a workspace.</span></span>

## <span data-ttu-id="d5e55-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5e55-104">SYNTAX</span></span>

### <span data-ttu-id="d5e55-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="d5e55-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5e55-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d5e55-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5e55-107">說明</span><span class="sxs-lookup"><span data-stu-id="d5e55-107">DESCRIPTION</span></span>
<span data-ttu-id="d5e55-108">**Enable-AzOperationalInsightsIISLogCollection** Cmdlet 會開始收集網際網路資訊服務 (IIS) 記錄從工作區中的連線電腦。</span><span class="sxs-lookup"><span data-stu-id="d5e55-108">The **Enable-AzOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="d5e55-109">示例</span><span class="sxs-lookup"><span data-stu-id="d5e55-109">EXAMPLES</span></span>

## <span data-ttu-id="d5e55-110">參數</span><span class="sxs-lookup"><span data-stu-id="d5e55-110">PARAMETERS</span></span>

### <span data-ttu-id="d5e55-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5e55-111">-DefaultProfile</span></span>
<span data-ttu-id="d5e55-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d5e55-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5e55-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5e55-113">-ResourceGroupName</span></span>
<span data-ttu-id="d5e55-114">指定包含電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5e55-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="d5e55-115">-工作區</span><span class="sxs-lookup"><span data-stu-id="d5e55-115">-Workspace</span></span>
<span data-ttu-id="d5e55-116">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="d5e55-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d5e55-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d5e55-117">-WorkspaceName</span></span>
<span data-ttu-id="d5e55-118">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="d5e55-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d5e55-119">-確認</span><span class="sxs-lookup"><span data-stu-id="d5e55-119">-Confirm</span></span>
<span data-ttu-id="d5e55-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d5e55-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5e55-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5e55-121">-WhatIf</span></span>
<span data-ttu-id="d5e55-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d5e55-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5e55-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5e55-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5e55-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5e55-124">CommonParameters</span></span>
<span data-ttu-id="d5e55-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5e55-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5e55-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d5e55-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5e55-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d5e55-127">INPUTS</span></span>

### <span data-ttu-id="d5e55-128">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="d5e55-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d5e55-129">System.object</span><span class="sxs-lookup"><span data-stu-id="d5e55-129">System.String</span></span>

## <span data-ttu-id="d5e55-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d5e55-130">OUTPUTS</span></span>

### <span data-ttu-id="d5e55-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d5e55-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d5e55-132">筆記</span><span class="sxs-lookup"><span data-stu-id="d5e55-132">NOTES</span></span>

## <span data-ttu-id="d5e55-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5e55-133">RELATED LINKS</span></span>

[<span data-ttu-id="d5e55-134">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="d5e55-134">Disable-AzOperationalInsightsIISLogCollection</span></span>](./Disable-AzOperationalInsightsIISLogCollection.md)

