---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
ms.openlocfilehash: 7264733055322c3d5886ff57f50d22e23f932a7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623734"
---
# <span data-ttu-id="ed47b-101">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed47b-101">New-AzureRmResourceGroup</span></span>

## <span data-ttu-id="ed47b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed47b-102">SYNOPSIS</span></span>
<span data-ttu-id="ed47b-103">建立 Azure 資源群組。</span><span class="sxs-lookup"><span data-stu-id="ed47b-103">Creates an Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed47b-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed47b-104">SYNTAX</span></span>

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed47b-105">說明</span><span class="sxs-lookup"><span data-stu-id="ed47b-105">DESCRIPTION</span></span>
<span data-ttu-id="ed47b-106">**新的-AzureRmResourceGroup** Cmdlet 會建立 Azure 資源群組。</span><span class="sxs-lookup"><span data-stu-id="ed47b-106">The **New-AzureRmResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="ed47b-107">您可以只使用名稱和位置來建立資源群組，然後使用 New-AzureRmResource Cmdlet 來建立要新增至資源群組的資源。</span><span class="sxs-lookup"><span data-stu-id="ed47b-107">You can create a resource group by using just a name and location, and then use the New-AzureRmResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="ed47b-108">若要將部署新增至現有的資源群組，請使用 New-AzureRmResourceGroupDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed47b-108">To add a deployment to an existing resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="ed47b-109">若要新增資源至現有的資源群組，請使用 **AzureRmResource** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed47b-109">To add a resource to an existing resource group, use the **New-AzureRmResource** cmdlet.</span></span> <span data-ttu-id="ed47b-110">Azure 資源是使用者管理的 Azure 實體，例如資料庫伺服器、資料庫或網站。</span><span class="sxs-lookup"><span data-stu-id="ed47b-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="ed47b-111">Azure 資源群組是一個以單位形式部署的 Azure 資源集合。</span><span class="sxs-lookup"><span data-stu-id="ed47b-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="ed47b-112">示例</span><span class="sxs-lookup"><span data-stu-id="ed47b-112">EXAMPLES</span></span>

### <span data-ttu-id="ed47b-113">範例1：建立空白的資源群組</span><span class="sxs-lookup"><span data-stu-id="ed47b-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="ed47b-114">這個命令會建立沒有資源的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ed47b-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="ed47b-115">您可以使用 **新的-AzureRmResource** 或 **AzureRmResourceGroupDeployment** Cmdlet，將資源和部署新增至此資源群組。</span><span class="sxs-lookup"><span data-stu-id="ed47b-115">You can use the **New-AzureRmResource** or **New-AzureRmResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="ed47b-116">範例2：使用位置參數建立空白的資源群組</span><span class="sxs-lookup"><span data-stu-id="ed47b-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzureRmResourceGroup RG01 "South Central US"
```

<span data-ttu-id="ed47b-117">這個命令會建立沒有資源的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ed47b-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="ed47b-118">範例3：使用標籤建立資源群組</span><span class="sxs-lookup"><span data-stu-id="ed47b-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="ed47b-119">這個命令會建立空白的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ed47b-119">This command creates an empty resource group.</span></span> <span data-ttu-id="ed47b-120">這個命令與範例1中的命令一樣，只不過它會將標記指派給資源群組。</span><span class="sxs-lookup"><span data-stu-id="ed47b-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="ed47b-121">名為 Empty 的第一個標籤可以用來找出沒有資源的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ed47b-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="ed47b-122">第二個標記為「部門」，且具有 [行銷] 的值。</span><span class="sxs-lookup"><span data-stu-id="ed47b-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="ed47b-123">您可以使用像這樣的標記，將資源群組分類以進行管理或編制預算。</span><span class="sxs-lookup"><span data-stu-id="ed47b-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="ed47b-124">參數</span><span class="sxs-lookup"><span data-stu-id="ed47b-124">PARAMETERS</span></span>

### <span data-ttu-id="ed47b-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ed47b-125">-ApiVersion</span></span>
<span data-ttu-id="ed47b-126">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="ed47b-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ed47b-127">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="ed47b-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="ed47b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed47b-128">-DefaultProfile</span></span>
<span data-ttu-id="ed47b-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ed47b-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed47b-130">-Force</span><span class="sxs-lookup"><span data-stu-id="ed47b-130">-Force</span></span>
<span data-ttu-id="ed47b-131">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ed47b-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ed47b-132">-位置</span><span class="sxs-lookup"><span data-stu-id="ed47b-132">-Location</span></span>
<span data-ttu-id="ed47b-133">指定資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="ed47b-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="ed47b-134">指定 Azure 資料中心位置，例如 [西部] 或 [東南部]。</span><span class="sxs-lookup"><span data-stu-id="ed47b-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="ed47b-135">您可以將資源群組放在任何位置。</span><span class="sxs-lookup"><span data-stu-id="ed47b-135">You can place a resource group in any location.</span></span> <span data-ttu-id="ed47b-136">資源群組不必須位於與您的 Azure 訂閱相同的位置，或與其資源位於相同的位置。</span><span class="sxs-lookup"><span data-stu-id="ed47b-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="ed47b-137">若要判斷哪個位置支援每個資源類型，請使用 Get-AzureRmResourceProvider Cmdlet 與 *ProviderNamespace* 參數。</span><span class="sxs-lookup"><span data-stu-id="ed47b-137">To determine which location supports each resource type, use the Get-AzureRmResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed47b-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed47b-138">-Name</span></span>
<span data-ttu-id="ed47b-139">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed47b-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="ed47b-140">資源名稱在訂閱中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="ed47b-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="ed47b-141">如果已經存在該名稱的資源群組，該命令會在您替換現有的資源群組之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed47b-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed47b-142">-預先</span><span class="sxs-lookup"><span data-stu-id="ed47b-142">-Pre</span></span>
<span data-ttu-id="ed47b-143">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="ed47b-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ed47b-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="ed47b-144">-Tag</span></span>
<span data-ttu-id="ed47b-145">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="ed47b-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ed47b-146">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"} 若要新增或變更標記，您必須取代資源群組的標記集合。</span><span class="sxs-lookup"><span data-stu-id="ed47b-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="ed47b-147">在您指派標籤至資源和群組之後，您可以使用 Get-AzureRmResource 和 Get-AzureRmResourceGroup 的 *tag* 參數，依標記名稱或名稱和值來搜尋資源和群組。</span><span class="sxs-lookup"><span data-stu-id="ed47b-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="ed47b-148">您可以使用標籤將資源分類（例如 [部門] 或 [成本中心]），或追蹤資源的備忘稿或意見。</span><span class="sxs-lookup"><span data-stu-id="ed47b-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="ed47b-149">若要取得預先定義的標記，請使用 Get-AzureRMTag Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed47b-149">To get your predefined tags, use the Get-AzureRMTag cmdlet.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed47b-150">-確認</span><span class="sxs-lookup"><span data-stu-id="ed47b-150">-Confirm</span></span>
<span data-ttu-id="ed47b-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed47b-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed47b-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed47b-152">-WhatIf</span></span>
<span data-ttu-id="ed47b-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed47b-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed47b-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed47b-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed47b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed47b-155">CommonParameters</span></span>
<span data-ttu-id="ed47b-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed47b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed47b-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed47b-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed47b-158">輸入</span><span class="sxs-lookup"><span data-stu-id="ed47b-158">INPUTS</span></span>

### <span data-ttu-id="ed47b-159">所有</span><span class="sxs-lookup"><span data-stu-id="ed47b-159">None</span></span>

## <span data-ttu-id="ed47b-160">輸出</span><span class="sxs-lookup"><span data-stu-id="ed47b-160">OUTPUTS</span></span>

### <span data-ttu-id="ed47b-161">PSResourceGroup 中的 ResourceManagement。</span><span class="sxs-lookup"><span data-stu-id="ed47b-161">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroup</span></span>

## <span data-ttu-id="ed47b-162">筆記</span><span class="sxs-lookup"><span data-stu-id="ed47b-162">NOTES</span></span>

## <span data-ttu-id="ed47b-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed47b-163">RELATED LINKS</span></span>

[<span data-ttu-id="ed47b-164">AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ed47b-164">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="ed47b-165">AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed47b-165">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="ed47b-166">新-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ed47b-166">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="ed47b-167">新-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ed47b-167">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="ed47b-168">移除-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed47b-168">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="ed47b-169">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed47b-169">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)