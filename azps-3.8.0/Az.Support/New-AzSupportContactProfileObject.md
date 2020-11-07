---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797978"
---
# <span data-ttu-id="89a8f-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="89a8f-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="89a8f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="89a8f-103">建立支援連絡人設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="89a8f-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="89a8f-104">句法</span><span class="sxs-lookup"><span data-stu-id="89a8f-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89a8f-105">說明</span><span class="sxs-lookup"><span data-stu-id="89a8f-105">DESCRIPTION</span></span>
<span data-ttu-id="89a8f-106">這是協助程式 Cmdlet，您可以用來在建立或更新支援票證時建立支援連絡人設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="89a8f-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="89a8f-107">您必須指定下列參數，才能建立支援票證：</span><span class="sxs-lookup"><span data-stu-id="89a8f-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="89a8f-108">示例</span><span class="sxs-lookup"><span data-stu-id="89a8f-108">EXAMPLES</span></span>

### <span data-ttu-id="89a8f-109">範例1：建立連絡人物件</span><span class="sxs-lookup"><span data-stu-id="89a8f-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="89a8f-110">參數</span><span class="sxs-lookup"><span data-stu-id="89a8f-110">PARAMETERS</span></span>

### <span data-ttu-id="89a8f-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="89a8f-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="89a8f-112">此處列出的電子郵件地址將會在有關支援票證的任何函件上複製。</span><span class="sxs-lookup"><span data-stu-id="89a8f-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a8f-113">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="89a8f-113">-Country</span></span>
<span data-ttu-id="89a8f-114">客戶國家/地區。</span><span class="sxs-lookup"><span data-stu-id="89a8f-114">Customer country.</span></span>
<span data-ttu-id="89a8f-115">這必須是合法的 ISO Alpha-3 國家/地區代碼 (ISO 3166) 。</span><span class="sxs-lookup"><span data-stu-id="89a8f-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="89a8f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89a8f-116">-DefaultProfile</span></span>
<span data-ttu-id="89a8f-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="89a8f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89a8f-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="89a8f-118">-FirstName</span></span>
<span data-ttu-id="89a8f-119">客戶名字。</span><span class="sxs-lookup"><span data-stu-id="89a8f-119">Customer first name.</span></span>

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

### <span data-ttu-id="89a8f-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="89a8f-120">-LastName</span></span>
<span data-ttu-id="89a8f-121">客戶姓氏。</span><span class="sxs-lookup"><span data-stu-id="89a8f-121">Customer last name.</span></span>

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

### <span data-ttu-id="89a8f-122">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="89a8f-122">-PhoneNumber</span></span>
<span data-ttu-id="89a8f-123">客戶電話號碼。</span><span class="sxs-lookup"><span data-stu-id="89a8f-123">Customer phone number.</span></span>
<span data-ttu-id="89a8f-124">如果您喜歡的連絡方式是手機，則需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="89a8f-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="89a8f-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="89a8f-125">-PreferredContactMethod</span></span>
<span data-ttu-id="89a8f-126">[首選連絡方式] 方法。</span><span class="sxs-lookup"><span data-stu-id="89a8f-126">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: (All)
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a8f-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="89a8f-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="89a8f-128">客戶慣用的支援語言。</span><span class="sxs-lookup"><span data-stu-id="89a8f-128">Customer preferred support language.</span></span>
<span data-ttu-id="89a8f-129">這必須是有效的語言 contry 程式碼，適用于此處所列的其中一個支援的語言 https://azure.microsoft.com/support/faq/ 。</span><span class="sxs-lookup"><span data-stu-id="89a8f-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="89a8f-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="89a8f-130">-PreferredTimeZone</span></span>
<span data-ttu-id="89a8f-131">客戶慣用時區。</span><span class="sxs-lookup"><span data-stu-id="89a8f-131">Customer preferred time zone.</span></span>
<span data-ttu-id="89a8f-132">這必須是有效的 System.TimeZoneInfo.Id 值。</span><span class="sxs-lookup"><span data-stu-id="89a8f-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="89a8f-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="89a8f-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="89a8f-134">客戶主要電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="89a8f-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="89a8f-135">-確認</span><span class="sxs-lookup"><span data-stu-id="89a8f-135">-Confirm</span></span>
<span data-ttu-id="89a8f-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="89a8f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89a8f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89a8f-137">-WhatIf</span></span>
<span data-ttu-id="89a8f-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="89a8f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89a8f-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89a8f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89a8f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89a8f-140">CommonParameters</span></span>
<span data-ttu-id="89a8f-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89a8f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89a8f-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="89a8f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89a8f-143">輸入</span><span class="sxs-lookup"><span data-stu-id="89a8f-143">INPUTS</span></span>

### <span data-ttu-id="89a8f-144">所有</span><span class="sxs-lookup"><span data-stu-id="89a8f-144">None</span></span>

## <span data-ttu-id="89a8f-145">輸出</span><span class="sxs-lookup"><span data-stu-id="89a8f-145">OUTPUTS</span></span>

### <span data-ttu-id="89a8f-146">PSContactProfile （支援）。</span><span class="sxs-lookup"><span data-stu-id="89a8f-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="89a8f-147">筆記</span><span class="sxs-lookup"><span data-stu-id="89a8f-147">NOTES</span></span>

## <span data-ttu-id="89a8f-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="89a8f-148">RELATED LINKS</span></span>