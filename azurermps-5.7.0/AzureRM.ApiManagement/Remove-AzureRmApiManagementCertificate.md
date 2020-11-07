---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
ms.openlocfilehash: a333f3e5263f565a44856a9af43be272cc971a22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623996"
---
# <span data-ttu-id="24373-101">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="24373-101">Remove-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="24373-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24373-102">SYNOPSIS</span></span>
<span data-ttu-id="24373-103">移除 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="24373-103">Removes an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24373-104">句法</span><span class="sxs-lookup"><span data-stu-id="24373-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24373-105">說明</span><span class="sxs-lookup"><span data-stu-id="24373-105">DESCRIPTION</span></span>
<span data-ttu-id="24373-106">**AzureRmApiManagementCertificate** Cmdlet 會移除 Azure API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="24373-106">The **Remove-AzureRmApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="24373-107">示例</span><span class="sxs-lookup"><span data-stu-id="24373-107">EXAMPLES</span></span>

### <span data-ttu-id="24373-108">範例1：移除憑證</span><span class="sxs-lookup"><span data-stu-id="24373-108">Example 1: Remove a certificate</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="24373-109">這個命令會移除指定的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="24373-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="24373-110">由於已指定 *Force* 參數，因此不需要確認。</span><span class="sxs-lookup"><span data-stu-id="24373-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="24373-111">參數</span><span class="sxs-lookup"><span data-stu-id="24373-111">PARAMETERS</span></span>

### <span data-ttu-id="24373-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="24373-112">-CertificateId</span></span>
<span data-ttu-id="24373-113">指定要移除的憑證識別碼。</span><span class="sxs-lookup"><span data-stu-id="24373-113">Specifies the ID of the certificate to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24373-114">-內容</span><span class="sxs-lookup"><span data-stu-id="24373-114">-Context</span></span>
<span data-ttu-id="24373-115">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="24373-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24373-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24373-116">-DefaultProfile</span></span>
<span data-ttu-id="24373-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24373-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24373-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24373-118">-PassThru</span></span>
<span data-ttu-id="24373-119">passthru</span><span class="sxs-lookup"><span data-stu-id="24373-119">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24373-120">-確認</span><span class="sxs-lookup"><span data-stu-id="24373-120">-Confirm</span></span>
<span data-ttu-id="24373-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24373-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24373-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24373-122">-WhatIf</span></span>
<span data-ttu-id="24373-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24373-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24373-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24373-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24373-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24373-125">CommonParameters</span></span>
<span data-ttu-id="24373-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24373-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24373-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24373-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24373-128">輸入</span><span class="sxs-lookup"><span data-stu-id="24373-128">INPUTS</span></span>

### <span data-ttu-id="24373-129">所有</span><span class="sxs-lookup"><span data-stu-id="24373-129">None</span></span>
<span data-ttu-id="24373-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="24373-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24373-131">輸出</span><span class="sxs-lookup"><span data-stu-id="24373-131">OUTPUTS</span></span>

### <span data-ttu-id="24373-132">布林值</span><span class="sxs-lookup"><span data-stu-id="24373-132">Boolean</span></span>

## <span data-ttu-id="24373-133">筆記</span><span class="sxs-lookup"><span data-stu-id="24373-133">NOTES</span></span>

## <span data-ttu-id="24373-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="24373-134">RELATED LINKS</span></span>

[<span data-ttu-id="24373-135">AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="24373-135">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="24373-136">新-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="24373-136">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="24373-137">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="24373-137">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)

