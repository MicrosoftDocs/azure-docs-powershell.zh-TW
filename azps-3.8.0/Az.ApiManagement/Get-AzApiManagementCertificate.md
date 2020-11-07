---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 9826de76a65fe097d2daba106bd74df5e94a730e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957878"
---
# <span data-ttu-id="e633b-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e633b-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="e633b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e633b-102">SYNOPSIS</span></span>
<span data-ttu-id="e633b-103">取得在服務中後端驗證所設定的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="e633b-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="e633b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e633b-104">SYNTAX</span></span>

### <span data-ttu-id="e633b-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e633b-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e633b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e633b-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e633b-107">說明</span><span class="sxs-lookup"><span data-stu-id="e633b-107">DESCRIPTION</span></span>
<span data-ttu-id="e633b-108">**AzApiManagementCertificate** Cmdlet 會取得您指定的所有 Azure API 管理憑證或憑證。</span><span class="sxs-lookup"><span data-stu-id="e633b-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="e633b-109">示例</span><span class="sxs-lookup"><span data-stu-id="e633b-109">EXAMPLES</span></span>

### <span data-ttu-id="e633b-110">範例1：取得所有憑證</span><span class="sxs-lookup"><span data-stu-id="e633b-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="e633b-111">這個命令會取得所有 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="e633b-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="e633b-112">範例2：根據其識別碼取得憑證</span><span class="sxs-lookup"><span data-stu-id="e633b-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="e633b-113">這個命令會取得具有指定識別碼的 API 管理憑證。</span><span class="sxs-lookup"><span data-stu-id="e633b-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="e633b-114">參數</span><span class="sxs-lookup"><span data-stu-id="e633b-114">PARAMETERS</span></span>

### <span data-ttu-id="e633b-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="e633b-115">-CertificateId</span></span>
<span data-ttu-id="e633b-116">指定要取得的憑證識別碼。</span><span class="sxs-lookup"><span data-stu-id="e633b-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e633b-117">-內容</span><span class="sxs-lookup"><span data-stu-id="e633b-117">-Context</span></span>
<span data-ttu-id="e633b-118">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="e633b-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e633b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e633b-119">-DefaultProfile</span></span>
<span data-ttu-id="e633b-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e633b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e633b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e633b-121">-ResourceId</span></span>
<span data-ttu-id="e633b-122">憑證的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e633b-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="e633b-123">如果已指定，將會嘗試依據識別碼尋找憑證。</span><span class="sxs-lookup"><span data-stu-id="e633b-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="e633b-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="e633b-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e633b-125">-確認</span><span class="sxs-lookup"><span data-stu-id="e633b-125">-Confirm</span></span>
<span data-ttu-id="e633b-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e633b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e633b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e633b-127">-WhatIf</span></span>
<span data-ttu-id="e633b-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e633b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e633b-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e633b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e633b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e633b-130">CommonParameters</span></span>
<span data-ttu-id="e633b-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e633b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e633b-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e633b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e633b-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e633b-133">INPUTS</span></span>

### <span data-ttu-id="e633b-134">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e633b-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e633b-135">System.object</span><span class="sxs-lookup"><span data-stu-id="e633b-135">System.String</span></span>

## <span data-ttu-id="e633b-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e633b-136">OUTPUTS</span></span>

### <span data-ttu-id="e633b-137">ServiceManagement. PsApiManagementCertificate （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e633b-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="e633b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e633b-138">NOTES</span></span>

## <span data-ttu-id="e633b-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e633b-139">RELATED LINKS</span></span>

[<span data-ttu-id="e633b-140">新-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e633b-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="e633b-141">移除-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e633b-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="e633b-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e633b-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)

