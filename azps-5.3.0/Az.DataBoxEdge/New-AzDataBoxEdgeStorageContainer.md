---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3561c77e79f0ee1be82b8f180fdf1b73879dc084
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439595"
---
# <span data-ttu-id="dea43-101">New-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="dea43-101">New-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="dea43-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dea43-102">SYNOPSIS</span></span>
<span data-ttu-id="dea43-103">在裝置上的 Edge 儲存空間帳戶中建立新的儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="dea43-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="dea43-104">句法</span><span class="sxs-lookup"><span data-stu-id="dea43-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dea43-105">說明</span><span class="sxs-lookup"><span data-stu-id="dea43-105">DESCRIPTION</span></span>
<span data-ttu-id="dea43-106">**新的-AzDataBoxEdgeStorageContainer** Cmdlet 會在資料盒 edge 裝置的 Edge 儲存空間帳戶中建立新的儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="dea43-106">The **New-AzDataBoxEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Data Box Edge device.</span></span>

## <span data-ttu-id="dea43-107">示例</span><span class="sxs-lookup"><span data-stu-id="dea43-107">EXAMPLES</span></span>

### <span data-ttu-id="dea43-108">範例1</span><span class="sxs-lookup"><span data-stu-id="dea43-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="dea43-109">參數</span><span class="sxs-lookup"><span data-stu-id="dea43-109">PARAMETERS</span></span>

### <span data-ttu-id="dea43-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dea43-110">-AsJob</span></span>
<span data-ttu-id="dea43-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dea43-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dea43-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="dea43-112">-DataFormat</span></span>
<span data-ttu-id="dea43-113">設定資料格式 ex： PageBlob、BlobBlob</span><span class="sxs-lookup"><span data-stu-id="dea43-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dea43-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dea43-114">-DefaultProfile</span></span>
<span data-ttu-id="dea43-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dea43-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dea43-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="dea43-116">-DeviceName</span></span>
<span data-ttu-id="dea43-117">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="dea43-117">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dea43-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dea43-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="dea43-119">提供現有 EdgeStorageAccount 的名稱</span><span class="sxs-lookup"><span data-stu-id="dea43-119">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dea43-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="dea43-120">-Name</span></span>
<span data-ttu-id="dea43-121">資源名稱</span><span class="sxs-lookup"><span data-stu-id="dea43-121">Resource Name</span></span>

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

### <span data-ttu-id="dea43-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dea43-122">-ResourceGroupName</span></span>
<span data-ttu-id="dea43-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="dea43-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dea43-124">-確認</span><span class="sxs-lookup"><span data-stu-id="dea43-124">-Confirm</span></span>
<span data-ttu-id="dea43-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dea43-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dea43-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dea43-126">-WhatIf</span></span>
<span data-ttu-id="dea43-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dea43-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dea43-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dea43-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dea43-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea43-129">CommonParameters</span></span>
<span data-ttu-id="dea43-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dea43-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea43-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dea43-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea43-132">輸入</span><span class="sxs-lookup"><span data-stu-id="dea43-132">INPUTS</span></span>

### <span data-ttu-id="dea43-133">System.object</span><span class="sxs-lookup"><span data-stu-id="dea43-133">System.String</span></span>

## <span data-ttu-id="dea43-134">輸出</span><span class="sxs-lookup"><span data-stu-id="dea43-134">OUTPUTS</span></span>

### <span data-ttu-id="dea43-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="dea43-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="dea43-136">筆記</span><span class="sxs-lookup"><span data-stu-id="dea43-136">NOTES</span></span>

## <span data-ttu-id="dea43-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="dea43-137">RELATED LINKS</span></span>