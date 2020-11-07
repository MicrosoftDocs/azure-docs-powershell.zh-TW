---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: ad2a97895f4876c008d1740e962bb3b746e67ec8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626334"
---
# <span data-ttu-id="b01d5-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="b01d5-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="b01d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b01d5-102">SYNOPSIS</span></span>
<span data-ttu-id="b01d5-103">檢查容器註冊名稱的可用性。</span><span class="sxs-lookup"><span data-stu-id="b01d5-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b01d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="b01d5-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b01d5-105">說明</span><span class="sxs-lookup"><span data-stu-id="b01d5-105">DESCRIPTION</span></span>
<span data-ttu-id="b01d5-106">**Test AzureRmContainerRegistryNameAvailability** Cmdlet 會檢查容器登錄名稱是否有效且可供使用。</span><span class="sxs-lookup"><span data-stu-id="b01d5-106">The **Test-AzureRmContainerRegistryNameAvailability** cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="b01d5-107">示例</span><span class="sxs-lookup"><span data-stu-id="b01d5-107">EXAMPLES</span></span>

### <span data-ttu-id="b01d5-108">範例1：檢查容器註冊名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="b01d5-108">Example 1: Check the availability of a container registry name</span></span>
```
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="b01d5-109">這個命令會檢查容器註冊名稱的可用性 `SomeRegistryName` 。</span><span class="sxs-lookup"><span data-stu-id="b01d5-109">This command checks the availability of the container registry name `SomeRegistryName`.</span></span>

## <span data-ttu-id="b01d5-110">參數</span><span class="sxs-lookup"><span data-stu-id="b01d5-110">PARAMETERS</span></span>

### <span data-ttu-id="b01d5-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="b01d5-111">-Name</span></span>
<span data-ttu-id="b01d5-112">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="b01d5-112">Container Registry Name.</span></span>

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

### <span data-ttu-id="b01d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b01d5-113">-DefaultProfile</span></span>
<span data-ttu-id="b01d5-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b01d5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b01d5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b01d5-115">CommonParameters</span></span>
<span data-ttu-id="b01d5-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b01d5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b01d5-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b01d5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b01d5-118">輸入</span><span class="sxs-lookup"><span data-stu-id="b01d5-118">INPUTS</span></span>

## <span data-ttu-id="b01d5-119">輸出</span><span class="sxs-lookup"><span data-stu-id="b01d5-119">OUTPUTS</span></span>

### <span data-ttu-id="b01d5-120">RegistryNameStatus 中的 ContainerRegistry。</span><span class="sxs-lookup"><span data-stu-id="b01d5-120">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="b01d5-121">筆記</span><span class="sxs-lookup"><span data-stu-id="b01d5-121">NOTES</span></span>

## <span data-ttu-id="b01d5-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="b01d5-122">RELATED LINKS</span></span>

[<span data-ttu-id="b01d5-123">新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b01d5-123">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)
