---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: d5923be20fd893aefee4e9a5789c2f6f57f20fbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792773"
---
# <span data-ttu-id="34024-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="34024-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="34024-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34024-102">SYNOPSIS</span></span>
<span data-ttu-id="34024-103">取得 Azure SQL managed 實例資料庫中資料行的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="34024-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="34024-104">句法</span><span class="sxs-lookup"><span data-stu-id="34024-104">SYNTAX</span></span>

### <span data-ttu-id="34024-105">DatabaseObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="34024-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34024-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="34024-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34024-107">說明</span><span class="sxs-lookup"><span data-stu-id="34024-107">DESCRIPTION</span></span>
<span data-ttu-id="34024-108">Get-AzSqlInstanceDatabaseSensitivityRecommendation Cmdlet 會傳回 Azure SQL managed 實例資料庫中資料行的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="34024-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="34024-109">示例</span><span class="sxs-lookup"><span data-stu-id="34024-109">EXAMPLES</span></span>

### <span data-ttu-id="34024-110">範例1：取得 Azure SQL managed 實例資料庫的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="34024-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="34024-111">範例2：使用管道取得 Azure SQL managed 實例資料庫的建議資訊類型和敏感度標籤。</span><span class="sxs-lookup"><span data-stu-id="34024-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

## <span data-ttu-id="34024-112">參數</span><span class="sxs-lookup"><span data-stu-id="34024-112">PARAMETERS</span></span>

### <span data-ttu-id="34024-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34024-113">-AsJob</span></span>
<span data-ttu-id="34024-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="34024-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34024-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="34024-115">-DatabaseName</span></span>
<span data-ttu-id="34024-116">Azure SQL managed 實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="34024-116">The name of the Azure SQL managed instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34024-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="34024-117">-DatabaseObject</span></span>
<span data-ttu-id="34024-118">Azure SQL managed 實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="34024-118">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34024-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34024-119">-DefaultProfile</span></span>
<span data-ttu-id="34024-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="34024-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34024-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="34024-121">-InstanceName</span></span>
<span data-ttu-id="34024-122">Azure SQL managed 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="34024-122">Azure SQL managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34024-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34024-123">-ResourceGroupName</span></span>
<span data-ttu-id="34024-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="34024-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34024-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34024-125">CommonParameters</span></span>
<span data-ttu-id="34024-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34024-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34024-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="34024-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34024-128">輸入</span><span class="sxs-lookup"><span data-stu-id="34024-128">INPUTS</span></span>

### <span data-ttu-id="34024-129">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="34024-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="34024-130">輸出</span><span class="sxs-lookup"><span data-stu-id="34024-130">OUTPUTS</span></span>

### <span data-ttu-id="34024-131">ManagedDatabaseSensitivityClassificationModel 中的 [DataClassification]</span><span class="sxs-lookup"><span data-stu-id="34024-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="34024-132">筆記</span><span class="sxs-lookup"><span data-stu-id="34024-132">NOTES</span></span>

## <span data-ttu-id="34024-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="34024-133">RELATED LINKS</span></span>

[<span data-ttu-id="34024-134">深入瞭解 Azure SQL 資料庫資料探索與分類</span><span class="sxs-lookup"><span data-stu-id="34024-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)