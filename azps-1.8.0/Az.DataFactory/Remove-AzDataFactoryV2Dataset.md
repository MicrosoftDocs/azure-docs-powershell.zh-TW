---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 8d1a4dfcaaa101a87fc687e78b8086823be7caab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622574"
---
# <span data-ttu-id="a24a8-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="a24a8-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="a24a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a24a8-102">SYNOPSIS</span></span>
<span data-ttu-id="a24a8-103">從資料工廠移除資料集。</span><span class="sxs-lookup"><span data-stu-id="a24a8-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="a24a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="a24a8-104">SYNTAX</span></span>

### <span data-ttu-id="a24a8-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="a24a8-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a24a8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a24a8-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a24a8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a24a8-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a24a8-108">說明</span><span class="sxs-lookup"><span data-stu-id="a24a8-108">DESCRIPTION</span></span>
<span data-ttu-id="a24a8-109">Remove-AzDataFactoryV2Dataset Cmdlet 會從 Azure 資料工廠中移除資料集。</span><span class="sxs-lookup"><span data-stu-id="a24a8-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="a24a8-110">示例</span><span class="sxs-lookup"><span data-stu-id="a24a8-110">EXAMPLES</span></span>

### <span data-ttu-id="a24a8-111">範例1：移除資料集</span><span class="sxs-lookup"><span data-stu-id="a24a8-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="a24a8-112">這個命令會從名為 WikiADF 的資料工廠中移除名為 DAWikiAggregatedData 的資料集。</span><span class="sxs-lookup"><span data-stu-id="a24a8-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="a24a8-113">命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="a24a8-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="a24a8-114">參數</span><span class="sxs-lookup"><span data-stu-id="a24a8-114">PARAMETERS</span></span>

### <span data-ttu-id="a24a8-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a24a8-115">-DataFactoryName</span></span>
<span data-ttu-id="a24a8-116">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="a24a8-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a24a8-117">這個 Cmdlet 會從資料工廠中移除此參數指定的資料集。</span><span class="sxs-lookup"><span data-stu-id="a24a8-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a24a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a24a8-118">-DefaultProfile</span></span>
<span data-ttu-id="a24a8-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a24a8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a24a8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a24a8-120">-Force</span></span>
<span data-ttu-id="a24a8-121">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a24a8-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a24a8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a24a8-122">-InputObject</span></span>
<span data-ttu-id="a24a8-123">指定要移除的資料集物件。</span><span class="sxs-lookup"><span data-stu-id="a24a8-123">Specifies a Dataset object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a24a8-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="a24a8-124">-Name</span></span>
<span data-ttu-id="a24a8-125">指定要移除的資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="a24a8-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a24a8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a24a8-126">-ResourceGroupName</span></span>
<span data-ttu-id="a24a8-127">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a24a8-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a24a8-128">這個 Cmdlet 會從這個參數指定的群組中移除資料集。</span><span class="sxs-lookup"><span data-stu-id="a24a8-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a24a8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a24a8-129">-ResourceId</span></span>
<span data-ttu-id="a24a8-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a24a8-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a24a8-131">-確認</span><span class="sxs-lookup"><span data-stu-id="a24a8-131">-Confirm</span></span>
<span data-ttu-id="a24a8-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a24a8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a24a8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a24a8-133">-WhatIf</span></span>
<span data-ttu-id="a24a8-134">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a24a8-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a24a8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a24a8-135">CommonParameters</span></span>
<span data-ttu-id="a24a8-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a24a8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a24a8-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a24a8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a24a8-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a24a8-138">INPUTS</span></span>

### <span data-ttu-id="a24a8-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="a24a8-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="a24a8-140">System.object</span><span class="sxs-lookup"><span data-stu-id="a24a8-140">System.String</span></span>

## <span data-ttu-id="a24a8-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a24a8-141">OUTPUTS</span></span>

### <span data-ttu-id="a24a8-142">System.void</span><span class="sxs-lookup"><span data-stu-id="a24a8-142">System.Void</span></span>

## <span data-ttu-id="a24a8-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a24a8-143">NOTES</span></span>
<span data-ttu-id="a24a8-144">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="a24a8-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a24a8-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="a24a8-145">RELATED LINKS</span></span>

[<span data-ttu-id="a24a8-146">AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="a24a8-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="a24a8-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="a24a8-147">Set-AzDataFactoryV2Dataset</span></span>]()