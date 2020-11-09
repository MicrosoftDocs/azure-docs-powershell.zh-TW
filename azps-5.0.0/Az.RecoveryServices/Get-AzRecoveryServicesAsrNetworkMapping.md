---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 1478a6fbe28e1d014767a829144138d7ada3dcfd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285829"
---
# <span data-ttu-id="cb8a6-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cb8a6-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="cb8a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="cb8a6-103">取得目前電子倉庫之網站復原網路對應的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cb8a6-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="cb8a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb8a6-104">SYNTAX</span></span>

### <span data-ttu-id="cb8a6-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="cb8a6-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb8a6-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="cb8a6-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb8a6-107">說明</span><span class="sxs-lookup"><span data-stu-id="cb8a6-107">DESCRIPTION</span></span>
<span data-ttu-id="cb8a6-108">**AzRecoveryServicesAsrNetworkMapping** Cmdlet 會取得有關恢復服務電子倉庫之 Azure Site Recovery 網路對應的資訊。</span><span class="sxs-lookup"><span data-stu-id="cb8a6-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="cb8a6-109">示例</span><span class="sxs-lookup"><span data-stu-id="cb8a6-109">EXAMPLES</span></span>

### <span data-ttu-id="cb8a6-110">範例1</span><span class="sxs-lookup"><span data-stu-id="cb8a6-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="cb8a6-111">取得已傳送網路的所有網路對應。</span><span class="sxs-lookup"><span data-stu-id="cb8a6-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="cb8a6-112">範例2</span><span class="sxs-lookup"><span data-stu-id="cb8a6-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="cb8a6-113">在指定的 azure 網站復原結構中取得已提供名稱的網路對應。</span><span class="sxs-lookup"><span data-stu-id="cb8a6-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="cb8a6-114">參數</span><span class="sxs-lookup"><span data-stu-id="cb8a6-114">PARAMETERS</span></span>

### <span data-ttu-id="cb8a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb8a6-115">-DefaultProfile</span></span>
<span data-ttu-id="cb8a6-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb8a6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="cb8a6-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb8a6-117">-Name</span></span>
<span data-ttu-id="cb8a6-118">要取得之 ASR 網路對應物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb8a6-118">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb8a6-119">-網路</span><span class="sxs-lookup"><span data-stu-id="cb8a6-119">-Network</span></span>
<span data-ttu-id="cb8a6-120">取得與指定的網路 ASR 物件相對應的 ASR 網路對應。</span><span class="sxs-lookup"><span data-stu-id="cb8a6-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb8a6-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="cb8a6-121">-PrimaryFabric</span></span>
<span data-ttu-id="cb8a6-122">取得與指定的主要結構物件相對應的 ASR 網路對應。</span><span class="sxs-lookup"><span data-stu-id="cb8a6-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb8a6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb8a6-123">CommonParameters</span></span>
<span data-ttu-id="cb8a6-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb8a6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb8a6-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cb8a6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb8a6-126">輸入</span><span class="sxs-lookup"><span data-stu-id="cb8a6-126">INPUTS</span></span>

### <span data-ttu-id="cb8a6-127">RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="cb8a6-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="cb8a6-128">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="cb8a6-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="cb8a6-129">輸出</span><span class="sxs-lookup"><span data-stu-id="cb8a6-129">OUTPUTS</span></span>

### <span data-ttu-id="cb8a6-130">RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cb8a6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="cb8a6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="cb8a6-131">NOTES</span></span>

## <span data-ttu-id="cb8a6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb8a6-132">RELATED LINKS</span></span>

[<span data-ttu-id="cb8a6-133">新-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cb8a6-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="cb8a6-134">移除-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cb8a6-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)