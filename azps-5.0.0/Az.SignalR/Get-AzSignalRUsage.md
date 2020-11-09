---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284652"
---
# <span data-ttu-id="665df-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="665df-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="665df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="665df-102">SYNOPSIS</span></span>
<span data-ttu-id="665df-103">取得訂閱的使用量配額。</span><span class="sxs-lookup"><span data-stu-id="665df-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="665df-104">句法</span><span class="sxs-lookup"><span data-stu-id="665df-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="665df-105">說明</span><span class="sxs-lookup"><span data-stu-id="665df-105">DESCRIPTION</span></span>
<span data-ttu-id="665df-106">取得訂閱的使用量配額。</span><span class="sxs-lookup"><span data-stu-id="665df-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="665df-107">示例</span><span class="sxs-lookup"><span data-stu-id="665df-107">EXAMPLES</span></span>

### <span data-ttu-id="665df-108">透過輸入位置來取得使用量配額</span><span class="sxs-lookup"><span data-stu-id="665df-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="665df-109">參數</span><span class="sxs-lookup"><span data-stu-id="665df-109">PARAMETERS</span></span>

### <span data-ttu-id="665df-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="665df-110">-DefaultProfile</span></span>
<span data-ttu-id="665df-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="665df-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="665df-112">-位置</span><span class="sxs-lookup"><span data-stu-id="665df-112">-Location</span></span>
<span data-ttu-id="665df-113">SignalR 服務位置。</span><span class="sxs-lookup"><span data-stu-id="665df-113">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="665df-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="665df-114">CommonParameters</span></span>
<span data-ttu-id="665df-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="665df-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="665df-116">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="665df-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="665df-117">輸入</span><span class="sxs-lookup"><span data-stu-id="665df-117">INPUTS</span></span>

### <span data-ttu-id="665df-118">所有</span><span class="sxs-lookup"><span data-stu-id="665df-118">None</span></span>

## <span data-ttu-id="665df-119">輸出</span><span class="sxs-lookup"><span data-stu-id="665df-119">OUTPUTS</span></span>

### <span data-ttu-id="665df-120">PSSignalRUsage 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="665df-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="665df-121">筆記</span><span class="sxs-lookup"><span data-stu-id="665df-121">NOTES</span></span>

## <span data-ttu-id="665df-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="665df-122">RELATED LINKS</span></span>