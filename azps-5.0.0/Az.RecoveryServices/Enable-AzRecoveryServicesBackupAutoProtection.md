---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: e47ed3d2859a78837c57803789721005a5248204
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286432"
---
# <span data-ttu-id="93991-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="93991-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="93991-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93991-102">SYNOPSIS</span></span>
<span data-ttu-id="93991-103">**Enable-AzRecoveryServicesBackupAutoProtection** Cmdlet 會使用提供的原則，為指定實例中的目前及未來的任何 SQL 內容設定自動保護。</span><span class="sxs-lookup"><span data-stu-id="93991-103">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets up automatic protection of current and any future SQL DBs within the given instance with the supplied policy.</span></span>

## <span data-ttu-id="93991-104">句法</span><span class="sxs-lookup"><span data-stu-id="93991-104">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93991-105">說明</span><span class="sxs-lookup"><span data-stu-id="93991-105">DESCRIPTION</span></span>
<span data-ttu-id="93991-106">這個命令可讓使用者自動保護所有現有的未受保護的 SQL 資料庫，以及稍後會以指定原則新增的任何資料庫。</span><span class="sxs-lookup"><span data-stu-id="93991-106">This command allows users to automatically protect all existing unprotected SQL DBs and any DB which will be added later with the given policy.</span></span>  <span data-ttu-id="93991-107">由於此指示是要備份所有未來的內容，因此，Azure 備份服務會定期針對任何新的系統來掃描自動保護的容器，並自動保護它們。</span><span class="sxs-lookup"><span data-stu-id="93991-107">Since the instruction is to back up all future DBs, the operation is done at a SQLInstance level, Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="93991-108">示例</span><span class="sxs-lookup"><span data-stu-id="93991-108">EXAMPLES</span></span>

### <span data-ttu-id="93991-109">範例1</span><span class="sxs-lookup"><span data-stu-id="93991-109">Example 1</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultSQLPolicy"
PS C:\> $SQLInstance = Get-AzRecoveryServicesBackupProtectableItem -workloadType MSSQL -ItemType SQLInstance -VaultId $targetVault.ID -Name "MSSQLInstance" -ServerName "TestSQLServer" 
PS C:\> Enable-AzRecoveryServicesBackupAutoProtection -InputItem $SQLInstance -BackupManagementType AzureWorkload -WorkloadType MSSQL -Policy $Pol -VaultId $targetvault.ID 
```

<span data-ttu-id="93991-110">第一個 Cmdlet 會取得預設原則物件，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="93991-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="93991-111">第二個 Cmdlet 會提取相關的 SQLInstance，這是可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="93991-111">The second cmdlet fetches the relevant SQLInstance which is a protectable item.</span></span> <span data-ttu-id="93991-112">然後，第三個命令會使用 $Pol 中的原則，為此實例設定自動保護。</span><span class="sxs-lookup"><span data-stu-id="93991-112">The 3rd command then sets up auto protection for this instance using the policy in $Pol.</span></span>

### <span data-ttu-id="93991-113">範例2</span><span class="sxs-lookup"><span data-stu-id="93991-113">Example 2</span></span>

<span data-ttu-id="93991-114">這個命令可讓使用者自動保護所有現有未受保護的資料庫，以及稍後會以指定原則新增的任何 DB。</span><span class="sxs-lookup"><span data-stu-id="93991-114">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="93991-115"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="93991-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType AzureVM -InputItem <ProtectableItemBase> -Policy $Pol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="93991-116">參數</span><span class="sxs-lookup"><span data-stu-id="93991-116">PARAMETERS</span></span>

### <span data-ttu-id="93991-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="93991-117">-BackupManagementType</span></span>
<span data-ttu-id="93991-118">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="93991-118">The class of resources being protected.</span></span> <span data-ttu-id="93991-119">這個 Cmdlet 支援的值目前為 MAB、AzureWorkload、Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="93991-119">Currently the values supported for this cmdlet are MAB, AzureWorkload, AzureVM</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93991-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93991-120">-DefaultProfile</span></span>
<span data-ttu-id="93991-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="93991-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93991-122">-InputItem</span><span class="sxs-lookup"><span data-stu-id="93991-122">-InputItem</span></span>
<span data-ttu-id="93991-123">指定可以傳送成輸入的可保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="93991-123">Specifies the protectable item object that can be passed as an input.</span></span> <span data-ttu-id="93991-124">目前支援的值是 "SQLInstance" 類型的 protectableItem 物件。</span><span class="sxs-lookup"><span data-stu-id="93991-124">The current supported value is a protectableItem object of type "SQLInstance".</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93991-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93991-125">-PassThru</span></span>
<span data-ttu-id="93991-126">傳回自動保護的結果。</span><span class="sxs-lookup"><span data-stu-id="93991-126">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="93991-127">-原則</span><span class="sxs-lookup"><span data-stu-id="93991-127">-Policy</span></span>
<span data-ttu-id="93991-128">保護原則物件。</span><span class="sxs-lookup"><span data-stu-id="93991-128">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93991-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="93991-129">-VaultId</span></span>
<span data-ttu-id="93991-130">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="93991-130">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93991-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="93991-131">-WorkloadType</span></span>
<span data-ttu-id="93991-132">資源的工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="93991-132">Workload type of the resource.</span></span> <span data-ttu-id="93991-133">目前支援的值為 Add-azurevm、WindowsServer、MSSQL</span><span class="sxs-lookup"><span data-stu-id="93991-133">The current supported values are AzureVM, WindowsServer, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93991-134">-確認</span><span class="sxs-lookup"><span data-stu-id="93991-134">-Confirm</span></span>
<span data-ttu-id="93991-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="93991-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93991-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93991-136">-WhatIf</span></span>
<span data-ttu-id="93991-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93991-137">Shows what would happen if the cmdlet runs.</span></span>


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

### <span data-ttu-id="93991-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93991-138">CommonParameters</span></span>
<span data-ttu-id="93991-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93991-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93991-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="93991-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93991-141">輸入</span><span class="sxs-lookup"><span data-stu-id="93991-141">INPUTS</span></span>

### <span data-ttu-id="93991-142">System.object</span><span class="sxs-lookup"><span data-stu-id="93991-142">System.String</span></span>

## <span data-ttu-id="93991-143">輸出</span><span class="sxs-lookup"><span data-stu-id="93991-143">OUTPUTS</span></span>

### <span data-ttu-id="93991-144">System.object</span><span class="sxs-lookup"><span data-stu-id="93991-144">System.Object</span></span>

## <span data-ttu-id="93991-145">筆記</span><span class="sxs-lookup"><span data-stu-id="93991-145">NOTES</span></span>

## <span data-ttu-id="93991-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="93991-146">RELATED LINKS</span></span>