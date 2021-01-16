---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 22acfc03afa4758c44d6c6f02ac1d734c90a806b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273895"
---
# <span data-ttu-id="6cace-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="6cace-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="6cace-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6cace-102">SYNOPSIS</span></span>
<span data-ttu-id="6cace-103">列出指定範圍內的 Azure RBAC 拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="6cace-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="6cace-104">根據預設，會列出所選 Azure 訂閱中的所有拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="6cace-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="6cace-105">使用個別的參數，將 [拒絕作業] 指派給特定的使用者，或列出特定資源群組或資源上的 [拒絕作業]。</span><span class="sxs-lookup"><span data-stu-id="6cace-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="6cace-106">句法</span><span class="sxs-lookup"><span data-stu-id="6cace-106">SYNTAX</span></span>

### <span data-ttu-id="6cace-107">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6cace-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cace-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-108">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cace-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cace-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cace-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cace-112">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-112">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cace-113">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-113">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cace-114">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-114">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cace-115">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-115">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cace-116">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-116">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cace-117">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-117">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cace-118">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-118">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cace-119">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-119">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cace-120">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-120">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cace-121">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-121">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cace-122">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-122">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cace-123">DenyAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-123">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -Id <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cace-124">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cace-124">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -DenyAssignmentName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cace-125">說明</span><span class="sxs-lookup"><span data-stu-id="6cace-125">DESCRIPTION</span></span>
<span data-ttu-id="6cace-126">使用 Get-AzDenyAssignment 命令來列出所有在範圍中都有效的拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="6cace-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="6cace-127">如果沒有任何參數，這個命令會傳回在訂閱下所做的所有拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="6cace-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="6cace-128">您可以使用 [本金] 的篩選參數、[拒絕作業名稱和範圍] 來篩選這個清單。</span><span class="sxs-lookup"><span data-stu-id="6cace-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="6cace-129">若要指定使用者，請使用 SignInName 或 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="6cace-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="6cace-130">若要指定安全性群組，請使用 Azure AD ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="6cace-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="6cace-131">若要指定 Azure AD 應用程式，請使用 ServicePrincipalName 或 ObjectId 參數。</span><span class="sxs-lookup"><span data-stu-id="6cace-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="6cace-132">可能會指定存取權遭到拒絕的範圍。</span><span class="sxs-lookup"><span data-stu-id="6cace-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="6cace-133">預設為選取的訂閱。</span><span class="sxs-lookup"><span data-stu-id="6cace-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="6cace-134">可使用下列其中一個參數組合來指定拒絕作業的範圍。</span><span class="sxs-lookup"><span data-stu-id="6cace-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="6cace-135">範圍-這是從/subscriptions/開始的完整限定範圍 \<subscriptionId\> 。</span><span class="sxs-lookup"><span data-stu-id="6cace-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="6cace-136">這將會篩選在該特定範圍中有效的拒絕作業，亦即，在該範圍及上述全部拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="6cace-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="6cace-137">乙.</span><span class="sxs-lookup"><span data-stu-id="6cace-137">b.</span></span>
<span data-ttu-id="6cace-138">ResourceGroupName-訂閱下任何資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6cace-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="6cace-139">這將會在指定的資源群組上篩選指派，亦即在該範圍及更上方的所有拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="6cace-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="6cace-140">c-clip.</span><span class="sxs-lookup"><span data-stu-id="6cace-140">c.</span></span>
<span data-ttu-id="6cace-141">[資源 ResourceGroupName]、[ResourceType]、[] 和 [ (] （選擇性）) ParentResource-識別訂閱下的特定資源，並且將在該資源範圍內篩選拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="6cace-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="6cace-142">若要判斷對訂閱中的特定使用者所拒絕的存取權，請使用 ExpandPrincipalGroups 開關。</span><span class="sxs-lookup"><span data-stu-id="6cace-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="6cace-143">這會列出指派給該使用者的所有拒絕作業，以及該使用者所屬的群組。</span><span class="sxs-lookup"><span data-stu-id="6cace-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="6cace-144">示例</span><span class="sxs-lookup"><span data-stu-id="6cace-144">EXAMPLES</span></span>

### <span data-ttu-id="6cace-145">範例1</span><span class="sxs-lookup"><span data-stu-id="6cace-145">Example 1</span></span>

<span data-ttu-id="6cace-146">列出訂閱中的所有拒絕作業</span><span class="sxs-lookup"><span data-stu-id="6cace-146">List all deny assignments in the subscription</span></span>

```
PS C:\> Get-AzDenyAssignment
Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  All Principals
                          ObjectType:   SystemDefined
                          ObjectId:     00000000-0000-0000-0000-000000000000
                          }
ExcludePrincipals       : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="6cace-147">範例2</span><span class="sxs-lookup"><span data-stu-id="6cace-147">Example 2</span></span>

<span data-ttu-id="6cace-148">取得在範圍 testRG 及更新版本中對使用者所做的全部拒絕作業 john.doe@contoso.com 。</span><span class="sxs-lookup"><span data-stu-id="6cace-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

```
PS C:\> Get-AzDenyAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com

Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="6cace-149">範例3</span><span class="sxs-lookup"><span data-stu-id="6cace-149">Example 3</span></span>

<span data-ttu-id="6cace-150">取得指定服務主體的全部拒絕作業</span><span class="sxs-lookup"><span data-stu-id="6cace-150">Gets all deny assignments of the specified service principal</span></span>

```
PS C:\> Get-AzDenyAssignment -ServicePrincipalName 'http://testapp1.com'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="6cace-151">範例4</span><span class="sxs-lookup"><span data-stu-id="6cace-151">Example 4</span></span>

<span data-ttu-id="6cace-152">取得「site1」網站範圍的拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="6cace-152">Gets deny assignments at the 'site1' website scope.</span></span>

```
PS C:\> Get-AzDenyAssignment -Scope '/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/testRG/providers/Microsoft.Web/sites/site1'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

## <span data-ttu-id="6cace-153">參數</span><span class="sxs-lookup"><span data-stu-id="6cace-153">PARAMETERS</span></span>

### <span data-ttu-id="6cace-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cace-154">-DefaultProfile</span></span>
<span data-ttu-id="6cace-155">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6cace-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cace-156">-DenyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="6cace-156">-DenyAssignmentName</span></span>
<span data-ttu-id="6cace-157">拒絕作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="6cace-157">Name of the deny assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: DenyAssignmentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cace-158">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="6cace-158">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="6cace-159">如果已指定，則會傳回直接指派給使用者的拒絕作業，以及使用者是其成員 (可) 的群組。</span><span class="sxs-lookup"><span data-stu-id="6cace-159">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="6cace-160">僅支援使用者主體。</span><span class="sxs-lookup"><span data-stu-id="6cace-160">Supported only for a user principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cace-161">-識別碼</span><span class="sxs-lookup"><span data-stu-id="6cace-161">-Id</span></span>
<span data-ttu-id="6cace-162">拒絕作業 id。</span><span class="sxs-lookup"><span data-stu-id="6cace-162">Deny assignment id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: DenyAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cace-163">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6cace-163">-ObjectId</span></span>
<span data-ttu-id="6cace-164">使用者、群組或服務主體的 Azure AD ObjectId。</span><span class="sxs-lookup"><span data-stu-id="6cace-164">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="6cace-165">篩選對指定主體所做的所有拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="6cace-165">Filters all deny assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cace-166">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="6cace-166">-ParentResource</span></span>
<span data-ttu-id="6cace-167">使用 [資源數] 參數指定之資源階層中的父資源。</span><span class="sxs-lookup"><span data-stu-id="6cace-167">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="6cace-168">必須與 ResourceGroupName、ResourceType 和 CoNtext.resourcename 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="6cace-168">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cace-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cace-169">-ResourceGroupName</span></span>
<span data-ttu-id="6cace-170">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6cace-170">The resource group name.</span></span>
<span data-ttu-id="6cace-171">列出在指定資源群組中生效的 [拒絕作業]。</span><span class="sxs-lookup"><span data-stu-id="6cace-171">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="6cace-172">當與 [資源清單]、[ResourceType] 和 [ParentResource] 參數搭配使用時，命令會列出 [拒絕作業] 在資源群組中的資源生效。</span><span class="sxs-lookup"><span data-stu-id="6cace-172">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cace-173">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="6cace-173">-ResourceName</span></span>
<span data-ttu-id="6cace-174">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6cace-174">The resource name.</span></span>
<span data-ttu-id="6cace-175">例如 storageaccountprod。</span><span class="sxs-lookup"><span data-stu-id="6cace-175">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="6cace-176">必須與 ResourceGroupName、ResourceType 及 (（選擇性）) ParentResource 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="6cace-176">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cace-177">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6cace-177">-ResourceType</span></span>
<span data-ttu-id="6cace-178">資源類型。</span><span class="sxs-lookup"><span data-stu-id="6cace-178">The resource type.</span></span>
<span data-ttu-id="6cace-179">例如，. Network/virtualNetworks。</span><span class="sxs-lookup"><span data-stu-id="6cace-179">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="6cace-180">必須與 ResourceGroupName、和 (（選擇性) ParentResource 參數）搭配使用。</span><span class="sxs-lookup"><span data-stu-id="6cace-180">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cace-181">-範圍</span><span class="sxs-lookup"><span data-stu-id="6cace-181">-Scope</span></span>
<span data-ttu-id="6cace-182">角色指派的範圍。</span><span class="sxs-lookup"><span data-stu-id="6cace-182">The Scope of the role assignment.</span></span>
<span data-ttu-id="6cace-183">相對 URI 的格式。</span><span class="sxs-lookup"><span data-stu-id="6cace-183">In the format of relative URI.</span></span>
<span data-ttu-id="6cace-184">例如/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG。</span><span class="sxs-lookup"><span data-stu-id="6cace-184">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="6cace-185">其開頭必須是 "/subscriptions/{id}"。</span><span class="sxs-lookup"><span data-stu-id="6cace-185">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="6cace-186">此命令會篩選在該範圍內生效的所有拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="6cace-186">The command filters all deny assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, DenyAssignmentIdParameterSet, DenyAssignmentNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cace-187">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="6cace-187">-ServicePrincipalName</span></span>
<span data-ttu-id="6cace-188">服務主體的 ServicePrincipalName。</span><span class="sxs-lookup"><span data-stu-id="6cace-188">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="6cace-189">篩選對指定的 Azure AD 應用程式所做的所有拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="6cace-189">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cace-190">-SignInName</span><span class="sxs-lookup"><span data-stu-id="6cace-190">-SignInName</span></span>
<span data-ttu-id="6cace-191">使用者的電子郵件地址或使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="6cace-191">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="6cace-192">篩選對指定使用者所做的所有拒絕作業。</span><span class="sxs-lookup"><span data-stu-id="6cace-192">Filters all deny assignments that are made to the specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cace-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cace-193">CommonParameters</span></span>
<span data-ttu-id="6cace-194">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6cace-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cace-195">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6cace-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cace-196">輸入</span><span class="sxs-lookup"><span data-stu-id="6cace-196">INPUTS</span></span>

### <span data-ttu-id="6cace-197">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="6cace-197">System.Guid</span></span>

### <span data-ttu-id="6cace-198">System.object</span><span class="sxs-lookup"><span data-stu-id="6cace-198">System.String</span></span>

## <span data-ttu-id="6cace-199">輸出</span><span class="sxs-lookup"><span data-stu-id="6cace-199">OUTPUTS</span></span>

### <span data-ttu-id="6cace-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="6cace-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="6cace-201">筆記</span><span class="sxs-lookup"><span data-stu-id="6cace-201">NOTES</span></span>
<span data-ttu-id="6cace-202">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="6cace-202">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="6cace-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="6cace-203">RELATED LINKS</span></span>