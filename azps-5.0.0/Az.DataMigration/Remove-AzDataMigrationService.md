---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 2ba182833fc1d4c59d9164b6db5d68bcd3c499f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284938"
---
# <span data-ttu-id="c60c6-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="c60c6-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="c60c6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c60c6-102">SYNOPSIS</span></span>
<span data-ttu-id="c60c6-103">從 Azure 移除 Azure 資料庫移轉服務的實例。</span><span class="sxs-lookup"><span data-stu-id="c60c6-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="c60c6-104">句法</span><span class="sxs-lookup"><span data-stu-id="c60c6-104">SYNTAX</span></span>

### <span data-ttu-id="c60c6-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c60c6-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c60c6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c60c6-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c60c6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c60c6-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c60c6-108">說明</span><span class="sxs-lookup"><span data-stu-id="c60c6-108">DESCRIPTION</span></span>
<span data-ttu-id="c60c6-109">Remove-AzDataMigrationService Cmdlet 會從 Azure 中移除 Azure 資料庫移轉服務的實例。</span><span class="sxs-lookup"><span data-stu-id="c60c6-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="c60c6-110">提供 DeleteRunningTask 參數會移除與移除之服務相關聯的所有 Azure 資料庫移轉服務工作。</span><span class="sxs-lookup"><span data-stu-id="c60c6-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="c60c6-111">示例</span><span class="sxs-lookup"><span data-stu-id="c60c6-111">EXAMPLES</span></span>

### <span data-ttu-id="c60c6-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c60c6-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="c60c6-113">上述範例會移除名為 [MyResourceGroup] 的 Azure 資源群組中包含的名為 TestService 的 Azure 資料庫移轉服務實例。</span><span class="sxs-lookup"><span data-stu-id="c60c6-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="c60c6-114">參數</span><span class="sxs-lookup"><span data-stu-id="c60c6-114">PARAMETERS</span></span>

### <span data-ttu-id="c60c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c60c6-115">-DefaultProfile</span></span>
<span data-ttu-id="c60c6-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c60c6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c60c6-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="c60c6-117">-DeleteRunningTask</span></span>
<span data-ttu-id="c60c6-118">刪除任何執行中的任務</span><span class="sxs-lookup"><span data-stu-id="c60c6-118">Delete any running task</span></span>

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

### <span data-ttu-id="c60c6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c60c6-119">-Force</span></span>
<span data-ttu-id="c60c6-120">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="c60c6-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c60c6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c60c6-121">-InputObject</span></span>
<span data-ttu-id="c60c6-122">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="c60c6-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c60c6-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="c60c6-123">-Name</span></span>
<span data-ttu-id="c60c6-124">資料庫移轉服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="c60c6-124">The name of the Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c60c6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c60c6-125">-PassThru</span></span>
<span data-ttu-id="c60c6-126">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="c60c6-126">Returns an true/false.</span></span>
<span data-ttu-id="c60c6-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c60c6-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c60c6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c60c6-128">-ResourceGroupName</span></span>
<span data-ttu-id="c60c6-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c60c6-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="c60c6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c60c6-130">-ResourceId</span></span>
<span data-ttu-id="c60c6-131">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c60c6-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="c60c6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="c60c6-132">-Confirm</span></span>
<span data-ttu-id="c60c6-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c60c6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c60c6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c60c6-134">-WhatIf</span></span>
<span data-ttu-id="c60c6-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c60c6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c60c6-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c60c6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c60c6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c60c6-137">CommonParameters</span></span>
<span data-ttu-id="c60c6-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c60c6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c60c6-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c60c6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c60c6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c60c6-140">INPUTS</span></span>

### <span data-ttu-id="c60c6-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="c60c6-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="c60c6-142">System.object</span><span class="sxs-lookup"><span data-stu-id="c60c6-142">System.String</span></span>

## <span data-ttu-id="c60c6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c60c6-143">OUTPUTS</span></span>

### <span data-ttu-id="c60c6-144">System.object</span><span class="sxs-lookup"><span data-stu-id="c60c6-144">System.Boolean</span></span>

## <span data-ttu-id="c60c6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="c60c6-145">NOTES</span></span>

## <span data-ttu-id="c60c6-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="c60c6-146">RELATED LINKS</span></span>