---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c76c2ebf40f360820ec3eef719b33142daacdbac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621074"
---
# <span data-ttu-id="ed725-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ed725-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="ed725-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed725-102">SYNOPSIS</span></span>
<span data-ttu-id="ed725-103">刪除指定的 ASR 儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="ed725-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="ed725-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed725-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed725-105">說明</span><span class="sxs-lookup"><span data-stu-id="ed725-105">DESCRIPTION</span></span>
<span data-ttu-id="ed725-106">**AzRecoveryServicesAsrStorageClassificationMapping** Cmdlet 會刪除指定的 Azure Site Recovery 儲存分類對應。</span><span class="sxs-lookup"><span data-stu-id="ed725-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="ed725-107">示例</span><span class="sxs-lookup"><span data-stu-id="ed725-107">EXAMPLES</span></span>

### <span data-ttu-id="ed725-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ed725-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="ed725-109">開始刪除指定的儲存分類對應，並傳回用於追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="ed725-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ed725-110">參數</span><span class="sxs-lookup"><span data-stu-id="ed725-110">PARAMETERS</span></span>

### <span data-ttu-id="ed725-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed725-111">-DefaultProfile</span></span>
<span data-ttu-id="ed725-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed725-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ed725-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed725-113">-InputObject</span></span>
<span data-ttu-id="ed725-114">Cmdlet 的輸入物件：與要刪除之 ASR 儲存分類對應的 ASR 儲存分類對應物件。</span><span class="sxs-lookup"><span data-stu-id="ed725-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed725-115">-確認</span><span class="sxs-lookup"><span data-stu-id="ed725-115">-Confirm</span></span>
<span data-ttu-id="ed725-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed725-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed725-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed725-117">-WhatIf</span></span>
<span data-ttu-id="ed725-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed725-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed725-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed725-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed725-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed725-120">CommonParameters</span></span>
<span data-ttu-id="ed725-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed725-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed725-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed725-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed725-123">輸入</span><span class="sxs-lookup"><span data-stu-id="ed725-123">INPUTS</span></span>

### <span data-ttu-id="ed725-124">RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ed725-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="ed725-125">輸出</span><span class="sxs-lookup"><span data-stu-id="ed725-125">OUTPUTS</span></span>

### <span data-ttu-id="ed725-126">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ed725-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ed725-127">筆記</span><span class="sxs-lookup"><span data-stu-id="ed725-127">NOTES</span></span>

## <span data-ttu-id="ed725-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed725-128">RELATED LINKS</span></span>

[<span data-ttu-id="ed725-129">AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ed725-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="ed725-130">新-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ed725-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)