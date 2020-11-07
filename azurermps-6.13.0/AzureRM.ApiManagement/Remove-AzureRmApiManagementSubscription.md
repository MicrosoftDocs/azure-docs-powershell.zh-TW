---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 09a0af4685701de60fc85c1572b492e7582ff71e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624952"
---
# <span data-ttu-id="9b376-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9b376-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="9b376-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b376-102">SYNOPSIS</span></span>
<span data-ttu-id="9b376-103">刪除現有的訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b376-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b376-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b376-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b376-105">說明</span><span class="sxs-lookup"><span data-stu-id="9b376-105">DESCRIPTION</span></span>
<span data-ttu-id="9b376-106">AzureRmApiManagementSubscription Cmdlet 會刪除現有 **的** 訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b376-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="9b376-107">示例</span><span class="sxs-lookup"><span data-stu-id="9b376-107">EXAMPLES</span></span>

### <span data-ttu-id="9b376-108">範例1：刪除訂閱</span><span class="sxs-lookup"><span data-stu-id="9b376-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="9b376-109">這個命令會刪除現有的訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b376-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="9b376-110">參數</span><span class="sxs-lookup"><span data-stu-id="9b376-110">PARAMETERS</span></span>

### <span data-ttu-id="9b376-111">-內容</span><span class="sxs-lookup"><span data-stu-id="9b376-111">-Context</span></span>
<span data-ttu-id="9b376-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="9b376-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b376-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b376-113">-DefaultProfile</span></span>
<span data-ttu-id="9b376-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b376-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b376-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b376-115">-PassThru</span></span>
<span data-ttu-id="9b376-116">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $false 的值。</span><span class="sxs-lookup"><span data-stu-id="9b376-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b376-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9b376-117">-SubscriptionId</span></span>
<span data-ttu-id="9b376-118">指定訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="9b376-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="9b376-119">-確認</span><span class="sxs-lookup"><span data-stu-id="9b376-119">-Confirm</span></span>
<span data-ttu-id="9b376-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9b376-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b376-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b376-121">-WhatIf</span></span>
<span data-ttu-id="9b376-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9b376-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b376-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b376-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b376-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b376-124">CommonParameters</span></span>
<span data-ttu-id="9b376-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b376-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b376-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b376-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b376-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9b376-127">INPUTS</span></span>

### <span data-ttu-id="9b376-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9b376-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9b376-129">System.object</span><span class="sxs-lookup"><span data-stu-id="9b376-129">System.String</span></span>

### <span data-ttu-id="9b376-130">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="9b376-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9b376-131">輸出</span><span class="sxs-lookup"><span data-stu-id="9b376-131">OUTPUTS</span></span>

### <span data-ttu-id="9b376-132">System.object</span><span class="sxs-lookup"><span data-stu-id="9b376-132">System.Boolean</span></span>

## <span data-ttu-id="9b376-133">筆記</span><span class="sxs-lookup"><span data-stu-id="9b376-133">NOTES</span></span>

## <span data-ttu-id="9b376-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b376-134">RELATED LINKS</span></span>

[<span data-ttu-id="9b376-135">AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9b376-135">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="9b376-136">新-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9b376-136">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="9b376-137">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9b376-137">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)

