---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 44339cb39396b18660d17bdbad0e597ded30ad18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792581"
---
# <span data-ttu-id="a63bf-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a63bf-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="a63bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a63bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a63bf-103">為 SQL Server 置備 Azure AD 管理員。</span><span class="sxs-lookup"><span data-stu-id="a63bf-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="a63bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="a63bf-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a63bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="a63bf-105">DESCRIPTION</span></span>
<span data-ttu-id="a63bf-106">AzSqlServerActiveDirectoryAdministrator Cmdlet 會在目前的訂閱中，為 AzureSQL Server (Azure AD) 管理員 **設定** Azure Active Directory。</span><span class="sxs-lookup"><span data-stu-id="a63bf-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="a63bf-107">您一次只能提供一個系統管理員。</span><span class="sxs-lookup"><span data-stu-id="a63bf-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="a63bf-108">下列 Azure AD 的成員可設為 SQL Server 系統管理員：</span><span class="sxs-lookup"><span data-stu-id="a63bf-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="a63bf-109">Azure AD 的原生成員</span><span class="sxs-lookup"><span data-stu-id="a63bf-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="a63bf-110">Azure AD 的聯合成員</span><span class="sxs-lookup"><span data-stu-id="a63bf-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="a63bf-111">從其他屬於原生或同盟成員的 Azure 廣告匯入的成員</span><span class="sxs-lookup"><span data-stu-id="a63bf-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="a63bf-112">已建立為安全性群組的 Azure AD 群組（例如 Outlook.com、Hotmail.com 或 Live.com 網域中的帳戶）不受系統管理員支援。</span><span class="sxs-lookup"><span data-stu-id="a63bf-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="a63bf-113">其他來賓帳戶（例如 Gmail.com 或 Yahoo.com 網域中的帳戶）不受系統管理員支援。</span><span class="sxs-lookup"><span data-stu-id="a63bf-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="a63bf-114">我們建議您以系統管理員身分提供專用的 Azure AD 群組。</span><span class="sxs-lookup"><span data-stu-id="a63bf-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="a63bf-115">示例</span><span class="sxs-lookup"><span data-stu-id="a63bf-115">EXAMPLES</span></span>

### <span data-ttu-id="a63bf-116">範例1：為伺服器提供管理員群組</span><span class="sxs-lookup"><span data-stu-id="a63bf-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a63bf-117">這個命令會為名為 Server01 的伺服器提供一個名為 Dba 的 Azure AD 管理員群組。</span><span class="sxs-lookup"><span data-stu-id="a63bf-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="a63bf-118">此伺服器與資源群組 ResourceGroup01 相關聯。</span><span class="sxs-lookup"><span data-stu-id="a63bf-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="a63bf-119">範例2：為伺服器提供管理員使用者</span><span class="sxs-lookup"><span data-stu-id="a63bf-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="a63bf-120">這個命令會將 Azure AD 使用者設為名為 Server01 的伺服器的管理員。</span><span class="sxs-lookup"><span data-stu-id="a63bf-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="a63bf-121">範例3：透過指定管理員群組的識別碼來提供該群組</span><span class="sxs-lookup"><span data-stu-id="a63bf-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a63bf-122">這個命令會為名為 Server01 的伺服器提供一個名為 Dba 的 Azure AD 管理員群組。</span><span class="sxs-lookup"><span data-stu-id="a63bf-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="a63bf-123">命令會指定 *ObjectId* 參數的 ID。</span><span class="sxs-lookup"><span data-stu-id="a63bf-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="a63bf-124">這可確保即使群組的顯示名稱不是唯一的，命令也會成功。</span><span class="sxs-lookup"><span data-stu-id="a63bf-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="a63bf-125">參數</span><span class="sxs-lookup"><span data-stu-id="a63bf-125">PARAMETERS</span></span>

### <span data-ttu-id="a63bf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a63bf-126">-DefaultProfile</span></span>
<span data-ttu-id="a63bf-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a63bf-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a63bf-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a63bf-128">-DisplayName</span></span>
<span data-ttu-id="a63bf-129">指定此 Cmdlet 所配之 Azure AD 管理員的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a63bf-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

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

### <span data-ttu-id="a63bf-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a63bf-130">-ObjectId</span></span>
<span data-ttu-id="a63bf-131">指定此 Cmdlet 所配之 Azure AD 管理員的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a63bf-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="a63bf-132">如果顯示名稱不是唯一的，您必須指定此參數的值。</span><span class="sxs-lookup"><span data-stu-id="a63bf-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a63bf-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a63bf-133">-ResourceGroupName</span></span>
<span data-ttu-id="a63bf-134">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a63bf-134">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a63bf-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a63bf-135">-ServerName</span></span>
<span data-ttu-id="a63bf-136">指定此 Cmdlet 為其提供管理員的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="a63bf-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

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

### <span data-ttu-id="a63bf-137">-確認</span><span class="sxs-lookup"><span data-stu-id="a63bf-137">-Confirm</span></span>
<span data-ttu-id="a63bf-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a63bf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a63bf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a63bf-139">-WhatIf</span></span>
<span data-ttu-id="a63bf-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a63bf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a63bf-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a63bf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a63bf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a63bf-142">CommonParameters</span></span>
<span data-ttu-id="a63bf-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a63bf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a63bf-144">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a63bf-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a63bf-145">輸入</span><span class="sxs-lookup"><span data-stu-id="a63bf-145">INPUTS</span></span>

### <span data-ttu-id="a63bf-146">System.object</span><span class="sxs-lookup"><span data-stu-id="a63bf-146">System.String</span></span>

### <span data-ttu-id="a63bf-147">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="a63bf-147">System.Guid</span></span>

## <span data-ttu-id="a63bf-148">輸出</span><span class="sxs-lookup"><span data-stu-id="a63bf-148">OUTPUTS</span></span>

### <span data-ttu-id="a63bf-149">AzureSqlServerActiveDirectoryAdministratorModel 中的 [ServerActiveDirectoryAdministrator]</span><span class="sxs-lookup"><span data-stu-id="a63bf-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="a63bf-150">筆記</span><span class="sxs-lookup"><span data-stu-id="a63bf-150">NOTES</span></span>

## <span data-ttu-id="a63bf-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="a63bf-151">RELATED LINKS</span></span>

[<span data-ttu-id="a63bf-152">AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a63bf-152">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a63bf-153">移除-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a63bf-153">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a63bf-154">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="a63bf-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

