---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/send-feedback
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Send-Feedback.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Send-Feedback.md
ms.openlocfilehash: 1405886572efabf1ffc91f071f262ca98515d141
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275708"
---
# <span data-ttu-id="234b9-101">Send-Feedback</span><span class="sxs-lookup"><span data-stu-id="234b9-101">Send-Feedback</span></span>

## <span data-ttu-id="234b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="234b9-102">SYNOPSIS</span></span>
<span data-ttu-id="234b9-103">透過一組引導提示，將意見反應傳送給 Azure PowerShell 小組。</span><span class="sxs-lookup"><span data-stu-id="234b9-103">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

## <span data-ttu-id="234b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="234b9-104">SYNTAX</span></span>

```
Send-Feedback [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="234b9-105">說明</span><span class="sxs-lookup"><span data-stu-id="234b9-105">DESCRIPTION</span></span>
<span data-ttu-id="234b9-106">Send-Feedback Cmdlet 會將意見反應傳送給 Azure PowerShell 小組。</span><span class="sxs-lookup"><span data-stu-id="234b9-106">The Send-Feedback cmdlet sends feedback to the Azure PowerShell team.</span></span>

## <span data-ttu-id="234b9-107">示例</span><span class="sxs-lookup"><span data-stu-id="234b9-107">EXAMPLES</span></span>

### <span data-ttu-id="234b9-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="234b9-108">Example 1:</span></span>
```
PS C:\> Send-Feedback

With zero (0) being the least and ten (10) being the most, how likely are you to recommend Azure PowerShell to a friend or colleague?

10

What does Azure PowerShell do well?

Response.

Upon what could Azure PowerShell improve?

Response.

Please enter your email if you are interested in providing follow up information:

your@email.com
```

## <span data-ttu-id="234b9-109">參數</span><span class="sxs-lookup"><span data-stu-id="234b9-109">PARAMETERS</span></span>

### <span data-ttu-id="234b9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="234b9-110">-DefaultProfile</span></span>
<span data-ttu-id="234b9-111">用於與 azure 進行通訊的認證、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="234b9-111">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="234b9-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="234b9-112">CommonParameters</span></span>
<span data-ttu-id="234b9-113">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="234b9-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="234b9-114">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="234b9-114">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="234b9-115">輸入</span><span class="sxs-lookup"><span data-stu-id="234b9-115">INPUTS</span></span>

### <span data-ttu-id="234b9-116">所有</span><span class="sxs-lookup"><span data-stu-id="234b9-116">None</span></span>

## <span data-ttu-id="234b9-117">輸出</span><span class="sxs-lookup"><span data-stu-id="234b9-117">OUTPUTS</span></span>

### <span data-ttu-id="234b9-118">System.void</span><span class="sxs-lookup"><span data-stu-id="234b9-118">System.Void</span></span>

## <span data-ttu-id="234b9-119">筆記</span><span class="sxs-lookup"><span data-stu-id="234b9-119">NOTES</span></span>

## <span data-ttu-id="234b9-120">相關連結</span><span class="sxs-lookup"><span data-stu-id="234b9-120">RELATED LINKS</span></span>