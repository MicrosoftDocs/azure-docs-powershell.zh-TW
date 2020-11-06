---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 94efd633a64bd1437206a00b83d86cf09fc56036
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620486"
---
# <span data-ttu-id="10e48-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="10e48-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="10e48-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10e48-102">SYNOPSIS</span></span>
<span data-ttu-id="10e48-103">取得備份短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="10e48-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="10e48-104">句法</span><span class="sxs-lookup"><span data-stu-id="10e48-104">SYNTAX</span></span>

### <span data-ttu-id="10e48-105">PolicyByResourceServerDatabaseSet (預設) </span><span class="sxs-lookup"><span data-stu-id="10e48-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10e48-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="10e48-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10e48-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="10e48-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10e48-108">說明</span><span class="sxs-lookup"><span data-stu-id="10e48-108">DESCRIPTION</span></span>
<span data-ttu-id="10e48-109">**AzSqlDatabaseBackupShortTermRetentionPolicy** Cmdlet 會取得已登錄至此資料庫的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="10e48-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="10e48-110">原則是在時間點還原備份的保留期間（以天數為單位）。</span><span class="sxs-lookup"><span data-stu-id="10e48-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="10e48-111">示例</span><span class="sxs-lookup"><span data-stu-id="10e48-111">EXAMPLES</span></span>

### <span data-ttu-id="10e48-112">範例1</span><span class="sxs-lookup"><span data-stu-id="10e48-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="10e48-113">這個命令會取得 database01 的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="10e48-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="10e48-114">範例2</span><span class="sxs-lookup"><span data-stu-id="10e48-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="10e48-115">這個命令會取得 database01 透過管道在資料庫物件中進行的短期保留原則。</span><span class="sxs-lookup"><span data-stu-id="10e48-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="10e48-116">參數</span><span class="sxs-lookup"><span data-stu-id="10e48-116">PARAMETERS</span></span>

### <span data-ttu-id="10e48-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="10e48-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="10e48-118">要取得原則的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="10e48-118">The database object to get the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10e48-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="10e48-119">-DatabaseName</span></span>
<span data-ttu-id="10e48-120">要使用之 Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="10e48-120">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e48-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e48-121">-DefaultProfile</span></span>
<span data-ttu-id="10e48-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10e48-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10e48-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10e48-123">-ResourceGroupName</span></span>
<span data-ttu-id="10e48-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="10e48-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e48-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10e48-125">-ResourceId</span></span>
<span data-ttu-id="10e48-126">短期保留原則資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="10e48-126">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e48-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="10e48-127">-ServerName</span></span>
<span data-ttu-id="10e48-128">資料庫所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="10e48-128">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e48-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e48-129">CommonParameters</span></span>
<span data-ttu-id="10e48-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10e48-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e48-131">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="10e48-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e48-132">輸入</span><span class="sxs-lookup"><span data-stu-id="10e48-132">INPUTS</span></span>

### <span data-ttu-id="10e48-133">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="10e48-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="10e48-134">System.object</span><span class="sxs-lookup"><span data-stu-id="10e48-134">System.String</span></span>

## <span data-ttu-id="10e48-135">輸出</span><span class="sxs-lookup"><span data-stu-id="10e48-135">OUTPUTS</span></span>

### <span data-ttu-id="10e48-136">AzureSqlDatabaseBackupShortTermRetentionPolicyModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="10e48-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="10e48-137">筆記</span><span class="sxs-lookup"><span data-stu-id="10e48-137">NOTES</span></span>

## <span data-ttu-id="10e48-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="10e48-138">RELATED LINKS</span></span>