---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
ms.openlocfilehash: e47cf4fe3eef11664640e947b7093dc302f90ea3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436034"
---
# <span data-ttu-id="f624b-101">Update-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="f624b-101">Update-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="f624b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f624b-102">SYNOPSIS</span></span>
<span data-ttu-id="f624b-103">更新私人雲端</span><span class="sxs-lookup"><span data-stu-id="f624b-103">Update a private cloud</span></span>

## <span data-ttu-id="f624b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f624b-104">SYNTAX</span></span>

### <span data-ttu-id="f624b-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="f624b-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f624b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f624b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f624b-107">說明</span><span class="sxs-lookup"><span data-stu-id="f624b-107">DESCRIPTION</span></span>
<span data-ttu-id="f624b-108">更新私人雲端</span><span class="sxs-lookup"><span data-stu-id="f624b-108">Update a private cloud</span></span>

## <span data-ttu-id="f624b-109">示例</span><span class="sxs-lookup"><span data-stu-id="f624b-109">EXAMPLES</span></span>

### <span data-ttu-id="f624b-110">範例1：依名稱更新私人雲端的大小</span><span class="sxs-lookup"><span data-stu-id="f624b-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="f624b-111">依名稱更新私人雲端的大小</span><span class="sxs-lookup"><span data-stu-id="f624b-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="f624b-112">範例2：依輸入物件更新私人雲端的大小</span><span class="sxs-lookup"><span data-stu-id="f624b-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMWarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="f624b-113">依輸入物件更新私人雲端的大小</span><span class="sxs-lookup"><span data-stu-id="f624b-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="f624b-114">參數</span><span class="sxs-lookup"><span data-stu-id="f624b-114">PARAMETERS</span></span>

### <span data-ttu-id="f624b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f624b-115">-AsJob</span></span>
<span data-ttu-id="f624b-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="f624b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f624b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f624b-117">-DefaultProfile</span></span>
<span data-ttu-id="f624b-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f624b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f624b-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="f624b-119">-IdentitySource</span></span>
<span data-ttu-id="f624b-120">vCenter 單一登入身分識別來源若要建立，請參閱 IDENTITYSOURCE 屬性和建立雜湊資料表的備忘稿一節。</span><span class="sxs-lookup"><span data-stu-id="f624b-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f624b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f624b-121">-InputObject</span></span>
<span data-ttu-id="f624b-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f624b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f624b-123">-網際網路</span><span class="sxs-lookup"><span data-stu-id="f624b-123">-Internet</span></span>
<span data-ttu-id="f624b-124">已啟用或停用網際網路連線</span><span class="sxs-lookup"><span data-stu-id="f624b-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f624b-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="f624b-125">-ManagementClusterSize</span></span>
<span data-ttu-id="f624b-126">群集大小</span><span class="sxs-lookup"><span data-stu-id="f624b-126">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f624b-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="f624b-127">-Name</span></span>
<span data-ttu-id="f624b-128">私有雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="f624b-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f624b-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f624b-129">-NoWait</span></span>
<span data-ttu-id="f624b-130">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="f624b-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f624b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f624b-131">-ResourceGroupName</span></span>
<span data-ttu-id="f624b-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f624b-132">The name of the resource group.</span></span>
<span data-ttu-id="f624b-133">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f624b-133">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f624b-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f624b-134">-SubscriptionId</span></span>
<span data-ttu-id="f624b-135">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="f624b-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f624b-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="f624b-136">-Tag</span></span>
<span data-ttu-id="f624b-137">資源標記。</span><span class="sxs-lookup"><span data-stu-id="f624b-137">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f624b-138">-確認</span><span class="sxs-lookup"><span data-stu-id="f624b-138">-Confirm</span></span>
<span data-ttu-id="f624b-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f624b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f624b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f624b-140">-WhatIf</span></span>
<span data-ttu-id="f624b-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f624b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f624b-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f624b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f624b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f624b-143">CommonParameters</span></span>
<span data-ttu-id="f624b-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f624b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f624b-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f624b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f624b-146">輸入</span><span class="sxs-lookup"><span data-stu-id="f624b-146">INPUTS</span></span>

### <span data-ttu-id="f624b-147">IVMWareIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f624b-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="f624b-148">輸出</span><span class="sxs-lookup"><span data-stu-id="f624b-148">OUTPUTS</span></span>

### <span data-ttu-id="f624b-149">IPrivateCloud 中的 Api20200320 （）。</span><span class="sxs-lookup"><span data-stu-id="f624b-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="f624b-150">筆記</span><span class="sxs-lookup"><span data-stu-id="f624b-150">NOTES</span></span>

<span data-ttu-id="f624b-151">別名</span><span class="sxs-lookup"><span data-stu-id="f624b-151">ALIASES</span></span>

<span data-ttu-id="f624b-152">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f624b-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f624b-153">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f624b-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f624b-154">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f624b-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f624b-155">IDENTITYSOURCE <IIdentitySource [] >： vCenter 單一登入身分識別來源</span><span class="sxs-lookup"><span data-stu-id="f624b-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="f624b-156">`[Alias <String>]`：網域的 NetBIOS 名稱</span><span class="sxs-lookup"><span data-stu-id="f624b-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="f624b-157">`[BaseGroupDn <String>]`：群組的基本辨別名稱</span><span class="sxs-lookup"><span data-stu-id="f624b-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="f624b-158">`[BaseUserDn <String>]`：使用者的基本辨別名稱</span><span class="sxs-lookup"><span data-stu-id="f624b-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="f624b-159">`[Domain <String>]`：網域的 dns 名稱</span><span class="sxs-lookup"><span data-stu-id="f624b-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="f624b-160">`[Name <String>]`：身分識別來源的名稱</span><span class="sxs-lookup"><span data-stu-id="f624b-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="f624b-161">`[Password <String>]`：適用于使用者和群組之基本 DN 的 Active Directory 使用者密碼（最小化）。</span><span class="sxs-lookup"><span data-stu-id="f624b-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="f624b-162">`[PrimaryServer <String>]`：主要伺服器 URL</span><span class="sxs-lookup"><span data-stu-id="f624b-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="f624b-163">`[SecondaryServer <String>]`：次要伺服器 URL</span><span class="sxs-lookup"><span data-stu-id="f624b-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="f624b-164">`[Ssl <SslEnum?>]`：使用 SSL 憑證 (LDAPS) 來保護 LDAP 通訊</span><span class="sxs-lookup"><span data-stu-id="f624b-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="f624b-165">`[Username <String>]`： Active Directory 使用者的識別碼，其最小只能讀取使用者與群組的基本 DN</span><span class="sxs-lookup"><span data-stu-id="f624b-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="f624b-166">INPUTOBJECT <IVMWareIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f624b-166">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f624b-167">`[AuthorizationName <String>]`：私人雲端中 ExpressRoute 線路授權的名稱</span><span class="sxs-lookup"><span data-stu-id="f624b-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="f624b-168">`[ClusterName <String>]`：私人雲端中的群集名稱</span><span class="sxs-lookup"><span data-stu-id="f624b-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="f624b-169">`[HcxEnterpriseSiteName <String>]`：私人雲端中的 HCX 企業網站名稱</span><span class="sxs-lookup"><span data-stu-id="f624b-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="f624b-170">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="f624b-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f624b-171">`[Location <String>]`： Azure region</span><span class="sxs-lookup"><span data-stu-id="f624b-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="f624b-172">`[PrivateCloudName <String>]`：私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="f624b-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="f624b-173">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f624b-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f624b-174">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f624b-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="f624b-175">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f624b-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="f624b-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="f624b-176">RELATED LINKS</span></span>
