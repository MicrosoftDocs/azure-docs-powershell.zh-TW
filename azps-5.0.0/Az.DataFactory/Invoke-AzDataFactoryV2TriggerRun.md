---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: af0fcf4e96d919c2c52a2ab30e583f288d20fc4e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285224"
---
# <span data-ttu-id="7eb1e-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="7eb1e-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="7eb1e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7eb1e-102">SYNOPSIS</span></span>
 <span data-ttu-id="7eb1e-103">會調用觸發程式執行的另一個實例。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="7eb1e-104">句法</span><span class="sxs-lookup"><span data-stu-id="7eb1e-104">SYNTAX</span></span>

### <span data-ttu-id="7eb1e-105">ByFactoryNameByParameterFile (預設) </span><span class="sxs-lookup"><span data-stu-id="7eb1e-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7eb1e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7eb1e-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eb1e-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="7eb1e-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eb1e-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7eb1e-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7eb1e-109">說明</span><span class="sxs-lookup"><span data-stu-id="7eb1e-109">DESCRIPTION</span></span>
<span data-ttu-id="7eb1e-110">**AzDataFactoryV2TriggerRun** 命令會以新的觸發程式執行 id 啟動觸發程式執行的另一個實例。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="7eb1e-111">示例</span><span class="sxs-lookup"><span data-stu-id="7eb1e-111">EXAMPLES</span></span>

### <span data-ttu-id="7eb1e-112">範例1</span><span class="sxs-lookup"><span data-stu-id="7eb1e-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="7eb1e-113">啟動另一個含有新的觸發程式執行 id 的觸發程式實例，並在原始觸發程式執行時保持相同的 windowStartTime 和 windowEndTime。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="7eb1e-114">參數</span><span class="sxs-lookup"><span data-stu-id="7eb1e-114">PARAMETERS</span></span>

### <span data-ttu-id="7eb1e-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7eb1e-115">-DataFactory</span></span>
<span data-ttu-id="7eb1e-116">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-116">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb1e-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7eb1e-117">-DataFactoryName</span></span>
<span data-ttu-id="7eb1e-118">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-118">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb1e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb1e-119">-DefaultProfile</span></span>
<span data-ttu-id="7eb1e-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eb1e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7eb1e-121">-InputObject</span></span>
<span data-ttu-id="7eb1e-122">觸發程式執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-122">The information about the trigger run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb1e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7eb1e-123">-PassThru</span></span>
<span data-ttu-id="7eb1e-124">如果已指定，則在 case 操作成功時，此 Cmdlet 會寫入 true。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="7eb1e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb1e-125">-ResourceGroupName</span></span>
<span data-ttu-id="7eb1e-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb1e-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="7eb1e-127">-TriggerName</span></span>
<span data-ttu-id="7eb1e-128">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-128">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb1e-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="7eb1e-129">-TriggerRunId</span></span>
<span data-ttu-id="7eb1e-130">觸發程式的 [執行識別碼]。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-130">The Run ID of the trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb1e-131">-確認</span><span class="sxs-lookup"><span data-stu-id="7eb1e-131">-Confirm</span></span>
<span data-ttu-id="7eb1e-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eb1e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eb1e-133">-WhatIf</span></span>
<span data-ttu-id="7eb1e-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eb1e-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eb1e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb1e-136">CommonParameters</span></span>
<span data-ttu-id="7eb1e-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb1e-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb1e-139">輸入</span><span class="sxs-lookup"><span data-stu-id="7eb1e-139">INPUTS</span></span>

### <span data-ttu-id="7eb1e-140">PSTriggerRun 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="7eb1e-141">System.object</span><span class="sxs-lookup"><span data-stu-id="7eb1e-141">System.String</span></span>

### <span data-ttu-id="7eb1e-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7eb1e-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="7eb1e-143">輸出</span><span class="sxs-lookup"><span data-stu-id="7eb1e-143">OUTPUTS</span></span>

### <span data-ttu-id="7eb1e-144">PSPipeline 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="7eb1e-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="7eb1e-145">筆記</span><span class="sxs-lookup"><span data-stu-id="7eb1e-145">NOTES</span></span>

## <span data-ttu-id="7eb1e-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="7eb1e-146">RELATED LINKS</span></span>