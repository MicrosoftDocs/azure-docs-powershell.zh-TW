---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
ms.openlocfilehash: 45e2c822bc21acfe69296f8d784a3a707dc1797f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274911"
---
# <span data-ttu-id="b893c-101">Remove-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="b893c-101">Remove-AzWvdMsixPackage</span></span>

## <span data-ttu-id="b893c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b893c-102">SYNOPSIS</span></span>
<span data-ttu-id="b893c-103">移除 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="b893c-103">Remove an MSIX Package.</span></span>

## <span data-ttu-id="b893c-104">句法</span><span class="sxs-lookup"><span data-stu-id="b893c-104">SYNTAX</span></span>

### <span data-ttu-id="b893c-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="b893c-105">Delete (Default)</span></span>
```
Remove-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b893c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b893c-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b893c-107">說明</span><span class="sxs-lookup"><span data-stu-id="b893c-107">DESCRIPTION</span></span>
<span data-ttu-id="b893c-108">移除 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="b893c-108">Remove an MSIX Package.</span></span>

## <span data-ttu-id="b893c-109">示例</span><span class="sxs-lookup"><span data-stu-id="b893c-109">EXAMPLES</span></span>

### <span data-ttu-id="b893c-110">範例1：依套件完整名稱刪除 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="b893c-110">Example 1: Delete MSIX Package by Package Full Name</span></span>
```powershell
PS C:\> Remove-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName
```

<span data-ttu-id="b893c-111">這個命令會刪除 HostPool 中的 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="b893c-111">This command deletes a MSIX Package in a HostPool</span></span>

## <span data-ttu-id="b893c-112">參數</span><span class="sxs-lookup"><span data-stu-id="b893c-112">PARAMETERS</span></span>

### <span data-ttu-id="b893c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b893c-113">-DefaultProfile</span></span>
<span data-ttu-id="b893c-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b893c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b893c-115">-FullName</span><span class="sxs-lookup"><span data-stu-id="b893c-115">-FullName</span></span>
<span data-ttu-id="b893c-116">指定 hostpool 中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="b893c-116">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b893c-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="b893c-117">-HostPoolName</span></span>
<span data-ttu-id="b893c-118">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="b893c-118">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b893c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b893c-119">-InputObject</span></span>
<span data-ttu-id="b893c-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b893c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b893c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b893c-121">-PassThru</span></span>
<span data-ttu-id="b893c-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="b893c-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b893c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b893c-123">-ResourceGroupName</span></span>
<span data-ttu-id="b893c-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b893c-124">The name of the resource group.</span></span>
<span data-ttu-id="b893c-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b893c-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b893c-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b893c-126">-SubscriptionId</span></span>
<span data-ttu-id="b893c-127">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="b893c-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b893c-128">-確認</span><span class="sxs-lookup"><span data-stu-id="b893c-128">-Confirm</span></span>
<span data-ttu-id="b893c-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b893c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b893c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b893c-130">-WhatIf</span></span>
<span data-ttu-id="b893c-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b893c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b893c-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b893c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b893c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b893c-133">CommonParameters</span></span>
<span data-ttu-id="b893c-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b893c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b893c-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b893c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b893c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b893c-136">INPUTS</span></span>

### <span data-ttu-id="b893c-137">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="b893c-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b893c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b893c-138">OUTPUTS</span></span>

### <span data-ttu-id="b893c-139">System.object</span><span class="sxs-lookup"><span data-stu-id="b893c-139">System.Boolean</span></span>

## <span data-ttu-id="b893c-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b893c-140">NOTES</span></span>

<span data-ttu-id="b893c-141">別名</span><span class="sxs-lookup"><span data-stu-id="b893c-141">ALIASES</span></span>

<span data-ttu-id="b893c-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b893c-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b893c-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b893c-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b893c-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b893c-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b893c-145">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b893c-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b893c-146">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="b893c-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b893c-147">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="b893c-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b893c-148">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="b893c-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b893c-149">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="b893c-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b893c-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b893c-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b893c-151">`[MsixPackageFullName <String>]`： MSIX 套件在指定 hostpool 中的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="b893c-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b893c-152">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b893c-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b893c-153">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b893c-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="b893c-154">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="b893c-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b893c-155">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b893c-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b893c-156">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="b893c-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b893c-157">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="b893c-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b893c-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="b893c-158">RELATED LINKS</span></span>
