---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: 0cd409f530225b2fadf104f787a1e926b5f8fb16
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798054"
---
# <span data-ttu-id="dcc13-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="dcc13-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="dcc13-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dcc13-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc13-103">建立新的 sql 虛擬電腦群組。</span><span class="sxs-lookup"><span data-stu-id="dcc13-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="dcc13-104">句法</span><span class="sxs-lookup"><span data-stu-id="dcc13-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcc13-105">說明</span><span class="sxs-lookup"><span data-stu-id="dcc13-105">DESCRIPTION</span></span>
<span data-ttu-id="dcc13-106">New-AzSqlVMGroup Cmdlet 會建立 Azure SQL 虛擬電腦群組。</span><span class="sxs-lookup"><span data-stu-id="dcc13-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="dcc13-107">示例</span><span class="sxs-lookup"><span data-stu-id="dcc13-107">EXAMPLES</span></span>

### <span data-ttu-id="dcc13-108">範例1</span><span class="sxs-lookup"><span data-stu-id="dcc13-108">Example 1</span></span>
```powershell
PS C:\> $secureKey = ConvertTo-SecureString $profile.StorageAccountPrimaryKey -AsPlainText -Force
PS C:\> New-AzSqlVMGroup $resourceGroupName $groupName $location -ClusterOperatorAccount $profile.ClusterOperatorAccount `
>>         -SqlServiceAccount $profile.SqlServiceAccount -StorageAccountUrl $profile.StorageAccountUrl `
>>         -StorageAccountPrimaryKey $secureKey -DomainFqdn $profile.DomainFqdn `
>>         -Offer 'SQL2017-WS2016' -Sku 'Developer'
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="dcc13-109">使用 [資源群組 ResourceGroup01] 中的測試組 vm 建立新的 Azure SQL 虛擬電腦群組。</span><span class="sxs-lookup"><span data-stu-id="dcc13-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="dcc13-110">$profile 是 WsfcDomainProfile SqlVirtualMachine 類型的物件。</span><span class="sxs-lookup"><span data-stu-id="dcc13-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="dcc13-111">參數</span><span class="sxs-lookup"><span data-stu-id="dcc13-111">PARAMETERS</span></span>

### <span data-ttu-id="dcc13-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcc13-112">-AsJob</span></span>
<span data-ttu-id="dcc13-113">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcc13-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="dcc13-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="dcc13-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="dcc13-115">用於建立群集的名稱</span><span class="sxs-lookup"><span data-stu-id="dcc13-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="dcc13-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="dcc13-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="dcc13-117">用於運營群集的名稱</span><span class="sxs-lookup"><span data-stu-id="dcc13-117">Name used for operating cluster</span></span>

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

### <span data-ttu-id="dcc13-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc13-118">-DefaultProfile</span></span>
<span data-ttu-id="dcc13-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dcc13-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcc13-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="dcc13-120">-DomainFqdn</span></span>
<span data-ttu-id="dcc13-121">網域的完整名稱</span><span class="sxs-lookup"><span data-stu-id="dcc13-121">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="dcc13-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="dcc13-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="dcc13-123">可供共用見證的選用路徑</span><span class="sxs-lookup"><span data-stu-id="dcc13-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="dcc13-124">-位置</span><span class="sxs-lookup"><span data-stu-id="dcc13-124">-Location</span></span>
<span data-ttu-id="dcc13-125">[SQL 虛擬機器群組位置]。</span><span class="sxs-lookup"><span data-stu-id="dcc13-125">SQL virtual machine group location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc13-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="dcc13-126">-Name</span></span>
<span data-ttu-id="dcc13-127">[SQL virtual 電腦群組名稱]。</span><span class="sxs-lookup"><span data-stu-id="dcc13-127">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc13-128">-優惠</span><span class="sxs-lookup"><span data-stu-id="dcc13-128">-Offer</span></span>
<span data-ttu-id="dcc13-129">SQL 虛擬電腦群組提供。</span><span class="sxs-lookup"><span data-stu-id="dcc13-129">SQL virtual machine group offer.</span></span>

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

### <span data-ttu-id="dcc13-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="dcc13-130">-OuPath</span></span>
<span data-ttu-id="dcc13-131">節點與群集將出現的組織單位路徑</span><span class="sxs-lookup"><span data-stu-id="dcc13-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="dcc13-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcc13-132">-ResourceGroupName</span></span>
<span data-ttu-id="dcc13-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dcc13-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc13-134">-Sku</span><span class="sxs-lookup"><span data-stu-id="dcc13-134">-Sku</span></span>
<span data-ttu-id="dcc13-135">[SQL virtual 電腦群組版本] 類型。</span><span class="sxs-lookup"><span data-stu-id="dcc13-135">SQL virtual machine group edition type.</span></span>

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

### <span data-ttu-id="dcc13-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="dcc13-136">-SqlServiceAccount</span></span>
<span data-ttu-id="dcc13-137">SQL 服務將在群集中所有參與的 SQL 虛擬機器上執行的名稱</span><span class="sxs-lookup"><span data-stu-id="dcc13-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="dcc13-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="dcc13-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="dcc13-139">見證儲存空間帳戶的主鍵</span><span class="sxs-lookup"><span data-stu-id="dcc13-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc13-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="dcc13-140">-StorageAccountUrl</span></span>
<span data-ttu-id="dcc13-141">見證儲存空間帳戶的主鍵</span><span class="sxs-lookup"><span data-stu-id="dcc13-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="dcc13-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="dcc13-142">-Tag</span></span>
<span data-ttu-id="dcc13-143">要與 SQL 虛擬電腦群組相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="dcc13-143">The tags to associate with the SQL virtual machine group.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc13-144">-確認</span><span class="sxs-lookup"><span data-stu-id="dcc13-144">-Confirm</span></span>
<span data-ttu-id="dcc13-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dcc13-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcc13-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcc13-146">-WhatIf</span></span>
<span data-ttu-id="dcc13-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dcc13-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcc13-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcc13-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcc13-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc13-149">CommonParameters</span></span>
<span data-ttu-id="dcc13-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dcc13-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc13-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dcc13-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc13-152">輸入</span><span class="sxs-lookup"><span data-stu-id="dcc13-152">INPUTS</span></span>

### <span data-ttu-id="dcc13-153">System.object</span><span class="sxs-lookup"><span data-stu-id="dcc13-153">System.String</span></span>

## <span data-ttu-id="dcc13-154">輸出</span><span class="sxs-lookup"><span data-stu-id="dcc13-154">OUTPUTS</span></span>

### <span data-ttu-id="dcc13-155">SqlVirtualMachine SqlVirtualMachine. AzureSqlVMGroupModel （）</span><span class="sxs-lookup"><span data-stu-id="dcc13-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="dcc13-156">筆記</span><span class="sxs-lookup"><span data-stu-id="dcc13-156">NOTES</span></span>

## <span data-ttu-id="dcc13-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="dcc13-157">RELATED LINKS</span></span>