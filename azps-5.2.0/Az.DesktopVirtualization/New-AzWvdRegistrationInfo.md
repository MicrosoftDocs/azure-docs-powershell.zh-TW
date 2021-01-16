---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 2268135ebd1e1c504aae7462730d104e842f288f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276100"
---
# <span data-ttu-id="2c1ea-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="2c1ea-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="2c1ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c1ea-102">SYNOPSIS</span></span>
<span data-ttu-id="2c1ea-103">建立 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="2c1ea-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="2c1ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c1ea-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2c1ea-105">說明</span><span class="sxs-lookup"><span data-stu-id="2c1ea-105">DESCRIPTION</span></span>
<span data-ttu-id="2c1ea-106">建立 Windows 虛擬桌面註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="2c1ea-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="2c1ea-107">示例</span><span class="sxs-lookup"><span data-stu-id="2c1ea-107">EXAMPLES</span></span>

### <span data-ttu-id="2c1ea-108">範例1：建立 Windows 虛擬桌面註冊權杖</span><span class="sxs-lookup"><span data-stu-id="2c1ea-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="2c1ea-109">這個命令會在主機池中建立 Windows 虛擬桌面註冊權杖。</span><span class="sxs-lookup"><span data-stu-id="2c1ea-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="2c1ea-110">參數</span><span class="sxs-lookup"><span data-stu-id="2c1ea-110">PARAMETERS</span></span>

### <span data-ttu-id="2c1ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c1ea-111">-DefaultProfile</span></span>
<span data-ttu-id="2c1ea-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c1ea-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c1ea-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="2c1ea-113">-ExpirationTime</span></span>
<span data-ttu-id="2c1ea-114">到期時間</span><span class="sxs-lookup"><span data-stu-id="2c1ea-114">Expiration Time</span></span>

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

### <span data-ttu-id="2c1ea-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="2c1ea-115">-HostPoolName</span></span>
<span data-ttu-id="2c1ea-116">主機池名稱</span><span class="sxs-lookup"><span data-stu-id="2c1ea-116">Host Pool Name</span></span>

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

### <span data-ttu-id="2c1ea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c1ea-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c1ea-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2c1ea-118">Resource Group Name</span></span>

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

### <span data-ttu-id="2c1ea-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c1ea-119">-SubscriptionId</span></span>
<span data-ttu-id="2c1ea-120">訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="2c1ea-120">Subscription Id</span></span>

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

### <span data-ttu-id="2c1ea-121">-確認</span><span class="sxs-lookup"><span data-stu-id="2c1ea-121">-Confirm</span></span>
<span data-ttu-id="2c1ea-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2c1ea-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c1ea-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c1ea-123">-WhatIf</span></span>
<span data-ttu-id="2c1ea-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c1ea-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c1ea-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c1ea-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c1ea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c1ea-126">CommonParameters</span></span>
<span data-ttu-id="2c1ea-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c1ea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c1ea-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2c1ea-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c1ea-129">輸入</span><span class="sxs-lookup"><span data-stu-id="2c1ea-129">INPUTS</span></span>

## <span data-ttu-id="2c1ea-130">輸出</span><span class="sxs-lookup"><span data-stu-id="2c1ea-130">OUTPUTS</span></span>

### <span data-ttu-id="2c1ea-131">IRegistrationInfo （DesktopVirtualization）。 Api20201019Preview。</span><span class="sxs-lookup"><span data-stu-id="2c1ea-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="2c1ea-132">筆記</span><span class="sxs-lookup"><span data-stu-id="2c1ea-132">NOTES</span></span>

<span data-ttu-id="2c1ea-133">別名</span><span class="sxs-lookup"><span data-stu-id="2c1ea-133">ALIASES</span></span>

## <span data-ttu-id="2c1ea-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c1ea-134">RELATED LINKS</span></span>
