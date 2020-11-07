---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/start-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
ms.openlocfilehash: 5858a1f17bcae3c003ed7b40200c065c36eb2b1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624742"
---
# <span data-ttu-id="d68ae-101">Start-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="d68ae-101">Start-AzureRmAksDashboard</span></span>

## <span data-ttu-id="d68ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d68ae-102">SYNOPSIS</span></span>
<span data-ttu-id="d68ae-103">建立 Kubectl SSH 隧道至 managed 群集的儀表板。</span><span class="sxs-lookup"><span data-stu-id="d68ae-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d68ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="d68ae-104">SYNTAX</span></span>

### <span data-ttu-id="d68ae-105">GroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d68ae-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzureRmAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d68ae-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d68ae-106">InputObjectParameterSet</span></span>
```
Start-AzureRmAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d68ae-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d68ae-107">IdParameterSet</span></span>
```
Start-AzureRmAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d68ae-108">說明</span><span class="sxs-lookup"><span data-stu-id="d68ae-108">DESCRIPTION</span></span>
<span data-ttu-id="d68ae-109">建立 Kubectl SSH 隧道至 managed 群集的儀表板。</span><span class="sxs-lookup"><span data-stu-id="d68ae-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="d68ae-110">SSH 隧道是在稱為 Kubectl-Tunnel 的 PowerShell 作業中設定，可透過執行來找到 `Get-Job` 。</span><span class="sxs-lookup"><span data-stu-id="d68ae-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="d68ae-111">隧道應該可透過進行 [http://127.0.0.1:8001](http://127.0.0.1:8001) 。</span><span class="sxs-lookup"><span data-stu-id="d68ae-111">The tunnel should be accessable via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="d68ae-112">示例</span><span class="sxs-lookup"><span data-stu-id="d68ae-112">EXAMPLES</span></span>

### <span data-ttu-id="d68ae-113">啟動 SSH 隧道並開啟瀏覽器至 Kubernetes 儀表板</span><span class="sxs-lookup"><span data-stu-id="d68ae-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzureRmAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="d68ae-114">參數</span><span class="sxs-lookup"><span data-stu-id="d68ae-114">PARAMETERS</span></span>

### <span data-ttu-id="d68ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d68ae-115">-DefaultProfile</span></span>
<span data-ttu-id="d68ae-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d68ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d68ae-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="d68ae-117">-DisableBrowser</span></span>
<span data-ttu-id="d68ae-118">在 establising kubectl 埠轉寄之後，不要使用 pop 開啟瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="d68ae-118">Do not pop open a browser after establising the kubectl port-forward.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d68ae-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="d68ae-119">-Id</span></span>
<span data-ttu-id="d68ae-120">受管理的 Kubernetes 群集的 Id</span><span class="sxs-lookup"><span data-stu-id="d68ae-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d68ae-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d68ae-121">-InputObject</span></span>
<span data-ttu-id="d68ae-122">PSKubernetesCluster 物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="d68ae-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d68ae-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="d68ae-123">-Name</span></span>
<span data-ttu-id="d68ae-124">受管理的 Kubernetes 群集的名稱</span><span class="sxs-lookup"><span data-stu-id="d68ae-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d68ae-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d68ae-125">-PassThru</span></span>
<span data-ttu-id="d68ae-126">如果傳遞的話，Cmdlet 會傳回 KubeTunnelJob。</span><span class="sxs-lookup"><span data-stu-id="d68ae-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d68ae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d68ae-127">-ResourceGroupName</span></span>
<span data-ttu-id="d68ae-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="d68ae-128">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d68ae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d68ae-129">CommonParameters</span></span>
<span data-ttu-id="d68ae-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d68ae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d68ae-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d68ae-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d68ae-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d68ae-132">INPUTS</span></span>

### <span data-ttu-id="d68ae-133">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="d68ae-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="d68ae-134">System.object</span><span class="sxs-lookup"><span data-stu-id="d68ae-134">System.String</span></span>

## <span data-ttu-id="d68ae-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d68ae-135">OUTPUTS</span></span>

### <span data-ttu-id="d68ae-136">KubeTunnelJob 中的 Aks</span><span class="sxs-lookup"><span data-stu-id="d68ae-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="d68ae-137">筆記</span><span class="sxs-lookup"><span data-stu-id="d68ae-137">NOTES</span></span>

## <span data-ttu-id="d68ae-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="d68ae-138">RELATED LINKS</span></span>