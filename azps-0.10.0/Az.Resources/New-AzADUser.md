---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: f7127b97790736e69dd138b861b5239a907ab4e7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795283"
---
# <span data-ttu-id="9dbe1-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="9dbe1-101">New-AzADUser</span></span>

## <span data-ttu-id="9dbe1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9dbe1-102">SYNOPSIS</span></span>
<span data-ttu-id="9dbe1-103">建立新的 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="9dbe1-104">句法</span><span class="sxs-lookup"><span data-stu-id="9dbe1-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-MailNickname <String>] [-ForceChangePasswordNextLogin]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dbe1-105">說明</span><span class="sxs-lookup"><span data-stu-id="9dbe1-105">DESCRIPTION</span></span>
<span data-ttu-id="9dbe1-106">建立新的 active directory 使用者 (公司/學校帳戶也會 popularly 稱為組織識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="9dbe1-107">如需詳細資訊： https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="9dbe1-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="9dbe1-108">示例</span><span class="sxs-lookup"><span data-stu-id="9dbe1-108">EXAMPLES</span></span>

### <span data-ttu-id="9dbe1-109">範例 1-建立新的廣告使用者</span><span class="sxs-lookup"><span data-stu-id="9dbe1-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="9dbe1-110">在租使用者中建立名為 "MyDisplayName" 和使用者主體名稱 "" 的新 AD 使用者 myemail@domain.com 。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="9dbe1-111">參數</span><span class="sxs-lookup"><span data-stu-id="9dbe1-111">PARAMETERS</span></span>

### <span data-ttu-id="9dbe1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dbe1-112">-DefaultProfile</span></span>
<span data-ttu-id="9dbe1-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9dbe1-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dbe1-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9dbe1-114">-DisplayName</span></span>
<span data-ttu-id="9dbe1-115">要顯示在使用者通訊錄中的名稱。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="9dbe1-116">範例「立民 Wu」。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="9dbe1-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="9dbe1-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="9dbe1-118">如果使用者必須在下一次成功的登入 (true) 時變更密碼，則必須指定它。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="9dbe1-119">預設行為是 (false) ，不會在下一次成功的登入時變更密碼。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="9dbe1-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="9dbe1-120">-ImmutableId</span></span>
<span data-ttu-id="9dbe1-121">只有在您針對使用者的使用者主要名稱 (upn) 屬性中使用聯盟網域時，才需要指定它。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="9dbe1-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="9dbe1-122">-MailNickname</span></span>
<span data-ttu-id="9dbe1-123">使用者的 [郵件別名]。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="9dbe1-124">-Password</span><span class="sxs-lookup"><span data-stu-id="9dbe1-124">-Password</span></span>
<span data-ttu-id="9dbe1-125">使用者的密碼。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-125">Password for the user.</span></span>
<span data-ttu-id="9dbe1-126">它必須符合租使用者的密碼複雜性需求。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="9dbe1-127">建議設定強式密碼。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-127">It is recommended to set a strong password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dbe1-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9dbe1-128">-UserPrincipalName</span></span>
<span data-ttu-id="9dbe1-129">使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-129">The user principal name.</span></span>
<span data-ttu-id="9dbe1-130">範例-" someuser@contoso.com "。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="9dbe1-131">-確認</span><span class="sxs-lookup"><span data-stu-id="9dbe1-131">-Confirm</span></span>
<span data-ttu-id="9dbe1-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dbe1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dbe1-133">-WhatIf</span></span>
<span data-ttu-id="9dbe1-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dbe1-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dbe1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dbe1-136">CommonParameters</span></span>
<span data-ttu-id="9dbe1-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dbe1-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9dbe1-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dbe1-139">輸入</span><span class="sxs-lookup"><span data-stu-id="9dbe1-139">INPUTS</span></span>

### <span data-ttu-id="9dbe1-140">System.object</span><span class="sxs-lookup"><span data-stu-id="9dbe1-140">System.String</span></span>

### <span data-ttu-id="9dbe1-141">SecureString</span><span class="sxs-lookup"><span data-stu-id="9dbe1-141">System.Security.SecureString</span></span>

### <span data-ttu-id="9dbe1-142">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="9dbe1-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9dbe1-143">輸出</span><span class="sxs-lookup"><span data-stu-id="9dbe1-143">OUTPUTS</span></span>

### <span data-ttu-id="9dbe1-144">Microsoft.Azure.Graph.RBAC.Version1_6 PSADUser</span><span class="sxs-lookup"><span data-stu-id="9dbe1-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="9dbe1-145">筆記</span><span class="sxs-lookup"><span data-stu-id="9dbe1-145">NOTES</span></span>

## <span data-ttu-id="9dbe1-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="9dbe1-146">RELATED LINKS</span></span>

[<span data-ttu-id="9dbe1-147">AzADUser</span><span class="sxs-lookup"><span data-stu-id="9dbe1-147">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="9dbe1-148">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="9dbe1-148">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="9dbe1-149">移除-AzADUser</span><span class="sxs-lookup"><span data-stu-id="9dbe1-149">Remove-AzADUser</span></span>](./Remove-AzADUser.md)