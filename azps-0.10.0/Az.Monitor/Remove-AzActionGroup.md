---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: 25185202bd0804960c6803b98955e62ab9410c76
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794570"
---
# <span data-ttu-id="03235-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="03235-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="03235-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03235-102">SYNOPSIS</span></span>
<span data-ttu-id="03235-103">移除動作群組。</span><span class="sxs-lookup"><span data-stu-id="03235-103">Removes an action group.</span></span>

## <span data-ttu-id="03235-104">句法</span><span class="sxs-lookup"><span data-stu-id="03235-104">SYNTAX</span></span>

### <span data-ttu-id="03235-105">ByPropertyName (預設) </span><span class="sxs-lookup"><span data-stu-id="03235-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03235-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="03235-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03235-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="03235-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03235-108">說明</span><span class="sxs-lookup"><span data-stu-id="03235-108">DESCRIPTION</span></span>
<span data-ttu-id="03235-109">**AzActionGroup** Cmdlet 會移除 [動作] 群組。</span><span class="sxs-lookup"><span data-stu-id="03235-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="03235-110">示例</span><span class="sxs-lookup"><span data-stu-id="03235-110">EXAMPLES</span></span>

### <span data-ttu-id="03235-111">範例1：移除動作群組</span><span class="sxs-lookup"><span data-stu-id="03235-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="03235-112">參數</span><span class="sxs-lookup"><span data-stu-id="03235-112">PARAMETERS</span></span>

### <span data-ttu-id="03235-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03235-113">-DefaultProfile</span></span>
<span data-ttu-id="03235-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="03235-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03235-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03235-115">-InputObject</span></span>
<span data-ttu-id="03235-116">[動作] 群組資源</span><span class="sxs-lookup"><span data-stu-id="03235-116">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03235-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="03235-117">-Name</span></span>
<span data-ttu-id="03235-118">動作群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="03235-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03235-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03235-119">-ResourceGroupName</span></span>
<span data-ttu-id="03235-120">資源群組</span><span class="sxs-lookup"><span data-stu-id="03235-120">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03235-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03235-121">-ResourceId</span></span>
<span data-ttu-id="03235-122">資源 i</span><span class="sxs-lookup"><span data-stu-id="03235-122">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03235-123">-確認</span><span class="sxs-lookup"><span data-stu-id="03235-123">-Confirm</span></span>
<span data-ttu-id="03235-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="03235-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03235-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03235-125">-WhatIf</span></span>
<span data-ttu-id="03235-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03235-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03235-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03235-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03235-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03235-128">CommonParameters</span></span>
<span data-ttu-id="03235-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03235-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03235-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="03235-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03235-131">輸入</span><span class="sxs-lookup"><span data-stu-id="03235-131">INPUTS</span></span>

### <span data-ttu-id="03235-132">System.object</span><span class="sxs-lookup"><span data-stu-id="03235-132">System.String</span></span>

### <span data-ttu-id="03235-133">PSActionGroupResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="03235-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="03235-134">輸出</span><span class="sxs-lookup"><span data-stu-id="03235-134">OUTPUTS</span></span>

### <span data-ttu-id="03235-135">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="03235-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="03235-136">筆記</span><span class="sxs-lookup"><span data-stu-id="03235-136">NOTES</span></span>

## <span data-ttu-id="03235-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="03235-137">RELATED LINKS</span></span>

<span data-ttu-id="03235-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
[AzActionGroup](./Get-AzActionGroup.md) 
[新-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="03235-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>