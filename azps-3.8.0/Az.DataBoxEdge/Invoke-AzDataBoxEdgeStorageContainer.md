---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: f897c2adfe4154aeff5bd370437ea8b23e4efd36
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959344"
---
# <span data-ttu-id="f21c4-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f21c4-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="f21c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f21c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f21c4-103">在儲存空間容器上調用特定動作</span><span class="sxs-lookup"><span data-stu-id="f21c4-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="f21c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="f21c4-104">SYNTAX</span></span>

### <span data-ttu-id="f21c4-105">InvokeByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f21c4-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f21c4-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f21c4-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f21c4-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f21c4-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f21c4-108">說明</span><span class="sxs-lookup"><span data-stu-id="f21c4-108">DESCRIPTION</span></span>
<span data-ttu-id="f21c4-109">**AzDataBoxEdgeStorageContainer** Cmdlet 會呼叫動作，以重新整理資料盒 Edge 裝置上儲存空間容器上的資料。</span><span class="sxs-lookup"><span data-stu-id="f21c4-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="f21c4-110">示例</span><span class="sxs-lookup"><span data-stu-id="f21c4-110">EXAMPLES</span></span>

### <span data-ttu-id="f21c4-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f21c4-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="f21c4-112">範例2</span><span class="sxs-lookup"><span data-stu-id="f21c4-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="f21c4-113">參數</span><span class="sxs-lookup"><span data-stu-id="f21c4-113">PARAMETERS</span></span>

### <span data-ttu-id="f21c4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f21c4-114">-AsJob</span></span>
<span data-ttu-id="f21c4-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f21c4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f21c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f21c4-116">-DefaultProfile</span></span>
<span data-ttu-id="f21c4-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f21c4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f21c4-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f21c4-118">-DeviceName</span></span>
<span data-ttu-id="f21c4-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="f21c4-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f21c4-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f21c4-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="f21c4-121">資源名稱</span><span class="sxs-lookup"><span data-stu-id="f21c4-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f21c4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f21c4-122">-InputObject</span></span>
<span data-ttu-id="f21c4-123">提供現有的 EdgeStorageAccount 物件</span><span class="sxs-lookup"><span data-stu-id="f21c4-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f21c4-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f21c4-124">-Name</span></span>
<span data-ttu-id="f21c4-125">資源名稱</span><span class="sxs-lookup"><span data-stu-id="f21c4-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f21c4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f21c4-126">-PassThru</span></span>
<span data-ttu-id="f21c4-127">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="f21c4-127">returns true if successful</span></span>

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

### <span data-ttu-id="f21c4-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="f21c4-128">-RefreshData</span></span>
<span data-ttu-id="f21c4-129">使用雲端的資料重新整理容器中繼資料</span><span class="sxs-lookup"><span data-stu-id="f21c4-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="f21c4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f21c4-130">-ResourceGroupName</span></span>
<span data-ttu-id="f21c4-131">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f21c4-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f21c4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f21c4-132">-ResourceId</span></span>
<span data-ttu-id="f21c4-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f21c4-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f21c4-134">-確認</span><span class="sxs-lookup"><span data-stu-id="f21c4-134">-Confirm</span></span>
<span data-ttu-id="f21c4-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f21c4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f21c4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f21c4-136">-WhatIf</span></span>
<span data-ttu-id="f21c4-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f21c4-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f21c4-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f21c4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f21c4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f21c4-139">CommonParameters</span></span>
<span data-ttu-id="f21c4-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f21c4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f21c4-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f21c4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f21c4-142">輸入</span><span class="sxs-lookup"><span data-stu-id="f21c4-142">INPUTS</span></span>

### <span data-ttu-id="f21c4-143">System.object</span><span class="sxs-lookup"><span data-stu-id="f21c4-143">System.String</span></span>

### <span data-ttu-id="f21c4-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f21c4-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="f21c4-145">輸出</span><span class="sxs-lookup"><span data-stu-id="f21c4-145">OUTPUTS</span></span>

### <span data-ttu-id="f21c4-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f21c4-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="f21c4-147">筆記</span><span class="sxs-lookup"><span data-stu-id="f21c4-147">NOTES</span></span>

## <span data-ttu-id="f21c4-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="f21c4-148">RELATED LINKS</span></span>