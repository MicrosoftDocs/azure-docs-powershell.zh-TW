---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 92720cd486abd5f79be7f044e3fe98d038976a82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623682"
---
# <span data-ttu-id="d372a-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="d372a-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="d372a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d372a-102">SYNOPSIS</span></span>
<span data-ttu-id="d372a-103">更新 Azure SQL 彈性 Pool Advisor 的自動執行狀態。</span><span class="sxs-lookup"><span data-stu-id="d372a-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d372a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d372a-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d372a-105">說明</span><span class="sxs-lookup"><span data-stu-id="d372a-105">DESCRIPTION</span></span>
<span data-ttu-id="d372a-106">**AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** Cmdlet 會為 Azure SQL 彈性 Pool Advisor 設定自動執行屬性。</span><span class="sxs-lookup"><span data-stu-id="d372a-106">The **Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="d372a-107">示例</span><span class="sxs-lookup"><span data-stu-id="d372a-107">EXAMPLES</span></span>

### <span data-ttu-id="d372a-108">範例1：啟用 advisor 的自動執行</span><span class="sxs-lookup"><span data-stu-id="d372a-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
'Enabled'ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : ElasticPool
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="d372a-109">這個命令會將名為 CreateIndex 的 advisor 的自動執行狀態設為 [啟用]。</span><span class="sxs-lookup"><span data-stu-id="d372a-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="d372a-110">參數</span><span class="sxs-lookup"><span data-stu-id="d372a-110">PARAMETERS</span></span>

### <span data-ttu-id="d372a-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="d372a-111">-AdvisorName</span></span>
<span data-ttu-id="d372a-112">指定此 Cmdlet 更新自動執行狀態的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="d372a-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="d372a-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="d372a-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="d372a-114">指定此 Cmdlet 更新自動執行狀態的新值。</span><span class="sxs-lookup"><span data-stu-id="d372a-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="d372a-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d372a-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d372a-116">後</span><span class="sxs-lookup"><span data-stu-id="d372a-116">Enabled</span></span>
- <span data-ttu-id="d372a-117">禁止</span><span class="sxs-lookup"><span data-stu-id="d372a-117">Disabled</span></span>
- <span data-ttu-id="d372a-118">設置</span><span class="sxs-lookup"><span data-stu-id="d372a-118">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d372a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d372a-119">-DefaultProfile</span></span>
<span data-ttu-id="d372a-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d372a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d372a-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d372a-121">-ElasticPoolName</span></span>
<span data-ttu-id="d372a-122">指定彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="d372a-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="d372a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d372a-123">-ResourceGroupName</span></span>
<span data-ttu-id="d372a-124">指定包含此彈性池之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d372a-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="d372a-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d372a-125">-ServerName</span></span>
<span data-ttu-id="d372a-126">指定彈性池所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d372a-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="d372a-127">-確認</span><span class="sxs-lookup"><span data-stu-id="d372a-127">-Confirm</span></span>
<span data-ttu-id="d372a-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d372a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d372a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d372a-129">-WhatIf</span></span>
<span data-ttu-id="d372a-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d372a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d372a-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d372a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d372a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d372a-132">CommonParameters</span></span>
<span data-ttu-id="d372a-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d372a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d372a-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d372a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d372a-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d372a-135">INPUTS</span></span>

### <span data-ttu-id="d372a-136">System.object</span><span class="sxs-lookup"><span data-stu-id="d372a-136">System.String</span></span>

### <span data-ttu-id="d372a-137">AdvisorAutoExecuteStatus 中的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="d372a-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="d372a-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d372a-138">OUTPUTS</span></span>

### <span data-ttu-id="d372a-139">AzureSqlElasticPoolAdvisorModel 中的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="d372a-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="d372a-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d372a-140">NOTES</span></span>
* <span data-ttu-id="d372a-141">關鍵字： azure、azurerm、arm、資源、管理、管理員、sql、彈性池、mssql、advisor</span><span class="sxs-lookup"><span data-stu-id="d372a-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="d372a-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="d372a-142">RELATED LINKS</span></span>

[<span data-ttu-id="d372a-143">AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="d372a-143">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="d372a-144">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="d372a-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)