---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8667de4551e9fc0c4baf623099f70f778ec8f0a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792710"
---
# <span data-ttu-id="27ff0-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="27ff0-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="27ff0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="27ff0-103">建立 Azure SQL Server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="27ff0-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="27ff0-104">句法</span><span class="sxs-lookup"><span data-stu-id="27ff0-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27ff0-105">說明</span><span class="sxs-lookup"><span data-stu-id="27ff0-105">DESCRIPTION</span></span>
<span data-ttu-id="27ff0-106">建立 Azure SQL Server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="27ff0-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="27ff0-107">虛擬網路規則是用來將 Azure SQL Server 連線至特定的虛擬網路，以限制 Azure SQL Server 上的存取權只在虛擬網路中提供。</span><span class="sxs-lookup"><span data-stu-id="27ff0-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="27ff0-108">示例</span><span class="sxs-lookup"><span data-stu-id="27ff0-108">EXAMPLES</span></span>

### <span data-ttu-id="27ff0-109">範例1</span><span class="sxs-lookup"><span data-stu-id="27ff0-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="27ff0-110">建立 Azure SQL Server 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="27ff0-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="27ff0-111">參數</span><span class="sxs-lookup"><span data-stu-id="27ff0-111">PARAMETERS</span></span>

### <span data-ttu-id="27ff0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27ff0-112">-AsJob</span></span>
<span data-ttu-id="27ff0-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="27ff0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27ff0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27ff0-114">-DefaultProfile</span></span>
<span data-ttu-id="27ff0-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="27ff0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27ff0-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="27ff0-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="27ff0-117">在虛擬網路啟用 vnet 服務端點之前，請先建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="27ff0-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="27ff0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27ff0-118">-ResourceGroupName</span></span>
<span data-ttu-id="27ff0-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="27ff0-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="27ff0-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="27ff0-120">-ServerName</span></span>
<span data-ttu-id="27ff0-121">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="27ff0-121">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ff0-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="27ff0-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="27ff0-123">Azure Sql Server 虛擬網路規則名稱。</span><span class="sxs-lookup"><span data-stu-id="27ff0-123">Azure Sql Server Virtual Network Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ff0-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="27ff0-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="27ff0-125">指定 Microsoft. 網路詳細資料的虛擬網路子網識別碼</span><span class="sxs-lookup"><span data-stu-id="27ff0-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ff0-126">-確認</span><span class="sxs-lookup"><span data-stu-id="27ff0-126">-Confirm</span></span>
<span data-ttu-id="27ff0-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="27ff0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27ff0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27ff0-128">-WhatIf</span></span>
<span data-ttu-id="27ff0-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="27ff0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27ff0-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27ff0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27ff0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ff0-131">CommonParameters</span></span>
<span data-ttu-id="27ff0-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27ff0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ff0-133">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="27ff0-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ff0-134">輸入</span><span class="sxs-lookup"><span data-stu-id="27ff0-134">INPUTS</span></span>

### <span data-ttu-id="27ff0-135">System.object</span><span class="sxs-lookup"><span data-stu-id="27ff0-135">System.String</span></span>

## <span data-ttu-id="27ff0-136">輸出</span><span class="sxs-lookup"><span data-stu-id="27ff0-136">OUTPUTS</span></span>

### <span data-ttu-id="27ff0-137">AzureSqlServerVirtualNetworkRuleModel 中的 [VirtualNetworkRule]</span><span class="sxs-lookup"><span data-stu-id="27ff0-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="27ff0-138">筆記</span><span class="sxs-lookup"><span data-stu-id="27ff0-138">NOTES</span></span>

## <span data-ttu-id="27ff0-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="27ff0-139">RELATED LINKS</span></span>