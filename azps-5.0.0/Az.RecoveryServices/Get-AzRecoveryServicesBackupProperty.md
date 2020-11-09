---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286408"
---
# <span data-ttu-id="8a7d5-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="8a7d5-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="8a7d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a7d5-102">SYNOPSIS</span></span>
<span data-ttu-id="8a7d5-103">取得備份屬性。</span><span class="sxs-lookup"><span data-stu-id="8a7d5-103">Gets Backup properties.</span></span>

## <span data-ttu-id="8a7d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a7d5-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a7d5-105">說明</span><span class="sxs-lookup"><span data-stu-id="8a7d5-105">DESCRIPTION</span></span>
<span data-ttu-id="8a7d5-106">**AzRecoveryServicesBackupProperty** Cmdlet 會取得恢復服務電子倉庫的備份屬性。</span><span class="sxs-lookup"><span data-stu-id="8a7d5-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="8a7d5-107">示例</span><span class="sxs-lookup"><span data-stu-id="8a7d5-107">EXAMPLES</span></span>

### <span data-ttu-id="8a7d5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8a7d5-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="8a7d5-109">取得保存庫的備份保存庫屬性。</span><span class="sxs-lookup"><span data-stu-id="8a7d5-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="8a7d5-110">參數</span><span class="sxs-lookup"><span data-stu-id="8a7d5-110">PARAMETERS</span></span>

### <span data-ttu-id="8a7d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a7d5-111">-DefaultProfile</span></span>
<span data-ttu-id="8a7d5-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a7d5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a7d5-113">-保存庫</span><span class="sxs-lookup"><span data-stu-id="8a7d5-113">-Vault</span></span>
<span data-ttu-id="8a7d5-114">指定保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a7d5-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="8a7d5-115">Vault 必須是 **AzureRmRecoveryServicesVault** 物件。</span><span class="sxs-lookup"><span data-stu-id="8a7d5-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a7d5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a7d5-116">CommonParameters</span></span>
<span data-ttu-id="8a7d5-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a7d5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a7d5-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8a7d5-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a7d5-119">輸入</span><span class="sxs-lookup"><span data-stu-id="8a7d5-119">INPUTS</span></span>

### <span data-ttu-id="8a7d5-120">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8a7d5-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="8a7d5-121">輸出</span><span class="sxs-lookup"><span data-stu-id="8a7d5-121">OUTPUTS</span></span>

### <span data-ttu-id="8a7d5-122">ASRVaultBackupProperties 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8a7d5-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="8a7d5-123">筆記</span><span class="sxs-lookup"><span data-stu-id="8a7d5-123">NOTES</span></span>

## <span data-ttu-id="8a7d5-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a7d5-124">RELATED LINKS</span></span>