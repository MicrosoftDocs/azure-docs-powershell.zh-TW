---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 0dc49732a6e6ad614a0330c3fe24b412be898a54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620898"
---
# <span data-ttu-id="78408-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="78408-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="78408-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78408-102">SYNOPSIS</span></span>
<span data-ttu-id="78408-103">篩選 active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="78408-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="78408-104">句法</span><span class="sxs-lookup"><span data-stu-id="78408-104">SYNTAX</span></span>

### <span data-ttu-id="78408-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="78408-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="78408-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="78408-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="78408-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="78408-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="78408-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78408-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="78408-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78408-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="78408-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78408-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="78408-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="78408-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="78408-112">說明</span><span class="sxs-lookup"><span data-stu-id="78408-112">DESCRIPTION</span></span>
<span data-ttu-id="78408-113">篩選 active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="78408-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="78408-114">示例</span><span class="sxs-lookup"><span data-stu-id="78408-114">EXAMPLES</span></span>

### <span data-ttu-id="78408-115">範例 1-清單廣告服務原則</span><span class="sxs-lookup"><span data-stu-id="78408-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="78408-116">列出租使用者中的所有廣告服務主體。</span><span class="sxs-lookup"><span data-stu-id="78408-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="78408-117">範例 2-使用分頁來列出廣告服務主體</span><span class="sxs-lookup"><span data-stu-id="78408-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="78408-118">列出租使用者中的第一個 100 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="78408-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="78408-119">範例3：依 SPN 列出服務主體</span><span class="sxs-lookup"><span data-stu-id="78408-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="78408-120">列出 SPN 為「36f81fc3-b00f-48cd-8218-3879f51ff39f」的服務主體。</span><span class="sxs-lookup"><span data-stu-id="78408-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="78408-121">範例4：依搜尋字串列出服務主體</span><span class="sxs-lookup"><span data-stu-id="78408-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="78408-122">列出顯示名稱以 "Web" 開頭的所有廣告服務主體。</span><span class="sxs-lookup"><span data-stu-id="78408-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="78408-123">範例5：依管道列出服務主體</span><span class="sxs-lookup"><span data-stu-id="78408-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="78408-124">取得物件 id 為 "39e64ec6-569b-4030-8e1c-c3c519a05d69" 的 AD 應用程式，並將其管道至 Get-AzADServicePrincipal Cmdlet，以列出該應用程式的所有服務主體。</span><span class="sxs-lookup"><span data-stu-id="78408-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="78408-125">參數</span><span class="sxs-lookup"><span data-stu-id="78408-125">PARAMETERS</span></span>

### <span data-ttu-id="78408-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="78408-126">-ApplicationId</span></span>
<span data-ttu-id="78408-127">服務主體應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="78408-127">The service principal application id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78408-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="78408-128">-ApplicationObject</span></span>
<span data-ttu-id="78408-129">要檢索其服務主體的應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="78408-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78408-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78408-130">-DefaultProfile</span></span>
<span data-ttu-id="78408-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="78408-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78408-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="78408-132">-DisplayName</span></span>
<span data-ttu-id="78408-133">服務主體顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="78408-133">The service principal display name.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78408-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="78408-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="78408-135">服務主體搜尋字串。</span><span class="sxs-lookup"><span data-stu-id="78408-135">The service principal search string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78408-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="78408-136">-ObjectId</span></span>
<span data-ttu-id="78408-137">服務主體的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="78408-137">Object id of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78408-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="78408-138">-ServicePrincipalName</span></span>
<span data-ttu-id="78408-139">服務的 SPN。</span><span class="sxs-lookup"><span data-stu-id="78408-139">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78408-140">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="78408-140">-IncludeTotalCount</span></span>
<span data-ttu-id="78408-141">報告資料集中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="78408-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="78408-142">這個參數目前不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="78408-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="78408-143">-略過</span><span class="sxs-lookup"><span data-stu-id="78408-143">-Skip</span></span>
<span data-ttu-id="78408-144">忽略前 N 個物件，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="78408-144">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78408-145">-優先</span><span class="sxs-lookup"><span data-stu-id="78408-145">-First</span></span>
<span data-ttu-id="78408-146">要傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="78408-146">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78408-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78408-147">CommonParameters</span></span>
<span data-ttu-id="78408-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78408-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78408-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78408-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78408-150">輸入</span><span class="sxs-lookup"><span data-stu-id="78408-150">INPUTS</span></span>

### <span data-ttu-id="78408-151">System.object</span><span class="sxs-lookup"><span data-stu-id="78408-151">System.String</span></span>

### <span data-ttu-id="78408-152">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="78408-152">System.Guid</span></span>

### <span data-ttu-id="78408-153">PSADApplication （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="78408-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="78408-154">輸出</span><span class="sxs-lookup"><span data-stu-id="78408-154">OUTPUTS</span></span>

### <span data-ttu-id="78408-155">PSADServicePrincipal （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="78408-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="78408-156">筆記</span><span class="sxs-lookup"><span data-stu-id="78408-156">NOTES</span></span>

## <span data-ttu-id="78408-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="78408-157">RELATED LINKS</span></span>

[<span data-ttu-id="78408-158">新-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="78408-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="78408-159">Set-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="78408-159">Set-AzADServicePrincipal</span></span>](./Set-AzADServicePrincipal.md)

[<span data-ttu-id="78408-160">移除-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="78408-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="78408-161">AzADApplication</span><span class="sxs-lookup"><span data-stu-id="78408-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="78408-162">AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="78408-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)
