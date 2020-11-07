---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: 3850e5f142e7ec1496ace1225ab53c160794775a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795293"
---
# <span data-ttu-id="3628b-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="3628b-101">New-AzADApplication</span></span>

## <span data-ttu-id="3628b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3628b-102">SYNOPSIS</span></span>
<span data-ttu-id="3628b-103">建立新的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3628b-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="3628b-104">句法</span><span class="sxs-lookup"><span data-stu-id="3628b-104">SYNTAX</span></span>

### <span data-ttu-id="3628b-105">ApplicationWithoutCredentialParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3628b-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3628b-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="3628b-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3628b-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="3628b-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3628b-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="3628b-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3628b-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="3628b-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3628b-110">說明</span><span class="sxs-lookup"><span data-stu-id="3628b-110">DESCRIPTION</span></span>
<span data-ttu-id="3628b-111">建立新的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3628b-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="3628b-112">示例</span><span class="sxs-lookup"><span data-stu-id="3628b-112">EXAMPLES</span></span>

### <span data-ttu-id="3628b-113">範例 1-建立新的 AAD 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3628b-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="3628b-114">建立不含任何認證的新 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3628b-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="3628b-115">範例 2-使用密碼建立新的 AAD 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3628b-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="3628b-116">建立新的 azure active directory 應用程式，並將密碼認證與它相關聯。</span><span class="sxs-lookup"><span data-stu-id="3628b-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="3628b-117">參數</span><span class="sxs-lookup"><span data-stu-id="3628b-117">PARAMETERS</span></span>

### <span data-ttu-id="3628b-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="3628b-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="3628b-119">指定應用程式是單一租使用者還是多租使用者的值。</span><span class="sxs-lookup"><span data-stu-id="3628b-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3628b-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="3628b-120">-CertValue</span></span>
<span data-ttu-id="3628b-121">"未對稱" 憑證類型的值。</span><span class="sxs-lookup"><span data-stu-id="3628b-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="3628b-122">它代表基64編碼證書。</span><span class="sxs-lookup"><span data-stu-id="3628b-122">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3628b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3628b-123">-DefaultProfile</span></span>
<span data-ttu-id="3628b-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3628b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3628b-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3628b-125">-DisplayName</span></span>
<span data-ttu-id="3628b-126">新應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3628b-126">Display name of the new application.</span></span>

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

### <span data-ttu-id="3628b-127">-結束日期</span><span class="sxs-lookup"><span data-stu-id="3628b-127">-EndDate</span></span>
<span data-ttu-id="3628b-128">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="3628b-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="3628b-129">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="3628b-129">The default end date value is one year from today.</span></span> <span data-ttu-id="3628b-130">針對 "不對稱" 類型認證，必須將它設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="3628b-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3628b-131">-首頁</span><span class="sxs-lookup"><span data-stu-id="3628b-131">-HomePage</span></span>
<span data-ttu-id="3628b-132">應用程式首頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="3628b-132">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="3628b-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="3628b-133">-IdentifierUris</span></span>
<span data-ttu-id="3628b-134">識別應用程式的 Uri。</span><span class="sxs-lookup"><span data-stu-id="3628b-134">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3628b-135">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="3628b-135">-KeyCredentials</span></span>
<span data-ttu-id="3628b-136">與應用程式相關聯的憑證認證清單。</span><span class="sxs-lookup"><span data-stu-id="3628b-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3628b-137">-Password</span><span class="sxs-lookup"><span data-stu-id="3628b-137">-Password</span></span>
<span data-ttu-id="3628b-138">要與應用程式相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="3628b-138">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3628b-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="3628b-139">-PasswordCredentials</span></span>
<span data-ttu-id="3628b-140">與應用程式相關聯的密碼認證清單。</span><span class="sxs-lookup"><span data-stu-id="3628b-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3628b-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="3628b-141">-ReplyUrls</span></span>
<span data-ttu-id="3628b-142">應用程式回復 url。</span><span class="sxs-lookup"><span data-stu-id="3628b-142">The application reply urls.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3628b-143">-開始日期</span><span class="sxs-lookup"><span data-stu-id="3628b-143">-StartDate</span></span>
<span data-ttu-id="3628b-144">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="3628b-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="3628b-145">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="3628b-145">The default start date value is today.</span></span> <span data-ttu-id="3628b-146">針對 "不對稱" 類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證有效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="3628b-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3628b-147">-確認</span><span class="sxs-lookup"><span data-stu-id="3628b-147">-Confirm</span></span>
<span data-ttu-id="3628b-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3628b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3628b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3628b-149">-WhatIf</span></span>
<span data-ttu-id="3628b-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3628b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3628b-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3628b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3628b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3628b-152">CommonParameters</span></span>
<span data-ttu-id="3628b-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3628b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3628b-154">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3628b-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3628b-155">輸入</span><span class="sxs-lookup"><span data-stu-id="3628b-155">INPUTS</span></span>

### <span data-ttu-id="3628b-156">System.object</span><span class="sxs-lookup"><span data-stu-id="3628b-156">System.String</span></span>

### <span data-ttu-id="3628b-157">System.object []</span><span class="sxs-lookup"><span data-stu-id="3628b-157">System.String[]</span></span>

### <span data-ttu-id="3628b-158">System.object</span><span class="sxs-lookup"><span data-stu-id="3628b-158">System.Boolean</span></span>

### <span data-ttu-id="3628b-159">PSADPasswordCredential [] Microsoft.Azure.Graph.RBAC.Version1_6</span><span class="sxs-lookup"><span data-stu-id="3628b-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="3628b-160">PSADKeyCredential [] Microsoft.Azure.Graph.RBAC.Version1_6</span><span class="sxs-lookup"><span data-stu-id="3628b-160">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="3628b-161">SecureString</span><span class="sxs-lookup"><span data-stu-id="3628b-161">System.Security.SecureString</span></span>

### <span data-ttu-id="3628b-162">System.object</span><span class="sxs-lookup"><span data-stu-id="3628b-162">System.DateTime</span></span>

## <span data-ttu-id="3628b-163">輸出</span><span class="sxs-lookup"><span data-stu-id="3628b-163">OUTPUTS</span></span>

### <span data-ttu-id="3628b-164">Microsoft.Azure.Graph.RBAC.Version1_6 PSADApplication</span><span class="sxs-lookup"><span data-stu-id="3628b-164">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="3628b-165">筆記</span><span class="sxs-lookup"><span data-stu-id="3628b-165">NOTES</span></span>
<span data-ttu-id="3628b-166">關鍵字： azure，Az，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="3628b-166">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3628b-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="3628b-167">RELATED LINKS</span></span>

[<span data-ttu-id="3628b-168">移除-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="3628b-168">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="3628b-169">AzADApplication</span><span class="sxs-lookup"><span data-stu-id="3628b-169">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="3628b-170">新-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3628b-170">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="3628b-171">AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3628b-171">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="3628b-172">新-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3628b-172">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="3628b-173">移除-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3628b-173">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
