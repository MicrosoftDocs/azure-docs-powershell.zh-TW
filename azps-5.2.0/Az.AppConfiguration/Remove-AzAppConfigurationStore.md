---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273072"
---
# <span data-ttu-id="5facb-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="5facb-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="5facb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5facb-102">SYNOPSIS</span></span>
<span data-ttu-id="5facb-103">刪除配置存放區。</span><span class="sxs-lookup"><span data-stu-id="5facb-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="5facb-104">句法</span><span class="sxs-lookup"><span data-stu-id="5facb-104">SYNTAX</span></span>

### <span data-ttu-id="5facb-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="5facb-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5facb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5facb-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5facb-107">說明</span><span class="sxs-lookup"><span data-stu-id="5facb-107">DESCRIPTION</span></span>
<span data-ttu-id="5facb-108">刪除配置存放區。</span><span class="sxs-lookup"><span data-stu-id="5facb-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="5facb-109">示例</span><span class="sxs-lookup"><span data-stu-id="5facb-109">EXAMPLES</span></span>

### <span data-ttu-id="5facb-110">範例1：移除 app 配置存放區</span><span class="sxs-lookup"><span data-stu-id="5facb-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="5facb-111">這個命令會移除 app 設定存放區。</span><span class="sxs-lookup"><span data-stu-id="5facb-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="5facb-112">範例2：移除 app 配置存放區</span><span class="sxs-lookup"><span data-stu-id="5facb-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="5facb-113">這個命令會移除 app 設定存放區。</span><span class="sxs-lookup"><span data-stu-id="5facb-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="5facb-114">參數</span><span class="sxs-lookup"><span data-stu-id="5facb-114">PARAMETERS</span></span>

### <span data-ttu-id="5facb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5facb-115">-AsJob</span></span>
<span data-ttu-id="5facb-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="5facb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5facb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5facb-117">-DefaultProfile</span></span>
<span data-ttu-id="5facb-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5facb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5facb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5facb-119">-InputObject</span></span>
<span data-ttu-id="5facb-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5facb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5facb-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5facb-121">-Name</span></span>
<span data-ttu-id="5facb-122">配置存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="5facb-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="5facb-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5facb-123">-NoWait</span></span>
<span data-ttu-id="5facb-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="5facb-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5facb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5facb-125">-PassThru</span></span>
<span data-ttu-id="5facb-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="5facb-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5facb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5facb-127">-ResourceGroupName</span></span>
<span data-ttu-id="5facb-128">容器註冊表所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5facb-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="5facb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5facb-129">-SubscriptionId</span></span>
<span data-ttu-id="5facb-130">Microsoft Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="5facb-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="5facb-131">-確認</span><span class="sxs-lookup"><span data-stu-id="5facb-131">-Confirm</span></span>
<span data-ttu-id="5facb-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5facb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5facb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5facb-133">-WhatIf</span></span>
<span data-ttu-id="5facb-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5facb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5facb-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5facb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5facb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5facb-136">CommonParameters</span></span>
<span data-ttu-id="5facb-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5facb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5facb-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5facb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5facb-139">輸入</span><span class="sxs-lookup"><span data-stu-id="5facb-139">INPUTS</span></span>

### <span data-ttu-id="5facb-140">IAppConfigurationIdentity （AppConfiguration）的</span><span class="sxs-lookup"><span data-stu-id="5facb-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="5facb-141">輸出</span><span class="sxs-lookup"><span data-stu-id="5facb-141">OUTPUTS</span></span>

### <span data-ttu-id="5facb-142">System.object</span><span class="sxs-lookup"><span data-stu-id="5facb-142">System.Boolean</span></span>

## <span data-ttu-id="5facb-143">筆記</span><span class="sxs-lookup"><span data-stu-id="5facb-143">NOTES</span></span>

<span data-ttu-id="5facb-144">別名</span><span class="sxs-lookup"><span data-stu-id="5facb-144">ALIASES</span></span>

<span data-ttu-id="5facb-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5facb-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5facb-146">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5facb-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5facb-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5facb-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5facb-148">INPUTOBJECT <IAppConfigurationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5facb-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5facb-149">`[ConfigStoreName <String>]`：配置存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="5facb-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="5facb-150">`[GroupName <String>]`：私人連結資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5facb-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="5facb-151">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="5facb-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5facb-152">`[PrivateEndpointConnectionName <String>]`：私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="5facb-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="5facb-153">`[ResourceGroupName <String>]`：容器註冊表所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5facb-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="5facb-154">`[SubscriptionId <String>]`： Microsoft Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="5facb-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="5facb-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="5facb-155">RELATED LINKS</span></span>
