---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: d8743b12757d5845107d6a38689059b90bf1e287
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625696"
---
# <span data-ttu-id="f1161-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="f1161-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="f1161-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1161-102">SYNOPSIS</span></span>
<span data-ttu-id="f1161-103">設定電子倉庫內容。</span><span class="sxs-lookup"><span data-stu-id="f1161-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1161-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1161-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1161-105">說明</span><span class="sxs-lookup"><span data-stu-id="f1161-105">DESCRIPTION</span></span>
<span data-ttu-id="f1161-106">**AzureRmRecoveryServicesVaultCoNtext** Cmdlet 會設定 Azure Site Recovery 服務的保存庫內容。</span><span class="sxs-lookup"><span data-stu-id="f1161-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="f1161-107">示例</span><span class="sxs-lookup"><span data-stu-id="f1161-107">EXAMPLES</span></span>

## <span data-ttu-id="f1161-108">參數</span><span class="sxs-lookup"><span data-stu-id="f1161-108">PARAMETERS</span></span>

### <span data-ttu-id="f1161-109">-保存庫</span><span class="sxs-lookup"><span data-stu-id="f1161-109">-Vault</span></span>
<span data-ttu-id="f1161-110">指定保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1161-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="f1161-111">Vault 必須是 **AzureRmRecoveryServicesVault** 物件。</span><span class="sxs-lookup"><span data-stu-id="f1161-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="f1161-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1161-112">-DefaultProfile</span></span>
<span data-ttu-id="f1161-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1161-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1161-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1161-114">CommonParameters</span></span>
<span data-ttu-id="f1161-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1161-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1161-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f1161-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1161-117">輸入</span><span class="sxs-lookup"><span data-stu-id="f1161-117">INPUTS</span></span>

### <span data-ttu-id="f1161-118">ARSVault</span><span class="sxs-lookup"><span data-stu-id="f1161-118">ARSVault</span></span>
<span data-ttu-id="f1161-119">參數 "Vault" 接受來自管線的 "ARSVault" 類型值</span><span class="sxs-lookup"><span data-stu-id="f1161-119">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="f1161-120">輸出</span><span class="sxs-lookup"><span data-stu-id="f1161-120">OUTPUTS</span></span>

## <span data-ttu-id="f1161-121">筆記</span><span class="sxs-lookup"><span data-stu-id="f1161-121">NOTES</span></span>

## <span data-ttu-id="f1161-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1161-122">RELATED LINKS</span></span>
