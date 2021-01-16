---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: f6344590828663a0cf44d96d6fe733adff8757c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435422"
---
# <span data-ttu-id="c19cf-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c19cf-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="c19cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c19cf-102">SYNOPSIS</span></span>
<span data-ttu-id="c19cf-103">從應用程式移除認證。</span><span class="sxs-lookup"><span data-stu-id="c19cf-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="c19cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="c19cf-104">SYNTAX</span></span>

### <span data-ttu-id="c19cf-105">ApplicationObjectIdWithKeyIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c19cf-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c19cf-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c19cf-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c19cf-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c19cf-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c19cf-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c19cf-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c19cf-109">說明</span><span class="sxs-lookup"><span data-stu-id="c19cf-109">DESCRIPTION</span></span>
<span data-ttu-id="c19cf-110">Remove-AzADAppCredential Cmdlet 可以用來從應用程式中移除認證金鑰（如果遭到破壞或認證金鑰滾動更新到期的部分）。</span><span class="sxs-lookup"><span data-stu-id="c19cf-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="c19cf-111">應用程式是透過提供物件識別碼或 AppId 來識別。</span><span class="sxs-lookup"><span data-stu-id="c19cf-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="c19cf-112">要移除的認證是由其金鑰識別碼來識別。</span><span class="sxs-lookup"><span data-stu-id="c19cf-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="c19cf-113">示例</span><span class="sxs-lookup"><span data-stu-id="c19cf-113">EXAMPLES</span></span>

### <span data-ttu-id="c19cf-114">範例1：從應用程式移除特定認證</span><span class="sxs-lookup"><span data-stu-id="c19cf-114">Example 1: Remove a specific credential from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="c19cf-115">從具有物件 id ' 09534157ebb」的應用程式中移除具有金鑰識別碼 ' 9044423a-60a3-45ac-9ab1-7663d3fb-6f86-4352-9e6d-cf9d50d5ee82」的認證。</span><span class="sxs-lookup"><span data-stu-id="c19cf-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="c19cf-116">範例2：移除應用程式的所有認證</span><span class="sxs-lookup"><span data-stu-id="c19cf-116">Example 2: Remove all credentials from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="c19cf-117">從應用程式 id ' 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58」移除應用程式的所有認證。</span><span class="sxs-lookup"><span data-stu-id="c19cf-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="c19cf-118">範例3：使用管道移除所有認證</span><span class="sxs-lookup"><span data-stu-id="c19cf-118">Example 3: Remove all credentials using piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="c19cf-119">取得含有 Remove-AzADAppCredential Cmdlet 之物件識別碼 ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82」和管道的應用程式，並移除該應用程式的所有認證。</span><span class="sxs-lookup"><span data-stu-id="c19cf-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="c19cf-120">參數</span><span class="sxs-lookup"><span data-stu-id="c19cf-120">PARAMETERS</span></span>

### <span data-ttu-id="c19cf-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c19cf-121">-ApplicationId</span></span>
<span data-ttu-id="c19cf-122">要從中移除認證的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="c19cf-122">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c19cf-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="c19cf-123">-ApplicationObject</span></span>
<span data-ttu-id="c19cf-124">要從中移除認證的應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="c19cf-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c19cf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c19cf-125">-DefaultProfile</span></span>
<span data-ttu-id="c19cf-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c19cf-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c19cf-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c19cf-127">-DisplayName</span></span>
<span data-ttu-id="c19cf-128">應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c19cf-128">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c19cf-129">-Force</span><span class="sxs-lookup"><span data-stu-id="c19cf-129">-Force</span></span>
<span data-ttu-id="c19cf-130">切換到 [刪除認證] 而不需確認。</span><span class="sxs-lookup"><span data-stu-id="c19cf-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="c19cf-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="c19cf-131">-KeyId</span></span>
<span data-ttu-id="c19cf-132">指定要移除的認證金鑰。</span><span class="sxs-lookup"><span data-stu-id="c19cf-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="c19cf-133">應用程式的索引鍵識別碼可以使用 Get-AzADAppCredential Cmdlet 取得。</span><span class="sxs-lookup"><span data-stu-id="c19cf-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c19cf-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c19cf-134">-ObjectId</span></span>
<span data-ttu-id="c19cf-135">要從中移除認證之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="c19cf-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c19cf-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c19cf-136">-PassThru</span></span>
<span data-ttu-id="c19cf-137">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="c19cf-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c19cf-138">-確認</span><span class="sxs-lookup"><span data-stu-id="c19cf-138">-Confirm</span></span>
<span data-ttu-id="c19cf-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c19cf-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c19cf-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c19cf-140">-WhatIf</span></span>
<span data-ttu-id="c19cf-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c19cf-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c19cf-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c19cf-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c19cf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c19cf-143">CommonParameters</span></span>
<span data-ttu-id="c19cf-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c19cf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c19cf-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c19cf-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c19cf-146">輸入</span><span class="sxs-lookup"><span data-stu-id="c19cf-146">INPUTS</span></span>

### <span data-ttu-id="c19cf-147">System.object</span><span class="sxs-lookup"><span data-stu-id="c19cf-147">System.String</span></span>

### <span data-ttu-id="c19cf-148">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="c19cf-148">System.Guid</span></span>

### <span data-ttu-id="c19cf-149">PSADApplication （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="c19cf-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="c19cf-150">輸出</span><span class="sxs-lookup"><span data-stu-id="c19cf-150">OUTPUTS</span></span>

### <span data-ttu-id="c19cf-151">System.object</span><span class="sxs-lookup"><span data-stu-id="c19cf-151">System.Boolean</span></span>

## <span data-ttu-id="c19cf-152">筆記</span><span class="sxs-lookup"><span data-stu-id="c19cf-152">NOTES</span></span>

## <span data-ttu-id="c19cf-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="c19cf-153">RELATED LINKS</span></span>

[<span data-ttu-id="c19cf-154">AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c19cf-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="c19cf-155">新-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c19cf-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="c19cf-156">AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c19cf-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)