---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 186ff32138bba0556b05e9674f1711e9425a20c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792569"
---
# <span data-ttu-id="4d978-101">Get-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="4d978-101">Get-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="4d978-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4d978-102">SYNOPSIS</span></span>
<span data-ttu-id="4d978-103">取得資料庫的高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="4d978-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="4d978-104">句法</span><span class="sxs-lookup"><span data-stu-id="4d978-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSettings [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d978-105">說明</span><span class="sxs-lookup"><span data-stu-id="4d978-105">DESCRIPTION</span></span>
<span data-ttu-id="4d978-106">**AzSqlDatabaseAdvancedThreatProtectionSettings** Cmdlet 會取得 Azure SQL 資料庫的高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="4d978-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSettings** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="4d978-107">若要使用這個 Cmdlet，請指定 *ResourceGroupName* 、 *ServerName* 和 *DatabaseName* 參數，以識別此 Cmdlet 取得其設定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="4d978-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="4d978-108">示例</span><span class="sxs-lookup"><span data-stu-id="4d978-108">EXAMPLES</span></span>

### <span data-ttu-id="4d978-109">範例1：取得資料庫的高級威脅防護設定</span><span class="sxs-lookup"><span data-stu-id="4d978-109">Example 1: Get the advanced threat protection settings for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="4d978-110">這個命令會取得名為 Database01 的資料庫的高級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="4d978-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="4d978-111">資料庫位於名為 Server01 的伺服器上，該伺服器已指派給資源群組 ResourceGroup11。</span><span class="sxs-lookup"><span data-stu-id="4d978-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="4d978-112">參數</span><span class="sxs-lookup"><span data-stu-id="4d978-112">PARAMETERS</span></span>

### <span data-ttu-id="4d978-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4d978-113">-DatabaseName</span></span>
<span data-ttu-id="4d978-114">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d978-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="4d978-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d978-115">-DefaultProfile</span></span>
<span data-ttu-id="4d978-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4d978-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d978-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d978-117">-ResourceGroupName</span></span>
<span data-ttu-id="4d978-118">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d978-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="4d978-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4d978-119">-ServerName</span></span>
<span data-ttu-id="4d978-120">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d978-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="4d978-121">-確認</span><span class="sxs-lookup"><span data-stu-id="4d978-121">-Confirm</span></span>
<span data-ttu-id="4d978-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4d978-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d978-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d978-123">-WhatIf</span></span>
<span data-ttu-id="4d978-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4d978-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d978-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4d978-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d978-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d978-126">CommonParameters</span></span>
<span data-ttu-id="4d978-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4d978-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d978-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4d978-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d978-129">輸入</span><span class="sxs-lookup"><span data-stu-id="4d978-129">INPUTS</span></span>

### <span data-ttu-id="4d978-130">System.object</span><span class="sxs-lookup"><span data-stu-id="4d978-130">System.String</span></span>

## <span data-ttu-id="4d978-131">輸出</span><span class="sxs-lookup"><span data-stu-id="4d978-131">OUTPUTS</span></span>

### <span data-ttu-id="4d978-132">DatabaseAdvancedThreatProtectionSettingsModel 中的 [ThreatDetection]</span><span class="sxs-lookup"><span data-stu-id="4d978-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="4d978-133">筆記</span><span class="sxs-lookup"><span data-stu-id="4d978-133">NOTES</span></span>

## <span data-ttu-id="4d978-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d978-134">RELATED LINKS</span></span>

[<span data-ttu-id="4d978-135">移除-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="4d978-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSettings.md)


