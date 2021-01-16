---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 44f351870e97d227484bd09be1e75b8cb19ac723
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98272999"
---
# <span data-ttu-id="ee00f-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ee00f-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="ee00f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ee00f-102">SYNOPSIS</span></span>
<span data-ttu-id="ee00f-103">取得使用者或使用者。</span><span class="sxs-lookup"><span data-stu-id="ee00f-103">Gets a user or users.</span></span>

## <span data-ttu-id="ee00f-104">句法</span><span class="sxs-lookup"><span data-stu-id="ee00f-104">SYNTAX</span></span>

### <span data-ttu-id="ee00f-105">GeAllUsers (預設) </span><span class="sxs-lookup"><span data-stu-id="ee00f-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee00f-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="ee00f-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee00f-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="ee00f-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee00f-108">說明</span><span class="sxs-lookup"><span data-stu-id="ee00f-108">DESCRIPTION</span></span>
<span data-ttu-id="ee00f-109">如果沒有指定使用者， **AzApiManagementUser** Cmdlet 會取得指定的使用者或所有使用者。</span><span class="sxs-lookup"><span data-stu-id="ee00f-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="ee00f-110">示例</span><span class="sxs-lookup"><span data-stu-id="ee00f-110">EXAMPLES</span></span>

### <span data-ttu-id="ee00f-111">範例1：取得所有使用者</span><span class="sxs-lookup"><span data-stu-id="ee00f-111">Example 1: Get all users</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="ee00f-112">這個命令會取得所有使用者。</span><span class="sxs-lookup"><span data-stu-id="ee00f-112">This command gets all users.</span></span>

### <span data-ttu-id="ee00f-113">範例2：依識別碼取得使用者</span><span class="sxs-lookup"><span data-stu-id="ee00f-113">Example 2: Get a user by ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="ee00f-114">這個命令會透過識別碼取得使用者。</span><span class="sxs-lookup"><span data-stu-id="ee00f-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="ee00f-115">範例3：依姓氏取得使用者</span><span class="sxs-lookup"><span data-stu-id="ee00f-115">Example 3: Get users by last name</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="ee00f-116">這個命令會取得擁有指定姓氏的使用者。</span><span class="sxs-lookup"><span data-stu-id="ee00f-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="ee00f-117">範例4：透過電子郵件地址取得使用者</span><span class="sxs-lookup"><span data-stu-id="ee00f-117">Example 4: Get a user by email address</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="ee00f-118">這個命令會取得擁有指定電子郵件地址的使用者。</span><span class="sxs-lookup"><span data-stu-id="ee00f-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="ee00f-119">範例5：取得群組中的所有使用者</span><span class="sxs-lookup"><span data-stu-id="ee00f-119">Example 5: Get all users within a group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="ee00f-120">這個命令會取得指定群組中的所有使用者。</span><span class="sxs-lookup"><span data-stu-id="ee00f-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="ee00f-121">參數</span><span class="sxs-lookup"><span data-stu-id="ee00f-121">PARAMETERS</span></span>

### <span data-ttu-id="ee00f-122">-內容</span><span class="sxs-lookup"><span data-stu-id="ee00f-122">-Context</span></span>
<span data-ttu-id="ee00f-123">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="ee00f-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="ee00f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee00f-124">-DefaultProfile</span></span>
<span data-ttu-id="ee00f-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee00f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee00f-126">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="ee00f-126">-Email</span></span>
<span data-ttu-id="ee00f-127">指定使用者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="ee00f-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="ee00f-128">如果指定此參數，此 Cmdlet 會透過電子郵件尋找使用者。</span><span class="sxs-lookup"><span data-stu-id="ee00f-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="ee00f-129">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ee00f-129">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee00f-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="ee00f-130">-FirstName</span></span>
<span data-ttu-id="ee00f-131">指定使用者的名字。</span><span class="sxs-lookup"><span data-stu-id="ee00f-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="ee00f-132">如果指定此參數，這個 Cmdlet 會依名字尋找使用者。</span><span class="sxs-lookup"><span data-stu-id="ee00f-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="ee00f-133">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ee00f-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee00f-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="ee00f-134">-GroupId</span></span>
<span data-ttu-id="ee00f-135">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee00f-135">Specifies the group identifier.</span></span>
<span data-ttu-id="ee00f-136">如果已指定，此 Cmdlet 會找出指定群組中的所有使用者。</span><span class="sxs-lookup"><span data-stu-id="ee00f-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="ee00f-137">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ee00f-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee00f-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="ee00f-138">-LastName</span></span>
<span data-ttu-id="ee00f-139">指定使用者的姓氏。</span><span class="sxs-lookup"><span data-stu-id="ee00f-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="ee00f-140">如果已指定，此 Cmdlet 會依姓氏尋找使用者。</span><span class="sxs-lookup"><span data-stu-id="ee00f-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="ee00f-141">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ee00f-141">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee00f-142">-State</span><span class="sxs-lookup"><span data-stu-id="ee00f-142">-State</span></span>
<span data-ttu-id="ee00f-143">指定使用者狀態。</span><span class="sxs-lookup"><span data-stu-id="ee00f-143">Specifies the user state.</span></span>
<span data-ttu-id="ee00f-144">如果已指定，此 Cmdlet 會尋找處於這種狀態的使用者。</span><span class="sxs-lookup"><span data-stu-id="ee00f-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="ee00f-145">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ee00f-145">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: GetByUser
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee00f-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="ee00f-146">-UserId</span></span>
<span data-ttu-id="ee00f-147">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee00f-147">Specifies a user ID.</span></span>
<span data-ttu-id="ee00f-148">如果已指定，此 Cmdlet 會依據此識別碼來尋找使用者。</span><span class="sxs-lookup"><span data-stu-id="ee00f-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="ee00f-149">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ee00f-149">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee00f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee00f-150">CommonParameters</span></span>
<span data-ttu-id="ee00f-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ee00f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee00f-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ee00f-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee00f-153">輸入</span><span class="sxs-lookup"><span data-stu-id="ee00f-153">INPUTS</span></span>

### <span data-ttu-id="ee00f-154">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="ee00f-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ee00f-155">System.object</span><span class="sxs-lookup"><span data-stu-id="ee00f-155">System.String</span></span>

### <span data-ttu-id="ee00f-156">ApiManagement 為 Nullable "1 [PsApiManagementUserState，，ServiceManagement，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））））））</span><span class="sxs-lookup"><span data-stu-id="ee00f-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ee00f-157">輸出</span><span class="sxs-lookup"><span data-stu-id="ee00f-157">OUTPUTS</span></span>

### <span data-ttu-id="ee00f-158">ServiceManagement. PsApiManagementUser （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="ee00f-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="ee00f-159">筆記</span><span class="sxs-lookup"><span data-stu-id="ee00f-159">NOTES</span></span>

## <span data-ttu-id="ee00f-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee00f-160">RELATED LINKS</span></span>

[<span data-ttu-id="ee00f-161">新-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ee00f-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="ee00f-162">移除-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ee00f-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="ee00f-163">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ee00f-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)

