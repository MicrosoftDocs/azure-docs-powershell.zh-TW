---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 410cd159aacadd83ee03c6e628339be38ca42d8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791888"
---
# <span data-ttu-id="9250f-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="9250f-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="9250f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9250f-102">SYNOPSIS</span></span>
<span data-ttu-id="9250f-103">取得備份屬性。</span><span class="sxs-lookup"><span data-stu-id="9250f-103">Gets Backup properties.</span></span>

## <span data-ttu-id="9250f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9250f-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9250f-105">說明</span><span class="sxs-lookup"><span data-stu-id="9250f-105">DESCRIPTION</span></span>
<span data-ttu-id="9250f-106">**AzRecoveryServicesBackupProperty** Cmdlet 會取得恢復服務電子倉庫的備份屬性。</span><span class="sxs-lookup"><span data-stu-id="9250f-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="9250f-107">示例</span><span class="sxs-lookup"><span data-stu-id="9250f-107">EXAMPLES</span></span>

### <span data-ttu-id="9250f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9250f-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="9250f-109">取得保存庫的備份保存庫屬性。</span><span class="sxs-lookup"><span data-stu-id="9250f-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="9250f-110">參數</span><span class="sxs-lookup"><span data-stu-id="9250f-110">PARAMETERS</span></span>

### <span data-ttu-id="9250f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9250f-111">-DefaultProfile</span></span>
<span data-ttu-id="9250f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9250f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9250f-113">-保存庫</span><span class="sxs-lookup"><span data-stu-id="9250f-113">-Vault</span></span>
<span data-ttu-id="9250f-114">指定保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9250f-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="9250f-115">Vault 必須是 **AzureRmRecoveryServicesVault** 物件。</span><span class="sxs-lookup"><span data-stu-id="9250f-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="9250f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9250f-116">CommonParameters</span></span>
<span data-ttu-id="9250f-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9250f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9250f-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9250f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9250f-119">輸入</span><span class="sxs-lookup"><span data-stu-id="9250f-119">INPUTS</span></span>

### <span data-ttu-id="9250f-120">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9250f-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="9250f-121">輸出</span><span class="sxs-lookup"><span data-stu-id="9250f-121">OUTPUTS</span></span>

### <span data-ttu-id="9250f-122">ASRVaultBackupProperties 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9250f-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="9250f-123">筆記</span><span class="sxs-lookup"><span data-stu-id="9250f-123">NOTES</span></span>

## <span data-ttu-id="9250f-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="9250f-124">RELATED LINKS</span></span>