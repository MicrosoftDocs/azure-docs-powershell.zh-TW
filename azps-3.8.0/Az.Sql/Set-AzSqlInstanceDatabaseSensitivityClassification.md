---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: f524c8b30f609cb2fef3fb3f59550078b26b11b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798225"
---
# <span data-ttu-id="04cb4-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="04cb4-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="04cb4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04cb4-102">SYNOPSIS</span></span>
<span data-ttu-id="04cb4-103">在 Azure SQL managed 實例資料庫中設定欄的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="04cb4-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="04cb4-104">句法</span><span class="sxs-lookup"><span data-stu-id="04cb4-104">SYNTAX</span></span>

### <span data-ttu-id="04cb4-105">ClassificationObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="04cb4-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04cb4-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="04cb4-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04cb4-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="04cb4-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04cb4-108">說明</span><span class="sxs-lookup"><span data-stu-id="04cb4-108">DESCRIPTION</span></span>
<span data-ttu-id="04cb4-109">Set-AzSqlInstanceDatabaseSensitivityClassification Cmdlet 會針對 Azure SQL managed 實例資料庫中的欄設定資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="04cb4-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="04cb4-110">示例</span><span class="sxs-lookup"><span data-stu-id="04cb4-110">EXAMPLES</span></span>

### <span data-ttu-id="04cb4-111">範例1：在 Azure SQL managed 實例資料庫中設定欄的資訊類型與敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="04cb4-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="04cb4-112">範例2：針對 Azure SQL managed 實例資料庫中的欄設定建議的資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="04cb4-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="04cb4-113">範例3：使用管道在 Azure SQL managed 實例資料庫中設定資料行的資訊類型與敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="04cb4-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="04cb4-114">參數</span><span class="sxs-lookup"><span data-stu-id="04cb4-114">PARAMETERS</span></span>

### <span data-ttu-id="04cb4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04cb4-115">-AsJob</span></span>
<span data-ttu-id="04cb4-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="04cb4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04cb4-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="04cb4-117">-ClassificationObject</span></span>
<span data-ttu-id="04cb4-118">代表 SQL Managed 實例資料庫敏感度分類的物件。</span><span class="sxs-lookup"><span data-stu-id="04cb4-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04cb4-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="04cb4-119">-ColumnName</span></span>
<span data-ttu-id="04cb4-120">資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="04cb4-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04cb4-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="04cb4-121">-DatabaseName</span></span>
<span data-ttu-id="04cb4-122">Azure SQL managed 實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="04cb4-122">The name of the Azure SQL managed instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04cb4-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="04cb4-123">-DatabaseObject</span></span>
<span data-ttu-id="04cb4-124">Azure SQL managed 實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="04cb4-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04cb4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04cb4-125">-DefaultProfile</span></span>
<span data-ttu-id="04cb4-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="04cb4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04cb4-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="04cb4-127">-InformationType</span></span>
<span data-ttu-id="04cb4-128">描述儲存在欄中之資料之資訊類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="04cb4-128">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04cb4-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="04cb4-129">-InstanceName</span></span>
<span data-ttu-id="04cb4-130">Azure SQL managed 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="04cb4-130">Azure SQL managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04cb4-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04cb4-131">-PassThru</span></span>
<span data-ttu-id="04cb4-132">指定是否要在 Cmdlet 執行結束時輸出靈敏度分類模型</span><span class="sxs-lookup"><span data-stu-id="04cb4-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="04cb4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04cb4-133">-ResourceGroupName</span></span>
<span data-ttu-id="04cb4-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="04cb4-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04cb4-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="04cb4-135">-SchemaName</span></span>
<span data-ttu-id="04cb4-136">架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="04cb4-136">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04cb4-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="04cb4-137">-SensitivityLabel</span></span>
<span data-ttu-id="04cb4-138">描述儲存在欄中之資料敏感度的名稱。</span><span class="sxs-lookup"><span data-stu-id="04cb4-138">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04cb4-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="04cb4-139">-TableName</span></span>
<span data-ttu-id="04cb4-140">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="04cb4-140">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04cb4-141">-確認</span><span class="sxs-lookup"><span data-stu-id="04cb4-141">-Confirm</span></span>
<span data-ttu-id="04cb4-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="04cb4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04cb4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04cb4-143">-WhatIf</span></span>
<span data-ttu-id="04cb4-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="04cb4-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04cb4-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04cb4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04cb4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04cb4-146">CommonParameters</span></span>
<span data-ttu-id="04cb4-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04cb4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04cb4-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="04cb4-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04cb4-149">輸入</span><span class="sxs-lookup"><span data-stu-id="04cb4-149">INPUTS</span></span>

### <span data-ttu-id="04cb4-150">ManagedDatabaseSensitivityClassificationModel 中的 [DataClassification]</span><span class="sxs-lookup"><span data-stu-id="04cb4-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="04cb4-151">輸出</span><span class="sxs-lookup"><span data-stu-id="04cb4-151">OUTPUTS</span></span>

### <span data-ttu-id="04cb4-152">System.object</span><span class="sxs-lookup"><span data-stu-id="04cb4-152">System.Boolean</span></span>

## <span data-ttu-id="04cb4-153">筆記</span><span class="sxs-lookup"><span data-stu-id="04cb4-153">NOTES</span></span>

## <span data-ttu-id="04cb4-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="04cb4-154">RELATED LINKS</span></span>

[<span data-ttu-id="04cb4-155">深入瞭解 Azure SQL 資料庫資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="04cb4-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)