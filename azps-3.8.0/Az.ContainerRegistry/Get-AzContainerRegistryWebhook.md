---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 231ff710e2c8c2945947ecf2d09845e635ee6244
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797345"
---
# <span data-ttu-id="b3ae3-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b3ae3-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="b3ae3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ae3-103">取得容器註冊 webhook。</span><span class="sxs-lookup"><span data-stu-id="b3ae3-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="b3ae3-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3ae3-104">SYNTAX</span></span>

### <span data-ttu-id="b3ae3-105">ListWebhookByNameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b3ae3-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3ae3-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3ae3-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3ae3-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3ae3-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3ae3-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3ae3-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3ae3-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3ae3-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3ae3-110">說明</span><span class="sxs-lookup"><span data-stu-id="b3ae3-110">DESCRIPTION</span></span>
<span data-ttu-id="b3ae3-111">Get-AzContainerRegistryWebhook Cmdlet 會取得容器登錄的指定 webhook，或容器註冊的所有 webhooks。</span><span class="sxs-lookup"><span data-stu-id="b3ae3-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="b3ae3-112">示例</span><span class="sxs-lookup"><span data-stu-id="b3ae3-112">EXAMPLES</span></span>

### <span data-ttu-id="b3ae3-113">範例1：取得容器註冊的指定 webhook</span><span class="sxs-lookup"><span data-stu-id="b3ae3-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="b3ae3-114">取得容器註冊的指定 webhook</span><span class="sxs-lookup"><span data-stu-id="b3ae3-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="b3ae3-115">範例2：取得容器註冊的所有 webhooks</span><span class="sxs-lookup"><span data-stu-id="b3ae3-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="b3ae3-116">取得容器註冊的所有 webhooks</span><span class="sxs-lookup"><span data-stu-id="b3ae3-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="b3ae3-117">範例3：使用配置詳細資料取得容器登錄的指定 webhook</span><span class="sxs-lookup"><span data-stu-id="b3ae3-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="b3ae3-118">使用配置詳細資料取得容器註冊表的指定 webhook</span><span class="sxs-lookup"><span data-stu-id="b3ae3-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="b3ae3-119">參數</span><span class="sxs-lookup"><span data-stu-id="b3ae3-119">PARAMETERS</span></span>

### <span data-ttu-id="b3ae3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ae3-120">-DefaultProfile</span></span>
<span data-ttu-id="b3ae3-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3ae3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3ae3-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3ae3-122">-IncludeConfiguration</span></span>
<span data-ttu-id="b3ae3-123">取得 webhook 的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="b3ae3-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="b3ae3-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3ae3-124">-Name</span></span>
<span data-ttu-id="b3ae3-125">Webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="b3ae3-125">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ae3-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="b3ae3-126">-Registry</span></span>
<span data-ttu-id="b3ae3-127">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="b3ae3-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ae3-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b3ae3-128">-RegistryName</span></span>
<span data-ttu-id="b3ae3-129">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="b3ae3-129">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ae3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3ae3-130">-ResourceGroupName</span></span>
<span data-ttu-id="b3ae3-131">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b3ae3-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ae3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3ae3-132">-ResourceId</span></span>
<span data-ttu-id="b3ae3-133">容器登錄 Webhook 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b3ae3-133">The container registry Webhook resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ae3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ae3-134">CommonParameters</span></span>
<span data-ttu-id="b3ae3-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3ae3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ae3-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b3ae3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ae3-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b3ae3-137">INPUTS</span></span>

### <span data-ttu-id="b3ae3-138">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b3ae3-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="b3ae3-139">System.object</span><span class="sxs-lookup"><span data-stu-id="b3ae3-139">System.String</span></span>

## <span data-ttu-id="b3ae3-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b3ae3-140">OUTPUTS</span></span>

### <span data-ttu-id="b3ae3-141">PSContainerRegistryWebhook 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b3ae3-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="b3ae3-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b3ae3-142">NOTES</span></span>

## <span data-ttu-id="b3ae3-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3ae3-143">RELATED LINKS</span></span>

[<span data-ttu-id="b3ae3-144">新-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b3ae3-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b3ae3-145">更新-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b3ae3-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b3ae3-146">移除-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b3ae3-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b3ae3-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b3ae3-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)