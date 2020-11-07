---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bd0483cf03ac5cff224824cc41b3fab994006acb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792243"
---
# <span data-ttu-id="450e5-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="450e5-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="450e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="450e5-102">SYNOPSIS</span></span>
<span data-ttu-id="450e5-103">取得使用 Azure RBAC 安全的 Azure 資源提供者的作業。</span><span class="sxs-lookup"><span data-stu-id="450e5-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="450e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="450e5-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="450e5-105">說明</span><span class="sxs-lookup"><span data-stu-id="450e5-105">DESCRIPTION</span></span>
<span data-ttu-id="450e5-106">Get-AzProviderOperation 會取得 Azure 資源提供者所公開的操作。</span><span class="sxs-lookup"><span data-stu-id="450e5-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="450e5-107">您可以撰寫作業來建立 Azure RBAC 中的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="450e5-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="450e5-108">此命令會以輸入操作的方式來執行作業搜尋字串 (有可能的萬用字元 ( *) 字元 (s) # A5，從而決定要顯示的操作詳細資料。使用 Get-AzProviderOperation \* 來取得所有 Azure 資源提供者的所有作業。使用 Get-AzProviderOperation 的 Microsoft. 計算/* 取得所有 microsoft 的操作。計算資源提供者。</span><span class="sxs-lookup"><span data-stu-id="450e5-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="450e5-109">示例</span><span class="sxs-lookup"><span data-stu-id="450e5-109">EXAMPLES</span></span>

### <span data-ttu-id="450e5-110">取得所有提供者的所有動作</span><span class="sxs-lookup"><span data-stu-id="450e5-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="450e5-111">針對特定資源提供者取得動作</span><span class="sxs-lookup"><span data-stu-id="450e5-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="450e5-112">取得可在虛擬機器上執行的所有動作</span><span class="sxs-lookup"><span data-stu-id="450e5-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="450e5-113">參數</span><span class="sxs-lookup"><span data-stu-id="450e5-113">PARAMETERS</span></span>

### <span data-ttu-id="450e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="450e5-114">-DefaultProfile</span></span>
<span data-ttu-id="450e5-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="450e5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="450e5-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="450e5-116">-OperationSearchString</span></span>
<span data-ttu-id="450e5-117">使用可能的萬用字元 ( \* ) 字元 (的操作搜尋字串) </span><span class="sxs-lookup"><span data-stu-id="450e5-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="450e5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450e5-118">CommonParameters</span></span>
<span data-ttu-id="450e5-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="450e5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450e5-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="450e5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450e5-121">輸入</span><span class="sxs-lookup"><span data-stu-id="450e5-121">INPUTS</span></span>

### <span data-ttu-id="450e5-122">System.object</span><span class="sxs-lookup"><span data-stu-id="450e5-122">System.String</span></span>

## <span data-ttu-id="450e5-123">輸出</span><span class="sxs-lookup"><span data-stu-id="450e5-123">OUTPUTS</span></span>

### <span data-ttu-id="450e5-124">PSResourceProviderOperation 中的 .Resources。</span><span class="sxs-lookup"><span data-stu-id="450e5-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="450e5-125">筆記</span><span class="sxs-lookup"><span data-stu-id="450e5-125">NOTES</span></span>
<span data-ttu-id="450e5-126">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="450e5-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="450e5-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="450e5-127">RELATED LINKS</span></span>