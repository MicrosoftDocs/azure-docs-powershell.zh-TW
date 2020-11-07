---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 3ab29642bcf9a6ba42f211705f3d5c2c6973a061
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791847"
---
# <span data-ttu-id="8add0-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8add0-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="8add0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8add0-102">SYNOPSIS</span></span>
<span data-ttu-id="8add0-103">從 [恢復服務] 保存庫刪除/取消註冊指定的 Azure Site Recovery 復原服務提供者。</span><span class="sxs-lookup"><span data-stu-id="8add0-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="8add0-104">句法</span><span class="sxs-lookup"><span data-stu-id="8add0-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8add0-105">說明</span><span class="sxs-lookup"><span data-stu-id="8add0-105">DESCRIPTION</span></span>
<span data-ttu-id="8add0-106">**AzRecoveryServicesAsrServicesProvider** Cmdlet 會從保存庫中移除指定的 Azure Site recovery 復原服務提供者。</span><span class="sxs-lookup"><span data-stu-id="8add0-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="8add0-107">示例</span><span class="sxs-lookup"><span data-stu-id="8add0-107">EXAMPLES</span></span>

### <span data-ttu-id="8add0-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8add0-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="8add0-109">啟動指定 Azure 網站復原服務提供者的刪除/登出，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="8add0-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8add0-110">參數</span><span class="sxs-lookup"><span data-stu-id="8add0-110">PARAMETERS</span></span>

### <span data-ttu-id="8add0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8add0-111">-DefaultProfile</span></span>
<span data-ttu-id="8add0-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8add0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8add0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8add0-113">-Force</span></span>
<span data-ttu-id="8add0-114">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="8add0-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="8add0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8add0-115">-InputObject</span></span>
<span data-ttu-id="8add0-116">Cmdlet 的輸入物件：對應至要刪除之 ASR 恢復服務提供者的 ASR 恢復服務提供者物件。</span><span class="sxs-lookup"><span data-stu-id="8add0-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8add0-117">-確認</span><span class="sxs-lookup"><span data-stu-id="8add0-117">-Confirm</span></span>
<span data-ttu-id="8add0-118">指定是否需要確認。</span><span class="sxs-lookup"><span data-stu-id="8add0-118">Specify if confirmation is required.</span></span> <span data-ttu-id="8add0-119">將確認參數的值設定為 [$false]，以略過確認。</span><span class="sxs-lookup"><span data-stu-id="8add0-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="8add0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8add0-120">-WhatIf</span></span>
<span data-ttu-id="8add0-121">顯示在未實際執行 Cmdlet 的情況下執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8add0-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="8add0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8add0-122">CommonParameters</span></span>
<span data-ttu-id="8add0-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8add0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8add0-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8add0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8add0-125">輸入</span><span class="sxs-lookup"><span data-stu-id="8add0-125">INPUTS</span></span>

### <span data-ttu-id="8add0-126">RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8add0-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="8add0-127">輸出</span><span class="sxs-lookup"><span data-stu-id="8add0-127">OUTPUTS</span></span>

### <span data-ttu-id="8add0-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8add0-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8add0-129">筆記</span><span class="sxs-lookup"><span data-stu-id="8add0-129">NOTES</span></span>

## <span data-ttu-id="8add0-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="8add0-130">RELATED LINKS</span></span>

[<span data-ttu-id="8add0-131">AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8add0-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="8add0-132">更新-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8add0-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)