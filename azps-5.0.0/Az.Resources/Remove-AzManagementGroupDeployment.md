---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: cf2f8f011803deb4649b8c7d1550c421c9e62017
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285959"
---
# <span data-ttu-id="7bdaf-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7bdaf-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="7bdaf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7bdaf-102">SYNOPSIS</span></span>
<span data-ttu-id="7bdaf-103">移除管理群組中的部署以及任何相關聯的作業</span><span class="sxs-lookup"><span data-stu-id="7bdaf-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="7bdaf-104">句法</span><span class="sxs-lookup"><span data-stu-id="7bdaf-104">SYNTAX</span></span>

### <span data-ttu-id="7bdaf-105">RemoveByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="7bdaf-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bdaf-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="7bdaf-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bdaf-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="7bdaf-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bdaf-108">說明</span><span class="sxs-lookup"><span data-stu-id="7bdaf-108">DESCRIPTION</span></span>
<span data-ttu-id="7bdaf-109">**AzManagementGroupDeployment** Cmdlet 會移除管理群組上的 Azure 部署以及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="7bdaf-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="7bdaf-110">示例</span><span class="sxs-lookup"><span data-stu-id="7bdaf-110">EXAMPLES</span></span>

### <span data-ttu-id="7bdaf-111">範例1：移除具有指定名稱的部署</span><span class="sxs-lookup"><span data-stu-id="7bdaf-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="7bdaf-112">這個命令會移除管理群組 "myMG" 的部署 "RolesDeployment"。</span><span class="sxs-lookup"><span data-stu-id="7bdaf-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="7bdaf-113">範例2：取得並移除部署</span><span class="sxs-lookup"><span data-stu-id="7bdaf-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="7bdaf-114">這個命令會取得管理群組「myMG」的部署「RolesDeployment」，然後將它移除。</span><span class="sxs-lookup"><span data-stu-id="7bdaf-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="7bdaf-115">參數</span><span class="sxs-lookup"><span data-stu-id="7bdaf-115">PARAMETERS</span></span>

### <span data-ttu-id="7bdaf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bdaf-116">-AsJob</span></span>
<span data-ttu-id="7bdaf-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7bdaf-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7bdaf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bdaf-118">-DefaultProfile</span></span>
<span data-ttu-id="7bdaf-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7bdaf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bdaf-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="7bdaf-120">-Id</span></span>
<span data-ttu-id="7bdaf-121">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7bdaf-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="7bdaf-122">範例：/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="7bdaf-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdaf-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bdaf-123">-InputObject</span></span>
<span data-ttu-id="7bdaf-124">部署物件。</span><span class="sxs-lookup"><span data-stu-id="7bdaf-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bdaf-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="7bdaf-125">-ManagementGroupId</span></span>
<span data-ttu-id="7bdaf-126">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="7bdaf-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdaf-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="7bdaf-127">-Name</span></span>
<span data-ttu-id="7bdaf-128">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bdaf-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bdaf-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bdaf-129">-PassThru</span></span>
<span data-ttu-id="7bdaf-130">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="7bdaf-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7bdaf-131">-預先</span><span class="sxs-lookup"><span data-stu-id="7bdaf-131">-Pre</span></span>
<span data-ttu-id="7bdaf-132">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="7bdaf-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7bdaf-133">-確認</span><span class="sxs-lookup"><span data-stu-id="7bdaf-133">-Confirm</span></span>
<span data-ttu-id="7bdaf-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7bdaf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bdaf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bdaf-135">-WhatIf</span></span>
<span data-ttu-id="7bdaf-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7bdaf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bdaf-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7bdaf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bdaf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bdaf-138">CommonParameters</span></span>
<span data-ttu-id="7bdaf-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7bdaf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bdaf-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7bdaf-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bdaf-141">輸入</span><span class="sxs-lookup"><span data-stu-id="7bdaf-141">INPUTS</span></span>

### <span data-ttu-id="7bdaf-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="7bdaf-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="7bdaf-143">輸出</span><span class="sxs-lookup"><span data-stu-id="7bdaf-143">OUTPUTS</span></span>

### <span data-ttu-id="7bdaf-144">System.object</span><span class="sxs-lookup"><span data-stu-id="7bdaf-144">System.Boolean</span></span>

## <span data-ttu-id="7bdaf-145">筆記</span><span class="sxs-lookup"><span data-stu-id="7bdaf-145">NOTES</span></span>

## <span data-ttu-id="7bdaf-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bdaf-146">RELATED LINKS</span></span>