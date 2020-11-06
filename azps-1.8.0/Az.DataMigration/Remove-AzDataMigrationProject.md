---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: 53dc4841dbbdcb7f3d855630b69a94320b4dfeff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622470"
---
# <span data-ttu-id="00a88-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="00a88-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="00a88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00a88-102">SYNOPSIS</span></span>
<span data-ttu-id="00a88-103">從 Azure 移除 Azure 資料庫移轉服務專案。</span><span class="sxs-lookup"><span data-stu-id="00a88-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="00a88-104">句法</span><span class="sxs-lookup"><span data-stu-id="00a88-104">SYNTAX</span></span>

### <span data-ttu-id="00a88-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="00a88-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00a88-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00a88-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00a88-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00a88-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00a88-108">說明</span><span class="sxs-lookup"><span data-stu-id="00a88-108">DESCRIPTION</span></span>
<span data-ttu-id="00a88-109">Remove-AzDataMigrationProject Cmdlet 會從 Azure 中移除 Azure 資料庫移轉服務專案。</span><span class="sxs-lookup"><span data-stu-id="00a88-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="00a88-110">提供 DeleteRunningTask 參數時，會移除與所移除專案相關聯的所有 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="00a88-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="00a88-111">示例</span><span class="sxs-lookup"><span data-stu-id="00a88-111">EXAMPLES</span></span>

### <span data-ttu-id="00a88-112">範例1</span><span class="sxs-lookup"><span data-stu-id="00a88-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="00a88-113">上述範例會根據 name 作為輸入參數，從 Azure 中移除名為 myDMProject 的 Azure 資料庫移轉服務專案</span><span class="sxs-lookup"><span data-stu-id="00a88-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="00a88-114">範例2</span><span class="sxs-lookup"><span data-stu-id="00a88-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="00a88-115">上述範例會根據 PSProject 物件做為輸入參數，移除 Azure 資料庫移轉服務專案。</span><span class="sxs-lookup"><span data-stu-id="00a88-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="00a88-116">參數</span><span class="sxs-lookup"><span data-stu-id="00a88-116">PARAMETERS</span></span>

### <span data-ttu-id="00a88-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00a88-117">-DefaultProfile</span></span>
<span data-ttu-id="00a88-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="00a88-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00a88-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="00a88-119">-DeleteRunningTask</span></span>
<span data-ttu-id="00a88-120">刪除任何執行中的任務</span><span class="sxs-lookup"><span data-stu-id="00a88-120">Delete any running task</span></span>

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

### <span data-ttu-id="00a88-121">-Force</span><span class="sxs-lookup"><span data-stu-id="00a88-121">-Force</span></span>
<span data-ttu-id="00a88-122">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="00a88-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="00a88-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00a88-123">-InputObject</span></span>
<span data-ttu-id="00a88-124">PSProject 物件。</span><span class="sxs-lookup"><span data-stu-id="00a88-124">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00a88-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="00a88-125">-Name</span></span>
<span data-ttu-id="00a88-126">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="00a88-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00a88-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00a88-127">-PassThru</span></span>
<span data-ttu-id="00a88-128">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="00a88-128">Returns an true/false.</span></span>
<span data-ttu-id="00a88-129">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="00a88-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="00a88-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00a88-130">-ResourceGroupName</span></span>
<span data-ttu-id="00a88-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="00a88-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00a88-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00a88-132">-ResourceId</span></span>
<span data-ttu-id="00a88-133">[專案資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="00a88-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="00a88-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="00a88-134">-ServiceName</span></span>
<span data-ttu-id="00a88-135">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="00a88-135">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00a88-136">-確認</span><span class="sxs-lookup"><span data-stu-id="00a88-136">-Confirm</span></span>
<span data-ttu-id="00a88-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="00a88-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00a88-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00a88-138">-WhatIf</span></span>
<span data-ttu-id="00a88-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="00a88-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00a88-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="00a88-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00a88-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00a88-141">CommonParameters</span></span>
<span data-ttu-id="00a88-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00a88-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00a88-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="00a88-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00a88-144">輸入</span><span class="sxs-lookup"><span data-stu-id="00a88-144">INPUTS</span></span>

### <span data-ttu-id="00a88-145">PSProject 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="00a88-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="00a88-146">System.object</span><span class="sxs-lookup"><span data-stu-id="00a88-146">System.String</span></span>

## <span data-ttu-id="00a88-147">輸出</span><span class="sxs-lookup"><span data-stu-id="00a88-147">OUTPUTS</span></span>

### <span data-ttu-id="00a88-148">System.object</span><span class="sxs-lookup"><span data-stu-id="00a88-148">System.Boolean</span></span>

## <span data-ttu-id="00a88-149">筆記</span><span class="sxs-lookup"><span data-stu-id="00a88-149">NOTES</span></span>

## <span data-ttu-id="00a88-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="00a88-150">RELATED LINKS</span></span>