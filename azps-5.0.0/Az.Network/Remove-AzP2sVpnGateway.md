---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288256"
---
# <span data-ttu-id="d88db-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d88db-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="d88db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d88db-102">SYNOPSIS</span></span>
<span data-ttu-id="d88db-103">移除現有的 P2SVpnGateway。</span><span class="sxs-lookup"><span data-stu-id="d88db-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="d88db-104">句法</span><span class="sxs-lookup"><span data-stu-id="d88db-104">SYNTAX</span></span>

### <span data-ttu-id="d88db-105">ByP2SVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="d88db-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d88db-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d88db-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d88db-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d88db-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d88db-108">說明</span><span class="sxs-lookup"><span data-stu-id="d88db-108">DESCRIPTION</span></span>
<span data-ttu-id="d88db-109">**AzP2sVpnGateway** Cmdlet 可讓您在 VirtualHub 中移除現有的 P2SVpnGateway。</span><span class="sxs-lookup"><span data-stu-id="d88db-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="d88db-110">移除 P2SVpnGateway 之後，所有指向網站用戶端的連線都將會失敗。</span><span class="sxs-lookup"><span data-stu-id="d88db-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="d88db-111">示例</span><span class="sxs-lookup"><span data-stu-id="d88db-111">EXAMPLES</span></span>

### <span data-ttu-id="d88db-112">範例1</span><span class="sxs-lookup"><span data-stu-id="d88db-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="d88db-113">**AzP2sVpnGateway** Cmdlet 可讓您在 VirtualHub 中移除現有的 P2SVpnGateway。</span><span class="sxs-lookup"><span data-stu-id="d88db-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="d88db-114">參數</span><span class="sxs-lookup"><span data-stu-id="d88db-114">PARAMETERS</span></span>

### <span data-ttu-id="d88db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d88db-115">-DefaultProfile</span></span>
<span data-ttu-id="d88db-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d88db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88db-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d88db-117">-Force</span></span>
<span data-ttu-id="d88db-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="d88db-118">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88db-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d88db-119">-InputObject</span></span>
<span data-ttu-id="d88db-120">要刪除的 p2sVpnGateway 物件。</span><span class="sxs-lookup"><span data-stu-id="d88db-120">The p2sVpnGateway object to be deleted.</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d88db-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d88db-121">-Name</span></span>
<span data-ttu-id="d88db-122">P2SVpnGateway 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d88db-122">The P2SVpnGateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88db-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d88db-123">-PassThru</span></span>
<span data-ttu-id="d88db-124">傳回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="d88db-124">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88db-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d88db-125">-ResourceGroupName</span></span>
<span data-ttu-id="d88db-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d88db-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88db-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d88db-127">-ResourceId</span></span>
<span data-ttu-id="d88db-128">要刪除之 p2sVpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d88db-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: p2sVpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d88db-129">-確認</span><span class="sxs-lookup"><span data-stu-id="d88db-129">-Confirm</span></span>
<span data-ttu-id="d88db-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d88db-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88db-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d88db-131">-WhatIf</span></span>
<span data-ttu-id="d88db-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d88db-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d88db-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d88db-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88db-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d88db-134">CommonParameters</span></span>
<span data-ttu-id="d88db-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d88db-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d88db-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d88db-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d88db-137">輸入</span><span class="sxs-lookup"><span data-stu-id="d88db-137">INPUTS</span></span>

### <span data-ttu-id="d88db-138">PSP2SVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d88db-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="d88db-139">System.object</span><span class="sxs-lookup"><span data-stu-id="d88db-139">System.String</span></span>

## <span data-ttu-id="d88db-140">輸出</span><span class="sxs-lookup"><span data-stu-id="d88db-140">OUTPUTS</span></span>

### <span data-ttu-id="d88db-141">System.object</span><span class="sxs-lookup"><span data-stu-id="d88db-141">System.Boolean</span></span>

## <span data-ttu-id="d88db-142">筆記</span><span class="sxs-lookup"><span data-stu-id="d88db-142">NOTES</span></span>

## <span data-ttu-id="d88db-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="d88db-143">RELATED LINKS</span></span>