---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: c63940ab03f6d288de3c1b5b0d767182168ed1fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621432"
---
# <span data-ttu-id="565a3-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="565a3-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="565a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="565a3-102">SYNOPSIS</span></span>
<span data-ttu-id="565a3-103">更新網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="565a3-103">Updates a network profile.</span></span>

## <span data-ttu-id="565a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="565a3-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="565a3-105">說明</span><span class="sxs-lookup"><span data-stu-id="565a3-105">DESCRIPTION</span></span>
<span data-ttu-id="565a3-106">**AzPublicIpPrefix** Cmdlet 會更新網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="565a3-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="565a3-107">示例</span><span class="sxs-lookup"><span data-stu-id="565a3-107">EXAMPLES</span></span>

### <span data-ttu-id="565a3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="565a3-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="565a3-109">第一個命令會取得現有的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="565a3-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="565a3-110">第二個命令會更新標記，第三個命令會在網路設定檔上新增網路介面配置。</span><span class="sxs-lookup"><span data-stu-id="565a3-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="565a3-111">第四個命令會更新網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="565a3-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="565a3-112">參數</span><span class="sxs-lookup"><span data-stu-id="565a3-112">PARAMETERS</span></span>

### <span data-ttu-id="565a3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="565a3-113">-AsJob</span></span>
<span data-ttu-id="565a3-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="565a3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="565a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="565a3-115">-DefaultProfile</span></span>
<span data-ttu-id="565a3-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="565a3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="565a3-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="565a3-117">-NetworkProfile</span></span>
<span data-ttu-id="565a3-118">網路設定檔</span><span class="sxs-lookup"><span data-stu-id="565a3-118">The network profile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="565a3-119">-確認</span><span class="sxs-lookup"><span data-stu-id="565a3-119">-Confirm</span></span>
<span data-ttu-id="565a3-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="565a3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="565a3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="565a3-121">-WhatIf</span></span>
<span data-ttu-id="565a3-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="565a3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="565a3-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="565a3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="565a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="565a3-124">CommonParameters</span></span>
<span data-ttu-id="565a3-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="565a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="565a3-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="565a3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="565a3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="565a3-127">INPUTS</span></span>

### <span data-ttu-id="565a3-128">PSNetworkProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="565a3-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="565a3-129">輸出</span><span class="sxs-lookup"><span data-stu-id="565a3-129">OUTPUTS</span></span>

### <span data-ttu-id="565a3-130">PSNetworkProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="565a3-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="565a3-131">筆記</span><span class="sxs-lookup"><span data-stu-id="565a3-131">NOTES</span></span>

## <span data-ttu-id="565a3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="565a3-132">RELATED LINKS</span></span>

[<span data-ttu-id="565a3-133">AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="565a3-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="565a3-134">新-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="565a3-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="565a3-135">移除-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="565a3-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)