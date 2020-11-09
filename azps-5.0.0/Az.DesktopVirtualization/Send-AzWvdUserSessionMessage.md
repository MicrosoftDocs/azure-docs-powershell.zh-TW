---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 047ede26246c31b17fbeb49fca4353b2cb17594c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284727"
---
# <span data-ttu-id="613d8-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="613d8-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="613d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="613d8-102">SYNOPSIS</span></span>
<span data-ttu-id="613d8-103">傳送訊息給使用者。</span><span class="sxs-lookup"><span data-stu-id="613d8-103">Send a message to a user.</span></span>

## <span data-ttu-id="613d8-104">句法</span><span class="sxs-lookup"><span data-stu-id="613d8-104">SYNTAX</span></span>

### <span data-ttu-id="613d8-105">SendExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="613d8-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="613d8-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="613d8-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="613d8-107">說明</span><span class="sxs-lookup"><span data-stu-id="613d8-107">DESCRIPTION</span></span>
<span data-ttu-id="613d8-108">傳送訊息給使用者。</span><span class="sxs-lookup"><span data-stu-id="613d8-108">Send a message to a user.</span></span>

## <span data-ttu-id="613d8-109">示例</span><span class="sxs-lookup"><span data-stu-id="613d8-109">EXAMPLES</span></span>

### <span data-ttu-id="613d8-110">範例1：傳送訊息給 UserSession</span><span class="sxs-lookup"><span data-stu-id="613d8-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="613d8-111">這個命令會將訊息傳送給 UserSession。</span><span class="sxs-lookup"><span data-stu-id="613d8-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="613d8-112">參數</span><span class="sxs-lookup"><span data-stu-id="613d8-112">PARAMETERS</span></span>

### <span data-ttu-id="613d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="613d8-113">-DefaultProfile</span></span>
<span data-ttu-id="613d8-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="613d8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="613d8-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="613d8-115">-HostPoolName</span></span>
<span data-ttu-id="613d8-116">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="613d8-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="613d8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="613d8-117">-InputObject</span></span>
<span data-ttu-id="613d8-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="613d8-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: SendViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="613d8-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="613d8-119">-MessageBody</span></span>
<span data-ttu-id="613d8-120">郵件的正文。</span><span class="sxs-lookup"><span data-stu-id="613d8-120">Body of message.</span></span>

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

### <span data-ttu-id="613d8-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="613d8-121">-MessageTitle</span></span>
<span data-ttu-id="613d8-122">郵件的標題。</span><span class="sxs-lookup"><span data-stu-id="613d8-122">Title of message.</span></span>

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

### <span data-ttu-id="613d8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="613d8-123">-PassThru</span></span>
<span data-ttu-id="613d8-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="613d8-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="613d8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="613d8-125">-ResourceGroupName</span></span>
<span data-ttu-id="613d8-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="613d8-126">The name of the resource group.</span></span>
<span data-ttu-id="613d8-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="613d8-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="613d8-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="613d8-128">-SessionHostName</span></span>
<span data-ttu-id="613d8-129">指定主機池中工作階段主機的名稱</span><span class="sxs-lookup"><span data-stu-id="613d8-129">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="613d8-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="613d8-130">-SubscriptionId</span></span>
<span data-ttu-id="613d8-131">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="613d8-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="613d8-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="613d8-132">-UserSessionId</span></span>
<span data-ttu-id="613d8-133">指定的工作階段主機中使用者會話的名稱</span><span class="sxs-lookup"><span data-stu-id="613d8-133">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="613d8-134">-確認</span><span class="sxs-lookup"><span data-stu-id="613d8-134">-Confirm</span></span>
<span data-ttu-id="613d8-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="613d8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="613d8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="613d8-136">-WhatIf</span></span>
<span data-ttu-id="613d8-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="613d8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="613d8-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="613d8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="613d8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="613d8-139">CommonParameters</span></span>
<span data-ttu-id="613d8-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="613d8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="613d8-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="613d8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="613d8-142">輸入</span><span class="sxs-lookup"><span data-stu-id="613d8-142">INPUTS</span></span>

### <span data-ttu-id="613d8-143">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="613d8-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="613d8-144">輸出</span><span class="sxs-lookup"><span data-stu-id="613d8-144">OUTPUTS</span></span>

### <span data-ttu-id="613d8-145">System.object</span><span class="sxs-lookup"><span data-stu-id="613d8-145">System.Boolean</span></span>

## <span data-ttu-id="613d8-146">筆記</span><span class="sxs-lookup"><span data-stu-id="613d8-146">NOTES</span></span>

<span data-ttu-id="613d8-147">別名</span><span class="sxs-lookup"><span data-stu-id="613d8-147">ALIASES</span></span>

<span data-ttu-id="613d8-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="613d8-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="613d8-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="613d8-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="613d8-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="613d8-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="613d8-151">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="613d8-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="613d8-152">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="613d8-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="613d8-153">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="613d8-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="613d8-154">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="613d8-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="613d8-155">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="613d8-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="613d8-156">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="613d8-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="613d8-157">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="613d8-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="613d8-158">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="613d8-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="613d8-159">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="613d8-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="613d8-160">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="613d8-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="613d8-161">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="613d8-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="613d8-162">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="613d8-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="613d8-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="613d8-163">RELATED LINKS</span></span>
