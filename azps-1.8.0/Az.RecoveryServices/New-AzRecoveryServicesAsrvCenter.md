---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 98bc2dfde30357e7f6a3db62ec550a2a0c173bb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621104"
---
# <span data-ttu-id="29ce9-101">New-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="29ce9-101">New-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="29ce9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="29ce9-103">新增 vCenter 伺服器以探索可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="29ce9-103">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="29ce9-104">句法</span><span class="sxs-lookup"><span data-stu-id="29ce9-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount> -Port <Int32>
 -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29ce9-105">說明</span><span class="sxs-lookup"><span data-stu-id="29ce9-105">DESCRIPTION</span></span>
<span data-ttu-id="29ce9-106">**新的-AzRecoveryServicesAsrvCenter** Cmdlet 會新增 vCenter 伺服器來探索可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="29ce9-106">The **New-AzRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="29ce9-107">這個 Cmdlet 會註冊 vCenter 伺服器以供在佈建服務器中探索。</span><span class="sxs-lookup"><span data-stu-id="29ce9-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="29ce9-108">示例</span><span class="sxs-lookup"><span data-stu-id="29ce9-108">EXAMPLES</span></span>

### <span data-ttu-id="29ce9-109">範例1</span><span class="sxs-lookup"><span data-stu-id="29ce9-109">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="29ce9-110">新增 vCenter 伺服器以探索可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="29ce9-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="29ce9-111">參數</span><span class="sxs-lookup"><span data-stu-id="29ce9-111">PARAMETERS</span></span>

### <span data-ttu-id="29ce9-112">-帳戶</span><span class="sxs-lookup"><span data-stu-id="29ce9-112">-Account</span></span>
<span data-ttu-id="29ce9-113">使用者登入 creadential 帳戶。</span><span class="sxs-lookup"><span data-stu-id="29ce9-113">User login creadential Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ce9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29ce9-114">-DefaultProfile</span></span>
<span data-ttu-id="29ce9-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29ce9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29ce9-116">-結構</span><span class="sxs-lookup"><span data-stu-id="29ce9-116">-Fabric</span></span>
<span data-ttu-id="29ce9-117">與佈建服務器相對應的 ASR 結構。</span><span class="sxs-lookup"><span data-stu-id="29ce9-117">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29ce9-118">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="29ce9-118">-IpOrHostName</span></span>
<span data-ttu-id="29ce9-119">VCenter 伺服器的 IPv4 位址或 FQDN。</span><span class="sxs-lookup"><span data-stu-id="29ce9-119">IPv4 address or FQDN of the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ce9-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="29ce9-120">-Name</span></span>
<span data-ttu-id="29ce9-121">VCenter 伺服器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="29ce9-121">A friendly name for the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ce9-122">-埠</span><span class="sxs-lookup"><span data-stu-id="29ce9-122">-Port</span></span>
<span data-ttu-id="29ce9-123">VCenter 伺服器上用來進行探索的 TCP 埠。</span><span class="sxs-lookup"><span data-stu-id="29ce9-123">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ce9-124">-確認</span><span class="sxs-lookup"><span data-stu-id="29ce9-124">-Confirm</span></span>
<span data-ttu-id="29ce9-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29ce9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29ce9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29ce9-126">-WhatIf</span></span>
<span data-ttu-id="29ce9-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29ce9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29ce9-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29ce9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29ce9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ce9-129">CommonParameters</span></span>
<span data-ttu-id="29ce9-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29ce9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ce9-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29ce9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ce9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="29ce9-132">INPUTS</span></span>

### <span data-ttu-id="29ce9-133">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="29ce9-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="29ce9-134">輸出</span><span class="sxs-lookup"><span data-stu-id="29ce9-134">OUTPUTS</span></span>

### <span data-ttu-id="29ce9-135">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="29ce9-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="29ce9-136">筆記</span><span class="sxs-lookup"><span data-stu-id="29ce9-136">NOTES</span></span>

## <span data-ttu-id="29ce9-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="29ce9-137">RELATED LINKS</span></span>