---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: fdcc8946070994cd172514f8da1578328ae61db2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790966"
---
# <span data-ttu-id="68af9-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="68af9-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="68af9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68af9-102">SYNOPSIS</span></span>
<span data-ttu-id="68af9-103">新增節點至群集中的特定節點類型。</span><span class="sxs-lookup"><span data-stu-id="68af9-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="68af9-104">句法</span><span class="sxs-lookup"><span data-stu-id="68af9-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68af9-105">說明</span><span class="sxs-lookup"><span data-stu-id="68af9-105">DESCRIPTION</span></span>
<span data-ttu-id="68af9-106">使用 [ **載入 AzServiceFabricNode** ]，將節點新增至特定的節點類型。</span><span class="sxs-lookup"><span data-stu-id="68af9-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="68af9-107">您只需指定要新增至節點類型的節點數。</span><span class="sxs-lookup"><span data-stu-id="68af9-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="68af9-108">示例</span><span class="sxs-lookup"><span data-stu-id="68af9-108">EXAMPLES</span></span>

### <span data-ttu-id="68af9-109">範例1</span><span class="sxs-lookup"><span data-stu-id="68af9-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="68af9-110">這個命令會將2個節點新增至節點類型 ' n1」。</span><span class="sxs-lookup"><span data-stu-id="68af9-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="68af9-111">參數</span><span class="sxs-lookup"><span data-stu-id="68af9-111">PARAMETERS</span></span>

### <span data-ttu-id="68af9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68af9-112">-DefaultProfile</span></span>
<span data-ttu-id="68af9-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68af9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68af9-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="68af9-114">-Name</span></span>
<span data-ttu-id="68af9-115">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="68af9-115">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68af9-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="68af9-116">-NodeType</span></span>
<span data-ttu-id="68af9-117">節點類型名稱</span><span class="sxs-lookup"><span data-stu-id="68af9-117">Node type name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68af9-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="68af9-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="68af9-119">要新增的節點數</span><span class="sxs-lookup"><span data-stu-id="68af9-119">The number of nodes to add</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68af9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68af9-120">-ResourceGroupName</span></span>
<span data-ttu-id="68af9-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68af9-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="68af9-122">-確認</span><span class="sxs-lookup"><span data-stu-id="68af9-122">-Confirm</span></span>
<span data-ttu-id="68af9-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="68af9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68af9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68af9-124">-WhatIf</span></span>
<span data-ttu-id="68af9-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="68af9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68af9-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68af9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68af9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68af9-127">CommonParameters</span></span>
<span data-ttu-id="68af9-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68af9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68af9-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="68af9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68af9-130">輸入</span><span class="sxs-lookup"><span data-stu-id="68af9-130">INPUTS</span></span>

### <span data-ttu-id="68af9-131">System.object</span><span class="sxs-lookup"><span data-stu-id="68af9-131">System.Int32</span></span>

### <span data-ttu-id="68af9-132">System.object</span><span class="sxs-lookup"><span data-stu-id="68af9-132">System.String</span></span>

## <span data-ttu-id="68af9-133">輸出</span><span class="sxs-lookup"><span data-stu-id="68af9-133">OUTPUTS</span></span>

### <span data-ttu-id="68af9-134">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="68af9-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="68af9-135">筆記</span><span class="sxs-lookup"><span data-stu-id="68af9-135">NOTES</span></span>

## <span data-ttu-id="68af9-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="68af9-136">RELATED LINKS</span></span>

[<span data-ttu-id="68af9-137">移除-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="68af9-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)