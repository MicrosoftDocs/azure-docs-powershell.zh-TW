---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: c3459a07eb6f92e4ec30b5018efc41ff13e1c41e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801886"
---
# <span data-ttu-id="d6f16-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d6f16-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="d6f16-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d6f16-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f16-103">註冊資源提供者。</span><span class="sxs-lookup"><span data-stu-id="d6f16-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6f16-104">句法</span><span class="sxs-lookup"><span data-stu-id="d6f16-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6f16-105">說明</span><span class="sxs-lookup"><span data-stu-id="d6f16-105">DESCRIPTION</span></span>
<span data-ttu-id="d6f16-106">**AzureRmResourceProvider** Cmdlet 會註冊 Azure 資源提供者。</span><span class="sxs-lookup"><span data-stu-id="d6f16-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="d6f16-107">示例</span><span class="sxs-lookup"><span data-stu-id="d6f16-107">EXAMPLES</span></span>

### <span data-ttu-id="d6f16-108">範例1：註冊提供者</span><span class="sxs-lookup"><span data-stu-id="d6f16-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzureRmResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="d6f16-109">這會為您的帳戶註冊 Microsoft. 網路提供者。</span><span class="sxs-lookup"><span data-stu-id="d6f16-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="d6f16-110">參數</span><span class="sxs-lookup"><span data-stu-id="d6f16-110">PARAMETERS</span></span>

### <span data-ttu-id="d6f16-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d6f16-111">-ApiVersion</span></span>
<span data-ttu-id="d6f16-112">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="d6f16-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d6f16-113">您可以指定不同于預設版本的版本。</span><span class="sxs-lookup"><span data-stu-id="d6f16-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f16-114">-DefaultProfile</span></span>
<span data-ttu-id="d6f16-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d6f16-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6f16-116">-預先</span><span class="sxs-lookup"><span data-stu-id="d6f16-116">-Pre</span></span>
<span data-ttu-id="d6f16-117">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="d6f16-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f16-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="d6f16-118">-ProviderNamespace</span></span>
<span data-ttu-id="d6f16-119">指定資源提供者的命名空間。</span><span class="sxs-lookup"><span data-stu-id="d6f16-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="d6f16-120">-確認</span><span class="sxs-lookup"><span data-stu-id="d6f16-120">-Confirm</span></span>
<span data-ttu-id="d6f16-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d6f16-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6f16-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f16-122">-WhatIf</span></span>
<span data-ttu-id="d6f16-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6f16-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6f16-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6f16-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6f16-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f16-125">CommonParameters</span></span>
<span data-ttu-id="d6f16-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d6f16-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f16-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d6f16-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f16-128">輸入</span><span class="sxs-lookup"><span data-stu-id="d6f16-128">INPUTS</span></span>

## <span data-ttu-id="d6f16-129">輸出</span><span class="sxs-lookup"><span data-stu-id="d6f16-129">OUTPUTS</span></span>

## <span data-ttu-id="d6f16-130">筆記</span><span class="sxs-lookup"><span data-stu-id="d6f16-130">NOTES</span></span>

## <span data-ttu-id="d6f16-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6f16-131">RELATED LINKS</span></span>

[<span data-ttu-id="d6f16-132">AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d6f16-132">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="d6f16-133">取消註冊-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d6f16-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)

