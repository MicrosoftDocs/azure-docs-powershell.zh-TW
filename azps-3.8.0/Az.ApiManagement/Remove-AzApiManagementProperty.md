---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
ms.openlocfilehash: 41ce5ae67bbc3b21b29740cde1503e474ebe9f8a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958081"
---
# <span data-ttu-id="418ca-101">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="418ca-101">Remove-AzApiManagementProperty</span></span>

## <span data-ttu-id="418ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="418ca-102">SYNOPSIS</span></span>
<span data-ttu-id="418ca-103">移除 API 管理屬性。</span><span class="sxs-lookup"><span data-stu-id="418ca-103">Removes an API Management Property.</span></span>

## <span data-ttu-id="418ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="418ca-104">SYNTAX</span></span>

```
Remove-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="418ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="418ca-105">DESCRIPTION</span></span>
<span data-ttu-id="418ca-106">**AzApiManagementProperty** Cmdlet 會移除 Azure API 管理 **屬性** 。</span><span class="sxs-lookup"><span data-stu-id="418ca-106">The **Remove-AzApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="418ca-107">示例</span><span class="sxs-lookup"><span data-stu-id="418ca-107">EXAMPLES</span></span>

### <span data-ttu-id="418ca-108">範例1：移除屬性</span><span class="sxs-lookup"><span data-stu-id="418ca-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="418ca-109">這個命令會移除 ID 為 Property11 的屬性。</span><span class="sxs-lookup"><span data-stu-id="418ca-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="418ca-110">參數</span><span class="sxs-lookup"><span data-stu-id="418ca-110">PARAMETERS</span></span>

### <span data-ttu-id="418ca-111">-內容</span><span class="sxs-lookup"><span data-stu-id="418ca-111">-Context</span></span>
<span data-ttu-id="418ca-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="418ca-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="418ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="418ca-113">-DefaultProfile</span></span>
<span data-ttu-id="418ca-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="418ca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="418ca-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="418ca-115">-PassThru</span></span>
<span data-ttu-id="418ca-116">指示這個 Cmdlet 會傳回 $True 的值（如果操作成功或 $False 則不然）。</span><span class="sxs-lookup"><span data-stu-id="418ca-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="418ca-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="418ca-117">-PropertyId</span></span>
<span data-ttu-id="418ca-118">指定此 Cmdlet 移除之屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="418ca-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="418ca-119">-確認</span><span class="sxs-lookup"><span data-stu-id="418ca-119">-Confirm</span></span>
<span data-ttu-id="418ca-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="418ca-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="418ca-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="418ca-121">-WhatIf</span></span>
<span data-ttu-id="418ca-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="418ca-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="418ca-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="418ca-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="418ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418ca-124">CommonParameters</span></span>
<span data-ttu-id="418ca-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="418ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418ca-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="418ca-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418ca-127">輸入</span><span class="sxs-lookup"><span data-stu-id="418ca-127">INPUTS</span></span>

### <span data-ttu-id="418ca-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="418ca-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="418ca-129">System.object</span><span class="sxs-lookup"><span data-stu-id="418ca-129">System.String</span></span>

### <span data-ttu-id="418ca-130">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="418ca-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="418ca-131">輸出</span><span class="sxs-lookup"><span data-stu-id="418ca-131">OUTPUTS</span></span>

### <span data-ttu-id="418ca-132">System.object</span><span class="sxs-lookup"><span data-stu-id="418ca-132">System.Boolean</span></span>

## <span data-ttu-id="418ca-133">筆記</span><span class="sxs-lookup"><span data-stu-id="418ca-133">NOTES</span></span>

## <span data-ttu-id="418ca-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="418ca-134">RELATED LINKS</span></span>

[<span data-ttu-id="418ca-135">新-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="418ca-135">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="418ca-136">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="418ca-136">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)

