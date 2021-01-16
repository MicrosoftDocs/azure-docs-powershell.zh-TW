---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: 2cd73cad57f36130ed11e37ad6dc2147e6c081ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447864"
---
# <span data-ttu-id="d6d04-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="d6d04-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="d6d04-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d6d04-102">SYNOPSIS</span></span>
<span data-ttu-id="d6d04-103">更新步驟。</span><span class="sxs-lookup"><span data-stu-id="d6d04-103">Updates the step.</span></span>

## <span data-ttu-id="d6d04-104">句法</span><span class="sxs-lookup"><span data-stu-id="d6d04-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6d04-105">說明</span><span class="sxs-lookup"><span data-stu-id="d6d04-105">DESCRIPTION</span></span>
<span data-ttu-id="d6d04-106">**AzDeploymentManagerStep** Cmdlet 會使用指定的步驟物件來更新步驟。</span><span class="sxs-lookup"><span data-stu-id="d6d04-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="d6d04-107">這個 Cmdlet 會傳回更新的步驟物件。</span><span class="sxs-lookup"><span data-stu-id="d6d04-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="d6d04-108">示例</span><span class="sxs-lookup"><span data-stu-id="d6d04-108">EXAMPLES</span></span>

### <span data-ttu-id="d6d04-109">範例1</span><span class="sxs-lookup"><span data-stu-id="d6d04-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="d6d04-110">這個命令會分別更新名稱和 ResourceGroup 與 $stepObject 的 Name 和 ResourceGroupName 屬性相符的步驟。</span><span class="sxs-lookup"><span data-stu-id="d6d04-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="d6d04-111">此步驟將會更新為 $stepObject 中設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="d6d04-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="d6d04-112">參數</span><span class="sxs-lookup"><span data-stu-id="d6d04-112">PARAMETERS</span></span>

### <span data-ttu-id="d6d04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6d04-113">-DefaultProfile</span></span>
<span data-ttu-id="d6d04-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6d04-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6d04-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6d04-115">-InputObject</span></span>
<span data-ttu-id="d6d04-116">Step 物件。</span><span class="sxs-lookup"><span data-stu-id="d6d04-116">The step object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6d04-117">-確認</span><span class="sxs-lookup"><span data-stu-id="d6d04-117">-Confirm</span></span>
<span data-ttu-id="d6d04-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d6d04-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6d04-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6d04-119">-WhatIf</span></span>
<span data-ttu-id="d6d04-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6d04-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6d04-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6d04-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6d04-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6d04-122">CommonParameters</span></span>
<span data-ttu-id="d6d04-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d6d04-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6d04-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d6d04-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6d04-125">輸入</span><span class="sxs-lookup"><span data-stu-id="d6d04-125">INPUTS</span></span>

### <span data-ttu-id="d6d04-126">PSStepResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="d6d04-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="d6d04-127">輸出</span><span class="sxs-lookup"><span data-stu-id="d6d04-127">OUTPUTS</span></span>

### <span data-ttu-id="d6d04-128">PSStepResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="d6d04-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="d6d04-129">筆記</span><span class="sxs-lookup"><span data-stu-id="d6d04-129">NOTES</span></span>

## <span data-ttu-id="d6d04-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6d04-130">RELATED LINKS</span></span>