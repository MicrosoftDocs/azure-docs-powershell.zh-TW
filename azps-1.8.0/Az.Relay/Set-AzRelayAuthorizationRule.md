---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
ms.openlocfilehash: ed95b9aa2e914d8f7c37132c372c4c1acaeafca1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620934"
---
# <span data-ttu-id="1dc8c-101">Set-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1dc8c-101">Set-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="1dc8c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1dc8c-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc8c-103">針對指定的中繼實體 (Namespace/WcfRelay/HybridConnection) 更新指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1dc8c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1dc8c-104">SYNTAX</span></span>

### <span data-ttu-id="1dc8c-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1dc8c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc8c-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1dc8c-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc8c-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1dc8c-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc8c-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1dc8c-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1dc8c-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="1dc8c-109">AuthoRulePropertiesSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dc8c-110">說明</span><span class="sxs-lookup"><span data-stu-id="1dc8c-110">DESCRIPTION</span></span>
<span data-ttu-id="1dc8c-111">**AzRelayAuthorizationRule** Cmdlet 會更新指定之中繼實體的特定授權規則的描述， (命名空間/WcfRelay/HybridConnection) 。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-111">The **Set-AzRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="1dc8c-112">示例</span><span class="sxs-lookup"><span data-stu-id="1dc8c-112">EXAMPLES</span></span>

### <span data-ttu-id="1dc8c-113">範例 1.1-具有 InputObject 的命名空間</span><span class="sxs-lookup"><span data-stu-id="1dc8c-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="1dc8c-114">從命名空間中授權規則的存取權利新增 [ **傳送** ] `AuthoRule1` `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="1dc8c-115">範例 1.2-含許可權參數的命名空間</span><span class="sxs-lookup"><span data-stu-id="1dc8c-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="1dc8c-116">從命名空間中授權規則的存取權利新增 [ **傳送** ] `AuthoRule1` `TestNameSpace-Relay1` 。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="1dc8c-117">範例 2.1-使用 InputObject WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1dc8c-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="1dc8c-118">將 [ **傳送** ] 新增至 WcfRelay 授權規則的存取權 `AuthoRule1` `TestWCFRelay1` 。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="1dc8c-119">範例 2.2-使用許可權參數 WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1dc8c-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="1dc8c-120">將 [ **傳送** ] 新增至 WcfRelay 授權規則的存取權 `AuthoRule1` `TestWCFRelay1` 。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="1dc8c-121">範例 3.1-使用 InputObject HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1dc8c-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="1dc8c-122">將 [ **傳送** ] 新增至 HybridConnection 授權規則的存取權 `AuthoRule1` `TestHybridConnection` 。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="1dc8c-123">範例 3.2-使用許可權參數 HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1dc8c-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="1dc8c-124">將 [ **傳送** ] 新增至 HybridConnection 授權規則的存取權 `AuthoRule1` `TestHybridConnection` 。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="1dc8c-125">參數</span><span class="sxs-lookup"><span data-stu-id="1dc8c-125">PARAMETERS</span></span>

### <span data-ttu-id="1dc8c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc8c-126">-DefaultProfile</span></span>
<span data-ttu-id="1dc8c-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dc8c-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="1dc8c-128">-HybridConnection</span></span>
<span data-ttu-id="1dc8c-129">HybridConnection [名稱]。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-129">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc8c-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dc8c-130">-InputObject</span></span>
<span data-ttu-id="1dc8c-131">轉接 AuthorizationRule 物件。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-131">Relay AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc8c-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="1dc8c-132">-Name</span></span>
<span data-ttu-id="1dc8c-133">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-133">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc8c-134">-命名空間</span><span class="sxs-lookup"><span data-stu-id="1dc8c-134">-Namespace</span></span>
<span data-ttu-id="1dc8c-135">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-135">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc8c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc8c-136">-ResourceGroupName</span></span>
<span data-ttu-id="1dc8c-137">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="1dc8c-138">-許可權</span><span class="sxs-lookup"><span data-stu-id="1dc8c-138">-Rights</span></span>
<span data-ttu-id="1dc8c-139">權力，例如 @ ( 「聆聽」、「傳送」、「管理」 ) </span><span class="sxs-lookup"><span data-stu-id="1dc8c-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc8c-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="1dc8c-140">-WcfRelay</span></span>
<span data-ttu-id="1dc8c-141">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-141">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc8c-142">-確認</span><span class="sxs-lookup"><span data-stu-id="1dc8c-142">-Confirm</span></span>
<span data-ttu-id="1dc8c-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dc8c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dc8c-144">-WhatIf</span></span>
<span data-ttu-id="1dc8c-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dc8c-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dc8c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc8c-147">CommonParameters</span></span>
<span data-ttu-id="1dc8c-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc8c-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1dc8c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc8c-150">輸入</span><span class="sxs-lookup"><span data-stu-id="1dc8c-150">INPUTS</span></span>

### <span data-ttu-id="1dc8c-151">System.object</span><span class="sxs-lookup"><span data-stu-id="1dc8c-151">System.String</span></span>

### <span data-ttu-id="1dc8c-152">PSAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1dc8c-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="1dc8c-153">System.object []</span><span class="sxs-lookup"><span data-stu-id="1dc8c-153">System.String[]</span></span>

## <span data-ttu-id="1dc8c-154">輸出</span><span class="sxs-lookup"><span data-stu-id="1dc8c-154">OUTPUTS</span></span>

### <span data-ttu-id="1dc8c-155">PSAuthorizationRuleAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1dc8c-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="1dc8c-156">筆記</span><span class="sxs-lookup"><span data-stu-id="1dc8c-156">NOTES</span></span>

## <span data-ttu-id="1dc8c-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dc8c-157">RELATED LINKS</span></span>