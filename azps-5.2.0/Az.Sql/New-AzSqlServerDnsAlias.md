---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 66f8c3acc178a922868177200e6d4f1f8f50931f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284652"
---
# <span data-ttu-id="eaae4-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="eaae4-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="eaae4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eaae4-102">SYNOPSIS</span></span>
<span data-ttu-id="eaae4-103">這個命令會建立新的 Azure SQL Server DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="eaae4-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="eaae4-104">句法</span><span class="sxs-lookup"><span data-stu-id="eaae4-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaae4-105">說明</span><span class="sxs-lookup"><span data-stu-id="eaae4-105">DESCRIPTION</span></span>
<span data-ttu-id="eaae4-106">建立指向指定伺服器的新 Azure SQL Server DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="eaae4-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="eaae4-107">示例</span><span class="sxs-lookup"><span data-stu-id="eaae4-107">EXAMPLES</span></span>

### <span data-ttu-id="eaae4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="eaae4-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="eaae4-109">這個命令會使用指向伺服器 serverName 的名稱 aliasName 來建立 Azure SQL Server DNS 別名</span><span class="sxs-lookup"><span data-stu-id="eaae4-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="eaae4-110">參數</span><span class="sxs-lookup"><span data-stu-id="eaae4-110">PARAMETERS</span></span>

### <span data-ttu-id="eaae4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eaae4-111">-AsJob</span></span>
<span data-ttu-id="eaae4-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eaae4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eaae4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaae4-113">-DefaultProfile</span></span>
<span data-ttu-id="eaae4-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eaae4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaae4-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="eaae4-115">-Name</span></span>
<span data-ttu-id="eaae4-116">Azure Sql Server Dns 別名名稱。</span><span class="sxs-lookup"><span data-stu-id="eaae4-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaae4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaae4-117">-ResourceGroupName</span></span>
<span data-ttu-id="eaae4-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eaae4-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="eaae4-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eaae4-119">-ServerName</span></span>
<span data-ttu-id="eaae4-120">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="eaae4-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="eaae4-121">-確認</span><span class="sxs-lookup"><span data-stu-id="eaae4-121">-Confirm</span></span>
<span data-ttu-id="eaae4-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eaae4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaae4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaae4-123">-WhatIf</span></span>
<span data-ttu-id="eaae4-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eaae4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaae4-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eaae4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaae4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaae4-126">CommonParameters</span></span>
<span data-ttu-id="eaae4-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eaae4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaae4-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="eaae4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaae4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="eaae4-129">INPUTS</span></span>

### <span data-ttu-id="eaae4-130">System.object</span><span class="sxs-lookup"><span data-stu-id="eaae4-130">System.String</span></span>

## <span data-ttu-id="eaae4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="eaae4-131">OUTPUTS</span></span>

### <span data-ttu-id="eaae4-132">AzureSqlServerDnsAliasModel 中的 [ServerDnsAlias]</span><span class="sxs-lookup"><span data-stu-id="eaae4-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="eaae4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="eaae4-133">NOTES</span></span>

## <span data-ttu-id="eaae4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="eaae4-134">RELATED LINKS</span></span>