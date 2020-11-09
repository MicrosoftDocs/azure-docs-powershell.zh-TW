---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ca7aeed13627bba3c380b3f1062ee80fcc7c3ebf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285769"
---
# <span data-ttu-id="ec067-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ec067-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="ec067-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec067-102">SYNOPSIS</span></span>
<span data-ttu-id="ec067-103">停止執行建議索引作業的工作流程。</span><span class="sxs-lookup"><span data-stu-id="ec067-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="ec067-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec067-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec067-105">說明</span><span class="sxs-lookup"><span data-stu-id="ec067-105">DESCRIPTION</span></span>
<span data-ttu-id="ec067-106">**AzSqlDatabaseExecuteIndexRecommendation** Cmdlet 會停止執行建議的索引作業的工作流程。</span><span class="sxs-lookup"><span data-stu-id="ec067-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="ec067-107">示例</span><span class="sxs-lookup"><span data-stu-id="ec067-107">EXAMPLES</span></span>

### <span data-ttu-id="ec067-108">範例1：停止執行索引建議</span><span class="sxs-lookup"><span data-stu-id="ec067-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="ec067-109">這個命令會停止執行索引建議。</span><span class="sxs-lookup"><span data-stu-id="ec067-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="ec067-110">參數</span><span class="sxs-lookup"><span data-stu-id="ec067-110">PARAMETERS</span></span>

### <span data-ttu-id="ec067-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ec067-111">-DatabaseName</span></span>
<span data-ttu-id="ec067-112">指定此 Cmdlet 停止工作流程之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec067-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec067-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec067-113">-DefaultProfile</span></span>
<span data-ttu-id="ec067-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ec067-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec067-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="ec067-115">-IndexRecommendationName</span></span>
<span data-ttu-id="ec067-116">指定此 Cmdlet 停止的索引建議名稱。</span><span class="sxs-lookup"><span data-stu-id="ec067-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec067-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec067-117">-ResourceGroupName</span></span>
<span data-ttu-id="ec067-118">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec067-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ec067-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ec067-119">-ServerName</span></span>
<span data-ttu-id="ec067-120">指定主持此 Cmdlet 停止工作流程之資料庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="ec067-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec067-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec067-121">CommonParameters</span></span>
<span data-ttu-id="ec067-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec067-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec067-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ec067-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec067-124">輸入</span><span class="sxs-lookup"><span data-stu-id="ec067-124">INPUTS</span></span>

### <span data-ttu-id="ec067-125">System.object</span><span class="sxs-lookup"><span data-stu-id="ec067-125">System.String</span></span>

## <span data-ttu-id="ec067-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ec067-126">OUTPUTS</span></span>

### <span data-ttu-id="ec067-127">IndexRecommendation （.Sql）命令</span><span class="sxs-lookup"><span data-stu-id="ec067-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="ec067-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ec067-128">NOTES</span></span>

## <span data-ttu-id="ec067-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec067-129">RELATED LINKS</span></span>

[<span data-ttu-id="ec067-130">AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ec067-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="ec067-131">開始-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ec067-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="ec067-132">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ec067-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

