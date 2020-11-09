---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284736"
---
# <span data-ttu-id="c8e34-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="c8e34-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="c8e34-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8e34-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e34-103">移除 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="c8e34-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="c8e34-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8e34-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c8e34-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8e34-105">DESCRIPTION</span></span>
<span data-ttu-id="c8e34-106">移除 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="c8e34-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="c8e34-107">示例</span><span class="sxs-lookup"><span data-stu-id="c8e34-107">EXAMPLES</span></span>

### <span data-ttu-id="c8e34-108">範例1：刪除 Windows 虛擬桌面註冊權杖</span><span class="sxs-lookup"><span data-stu-id="c8e34-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="c8e34-109">這個命令會刪除主機池中的 Windows 虛擬桌面註冊權杖。</span><span class="sxs-lookup"><span data-stu-id="c8e34-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="c8e34-110">參數</span><span class="sxs-lookup"><span data-stu-id="c8e34-110">PARAMETERS</span></span>

### <span data-ttu-id="c8e34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8e34-111">-DefaultProfile</span></span>
<span data-ttu-id="c8e34-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8e34-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8e34-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="c8e34-113">-HostPoolName</span></span>
<span data-ttu-id="c8e34-114">主機池名稱</span><span class="sxs-lookup"><span data-stu-id="c8e34-114">Host Pool Name</span></span>

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

### <span data-ttu-id="c8e34-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8e34-115">-ResourceGroupName</span></span>
<span data-ttu-id="c8e34-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c8e34-116">Resource Group Name</span></span>

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

### <span data-ttu-id="c8e34-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8e34-117">-SubscriptionId</span></span>
<span data-ttu-id="c8e34-118">協助 foo 1</span><span class="sxs-lookup"><span data-stu-id="c8e34-118">help foo 1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8e34-119">-確認</span><span class="sxs-lookup"><span data-stu-id="c8e34-119">-Confirm</span></span>
<span data-ttu-id="c8e34-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c8e34-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8e34-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8e34-121">-WhatIf</span></span>
<span data-ttu-id="c8e34-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8e34-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8e34-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8e34-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8e34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e34-124">CommonParameters</span></span>
<span data-ttu-id="c8e34-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8e34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e34-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c8e34-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e34-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c8e34-127">INPUTS</span></span>

## <span data-ttu-id="c8e34-128">輸出</span><span class="sxs-lookup"><span data-stu-id="c8e34-128">OUTPUTS</span></span>

## <span data-ttu-id="c8e34-129">筆記</span><span class="sxs-lookup"><span data-stu-id="c8e34-129">NOTES</span></span>

<span data-ttu-id="c8e34-130">別名</span><span class="sxs-lookup"><span data-stu-id="c8e34-130">ALIASES</span></span>

## <span data-ttu-id="c8e34-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8e34-131">RELATED LINKS</span></span>
