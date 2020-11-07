---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: a6d1ff6d169fab90fa866e94577ce9b3f9580a4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786842"
---
# <span data-ttu-id="0510c-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0510c-101">Get-AzMediaService</span></span>

## <span data-ttu-id="0510c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0510c-102">SYNOPSIS</span></span>
<span data-ttu-id="0510c-103">取得媒體服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0510c-103">Gets information about a media service.</span></span>

## <span data-ttu-id="0510c-104">句法</span><span class="sxs-lookup"><span data-stu-id="0510c-104">SYNTAX</span></span>

### <span data-ttu-id="0510c-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0510c-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0510c-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0510c-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0510c-107">說明</span><span class="sxs-lookup"><span data-stu-id="0510c-107">DESCRIPTION</span></span>
<span data-ttu-id="0510c-108">**AzMediaService** Cmdlet 會取得媒體服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0510c-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="0510c-109">示例</span><span class="sxs-lookup"><span data-stu-id="0510c-109">EXAMPLES</span></span>

### <span data-ttu-id="0510c-110">範例1：取得資源群組中的所有媒體服務</span><span class="sxs-lookup"><span data-stu-id="0510c-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="0510c-111">這個命令會取得名為 ResourceGroup001 之資源群組中所有媒體服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="0510c-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="0510c-112">範例2：取得媒體服務屬性</span><span class="sxs-lookup"><span data-stu-id="0510c-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="0510c-113">這個命令會取得屬於名為 ResourceGroup002 之資源群組之名為 MediaService1 的媒體服務屬性。</span><span class="sxs-lookup"><span data-stu-id="0510c-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="0510c-114">參數</span><span class="sxs-lookup"><span data-stu-id="0510c-114">PARAMETERS</span></span>

### <span data-ttu-id="0510c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0510c-115">-AccountName</span></span>
<span data-ttu-id="0510c-116">指定此 Cmdlet 取得的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="0510c-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0510c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0510c-117">-DefaultProfile</span></span>
<span data-ttu-id="0510c-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0510c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0510c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0510c-119">-ResourceGroupName</span></span>
<span data-ttu-id="0510c-120">指定包含媒體服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0510c-120">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0510c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0510c-121">CommonParameters</span></span>
<span data-ttu-id="0510c-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0510c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0510c-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0510c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0510c-124">輸入</span><span class="sxs-lookup"><span data-stu-id="0510c-124">INPUTS</span></span>

### <span data-ttu-id="0510c-125">System.object</span><span class="sxs-lookup"><span data-stu-id="0510c-125">System.String</span></span>

## <span data-ttu-id="0510c-126">輸出</span><span class="sxs-lookup"><span data-stu-id="0510c-126">OUTPUTS</span></span>

### <span data-ttu-id="0510c-127">PSMediaService 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0510c-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="0510c-128">筆記</span><span class="sxs-lookup"><span data-stu-id="0510c-128">NOTES</span></span>

## <span data-ttu-id="0510c-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="0510c-129">RELATED LINKS</span></span>

[<span data-ttu-id="0510c-130">新-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0510c-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="0510c-131">移除-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0510c-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="0510c-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0510c-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)

