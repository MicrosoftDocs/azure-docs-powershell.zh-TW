---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
ms.openlocfilehash: 1274b04ed85917a9c1e185bfbef6307eaedecc05
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801150"
---
# <span data-ttu-id="c795f-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="c795f-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="c795f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c795f-102">SYNOPSIS</span></span>
<span data-ttu-id="c795f-103">取得使用 Azure RBAC 安全的 Azure 資源提供者的作業。</span><span class="sxs-lookup"><span data-stu-id="c795f-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c795f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c795f-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c795f-105">說明</span><span class="sxs-lookup"><span data-stu-id="c795f-105">DESCRIPTION</span></span>
<span data-ttu-id="c795f-106">Get-AzureRmProviderOperation 會取得 Azure 資源提供者所公開的操作。</span><span class="sxs-lookup"><span data-stu-id="c795f-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="c795f-107">您可以撰寫作業來建立 Azure RBAC 中的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="c795f-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="c795f-108">此命令會以輸入操作的方式來執行作業搜尋字串 (有可能的萬用字元 ( *) 字元 (s) # A5，從而決定要顯示的操作詳細資料。使用 Get-AzureRmProviderOperation \* 來取得所有 Azure 資源提供者的所有作業。使用 Get-AzureRmProviderOperation 的 Microsoft. 計算/* 取得所有 microsoft 的操作。計算資源提供者。</span><span class="sxs-lookup"><span data-stu-id="c795f-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzureRmProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="c795f-109">示例</span><span class="sxs-lookup"><span data-stu-id="c795f-109">EXAMPLES</span></span>

### <span data-ttu-id="c795f-110">取得所有提供者的所有動作</span><span class="sxs-lookup"><span data-stu-id="c795f-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="c795f-111">針對特定資源提供者取得動作</span><span class="sxs-lookup"><span data-stu-id="c795f-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="c795f-112">取得可在虛擬機器上執行的所有動作</span><span class="sxs-lookup"><span data-stu-id="c795f-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="c795f-113">參數</span><span class="sxs-lookup"><span data-stu-id="c795f-113">PARAMETERS</span></span>

### <span data-ttu-id="c795f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c795f-114">-DefaultProfile</span></span>
<span data-ttu-id="c795f-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c795f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c795f-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="c795f-116">-OperationSearchString</span></span>
<span data-ttu-id="c795f-117">使用可能的萬用字元 ( \* ) 字元 (的操作搜尋字串) </span><span class="sxs-lookup"><span data-stu-id="c795f-117">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c795f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c795f-118">CommonParameters</span></span>
<span data-ttu-id="c795f-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c795f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c795f-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c795f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c795f-121">輸入</span><span class="sxs-lookup"><span data-stu-id="c795f-121">INPUTS</span></span>

### <span data-ttu-id="c795f-122">System.object</span><span class="sxs-lookup"><span data-stu-id="c795f-122">System.String</span></span>
<span data-ttu-id="c795f-123">參數： OperationSearchString (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c795f-123">Parameters: OperationSearchString (ByValue)</span></span>

## <span data-ttu-id="c795f-124">輸出</span><span class="sxs-lookup"><span data-stu-id="c795f-124">OUTPUTS</span></span>

### <span data-ttu-id="c795f-125">PSResourceProviderOperation 中的 .Resources。</span><span class="sxs-lookup"><span data-stu-id="c795f-125">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="c795f-126">筆記</span><span class="sxs-lookup"><span data-stu-id="c795f-126">NOTES</span></span>
<span data-ttu-id="c795f-127">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="c795f-127">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c795f-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="c795f-128">RELATED LINKS</span></span>