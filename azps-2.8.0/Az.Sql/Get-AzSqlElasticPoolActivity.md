---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 61a72691aaaaf9cbdfd4e0706f6ace17d7291851
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792609"
---
# <span data-ttu-id="3010c-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="3010c-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="3010c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3010c-102">SYNOPSIS</span></span>
<span data-ttu-id="3010c-103">取得彈性池中作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="3010c-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="3010c-104">句法</span><span class="sxs-lookup"><span data-stu-id="3010c-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3010c-105">說明</span><span class="sxs-lookup"><span data-stu-id="3010c-105">DESCRIPTION</span></span>
<span data-ttu-id="3010c-106">**AzSqlElasticPoolActivity** Cmdlet 會取得 Azure SQL 資料庫彈性池中作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="3010c-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="3010c-107">您可以查看 [建立池] 與 [配置更新] 的狀態。</span><span class="sxs-lookup"><span data-stu-id="3010c-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="3010c-108">示例</span><span class="sxs-lookup"><span data-stu-id="3010c-108">EXAMPLES</span></span>

### <span data-ttu-id="3010c-109">範例1：取得彈性池作業的狀態</span><span class="sxs-lookup"><span data-stu-id="3010c-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="3010c-110">這個命令會取得名為 ElasticPool01 的彈性池作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="3010c-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="3010c-111">參數</span><span class="sxs-lookup"><span data-stu-id="3010c-111">PARAMETERS</span></span>

### <span data-ttu-id="3010c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3010c-112">-DefaultProfile</span></span>
<span data-ttu-id="3010c-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3010c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3010c-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3010c-114">-ElasticPoolName</span></span>
<span data-ttu-id="3010c-115">指定彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="3010c-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="3010c-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="3010c-116">-OperationId</span></span>
<span data-ttu-id="3010c-117">要檢索的操作識別碼。</span><span class="sxs-lookup"><span data-stu-id="3010c-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="3010c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3010c-118">-ResourceGroupName</span></span>
<span data-ttu-id="3010c-119">指定將彈性池指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3010c-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="3010c-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3010c-120">-ServerName</span></span>
<span data-ttu-id="3010c-121">指定包含彈性池的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="3010c-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="3010c-122">-確認</span><span class="sxs-lookup"><span data-stu-id="3010c-122">-Confirm</span></span>
<span data-ttu-id="3010c-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3010c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3010c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3010c-124">-WhatIf</span></span>
<span data-ttu-id="3010c-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3010c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3010c-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3010c-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3010c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3010c-127">CommonParameters</span></span>
<span data-ttu-id="3010c-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3010c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3010c-129">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3010c-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3010c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="3010c-130">INPUTS</span></span>

### <span data-ttu-id="3010c-131">System.object</span><span class="sxs-lookup"><span data-stu-id="3010c-131">System.String</span></span>

### <span data-ttu-id="3010c-132">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3010c-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3010c-133">輸出</span><span class="sxs-lookup"><span data-stu-id="3010c-133">OUTPUTS</span></span>

### <span data-ttu-id="3010c-134">AzureSqlElasticPoolActivityModel 中的 [ElasticPool]</span><span class="sxs-lookup"><span data-stu-id="3010c-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="3010c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="3010c-135">NOTES</span></span>

## <span data-ttu-id="3010c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="3010c-136">RELATED LINKS</span></span>

[<span data-ttu-id="3010c-137">AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3010c-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="3010c-138">AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="3010c-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="3010c-139">新-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3010c-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="3010c-140">移除-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3010c-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="3010c-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3010c-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

