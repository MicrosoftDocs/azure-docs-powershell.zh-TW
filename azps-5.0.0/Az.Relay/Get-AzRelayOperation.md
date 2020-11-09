---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
ms.openlocfilehash: 21bf1e235d9e6b2f6bb4d2017b69f607e559e46b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287343"
---
# <span data-ttu-id="19bf4-101">Get-AzRelayOperation</span><span class="sxs-lookup"><span data-stu-id="19bf4-101">Get-AzRelayOperation</span></span>

## <span data-ttu-id="19bf4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="19bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="19bf4-103">清單支援的中繼作業</span><span class="sxs-lookup"><span data-stu-id="19bf4-103">List supported Relay Operations</span></span>

## <span data-ttu-id="19bf4-104">句法</span><span class="sxs-lookup"><span data-stu-id="19bf4-104">SYNTAX</span></span>

```
Get-AzRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19bf4-105">說明</span><span class="sxs-lookup"><span data-stu-id="19bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="19bf4-106">**AzRelayOperation** Cmdlet 會列出中繼支援的作業。</span><span class="sxs-lookup"><span data-stu-id="19bf4-106">The **Get-AzRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="19bf4-107">示例</span><span class="sxs-lookup"><span data-stu-id="19bf4-107">EXAMPLES</span></span>

### <span data-ttu-id="19bf4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="19bf4-108">Example 1</span></span>
```
PS C:\> Get-AzRelayOperation

Name                                                                            Display
----                                                                            -------
Microsoft.Relay/checkNamespaceAvailability/action                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/register/action                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/write                                                Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/read                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/Delete                                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/write                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/delete                            Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/listkeys/action                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/write                              Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/read                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/Delete                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write           Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete          Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/write                                      Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/read                                       Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/Delete                                     Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete                  Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action         Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
```

<span data-ttu-id="19bf4-109">列出中繼支援的作業</span><span class="sxs-lookup"><span data-stu-id="19bf4-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="19bf4-110">參數</span><span class="sxs-lookup"><span data-stu-id="19bf4-110">PARAMETERS</span></span>

### <span data-ttu-id="19bf4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19bf4-111">-DefaultProfile</span></span>
<span data-ttu-id="19bf4-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="19bf4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19bf4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19bf4-113">CommonParameters</span></span>
<span data-ttu-id="19bf4-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="19bf4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19bf4-115">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="19bf4-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19bf4-116">輸入</span><span class="sxs-lookup"><span data-stu-id="19bf4-116">INPUTS</span></span>

### <span data-ttu-id="19bf4-117">所有</span><span class="sxs-lookup"><span data-stu-id="19bf4-117">None</span></span>

## <span data-ttu-id="19bf4-118">輸出</span><span class="sxs-lookup"><span data-stu-id="19bf4-118">OUTPUTS</span></span>

### <span data-ttu-id="19bf4-119">PSOperationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="19bf4-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="19bf4-120">筆記</span><span class="sxs-lookup"><span data-stu-id="19bf4-120">NOTES</span></span>

## <span data-ttu-id="19bf4-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="19bf4-121">RELATED LINKS</span></span>