---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 6e8ba9fb6fb65980113ae8093bc4e3c258861968
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958784"
---
# <span data-ttu-id="f8bc1-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="f8bc1-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="f8bc1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="f8bc1-103">將內容載入到端點。</span><span class="sxs-lookup"><span data-stu-id="f8bc1-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="f8bc1-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8bc1-104">SYNTAX</span></span>

### <span data-ttu-id="f8bc1-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f8bc1-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8bc1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8bc1-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8bc1-107">說明</span><span class="sxs-lookup"><span data-stu-id="f8bc1-107">DESCRIPTION</span></span>
<span data-ttu-id="f8bc1-108">**AzCdnEndpointContent** Cmdlet 會從來源伺服器載入 Azure 內容傳遞網路 (CDN) 端點的內容。</span><span class="sxs-lookup"><span data-stu-id="f8bc1-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="f8bc1-109">示例</span><span class="sxs-lookup"><span data-stu-id="f8bc1-109">EXAMPLES</span></span>

## <span data-ttu-id="f8bc1-110">參數</span><span class="sxs-lookup"><span data-stu-id="f8bc1-110">PARAMETERS</span></span>

### <span data-ttu-id="f8bc1-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8bc1-111">-CdnEndpoint</span></span>
<span data-ttu-id="f8bc1-112">指定 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="f8bc1-112">Specifies the CDN endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8bc1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8bc1-113">-DefaultProfile</span></span>
<span data-ttu-id="f8bc1-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f8bc1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8bc1-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="f8bc1-115">-EndpointName</span></span>
<span data-ttu-id="f8bc1-116">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8bc1-116">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8bc1-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="f8bc1-117">-LoadContent</span></span>
<span data-ttu-id="f8bc1-118">指定此 Cmdlet 發佈之原始伺服器內容的相對路徑陣列。</span><span class="sxs-lookup"><span data-stu-id="f8bc1-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8bc1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8bc1-119">-PassThru</span></span>
<span data-ttu-id="f8bc1-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="f8bc1-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f8bc1-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f8bc1-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f8bc1-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f8bc1-122">-ProfileName</span></span>
<span data-ttu-id="f8bc1-123">指定原始伺服器所屬之設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8bc1-123">Specifies the name of the profile to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8bc1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8bc1-124">-ResourceGroupName</span></span>
<span data-ttu-id="f8bc1-125">指定原始伺服器所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8bc1-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8bc1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8bc1-126">CommonParameters</span></span>
<span data-ttu-id="f8bc1-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8bc1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8bc1-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f8bc1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8bc1-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f8bc1-129">INPUTS</span></span>

### <span data-ttu-id="f8bc1-130">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="f8bc1-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="f8bc1-131">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f8bc1-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f8bc1-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f8bc1-132">OUTPUTS</span></span>

### <span data-ttu-id="f8bc1-133">System.object</span><span class="sxs-lookup"><span data-stu-id="f8bc1-133">System.Boolean</span></span>

## <span data-ttu-id="f8bc1-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f8bc1-134">NOTES</span></span>

## <span data-ttu-id="f8bc1-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8bc1-135">RELATED LINKS</span></span>

[<span data-ttu-id="f8bc1-136">取消發佈-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="f8bc1-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)

