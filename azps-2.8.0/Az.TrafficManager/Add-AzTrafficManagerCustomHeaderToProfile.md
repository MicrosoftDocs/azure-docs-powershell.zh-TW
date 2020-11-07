---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: 4479cad8117c078c3d863b58cd764a388f78cd28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792024"
---
# <span data-ttu-id="8a850-101">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="8a850-101">Add-AzTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="8a850-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a850-102">SYNOPSIS</span></span>
<span data-ttu-id="8a850-103">將自訂標頭資訊新增到本機流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="8a850-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="8a850-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a850-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a850-105">說明</span><span class="sxs-lookup"><span data-stu-id="8a850-105">DESCRIPTION</span></span>
<span data-ttu-id="8a850-106">**載入 AzTrafficManagerCustomHeaderToProfile** Cmdlet 會將自訂標頭資訊新增到本機 Azure 流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="8a850-106">The **Add-AzTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="8a850-107">您可以使用 New-AzTrafficManagerProfile 或 Get-AzTrafficManagerProfile Cmdlet 來取得設定檔。</span><span class="sxs-lookup"><span data-stu-id="8a850-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="8a850-108">這個 Cmdlet 作用於本機設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="8a850-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="8a850-109">使用 Set-AzTrafficManagerProfile Cmdlet，將您的變更提交至流量管理器的設定檔。</span><span class="sxs-lookup"><span data-stu-id="8a850-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="8a850-110">示例</span><span class="sxs-lookup"><span data-stu-id="8a850-110">EXAMPLES</span></span>

### <span data-ttu-id="8a850-111">範例1：在設定檔中新增自訂標頭資訊</span><span class="sxs-lookup"><span data-stu-id="8a850-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="8a850-112">第一個命令會使用 **AzTrafficManagerProfile** Cmdlet 取得 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="8a850-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="8a850-113">該命令會將本機設定檔儲存在 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="8a850-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="8a850-114">第二個命令會將自訂標頭資訊新增至儲存在 $TrafficManagerProfile 中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="8a850-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="8a850-115">最後一個命令會更新流量管理器中的設定檔，以符合 $TrafficManagerProfile 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="8a850-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="8a850-116">參數</span><span class="sxs-lookup"><span data-stu-id="8a850-116">PARAMETERS</span></span>

### <span data-ttu-id="8a850-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a850-117">-DefaultProfile</span></span>
<span data-ttu-id="8a850-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a850-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a850-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="8a850-119">-Name</span></span>
<span data-ttu-id="8a850-120">指定要新增之自訂標頭資訊的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a850-120">Specifies the name of the custom header information to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a850-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8a850-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="8a850-122">指定本機 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="8a850-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="8a850-123">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="8a850-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="8a850-124">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a850-124">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a850-125">-值</span><span class="sxs-lookup"><span data-stu-id="8a850-125">-Value</span></span>
<span data-ttu-id="8a850-126">指定要新增之自訂標頭資訊的值。</span><span class="sxs-lookup"><span data-stu-id="8a850-126">Specifies the value of the custom header information to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a850-127">-確認</span><span class="sxs-lookup"><span data-stu-id="8a850-127">-Confirm</span></span>
<span data-ttu-id="8a850-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8a850-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a850-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a850-129">-WhatIf</span></span>
<span data-ttu-id="8a850-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8a850-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a850-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a850-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a850-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a850-132">CommonParameters</span></span>
<span data-ttu-id="8a850-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a850-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a850-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8a850-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a850-135">輸入</span><span class="sxs-lookup"><span data-stu-id="8a850-135">INPUTS</span></span>

### <span data-ttu-id="8a850-136">TrafficManagerProfile 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="8a850-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="8a850-137">輸出</span><span class="sxs-lookup"><span data-stu-id="8a850-137">OUTPUTS</span></span>

### <span data-ttu-id="8a850-138">TrafficManagerProfile 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="8a850-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="8a850-139">筆記</span><span class="sxs-lookup"><span data-stu-id="8a850-139">NOTES</span></span>

## <span data-ttu-id="8a850-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a850-140">RELATED LINKS</span></span>

[<span data-ttu-id="8a850-141">移除-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="8a850-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="8a850-142">AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8a850-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="8a850-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8a850-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)