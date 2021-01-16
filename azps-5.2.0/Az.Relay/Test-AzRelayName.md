---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 45c3e0a4271a5eb2527ff25b5858a3f5aa35dc0a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284887"
---
# <span data-ttu-id="c4ce2-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="c4ce2-101">Test-AzRelayName</span></span>

## <span data-ttu-id="c4ce2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ce2-103">檢查指定命名空間名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="c4ce2-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="c4ce2-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4ce2-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4ce2-105">說明</span><span class="sxs-lookup"><span data-stu-id="c4ce2-105">DESCRIPTION</span></span>
<span data-ttu-id="c4ce2-106">**Test AzRelayName** Cmdlet 會檢查命名空間名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="c4ce2-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="c4ce2-107">示例</span><span class="sxs-lookup"><span data-stu-id="c4ce2-107">EXAMPLES</span></span>

### <span data-ttu-id="c4ce2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c4ce2-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="c4ce2-109">範例2</span><span class="sxs-lookup"><span data-stu-id="c4ce2-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="c4ce2-110">範例3</span><span class="sxs-lookup"><span data-stu-id="c4ce2-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="c4ce2-111">傳回命名空間名稱的可用性狀態</span><span class="sxs-lookup"><span data-stu-id="c4ce2-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="c4ce2-112">參數</span><span class="sxs-lookup"><span data-stu-id="c4ce2-112">PARAMETERS</span></span>

### <span data-ttu-id="c4ce2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ce2-113">-DefaultProfile</span></span>
<span data-ttu-id="c4ce2-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4ce2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4ce2-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="c4ce2-115">-Namespace</span></span>
<span data-ttu-id="c4ce2-116">中繼命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="c4ce2-116">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ce2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ce2-117">CommonParameters</span></span>
<span data-ttu-id="c4ce2-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4ce2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ce2-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c4ce2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ce2-120">輸入</span><span class="sxs-lookup"><span data-stu-id="c4ce2-120">INPUTS</span></span>

### <span data-ttu-id="c4ce2-121">System.object</span><span class="sxs-lookup"><span data-stu-id="c4ce2-121">System.String</span></span>

## <span data-ttu-id="c4ce2-122">輸出</span><span class="sxs-lookup"><span data-stu-id="c4ce2-122">OUTPUTS</span></span>

### <span data-ttu-id="c4ce2-123">PSCheckNameAvailabilityResultAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c4ce2-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="c4ce2-124">筆記</span><span class="sxs-lookup"><span data-stu-id="c4ce2-124">NOTES</span></span>

## <span data-ttu-id="c4ce2-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4ce2-125">RELATED LINKS</span></span>