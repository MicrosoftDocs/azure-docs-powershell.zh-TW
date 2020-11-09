---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284818"
---
# <span data-ttu-id="7b7b8-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7b7b8-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="7b7b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b7b8-102">SYNOPSIS</span></span>
<span data-ttu-id="7b7b8-103">取得推出。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-103">Gets the rollout.</span></span>

## <span data-ttu-id="7b7b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b7b8-104">SYNTAX</span></span>

### <span data-ttu-id="7b7b8-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="7b7b8-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b7b8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b7b8-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b7b8-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7b7b8-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b7b8-108">說明</span><span class="sxs-lookup"><span data-stu-id="7b7b8-108">DESCRIPTION</span></span>
<span data-ttu-id="7b7b8-109">**AzDeploymentManagerRollout** Cmdlet 會取得推出，並傳回一個物件，該物件代表有關推出進度之所有詳細資訊的推出。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="7b7b8-110">依其名稱和資源群組名稱來指定推出。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="7b7b8-111">或者，您也可以提供推出物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="7b7b8-112">傳回的推出物件包含已部署的服務、服務單元和步驟，以及進行中的步驟。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="7b7b8-113">尚未部署的回應不在回應中。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="7b7b8-114">示例</span><span class="sxs-lookup"><span data-stu-id="7b7b8-114">EXAMPLES</span></span>

### <span data-ttu-id="7b7b8-115">範例1取得推出</span><span class="sxs-lookup"><span data-stu-id="7b7b8-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="7b7b8-116">這個命令會在 ContosoResourceGroup 中取得名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="7b7b8-117">範例2取得並顯示推出詳細資料</span><span class="sxs-lookup"><span data-stu-id="7b7b8-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="7b7b8-118">這個命令會在 ContosoResourceGroup 中取得名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="7b7b8-119">-Verbose 開關會以分層顯示所有推出的詳細資料，針對推出的整體視圖，顯示每個步驟的服務、ServiceUnits 和步驟，以及每個步驟的各個 ServiceUnit 與內容資訊。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="7b7b8-120">範例3：使用資源識別碼取得推出</span><span class="sxs-lookup"><span data-stu-id="7b7b8-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="7b7b8-121">這個命令會在 ContosoResourceGroup 中取得名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7b7b8-122">範例4：使用 [推出] 物件取得推出。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="7b7b8-123">這個命令會分別取得名稱和 ResourceGroup 與 $rolloutObject 之 Name 和 ResourceGroupName 屬性相符的推出。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="7b7b8-124">參數</span><span class="sxs-lookup"><span data-stu-id="7b7b8-124">PARAMETERS</span></span>

### <span data-ttu-id="7b7b8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b7b8-125">-DefaultProfile</span></span>
<span data-ttu-id="7b7b8-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b7b8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b7b8-127">-InputObject</span></span>
<span data-ttu-id="7b7b8-128">推出物件。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-128">Rollout object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b7b8-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="7b7b8-129">-Name</span></span>
<span data-ttu-id="7b7b8-130">推出的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-130">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b7b8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b7b8-131">-ResourceGroupName</span></span>
<span data-ttu-id="7b7b8-132">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-132">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b7b8-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b7b8-133">-ResourceId</span></span>
<span data-ttu-id="7b7b8-134">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-134">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b7b8-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="7b7b8-135">-RetryAttempt</span></span>
<span data-ttu-id="7b7b8-136">首次嘗試嘗試。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-136">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b7b8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b7b8-137">CommonParameters</span></span>
<span data-ttu-id="7b7b8-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b7b8-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b7b8-140">輸入</span><span class="sxs-lookup"><span data-stu-id="7b7b8-140">INPUTS</span></span>

### <span data-ttu-id="7b7b8-141">System.object</span><span class="sxs-lookup"><span data-stu-id="7b7b8-141">System.String</span></span>

### <span data-ttu-id="7b7b8-142">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7b7b8-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7b7b8-143">PSRollout 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7b7b8-144">輸出</span><span class="sxs-lookup"><span data-stu-id="7b7b8-144">OUTPUTS</span></span>

### <span data-ttu-id="7b7b8-145">PSRollout 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="7b7b8-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7b7b8-146">筆記</span><span class="sxs-lookup"><span data-stu-id="7b7b8-146">NOTES</span></span>

## <span data-ttu-id="7b7b8-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b7b8-147">RELATED LINKS</span></span>