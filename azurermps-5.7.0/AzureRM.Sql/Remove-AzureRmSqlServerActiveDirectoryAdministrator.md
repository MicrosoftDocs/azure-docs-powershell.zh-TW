---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 0dd74526adbc821fe3e256d2fb59850d5bf72943
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624655"
---
# <span data-ttu-id="98bc7-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="98bc7-101">Remove-AzureRmSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="98bc7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="98bc7-103">移除 SQL Server 的 Azure AD 管理員。</span><span class="sxs-lookup"><span data-stu-id="98bc7-103">Removes an Azure AD administrator for SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98bc7-104">句法</span><span class="sxs-lookup"><span data-stu-id="98bc7-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98bc7-105">說明</span><span class="sxs-lookup"><span data-stu-id="98bc7-105">DESCRIPTION</span></span>
<span data-ttu-id="98bc7-106">**AzureRmSqlServerActiveDirectoryAdministrator** Cmdlet 會將 Azure Active Directory (azure AD) 管理員，在目前的訂閱中移除 AzureSQL 伺服器。</span><span class="sxs-lookup"><span data-stu-id="98bc7-106">The **Remove-AzureRmSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="98bc7-107">示例</span><span class="sxs-lookup"><span data-stu-id="98bc7-107">EXAMPLES</span></span>

### <span data-ttu-id="98bc7-108">範例1：移除系統管理員</span><span class="sxs-lookup"><span data-stu-id="98bc7-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="98bc7-109">這個命令會移除與資源群組 ResourceGroup01 相關聯之伺服器的 Azure AD 系統管理員（名為 Server01）。</span><span class="sxs-lookup"><span data-stu-id="98bc7-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="98bc7-110">參數</span><span class="sxs-lookup"><span data-stu-id="98bc7-110">PARAMETERS</span></span>

### <span data-ttu-id="98bc7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98bc7-111">-DefaultProfile</span></span>
<span data-ttu-id="98bc7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="98bc7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98bc7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="98bc7-113">-Force</span></span>
<span data-ttu-id="98bc7-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="98bc7-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98bc7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98bc7-115">-ResourceGroupName</span></span>
<span data-ttu-id="98bc7-116">指定指派 SQL Server 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="98bc7-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98bc7-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="98bc7-117">-ServerName</span></span>
<span data-ttu-id="98bc7-118">指定此 Cmdlet 移除系統管理員的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="98bc7-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98bc7-119">-確認</span><span class="sxs-lookup"><span data-stu-id="98bc7-119">-Confirm</span></span>
<span data-ttu-id="98bc7-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="98bc7-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98bc7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98bc7-121">-WhatIf</span></span>
<span data-ttu-id="98bc7-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98bc7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98bc7-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98bc7-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98bc7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98bc7-124">CommonParameters</span></span>
<span data-ttu-id="98bc7-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98bc7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98bc7-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="98bc7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98bc7-127">輸入</span><span class="sxs-lookup"><span data-stu-id="98bc7-127">INPUTS</span></span>

### <span data-ttu-id="98bc7-128">AzureSqlServerActiveDirectoryAdministratorModel 中的 [ServerActiveDirectoryAdministrator]</span><span class="sxs-lookup"><span data-stu-id="98bc7-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="98bc7-129">輸出</span><span class="sxs-lookup"><span data-stu-id="98bc7-129">OUTPUTS</span></span>

### <span data-ttu-id="98bc7-130">AzureSqlServerActiveDirectoryAdministratorModel 中的 [ServerActiveDirectoryAdministrator]</span><span class="sxs-lookup"><span data-stu-id="98bc7-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="98bc7-131">筆記</span><span class="sxs-lookup"><span data-stu-id="98bc7-131">NOTES</span></span>

## <span data-ttu-id="98bc7-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="98bc7-132">RELATED LINKS</span></span>

[<span data-ttu-id="98bc7-133">AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="98bc7-133">Get-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="98bc7-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="98bc7-134">Set-AzureRmSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzureRmSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="98bc7-135">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="98bc7-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

