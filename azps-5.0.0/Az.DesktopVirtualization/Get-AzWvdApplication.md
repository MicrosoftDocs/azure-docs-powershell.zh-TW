---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: e75a9db71a4b20ed87d4e9564597af758af16304
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284773"
---
# <span data-ttu-id="c4b3e-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="c4b3e-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="c4b3e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b3e-103">取得應用程式。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-103">Get an application.</span></span>

## <span data-ttu-id="c4b3e-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4b3e-104">SYNTAX</span></span>

### <span data-ttu-id="c4b3e-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="c4b3e-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c4b3e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="c4b3e-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c4b3e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c4b3e-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4b3e-108">說明</span><span class="sxs-lookup"><span data-stu-id="c4b3e-108">DESCRIPTION</span></span>
<span data-ttu-id="c4b3e-109">取得應用程式。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-109">Get an application.</span></span>

## <span data-ttu-id="c4b3e-110">示例</span><span class="sxs-lookup"><span data-stu-id="c4b3e-110">EXAMPLES</span></span>

### <span data-ttu-id="c4b3e-111">範例1：透過名稱取得 Windows 虛擬桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="c4b3e-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="c4b3e-112">這個命令會在 applicaton 群組中取得 Windows 虛擬桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="c4b3e-113">範例2：列出 Windows 虛擬桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="c4b3e-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="c4b3e-114">這個命令會在 applicaton 群組中列出 Windows 虛擬桌面應用程式。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="c4b3e-115">參數</span><span class="sxs-lookup"><span data-stu-id="c4b3e-115">PARAMETERS</span></span>

### <span data-ttu-id="c4b3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4b3e-116">-DefaultProfile</span></span>
<span data-ttu-id="c4b3e-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4b3e-118">-[名]</span><span class="sxs-lookup"><span data-stu-id="c4b3e-118">-GroupName</span></span>
<span data-ttu-id="c4b3e-119">應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="c4b3e-119">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b3e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4b3e-120">-InputObject</span></span>
<span data-ttu-id="c4b3e-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4b3e-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c4b3e-122">-Name</span></span>
<span data-ttu-id="c4b3e-123">指定應用程式群組內的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="c4b3e-123">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b3e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4b3e-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4b3e-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-125">The name of the resource group.</span></span>
<span data-ttu-id="c4b3e-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b3e-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4b3e-127">-SubscriptionId</span></span>
<span data-ttu-id="c4b3e-128">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b3e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b3e-129">CommonParameters</span></span>
<span data-ttu-id="c4b3e-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b3e-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b3e-132">輸入</span><span class="sxs-lookup"><span data-stu-id="c4b3e-132">INPUTS</span></span>

### <span data-ttu-id="c4b3e-133">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="c4b3e-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c4b3e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c4b3e-134">OUTPUTS</span></span>

### <span data-ttu-id="c4b3e-135">IApplication （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="c4b3e-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c4b3e-136">NOTES</span></span>

<span data-ttu-id="c4b3e-137">別名</span><span class="sxs-lookup"><span data-stu-id="c4b3e-137">ALIASES</span></span>

<span data-ttu-id="c4b3e-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c4b3e-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c4b3e-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4b3e-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c4b3e-141">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="c4b3e-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4b3e-142">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="c4b3e-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c4b3e-143">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="c4b3e-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c4b3e-144">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="c4b3e-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c4b3e-145">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="c4b3e-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c4b3e-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="c4b3e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4b3e-147">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c4b3e-148">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="c4b3e-149">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="c4b3e-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c4b3e-150">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c4b3e-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c4b3e-151">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="c4b3e-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c4b3e-152">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="c4b3e-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c4b3e-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4b3e-153">RELATED LINKS</span></span>
