---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 09d27926f489feea397c98a217840bb973e002ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956827"
---
# <span data-ttu-id="23dbf-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="23dbf-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="23dbf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="23dbf-103">取得 SCDPM 和 Azure 備份管理伺服器。</span><span class="sxs-lookup"><span data-stu-id="23dbf-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="23dbf-104">句法</span><span class="sxs-lookup"><span data-stu-id="23dbf-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23dbf-105">說明</span><span class="sxs-lookup"><span data-stu-id="23dbf-105">DESCRIPTION</span></span>
<span data-ttu-id="23dbf-106">**AzRecoveryServicesBackupManagementServer** Cmdlet 會取得在電子倉庫中註冊的備份管理伺服器清單。</span><span class="sxs-lookup"><span data-stu-id="23dbf-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="23dbf-107">備份管理伺服器有兩種類型：系統中心資料保護管理員 (SCDPM) 和 Azure 備份管理伺服器。</span><span class="sxs-lookup"><span data-stu-id="23dbf-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="23dbf-108">備份管理伺服器會另行安裝，以管理備份業務流程。</span><span class="sxs-lookup"><span data-stu-id="23dbf-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="23dbf-109">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23dbf-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="23dbf-110">示例</span><span class="sxs-lookup"><span data-stu-id="23dbf-110">EXAMPLES</span></span>

### <span data-ttu-id="23dbf-111">範例1：取得所有備份管理伺服器</span><span class="sxs-lookup"><span data-stu-id="23dbf-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="23dbf-112">這個命令會取得所有使用保存庫註冊的備份管理伺服器。</span><span class="sxs-lookup"><span data-stu-id="23dbf-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="23dbf-113">參數</span><span class="sxs-lookup"><span data-stu-id="23dbf-113">PARAMETERS</span></span>

### <span data-ttu-id="23dbf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23dbf-114">-DefaultProfile</span></span>
<span data-ttu-id="23dbf-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23dbf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23dbf-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="23dbf-116">-Name</span></span>
<span data-ttu-id="23dbf-117">指定要取得之備份管理伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="23dbf-117">Specifies the name of the Backup management server to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23dbf-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="23dbf-118">-VaultId</span></span>
<span data-ttu-id="23dbf-119">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="23dbf-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="23dbf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23dbf-120">CommonParameters</span></span>
<span data-ttu-id="23dbf-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23dbf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23dbf-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="23dbf-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23dbf-123">輸入</span><span class="sxs-lookup"><span data-stu-id="23dbf-123">INPUTS</span></span>

### <span data-ttu-id="23dbf-124">System.object</span><span class="sxs-lookup"><span data-stu-id="23dbf-124">System.String</span></span>

## <span data-ttu-id="23dbf-125">輸出</span><span class="sxs-lookup"><span data-stu-id="23dbf-125">OUTPUTS</span></span>

### <span data-ttu-id="23dbf-126">BackupEngineBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="23dbf-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="23dbf-127">筆記</span><span class="sxs-lookup"><span data-stu-id="23dbf-127">NOTES</span></span>

## <span data-ttu-id="23dbf-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="23dbf-128">RELATED LINKS</span></span>

[<span data-ttu-id="23dbf-129">取消註冊-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="23dbf-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)

