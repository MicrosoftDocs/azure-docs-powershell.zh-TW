---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 5e9a4e25d54be7282e4d2f0b5f83471140241c58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623886"
---
# <span data-ttu-id="2d85d-101">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d85d-101">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="2d85d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d85d-102">SYNOPSIS</span></span>
<span data-ttu-id="2d85d-103">在伺服器上設定威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="2d85d-103">Sets a threat detection policy on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d85d-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d85d-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d85d-105">說明</span><span class="sxs-lookup"><span data-stu-id="2d85d-105">DESCRIPTION</span></span>
<span data-ttu-id="2d85d-106">**AzureRmSqlServerThreatDetectionPolicy** Cmdlet 會在 Azure SQL server 上設定威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="2d85d-106">The **Set-AzureRmSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="2d85d-107">若要在伺服器上啟用威脅偵測，必須在該伺服器上啟用審核原則。</span><span class="sxs-lookup"><span data-stu-id="2d85d-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="2d85d-108">若要使用這個 Cmdlet，請指定 *ResourceGroupName* 和 ServerName 參數來識別伺服器。</span><span class="sxs-lookup"><span data-stu-id="2d85d-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="2d85d-109">示例</span><span class="sxs-lookup"><span data-stu-id="2d85d-109">EXAMPLES</span></span>

### <span data-ttu-id="2d85d-110">範例1：為資料庫設定威脅偵測原則</span><span class="sxs-lookup"><span data-stu-id="2d85d-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="2d85d-111">這個命令會為名為 Server01 的伺服器設定威脅偵測原則。</span><span class="sxs-lookup"><span data-stu-id="2d85d-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="2d85d-112">參數</span><span class="sxs-lookup"><span data-stu-id="2d85d-112">PARAMETERS</span></span>

### <span data-ttu-id="2d85d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d85d-113">-DefaultProfile</span></span>
<span data-ttu-id="2d85d-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2d85d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d85d-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="2d85d-115">-EmailAdmins</span></span>
<span data-ttu-id="2d85d-116">指定威脅偵測原則是否使用電子郵件與管理員聯絡。</span><span class="sxs-lookup"><span data-stu-id="2d85d-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d85d-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="2d85d-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="2d85d-118">指定要從原則中排除的偵測類型陣列。</span><span class="sxs-lookup"><span data-stu-id="2d85d-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="2d85d-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2d85d-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2d85d-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="2d85d-120">Sql_Injection</span></span>
- <span data-ttu-id="2d85d-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="2d85d-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="2d85d-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="2d85d-122">Access_Anomaly</span></span>
- <span data-ttu-id="2d85d-123">所有</span><span class="sxs-lookup"><span data-stu-id="2d85d-123">None</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]
Parameter Sets: (All)
Aliases:
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d85d-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="2d85d-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="2d85d-125">指定原則要傳送提醒的電子郵件地址清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="2d85d-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d85d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d85d-126">-PassThru</span></span>
<span data-ttu-id="2d85d-127">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="2d85d-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2d85d-128">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="2d85d-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2d85d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d85d-129">-ResourceGroupName</span></span>
<span data-ttu-id="2d85d-130">指定伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d85d-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="2d85d-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2d85d-131">-RetentionInDays</span></span>
<span data-ttu-id="2d85d-132">審計記錄的保留天數</span><span class="sxs-lookup"><span data-stu-id="2d85d-132">The number of retention days for the audit logs</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d85d-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2d85d-133">-ServerName</span></span>
<span data-ttu-id="2d85d-134">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d85d-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="2d85d-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2d85d-135">-StorageAccountName</span></span>
<span data-ttu-id="2d85d-136">指定要使用的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2d85d-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="2d85d-137">不允許使用萬用字元。</span><span class="sxs-lookup"><span data-stu-id="2d85d-137">Wildcards are not permitted.</span></span> <span data-ttu-id="2d85d-138">不需要此參數。</span><span class="sxs-lookup"><span data-stu-id="2d85d-138">This parameter is not required.</span></span> <span data-ttu-id="2d85d-139">如果未提供此參數，則 Cmdlet 會使用先前在資料庫的威脅偵測原則中定義的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="2d85d-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="2d85d-140">如果這是已定義資料庫 theat 偵測原則的第一次，且未提供此參數，則 Cmdlet 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="2d85d-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d85d-141">-確認</span><span class="sxs-lookup"><span data-stu-id="2d85d-141">-Confirm</span></span>
<span data-ttu-id="2d85d-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2d85d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d85d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d85d-143">-WhatIf</span></span>
<span data-ttu-id="2d85d-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2d85d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d85d-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d85d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d85d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d85d-146">CommonParameters</span></span>
<span data-ttu-id="2d85d-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d85d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d85d-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2d85d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d85d-149">輸入</span><span class="sxs-lookup"><span data-stu-id="2d85d-149">INPUTS</span></span>

### <span data-ttu-id="2d85d-150">System.object</span><span class="sxs-lookup"><span data-stu-id="2d85d-150">System.String</span></span>

### <span data-ttu-id="2d85d-151">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2d85d-151">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2d85d-152">DetectionType [] 的 ThreatDetection [）]</span><span class="sxs-lookup"><span data-stu-id="2d85d-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="2d85d-153">System.object "1 [[System. UInt32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2d85d-153">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="2d85d-154">輸出</span><span class="sxs-lookup"><span data-stu-id="2d85d-154">OUTPUTS</span></span>

### <span data-ttu-id="2d85d-155">ServerThreatDetectionPolicyModel 中的 [ThreatDetection]</span><span class="sxs-lookup"><span data-stu-id="2d85d-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="2d85d-156">筆記</span><span class="sxs-lookup"><span data-stu-id="2d85d-156">NOTES</span></span>

## <span data-ttu-id="2d85d-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d85d-157">RELATED LINKS</span></span>

[<span data-ttu-id="2d85d-158">AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d85d-158">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="2d85d-159">移除-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d85d-159">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="2d85d-160">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="2d85d-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)