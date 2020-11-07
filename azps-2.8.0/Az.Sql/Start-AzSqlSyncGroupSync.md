---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: 6e6f0279f8cf3e0ea4481e31b06c42c25d0a0180
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792823"
---
# <span data-ttu-id="99df4-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="99df4-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="99df4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99df4-102">SYNOPSIS</span></span>
<span data-ttu-id="99df4-103">啟動同步處理群組同步處理。</span><span class="sxs-lookup"><span data-stu-id="99df4-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="99df4-104">句法</span><span class="sxs-lookup"><span data-stu-id="99df4-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99df4-105">說明</span><span class="sxs-lookup"><span data-stu-id="99df4-105">DESCRIPTION</span></span>
<span data-ttu-id="99df4-106">**Start-AzSqlSyncGroupSync** Cmdlet 會啟動同步處理群組同步處理。</span><span class="sxs-lookup"><span data-stu-id="99df4-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="99df4-107">示例</span><span class="sxs-lookup"><span data-stu-id="99df4-107">EXAMPLES</span></span>

### <span data-ttu-id="99df4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="99df4-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="99df4-109">這個命令會針對同步處理群組 mysg 啟動一輪同步處理。</span><span class="sxs-lookup"><span data-stu-id="99df4-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="99df4-110">參數</span><span class="sxs-lookup"><span data-stu-id="99df4-110">PARAMETERS</span></span>

### <span data-ttu-id="99df4-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="99df4-111">-DatabaseName</span></span>
<span data-ttu-id="99df4-112">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="99df4-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="99df4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99df4-113">-DefaultProfile</span></span>
<span data-ttu-id="99df4-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="99df4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99df4-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99df4-115">-PassThru</span></span>
<span data-ttu-id="99df4-116">定義是否要傳回同步處理群組</span><span class="sxs-lookup"><span data-stu-id="99df4-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="99df4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99df4-117">-ResourceGroupName</span></span>
<span data-ttu-id="99df4-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="99df4-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="99df4-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="99df4-119">-ServerName</span></span>
<span data-ttu-id="99df4-120">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="99df4-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="99df4-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="99df4-121">-SyncGroupName</span></span>
<span data-ttu-id="99df4-122">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="99df4-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99df4-123">-確認</span><span class="sxs-lookup"><span data-stu-id="99df4-123">-Confirm</span></span>
<span data-ttu-id="99df4-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="99df4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99df4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99df4-125">-WhatIf</span></span>
<span data-ttu-id="99df4-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99df4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99df4-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99df4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99df4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99df4-128">CommonParameters</span></span>
<span data-ttu-id="99df4-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99df4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99df4-130">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="99df4-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99df4-131">輸入</span><span class="sxs-lookup"><span data-stu-id="99df4-131">INPUTS</span></span>

### <span data-ttu-id="99df4-132">System.object</span><span class="sxs-lookup"><span data-stu-id="99df4-132">System.String</span></span>

## <span data-ttu-id="99df4-133">輸出</span><span class="sxs-lookup"><span data-stu-id="99df4-133">OUTPUTS</span></span>

### <span data-ttu-id="99df4-134">AzureSqlSyncGroupModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="99df4-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="99df4-135">筆記</span><span class="sxs-lookup"><span data-stu-id="99df4-135">NOTES</span></span>

## <span data-ttu-id="99df4-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="99df4-136">RELATED LINKS</span></span>

[<span data-ttu-id="99df4-137">停止 AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="99df4-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)
