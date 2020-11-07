---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: db7d9165b8aec6a69f31850f7a37eddb2450e53b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798221"
---
# <span data-ttu-id="8025f-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="8025f-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="8025f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8025f-102">SYNOPSIS</span></span>
<span data-ttu-id="8025f-103">設定 Azure SQL 實例池的屬性。</span><span class="sxs-lookup"><span data-stu-id="8025f-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="8025f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8025f-104">SYNTAX</span></span>

### <span data-ttu-id="8025f-105">DefaultSetInstancePoolParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8025f-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8025f-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="8025f-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8025f-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="8025f-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8025f-108">說明</span><span class="sxs-lookup"><span data-stu-id="8025f-108">DESCRIPTION</span></span>
<span data-ttu-id="8025f-109">**AzSqlInstancePool** Cmdlet 會修改 Azure SQL 實例池的屬性。</span><span class="sxs-lookup"><span data-stu-id="8025f-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="8025f-110">示例</span><span class="sxs-lookup"><span data-stu-id="8025f-110">EXAMPLES</span></span>

### <span data-ttu-id="8025f-111">範例1：設定實例池授權類型</span><span class="sxs-lookup"><span data-stu-id="8025f-111">Example 1 : Set an instance pool license type</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0 -LicenseType LicenseIncluded
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="8025f-112">這個命令會設定名為 instancePool0 的實例池的授權類型和/或標記。</span><span class="sxs-lookup"><span data-stu-id="8025f-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="8025f-113">範例2：使用實例池物件設定實例池授權類型</span><span class="sxs-lookup"><span data-stu-id="8025f-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
PS C:\> Set-AzSqlInstancePool -InputObject $instancePool -LicenseType LicenseIncluded
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="8025f-114">這個命令會使用實例池物件來設定實例池的授權類型和/或標記。</span><span class="sxs-lookup"><span data-stu-id="8025f-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="8025f-115">範例3：使用實例池資源識別碼設定實例池授權類型</span><span class="sxs-lookup"><span data-stu-id="8025f-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0" -LicenseType LicenseIncluded
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="8025f-116">這個命令會設定名為 instancePool0 的實例池的授權類型和/或標記。</span><span class="sxs-lookup"><span data-stu-id="8025f-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="8025f-117">參數</span><span class="sxs-lookup"><span data-stu-id="8025f-117">PARAMETERS</span></span>

### <span data-ttu-id="8025f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8025f-118">-AsJob</span></span>
<span data-ttu-id="8025f-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8025f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8025f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8025f-120">-DefaultProfile</span></span>
<span data-ttu-id="8025f-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8025f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8025f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8025f-122">-InputObject</span></span>
<span data-ttu-id="8025f-123">實例池輸入物件。</span><span class="sxs-lookup"><span data-stu-id="8025f-123">The instance pool input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InputObjectSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8025f-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8025f-124">-LicenseType</span></span>
<span data-ttu-id="8025f-125">決定要使用哪一種授權類型。</span><span class="sxs-lookup"><span data-stu-id="8025f-125">Determines which License Type to use.</span></span>
<span data-ttu-id="8025f-126">可能的值為 BasePrice (，AHB 折扣) 和 LicenseIncluded (沒有 AHB 的折扣) 。</span><span class="sxs-lookup"><span data-stu-id="8025f-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8025f-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="8025f-127">-Name</span></span>
<span data-ttu-id="8025f-128">實例池的名稱。</span><span class="sxs-lookup"><span data-stu-id="8025f-128">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8025f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8025f-129">-ResourceGroupName</span></span>
<span data-ttu-id="8025f-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8025f-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8025f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8025f-131">-ResourceId</span></span>
<span data-ttu-id="8025f-132">實例池資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8025f-132">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8025f-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="8025f-133">-Tag</span></span>
<span data-ttu-id="8025f-134">要與實例關聯的標記</span><span class="sxs-lookup"><span data-stu-id="8025f-134">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8025f-135">-確認</span><span class="sxs-lookup"><span data-stu-id="8025f-135">-Confirm</span></span>
<span data-ttu-id="8025f-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8025f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8025f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8025f-137">-WhatIf</span></span>
<span data-ttu-id="8025f-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8025f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8025f-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8025f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8025f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8025f-140">CommonParameters</span></span>
<span data-ttu-id="8025f-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8025f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8025f-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8025f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8025f-143">輸入</span><span class="sxs-lookup"><span data-stu-id="8025f-143">INPUTS</span></span>

### <span data-ttu-id="8025f-144">Microsoft.Azure.Commands.Sql.Instance_Pools AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="8025f-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="8025f-145">System.object</span><span class="sxs-lookup"><span data-stu-id="8025f-145">System.String</span></span>

## <span data-ttu-id="8025f-146">輸出</span><span class="sxs-lookup"><span data-stu-id="8025f-146">OUTPUTS</span></span>

### <span data-ttu-id="8025f-147">System.object</span><span class="sxs-lookup"><span data-stu-id="8025f-147">System.Object</span></span>
## <span data-ttu-id="8025f-148">筆記</span><span class="sxs-lookup"><span data-stu-id="8025f-148">NOTES</span></span>

## <span data-ttu-id="8025f-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="8025f-149">RELATED LINKS</span></span>