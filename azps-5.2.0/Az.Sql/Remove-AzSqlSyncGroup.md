---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 3a5da7972e70e3ebf9c86df62b2bbc79651e72a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275579"
---
# <span data-ttu-id="9eb95-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9eb95-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="9eb95-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9eb95-102">SYNOPSIS</span></span>
<span data-ttu-id="9eb95-103">移除 Azure SQL 資料庫同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="9eb95-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="9eb95-104">句法</span><span class="sxs-lookup"><span data-stu-id="9eb95-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9eb95-105">說明</span><span class="sxs-lookup"><span data-stu-id="9eb95-105">DESCRIPTION</span></span>
<span data-ttu-id="9eb95-106">**AzSqlSyncGroup** Cmdlet 會移除 Azure SQL 資料庫同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="9eb95-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="9eb95-107">示例</span><span class="sxs-lookup"><span data-stu-id="9eb95-107">EXAMPLES</span></span>

### <span data-ttu-id="9eb95-108">範例1：移除同步處理群組</span><span class="sxs-lookup"><span data-stu-id="9eb95-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="9eb95-109">這個命令會移除名為 syncGroup01 的 Azure SQL 資料庫同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="9eb95-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="9eb95-110">參數</span><span class="sxs-lookup"><span data-stu-id="9eb95-110">PARAMETERS</span></span>

### <span data-ttu-id="9eb95-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9eb95-111">-DatabaseName</span></span>
<span data-ttu-id="9eb95-112">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9eb95-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="9eb95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eb95-113">-DefaultProfile</span></span>
<span data-ttu-id="9eb95-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9eb95-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9eb95-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9eb95-115">-Force</span></span>
<span data-ttu-id="9eb95-116">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="9eb95-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="9eb95-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="9eb95-117">-Name</span></span>
<span data-ttu-id="9eb95-118">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="9eb95-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eb95-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9eb95-119">-PassThru</span></span>
<span data-ttu-id="9eb95-120">定義是否傳回已移除的同步處理群組</span><span class="sxs-lookup"><span data-stu-id="9eb95-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="9eb95-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eb95-121">-ResourceGroupName</span></span>
<span data-ttu-id="9eb95-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9eb95-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="9eb95-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9eb95-123">-ServerName</span></span>
<span data-ttu-id="9eb95-124">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9eb95-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="9eb95-125">-確認</span><span class="sxs-lookup"><span data-stu-id="9eb95-125">-Confirm</span></span>
<span data-ttu-id="9eb95-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9eb95-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eb95-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eb95-127">-WhatIf</span></span>
<span data-ttu-id="9eb95-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9eb95-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eb95-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9eb95-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eb95-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eb95-130">CommonParameters</span></span>
<span data-ttu-id="9eb95-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9eb95-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eb95-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9eb95-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eb95-133">輸入</span><span class="sxs-lookup"><span data-stu-id="9eb95-133">INPUTS</span></span>

### <span data-ttu-id="9eb95-134">System.object</span><span class="sxs-lookup"><span data-stu-id="9eb95-134">System.String</span></span>

## <span data-ttu-id="9eb95-135">輸出</span><span class="sxs-lookup"><span data-stu-id="9eb95-135">OUTPUTS</span></span>

### <span data-ttu-id="9eb95-136">AzureSqlSyncGroupModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="9eb95-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="9eb95-137">筆記</span><span class="sxs-lookup"><span data-stu-id="9eb95-137">NOTES</span></span>

## <span data-ttu-id="9eb95-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="9eb95-138">RELATED LINKS</span></span>

[<span data-ttu-id="9eb95-139">新-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9eb95-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="9eb95-140">更新-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9eb95-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="9eb95-141">AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9eb95-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)
