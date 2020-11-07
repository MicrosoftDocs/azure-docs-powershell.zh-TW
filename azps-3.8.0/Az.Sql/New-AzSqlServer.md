---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: 7a28e29e6ee517d15c6edcd462c274ef3a7dbced
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799054"
---
# <span data-ttu-id="73ab4-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="73ab4-101">New-AzSqlServer</span></span>

## <span data-ttu-id="73ab4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="73ab4-103">建立 SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="73ab4-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="73ab4-104">句法</span><span class="sxs-lookup"><span data-stu-id="73ab4-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-PublicNetworkAccess <String>] [-MinimalTlsVersion <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73ab4-105">說明</span><span class="sxs-lookup"><span data-stu-id="73ab4-105">DESCRIPTION</span></span>
<span data-ttu-id="73ab4-106">**新的-AzSqlServer** Cmdlet 會建立 Azure SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="73ab4-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="73ab4-107">示例</span><span class="sxs-lookup"><span data-stu-id="73ab4-107">EXAMPLES</span></span>

### <span data-ttu-id="73ab4-108">範例1：建立新的 Azure SQL 資料庫伺服器</span><span class="sxs-lookup"><span data-stu-id="73ab4-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="73ab4-109">這個命令會建立版本 12 Azure SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="73ab4-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="73ab4-110">參數</span><span class="sxs-lookup"><span data-stu-id="73ab4-110">PARAMETERS</span></span>

### <span data-ttu-id="73ab4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73ab4-111">-AsJob</span></span>
<span data-ttu-id="73ab4-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="73ab4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73ab4-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="73ab4-113">-AssignIdentity</span></span>
<span data-ttu-id="73ab4-114">針對此伺服器產生並指派 Azure Active Directory 身分識別，以搭配諸如 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="73ab4-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="73ab4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73ab4-115">-DefaultProfile</span></span>
<span data-ttu-id="73ab4-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="73ab4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73ab4-117">-位置</span><span class="sxs-lookup"><span data-stu-id="73ab4-117">-Location</span></span>
<span data-ttu-id="73ab4-118">指定此 Cmdlet 建立伺服器的資料中心位置。</span><span class="sxs-lookup"><span data-stu-id="73ab4-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="73ab4-119">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="73ab4-119">-PublicNetworkAccess</span></span>
<span data-ttu-id="73ab4-120">接受標誌、啟用/停用，以指定是否允許公用網路存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="73ab4-120">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="73ab4-121">停用時，只有透過私人連結建立的連線才能到達此伺服器。</span><span class="sxs-lookup"><span data-stu-id="73ab4-121">When disabled, only connections made through Private Links can reach this server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ab4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73ab4-122">-ResourceGroupName</span></span>
<span data-ttu-id="73ab4-123">指定此 Cmdlet 指派伺服器的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="73ab4-123">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="73ab4-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="73ab4-124">-ServerName</span></span>
<span data-ttu-id="73ab4-125">指定新伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="73ab4-125">Specifies the name of the new server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ab4-126">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="73ab4-126">-ServerVersion</span></span>
<span data-ttu-id="73ab4-127">指定新伺服器的版本。</span><span class="sxs-lookup"><span data-stu-id="73ab4-127">Specifies the version of the new server.</span></span> <span data-ttu-id="73ab4-128">此參數可接受的值為：2.0 和12.0。</span><span class="sxs-lookup"><span data-stu-id="73ab4-128">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="73ab4-129">指定2.0 來建立版本11伺服器，或指定12.0 以建立版本12的伺服器。</span><span class="sxs-lookup"><span data-stu-id="73ab4-129">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ab4-130">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="73ab4-130">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="73ab4-131">指定新伺服器的 SQL 資料庫伺服器管理員認證。</span><span class="sxs-lookup"><span data-stu-id="73ab4-131">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="73ab4-132">若要取得 **PSCredential** 物件，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73ab4-132">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="73ab4-133">如需詳細資訊，請輸入 `Get-Help
Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="73ab4-133">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ab4-134">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="73ab4-134">-MinimalTlsVersion</span></span>
<span data-ttu-id="73ab4-135">要針對 Sql Server 強制執行的最小 TLS 版本</span><span class="sxs-lookup"><span data-stu-id="73ab4-135">The minimal TLS version to enforce for Sql Server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ab4-136">-標記</span><span class="sxs-lookup"><span data-stu-id="73ab4-136">-Tags</span></span>
<span data-ttu-id="73ab4-137">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="73ab4-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="73ab4-138">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="73ab4-138">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ab4-139">-確認</span><span class="sxs-lookup"><span data-stu-id="73ab4-139">-Confirm</span></span>
<span data-ttu-id="73ab4-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="73ab4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73ab4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73ab4-141">-WhatIf</span></span>
<span data-ttu-id="73ab4-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="73ab4-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73ab4-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73ab4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73ab4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ab4-144">CommonParameters</span></span>
<span data-ttu-id="73ab4-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73ab4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ab4-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="73ab4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ab4-147">輸入</span><span class="sxs-lookup"><span data-stu-id="73ab4-147">INPUTS</span></span>

### <span data-ttu-id="73ab4-148">System.object</span><span class="sxs-lookup"><span data-stu-id="73ab4-148">System.String</span></span>

## <span data-ttu-id="73ab4-149">輸出</span><span class="sxs-lookup"><span data-stu-id="73ab4-149">OUTPUTS</span></span>

### <span data-ttu-id="73ab4-150">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="73ab4-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="73ab4-151">筆記</span><span class="sxs-lookup"><span data-stu-id="73ab4-151">NOTES</span></span>

## <span data-ttu-id="73ab4-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="73ab4-152">RELATED LINKS</span></span>

[<span data-ttu-id="73ab4-153">AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="73ab4-153">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="73ab4-154">移除-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="73ab4-154">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="73ab4-155">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="73ab4-155">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="73ab4-156">新-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="73ab4-156">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="73ab4-157">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="73ab4-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)