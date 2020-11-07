---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797313"
---
# <span data-ttu-id="dc753-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="dc753-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="dc753-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc753-102">SYNOPSIS</span></span>
<span data-ttu-id="dc753-103">檢查容器註冊名稱的可用性。</span><span class="sxs-lookup"><span data-stu-id="dc753-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="dc753-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc753-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc753-105">說明</span><span class="sxs-lookup"><span data-stu-id="dc753-105">DESCRIPTION</span></span>
<span data-ttu-id="dc753-106">Test-AzContainerRegistryNameAvailability Cmdlet 會檢查容器登錄名稱是否有效且可供使用。</span><span class="sxs-lookup"><span data-stu-id="dc753-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="dc753-107">示例</span><span class="sxs-lookup"><span data-stu-id="dc753-107">EXAMPLES</span></span>

### <span data-ttu-id="dc753-108">範例1：檢查容器註冊名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="dc753-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="dc753-109">這個命令會檢查容器登錄名稱 SomeRegistryName 的可用性 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="dc753-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="dc753-110">參數</span><span class="sxs-lookup"><span data-stu-id="dc753-110">PARAMETERS</span></span>

### <span data-ttu-id="dc753-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc753-111">-DefaultProfile</span></span>
<span data-ttu-id="dc753-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="dc753-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc753-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc753-113">-Name</span></span>
<span data-ttu-id="dc753-114">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="dc753-114">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc753-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc753-115">CommonParameters</span></span>
<span data-ttu-id="dc753-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc753-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc753-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dc753-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc753-118">輸入</span><span class="sxs-lookup"><span data-stu-id="dc753-118">INPUTS</span></span>

### <span data-ttu-id="dc753-119">System.object</span><span class="sxs-lookup"><span data-stu-id="dc753-119">System.String</span></span>

## <span data-ttu-id="dc753-120">輸出</span><span class="sxs-lookup"><span data-stu-id="dc753-120">OUTPUTS</span></span>

### <span data-ttu-id="dc753-121">RegistryNameStatus 中的 ContainerRegistry。</span><span class="sxs-lookup"><span data-stu-id="dc753-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="dc753-122">筆記</span><span class="sxs-lookup"><span data-stu-id="dc753-122">NOTES</span></span>

## <span data-ttu-id="dc753-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc753-123">RELATED LINKS</span></span>

[<span data-ttu-id="dc753-124">新-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dc753-124">New-AzContainerRegistry</span></span>]()
