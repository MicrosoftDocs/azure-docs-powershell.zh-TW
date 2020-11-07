---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 0082918e09c0f42910ead42d03319577d4b4c9c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792817"
---
# <span data-ttu-id="0f028-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="0f028-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="0f028-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0f028-102">SYNOPSIS</span></span>
<span data-ttu-id="0f028-103">取消彈性池中的非同步更新作業。</span><span class="sxs-lookup"><span data-stu-id="0f028-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="0f028-104">句法</span><span class="sxs-lookup"><span data-stu-id="0f028-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f028-105">說明</span><span class="sxs-lookup"><span data-stu-id="0f028-105">DESCRIPTION</span></span>
<span data-ttu-id="0f028-106">**AzSqlElasticPoolActivity** Cmdlet 會取消彈性池中的非同步更新作業。</span><span class="sxs-lookup"><span data-stu-id="0f028-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="0f028-107">示例</span><span class="sxs-lookup"><span data-stu-id="0f028-107">EXAMPLES</span></span>

### <span data-ttu-id="0f028-108">範例1：取消彈性池中的非同步更新作業</span><span class="sxs-lookup"><span data-stu-id="0f028-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete :
```

<span data-ttu-id="0f028-109">這個命令會取消彈性池中的非同步更新作業。</span><span class="sxs-lookup"><span data-stu-id="0f028-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="0f028-110">參數</span><span class="sxs-lookup"><span data-stu-id="0f028-110">PARAMETERS</span></span>

### <span data-ttu-id="0f028-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f028-111">-DefaultProfile</span></span>
<span data-ttu-id="0f028-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f028-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f028-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0f028-113">-ElasticPoolName</span></span>
<span data-ttu-id="0f028-114">Azure SQL 彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f028-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="0f028-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="0f028-115">-OperationId</span></span>
<span data-ttu-id="0f028-116">要檢索的操作識別碼。</span><span class="sxs-lookup"><span data-stu-id="0f028-116">The ID of the operation to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f028-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f028-117">-PassThru</span></span>
<span data-ttu-id="0f028-118">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="0f028-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0f028-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f028-119">-ResourceGroupName</span></span>
<span data-ttu-id="0f028-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f028-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="0f028-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0f028-121">-ServerName</span></span>
<span data-ttu-id="0f028-122">彈性池所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f028-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="0f028-123">-確認</span><span class="sxs-lookup"><span data-stu-id="0f028-123">-Confirm</span></span>
<span data-ttu-id="0f028-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0f028-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f028-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f028-125">-WhatIf</span></span>
<span data-ttu-id="0f028-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0f028-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f028-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f028-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f028-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f028-128">CommonParameters</span></span>
<span data-ttu-id="0f028-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0f028-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f028-130">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0f028-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f028-131">輸入</span><span class="sxs-lookup"><span data-stu-id="0f028-131">INPUTS</span></span>

### <span data-ttu-id="0f028-132">System.object</span><span class="sxs-lookup"><span data-stu-id="0f028-132">System.String</span></span>

### <span data-ttu-id="0f028-133">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0f028-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0f028-134">輸出</span><span class="sxs-lookup"><span data-stu-id="0f028-134">OUTPUTS</span></span>

### <span data-ttu-id="0f028-135">AzureSqlElasticPoolActivityModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="0f028-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="0f028-136">筆記</span><span class="sxs-lookup"><span data-stu-id="0f028-136">NOTES</span></span>

## <span data-ttu-id="0f028-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f028-137">RELATED LINKS</span></span>